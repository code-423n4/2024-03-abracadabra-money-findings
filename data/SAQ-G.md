## Summary

### Gas Optimization

no | Issue |Instances||
|-|:-|:-:|:-:|
| [G-01] | Internal functions only called once can be inlined to save gas | 12 | - |
| [G-02] | ptimize Names to save Gas | 6 | - |
| [G-03] | Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead | 6 | - |
| [G-04] | Using fixed bytes is cheaper than using string | 2 | - |
| [G-05] | Setting the constructor to `payable` | 5 | - |
| [G-06] | Multiple address /ID mappings can be combined into a single mapping of an address/ID to a struct , where appropriate | 4 | - |
| [G-07] |  State variables should be cached in stack variables rather than re-reading them from storage | 1 | - |
| [G-08] | Can make the variable outside the loop to save gas | 7 | - |
| [G-09] | Using `calldata` instead of `memory` for read-only arguments in external functions saves gas  | 2 | - |
| [G-10] | Public function not called by the contract should be declared external instead  | 5 | - |
| [G-11] | Use assembly to check for `address(0)` | 11 | - |
| [G-12] | Use bitmap to save gas | 1 | - |
| [G-13] | Empty blocks should be removed or emit something | 3 | - |
| [G-14] | Use constants instead of type(uintx).max | 4 | - |
| [G-15] | Use nested if and, avoid multiple check combinations | 3 | - |
| [G-16] | USE A MORE RECENT VERSION OF SOLIDITY | 22, All file | - |
| [G-17] | Do not calculate constant | 1 | - |
| [G-18] | Use assembly to emit events | 9 | - |
| [G-19] | Use assembly for math (add, sub, mul, div) | 2 | - |
| [G-20] | State variable read in a loop | 1 | - |
| [G-21] | Use uint256(1)/uint256(2) instead for `true` and `false` boolean states | 1 | - |
| [G-22] | bytes.concat() can be used in place of abi.encodePacked | 1 | - |
| [G-23] | Use assembly for small keccak256 hashes, in order to save gas  | 1 | - |
| [G-24] | Avoid fetching a low-level call's return data by using assembly  | 2 | - |
| [G-25] | Using assembly to check for zero can save gas | 8 | - |
| [G-26] | Use assembly to validate msg.sender | 3 | - |
| [G-27] | Pre-increment and pre-decrement are cheaper than + 1 ,- 1 | 3 | - |
| [G-28] | `do-while` is cheaper than `for-loops` when the initial check can be skipped | 6 | - |
| [G-29] | address(this) should be cached | 2 | - |


## Gas Optimizations  

## [G-01]  Internal functions only called once can be inlined to save gas


```solidity
file: /src/mimswap/MagicLP.sol

528    function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {

601    function _afterInitialized() internal virtual {} 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L528C1-L528C101


```solidity
file: /src/mimswap/libraries/DecimalMath.sol

47    function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L47C1-L47C83


```solidity
file: /src/mimswap/libraries/Math.sol

19    function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L19C1-L19C77


```solidity
file: /src/mimswap/libraries/PMMPricing.sol

