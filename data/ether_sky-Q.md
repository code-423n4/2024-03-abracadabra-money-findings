**[L-1] Disable the `stakeFor` function when the `system` is `paused`.**
-

In the `LockingMultiRewards` contract, users cannot `stake` when the system is `paused`.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L150
```
function stake(uint256 amount, bool lock_) public whenNotPaused {
    _stakeFor(msg.sender, amount, lock_);
}
```
Additionally, users cannot lock already deposited tokens when the `system` is `paused`.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L155
```
function lock(uint256 amount) public whenNotPaused {
}
```
All operations should be disabled when the `system` is `paused`.
However, `operators` can still `stake` for other users when the `system` is `paused`.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L349-L351
```
function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {
    _stakeFor(account, amount, lock_);
}
```

Should include the `whenNotPaused` `modifier`.
```
- function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {
+ function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators whenNotPaused  {
    _stakeFor(account, amount, lock_);
}
```

**[L-2] The `cap` can be associated with `locked` tokens in the `BlastOnboarding` contract.**
-

Users cannot `deposit` more tokens than the `cap`. 
I guess the `cap` is intended to `limit` the tokens for creating the initial `MagicLP`.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L114-L116
```
function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
    totals[token].total += amount;

    if (caps[token] > 0 && totals[token].total > caps[token]) {
        revert ErrCapReached();
    }
}
```
There are two types of tokens: `locked` and `unlocked` tokens.
Only the `locked` tokens will be used to create `MagicLP`.
`Unlocked` tokens can be claimed anytime and have no effect on the `pool`.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L132-L141
```
function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
    balances[msg.sender][token].unlocked -= amount;
    balances[msg.sender][token].total -= amount;
    totals[token].unlocked -= amount;
    totals[token].total -= amount;
    token.safeTransfer(msg.sender, amount);
}
```
If the `cap` is set, any malicious user can deposit many `unlocked` tokens and prevent other users from depositing. 
If there are not enough tokens to create a `pool` because of this, the only solution is to increase the `cap`. 
However, this is not a perfect solution.

Please modify `deposit` function.
```
function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
    totals[token].total += amount;

-    if (caps[token] > 0 && totals[token].total > caps[token]) {
+    if (caps[token] > 0 && totals[token].locked > caps[token]) {
        revert ErrCapReached();
    }
}
```
Also modify `lock` function.
```
function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
    balances[msg.sender][token].unlocked -= amount;
    balances[msg.sender][token].locked += amount;
    totals[token].unlocked -= amount;
    totals[token].locked += amount;
+    if (caps[token] > 0 && totals[token].locked > caps[token]) {
+        revert ErrCapReached();
+    }
}
```

**[L-3] The `rounding direction` should be set to `round up` in the `_adjustAddLiquidity` function in the `router` contract**
-

In the `_adjustAddLiquidity` function, all calculations are `rounded down`.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L521-L538
```
function _adjustAddLiquidity(
    address lp,
    uint256 baseInAmount,
    uint256 quoteInAmount
) internal view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount) {
        if (IERC20(lp).totalSupply() == 0) {
            uint256 i = IMagicLP(lp)._I_();
            uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
            baseAdjustedInAmount = shares;
@here:            quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);
        } else {
            if (quoteReserve > 0 && baseReserve > 0) {
                uint256 baseIncreaseRatio = DecimalMath.divFloor(baseInAmount, baseReserve);
                uint256 quoteIncreaseRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);
                if (baseIncreaseRatio <= quoteIncreaseRatio) {
                    baseAdjustedInAmount = baseInAmount;
@here:                    quoteAdjustedInAmount = DecimalMath.mulFloor(quoteReserve, baseIncreaseRatio);
                } else {
                    quoteAdjustedInAmount = quoteInAmount;
@here:                    baseAdjustedInAmount = DecimalMath.mulFloor(baseReserve, quoteIncreaseRatio);
                }
            }
        }
}
```
These adjusted values are exactly what are deposited into the `pool`. 
Generally, in most `protocols`, the deposited token amounts should be `rounded up` in favor of the `protocol` rather than the `users` and such kind of issues have been treated as `medium`.
In short, the `shares` calculation should be `rounded down`, while the token amounts calculation should be `rounded up`.

Also in the `previewCreatePool` function.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L103
```
function previewCreatePool() external pure returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
    quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);
}
```
And in the `previewAddLiquidity` function.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L140
```
function previewAddLiquidity() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
    if (totalSupply == 0) {
        quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);
    }
}
```
Should use `mulCeil` instead of `mulFloor`.

**[L-4] We should check the `totals[token].total` when rescuing tokens in the `BlastOnboarding`.**
-

When rescuing tokens, we only check whether this token is supported.
If it is not a supported token, the `owner` can claim any amounts.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L205-L212
```
function rescue(address token, address to, uint256 amount) external onlyOwner {
    if (supportedTokens[token]) {
        revert ErrNotAllowed();
    }
    token.safeTransfer(to, amount);
    emit LogTokenRescue(token, to, amount);
}
```
There might be a scenario as follows:
`Token A` is initially set as a `supported` token.
Users deposit some amounts.
After some time, this token is set as `unsupported`.
As a result, the owner can claim this token, and therefore users who deposited it cannot `claim` their tokens.

Please add below additional check.
```
function rescue(address token, address to, uint256 amount) external onlyOwner {
+    if (amount > IERC20(token).balanceOf(address(this)) - totals[token].total) revert();
-     if (supportedTokens[token]) {
-         revert ErrNotAllowed();
-     }
    token.safeTransfer(to, amount);
    emit LogTokenRescue(token, to, amount);
}
```
By doing this, the `owner` can claim the donated `supported` tokens also.

