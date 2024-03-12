## Summary

### Gas Optimization

no |Issue |Instances||
|-|:-|:-:|:-:|
| [G-01] |Private functions used once can be inlined |  |1|--| 
| [G-02] |Use bytes.concat() instead of abi.encodePacked(), since this is preferred since 0.8.4 |  |2|--| 
| [G-03] |State variables can be packed into fewer storage slots by truncating timestamp bytes |  |8|--| 
| [G-04] | Constructors can be marked `payable` |  |13|--| 
| [G-05] |`internal` functions only called once can be inlined to save gas |  |24|--| 
| [G-06] | Do not calculate constants |  |4|--| 
| [G-07] | Empty blocks should be removed or emit something |  |1|--| 
| [G-08] |with assembly, `.call (bool success)` transfer can be done gas-optimized |  |1|--| 
| [G-09] |Use assembly to check for `address(0)` |  |21|--| 
| [G-10] |abi.encode() is less efficient than  abi.encodepacked() |  |2|--| 
| [G-11] |Use assembly to write address storage values |  |12|--| 
| [G-12] |Use nested if and, avoid multiple check combinations |  |11|--| 
| [G-13] |Add unchecked{} for subtractions where the operands cannot underflow because of a previous require() or if statement |  |9|--| 
| [G-14]Using fixed bytes is cheaper than using string | |  |3|--| 
| [G-15] |Using `calldata` instead of `memory` for read-only arguments in external functions saves gas |  |2|--| 
| [G-16] |Multiple address /ID mappings can be combined into a single mapping of an address/ID to a struct , where appropriate |  |2|--| 
| [G-17] |Multiplication/division by two should use bit shifting |  |5|--| 
| [G-18] |A modifier used only once and not being inherited should be inlined to save gas |   |1|--| |
| [G-19] |>= costs less gas than > | |23|--| |
| [G-20] |Use assembly to emit events | |28|--|



## Gas Optimizations  

## [G-1] Private functions used once can be inlined
Issue Description - Private functions that are only used internally in a single caller do not provide any abstraction benefits. The function call overhead is wasted gas in this case.

Proposed Optimization - Identify private functions that are only used in a single internal caller, and inline their code directly into the caller by copy-pasting the function body. This avoids the unnecessary function call.

Estimated Gas Savings - Inlining a private function saves approximately 200-500 gas by removing the function call overhead. This adds up over many private functions.

```solidity
file:/src/blast/BlastWrappers.sol
70     function _setupBlacklist() private {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L70-L70





## [G-2] Use bytes.concat() instead of abi.encodePacked(), since this is preferred since 0.8.4
Issue Description - The abi.encodePacked() function is used to concatenate multiple arguments into a byte array prior to 0.8.4. However, since 0.8.4 the bytes.concat() function was introduced which performs the same role but is preferred since it avoids ABI encoding overhead.

Proposed Optimization - Replace uses of abi.encodePacked() with bytes.concat() where multiple arguments need to be concatenated into a byte array.

Estimated Gas Savings - Using bytes.concat() instead of abi.encodePacked() saves approximately 300-500 gas per concatenation by avoiding ABI encoding.

```solidity
File: /src/mimswap/MagicLP.sol
156       return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata   (_QUOTE_TOKEN_).symbol()));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L156
```solidity
file: /src/mimswap/periphery/Factory.sol
 163      return keccak256(abi.encodePacked(sender_, implementation, baseToken_, quoteToken_, lpFeeRate_, i_, k_));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L163

## [G-3] State variables can be packed into fewer storage slots by truncating timestamp bytes

By using a uint32 rather than a larger type for variables that track timestamps/block numbers, one can save gas by using fewer storage slots per struct, at the expense of the protocol breaking after the year 2106 (when uint32 wraps). If this is an acceptable tradeoff, if variables occupying the same slot are both written the same function or by the constructor, avoids a separate Gsset (20000 gas). Reads of the variables can also be cheaper

There are 1 instance(s) of this issue: 

```solidity
file:/src/mimswap/MagicLP.sol#L66-L78


66   uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%
72   uint112 public _BASE_RESERVE_;
73    uint112 public _QUOTE_RESERVE_;
74    uint32 public _BLOCK_TIMESTAMP_LAST_;
75    uint256 public _BASE_PRICE_CUMULATIVE_LAST_;
76    uint112 public _BASE_TARGET_;
77    uint112 public _QUOTE_TARGET_;
78    uint32 public _RState_;


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L66-L78

