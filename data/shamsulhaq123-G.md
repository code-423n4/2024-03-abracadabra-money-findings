## Gas Optimization

## Summary

|No|Issue|Instence|
|--|-----|--------|
|[G-01]|Change public function visibility to external|20|
|[G-02]|Setting the constructor to payable|15|
|[G-03]| Use calldata instead of memory for function arguments that do not get mutated|21|
|[G-04]|Use hardcode address instead address(this)|39|
|[G-05]|Unnecessary look up in if condition|43|
|[G-06]|>= costs less gas than >|34|
|[G-07]| Use assembly to check for address(0) |25|
|[G-08]|Do not calculate constants|3|
|[G-09]|Modifiers are redundant if used only once or not used at all. (5 instances)|2|
|[G-10]|Use function instead of modifiers (4 instances)|4|
|[G-11]|Use Custom Errors instead of Revert Strings to save Gas|4|
|[G-12]|Empty Blocks Should Be Removed Or Emit Something|3|
|[G-13]| Counting down in for statements is more gas efficient|2|
|[G-14]| Nested for loops should be avoided due to high gas costs resulting from O^2 time complexity|1|
|[G-15]|Consider using OZ EnumerateSet in place of nested mappings|3|
|[G-16]|Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct, where appropriate|7|
|[G-17]|State variables only set in the constructor should be declared immutable|15|
|[G-18]|Use nested if and, avoid multiple check combinations|11|
|[G-19]|Default value initialization|4|
|[G-20]|Using bools for storage incurs overhead|5|
|[G-21]|address(this) can be stored in state variable that will ultimately cost less|43|
|[G-22]|Use assembly to emit events|51|
|[G-23]|Use assembly for loops|8|
|[G-24]|Should use arguments instead of state variable |51|
|[G-25]|Cache array length outside of loop|8|
|[G-26]|Use constants instead of type(uintx).max|3|
|[G-27]|Emitting constants wastes gas|51|
|[G-28]|Using this to access functions results in an external call, wasting gas|39|
|[G-29]|Using `delete` statement can save gas|2|
|[G-30]| Superfluous event fields|12|

## [G-01] Change public function visibility to external
Since the following public functions are not called from within the contract, their visibility can be made external for gas optimization.

```solidity

file: blast/BlastWrappers.sol

59  function init(bytes calldata data) public payable override 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59

```solidity

file: mimswap/MagicLP.sol

155  function name() public view override returns (string memory) {
        return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));
    }

    function symbol() public pure override returns (string memory) {
        return "MagicLP";
    }

    function decimals() public view override returns (uint8) {
        return IERC20Metadata(_BASE_TOKEN_).decimals();
    }

167  function querySellBase(
        address trader,
        uint256 payBaseAmount
    ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) 

180  function querySellQuote(
        address trader,
        uint256 payQuoteAmount
 
    ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) 

193 function getPMMState() public view returns (PMMPricing.PMMState memory state)

215   function getMidPrice() public view returns (uint256 midPrice) {
        return PMMPricing.getMidPrice(getPMMState());
    }

228   function getBaseInput() public view returns (uint256 input) {
        return _BASE_TOKEN_.balanceOf(address(this)) - uint256(_BASE_RESERVE_);
    }

232   function getQuoteInput() public view returns (uint256 input) 

470  function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155-L163
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L167
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L180
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L193
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L215
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L228-L232
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470

```solidity

file: mimswap/auxiliary/FeeRateModel.sol

57  function setImplementation(address implementation_) public onlyOwner

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57

```solidity

file: mimswap/periphery/Factory.sol

65   function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address) 


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65

```solidity

file: oracles/aggregators/MagicLpAggregator.sol

37 function latestAnswer() public view override returns (int256)

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L37

```solidity

file: staking/LockingMultiRewards.sol

150  function stake(uint256 amount, bool lock_) public whenNotPaused {
        _stakeFor(msg.sender, amount, lock_);
    }

    /// @notice Locks an existing unlocked balance.
155  function lock(uint256 amount) public whenNotPaused 

170     function withdraw(uint256 amount) public virtual

186  function withdrawWithRewards(uint256 amount) public virtual 

191  function getRewards() public virtual 

235   function totalSupply() public view returns (uint256) {
        return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);
    }

239  function balanceOf(address user) public view returns (uint256) 

253   function nextUnlockTime() public view returns (uint256) {
        return nextEpoch() + lockDuration;
    }

    function epoch() public view returns (uint256) {
        return (block.timestamp / rewardsDuration) * rewardsDuration;
    }

    function nextEpoch() public view returns (uint256) {
        return epoch() + rewardsDuration;
    }

    function remainingEpochTime() public view returns (uint256) {
        return nextEpoch() - block.timestamp;
    }

    function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {
        return MathLib.min(block.timestamp, _rewardData[rewardToken].periodFinish);
    }

    function rewardPerToken(address rewardToken) public view returns (uint256) {
        return _rewardPerToken(rewardToken, lastTimeRewardApplicable(rewardToken), totalSupply());
    }

277 function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

288   function earned(address user, address rewardToken) public view returns (uint256)

300   function addReward(address rewardToken) public onlyOwner 

361   function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L150-155
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L170
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L186
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L191
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L235-L239
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L253-L277
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L288
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361

## [G-02] Setting the constructor to payable
You can cut out 10 opcodes in the creation-time EVM bytecode if you declare a constructor payable. Making the constructor payable eliminates the need for an initial check of msg.value == 0 and saves 13 gas on deployment with no security risks.\

```solidity

file: blast/BlastDapp.sol

7  constructor()

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L7

```solidity

file: blast/BlastBox.sol

24  constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_)

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24

```solidity

file: blast/BlastGovernor.sol

15   constructor(address feeTo_, address _owner) OperatableV2(_owner) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15

```solidity

file: blast/BlastMagicLP.sol

23   constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23

```solidity

file: blast/BlastOnboarding.sol

58  constructor() Owned(msg.sender) 

84   constructor(BlastTokenRegistry registry_, address feeTo_) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L58
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L84

```solidity

file: BlastTokenRegistry.sol

12     constructor(address _owner) Owned(_owner) {}
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12

```solidity

file: blast/BlastWrappers.sol

20  constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory)

29 contract BlastMIMSwapFactory is Factory {
    constructor(
        address implementation_,
        IFeeRateModel maintainerFeeRateModel_,
        address owner_,
        address governor_
    )

47  constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_))
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L29
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L47

```solidity

file: mimswap/MagicLP.sol

84  constructor(address owner_) Owned(owner_) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84

```solidity

file: mimswap/auxiliary/FeeRateModel.sol

22   constructor(address maintainer_, address owner_) Owned(owner_) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22

```solidity

file: mimswap/periphery/Factory.sol

38   constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38

