## [G-01] BlastTokenRegistry CAN BE SET AS IMMUTABLE

**`BlastTokenRegistry public registry` can be set as immutable because:**

- **Single Assignment**: It is assigned only once in the constructor of the BlastOnboarding contract.

- **No Reassignment**: There's no functionality in the contract to reassign registry after it's set in the constructor, which aligns with the immutable variable's restriction of being writable only once.

By using immutable for registry, you save gas on deployment and on every subsequent read of the registry variable.

>BlastTokenRegistry public registry;

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L33-L33

## [G-02] CODE OPTIMIZATION BY USING MAX AND MIN

In Solidity, `type(uint32).max` is a constant expression that evaluates to the maximum value that can be held by a `uint32` data type. Similarly, `type(uint32).min` evaluates to the minimum value, which for unsigned integers is always zero. These are built-in constant expressions provided by the Solidity language for convenience and code clarity.

When you use `2 ** 32`, Solidity computes the power operation at compile time, which results in the same maximum value for a `uint32`. `2**32` can be replaced by `type(uint32).max`; which is more readable and will also save some gas.

***Instances***: 2

>_BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L125-L125

>uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L546-L546

## [G-03] OPTIMIZING MULTIPLE MAPPINGS

Using a struct to combine multiple mappings into a single mapping can bring several benefits to a smart contract's design, particularly in terms of efficiency and gas costs. 

It saves storage slot for the mapping and depending on the circumstances and sizes of types, it can avoid a `Gsset (20000 gas)` per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they fit in the same storage slot.

***Here's an example***:

>mapping(address user => mapping(address token => Balances)) public balances;

**REFACTORING CODE**

>struct TokenBalance {
        address token;
        uint256 balance;
    }
mapping(address => TokenBalance[]) public userBalances;

**Instances**: 3

>mapping(address user => mapping(address token => Balances)) public balances;

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L41-L41

>mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L94-L94

>mapping(address user => mapping(address token => uint256 amount)) public rewards;

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L95-L95

## [G-04] DEFINE CONSTRUCTOR AS PAYABLE

Developers can save around 10 opcodes and some gas if the constructors are defined as payable. This optimization results in fewer opcodes being executed during deployment, leading to lower gas costs.

However, it's essential to consider security implications when making a constructor payable. Receiving Ether during deployment opens up possibilities for attack vectors. Therefore, if you decide to make your constructor payable for gas savings, ensure you thoroughly test your contract's security and consider implementing appropriate safeguards to mitigate potential risks.

**Instances**: 10

>constructor() { BlastPoints.configure(); }

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L7-L9

>constructor(address _owner) Owned(_owner) {}

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12-L12

>constructor(address feeTo_, address _owner) OperatableV2(_owner)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15-L22

>constructor(address maintainer_, address owner_) Owned(owner_)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22-L28

>constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20-L25

>constructor(address implementation_,IFeeRateModel maintainerFeeRateModel_,address owner_, address governor_) Factory(implementation_, maintainerFeeRateModel_, owner_)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L29-L39

>constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_))

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L47-L57

>constructor() Owned(msg.sender)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L58-L61

>constructor(BlastTokenRegistry registry_, address feeTo_)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L84-L95

>constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21-L27

## [G-05] INTERNAL FUNCTIONS NEVER USED

The contract declared internal functions but was not using them in any of the functions or contracts.

Since internal functions can only be called from inside the contracts, it makes no sense to have them if they are not used. This uses up gas and causes issues for auditors when understanding the contract logic.

Having dead code in the contracts uses up unnecessary gas and increases the complexity of the overall smart contract.

It is recommended to remove the internal functions from the contracts if they are never used.

**Instances**: 4

>function _implementation() internal view override returns (address)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L226-L228

>function isOwner(address _account) internal view override returns (bool)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L103-L105

>function _onBeforeDeposit(IERC20 token,address /*from*/,address /*to*/,uint256 /*amount*/,uint256 /*share*/) internal view override

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L36-L46

