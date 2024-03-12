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

**[L-5] We cannot create the `MagicLP` when the `decimal` of the `quote` token is less than the `decimal` of the `base` token.**
-

When creating the `MagicLP` through the `router`, we validate the `decimals` of the `base` and `quote` tokens. 
In case of `overflow/underflow`, the transaction will be reverted if the `decimal` of the `quote` token is less than the `decimal` of the `base` token.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L598-L605
```
function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {
    if (baseDecimals == 0 || quoteDecimals == 0) {
        revert ErrZeroDecimals();
    }
    if (quoteDecimals - baseDecimals > MAX_BASE_QUOTE_DECIMALS_DIFFERENCE) {
        revert ErrDecimalsDifferenceTooLarge();
    }
}
```
And obviously, `A/B MagicLP` is different from `B/A MagicLP` because the `shares` calculation is based on the `base` token. 
It means that in some cases, we cannot create the necessary `MagicLP` due to `decimals`.

Please modify like below:
```
function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {
    if (baseDecimals == 0 || quoteDecimals == 0) {
        revert ErrZeroDecimals();
    }
-     if (quoteDecimals - baseDecimals > MAX_BASE_QUOTE_DECIMALS_DIFFERENCE) {
+     if (quoteDecimals > MAX_BASE_QUOTE_DECIMALS_DIFFERENCE + baseDecimals || baseDecimals > MAX_BASE_QUOTE_DECIMALS_DIFFERENCE + quoteDecimals ) {
        revert ErrDecimalsDifferenceTooLarge();
    }
}
```

**[L-6] There is no functionality to change the `fee rate model` in the `MagicLP`.**
-

When creating `MagicLP` using the `create` function in the `factory`, we insert `maintainerFeeRateModel` as the `fee rate model`. 
This model will be used to calculate the `maintainer fee` in the `MagicLP`.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L86
```
function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
    IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
}
```
There is a functionality to change `maintainerFeeRateModel` in the `factory`.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L105-L112
```
function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
    if (address(maintainerFeeRateModel_) == address(0)) {
        revert ErrZeroAddress();
    }

    maintainerFeeRateModel = maintainerFeeRateModel_;
    emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);
}
```
This implies that the `maintainerFeeRateModel` will require updating in the `future`.
However, there's currently no functionality within `MagicLP` to modify the `fee rate model`. 
Consequently, existing `MagicLP`s are unable to alter the `fee rate model`.

Please add a functionality to change `fee rate model` in the `MagicLP`.

**[L-7] Ensure to call the `_twapUpdate` function before making any changes to the `reserves`.**
-

There is a `_twapUpdate` function to calculate `cumulative price`.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L545-L558
```
function _twapUpdate() internal {
    uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
    uint32 timeElapsed = blockTimestamp - _BLOCK_TIMESTAMP_LAST_;

    if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
        unchecked {
            _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
        }
    }

    _BLOCK_TIMESTAMP_LAST_ = blockTimestamp;
}
```
Ensure this function is invoked prior to modifying any `reserves`. 
It's crucial to first update the `cumulative price` using the `previous reserves`, then proceed with `reserve` adjustments. 
However, the current process involves calling the `_twapUpdate` function after modifying `reserves`. 
Consequently, the `updated reserves` are multiplied by the `elapsed time`, leading to inaccuracies in the `cumulative price`.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L564
```
function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {
    _BASE_RESERVE_ = baseReserve.toUint112();
    _QUOTE_RESERVE_ = quoteReserve.toUint112();

    _twapUpdate();
}
```
The same for the `_sync` function.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L578
```
function _sync() internal {
    uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
    uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
    ....
    _twapUpdate();
}
```
The same for the `_resetTargetAndReserve` function.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L542
```
function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {
    _twapUpdate();
}
```
Should call `_twapUpdate` function before making changes to the `reserves`.

**[L-8] There might be a loss of funds if users directly `invoke` the `buyShares` function within the `MagicLP`.**
-

In the `buyShares` function, both the `base` and `quote` tokens are deposited in the same `ratio`, and the `shares` are calculated accordingly. 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L397-L400
```
function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
    if (totalSupply() == 0) {
    } else if (baseReserve > 0 && quoteReserve > 0) {
        uint256 baseInputRatio = DecimalMath.divFloor(baseInput, baseReserve);
        uint256 quoteInputRatio = DecimalMath.divFloor(quoteInput, quoteReserve);
        uint256 mintRatio = quoteInputRatio < baseInputRatio ? quoteInputRatio : baseInputRatio;
        shares = DecimalMath.mulFloor(totalSupply(), mintRatio);
    }
}
```
If a user deposits one token in a `higher ratio` than the other, the excess amount cannot be used for calculating `shares`. 
This means users may lose these funds.

