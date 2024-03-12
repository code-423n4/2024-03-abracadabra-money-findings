# Low-Severity

## [L-01] Missing `address(0)` check in `constructor`

Not checking for `address(0)` in the `constructor` could lead to scenarios where the contract is deployed with invalid or uninitialized parameters, which might cause re-deployment or in worst case always set to 0 which can cause undesired behavior or even security vulnerabilities.

### Check `_stakingToken` for `address(0)`

```solidity
File : src/staking/LockingMultiRewards.sol

112:   constructor(
...
135:        stakingToken = _stakingToken;

```

[135](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L135)

### Check `pair_`, `baseOracle_` and `quoteOracle_` for `address(0)`

```solidity
File : src/oracles/aggregators/MagicLpAggregator.sol

21:   constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
22:        pair = pair_;
23:        baseOracle = baseOracle_;
24:        quoteOracle = quoteOracle_;

```

[21-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21C5-L24C36)

## [L-02] The function `_rewardPerToken` appears to be intended for `internal` use within the `contract`

The function `_rewardPerToken` appears to be intended for `internal` use within the contract, as indicated by the leading underscore (`_`). However, it has been mistakenly marked as `public`, which means it is accessible from outside the contract. Fortunately, marking it as `public` with a view modifier doesn't pose any security risks, but it does expose an `internal` function to `external` callers unnecessarily.

```solidity
File : src/staking/LockingMultiRewards.sol

277:    function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

```

[277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277C5-L277C139)

## [L-03] `safeTransfer` doesn't check for `address(0)` before transfer

Since `safeTransfer` doesn't check for address(0) it totally upto the ERC20 contract's `transfer` function definition. Some libraries like solmate ERC20 `transfer` doesn't check for address 0 and amount will be transferred if address 0 passed. So it always better to check for address 0 before transferring tokens to it where safeTransfer/transfer used.

### Check address `to` for `address(0)` in rescue function

```solidity
File : src/mimswap/MagicLP.sol

461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {
            if (token == _BASE_TOKEN_ || token == _QUOTE_TOKEN_) {
            revert ErrNotAllowed();
            }

466:        token.safeTransfer(to, amount);
            emit TokenRescue(token, to, amount);
        }

```

[461-168](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L461C1-L468C6)

### Check address `to` for `address(0)` in \_transferBaseOut function

```solidity
File : src/mimswap/MagicLP.sol

581:    function _transferBaseOut(address to, uint256 amount) internal {
            if (amount > 0) {
583:            _BASE_TOKEN_.safeTransfer(to, amount);
            }
        }

```

[581-585](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L581C1-L585C6)

### Check address `to` for `address(0)`

```solidity
File : src/mimswap/MagicLP.sol

587:    function _transferQuoteOut(address to, uint256 amount) internal {
           if (amount > 0) {
589:            _QUOTE_TOKEN_.safeTransfer(to, amount);
           }
        }

```

[587-591](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L587C1-L591C6)

## [L-04] In `execute` function check `success` for `true/false` when calling low level `call`

If `success` is `false` then revert just after low level call fails immediately is safer approach rather than relying on the caller of this `execute` function, since `execute` is `external` function so it is safe to revert whenever low level `call` failed.

```solidity
File : src/blast/BlastGovernor.sol

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
54:          (success, result) = to.call{value: value}(data);
55:      }

```

[53-55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53C5-L55C6)

## [L-05] Checks Effects Interactions pattern not followed in `LockingMultiRewards::withdraw` function

Updating state var. after external call when state var. is not depends on that call. So it is safe to update it before to follow CEI. To avoid reentrancy possibilities. Although `stakingToken` is immutable and fixed contract lesser chances to reenter still it is best practice to follow CEI as much as possible to avoid any kind of reentrancy.
This issue can be mitigated by following the Checks-Effects-Interactions Pattern which suggests that a smart contract should first do the relevant Checks, then make the relevant internal changes to its state (Effects), and only then interact with other smart contracts which may well be malicious.

```solidity
File : src/staking/LockingMultiRewards.sol

170:    function withdraw(uint256 amount) public virtual {
            if (amount == 0) {
                 revert ErrZeroAmount();
            }

            _updateRewardsForUser(msg.sender);

            _balances[msg.sender].unlocked -= amount;
            unlockedSupply -= amount;

            stakingToken.safeTransfer(msg.sender, amount);
            stakingTokenBalance -= amount; //@audit updating state var. after external call when this is not depends on that call. So it is safe to update it before to follow CEI.

           emit LogWithdrawn(msg.sender, amount);
        }

```