```solidity

file: mimswap/periphery/Router.sol

38  constructor(IWETH weth_, IFactory factory_) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38

```solidity

file: oracles/aggregators/MagicLpAggregator.sol

21  constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_)

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21

## [G-03] Use calldata instead of memory for function arguments that do not get mutated
When you specify a data location as memory, that value will be copied into memory. When you specify the location as calldata, the value will stay static within calldata. If the value is a large, complex type, using memory may result in extra memory expansion costs.

```solidity

file: blast/BlastGovernor.sol

53  function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
        (success, result) = to.call{value: value}(data);
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53

```solidity

file: blast/BlastMagicLP.sol

39   function version() external pure override returns (string memory) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L39

```solidity

file: blast/BlastOnboarding.sol

164  function claimTokenYields(address[] memory tokens) external onlyOwner 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164

```solidity

file: mimswap/MagicLP.sol

155  function name() public view override returns (string memory)

159  function symbol() public pure override returns (string memory

193   function getPMMState() public view returns (PMMPricing.PMMState memory state) 

236   function version() external pure virtual returns (string memory) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L159
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L193
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L236

```solidity

file: mimswap/libraries/PMMPricing.sol

39 function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR)

76   function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) 

104  function _ROneSellBaseToken(
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

147  function _RBelowSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )

162   function _RAboveSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )

175   function _RAboveSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )   

190   function adjustedTarget(PMMState memory state) internal pure 

203 function getMidPrice(PMMState memory state) internal pure returns (uint256)
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L39
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L76
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L104
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L119
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L134
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L147
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L162
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L175
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L190
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L203

```solidity

file: staking/LockingMultiRewards.sol

199 function rewardData(address token) external view returns (Reward memory) {
        return _rewardData[token];
    }

211   function balances(address user) external view returns (Balances memory) {
        return _balances[user];
    }

    function userRewardLock(address user) external view returns (RewardLock memory) {
        return _userRewardLock[user];
    }

219    function userLocks(address user) external view returns (LockedBalance[] memory)

397   function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators 

572    function _updateRewardsForUsers(address[] memory users) internal
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L211-L219
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L572

## [G-04] Use hardcode address instead address(this)
Instead of using address(this), it is more gas-efficient to pre-calculate and use the hardcoded address. Foundry’s script.sol and solmate’s LibRlp.sol contracts can help achieve this.

```solidity

file: blast/BlastBox.sol

99  BlastYields.configureDefaultClaimables(address(this));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L99

```solidity

file: blast/BlastGovernor.sol

21    BlastYields.configureDefaultClaimables(address(this));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L21

```solidity

file: blast/BlastMagicLP.sol

99  BlastYields.configureDefaultClaimables(address(this));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L99

```solidity

file: blast/BlastOnboarding.sol

59  BlastYields.configureDefaultClaimables(address(this));

102   token.safeTransferFrom(msg.sender, address(this), amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L59
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L102

```solidity

file: blast/BlastOnboardingBoot.sol

106    (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

117   staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
        staking.setOperator(address(this), true);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117-L18

```solidity

file: blast/BlastWrappers.sol

51   if (governor_ == address(this)) 

60   if (_governor == address(this))
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L51
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L60

```solidity

file: blast/libraries/BlastYields.sol

21  if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) 

26    emit LogBlastTokenClaimableEnabled(address(this), token);

31    emit LogBlastNativeClaimableEnabled(address(this));

39  return claimMaxGasYields(address(this), recipient);

52  return claimAllNativeYields(address(this), recipient);

71  amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L21
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L26
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L31
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L39
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L52
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L71

```solidity

file: mimswap/MagicLP.sol

262    _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));

268 uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

285  _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);

298    uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
299    uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

361  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
362  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this)

427  if (to == address(this))

431  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
432   uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

505 uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
506 uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

529   baseBalance = _BASE_TOKEN_.balanceOf(address(this));
530    quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

568   uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
569   uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

615  if (address(this) == address(implementation)) 

622  if (address(this) != address(implementation))
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L262
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L268
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L285
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L298-299
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L361-L362
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L427
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L431-L432 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L505-L506
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L529-L530
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L568-L569
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L615
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L622

```solidity

file: mimswap/periphery/Factory.sol

77  address(this)

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L77

```solidity

file: mimswap/periphery/Router.sol

92   address(weth).safeTransferFrom(address(this), clone, msg.value);

269  lp.safeTransferFrom(msg.sender, address(this), sharesIn);

282    lp.safeTransferFrom(msg.sender, address(this), sharesIn);

289  address(this),

298  address(this),

398   amountOut = _swap(address(this), path, directions, minimumOut);

444   amountOut = _sellBase(lp, address(this), minimumOut);

490  amountOut = _sellQuote(lp, address(this), minimumOut);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L269
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L289
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L298
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L398
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L444
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L490

```solidity

file: staking/LockingMultiRewards.sol

326  if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance)

367   rewardToken.safeTransferFrom(msg.sender, address(this), amount);

464  stakingToken.safeTransferFrom(msg.sender, address(this), amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L464

## [G-05] Unnecessary look up in if condition
If the || condition isn’t required, the second condition will have been looked up unnecessarily.

```solidity

file: blast/BlastOnboardingBoot.sol

79   if (!ready || claimed[user])

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L79

```solidity

file: mimswap/MagicLP.sol

102   if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
            revert ErrZeroAddress();
        }
        if (baseTokenAddress == quoteTokenAddress) {
            revert ErrBaseQuoteSame();
        }
        if (i == 0 || i > MAX_I) {
            revert ErrInvalidI();
        }
        if (k > MAX_K) {
            revert ErrInvalidK();
        }
114   if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) 

462  if (token == _BASE_TOKEN_ || token == _QUOTE_TOKEN_) 

480  if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
            revert ErrReserveAmountNotEnough();
        }
        if (newI == 0 || newI > MAX_I) {
            revert ErrInvalidI();
        }
        if (newK > MAX_K) {
            revert ErrInvalidK();
        }
489  if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE)

508  if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) 

532  if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max)
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L462
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L480-L489 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L532

```solidity

file: mimswap/periphery/Router.sol

39  if (address(weth_) == address(0) || address(factory_) == address(0)) 

599  if (baseDecimals == 0 || quoteDecimals == 0)
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L39
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L599

```solidity

file: staking/LockingMultiRewards.sol

490  if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime)
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L490

## [G‑06] >= costs less gas than >
The compiler uses opcodes GT and ISZERO for solidity code that uses >, but only requires LT for >=, which saves 3 gas

```solidity

file: blast/BlastOnboarding.sol

114  if (caps[token] > 0 && totals[token].total > caps[token])

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114

