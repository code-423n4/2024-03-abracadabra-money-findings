
# Gas Optimizations

| Number | Issue | Instances |
|--------|-------|-----------|
|[G-01]| Use assembly to emit events | 59 |
|[G-02]| Multiple accesses of a mapping/array should use a storage pointer | 14 |
|[G-03]| Use assembly to validate msg.sender | 2 |
|[G-04]| Declare Constructor Function as Payable to Save Gas | 16 |
|[G-05]| State variables can be packed into fewer storage slots | 2 |
|[G-06]| Empty Block | 2 |
|[G-07]| Use the external Visibility Modifier | 6 |
|[G-08]| Cache Array Length Outside of Loop | 7 |
|[G-09]| State variables should be cached in stack variables rather than re-reading them from storage | 2 |
|[G-10]| Optimize address(0) Checks Using Assembly | 23 |
|[G-11]| Redundant state variable getters | 2 |
|[G-12]| Store Data in calldata Instead of Memory for Certain Function Parameters  | 13 |
|[G-13]| Splitting if() statements that use && saves gas | 10 |
|[G-14]| Use assembly to write address storage values | 8 |
|[G-15]| Use of emit inside a loop | 4 |
|[G-16]| Check Arguments Early | 1 |
|[G-17]| Use uint8 Can Increase Gas Cost | 5 |
|[G-18]| address(this) can be stored in state variable that will ultimately cost less, than every time calculating this, specifically when it used multiple times in a contract | 43 |
|[G-19]| Using delete statement can save gas | 1 |
|[G-20]| Don’t make variables public unless necessary | 15 |
|[G-21]| Use uint256(1)/uint256(2) instead for true and false boolean states | 4 |
|[G-22]| Using bytes32 is cheaper than using string. | 4 |
|[G-23]| Avoid Loops and Complex Computations | 2 |
|[G-24]| Check if amount is greater than zero before performing safeTransfer | 5 |
|[G-25]| Use constants instead of type(uintX).max | 4 |
|[G-26]| Use hardcoded address instead address(this) | 43 |


## [G-01] Use assembly to emit events

This detector checks for instances where a contract uses assembly code to emit events. While it’s technically possible to emit events using inline assembly in Solidity, it’s generally discouraged due to readability concerns and potential for errors. Events should usually be emitted using higher-level Solidity constructs.

```solidity
file: blob/main/src/blast/BlastBox.sol

78   emit LogFeeToChanged(feeTo_);

90   emit LogTokenDepositEnabled(token, enabled);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L78

```solidity
file: blob/main/src/blast/BlastGovernor.sol

46   emit LogFeeToChanged(_feeTo);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L46

```solidity
file: blob/main/src/blast/BlastMagicLP.sol

86    emit LogFeeToChanged(feeTo_);

91    emit LogOperatorChanged(operator, status);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L86

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

120   emit LogDeposit(msg.sender, token, amount, lock_);

129   emit LogLock(msg.sender, token, amount);

140   emit LogWithdraw(msg.sender, token, amount);

153   emit LogFeeToChanged(feeTo_);

182   emit LogTokenSupported(token, supported);

187   emit LogTokenCapChanged(token, cap);

192   emit LogBootstrapperChanged(bootstrapper_);

197   emit LogStateChange(State.Opened);

202   emit LogStateChange(State.Closed);

211   emit LogTokenRescue(token, to, amount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L120

```solidity
file: blob/main/src/blast/BlastOnboardingBoot.sol

71   emit LogClaimed(msg.sender, shares, lock);

124  emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

132  emit LogInitialized(_router);

143  emit LogStakingChanged(address(_staking));

148  emit LogReadyChanged(ready);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L71

```solidity
file: blob/main/src/blast/BlastTokenRegistry.sol

20   emit LogNativeYieldTokenEnabled(token, enabled);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L20

```solidity
file: blob/main/src/blast/libraries/BlastYields.sol

26   emit LogBlastTokenClaimableEnabled(address(this), token);

31   emit LogBlastNativeClaimableEnabled(address(this));

44   emit LogBlastGasClaimed(recipient, amount);

57   emit LogBlastETHClaimed(recipient, amount);

62   emit LogBlastETHClaimed(recipient, amount);

72   emit LogBlastTokenClaimed(recipient, address(token), amount);

