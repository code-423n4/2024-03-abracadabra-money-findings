# QA Report: Abracadabra Mimswap

## L-01 Unlimited Token Approval to Potentially Malicious Router Contract Allows Draining Contract's assets

**Loc:** https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L103C9-L105C1


BlastOnboardingBoot contract approves the router to spend an unlimited amount of MIN and USDB tokens by setting approval to type(uint256).max. This is an attempt to simplify logic for token spending limits but this introduces a huge risk if contract is compromised. This does not adhere to solidity best practices for setting approvals.

The problem can be seen here

```solidity
MIM.safeApprove(address(router), type(uint256).max);
USDB.safeApprove(address(router), type(uint256).max);
```

In the case of a malicious or compromised router this unlimited approval feature can be abused to drain all of the contract's MIM and USDB token balanaces.

### Impact

Loss of funds 


### Mitigation

A workaround for this is to calculate and approve only necessary amounts for each operation to mitigate risks when router permissions are abused.

```solidity
MIM.safeApprove(address(router), baseAmount);
USDB.safeApprove(address(router), quoteAmount);
```

## L-02 Precision Loss in BlastOnboardingBoot::_claimable function


In `BlastOnboardingBoot::_claimable` function shares are calculated based on locked assets. In the function `userLocked * totalPoolShares` is divided by `totalLocked`. This can potentially lead to precision loss due to how solidity handles integer division.

**Line of code:** https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L155C4-L164C6

```solidity
function _claimable(address user) internal view returns (uint256 shares) {
    uint256 totalLocked = totals[MIM].locked + totals[USDB].locked;
    if (totalLocked == 0) {
        return 0;
    }
    uint256 userLocked = balances[user][MIM].locked + balances[user][USDB].locked;
    return (userLocked * totalPoolShares) / totalLocked;
}
```

Take for instance, if both `totalPoolShares` and `totalLocked` are of similar magnitude the multiplication of `userLocked * totalPoolShares` followed by division by `totalLocked` may not accurately reflect the user's proportion of locked assets due to truncation of decimals. 

### Impact

User receive less shares than they are entitled leading to a flawed distribution mechanism.

### Mitigation

Using a scaling factor when carrying out the calculation should mitigate the issue.

   
```solidity
function _claimable(address user) internal view returns (uint256 shares) {
    uint256 totalLocked = totals[MIM].locked + totals[USDB].locked;
    if (totalLocked == 0) {
        return 0;
    }
    uint256 userLocked = balances[user][MIM].locked + balances[user][USDB].locked;
    // Use a scaling factor to mitigate precision loss
    uint256 scaleFactor = 1e18;
    return (userLocked * totalPoolShares * scaleFactor) / totalLocked / scaleFactor;
}
```


## L-03 Precision Loss Due to Integer Division in `ratioSync` Function

The ratioSync function adjusts the target reserves of base and quote tokens. It recalculates `_BASE_TARGET_` and `_QUOTE_TARGET_` based on the current balances of base and quote tokens held by the contract.

Precision loss can occur in this function in the case where `baseBalance` is less than `_BASE_RESERVE_` or `quoteBalance` is less than `_QUOTE_RESERVE_` . This inaccuracy affects the protocol's ability to maintain proper reserve ratios

**Line of code**: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L571

```solidity
if (baseBalance != _BASE_RESERVE_) {
    _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
    _BASE_RESERVE_ = uint112(baseBalance);
}
if (quoteBalance != _QUOTE_RESERVE_) {
    _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
    _QUOTE_RESERVE_ = uint112(quoteBalance);
}
```

### Mitigation

Multiply numerator by scaling factor before performing the division to preserve precision through the calculation. 

```solidity

uint256 scalingFactor = 10**18; // Example scaling factor

if (baseBalance != _BASE_RESERVE_) {
    _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance * scalingFactor) / uint256(_BASE_RESERVE_) / scalingFactor);
    _BASE_RESERVE_ = uint112(baseBalance);
}
if (quoteBalance != _QUOTE_RESERVE_) {
    _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance * scalingFactor) / uint256(_QUOTE_RESERVE_) / scalingFactor);
    _QUOTE_RESERVE_ = uint112(quoteBalance);
}
```

## L-04 Potential Silent Overflow in `ratioSync` Function Due to Direct Casting

The `ratioSync` function casts `uint256` values directly to `uint112` following arithmetic operations. This is done without explicit overflow checks which is not best practice in solidity. This operation occurs after recalculating `_BASE_TARGET_` and `_QUOTE_TARGET_` based on the current balances of base and quote tokens held by the contract. The function implements an initial check to ensure that `baseBalance` and `quoteBalance` do not exceed `type(uint112).max`, this however, does not guarantee that the results of the subsequent multiplication and division operations will also be within the bounds of `uint112`.

This oversight could lead to silent overflow issues, where values that exceed the maximum representable value of `uint112` (2^112 - 1) are wrapped around, resulting in incorrect and potentially exploitable reserve values being set. This can lead to loss of funds or manipulation of the contract's intended economic mechanisms.

**Line of code:**: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L504
```solidity
_BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
_BASE_RESERVE_ = uint112(baseBalance);

_QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
_QUOTE_RESERVE_ = uint112(quoteBalance);
```

### Mitigation

Add explicit checks to ensure the values do not exceed the `uint112` bounds before casting the results of arithmetic operations to `uint112`

You can achieve this by comparing the result against `type(uint112).max`.

```solidity
// Assuming Solidity >=0.8.0 for built-in overflow checks
uint256 newBaseTarget = (uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_);
require(newBaseTarget <= type(uint112).max, "Overflow in newBaseTarget calculation");
_BASE_TARGET_ = uint112(newBaseTarget);

uint256 newQuoteTarget = (uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_);
require(newQuoteTarget <= type(uint112).max, "Overflow in newQuoteTarget calculation");
_QUOTE_TARGET_ = uint112(newQuoteTarget);
```

## L-05 Incorrect Reward Rate Calculations

In notifyRewardAmount, the line `amount += _remainingRewardTime * reward.rewardRate;` adds the remaining rewards to the new amount being notified based on the current `rewardRate` and the time until the next epoch. This approach has the potential to inaccurately calculate the reward amount due to not properly accounting for the actual remaining rewards if the `rewardRate` was previously updated inaccurately.

**Line of code:** https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L379

```solidity
if (block.timestamp < reward.periodFinish) {
    amount += _remainingRewardTime * reward.rewardRate;
}
```

The calculation assumes that the current `rewardRate` accurately reflects the remaining rewards to be distributed until `periodFinish`. If there was an error in a previous update of `rewardRate`, this calculation will propagate that error.

### Mitigation
Calculate the actual remaining rewards based on the difference between the `rewardPerTokenStored` which represents the accumulated reward per token until the last update and the current accumulated reward per token. 

Add this check to ensure the reward rate calculation does not lead to inaccuracies due to previous state inconsistencies:

```solidity
if (block.timestamp < reward.periodFinish) {
    uint256 remainingRewards = (reward.periodFinish - block.timestamp) * reward.rewardRate;
    amount += remainingRewards;
}


if (amount < _remainingRewardTime) {
    revert ErrNotEnoughReward();
}

reward.rewardRate = amount / _remainingRewardTime;
```