```solidity

file: mimswap/MagicLP.sol

108   if (i == 0 || i > MAX_I) 

111   if (k > MAX_K) 

114  if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) 

294  if (data.length > 0)

315  if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) 

337   if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount)

395 else if (baseReserve > 0 && quoteReserve > 0)

424  if (shareAmount > balanceOf(msg.sender))

450   if (data.length > 0)

483  if (newI == 0 || newI > MAX_I) {
            revert ErrInvalidI();
        }
486   if (newK > MAX_K)

489  if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE)

508  if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max)

532   if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) 

549    if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0)

582 if (amount > 0) 

588    if (amount > 0) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L108
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L111
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L114
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L294
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L315
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L337
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L424
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L450
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L483-L486
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L489
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L532
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L582
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L588

```solidity

file: mimswap/libraries/Math.sol

22   if (remainder > 0) 

141  return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);

174  if (bAbs >= part2) 

200  if (V2 > V1) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L22
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L141
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L174
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L200

```solidity

file: mimswap/libraries/PMMPricing.sol

54 if (receiveQuoteAmount > backToOneReceiveQuote) 

89  if (receiveBaseAmount > backToOneReceiveBase)
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L54
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L89

```solidity

file: mimswap/periphery/Router.sol

48  if (block.timestamp > deadline) 

147 else if (baseReserve > 0 && quoteReserve > 0) 

220   if (msg.value > wethAdjustedAmount) 

379   if ((directions >> lastLpIndex) & 1 == 0) 

527 if (quoteReserve > 0 && baseReserve > 0)

590 if (pathLength > 256)

602   if (pathLength > 256) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L48
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L220
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L379
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L590
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L602

```solidity

file: staking/LockingMultiRewards.sol

326   if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance)

417  if (locks[index].unlockTime > block.timestamp) 

422  if (locks[index].unlockTime > block.timestamp) 

636   if (amount > 0) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L417
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L422
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L636

## [G-07] Use assembly to check for address(0) 

```solidity

file: blast/BlastBox.sol

25   if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
        }
28   if (address(registry_) == address(0))

73  if (feeTo_ == address(0))
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L25-L28
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L73

```solidity

file: blast/BlastGovernor.sol

16  if (feeTo_ == address(0))

41  if(_feeTo == address(0)) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L16
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L41

```solidity

file: blast/BlastMagicLP.sol

24  if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
        }
27   if (address(registry_) == address(0)) 

81  if (feeTo_ == address(0))
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L24-L27
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L81

```solidity

file: blast/BlastOnboarding.sol

85  if (address(registry_) == address(0))

89   if (feeTo_ == address(0))

148 if (feeTo_ == address(0)) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L85
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L89
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L148

```solidity

file: blast/BlastOnboardingBoot.sol

97       if (pool != address(0)) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L97

```solidity

file: blast/BlastTokenRegistry.sol

15   if (token == address(0)) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L15

```solidity

file: blast/BlastWrappers.sol

21 if (governor_ == address(0)) 

35   if (governor_ == address(0)) 

48  if (governor_ == address(0)) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L21
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L35
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L48

```solidity

file: mimswap/MagicLP.sol

102 if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) 

393  _mint(address(0), 1001);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L393


```solidity

file: mimswap/auxiliary/FeeRateModel.sol

23  if (maintainer_ == address(0))

35   if (implementation == address(0))

47  if (maintainer_ == address(0)) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L23
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L35
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L47

```solidity

file: mimswap/periphery/Factory.sol

39  if (implementation_ == address(0))

42  if (address(maintainerFeeRateModel_) == address(0)) 

97  if (implementation_ == address(0))

106   if (address(maintainerFeeRateModel_) == address(0)) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L39
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L42
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L97
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L106

```solidity

file: mimswap/periphery/Router.sol

39   if (address(weth_) == address(0) || address(factory_) == address(0)) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L39

```solidity

file: staking/LockingMultiRewards.sol

301  if (rewardToken == address(0))

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L301

## [G-08] Do not calculate constants
Due to how constant variables are implemented (replacements at compile-time), an expression assigned to a constant variable is recomputed each time that the variable is used, which wastes some gas.

```solidity

file: blast/BlastOnboardingBoot.sol

13 address constant USDB = 0x4300000000000000000000000000000000000003;
 address constant MIM = 0x76DA31D7C9CbEAE102aff34D3398bC450c8374c1;
 uint256 constant FEE_RATE = 0.0005 ether; // 0.05%
 uint256 constant K = 0.00025 ether; // 0.00025, 1.25% price fluctuation, similar to A2000 in curve
 uint256 constant I = 0.998 ether; // 1 MIM = 0.998 USDB
 uint256 constant USDB_TO_MIN = 1.002 ether; // 1 USDB = 1.002 MIM
19 uint256 constant MIM_TO_MIN = I;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L13

```solidity

file: mimswap/MagicLP.sol

63  uint256 public constant MAX_I = 10 ** 36;
    uint256 public constant MAX_K = 10 ** 18;
    uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%
66  uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63-L66

```solidity

file: mimswap/libraries/DecimalMath.sol

20  uint256 internal constant ONE = 10 ** 18;
21 uint256 internal constant ONE2 = 10 ** 36;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20

## [G-09] Modifiers are redundant if used only once or not used at all. (5 instances)
• Deployment. Gas Saved: 33 649
• Minumal Method Call. Gas Saved: -202
• Average Method Call. Gas Saved: 2 700
• Maximum Method Call. Gas Saved: 4 931

```solidity

file: blast/BlastOnboarding.sol

43   modifier onlyState(State _state) {
        if (state != _state) {
            revert ErrWrongState();
        }
        _;
    }

50    modifier onlySupportedTokens(address token) {
        if (!supportedTokens[token]) {
            revert ErrUnsupportedToken();
        }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L43-L50

```solidity

file: mimswap/MagicLP.sol

607    modifier onlyImplementationOwner() {
        if (msg.sender != implementation.owner()) {
            revert ErrNotImplementationOwner();
        }
        _;
    }

    modifier onlyClones() {
        if (address(this) == address(implementation)) {
            revert ErrNotClone();
        }
        _;
    }