77   emit LogBlastTokenClaimed(recipient, address(token), amount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L26

```solidity
file: blob/main/src/mimswap/MagicLP.sol

259  emit RChange(newRState);

264  emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

282  emit RChange(newRState);

287  emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

323  emit RChange(newRState);

325  emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

345  emit RChange(newRState);

347  emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

352  emit FlashLoan(msg.sender, assetTo, baseAmount, quoteAmount);

409  emit BuyShares(to, shares, balanceOf(to));

454  emit SellShares(msg.sender, to, shareAmount, balanceOf(msg.sender));

467  emit TokenRescue(token, to, amount);

501  emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L259

```solidity
file: blob/main/src/mimswap/auxiliary/FeeRateModel.sol

52   emit LogMaintainerChanged(maintainer_);

59   emit LogImplementationChanged(implementation_);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L52

```solidity
file: blob/main/src/mimswap/periphery/Factory.sol

88  emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
        _addPool(creator, baseToken_, quoteToken_, clone);

102 emit LogSetImplementation(implementation_);

111 emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);

141 emit LogPoolRemoved(pool);

152 emit LogPoolAdded(baseToken, quoteToken, creator, pool);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

183  emit LogWithdrawn(msg.sender, amount);

318  emit LogSetMinLockAmount(minLockAmount, _minLockAmount);

331  emit LogRecovered(tokenAddress, tokenAmount);

392  emit LogRewardAdded(amount);

436  emit LogLockIndexChanged(user, lastIndex, index);

447  emit LogUnlocked(user, amount, index);

475  emit LogStaked(account, amount);

513  emit LogLocked(user, amount, _nextUnlockTime, lockCount);

611  emit LogRewardLockCreated(user, _rewardLock.unlockTime);

638  emit LogRewardPaid(user, rewardToken, amount);

651  emit LogRewardLocked(user, rewardToken, rewardAmount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L183

## [G-02] Multiple accesses of a mapping/array should use a storage pointer

Caching a mapping’s value in a storage pointer when the value is accessed multiple times saves ~40 gas per access due to not having to perform the same offset calculation every time. Help the Optimizer by saving a storage variable’s reference instead of repeatedly fetching it.
To achieve this, declare a storage pointer for the variable and use it instead of repeatedly fetching the reference in a map or an array. As an example, instead of repeatedly calling proposals[_proposalId], save its reference via a storage pointer: Proposal storage proposal_ = proposals[_proposalId] and use the pointer instead.

### _rewardData[rewardToken] can be cached as a storage pointer

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

277  function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
        if (totalSupply_ == 0) {
            return _rewardData[rewardToken].rewardPerTokenStored;
        }

        uint256 timeElapsed = lastTimeRewardApplicable_ - _rewardData[rewardToken].lastUpdateTime;
        uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

        return _rewardData[rewardToken].rewardPerTokenStored + pendingRewardsPerToken;
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277-L286

### _userLocks[user] can be cached as a storage pointer


```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

479  function _createLock(address user, uint256 amount) internal {
        Balances storage bal = _balances[user];
        uint256 _nextUnlockTime = nextUnlockTime();
        uint256 _lastLockIndex = lastLockIndex[user];
        uint256 lockCount = _userLocks[user].length;

        bal.locked += amount;
        lockedSupply += amount;

        // Add to current lock if it's the same unlock time or the first one
        // userLocks is sorted by unlockTime, so the last lock is the most recent one
        if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {
            // Limit the number of locks per user to avoid too much gas costs per user
            // when looping through the locks
            if (lockCount == maxLocks) {
                revert ErrMaxUserLocksExceeded();
            }

            if (amount < minLockAmount) {
                revert ErrLockAmountTooSmall();
            }

            _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));
            lastLockIndex[user] = lockCount;

            unchecked {
                ++lockCount;
            }
        }
        /// It's the same reward period, so we just add the amount to the current lock
        else {
            _userLocks[user][_lastLockIndex].amount += amount;
        }

        emit LogLocked(user, amount, _nextUnlockTime, lockCount);
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L479-L514

### _rewardData[rewardToken] can be cached as a storage pointer

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

