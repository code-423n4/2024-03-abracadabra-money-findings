[L-1] Natspec and Variables Ordering Mismatch

Description:

LockingMultiReward.sol Constructor has a mismatch between the the natspecs and the 
variables ordering

the _owner variable is supposed to be the second variable after _stakingToken 
in the natspec comment, but in the actual order it comes last.

Impact:

this might create a confusion for other devs and auditors reading the code.

Proof of Concept:

```
    /// @dev Constructor
    /// @param _stakingToken The token that is being staked
    /// @param _owner The owner of the contract
    /// @param _lockingBoostMultiplerInBips The multiplier for the locking boost. 30000 means if you stake 100, you get 300 locked
    /// @param _rewardsDuration The duration of the rewards period in seconds, should be 7 days by default.
    /// @param _lockDuration The duration of the lock period in seconds, should be 13 weeks by default.
    constructor(
        address _stakingToken,
        uint256 _lockingBoostMultiplerInBips,
        uint256 _rewardsDuration,
        uint256 _lockDuration,
        address _owner
```


Recommended Mitigation:
change the order of the _owner variable to be the second variable after _stakingToken so it matches the natspec