134    function _RBelowSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {


147    function _RBelowSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {


162    function _RAboveSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {


175
    function _RAboveSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {          

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L134C1-L143C6

```solidity
file: /oracles/aggregators/MagicLpAggregator.sol

33    function _getReserves() internal view virtual returns (uint256, uint256) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L33C1-L33C79


```solidity
file: /src/staking/LockingMultiRewards.sol

272    function _updateRewardsForUsers(address[] memory users) internal {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L572C1-L572C71


```solidity
file: /blast/libraries/BlastYields.sol

42    function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {

55    function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L42C1-L42C111



## [G-02] Optimize Names to save Gas'

public/external function names and public member variable names can be optimized to save gas. See this link for an example of how it works. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, per sorted position shifted.


[MagicLP.sol](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L25C1-L25C52)


[BlastBox.sol](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L13C1-L13C46)

[BlastGovernor.sol](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L7)

[BlastOnboarding.sol](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L12)

[BlastOnboardingBoot.sol](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23)

[LockingMultiRewards.sol](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L14)


## [G-03] Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead         

When using elements that are smaller than 32 bytes, your contract's gas usage may be higher. This is because the EVM operates on 32 bytes at a time. Therefore, if the element is smaller than that, the EVM must use more operations in order to reduce the size of the element from 32 bytes to the desired size.

```solidity
file: /src/mimswap/MagicLP.sol

// @audit  uint8 

163    function decimals() public view override returns (uint8) {


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163C1-L163C63

```solidity 
file: /src/oracles/aggregators/MagicLpAggregator.sol

13    uint8 public immutable baseDecimals;

14    uint8 public immutable quoteDecimals;

29    function decimals() external pure override returns (uint8) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L13C1-L14C42

```solidity
file: /src/mimswap/MagicLP.sol

72    uint112 public _BASE_RESERVE_;

78    uint32 public _RState_;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72s


## [G-04] Using fixed bytes is cheaper than using string

As a rule of thumb, use bytes for arbitrary-length raw byte data and string for arbitrary-length string (UTF-8) data.
If you can limit the length to a certain number of bytes, always use one of bytes1 to bytes32 because they are much cheaper.


```solidity
file: /src/blast/BlastMagicLP.sol

39    function version() external pure override returns (string memory) {
        return "BlastMagicLP 1.0.0";
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L39C1-L42C1


```solidity
file: /src/mimswap/MagicLP.sol

236    function version() external pure virtual returns (string memory) {
        return "MagicLP 1.0.0";
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L236C1-L237C32


## [G-05] Setting the constructor to `payable`

You can cut out 10 opcodes in the creation-time EVM bytecode if you declare a constructor payable. Making the constructor payable eliminates the need for an initial check of msg.value == 0 and saves 13 gas on deployment with no security risks.


```solidity
file: /src/blast/BlastBox.sol

24    constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24C1-L24C94


```solidity
file: /src/blast/BlastGovernor.sol

15    constructor(address feeTo_, address _owner) OperatableV2(_owner) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15C1-L15C71


```solidity
file: /src/blast/BlastMagicLP.sol

23    constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23C1-L23C96


```solidity
file: src/mimswap/auxiliary/FeeRateModel.sol

22    constructor(address maintainer_, address owner_) Owned(owner_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22C1-L22C69


```solidity
file: /src/mimswap/periphery/Factory.sol

38    constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38C1-L38C112

## [G-06] Multiple address /ID mappings can be combined into a single mapping of an address/ID to a struct , where appropriate

```solidity
file: /src/staking/LockingMultiRewards.sol

89    mapping(address token => Reward info) private _rewardData;
90    mapping(address user => Balances balances) private _balances;
91    mapping(address user => LockedBalance[] locks) private _userLocks;
92    mapping(address user => RewardLock rewardLock) private _userRewardLock;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L89C1-L92C74


## [G-07] State variables should be cached in stack variables rather than re-reading them from storage

The instances below point to the second+ access of a state variable within a function.
Caching of a state variable replace each Gwarmaccess (100 gas) with a much cheaper stack read.
Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.
Most of the times this if statement will be true and we will save 100 gas at a small possibility of 3 gas loss ,

```solidity
file: /src/blast/BlastOnboardingBoot.sol

///@audit ' pool ' is state variable , stack should be used instead in this function for gas.

96   function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
        if (pool != address(0)) {                                   // FOUND
            revert ErrAlreadyBootstrapped();
        }

        uint256 baseAmount = totals[MIM].locked;
        uint256 quoteAmount = totals[USDB].locked;
        MIM.safeApprove(address(router), type(uint256).max);
        USDB.safeApprove(address(router), type(uint256).max);

        (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount); // FOUND

        if (totalPoolShares < minAmountOut) {
            revert ErrInsufficientAmountOut();
        }

        // Create staking contract
        // 3x boosting for locker, 7 days reward duration, 13 weeks lp locking
        // make this contract temporary the owner the set it as an operator
        // for permissionned `stakeFor` during the claiming process and then
        // transfer the ownership to the onboarding owner.
        staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));     // FOUND
        staking.setOperator(address(this), true);
        staking.transferOwnership(owner);

        // Approve staking contract
        pool.safeApprove(address(staking), totalPoolShares);     

        emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);   // FOUND

        return (pool, address(staking), totalPoolShares);         // FOUND
    }


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96C5-L128C1


## [G-08] Can make the variable outside the loop to save gas

Consider making the stack variables before the loop which gonna save gas

```solidity
file: /src/staking/LockingMultiRewards.sol

406            address user = users[i];
407            Balances storage bal = _balances[user];
408            LockedBalance[] storage locks = _userLocks[user];

414            uint256 index = lockIndexes[i];

562            address token = rewardTokens[i];

576            address token = rewardTokens[i];
577            uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L406C2-L408C62


## [G-09] Using `calldata` instead of `memory` for read-only arguments in external functions saves gas 

```solidity
file: /src/blast/BlastOnboarding.sol

164    function claimTokenYields(address[] memory tokens) external onlyOwner {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164C1-L164C76


```solidity
file: /src/staking/LockingMultiRewards.sol

397    function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397C1-L397C114


## [G-10] Public function not called by the contract should be declared external instead 

Contracts are allowed to override their parents' functions and change the visibility from external to public and can save gas by doing so.

```solidity
file: /src/mimswap/MagicLP.sol

470    function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470C1-L479C52


```solidity
file: /src/mimswap/auxiliary/FeeRateModel.sol

57    function setImplementation(address implementation_) public onlyOwner {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57C1-L57C75


```solidity
file: /src/staking/LockingMultiRewards.sol

265    function remainingEpochTime() public view returns (uint256) {

300    function addReward(address rewardToken) public onlyOwner { 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L265C1-L265C66


```solidity
file: /src/mimswap/MagicLP.sol

155    function name() public view override returns (string memory) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155C1-L155C67


## [G-11] Use assembly to check for `address(0)`

Save 6 gas per instance.

```solidity
file: /src/blast/BlastOnboardingBoot.sol

97        if (pool != address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L97C1-L97C34


```solidity
file: /src/blast/BlastBox.sol

25        if (feeTo_ == address(0)) {
    
28        if (address(registry_) == address(0)) {

73        if (feeTo_ == address(0)) { 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L25C1-L28C48


```solidity
file: /src/blast/BlastGovernor.sol

41        if(_feeTo == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L41C1-L41C35


```solidity
file: /src/blast/BlastMagicLP.sol

81        if (feeTo_ == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L81C1-L81C36



```solidity
file: /src/blast/BlastTokenRegistry.sol

15        if (token == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L15C1-L15C35


```solidity
file: /src/blast/BlastWrappers.solidity

35        if (governor_ == address(0)) { 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L35C1-L35C39

```solidity
file: /src/mimswap/MagicLP.sol

102        if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102C1-L102C113


```solidity
file: /src/mimswap/auxiliary/FeeRateModel.sol

35        if (implementation == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L35C1-L35C44

```solidity
file: /src/mimswap/periphery/Factory.sol

106        if (address(maintainerFeeRateModel_) == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L106C1-L106C62


## [G-12] Use bitmap to save gas

```solidity
file: /src/blast/BlastBox.sol

21    mapping(address => bool) public enabledTokens;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21C1-L21C51

## [G-13] Empty blocks should be removed or emit something

The gas cost of an empty constructor block in Solidity is typically in the range of 200-500 gas units. 

The code should be refactored such that they no longer exist, or the block should do something useful, such as emitting an event or reverting.

```solidity
file: /src/mimswap/MagicLP.sol

601    function _afterInitialized() internal virtual {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L601C1-L601C53


```solidity
file: /src/mimswap/periphery/Router.sol

36    receive() external payable {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L36C1-L36C34


```solidity
file: /src/blast/BlastTokenRegistry.sol

12    constructor(address _owner) Owned(_owner) {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12C1-L12C49



## [G-14] Use constants instead of type(uintx).max

type(uint120).max or type(uint128).max, etc. it uses more gas in the distribution process and also for each transaction than constant usage.


```solidity
file: /src/mimswap/MagicLP.sol

508        if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {

532        if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508C1-L508C83


```solidity
file: /src/blast/BlastOnboardingBoot.sol

103        MIM.safeApprove(address(router), type(uint256).max);

104        USDB.safeApprove(address(router), type(uint256).max);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L103C1-L104C62


## [G-15] Use nested if and, avoid multiple check combinations

Using nested if is cheaper than using && multiple check combinations. There are more advantages, such as easier to read code and better coverage reports.


```solidity
file: /src/mimswap/MagicLP.sol

549        if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549C1-L549C78

```solidity
file: /src/blast/BlastMagicLP.sol

119        if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119C1-L119C116


```solidity 
file: /src/blast/BlastOnboarding.sol

114        if (caps[token] > 0 && totals[token].total > caps[token]) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114C1-L114C68


## [G-16] USE A MORE RECENT VERSION OF SOLIDITY

#### Recommended
```
pragma solidity >=0.8.0; ==> pragma solidity 0.8.24;

```
*Instances*

```solidity
file: All files


2 pragma solidity >=0.8.0;


                  All fils have this instance.

```



## [G-17] Do not calculate constant

When you define a constant in Solidity, the compiler can calculate its value at compile-time and replace all references to the constant with its computed value. This can be helpful for readability and reducing the size of the compiled code, but it can also increase gas usage at runtime.

```solidity
file: /src/mimswap/MagicLP.sol

63    uint256 public constant MAX_I = 10 ** 36;
64    uint256 public constant MAX_K = 10 ** 18;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63C1-L64C46


## [G-18] Use assembly to emit events

We can use assembly to emit events efficiently by utilizing scratch space and the free memory pointer. This will allow us to potentially avoid memory expansion costs. Note: In order to do this optimization safely, we will need to cache and restore the free memory pointer.


```solidity
file: /src/blast/BlastOnboarding.sol

120        emit LogDeposit(msg.sender, token, amount, lock_);

129        emit LogLock(msg.sender, token, amount);

211        emit LogTokenRescue(token, to, amount);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L120C1-L120C59


```solidity 
file: /src/blast/BlastOnboardingBoot.sol

71        emit LogClaimed(msg.sender, shares, lock);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L71C1-L71C51


```solidity
file: /src/mimswap/periphery/Factory.sol

88        emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88C1-L88C110

```solidity
file: /src/blast/BlastBox.sol

78        emit LogFeeToChanged(feeTo_);

99        emit LogTokenDepositEnabled(token, enabled);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L78C1-L78C38


```solidity
file: /src/blast/BlastGovernor.sol

46        emit LogFeeToChanged(_feeTo);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L46C1-L46C38


```solidity
file: /src/blast/BlastMagicLP.sol
 
91        emit LogOperatorChanged(operator, status);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L91C1-L91C51


## [G-19] Use assembly for math (add, sub, mul, div)

Use assembly for math instead of Solidity. You can check for overflow/underflow in assembly to ensure safety. If using Solidity versions < 0.8.0 and you are using Safemath, you can gain significant gas savings by using assembly to calculate values and checking for overflow/underflow.

```solidity
file: /src/mimswap/libraries/DecimalMath.sol

53            uint p = powFloor(target, e / 2);
            p = (p * p) / ONE;
            if (e % 2 == 1) {
                p = (p * target) / ONE;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L53C1-L56C40


```solidity
file: /src/mimswap/libraries/Math.sol

153           if (idelta == 0) {
                temp = 0;
            } else if ((idelta * V1) / idelta == V1) {
                temp = (idelta * V1) / (V0 * V0);
            } else {
                temp = (((delta * V1) / V0) * i) / V0;
            }
            return (V1 * temp) / (temp + DecimalMath.ONE);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L153C2-L160C59


## [G-20] State variable read in a loop

State variable reads and writes are more expensive than local variable reads and writes. Therefore, it is recommended to replace state variable reads and writes within loops with local variable reads and writes.

```solidity
file: /src/blast/BlastOnboarding.sol

///@audit ' feeTo ' is state var.

170                 BlastYields.claimAllTokenYields(tokens[i], feeTo);    // FOUND

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L170C1-L170C67


## [G-21] Use uint256(1)/uint256(2) instead for `true` and `false` boolean states

If you don't use boolean for storage you will avoid Gwarmaccess 100 gas. In addition, state changes of boolean from true to false can cost up to ~20000 gas rather than uint256(2) to uint256(1) that would cost significantly less.

```solidity
file: /src/blast/BlastOnboardingBoot.sol

30    mapping(address user => bool claimed) public claimed;

68         claimed[msg.sender] = true;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L30C1-L30C58

## [G-22] bytes.concat() can be used in place of abi.encodePacked

Given concatenation is not going to be used for hashing bytes.concat is the preferred method to use as its more gas efficient

```solidity
file: /src/mimswap/periphery/Factory.sol

163        return keccak256(abi.encodePacked(sender_, implementation, baseToken_, quoteToken_, lpFeeRate_, i_, k_));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L163C1-L163C114


## [G-23] Use assembly for small keccak256 hashes, in order to save gas  

If the arguments to the encode call can fit into the scratch space (two words or fewer), then it's more efficient to use assembly to generate the hash (80 gas): `keccak256(abi.encodePacked(x, y))` -> `assembly {mstore(0x00, a); mstore(0x20, b); let hash := keccak256(0x00, 0x40); }`

```solidity
file: /src/mimswap/periphery/Factory.sol

163        return keccak256(abi.encodePacked(sender_, implementation, baseToken_, quoteToken_, lpFeeRate_, i_, k_));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L163C1-L163C114


## [G-24] Avoid fetching a low-level call's return data by using assembly

Even if you don't assign the call's second return value, it still gets copied to memory. Use assembly instead to prevent this and save 159 gas:
`(bool success,) = payable(receiver).call{gas: gas, value: value}("");` -> `bool success; assembly { success := call(gas, receiver, value, 0, 0, 0, 0) }`

```solidity
file: /src/blast/BlastGovernor.sol

54        (success, result) = to.call{value: value}(data);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L54C1-L54C57


```solidity
file: /src/blast/BlastBox.sol

69        BlastYields.callPrecompile(data);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L69C1-L69C42


## [G-25]  Using assembly to check for zero can save gas

Using assembly to check for zero can save gas by allowing more direct access to the evm and reducing some of the overhead associated with high-level operations in solidity.


```solidity
file: /src/staking/LockingMultiRewards.sol

156        if (amount == 0) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L156C1-L156C27

```solidity
file: /src/blast/BlastOnboardingBoot.sol

64        if (shares == 0) {

158        if (totalLocked == 0) { 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L64C1-L64C27


```solidity
file: /src/mimswap/MagicLP.sol

369        if (baseInput == 0) {

375        if (totalSupply() == 0) { 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L369C1-L369C30

```solidity
file: /src/mimswap/libraries/DecimalMath.sol

48        if (e == 0) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L48C1-L48C22


```solidity
file: /src/mimswap/periphery/Router.sol

545            if (directions & 1 == 0) {

560        if ((directions & 1 == 0)) { 

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L545C1-L545C39


## [G-26] Use assembly to validate msg.sender

We can use assembly to efficiently validate msg.sender for the didPay and uniswapV3SwapCallback functions with the least amount of opcodes necessary. Additionally, we can use xor() instead of iszero(eq()), saving 3 gas. We can also potentially save gas on the unhappy path by using scratch space to store the error selector, potentially avoiding memory expansion costs.

```solidity
file: /src/blast/BlastMagicLP.sol

119        if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119C1-L119C116


```solidity
file: /src/blast/BlastOnboardingBoot.sol
 
59        if (claimed[msg.sender]) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L59C1-L59C35

```solidity
file: /src/mimswap/MagicLP.sol

424        if (shareAmount > balanceOf(msg.sender)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L424C1-L424C51


## [G-27] Pre-increment and pre-decrement are cheaper than + 1 ,- 1

```solidity
file: /src/mimswap/libraries/Math.sol

23            return quotient + 1;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L23C1-L23C33


```solidity
file: /src/mimswap/periphery/Factory.sol

131        _pools[poolIndex] = _pools[_pools.length - 1];

138        _userPools[userPoolIndex] = _userPools[_userPools.length - 1];

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L131C1-L131C55


## [G-28] `do-while` is cheaper than `for-loops` when the initial check can be skipped


`for (uint256 i; i < len; ++i){ ... }` -> `do { ...; ++i } while (i < len);`

```solidity
file: /src/mimswap/periphery/Router.sol

544        for (uint256 i = 0; i < iterations; ) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544C8-L544C48


```solidity
file: /src/staking/LockingMultiRewards.sol

547        for (uint256 i; i < rewardTokens.length; ) {

561        for (uint256 i; i < rewardTokens.length; ) {

575        for (uint256 i; i < rewardTokens.length; ) {

580            for (uint256 j; j < users.length; ) {

514        for (uint256 i; i < rewardTokens.length; ) {    

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547C1-L547C53


## [G-29] address(this) should be cached

Cacheing saves gas when compared to repeating the calculation at each point it is used in the contract.The instance below represents the second+ time of calling address(this) in a specific function

```solidity
file: /src/blast/BlastOnboardingBoot.sol

106        (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

117        staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));

118        staking.setOperator(address(this), true);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106C1-L106C120


```solidity
file: /src/mimswap/periphery/Router.sol

282        lp.safeTransferFrom(msg.sender, address(this), sharesIn);

289                address(this),

298                address(this),

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282C1-L282C66