621    modifier onlyImplementation() {
        if (address(this) != address(implementation)) {
            revert ErrNotImplementation();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L607-L621

## [G-10] Use function instead of modifiers (4 instances)
Deployment. Gas Saved: 115 926
Minimum Method Call. Gas Saved: 162
Average Method Call. Gas Saved: -264
Maximum Method Call. Gas Saved: -481
Overall gas change: 734 (2.459%)

```solidity

file: blast/BlastMagicLP.sol

118   modifier onlyImplementationOperators() 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L118

```solidity

file: blast/BlastOnboarding.sol

43   modifier onlyState(State _state) {
        if (state != _state) {
            revert ErrWrongState();
        }
        _;
    }

50    modifier onlySupportedTokens(address token) {
        if (!supportedTokens[token]) {
            revert ErrUnsupportedToken();
        }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L43-L50

```solidity

file: mimswap/MagicLP.sol

607    modifier onlyImplementationOwner() {
        if (msg.sender != implementation.owner()) {
            revert ErrNotImplementationOwner();
        }
        _;
    }

    modifier onlyClones() {
        if (address(this) == address(implementation)) {
            revert ErrNotClone();
        }
        _;
    }

621    modifier onlyImplementation() {
        if (address(this) != address(implementation)) {
            revert ErrNotImplementation();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L607-L621

```solidity

file: mimswap/periphery/Router.sol

47  modifier ensureDeadline(uint256 deadline) {
        if (block.timestamp > deadline) {
            revert ErrExpired();
        }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L47

## [G-11] Use Custom Errors instead of Revert Strings to save Gas

```solidity

file: blast/BlastMagicLP.sol

40  return "BlastMagicLP 1.0.0";
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L40

```solidity

file: mimswap/MagicLP.sol

156  return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));

160  return "MagicLP";

237  return "MagicLP 1.0.0";
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L156
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L160
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L237

## [G-12] Empty Blocks Should Be Removed Or Emit Something
The code should be refactored such that they no longer exist, or the block should do something useful, such as emitting an event or reverting. If the contract is meant to be extended, the contract should be abstract and the function signatures be added without any default implementation. If the block is an empty if-statement block to avoid doing subsequent checks in the else-if/else conditions, the else-if/else conditions should be nested under the negation of the if-statement, because they involve different classes of checks, which may lead to the introduction of errors when the code is later modified (if(x){}else if(y){…}else{…} => if(!x){if(y){…}else{…}})

```solidity

file: blast/BlastGovernor.sol

13   receive() external payable {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L13

```solidity

file: blast/BlastTokenRegistry.sol

12     constructor(address _owner) Owned(_owner) {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12

```solidity

file: mimswap/MagicLP.sol

601   function _afterInitialized() internal virtual {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L601

```solidity

file: mimswap/periphery/Router.sol

36  receive() external payable {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L36

## [G‑13] Counting down in for statements is more gas efficient
Counting down is more gas efficient than counting up because neither we are making zero variable to non-zero variable and also we will get gas refund in the last transaction when making non-zero to zero variable.

```solidity

file: blast/BlastOnboarding.sol

165  for (uint256 i = 0; i < tokens.length; i++) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165

```solidity

file: mimswap/periphery/Router.sol


544   for (uint256 i = 0; i < iterations; )

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544

## [G-14] Nested for loops should be avoided due to high gas costs resulting from O^2 time complexity
In Solidity, avoiding nested for loops is a recommended practice primarily due to the high gas costs associated with them. These loops can lead to quadratic (O^2) time complexity, especially when they iterate over large data sets or perform complex computations. Since every operation in a smart contract consumes gas, and users pay for this gas, optimizing for lower gas usage is crucial. Nested loops, which inherently have higher computational complexity, can significantly increase the gas costs of a contract. To optimize for efficiency, it's advisable to minimize the use of loops, limit their range, and reduce computations within each loop iteration. Alternative patterns like map/filter/reduce might often be cheaper than traditional for loops in terms of gas usage

```solidity

file: staking/LockingMultiRewards.sol

575  for (uint256 i; i < rewardTokens.length; ) {
            address token = rewardTokens[i];
            uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);

            // Record each user's rewards
            for (uint256 j; j < users.length; ) {
                address user = users[j];
                _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);

                unchecked {
                    ++j;
                }
            }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575

## [G-15] Consider using OZ EnumerateSet in place of nested mappings
Nested mappings and multi-dimensional arrays in Solidity operate through a process of double hashing, wherein the original storage slot and the first key are concatenated and hashed, and then this hash is again concatenated with the second key and hashed. This process can be quite gas expensive due to the double-hashing operation and subsequent storage operation (sstore).
A possible optimization involves manually concatenating the keys followed by a single hash operation and an sstore. However, this technique introduces the risk of storage collision, especially when there are other nested hash maps in the contract that use the same key types. Because Solidity is unaware of the number and structure of nested hash maps in a contract, it follows a conservative approach in computing the storage slot to avoid possible collisions.
OpenZeppelin's EnumerableSet provides a potential solution to this problem. It creates a data structure that combines the benefits of set operations with the ability to enumerate stored elements, which is not natively available in Solidity. EnumerableSet handles the element uniqueness internally and can therefore provide a more gas-efficient and collision-resistant alternative to nested mappings or multi-dimensional arrays in certain scenarios.

```solidity

file: blast/BlastOnboarding.sol

41    mapping(address user => mapping(address token => Balances)) public balances;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L41

```solidity

file: mimswap/periphery/Factory.sol

35  mapping(address base => mapping(address quote => address[] pools)) public pools;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L35

```solidity

file: staking/LockingMultiRewards.sol

94  mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
95 mapping(address user => mapping(address token => uint256 amount)) public rewards

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L94-L95

## [G-16] Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct, where appropriate
Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (20000 gas) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save ~42 gas per access due to not having to recalculate the key’s keccak256 hash (Gkeccak256 - 30 gas) and that calculation’s associated stack operations.

```solidity

file: blast/BlastBox.sol

21   mapping(address => bool) public enabledTokens;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21

```solidity

file: blast/BlastMagicLP.sol

21  mapping(address => bool) public operators;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L21

```solidity

file: blast/BlastOnboarding.sol

36  mapping(address token => bool) public supportedTokens;
    mapping(address token => Balances) public totals;
    mapping(address token => uint256 cap) public caps;

    // Per-user
41 mapping(address user => mapping(address token => Balances)) public balances;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36-L41


```solidity

file: blast/BlastOnboardingBoot.sol

30   mapping(address user => bool claimed) public claimed

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L30

```solidity

file: blast/BlastTokenRegistry.sol

10   mapping(address => bool) public nativeYieldTokens;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10

```solidity

file: mimswap/periphery/Factory.sol

35 mapping(address base => mapping(address quote => address[] pools)) public pools;
36 mapping(address creator => address[] pools) public userPools;


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L35-L36

```solidity

file: staking/LockingMultiRewards.sol

89  mapping(address token => Reward info) private _rewardData;
    mapping(address user => Balances balances) private _balances;
    mapping(address user => LockedBalance[] locks) private _userLocks;
    mapping(address user => RewardLock rewardLock) private _userRewardLock;

    mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
    mapping(address user => mapping(address token => uint256 amount)) public rewar
96  mapping(address user => uint256 index) public lastLockIndex;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L89-L96

## [G-17] State variables only set in the constructor should be declared immutable

```solidity

file: blast/BlastDapp.sol

7  constructor()

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L7

```solidity

file: blast/BlastBox.sol

24  constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_)

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24

```solidity

file: blast/BlastGovernor.sol

15   constructor(address feeTo_, address _owner) OperatableV2(_owner) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15

```solidity

file: blast/BlastMagicLP.sol

23   constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23

```solidity

file: blast/BlastOnboarding.sol

58  constructor() Owned(msg.sender) 

84   constructor(BlastTokenRegistry registry_, address feeTo_) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L58
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L84

```solidity

file: BlastTokenRegistry.sol

12     constructor(address _owner) Owned(_owner) {}
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12

```solidity

file: blast/BlastWrappers.sol

20  constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory)

29 contract BlastMIMSwapFactory is Factory {
    constructor(
        address implementation_,
        IFeeRateModel maintainerFeeRateModel_,
        address owner_,
        address governor_
    )

47  constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_))
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L29
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L47

```solidity

file: mimswap/MagicLP.sol

84  constructor(address owner_) Owned(owner_) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84

```solidity

file: mimswap/auxiliary/FeeRateModel.sol

22   constructor(address maintainer_, address owner_) Owned(owner_) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22

```solidity

file: mimswap/periphery/Factory.sol

38   constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38

```solidity

file: mimswap/periphery/Router.sol

38  constructor(IWETH weth_, IFactory factory_) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38

```solidity

file: oracles/aggregators/MagicLpAggregator.sol

21  constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_)

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21

## [G-18] Use nested if and, avoid multiple check combinations
Using nested is cheaper than using && multiple check combinations. There are more advantages, such as easier to read code and better coverage reports.

```solidity

file: blast/BlastMagicLP.sol

119   if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner())

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119

```solidity

file: blast/BlastOnboarding.sol

114   if (caps[token] > 0 && totals[token].total > caps[token])

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114

```solidity

file: mimswap/MagicLP.sol

139   if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) 