300   function addReward(address rewardToken) public onlyOwner {
        if (rewardToken == address(0)) {
            revert ErrInvalidTokenAddress();
        }

        if (_rewardData[rewardToken].exists) {
            revert ErrRewardAlreadyExists();
        }

        if (rewardTokens.length == MAX_NUM_REWARDS) {
            revert ErrMaxRewardsExceeded();
        }

        rewardTokens.push(rewardToken);
        _rewardData[rewardToken].exists = true;
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300-L315

### rewards[user] can be cached as a storage pointer

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

615     address rewardToken = rewardTokens[i];
       uint256 rewardAmount = rewards[user][rewardToken];

            // in all scenario, reset the reward amount immediately
      rewards[user][rewardToken] = 0;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L615-L619

### _rewardData[rewardToken] can be cached as a storage pointer

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

361   function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
        if (!_rewardData[rewardToken].exists) {
            revert ErrInvalidTokenAddress();
        }

        _updateRewards();
        rewardToken.safeTransferFrom(msg.sender, address(this), amount);

        Reward storage reward = _rewardData[rewardToken];
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361-L369

### lastLockIndex[user] can be cached as a storage pointer

```solidity
file:  blob/main/src/staking/LockingMultiRewards.sol

397     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
        if (users.length != lockIndexes.length) {
            revert ErrLengthMismatch();
        }

        _updateRewardsForUsers(users);

        // Release all expired users' locks
        for (uint256 i; i < users.length; ) {
            address user = users[i];
            Balances storage bal = _balances[user];
            LockedBalance[] storage locks = _userLocks[user];

            if (locks.length == 0) {
                revert ErrNoLocks();
            }

            uint256 index = lockIndexes[i];

            // Prevents processing `lastLockIndex` out of order
            if (index == lastLockIndex[user] && locks.length > 1) {
                revert ErrInvalidLockIndex();
            }

            // prohibit releasing non-expired locks
            if (locks[index].unlockTime > block.timestamp) {
                revert ErrLockNotExpired();
            }

            uint256 amount = locks[index].amount;
            uint256 lastIndex = locks.length - 1;

            /// Last lock index changed place with the one we just swapped.
            if (lastLockIndex[user] == lastIndex) {
                lastLockIndex[user] = index;
            }

            if (index != lastIndex) {
                locks[index] = locks[lastIndex];
                emit LogLockIndexChanged(user, lastIndex, index);
            }

            locks.pop();

            unlockedSupply += amount;
            lockedSupply -= amount;

            bal.unlocked += amount;
            bal.locked -= amount;

            emit LogUnlocked(user, amount, index);

            unchecked {
                ++i;
            }
        }
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397-L453

### claimed[msg.sender] can be cached as a storage pointer

```solidity
file:

55  function claim(bool lock) external returns (uint256 shares) {
        if (!ready) {
            revert ErrNotReady();
        }
        if (claimed[msg.sender]) {
            revert ErrAlreadyClaimed();
        }

        shares = _claimable(msg.sender);
        if (shares == 0) {
            revert ErrNothingToClaim();
        }

        claimed[msg.sender] = true;
        staking.stakeFor(msg.sender, shares, lock);

        emit LogClaimed(msg.sender, shares, lock);
    }
```

### totals[token] can be cached as a storage pointer

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

101   function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
        token.safeTransferFrom(msg.sender, address(this), amount);

        if (lock_) {
            totals[token].locked += amount;
            balances[msg.sender][token].locked += amount;
        } else {
            totals[token].unlocked += amount;
            balances[msg.sender][token].unlocked += amount;
        }

        totals[token].total += amount;

        if (caps[token] > 0 && totals[token].total > caps[token]) {
            revert ErrCapReached();
        }

        balances[msg.sender][token].total += amount;

        emit LogDeposit(msg.sender, token, amount, lock_);
    }


123  function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
        balances[msg.sender][token].unlocked -= amount;
        balances[msg.sender][token].locked += amount;
        totals[token].unlocked -= amount;
        totals[token].locked += amount;

        emit LogLock(msg.sender, token, amount);
    }

132   function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
        balances[msg.sender][token].unlocked -= amount;
        balances[msg.sender][token].total -= amount;
        totals[token].unlocked -= amount;
        totals[token].total -= amount;

        token.safeTransfer(msg.sender, amount);

        emit LogWithdraw(msg.sender, token, amount);
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101-L121

### caps[token] can be cached as a storage pointer

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

114  if (caps[token] > 0 && totals[token].total > caps[token]) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114

### balances[msg.sender] can be cached as a storage pointer

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

101  function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
        token.safeTransferFrom(msg.sender, address(this), amount);

        if (lock_) {
            totals[token].locked += amount;
            balances[msg.sender][token].locked += amount;
        } else {
            totals[token].unlocked += amount;
            balances[msg.sender][token].unlocked += amount;
        }

        totals[token].total += amount;

        if (caps[token] > 0 && totals[token].total > caps[token]) {
            revert ErrCapReached();
        }

        balances[msg.sender][token].total += amount;

        emit LogDeposit(msg.sender, token, amount, lock_);
    }

123 function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
            balances[msg.sender][token].unlocked -= amount;
            balances[msg.sender][token].locked += amount;
            totals[token].unlocked -= amount;
            totals[token].locked += amount;

            emit LogLock(msg.sender, token, amount);
        }

132  function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
        balances[msg.sender][token].unlocked -= amount;
        balances[msg.sender][token].total -= amount;
        totals[token].unlocked -= amount;
        totals[token].total -= amount;

        token.safeTransfer(msg.sender, amount);

        emit LogWithdraw(msg.sender, token, amount);
    }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101-L121

## [G-03] Use assembly to validate msg.sender

We can use assembly to efficiently validate msg.sender for the didPay and uniswapV3SwapCallback functions with the least amount of opcodes necessary. Additionally, we can use xor() instead of iszero(eq()), saving 3 gas. We can also potentially save gas on the unhappy path by using scratch space to store the error selector, potentially avoiding memory expansion costs.

```solidity
file: blob/main/src/blast/BlastMagicLP.sol

119  if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119

```solidity
file: blob/main/src/mimswap/MagicLP.sol

608  if (msg.sender != implementation.owner()) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L608

## [G-04] Declare Constructor Function as Payable to Save Gas

```solidity
file: blob/main/src/blast/BlastBox.sol

24  constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24

```solidity
file: blob/main/src/blast/BlastDapp.sol

7   constructor() {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L7

```solidity
file: blob/main/src/blast/BlastGovernor.sol

15  constructor(address feeTo_, address _owner) OperatableV2(_owner) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15

```solidity
file: blob/main/src/blast/BlastMagicLP.sol

23  constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

58   constructor() Owned(msg.sender) {

84   constructor(BlastTokenRegistry registry_, address feeTo_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L58

```solidity
file: blob/main/src/blast/BlastTokenRegistry.sol

12   constructor(address _owner) Owned(_owner) {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12

```solidity
file: blob/main/src/blast/BlastWrappers.sol

20    constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

29    constructor(
        address implementation_,
        IFeeRateModel maintainerFeeRateModel_,
        address owner_,
        address governor_
    ) Factory(implementation_, maintainerFeeRateModel_, owner_) {

47  constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20

```solidity
file: blob/main/src/mimswap/MagicLP.sol

84  constructor(address owner_) Owned(owner_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84

```solidity
file: blob/main/src/mimswap/auxiliary/FeeRateModel.sol

22    constructor(address maintainer_, address owner_) Owned(owner_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22

```solidity
file: blob/main/src/mimswap/periphery/Factory.sol

38     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38


```solidity
file: blob/main/src/mimswap/periphery/Router.sol
  
38   constructor(IWETH weth_, IFactory factory_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38

```solidity
file: blob/main/src/oracles/aggregators/MagicLpAggregator.sol

21    constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

112  constructor(
        address _stakingToken,
        uint256 _lockingBoostMultiplerInBips,
        uint256 _rewardsDuration,
        uint256 _lockDuration,
        address _owner
    ) OperatableV2(_owner) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L112-L118

## [G-05] State variables can be packed into fewer storage slots

If variables occupying the same slot are both written the same function or by the constructor, avoids a separate Gsset (20000 gas). Reads of the variables can also be cheaper

```solidity
file: blob/main/src/blast/BlastOnboardingBoot.sol

24   address public pool;
    Router public router;
    IFactory public factory;
    uint256 public totalPoolShares;
    bool public ready;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L24-L28

```solidity
file: blob/main/src/mimswap/MagicLP.sol

70  address public _BASE_TOKEN_;
    address public _QUOTE_TOKEN_;
    uint112 public _BASE_RESERVE_;
    uint112 public _QUOTE_RESERVE_;
    uint32 public _BLOCK_TIMESTAMP_LAST_;
    uint256 public _BASE_PRICE_CUMULATIVE_LAST_;
    uint112 public _BASE_TARGET_;
    uint112 public _QUOTE_TARGET_;
    uint32 public _RState_;
    IFeeRateModel public _MT_FEE_RATE_MODEL_;
    uint256 public _LP_FEE_RATE_;
    uint256 public _K_;
    uint256 public _I_;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L70-L82

## [G-06] Empty Block

The code should be refactored such that they no longer exist, or the block should do something useful, such as emitting an event or reverting. If the contract is meant to be extended, the contract should be abstract and the function signatures be added without any default implementation. If the block is an empty if-statement block to avoid doing subsequent checks in the else-if/else conditions, the else-if/else conditions should be nested under the negation of the if-statement, because they involve different classes of checks, which may lead to the introduction of errors when the code is later modified.

```solidity
file: blob/main/src/blast/BlastGovernor.sol

13    receive() external payable {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L13

```solidity
file: blob/main/src/mimswap/periphery/Router.sol

36   receive() external payable {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L36

## [G-07] Use the external Visibility Modifier

Use the external function visibility (https://www.alchemy.com/overviews/solidity-function-visibility) for gas optimization because the public visibility modifier is equivalent to using the external and internal visibility modifier, meaning both public and external can be called from outside of your contract, which requires more gas.

Remember that of these two visibility modifiers, only the public modifier can be called from other functions inside of your contract. for example

```solidity
function one() public view returns (string memory){
         return message;
    }

 
    function two() external view returns  (string memory){
         return message;
    }

```

```solidity
file: blob/main/src/mimswap/MagicLP.sol

159   function symbol() public pure override returns (string memory) {
        return "MagicLP";
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L159-L161

```solidity
file: blob/main/src/mimswap/MagicLP.sol

163  function decimals() public view override returns (uint8) {
        return IERC20Metadata(_BASE_TOKEN_).decimals();
    }

215  function getMidPrice() public view returns (uint256 midPrice) {
        return PMMPricing.getMidPrice(getPMMState());
    }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163-L165


```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

253  function nextUnlockTime() public view returns (uint256) {
        return nextEpoch() + lockDuration;
    }

261  function nextEpoch() public view returns (uint256) {
        return epoch() + rewardsDuration;
    }

265  function remainingEpochTime() public view returns (uint256) {
        return nextEpoch() - block.timestamp;
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L253-L255

## [G-08] Cache Array Length Outside of Loop

When using arrays in a for loop, calling .length on every iteration will result in unnecessary gas expenses. Instead, it is recommended to cache the array length beforehand, which saves 3 gas per iteration. For storage arrays, an additional 100 gas per iteration (except the first) can be saved by pre-caching the length

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

165    for (uint256 i = 0; i < tokens.length; i++) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

405  for (uint256 i; i < users.length; ) {

547  for (uint256 i; i < rewardTokens.length; ) {

561  for (uint256 i; i < rewardTokens.length; ) {

575  for (uint256 i; i < rewardTokens.length; ) {

580  for (uint256 j; j < users.length; ) {

614  for (uint256 i; i < rewardTokens.length; ) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405


## [G-09] State variables should be cached in stack variables rather than re-reading them from storage

State variables should be cached instead of re-reading them.Subsequent reads incur a 100 gas


### Cache the implementation state variable in stack variable   

```solidity
file: blob/main/src/mimswap/auxiliary/FeeRateModel.sol

34  function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
        if (implementation == address(0)) {
            return (lpFeeRate, 0);
        }

        return IFeeRateImpl(implementation).getFeeRate(msg.sender, trader, lpFeeRate);
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34-L40

### Cache the _RState_ state variable in stack variable and also cache _RState_ state variable in `MagicLP.sellQuote` and  `MagicLP.flashLoan` function to save gas 

```solidity
file: blob/main/src/mimswap/MagicLP.sol

256  if (_RState_ != uint32(newRState)) {
            _BASE_TARGET_ = newBaseTarget.toUint112();
            _RState_ = uint32(newRState);
            emit RChange(newRState);
        }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L256-L260

## [G-10] Optimize address(0) Checks Using Assembly

Solidity provides address(0) as a constant for the zero address. While it is generally safe to use, explicit checks against address(0) in your code might be slightly more gas efficient if implemented in inline assembly, due to reduced overhead.

```solidity
file: blob/main/src/blast/BlastBox.sol

25  if (feeTo_ == address(0)) {

28  if (address(registry_) == address(0)) {

73  if (feeTo_ == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L25

```solidity
file: blob/main/src/blast/BlastGovernor.sol

16  if (feeTo_ == address(0)) {

41  if(_feeTo == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L16

```solidity
file: blob/main/src/blast/BlastMagicLP.sol

24   if (feeTo_ == address(0)) {

27   if (address(registry_) == address(0)) {

81   if (feeTo_ == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L24

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

85   if (address(registry_) == address(0)) {

89   if (feeTo_ == address(0)) {

148  if (feeTo_ == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L85

```solidity
file: blob/main/src/blast/BlastWrappers.sol

21   if (governor_ == address(0)) {

35   if (governor_ == address(0)) {

48   if (governor_ == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L21

```solidity
file: blob/main/src/mimswap/MagicLP.sol

102   if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {

393  _mint(address(0), 1001);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102

```solidity
file: blob/main/src/mimswap/auxiliary/FeeRateModel.sol

23   if (maintainer_ == address(0)) {

35   if (implementation == address(0)) {

47   if (maintainer_ == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L23

```solidity
file: blob/main/src/mimswap/periphery/Factory.sol

39   if (implementation_ == address(0)) {

42   if (address(maintainerFeeRateModel_) == address(0)) {

97   if (implementation_ == address(0)) {

106  if (address(maintainerFeeRateModel_) == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L39

## [G-11] Redundant state variable getters

Getters for public state variables are automatically generated by the solidity compiler so there is no need to code them manually as this increases deployment cost.

###  Make pools mapping variable private or internal since a getter function was defined for it

The solidity compiler would automatically create a getter function for the pools mapping since it is declared as a public variable but a getter function getPoolCount() was also declared in the contract for the same variable thereby making it two getter functions for the same variable in the contract. We could rectify this issue by making the pools variable private or internal (if the variable is to be inherited). The diff below shows how the code could be refactored:

```solidity
file: blob/main/src/mimswap/periphery/Factory.sol


35  mapping(address base => mapping(address quote => address[] pools)) public pools;

53  function getPoolCount(address token0, address token1) external view returns (uint256) {
        return pools[token0][token1].length;
    }


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L53-L55

### Make userPools mapping variable private or internal since a getter function was defined for it

The solidity compiler would automatically create a getter function for the userPools mapping since it is declared as a public variable but a getter function getUserPoolCount() was also declared in the contract for the same variable thereby making it two getter functions for the same variable in the contract. We could rectify this issue by making the userPools variable private or internal (if the variable is to be inherited). The diff below shows how the code could be refactored:

```solidity
file: blob/main/src/mimswap/periphery/Factory.sol

36   mapping(address creator => address[] pools) public userPools;

57  function getUserPoolCount(address creator) external view returns (uint256) {
        return userPools[creator].length;
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L57-L59




## [G-12] Store Data in calldata Instead of Memory for Certain Function Parameters 

Instead of copying variables to memory, it is typically more cost-effective to load them immediately from calldata. If all you need to do is read data, you can conserve gas by saving the data in calldata.

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

164   function claimTokenYields(address[] memory tokens) external onlyOwner {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

397  function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {

572  function _updateRewardsForUsers(address[] memory users) internal {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397

```solidity
file: blob/main/src/mimswap/libraries/PMMPricing.sol

39   function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {

76   function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {

104   function _ROneSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )

119   function _ROneSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        
134  function _RBelowSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )

147   function _RBelowSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )

162  function _RAboveSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )

175  function _RAboveSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )

190  function adjustedTarget(PMMState memory state) internal pure {

203  function getMidPrice(PMMState memory state) internal pure returns (uint256) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L39

## [G‑13] Splitting if() statements that use && saves gas

```solidity
file: blob/main/src/blast/BlastMagicLP.sol

119  if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

114  if (caps[token] > 0 && totals[token].total > caps[token]) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114

```solidity
file: blob/main/src/mimswap/MagicLP.sol

139  if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {

144  if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

302  if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {

549  if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139

```solidity
file:  blob/main/src/staking/LockingMultiRewards.sol

326  if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

417  if (index == lastLockIndex[user] && locks.length > 1) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326

```solidity
file:  blob/main/src/mimswap/periphery/Router.sol

147    } else if (baseReserve > 0 && quoteReserve > 0) {

527   if (quoteReserve > 0 && baseReserve > 0) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147

## [G-14] Use assembly to write address storage values

Using assembly to write address storage values can potentially save gas costs. This detector flags instances where address storage values are written without using assembly.

```solidity
file: blob/main/src/blast/BlastGovernor.sol

45  feeTo = _feeTo;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L45


```solidity
file: blob/main/src/mimswap/auxiliary/FeeRateModel.sol

51  maintainer = maintainer_;

58  implementation = implementation_;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L51

```solidity
file: blob/main/src/blast/BlastMagicLP.sol

85  feeTo = feeTo_;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L85

```solidity
file: blob/main/src/blast/BlastBox.sol

77    feeTo = feeTo_;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L77

```solidity
file: blob/main/src/mimswap/periphery/Factory.sol

45    implementation = implementation_;

101   implementation = implementation_;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L45

```solidity
file: blob/main/src/blast/BlastGovernor.sol

20  feeTo = feeTo_;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L20

## [G-15] Use of emit inside a loop

Emitting an event inside a loop performs a LOG op N times, where N is the loop length. This can lead to significant gas costs.

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

436   emit LogLockIndexChanged(user, lastIndex, index);

447   emit LogUnlocked(user, amount, index);

638   emit LogRewardPaid(user, rewardToken, amount);

651   emit LogRewardLocked(user, rewardToken, rewardAmount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L436

## [G-16] Check Arguments Early

### check the lock argument first in `BlastOnboarding.deposit` function 

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

101   function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
        token.safeTransferFrom(msg.sender, address(this), amount);

        if (lock_) {
            totals[token].locked += amount;
            balances[msg.sender][token].locked += amount;
        } else {
            totals[token].unlocked += amount;
            balances[msg.sender][token].unlocked += amount;
        }

        totals[token].total += amount;

        if (caps[token] > 0 && totals[token].total > caps[token]) {
            revert ErrCapReached();
        }

        balances[msg.sender][token].total += amount;

        emit LogDeposit(msg.sender, token, amount, lock_);
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101-L122

Recommandation code 

```diff
 
 function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

-        token.safeTransferFrom(msg.sender, address(this), amount);

-        if (lock_) {
            totals[token].locked += amount;
            balances[msg.sender][token].locked += amount;
        } else {
            totals[token].unlocked += amount;
            balances[msg.sender][token].unlocked += amount;
        }

        totals[token].total += amount;

        if (caps[token] > 0 && totals[token].total > caps[token]) {
            revert ErrCapReached();
        }

        balances[msg.sender][token].total += amount;

        emit LogDeposit(msg.sender, token, amount, lock_);
    }

    function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {   

+     if (lock_) {
            totals[token].locked += amount;
            balances[msg.sender][token].locked += amount;
        } else {
            totals[token].unlocked += amount;
            balances[msg.sender][token].unlocked += amount;
        }

+        token.safeTransferFrom(msg.sender, address(this), amount);

        totals[token].total += amount;

        if (caps[token] > 0 && totals[token].total > caps[token]) {
            revert ErrCapReached();
        }

        balances[msg.sender][token].total += amount;

        emit LogDeposit(msg.sender, token, amount, lock_);
    }


```

## [G-17] Use uint8 Can Increase Gas Cost

A smart contract's gas consumption can be higher if developers use items that are less than 32 bytes in size because the Ethereum Virtual Machine can only handle 32 bytes at a time. In order to increase the element's size to the necessary size, the EVM has to perform additional operations. 

```solidity
file: blob/main/src/oracles/aggregators/MagicLpAggregator.sol

13   uint8 public immutable baseDecimals;

14   uint8 public immutable quoteDecimals;

29   function decimals() external pure override returns (uint8) {

```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol


```solidity
file: blob/main/src/mimswap/periphery/Router.sol

598   function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L598

```solidity
file: blob/main/src/mimswap/MagicLP.sol
 
163   function decimals() public view override returns (uint8) {
    
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163

## [G-18] address(this) can be stored in state variable that will ultimately cost less, than every time calculating this, specifically when it used multiple times in a contract

```solidity
file: blob/main/src/blast/BlastBox.sol

99  BlastYields.configureDefaultClaimables(address(this));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L99

```solidity
file: blob/main/src/blast/BlastGovernor.sol

21  BlastYields.configureDefaultClaimables(address(this));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L21

```solidity
file: blob/main/src/blast/BlastMagicLP.sol

99  BlastYields.configureDefaultClaimables(address(this));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L99

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

59  BlastYields.configureDefaultClaimables(address(this));

102 token.safeTransferFrom(msg.sender, address(this), amount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L59

```solidity
file: blob/main/src/blast/BlastOnboardingBoot.sol

106  (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

117   staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));

118    staking.setOperator(address(this), true);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106

```solidity
file: blob/main/src/blast/BlastWrappers.sol

51   if (governor_ == address(this)) {

60   if (_governor == address(this)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L51

```solidity
file: blob/main/src/blast/libraries/BlastYields.sol

21  if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {

26   emit LogBlastTokenClaimableEnabled(address(this), token);

31   emit LogBlastNativeClaimableEnabled(address(this));

39   return claimMaxGasYields(address(this), recipient);

52   return claimAllNativeYields(address(this), recipient);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L21

```solidity
file: blob/main/src/mimswap/MagicLP.sol

229  return _BASE_TOKEN_.balanceOf(address(this)) - uint256(_BASE_RESERVE_);

233  return _QUOTE_TOKEN_.balanceOf(address(this)) - uint256(_QUOTE_RESERVE_);

245  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

262  _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));

268  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

285  _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);

298  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

299  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

361  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

362  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

427  if (to == address(this)) {

431  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

432  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

505  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

506  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

529  baseBalance = _BASE_TOKEN_.balanceOf(address(this));

530  quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

568  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

569  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L229

```solidity
file: blob/main/src/mimswap/periphery/Router.sol

92   address(weth).safeTransferFrom(address(this), clone, msg.value);

269  lp.safeTransferFrom(msg.sender, address(this), sharesIn);

282  lp.safeTransferFrom(msg.sender, address(this), sharesIn);

289   address(this),

298  address(this)

398  amountOut = _swap(address(this), path, directions, minimumOut);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

367   rewardToken.safeTransferFrom(msg.sender, address(this), amount);

467   stakingToken.safeTransferFrom(msg.sender, address(this), amount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367

## [G-19] Using delete statement can save gas

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

619  rewards[user][rewardToken] = 0;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L619

## [G-20] Don’t make variables public unless necessary

Issue Description - Making variables public comes with some overhead costs that can be avoided in many cases. A public variable implicitly creates a public getter function of the same name, increasing the contract size.

Proposed Optimization - Only mark variables as public if their values truly need to be readable by external contracts/users. Otherwise, use private or internal visibility.

Estimated Gas Savings - The savings from avoiding unnecessary public variables are small per transaction, around 5-10 gas. However, this adds up over many transactions targeting a contract with public state variables that don’t need to be public.

```solidity
file: blob/main/src/blast/BlastBox.sol

20   BlastTokenRegistry public immutable registry;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L20

```solidity
file: blob/main/src/blast/BlastMagicLP.sol

17  BlastTokenRegistry public immutable registry;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L17

```solidity
file: blob/main/src/mimswap/MagicLP.sol

61    MagicLP public immutable implementation;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L61

```solidity
file: blob/main/src/mimswap/periphery/Router.sol

33  IWETH public immutable weth;

34  IFactory public immutable factory;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L33

```solidity
file: blob/main/src/oracles/aggregators/MagicLpAggregator.sol

10    IMagicLP public immutable pair;

11    IAggregator public immutable baseOracle;

12    IAggregator public immutable quoteOracle;

13    uint8 public immutable baseDecimals;

14    uint8 public immutable quoteDecimals;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L10

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

83    uint256 public immutable maxLocks;

84    uint256 public immutable lockingBoostMultiplerInBips;

85    uint256 public immutable rewardsDuration;

86    uint256 public immutable lockDuration;

87    address public immutable stakingToken;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L83

## [G-21] Use uint256(1)/uint256(2) instead for true and false boolean states

Use uint256(1) and uint256(2) for true/false to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from ‘false’ to ‘true’, after having been ‘true’ in the past. see source:

```solidity
file: blob/main/src/mimswap/MagicLP.sol

88  _INITIALIZED_ = true;

118  _INITIALIZED_ = true;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L88

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

314  _rewardData[rewardToken].exists = true;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L314

```solidity
file: blob/main/src/blast/BlastOnboardingBoot.sol

68  claimed[msg.sender] = true;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L68

## [G-22] Using bytes32 is cheaper than using string.

Storing and manipulating data in bytes32 is more gas-efficient than using string, which involves dynamic storage allocation. bytes32 is a fixed-size type, whereas string can have variable length, resulting in higher gas costs.

```solidity
file: blob/main/src/blast/BlastMagicLP.sol

39   function version() external pure override returns (string memory) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L39

```solidity
file: blob/main/src/mimswap/MagicLP.sol

155   function name() public view override returns (string memory) {

159   function symbol() public pure override returns (string memory) {

236   function version() external pure virtual returns (string memory) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155


## [G-23] Avoid Loops and Complex Computations

Loops that iterate or compute over arrays and mappings are expensive:

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

165  for (uint256 i = 0; i < tokens.length; i++) {
            if (!supportedTokens[tokens[i]]) {
                revert ErrUnsupportedToken();
            }
            if (registry.nativeYieldTokens(tokens[i])) {
                BlastYields.claimAllTokenYields(tokens[i], feeTo);
            }
        }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165-L172

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

405  for (uint256 i; i < users.length; ) {
            address user = users[i];
            Balances storage bal = _balances[user];
            LockedBalance[] storage locks = _userLocks[user];

            if (locks.length == 0) {
                revert ErrNoLocks();
            }

            uint256 index = lockIndexes[i];

            // Prevents processing `lastLockIndex` out of order
            if (index == lastLockIndex[user] && locks.length > 1) {
                revert ErrInvalidLockIndex();
            }

            // prohibit releasing non-expired locks
            if (locks[index].unlockTime > block.timestamp) {
                revert ErrLockNotExpired();
            }

            uint256 amount = locks[index].amount;
            uint256 lastIndex = locks.length - 1;

            /// Last lock index changed place with the one we just swapped.
            if (lastLockIndex[user] == lastIndex) {
                lastLockIndex[user] = index;
            }

            if (index != lastIndex) {
                locks[index] = locks[lastIndex];
                emit LogLockIndexChanged(user, lastIndex, index);
            }

            locks.pop();

            unlockedSupply += amount;
            lockedSupply -= amount;

            bal.unlocked += amount;
            bal.locked -= amount;

            emit LogUnlocked(user, amount, index);

            unchecked {
                ++i;
            }
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405-L452

## [G-24] Check if amount is greater than zero before performing safeTransfer

safeTransfer‘ing when amount = 0 is a waste of gas, since there will be no funds transferred. To save gas, check if amount is greater than 0, before calling safeTransfer.

```solidity
file: blob/main/src/blast/BlastOnboarding.sol
 
138   token.safeTransfer(msg.sender, amount);

210   token.safeTransfer(to, amount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L138

```solidity
file: blob/main/src/mimswap/MagicLP.sol

466  token.safeTransfer(to, amount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L466

```solidity
file: blob/main/src/mimswap/periphery/Router.sol

489  IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L489

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

367  rewardToken.safeTransferFrom(msg.sender, address(this), amount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367

## [G-25] Use constants instead of type(uintX).max

When you use type(uintX).max, it may result in higher gas costs because it involves a runtime operation to calculate the type(uintX).max at runtime. This calculation is performed every time the expression is evaluated.

To save gas, it is recommended to use constants to represent the maximum value. Declaration of a constant with the maximum value means that the value is known at compile-time and does not require any runtime calculations.

```solidity
file: blob/main/src/blast/BlastOnboardingBoot.sol

103   MIM.safeApprove(address(router), type(uint256).max);

104   USDB.safeApprove(address(router), type(uint256).max);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L103

```solidity
file: blob/main/src/mimswap/MagicLP.sol

508   if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {

532   if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508

## [G-26] Use hardcoded address instead address(this)

```solidity
file: blob/main/src/blast/BlastBox.sol

99  BlastYields.configureDefaultClaimables(address(this));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L99

```solidity
file: blob/main/src/blast/BlastGovernor.sol

21  BlastYields.configureDefaultClaimables(address(this));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L21

```solidity
file: blob/main/src/blast/BlastMagicLP.sol

99  BlastYields.configureDefaultClaimables(address(this));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L99

```solidity
file: blob/main/src/blast/BlastOnboarding.sol

59  BlastYields.configureDefaultClaimables(address(this));

102 token.safeTransferFrom(msg.sender, address(this), amount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L59

```solidity
file: blob/main/src/blast/BlastOnboardingBoot.sol

106  (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

117   staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));

118    staking.setOperator(address(this), true);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106

```solidity
file: blob/main/src/blast/BlastWrappers.sol

51   if (governor_ == address(this)) {

60   if (_governor == address(this)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L51

```solidity
file: blob/main/src/blast/libraries/BlastYields.sol

21  if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {

26   emit LogBlastTokenClaimableEnabled(address(this), token);

31   emit LogBlastNativeClaimableEnabled(address(this));

39   return claimMaxGasYields(address(this), recipient);

52   return claimAllNativeYields(address(this), recipient);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L21

```solidity
file: blob/main/src/mimswap/MagicLP.sol

229  return _BASE_TOKEN_.balanceOf(address(this)) - uint256(_BASE_RESERVE_);

233  return _QUOTE_TOKEN_.balanceOf(address(this)) - uint256(_QUOTE_RESERVE_);

245  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

262  _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));

268  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

285  _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);

298  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

299  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

361  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

362  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

427  if (to == address(this)) {

431  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

432  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

505  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

506  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

529  baseBalance = _BASE_TOKEN_.balanceOf(address(this));

530  quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

568  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

569  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L229

```solidity
file: blob/main/src/mimswap/periphery/Router.sol

92   address(weth).safeTransferFrom(address(this), clone, msg.value);

269  lp.safeTransferFrom(msg.sender, address(this), sharesIn);

282  lp.safeTransferFrom(msg.sender, address(this), sharesIn);

289   address(this),

298  address(this)

398  amountOut = _swap(address(this), path, directions, minimumOut);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92

```solidity
file: blob/main/src/staking/LockingMultiRewards.sol

367   rewardToken.safeTransferFrom(msg.sender, address(this), amount);

467   stakingToken.safeTransferFrom(msg.sender, address(this), amount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367