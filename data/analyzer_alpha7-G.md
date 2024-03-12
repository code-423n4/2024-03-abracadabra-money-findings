
## [GAS-01] Constructors can be marked as payable to save deployment gas
payable functions cost less gas to execute, since the compiler does not have to add extra checks to
ensure that a payment wasn't provided.
A constructor can safely be marked as payable , since only the deployer would be able to pass funds, and the project itself would not pass any funds.

```
 constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24C4-L24C94

```
  constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15C3-L15C71

```
  constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23C3-L23C96

```
  constructor() Owned(msg.sender) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L58C3-L58C38

```
   constructor(address _owner) Owned(_owner) {}
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12C2-L12C49

```
    constructor(
        address implementation_,
        IFeeRateModel maintainerFeeRateModel_,
        address owner_,
        address governor_
    ) Factory(implementation_, maintainerFeeRateModel_, owner_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L29C1-L34C66

```
 constructor(address owner_) Owned(owner_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84C4-L84C48

```
     constructor(address maintainer_, address owner_) Owned(owner_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22C3-L22C69

```
 constructor(IWETH weth_, IFactory factory_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38C4-L38C50

```
  constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21C3-L21C85

```
   /// @param _lockDuration The duration of the lock period in seconds, should be 13 weeks by default.
    constructor(
        address _stakingToken,
        uint256 _lockingBoostMultiplerInBips,
        uint256 _rewardsDuration,
        uint256 _lockDuration,
        address _owner
    ) OperatableV2(_owner) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L111C2-L118C29


## [G-02] Empty blocks should be removed or emit 

```
 constructor(address _owner) Owned(_owner) {}
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12C2-L12C49


## [G‑03] Structs can be packed into fewer storage slots
Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.

```
 struct Reward {
        uint256 periodFinish;
        uint256 rewardRate;
        uint256 rewardPerTokenStored;
        bool exists;
        uint248 lastUpdateTime;
    }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L50C4-L56C6

```
 struct Balances {
        uint256 unlocked;
        uint256 locked;
    }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L58C4-L61C6

```
 struct LockedBalance {
        uint256 amount;
        uint256 unlockTime;
    }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L63C4-L66C6

```
 struct RewardLockItem {
        address token;
        uint256 amount;
    }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L68C4-L71C6

```
  struct RewardLock {
        RewardLockItem[] items;
        uint256 unlockTime;
    }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L73C3-L76C6
## [G-04] Use double if statements instead of &&
If the if statement has a logical AND and is not followed by an else statement, it can be replaced with 2 if statements.

```
    if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
            revert ErrNotAllowedImplementationOperator();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119C5-L121C10

```
 if (caps[token] > 0 && totals[token].total > caps[token]) {
            revert ErrCapReached();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114C8-L116C10

```
 if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
            _RState_ = uint32(PMMPricing.RState.ONE);
            _BASE_TARGET_ = _BASE_RESERVE_;
            _QUOTE_TARGET_ = _QUOTE_RESERVE_;
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139C8-L143C10

```
 if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
            _RState_ = uint32(PMMPricing.RState.ONE);
            _BASE_TARGET_ = _BASE_RESERVE_;
            _QUOTE_TARGET_ = _QUOTE_RESERVE_;
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144C8-L148C10

```
 if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
            revert ErrFlashLoanFailed();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302C8-L304C10

```
  if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549C7-L549C78

## [G‑05]	Operator >=/<= costs less gas than operator >/<

```
  if (totalPoolShares < minAmountOut) {
            revert ErrInsufficientAmountOut();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L108C7-L110C10

```
   if (i == 0 || i > MAX_I) {
            revert ErrInvalidI();
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L108C6-L109C34

```
 if (k > MAX_K) {
            revert ErrInvalidK();
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L111C8-L112C34

```
if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {
            revert ErrInvalidLPFeeRate();
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L114C9-L115C42

```
  if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139C7-L139C97

```
  if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144C7-L144C99

```
 if (data.length > 0) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L294C8-L294C31

```
 if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302C8-L302C78

```
  if (baseBalance < _BASE_RESERVE_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L308C7-L308C44

```
 if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L315C12-L315C77

```
   if (quoteBalance < _QUOTE_RESERVE_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L330C6-L330C46

```
   if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L337C10-L337C80

```
   shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L381C10-L381C132

```
     } else if (baseReserve > 0 && quoteReserve > 0) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395C4-L395C58

```
  uint256 mintRatio = quoteInputRatio < baseInputRatio ? quoteInputRatio : baseInputRatio;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L399

```
  if (deadline < block.timestamp) {
            revert ErrExpired();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L421C7-L423C10

```
  if (shareAmount > balanceOf(msg.sender)) {
            revert ErrNotEnough();
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L424C7-L425C35

```
   if (baseAmount < baseMinAmount || quoteAmount < quoteMinAmount) {
            revert ErrWithdrawNotEnough();
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L441C6-L442C43

```
 if (data.length > 0) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L450C8-L450C31

```
 if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
            revert ErrReserveAmountNotEnough();
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L480C8-L481C48

```
 if (newI == 0 || newI > MAX_I) {
            revert ErrInvalidI();
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L483C8-L484C34

```
 if (newK > MAX_K) {
            revert ErrInvalidK();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L486C8-L488C10

```
 if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {
            revert ErrInvalidLPFeeRate();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L489C8-L491C10

```
  if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549C7-L549C78

```
 if (remainder > 0) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L22C8-L22C29

```
   if (V2 > V1) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L200C6-L200C23

```
 if (payBaseAmount < backToOnePayBase) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L50C12-L50C52

```
    if (receiveQuoteAmount > backToOneReceiveQuote) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L54C13-L54C66

```
  if (payQuoteAmount < backToOnePayQuote) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L86C11-L86C54

```
  if (receiveBaseAmount > backToOneReceiveBase) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L89C15-L89C64

```
  if (block.timestamp > deadline) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L48C7-L48C42

```
  shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L101C7-L101C128

```
   shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L138C10-L138C128

```
  } else if (baseReserve > 0 && quoteReserve > 0) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147C7-L147C58

```
   uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L523C10-L523C140

```
 if (quoteReserve > 0 && baseReserve > 0) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527C12-L527C55

```
 for (uint256 i = 0; i < iterations; ) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544C8-L544C48

```
   if (amountOut < minimumOut) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L573C6-L573C38

```
   if (pathLength > 256) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L590C6-L590C32

```
   if (quoteDecimals - baseDecimals > MAX_BASE_QUOTE_DECIMALS_DIFFERENCE) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L602C6-L602C81

```
      if (_lockDuration < MIN_LOCK_DURATION) {
            revert ErrInvalidLockDuration();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L123C3-L125C10

```
 if (_rewardsDuration < MIN_REWARDS_DURATION) {
            revert ErrInvalidRewardDuration();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L127C8-L129C10

```
  if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326C7-L326C121

```
 if (_remainingRewardTime < minRemainingTime) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L374

```
  if (block.timestamp < reward.periodFinish) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L379C7-L379C53

```
    if (amount < _remainingRewardTime) {
            revert ErrNotEnoughReward();
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L384C5-L385C41

```
   for (uint256 i; i < users.length; ) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405C6-L405C46

```
     if (index == lastLockIndex[user] && locks.length > 1) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L417C8-L417C68

```
  if (locks[index].unlockTime > block.timestamp) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L422C11-L422C61

```
   if (amount < minLockAmount) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L497C10-L497C42

```
   for (uint256 i; i < rewardTokens.length; ) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561C6-L561C53

```
 for (uint256 i; i < rewardTokens.length; ) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575C8-L575C53

```
  for (uint256 j; j < users.length; ) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580C11-L580C50

```
  for (uint256 i; i < rewardTokens.length; ) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614C7-L614C53

```
if (i < rewardItemLength) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L623C13-L623C40

```
   if (amount > 0) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L636C18-L636C38

## [G-06] Use a more recent version of solidity
Use a solidity version of at least 0.8.2 to get simple compiler automatic inlining 
Use a solidity version of at least 0.8.3 to get better struct packing and cheaper multiple storage reads 
Use a solidity version of at least 0.8.4 to get custom errors, which are cheaper at deployment than revert()/require() strings 
Use asolidity version of at least 0.8.10 to have external calls skip contract existence checks if the external call
has a return value.
In 0.8.15 the conditions necessary for inlining are relaxed. Benchmarks show that the change
significantly decreases the bytecode size (which impacts the deployment cost) while the effect on the
runtime gas usage is smaller.
In 0.8.17 prevent the incorrect removal of storage writes before calls to Yul functions that conditionally
terminate the external EVM call; Simplify the starting offset of zero-length operations to zero. More
efficient overflow checks for multiplication.

```
pragma solidity >=0.8.0;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2C1-L2C25


## [G-07] Use recent version of solidity 0.8.24

```
pragma solidity >=0.8.0;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2C1-L2C25