144   if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) 

302  if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) 

395 else if (baseReserve > 0 && quoteReserve > 0) 

549  if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549

```solidity

file: mimswap/periphery/Router.sol

147 else if (baseReserve > 0 && quoteReserve > 0)

527   if (quoteReserve > 0 && baseReserve > 0)
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527

```solidity

file: staking/LockingMultiRewards.sol

326   if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) 

417     if (index == lastLockIndex[user] && locks.length > 1) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L417

## [G-19] Default value initialization
Problem
If a variable is not set/initialized, it is assumed to have the default value (0, false, 0x0 etc depending on the data type).
Explicitly initializing it with its default value is an anti-pattern and wastes gas.

```solidity

file: blast/BlastOnboarding.sol

165  for (uint256 i = 0; i < tokens.length; i++) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165

```solidity

file: mimswap/libraries/Math.sol

154   temp = 0;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L154

```solidity

file: mimswap/periphery/Router.sol

544 for (uint256 i = 0; i < iterations; ) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544

```solidity

file: staking/LockingMultiRewards.sol

619    rewards[user][rewardToken] = 0;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L619

## [G‑20] Using bools for storage incurs overhead
    // Booleans are more expensive than uint256 or any type that takes up a full
    // word because each write operation emits an extra SLOAD to first read the
    // slot's contents, replace the bits taken up by the boolean, and then write
    // back. This is the compiler's defense against contract upgrades and
    // pointer aliasing, and it cannot be disabled.

```solidity

file: blast/BlastBox.sol

21   mapping(address => bool) public enabledTokens;


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21

```solidity

file: blast/BlastMagicLP.sol

21  mapping(address => bool) public operators;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L21

```solidity

file: blast/BlastOnboarding.sol

36  mapping(address token => bool) public supportedTokens;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36

```solidity

file: blast/BlastOnboardingBoot.sol

30   mapping(address user => bool claimed) public claimed

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L30

```solidity

file: blast/BlastTokenRegistry.sol

10   mapping(address => bool) public nativeYieldTokens;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10

## [G-21] address(this) can be stored in state variable that will ultimately cost less
than every time calculating this specifically when it used multiple times in a contrac
```solidity

file: blast/BlastBox.sol

99  BlastYields.configureDefaultClaimables(address(this));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L99

```solidity

file: blast/BlastGovernor.sol

21    BlastYields.configureDefaultClaimables(address(this));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L21

```solidity

file: blast/BlastMagicLP.sol

99  BlastYields.configureDefaultClaimables(address(this));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L99

```solidity

file: blast/BlastOnboarding.sol

59  BlastYields.configureDefaultClaimables(address(this));

102   token.safeTransferFrom(msg.sender, address(this), amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L59
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L102

```solidity

file: blast/BlastOnboardingBoot.sol

106    (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

117   staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
        staking.setOperator(address(this), true);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117-L18

```solidity

file: blast/BlastWrappers.sol

51   if (governor_ == address(this)) 

60   if (_governor == address(this))
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L51
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L60

```solidity

file: blast/libraries/BlastYields.sol

21  if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) 

26    emit LogBlastTokenClaimableEnabled(address(this), token);

31    emit LogBlastNativeClaimableEnabled(address(this));

39  return claimMaxGasYields(address(this), recipient);

52  return claimAllNativeYields(address(this), recipient);

71  amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L21
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L26
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L31
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L39
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L52
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L71

```solidity

file: mimswap/MagicLP.sol

262    _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));

268 uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

285  _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);

298    uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
299    uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

361  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
362  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this)

427  if (to == address(this))

431  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
432   uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

505 uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
506 uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

529   baseBalance = _BASE_TOKEN_.balanceOf(address(this));
530    quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

568   uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
569   uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

615  if (address(this) == address(implementation)) 

622  if (address(this) != address(implementation))
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L262
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L268
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L285
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L298-299
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L361-L362
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L427
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L431-L432 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L505-L506
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L529-L530
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L568-L569
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L615
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L622

```solidity

file: mimswap/periphery/Factory.sol

77  address(this)

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L77

```solidity

file: mimswap/periphery/Router.sol

92   address(weth).safeTransferFrom(address(this), clone, msg.value);

269  lp.safeTransferFrom(msg.sender, address(this), sharesIn);

282    lp.safeTransferFrom(msg.sender, address(this), sharesIn);

289  address(this),

298  address(this),

398   amountOut = _swap(address(this), path, directions, minimumOut);

444   amountOut = _sellBase(lp, address(this), minimumOut);

490  amountOut = _sellQuote(lp, address(this), minimumOut);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L269
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L289
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L298
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L398
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L444
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L490

```solidity

file: staking/LockingMultiRewards.sol

326  if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance)

367   rewardToken.safeTransferFrom(msg.sender, address(this), amount);