To mitigate this risk, there's an `addLiquidity` function in the `router`.
However, it's uncertain what will happen if users directly call this function.

And there is also no `minimum shares check`.
And `transferFrom` is not used to transfer `base` and `quote` tokens from `msg.sender` to this `MagicLP`.
While these approaches may present vulnerabilities, they can be mitigated when these functions including `buyShares` and `sellShares` are called from the `router`, as the `router` performs relevant checks.

Please ensure that these functions can only be invoked from the `router`.

**[L-9] There's no guarantee that the `locked` amounts of `MIM` and `USDB` tokens will exceed specific thresholds when creating a `MagicLP` through `bootstrap`**
-

When creating a `MagicLP` using the `locked` `MIM` and `USDB` tokens, there's no verification performed to ensure that the amounts exceed a certain `threshold`.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L101-L106
```
function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
    uint256 baseAmount = totals[MIM].locked;
    uint256 quoteAmount = totals[USDB].locked;
    MIM.safeApprove(address(router), type(uint256).max);
    USDB.safeApprove(address(router), type(uint256).max);

    (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
}
```
Users may `lock` more `USDB` tokens than `MIM` tokens. 
Since `MIM` is the `base` token, the `totalPoolShares` will be based on the amount of `MIM` tokens. 
If this value is significantly smaller than the amount of `USDB` tokens, the calculation of `claimable shares` for users will be affected by rounding because the `totalPoolShares` are significantly smaller than the `totalLocked` amount.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L155-L165
```
function _claimable(address user) internal view returns (uint256 shares) {
    uint256 totalLocked = totals[MIM].locked + totals[USDB].locked;

    if (totalLocked == 0) {
        return 0;
    }

    uint256 userLocked = balances[user][MIM].locked + balances[user][USDB].locked;
    return (userLocked * totalPoolShares) / totalLocked;
}
```
This can lead to some dust staking tokens being stuck in the `BlastOnboarding` contract.

Please set the `threshold` for the `locked` amounts of `MIM` and `USDB` tokens.

**[L-10] The `minimum value check` should be conducted after adjusting the `reserves` in the `setParameters` function.**
-

In `MagicLP`, when updating the parameters, we perform the `minimum value check` at the beginning of the function.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L480-L482
```
function setParameters(
    address assetTo,
    uint256 newLpFeeRate,
    uint256 newI,
    uint256 newK,
    uint256 baseOutAmount,
    uint256 quoteOutAmount,
    uint256 minBaseReserve,
    uint256 minQuoteReserve
) public nonReentrant onlyImplementationOwner {
    if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
        revert ErrReserveAmountNotEnough();
    }
}
```
In this function, we transfer some `base` and `quote` tokens, rendering this check redundant. 
It should be conducted after reducing the `reserves`.
```
function setParameters(
    address assetTo,
    uint256 newLpFeeRate,
    uint256 newI,
    uint256 newK,
    uint256 baseOutAmount,
    uint256 quoteOutAmount,
    uint256 minBaseReserve,
    uint256 minQuoteReserve
) public nonReentrant onlyImplementationOwner {
-     if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
-         revert ErrReserveAmountNotEnough();
-     }
    _transferBaseOut(assetTo, baseOutAmount);
    _transferQuoteOut(assetTo, quoteOutAmount);
    (uint256 newBaseBalance, uint256 newQuoteBalance) = _resetTargetAndReserve();

+     if (newBaseBalance < minBaseReserve || newQuoteBalance < minQuoteReserve) {
+         revert ErrReserveAmountNotEnough();
+     }

}
```

**[L-11] The `symbols` of the `base` and `quote` tokens should be included in the `symbol` of `MagicLP`**
-

The name of `MagicLP` involves the names of the `base` and `quote` tokens.the 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L155-L157
```
function name() public view override returns (string memory) {
    return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));
}
```
But the `symbol` of `MagicLP` remains constant.
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L159-L161
```
function symbol() public pure override returns (string memory) {
    return "MagicLP";
}
```
It should incorporate the `symbols` of the `base` and `quote` tokens.

**[L-12] In some contracts, there are no functionality to claim `native yield` from `Blast`.**
-

Some contracts, such as `BlastMagicLP`, `BlastBox`, and `BlastOnboarding`, lack functionality for claiming `native yield` from `Blast`.

**[L-13] Users are unable to create `locks` due to the `max locks checks` in the `staking` contract**
-

Only `operators` have the authority to clear the `expired locks` of users using the `processExpiredLocks` function. 
However, even though this function should be called every `reward duration`, users cannot create `locks` when the `maxLocks` is set to `1`(the `reward duration` matches the `lock duration`). 
Users can clear their expired `locks` when they create a `lock` and have already reached the `maximum lock count`.