>function _configure() internal override

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L98-L101

## [G-06] SPLITTING REVERT STATEMENTS

The contract is using multiple conditions in a single if statement followed by a revert. This costs some extra gas. It is recommended to split the conditions into multiple if statements such that there’s only one condition in each of them.

**Here's an example**:

 >if (caps[token] > 0 && totals[token].total > caps[token]) {
            revert ErrCapReached();
}

**REFACTORING CODE**

>if (caps[token] > 0) {
    if (totals[token].total > caps[token]) {
        revert ErrCapReached();
    }
}

**Instances**: 3

>if (caps[token] > 0 && totals[token].total > caps[token]) {

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114-L116

>if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326-L328

>if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302-L304

## [G-07] STORAGE VARIABLE CACHING IN MEMORY

In Solidity, caching a state variable in memory can save gas if that variable is accessed multiple times within a function. This optimization is based on the fact that accessing state variables is more expensive than accessing variables stored in memory.

When you access a state variable, it involves a lookup on the Ethereum blockchain, which can be costly in terms of gas. On the other hand, accessing variables stored in memory is much cheaper because it doesn't involve any interactions with the blockchain.

Instances: 10

The contract `BlastCauldronV4` is using the state variable `_governor` multiple times in the function `init`. `SLOADs` are expensive (100 gas after the 1st one) compared to `MLOAD/MSTORE` (3 gas each).

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59-L68

The contract `BlastMagicLP` is using the state variable `registry` multiple times in the function `claimTokenYields`. 

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L53-L62

The contract `BlastMagicLP` is using the state variable `registry` multiple times in the function `_updateTokenClaimables`. 

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L104-L112

The contract `LockingMultiRewards` is using the state variable `_rewardData` multiple times in the function `addReward`. 

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300-L315

The contract `LockingMultiRewards` is using the state variable `rewardTokens` multiple times in the function `addReward`.

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300-L315

The contract `LockingMultiRewards` is using the state variable `stakingToken` multiple times in the function `recover`. 

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L324-L332

The contract `LockingMultiRewards` is using the state variable `_rewardData` multiple times in the function `notifyRewardAmount`. 

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361-L393

The contract `LockingMultiRewards` is using the state variable `lastLockIndex` multiple times in the function `processExpiredLocks`.

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397-L453

The contract `LockingMultiRewards` is using the state variable `_userLocks` multiple times in the function `_createLock`. 

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L479-L514

The contract `LockingMultiRewards` is using the state variable `lastLockIndex` multiple times in the function `_createLock`. 

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L479-L514

## [G-08] CHEAPER INEQUALITIES IN IF()

The contract was found to be doing comparisons using inequalities inside the if statement.

When inside the if statements, non-strict inequalities `(>=, <=)` are usually cheaper than the strict equalities `(>, <)`.

It is recommended to go through the code logic, and, if possible, modify the strict inequalities with the non-strict ones to save ~3 gas as long as the logic of the code is not affected.

**Instances**: 14

>if (totalPoolShares < minAmountOut)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L108-L108

>if (remainder > 0)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L22-L22

>if (caps[token] > 0 && totals[token].total > caps[token])

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114-L114

>if (_lockDuration < MIN_LOCK_DURATION) 

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L123-L123

>if (_rewardsDuration < MIN_REWARDS_DURATION)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L127-L127

>if (_remainingRewardTime < minRemainingTime)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L374-L374

>if (block.timestamp < reward.periodFinish)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L379-L379

>if (amount < _remainingRewardTime)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L384-L384

>if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L490-L490

>if (msg.value > wethAdjustedAmount)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L220-L220

>if (shares < minimumShares)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L502-L502

>if (amountOut < minimumOut)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L566-L566

>if (amountOut < minimumOut)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L573-L573

>if (amountOut < minimumOut)

https://github.com//code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L581-L581



 
