464  stakingToken.safeTransferFrom(msg.sender, address(this), amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L464

## [G-22] Use assembly to emit events
We can use assembly to emit events efficiently by utilizing `scratch space` and the `free memory pointer`. This will allow us to potentially avoid memory expansion costs. Note: In order to do this optimization safely, we will need to cache and restore the free memory pointer.

```solidity

file: blast/BlastBox.sol

78  emit LogFeeToChanged(feeTo_);

90   emit LogTokenDepositEnabled(token, enabled);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L78
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L90

```solidity

file: blast/BlastGovernor.sol

46    emit LogFeeToChanged(_feeTo);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L46

```solidity

file: blast/BlastMagicLP.sol

86   emit LogFeeToChanged(feeTo_);

91 emit LogOperatorChanged(operator, status);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L86
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L91

```solidity

file: blast/BlastOnboarding.sol

120  emit LogDeposit(msg.sender, token, amount, lock_);

129  emit LogLock(msg.sender, token, amount);

140    emit LogWithdraw(msg.sender, token, amount);

153  emit LogFeeToChanged(feeTo_);

182    emit LogTokenSupported(token, supported);
    }

    function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
        caps[token] = cap;
        emit LogTokenCapChanged(token, cap);
    }

    function setBootstrapper(address bootstrapper_) external onlyOwner {
        bootstrapper = bootstrapper_;
        emit LogBootstrapperChanged(bootstrapper_);
    }

    function open() external onlyOwner onlyState(State.Idle) {
        state = State.Opened;
        emit LogStateChange(State.Opened);
    }

    function close() external onlyOwner onlyState(State.Opened) {
        state = State.Closed;
202   emit LogStateChange(State.Clo

211   emit LogTokenRescue(token, to, amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L120
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L129
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L140
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L153
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L182-L202
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L211

```solidity

file: last/BlastOnboardingBoot.sol

71  emit LogClaimed(msg.sender, shares, lock);

124  emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

132  emit LogInitialized(_router);

143  emit LogStakingChanged(address(_staking));

148    emit LogReadyChanged(ready);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L71
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L132
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L143
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148

```solidity

file: blast/BlastTokenRegistry.sol

20         emit LogNativeYieldTokenEnabled(token, enabled);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L20

```solidity

file: blast/libraries/BlastYields.sol

26     emit LogBlastTokenClaimableEnabled(address(this), token);
    
31        emit LogBlastNativeClaimableEnabled(address(this));

44  emit LogBlastGasClaimed(recipient, amount);

57  emit LogBlastETHClaimed(recipient, amount);

62  emit LogBlastETHClaimed(recipient, amount);

72  emit LogBlastTokenClaimed(recipient, address(token), amount);

77    emit LogBlastTokenClaimed(recipient, address(token), amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L26-L31 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L44
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L57
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L62
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L72
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L77

```solidity

file: mimswap/MagicLP.sol

259  emit RChange(newRState);

264  emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

282  emit RChange(newRState);

287  emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

323  emit RChange(newRState);
325  emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);  

345     emit RChange(newRState);
            }
            emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
        }

352    emit FlashLoan(msg.sender, assetTo, baseAmount, quoteAmount);

409 emit BuyShares(to, shares, balanceOf(to));

454  emit SellShares(msg.sender, to, shareAmount, balanceOf(msg.sender));

467  emit TokenRescue(token, to, amount);

501 
```
https://github.com/code-423n4/2024-03-abracadabra-  emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);money/blob/main/src/mimswap/MagicLP.sol#L259
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L264
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L282
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L287
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L323-L325
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L345-L352 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L409
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L454
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L467
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L501

```solidity

file: mimswap/auxiliary/FeeRateModel.sol

52   emit LogMaintainerChanged(maintainer_);

59  emit LogImplementationChanged(implementation_);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L52
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L59

```solidity

file: mimswap/periphery/Factory.sol

88         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);

102 emit LogSetImplementation(implementation_);

111    emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);

141   emit LogPoolRemoved(pool);

152  emit LogPoolAdded(baseToken, quoteToken, creator, pool);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L102
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L111
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L141
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L152

```solidity

file: staking/LockingMultiRewards.sol

183     emit LogWithdrawn(msg.sender, amount);

318    emit LogSetMinLockAmount(minLockAmount, _minLockAmount);

331    emit LogRecovered(tokenAddress, tokenAmount);

392  emit LogRewardAdded(amount);

436  emit LogLockIndexChanged(user, lastIndex, index);

447   emit LogUnlocked(user, amount, index);

475  emit LogStaked(account, amount);

513  emit LogLocked(user, amount, _nextUnlockTime, lockCount);

611   emit LogRewardLockCreated(user, _rewardLock.unlockTime);

638   emit LogRewardPaid(user, rewardToken, amount);

651   emit LogRewardLocked(user, rewardToken, rewardAmount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L183
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L318
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L331
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L392
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L436
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L447
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L475
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L513
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L611
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L638
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L651

## [G-23]  Use assembly for loops
In the following instances, assembly is used for more gas efficient loops.

```solidity

file: blast/BlastOnboarding.sol

165  for (uint256 i = 0; i < tokens.length; i++)
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165


```solidity

file: mimswap/periphery/Router.sol

544  for (uint256 i = 0; i < iterations; ) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544

```solidity

file: staking/LockingMultiRewards.sol

405   for (uint256 i; i < users.length; ) 

547   for (uint256 i; i < rewardTokens.length; ) 

561   for (uint256 i; i < rewardTokens.length; ) 

575  for (uint256 i; i < rewardTokens.length; ) 

580  for (uint256 j; j < users.length; ) 

614  for (uint256 i; i < rewardTokens.length; )
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614

## [G-24] Should use arguments instead of state variable 

state variables should not used in emit  ,  This will save near 97 gas  

```solidity

file: blast/BlastBox.sol

78  emit LogFeeToChanged(feeTo_);

90   emit LogTokenDepositEnabled(token, enabled);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L78
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L90

```solidity

file: blast/BlastGovernor.sol

46    emit LogFeeToChanged(_feeTo);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L46

```solidity

file: blast/BlastMagicLP.sol

86   emit LogFeeToChanged(feeTo_);

91 emit LogOperatorChanged(operator, status);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L86
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L91

```solidity

file: blast/BlastOnboarding.sol

120  emit LogDeposit(msg.sender, token, amount, lock_);

129  emit LogLock(msg.sender, token, amount);

140    emit LogWithdraw(msg.sender, token, amount);

153  emit LogFeeToChanged(feeTo_);

182    emit LogTokenSupported(token, supported);
    }

    function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
        caps[token] = cap;
        emit LogTokenCapChanged(token, cap);
    }

    function setBootstrapper(address bootstrapper_) external onlyOwner {
        bootstrapper = bootstrapper_;
        emit LogBootstrapperChanged(bootstrapper_);
    }

    function open() external onlyOwner onlyState(State.Idle) {
        state = State.Opened;
        emit LogStateChange(State.Opened);
    }

    function close() external onlyOwner onlyState(State.Opened) {
        state = State.Closed;
202   emit LogStateChange(State.Clo

211   emit LogTokenRescue(token, to, amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L120
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L129
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L140
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L153
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L182-L202
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L211

```solidity

file: last/BlastOnboardingBoot.sol

71  emit LogClaimed(msg.sender, shares, lock);

124  emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

132  emit LogInitialized(_router);

143  emit LogStakingChanged(address(_staking));

148    emit LogReadyChanged(ready);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L71
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L132
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L143
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148

```solidity

file: blast/BlastTokenRegistry.sol

20         emit LogNativeYieldTokenEnabled(token, enabled);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L20

```solidity

file: blast/libraries/BlastYields.sol

26     emit LogBlastTokenClaimableEnabled(address(this), token);
    
31        emit LogBlastNativeClaimableEnabled(address(this));

44  emit LogBlastGasClaimed(recipient, amount);

57  emit LogBlastETHClaimed(recipient, amount);

62  emit LogBlastETHClaimed(recipient, amount);

72  emit LogBlastTokenClaimed(recipient, address(token), amount);

77    emit LogBlastTokenClaimed(recipient, address(token), amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L26-L31 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L44
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L57
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L62
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L72
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L77

```solidity

file: mimswap/MagicLP.sol

259  emit RChange(newRState);

264  emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

282  emit RChange(newRState);

287  emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

323  emit RChange(newRState);
325  emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);  

345     emit RChange(newRState);
            }
            emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
        }

352    emit FlashLoan(msg.sender, assetTo, baseAmount, quoteAmount);

409 emit BuyShares(to, shares, balanceOf(to));

454  emit SellShares(msg.sender, to, shareAmount, balanceOf(msg.sender));

467  emit TokenRescue(token, to, amount);

501 
```
https://github.com/code-423n4/2024-03-abracadabra-  emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);money/blob/main/src/mimswap/MagicLP.sol#L259
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L264
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L282
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L287
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L323-L325
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L345-L352 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L409
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L454
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L467
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L501

```solidity

file: mimswap/auxiliary/FeeRateModel.sol

52   emit LogMaintainerChanged(maintainer_);

59  emit LogImplementationChanged(implementation_);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L52
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L59

```solidity

file: mimswap/periphery/Factory.sol

88         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);

102 emit LogSetImplementation(implementation_);

111    emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);

