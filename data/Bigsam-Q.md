# Report on `_rewardPerToken` Function




## Impact
The `_rewardPerToken` function, despite being only utilized for internal logic and calculations within the contract, has been labeled as a public function. This exposes it to external calls and inputs, potentially leading to unexpected contract behaviors. Given the function's critical role in calculating the sensitive value `REWARDPERTOKEN` for fairness and reward distribution, this exposure poses a security risk.

```solidity
    function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
        if (totalSupply_ == 0) {
            return _rewardData[rewardToken].rewardPerTokenStored;
        }

        uint256 timeElapsed = lastTimeRewardApplicable_ - _rewardData[rewardToken].lastUpdateTime;
        uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

        return _rewardData[rewardToken].rewardPerTokenStored + pendingRewardsPerToken;
    }
```


## Proof of Concept
1. The function is currently declared as public, allowing external entities to call it.
2. External calls to this function could manipulate the input logic and inaccurately calculate `REWARDPERTOKEN` by calling the function multiple times with wrong inputs.

### Code Reference
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L277-L286

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L528-L534

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L273-L275


## Tools Used
Manual code analysis.

## Recommended Mitigation Steps
To enhance the security of the contract and protect the critical internal logic implemented in the `_rewardPerToken` function, it is strongly recommended to change the function's visibility to internal. This adjustment ensures that the function can only be called within the current contract or contracts that inherit from it.

Update the function declaration as follows:

```solidity
function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) internal view returns (uint256) {
   
}
```

By making this adjustment, you limit external access to the `_rewardPerToken` function, reducing the risk of unintended manipulation and ensuring the integrity of the sensitive calculations it performs.