## [G-4] Constructors can be marked `payable`
Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn't provided.A constructor can safely be marked as payable, since only the deployer would be able to pass funds, and the project itself would not pass any funds. 

```solidity
file: /src/blast/BlastDapp.sol
 7   constructor() {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L7-L7

```solidity
file:/src/blast/BlastBox.sol
24    constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L24


```solidity
file:/src/blast/BlastGovernor.so
15    constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L15

```solidity
file:/src/blast/BlastMagicLP.sol
23    constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L23

```solidity
file:/src/blast/BlastOnboarding.sol
 58   constructor() Owned(msg.sender) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L58

```solidity
file:/src/blast/BlastTokenRegistry.sol
12    constructor(address _owner) Owned(_owner) {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L12

```solidity
file:/src/blast/BlastWrappers.sol
20    constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L20

```solidity
file:/src/mimswap/MagicLP.sol
 84   constructor(address owner_) Owned(owner_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L84

```solidity
file:/src/mimswap/auxiliary/FeeRateModel.sol
22    constructor(address maintainer_, address owner_) Owned(owner_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L22

```solidity
file:/src/mimswap/periphery/Factory.sol
38    constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L38

```solidity
file:/src/mimswap/periphery/Router.sol
38    constructor(IWETH weth_, IFactory factory_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L38

```solidity
file:/src/oracles/aggregators/MagicLpAggregator.sol
 21   constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L21

```solidity
file:/src/staking/LockingMultiRewards.sol
112    constructor(
        address _stakingToken,
        uint256 _lockingBoostMultiplerInBips,
        uint256 _rewardsDuration,
        uint256 _lockDuration,
        address _owner

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L112-L117
## [G-5]  `internal` functions only called once can be inlined to save gas
Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.

*There are 24 instance(s) of this issue:*



```solidity
file:/src/blast/BlastBox.sol
98    function _configure() internal override {


36        function _onBeforeDeposit(
        IERC20 token,
        address /*from*/,
        address /*to*/,
        uint256 /*amount*/,
        uint256 /*share*/
    ) internal view override {
        if (!enabledTokens[address(token)]) {
            revert ErrUnsupportedToken();  }   }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L36-L46

```solidity
file:/src/blast/BlastMagicLP.sol
 98   function _afterInitialized() internal override {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L98-L98

```solidity
file:/src/blast/BlastMagicLP.sol
104     function _updateTokenClaimables() internal {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L104


```solidity
file:/src/blast/BlastOnboarding.sol#L226
226    function _implementation() internal view override returns (address) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L226

```solidity
file:/src/blast/libraries/BlastPoints.sol
10    function configure() internal {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L10-L10

```solidity
file:/src/blast/libraries/BlastYields.sol
20    function enableTokenClaimable(address token) internal {
29    function configureDefaultClaimables(address governor_) internal {
38    function claimMaxGasYields(address recipient) internal returns (uint256) {
42    function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {
51    function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
55    function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {
60    function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {
70    function claimAllTokenYields(address token, address recipient) internal returns (uint256 amount) {
75    function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {
86    function callPrecompile(bytes calldata data) internal {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L20-L20


```solidity
file:/src/mimswap/libraries/DecimalMath.so
23    function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {
27    function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {
31    function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {
39    function reciprocalFloor(uint256 target) internal pure returns (uint256) {
43    function reciprocalCeil(uint256 target) internal pure returns (uint256) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L23-L23

```solidity
file:/src/mimswap/libraries/Math.sol
51    function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79    function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51-L51

```solidity
file:

```

```solidity
file:

```
## [G-6] Do not calculate constants
Due to how constant variables are implemented (replacements at compile-time), an expression assigned to a constant variable is recomputed each time that the variable is used, which wastes some gas.
```solidity
file:
    uint256 internal constant ONE = 10 ** 18;
    uint256 internal constant ONE2 = 10 ** 36;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L20-L21
```solidity
file:
63    uint256 public constant MAX_I = 10 ** 36;
64    uint256 public constant MAX_K = 10 ** 18;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L63-L64

## [G-7] Empty blocks should be removed or emit something
The code should be refactored such that they no longer exist, or the block should do something useful, such as emitting an event or reverting. If the contract is meant to be extended, the contract should be `abstract` and the function signatures be added without any default implementation. If the block is an empty `if`-statement block to avoid doing subsequent checks in the else-if/else conditions, the else-if/else conditions should be nested under the negation of the if-statement, because they involve different classes of checks, which may lead to the introduction of errors when the code is later modified (`if (x) {...} else if (y) {...} else {...}` => `if (!x) { if (y) {...} else {...} }`). Empty `receive()`/`fallback() payable` functions that are not used, can be removed to save deployment gas.

*There are 1 instance(s) of this issue:*


```solidity
file:/blast/BlastGovernor.sol
113    receive() external payable {}
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L13


## [G-8] with assembly, `.call (bool success)` transfer can be done gas-optimized
`return` data `(bool success,)` has to be stored due to EVM architecture, but in a usage like below, `out` and `outsize` values are given (0,0), this storage disappears and gas optimization is provided.

```solidity
file:/src/blast/BlastGovernor.sol
 54       (success, result) = to.call{value: value}(data);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L54


## [G-9]Use assembly to check for `address(0)`
*There are 21 instance(s) of this issue:*
```solidity
file:/src/blast/BlastBox.sol
25       if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
        }
28     if (address(registry_) == address(0)) {
            revert ErrZeroAddress();

73        if (feeTo_ == address(0)) {            
```https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L25-L25
```solidity
file:/src/blast/BlastGovernor.so
16        if (feeTo_ == address(0)) {
41        if(_feeTo == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L16

```solidity
file:/src/blast/BlastOnboardingBoot.sol
97        if (pool != address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L97
```solidity
file:/src/blast/BlastTokenRegistry.sol
14        if (token == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L15

```solidity
file:/src/blast/BlastWrappers.sol
21        if (governor_ == address(0)) {
35        if (governor_ == address(0)) {
48        if (governor_ == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L21
```solidity
file:/src/mimswap/MagicLP.sol
102        if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
393            _mint(address(0), 1001);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L102
```solidity
file:/src/mimswap/auxiliary/FeeRateModel.sol
23       if (maintainer_ == address(0)) {
35       if (implementation == address(0)) {
47        if (maintainer_ == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L23
```solidity
file:/src/mimswap/periphery/Factory.sol
39        if (implementation_ == address(0)) {
42        if (address(maintainerFeeRateModel_) == address(0)) {
97        if (implementation_ == address(0)) {
106        if (address(maintainerFeeRateModel_) == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L39

```solidity
file:
 39       if (address(weth_) == address(0) || address(factory_) == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L39
```solidity
file:/src/staking/LockingMultiRewards.sol
301        if (rewardToken == address(0)) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L301


## [G-10] abi.encode() is less efficient than  abi.encodepacked()

In terms of efficiency, abi.encodePacked() is generally considered to be more gas-efficient than abi.encode(), because it skips the step of adding function signatures and other metadata to the encoded data. However, this comes at the cost of reduced safety, as abi.encodePacked() does not perform any type checking or padding of data.

```solidity
file:/src/mimswap/MagicLP.sol
        return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L156

```solidity
file:/src/mimswap/periphery/Factory.sol
163     return keccak256(abi.encodePacked(sender_, implementation, baseToken_, quoteToken_, lpFeeRate_, i_, k_));

  ```
  https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L163

## [G-11] Use assembly to write address storage values

By using assembly to write to address storage values, you can bypass some of these operations and lower the gas cost of writing to storage. Assembly code allows you to directly access the Ethereum Virtual Machine (EVM) and perform low-level operations that are not possible in Solidity.

```solidity
  file:/src/blast/BlastBox.sol
  15    constructor(address feeTo_, address _owner) OperatableV2(_owner) {
        if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
        }


        feeTo = feeTo_;
        BlastYields.configureDefaultClaimables(address(this));
    }

 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L15-L22
  ```solidity
  file:/src/blast/BlastMagicLP.sol
  32      feeTo = feeTo_;
  ```
  https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L32

  ```solidity
  file:/src/blast/BlastOnboarding.sol
  94        feeTo = feeTo_;
  191     bootstrapper = bootstrapper_;

  ```
  https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L94
  ```solidity
  file:/src/mimswap/MagicLP.sol
  119        _BASE_TOKEN_ = baseTokenAddress;
  120      _QUOTE_TOKEN_ = quoteTokenAddress;
  ```
  https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L119-L120
  ```solidity
  file:/src/mimswap/auxiliary/FeeRateModel.so
  27      maintainer = maintainer_;
  58        implementation = implementation_;
  ```
  https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L27

  ```solidity
         
  file:/src/mimswap/periphery/Factory.sol
  45      implementation = implementation_;
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L45

 ```solidity
 file:/src/staking/LockingMultiRewards.sol
 135       stakingToken = _stakingToken;
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L135

 ## [G-12] Use nested if and, avoid multiple check combinations

Using nested if is cheaper than using && multiple check combinations. There are more advantages, such as easier to read code and better coverage reports.
 ```solidity
 file:/src/blast/BlastMagicLP.sol
 119    if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L119
 ```solidity
 file:/src/blast/BlastOnboarding.sol
 114       if (caps[token] > 0 && totals[token].total > caps[token]) {
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L114

 ```solidity
 file:/src/mimswap/MagicLP.sol
  139     if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
  144        if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
  302       if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
  549        if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L139
 ```solidity
 file:/src/mimswap/periphery/Router.sol
  147      } else if (baseReserve > 0 && quoteReserve > 0) {
  527            if (quoteReserve > 0 && baseReserve > 0) {
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L147

 ```solidity
 file:/src/staking/LockingMultiRewards.sol
   326       if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {
   417            if (index == lastLockIndex[user] && locks.length > 1) {
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L326
 ## [G-13]Add unchecked{} for subtractions where the operands cannot underflow because of a previous require() or if statement  
Solidity version 0.8+ comes with implicit overflow and underflow checks on unsigned integers. When an overflow or an underflow isn't possible (as an example, when a comparison is made before the arithmetic operation), some gas can be saved by using an unchecked block.
 ```solidity
 file:/src/staking/LockingMultiRewards.sol
  162        _balances[msg.sender].unlocked -= amount;    unlockedSupply -= amount;
  172        _balances[msg.sender].unlocked -= amount;   unlockedSupply -= amount;
  282        uint256 timeElapsed = lastTimeRewardApplicable_ - _rewardData[rewardToken].lastUpdateTime;
  283        uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
  293        uint256 pendingUserRewardsPerToken = rewardPerToken_ - userRewardPerTokenPaid[user][rewardToken];

  373        uint256 _remainingRewardTime = _nextEpoch - block.timestamp;
  427            uint256 lastIndex = locks.length - 1;

 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L162-L163
 ```solidity
 file:/src/oracles/aggregators/MagicLpAggregator.sol
  38      uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
  39      uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L38-L39
 
 ## [G-14] Using fixed bytes is cheaper than using string
As a rule of thumb, use bytes for arbitrary-length raw byte data and string for arbitrary-length string (UTF-8) data.
If you can limit the length to a certain number of bytes, always use one of bytes1 to bytes32 because they are much cheaper.
 ```solidity
 file:/src/blast/BlastMagicLP.sol
 39    function version() external pure override returns (string memory) {
 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L39
 ```
 ```solidity
 file:/src/mimswap/MagicLP.sol
 159   function symbol() public pure override returns (string memory) {
 239    function version() external pure virtual returns (string memory) {
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L159

 ## [G-15] Using `calldata` instead of `memory` for read-only arguments in external functions saves gas
 ```solidity
 file:/src/blast/BlastMagicLP.sol
 39    function version() external pure override returns (string memory) {
 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L39
 ```
 ```solidity
 file:/src/mimswap/MagicLP.sol
 
 236    function version() external pure virtual returns (string memory) {
 ```
  https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L236   


## [G-16]Multiple address /ID mappings can be combined into a single mapping of an address/ID to a struct , where appropriate


Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (20000 gas) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save ~42 gas per access due to not having to re
 the key’s keccak256 hash (Gkeccak256 - 30 gas) and that calculation’s associated stack operations.

 ```solidity
 file:/src/staking/LockingMultiRewards.so
 94   mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
 95  mapping(address user => mapping(address token => uint256 amount)) public rewards;
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L94-L95

## [G-17]Multiplication/division by two should use bit shifting
 <x> * 2 is the same as <x> << 1. While the compiler uses the SHL opcode to accomplish both, the version that uses multiplication incurs an overhead of 20 gas due to JUMPs to and from a compiler utility function that introduces checks which can be avoided by using unchecked {} around the division by two.
 `solidity
 file:/src/mimswap/libraries/Math.sol
  30       uint256 z = x / 2 + 1;
  31      y = x;
  32      while (z < y) {
  33          y = z;
  34          z = (x / z + z) / 2;
        }

  168        uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
``
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L30-L35

## [G-18] A modifier used only once and not being inherited should be inlined to save gas
 ```solidity
 file:/src/mimswap/MagicLP.sol
 614    modifier onlyClones() {
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L614-L614

## [G-19] >= costs less gas than >
 
The compiler uses opcodes GT and ISZERO for solidity code that uses >, but only requires LT for >=, which saves 3 gas 
Reference:  https://gist.github.com/IllIllI000/3dc79d25acccfa16dee4e83ffdc6ffde

 ```solidity
 file:/src/blast/BlastOnboarding.sol
  114       if (caps[token] > 0 && totals[token].total > caps[token]) {
 ```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L114

 ```solidity
 file:/src/mimswap/MagicLP.sol
 111                   if (k > MAX_K) {
 114        if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {
 294        if (data.length > 0) {
 315            if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {
 337            if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {
 395        } else if (baseReserve > 0 && quoteReserve > 0) {
 424        if (shareAmount > balanceOf(msg.sender)) {
 450        if (data.length > 0) {
 483        if (newI == 0 || newI > MAX_I) {
 486        if (newK > MAX_K) {
 489        if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {
 508        if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
 532        if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
 549        if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
 ```
 https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L111

```solidity
   file:/src/mimswap/libraries/Math.sol
  22        if (remainder > 0) {
  174        if (bAbs >= part2) {
  200        if (V2 > V1) {

   ```
   https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L22
   ```solidity
   file:/src/mimswap/libraries/PMMPricing.sol
   89                if (receiveBaseAmount > backToOneReceiveBase) {
   
   ```
   https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L89
   ```solidity
   file:/src/mimswap/periphery/Router.sol
    220       if (msg.value > wethAdjustedAmount) {
    590        if (pathLength > 256) {
    602        if (quoteDecimals - baseDecimals > MAX_BASE_QUOTE_DECIMALS_DIFFERENCE) {
    
   ```
   https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L220
   ```solidity
   file:/src/staking/LockingMultiRewards.sol
  326         if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

  417            if (index == lastLockIndex[user] && locks.length > 1) {

   ```
   https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L326


## [G-20] Use assembly to emit events

We can use assembly to emit events efficiently by utilizing scratch space and the free memory pointer. This will allow us to potentially avoid memory expansion costs. Note: In order to do this optimization safely, we will need to cache and restore the free memory pointer.


   ```solidity
   file:/src/blast/BlastBox.sol#
   78        emit LogFeeToChanged(feeTo_);
   90        emit LogTokenDepositEnabled(token, enabled);
   ```
   https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L78

           
   ```solidity
   file:/src/blast/BlastGovernor.sol
    46   emit LogFeeToChanged(_feeTo);
   ```
   https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L46
   ```solidity
   file:/src/blast/BlastMagicLP.sol
   86        emit LogFeeToChanged(feeTo_);
   91        emit LogOperatorChanged(operator, status);

   ```
   https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L86
   ```solidity
   file:/src/blast/BlastOnboarding.sol
   120       emit LogDeposit(msg.sender, token, amount, lock_);
   129        emit LogLock(msg.sender, token, amount);
   140        emit LogWithdraw(msg.sender, token, amount);
   153        emit LogFeeToChanged(feeTo_);
   182        emit LogTokenSupported(token, supported);
   187        emit LogTokenCapChanged(token, cap);
   192        emit LogBootstrapperChanged(bootstrapper_);
   197        emit LogStateChange(State.Opened);
   201        emit LogStateChange(State.Closed);
   211        emit LogTokenRescue(token, to, amount);

   ```
   https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L120
   ```solidity
   file:/src/blast/BlastOnboardingBoot.sol
   71    emit LogClaimed(msg.sender, shares, lock);
   124        emit LogLiquidityBootstrapped(pool, 1address(staking), totalPoolShares);
   132        emit LogInitialized(_router);
   143        emit LogStakingChanged(address(_staking));
   148        emit LogReadyChanged(ready);

   ```
   https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L71
   ```solidity
   file:/src/blast/BlastTokenRegistry.sol
    20       emit LogNativeYieldTokenEnabled(token, enabled);


   ```
   https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L20

   ```solidity
   file:/src/blast/libraries/BlastYields.sol
   26        emit LogBlastTokenClaimableEnabled(address(this), token);
   31        emit LogBlastNativeClaimableEnabled(address(this));
   44        emit LogBlastGasClaimed(recipient, amount);
   57        emit LogBlastETHClaimed(recipient, amount);
   62        emit LogBlastETHClaimed(recipient, amount);
   72        emit LogBlastTokenClaimed(recipient, address(token), amount);
   77        emit LogBlastTokenClaimed(recipient, address(token), amount);
   ```
   https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L26
  