[170-184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L170C1-L184C6)

# Non-Critical

**Note: N-03 covers only those instances which were missed by analyzer.**

## [N-01] Typos

It is always better to write right spellings to improve readability and avoids confusion when writing function or variable names inside contract.

### Wrong spelling `Multipler` in `lockingBoostMultiplerInBips`

```diff
File : src/staking/LockingMultiRewards.sol

-84:     uint256 public immutable lockingBoostMultiplerInBips;
+84:     uint256 public immutable lockingBoostMultiplierInBips;

```

[84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L84)

### Wrong spelling `_udpateUserRewards` function name can create confusion or other logic breaking

```diff
File : src/staking/LockingMultiRewards

-536:    function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
+536:    function _updateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

```

[536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L536)

### Wrong spelling `Nomalized` in `baseAnswerNomalized`

```diff
File : src/oracles/aggregators/MagicLpAggregator.sol

37:    function latestAnswer() public view override returns (int256) {
-38:        uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
+38:        uint256 baseAnswerNormalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
39:         uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
-40:        uint256 minAnswer = baseAnswerNomalized < quoteAnswerNormalized ? baseAnswerNomalized : quoteAnswerNormalized;
+40:        uint256 minAnswer = baseAnswerNormalized < quoteAnswerNormalized ? baseAnswerNormalized : quoteAnswerNormalized;

```

[37-40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L37C1-L40C119)

## [N-02] Change the name of these `locked` and `unlocked` functions

Changing the names of the `locked` and `unlocked` functions to `userLockedBalance` and `userUnlockedBalance`, respectively, makes the purpose of these functions more explicit and understandable. Improves code readability and clarity.

```solidity
File : src/staking/LockingMultiRewards.sol

227:    function locked(address user) external view returns (uint256) {
            return _balances[user].locked;
        }

231:    function unlocked(address user) external view returns (uint256) {
            return _balances[user].unlocked;
        }

```

[227-233](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L227C1-L233C6)

## [N-03] Instead of using magic numbers, use constant (_Note: Instances missed by analyzer_)

By replacing 1e18 with a named constant, you make your code more readable, maintainable, and less prone to errors.

```solidity
File : src/staking/LockingMultiRewards.sol

292:   function _earned(
...
294:     return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];

```

[294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294)

## [N-04] Using `_rewardLock` instead of `_userRewardLock[user]` improves readability and maintains a single flow in the code

By assigning `_userRewardLock[user]` to `_rewardLock` as storage pointer at the beginning of the function, you establish a single point of reference for the reward lock associated with the user. It is better to use `_rewardLock` throughout the function to improve readability. Since both are pointing to same storage variable.

```solidity
File : src/staking/LockingMultiRewards.sol

597:    function _getRewards(address user) internal {
598:        RewardLock storage _rewardLock = _userRewardLock[user];
...

648:      _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));

```

[648](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L648)

## [N-05] In function `rescue` before calling `safeTransfer` check `amount` for `zero`

safeTransfer doesn't check for amount 0. so it better to check that before. Since amount 0 transferring has no effect.

```solidity
File : src/mimswap/MagicLP.sol

461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {
            if (token == _BASE_TOKEN_ || token == _QUOTE_TOKEN_) {
            revert ErrNotAllowed();
            }

466:        token.safeTransfer(to, amount);
            emit TokenRescue(token, to, amount);
        }

```

[461-468](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L461C1-L468C6)

## [N-06] Prepending an underscore (`_`) before internal function names is a convention to visually distinguish them from external or public functions

It is a general convention to use \_ before private/internal function to improve clarity.

```diff
File : src/blast/BlastBox.sol

-103:    function isOwner(address _account) internal view override returns (bool) {
+103:    function _isOwner(address _account) internal view override returns (bool) {

```

[103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L103)

## [N-07] Do not declare named return variables if returned explicitly.

It creates the confusion and reduce readability to use both named return variables and explicit returns. Use one of that method consistently to maintain readability.

```solidity
File : src/blast/BlastOnboardingBoot.sol

78:    function claimable(address user) external view returns (uint256 shares) {
...
83:        return _claimable(user);


86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
89:        return router.previewCreatePool(I, baseAmount, quoteAmount);


155:     function _claimable(address user) internal view returns (uint256 shares) {
...
163:        return (userLocked * totalPoolShares) / totalLocked;

```

[78-83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L78C1-L83C33), [86-89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86C1-L89C69), [155-163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L155C1-L163C61)