141   emit LogPoolRemoved(pool);

152  emit LogPoolAdded(baseToken, quoteToken, creator, pool);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L102
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L111
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L141
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L152

```solidity

file: staking/LockingMultiRewards.sol

183     emit LogWithdrawn(msg.sender, amount);

318    emit LogSetMinLockAmount(minLockAmount, _minLockAmount);

331    emit LogRecovered(tokenAddress, tokenAmount);

392  emit LogRewardAdded(amount);

436  emit LogLockIndexChanged(user, lastIndex, index);

447   emit LogUnlocked(user, amount, index);

475  emit LogStaked(account, amount);

513  emit LogLocked(user, amount, _nextUnlockTime, lockCount);

611   emit LogRewardLockCreated(user, _rewardLock.unlockTime);

638   emit LogRewardPaid(user, rewardToken, amount);

651   emit LogRewardLocked(user, rewardToken, rewardAmount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L183
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L318
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L331
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L392
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L436
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L447
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L475
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L513
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L611
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L638
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L651

## [G-25] Cache array length outside of loop
If not cached, the solidity compiler will always read the length of the array during each iteration. That is, if it is a storage array, this is an extra sload operation (100 additional extra gas for each iteration except for the first) and if it is a memory array, this is an extra mload operation (3 additional gas for each iteration except for the first).

```solidity

file: blast/BlastOnboarding.sol

165  for (uint256 i = 0; i < tokens.length; i++)
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165


```solidity

file: mimswap/periphery/Router.sol

544  for (uint256 i = 0; i < iterations; ) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544

```solidity

file: staking/LockingMultiRewards.sol

405   for (uint256 i; i < users.length; ) 

547   for (uint256 i; i < rewardTokens.length; ) 

561   for (uint256 i; i < rewardTokens.length; ) 

575  for (uint256 i; i < rewardTokens.length; ) 

580  for (uint256 j; j < users.length; ) 

614  for (uint256 i; i < rewardTokens.length; )
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614

## [G-26] Use constants instead of type(uintx).max

type(uint120).max or type(uint128).max, etc. it uses more gas in the distribution process and also for each transaction than constant usage.

```solidity

file: blast/BlastOnboardingBoot.sol

103  MIM.safeApprove(address(router), type(uint256).max);
104  USDB.safeApprove(address(router), type(uint256).max);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L103-L104


```solidity

file: mimswap/MagicLP.sol

508   if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max)

532  if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) 
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L532

## [G-27] Emitting constants wastes gas
Every event parameter costs Glogdata (8 gas) per byte. You can avoid this extra cost, in cases where you're emitting a constant, by creating a new version of the event which doesn't have the parameter (and have users look to the contract's variables for its value instead). Alternatively, in the case of boolean constants, two events can be created - one representing the true case and one representing the false case.

```solidity

file: blast/BlastBox.sol

78  emit LogFeeToChanged(feeTo_);

90   emit LogTokenDepositEnabled(token, enabled);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L78
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L90

```solidity

file: blast/BlastGovernor.sol

46    emit LogFeeToChanged(_feeTo);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L46

```solidity

file: blast/BlastMagicLP.sol

86   emit LogFeeToChanged(feeTo_);

91 emit LogOperatorChanged(operator, status);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L86
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L91

```solidity

file: blast/BlastOnboarding.sol

120  emit LogDeposit(msg.sender, token, amount, lock_);

129  emit LogLock(msg.sender, token, amount);

140    emit LogWithdraw(msg.sender, token, amount);

153  emit LogFeeToChanged(feeTo_);

182    emit LogTokenSupported(token, supported);
    }

    function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
        caps[token] = cap;
        emit LogTokenCapChanged(token, cap);
    }

    function setBootstrapper(address bootstrapper_) external onlyOwner {
        bootstrapper = bootstrapper_;
        emit LogBootstrapperChanged(bootstrapper_);
    }

    function open() external onlyOwner onlyState(State.Idle) {
        state = State.Opened;
        emit LogStateChange(State.Opened);
    }

    function close() external onlyOwner onlyState(State.Opened) {
        state = State.Closed;
202   emit LogStateChange(State.Clo

211   emit LogTokenRescue(token, to, amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L120
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L129
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L140
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L153
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L182-L202
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L211

```solidity

file: last/BlastOnboardingBoot.sol

71  emit LogClaimed(msg.sender, shares, lock);

124  emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

132  emit LogInitialized(_router);

143  emit LogStakingChanged(address(_staking));

148    emit LogReadyChanged(ready);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L71
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L132
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L143
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148

```solidity

file: blast/BlastTokenRegistry.sol

20         emit LogNativeYieldTokenEnabled(token, enabled);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L20

```solidity

file: blast/libraries/BlastYields.sol

26     emit LogBlastTokenClaimableEnabled(address(this), token);
    
31        emit LogBlastNativeClaimableEnabled(address(this));

44  emit LogBlastGasClaimed(recipient, amount);

57  emit LogBlastETHClaimed(recipient, amount);

62  emit LogBlastETHClaimed(recipient, amount);

72  emit LogBlastTokenClaimed(recipient, address(token), amount);

77    emit LogBlastTokenClaimed(recipient, address(token), amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L26-L31 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L44
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L57
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L62
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L72
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L77

```solidity

file: mimswap/MagicLP.sol

259  emit RChange(newRState);

264  emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

282  emit RChange(newRState);

287  emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

323  emit RChange(newRState);
325  emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);  

345     emit RChange(newRState);
            }
            emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
        }

