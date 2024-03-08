# [L-01]: Removing supported tokens prevents users from withdrawing tokens from `BlastOnboarding`.

Due to the `onlySupportedTokens(token)` modifier, if the owner removes support for tokens, users can no longer withdraw their tokens and their funds will get stuck in the `BlastOnboarding`

Consider removing `onlySupportedTokens(token)` modifier for withdrawals.

[BlastOnboarding.sol#L132-L141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132-L141)
```solidity
    function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
        balances[msg.sender][token].unlocked -= amount;
        balances[msg.sender][token].total -= amount;
        totals[token].unlocked -= amount;
        totals[token].total -= amount;

        token.safeTransfer(msg.sender, amount);

        emit LogWithdraw(msg.sender, token, amount);
    }
```

## [R-01] Consider a clearer naming for the maximum boost multiplier that can be set in basis points

The `BIPS` variable caps the maximum boost multiplier at 100%. It could do well to be renamed to `MAX_BIPS` for better code readability.

- (LockingMultiRewards.sol#L78)[https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L78]

```diff
- uint256 private constant BIPS = 10_000;
+ uint256 private constant MAX_BIPS = 10_000;
```

## [N-01] Typo in the `_udpateUserRewards` function naming
As can be seen from the title of this log and in the codebase, the function to update user rewards has a typo and should be corrected.

- (LockingMultiRewards.sol#L536-L539)[https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L536-L539]

```js
function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
    rewards[user_][token_] = _earned(user_, balance_, token_, rewardPerToken_);
    userRewardPerTokenPaid[user_][token_] = rewardPerToken_;
}
```

```diff
- function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
+ function _updateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
    rewards[user_][token_] = _earned(user_, balance_, token_, rewardPerToken_);
    userRewardPerTokenPaid[user_][token_] = rewardPerToken_;
}
```