352    emit FlashLoan(msg.sender, assetTo, baseAmount, quoteAmount);

409 emit BuyShares(to, shares, balanceOf(to));

454  emit SellShares(msg.sender, to, shareAmount, balanceOf(msg.sender));

467  emit TokenRescue(token, to, amount);

501 emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L259
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L264
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L282
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L287
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L323-L325
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L345-L352 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L409
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L454
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L467
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L501

```solidity

file: mimswap/auxiliary/FeeRateModel.sol

52   emit LogMaintainerChanged(maintainer_);

59  emit LogImplementationChanged(implementation_);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L52
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L59

```solidity

file: mimswap/periphery/Factory.sol

88         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);

102 emit LogSetImplementation(implementation_);

111    emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);

141   emit LogPoolRemoved(pool);

152  emit LogPoolAdded(baseToken, quoteToken, creator, pool);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L102
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L111
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L141
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L152

```solidity

file: staking/LockingMultiRewards.sol

183     emit LogWithdrawn(msg.sender, amount);

318    emit LogSetMinLockAmount(minLockAmount, _minLockAmount);

331    emit LogRecovered(tokenAddress, tokenAmount);

392  emit LogRewardAdded(amount);

436  emit LogLockIndexChanged(user, lastIndex, index);

447   emit LogUnlocked(user, amount, index);

475  emit LogStaked(account, amount);

513  emit LogLocked(user, amount, _nextUnlockTime, lockCount);

611   emit LogRewardLockCreated(user, _rewardLock.unlockTime);

638   emit LogRewardPaid(user, rewardToken, amount);

651   emit LogRewardLocked(user, rewardToken, rewardAmount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L183
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L318
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L331
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L392
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L436
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L447
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L475
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L513
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L611
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L638
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L651

## [G-28] Using this to access functions results in an external call, wasting gas
External calls have an overhead of 100 gas, which can be avoided by not referencing the function using this. Contracts are allowed to override their parents' functions and change the visibility from external to public, so make this change if it's required in order to call the function internally.

```solidity

file: blast/BlastBox.sol

99  BlastYields.configureDefaultClaimables(address(this));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L99

```solidity

file: blast/BlastGovernor.sol

21    BlastYields.configureDefaultClaimables(address(this));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L21

```solidity

file: blast/BlastMagicLP.sol

99  BlastYields.configureDefaultClaimables(address(this));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L99

```solidity

file: blast/BlastOnboarding.sol

59  BlastYields.configureDefaultClaimables(address(this));

102   token.safeTransferFrom(msg.sender, address(this), amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L59
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L102

```solidity

file: blast/BlastOnboardingBoot.sol

106    (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

117   staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
        staking.setOperator(address(this), true);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117-L18

```solidity

file: blast/BlastWrappers.sol

51   if (governor_ == address(this)) 

60   if (_governor == address(this))
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L51
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L60

```solidity

file: blast/libraries/BlastYields.sol

21  if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) 

26    emit LogBlastTokenClaimableEnabled(address(this), token);

31    emit LogBlastNativeClaimableEnabled(address(this));

39  return claimMaxGasYields(address(this), recipient);

52  return claimAllNativeYields(address(this), recipient);

71  amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L21
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L26
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L31
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L39
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L52
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L71

```solidity

file: mimswap/MagicLP.sol

262    _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));

268 uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

285  _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);

298    uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
299    uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

361  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
362  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this)

427  if (to == address(this))

431  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
432   uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

505 uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
506 uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

529   baseBalance = _BASE_TOKEN_.balanceOf(address(this));
530    quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

568   uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
569   uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

615  if (address(this) == address(implementation)) 

622  if (address(this) != address(implementation))
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L262
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L268
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L285
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L298-299
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L361-L362
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L427
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L431-L432 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L505-L506
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L529-L530
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L568-L569
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L615
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L622

```solidity

file: mimswap/periphery/Factory.sol

77  address(this)

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L77

```solidity

file: mimswap/periphery/Router.sol

92   address(weth).safeTransferFrom(address(this), clone, msg.value);

269  lp.safeTransferFrom(msg.sender, address(this), sharesIn);

282    lp.safeTransferFrom(msg.sender, address(this), sharesIn);

289  address(this),

298  address(this),

398   amountOut = _swap(address(this), path, directions, minimumOut);

444   amountOut = _sellBase(lp, address(this), minimumOut);

490  amountOut = _sellQuote(lp, address(this), minimumOut);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L269
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L289
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L298
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L398
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L444
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L490

```solidity

file: staking/LockingMultiRewards.sol

326  if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance)

367   rewardToken.safeTransferFrom(msg.sender, address(this), amount);

464  stakingToken.safeTransferFrom(msg.sender, address(this), amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L464

## [G-29] Using `delete` statement can save gas

```solidity


file: mimswap/libraries/Math.sol

154   temp = 0;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L154

```solidity

file: staking/LockingMultiRewards.sol

619    rewards[user][rewardToken] = 0;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L619

## [G-30] Superfluous event fields
`block.timestamp` and `block.number` are added to event information by default so adding them manually wastes gas

```solidity

file: mimswap/MagicLP.sol

125 _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

421   if (deadline < block.timestamp) 

546   uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L125
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L421
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L546

```solidity

file: mimswap/periphery/Router.sol

48 if (block.timestamp > deadline) 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L48

```solidity

file: staking/LockingMultiRewards.sol

258   return (block.timestamp / rewardsDuration) * rewardsDuration;

266  return nextEpoch() - block.timestamp;

270  return MathLib.min(block.timestamp, _rewardData[rewardToken].periodFinish);

372   uint256 _remainingRewardTime = _nextEpoch - block.timestamp;

379   if (block.timestamp < reward.periodFinish) 

389  reward.lastUpdateTime = uint248(block.timestamp);

422  if (locks[index].unlockTime > block.timestamp) 

602    bool expired = _rewardLock.unlockTime <= block.timestamp;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L258
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L266
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L270
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L372
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L379
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L389
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L422
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L602