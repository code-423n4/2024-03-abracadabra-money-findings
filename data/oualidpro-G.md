## Summary
## Gas Optimizations


| |Issue|Instances|Gas Saved|
|-|:-|:-:|-:|
| [GAS-1](#GAS-1-1705424649) | Consider using OZ EnumerateSet in place of nested mappings | 4 | 4000 |
| [GAS-2](#GAS-2-1706546944) | Optimize Deployment Size by Fine-tuning IPFS Hash | 24 | 254400 |
| [GAS-3](#GAS-3-1706545887) | Trade-offs Between Modifiers and Internal Functions | 67 | 2077 |
| [GAS-4](#GAS-4-1705426850) | Avoid emitting event on every iteration | 2 | 750 |
| [GAS-5](#GAS-5-1693311630) | Use assembly to check for `address(0)` | 29 | 174 |
| [GAS-6](#GAS-6-1693311540) | Multiple accesses of a mapping/array should use a local variable cache | 29 | 1218 |
| [GAS-7](#GAS-7-1706548063) | Use assembly scratch space to build calldata for external calls | 37 | 8140 |
| [GAS-8](#GAS-8-1693311599) | Use assembly to calculate hashes to save gas | 1 | 80 |
| [GAS-9](#GAS-9-1693311695) | Optimize Address Storage Value Management with `assembly` | 15 | - |
| [GAS-10](#GAS-10-1693311732) | Use assembly to emit events | 59 | 2242 |
| [GAS-11](#GAS-11-1693311856) | Using bools for storage incurs overhead | 8 | 800 |
| [GAS-12](#GAS-12-1693311904) | Cache array length outside of loop | 7 | 679 |
| [GAS-13](#GAS-13-1693311936) | State variables should be cached in stack variables rather than re-reading them from storage | 11 | 1067 |
| [GAS-14](#GAS-14-1699447317) | Avoid caching global special variables | 1 | 12 |
| [GAS-15](#GAS-15-1693311965) | With assembly, `.call (bool success)` transfer can be done gas-optimized | 1 | - |
| [GAS-16](#GAS-16-1693311951) | Use calldata instead of memory for function arguments that do not get mutated | 1 | - |
| [GAS-17](#GAS-17-1693312015) | Add `unchecked {}` for subtractions where the operands cannot underflow because of a previous `require()` or `if`-statement | 5 | 425 |
| [GAS-18](#GAS-18-1693312028) | `x += y` costs more gas than `x = x + y` for state variables | 9 | 1017 |
| [GAS-19](#GAS-19-1696084432) | Simple checks for zero `uint` can be done using assembly to save gas | 37 | 222 |
| [GAS-20](#GAS-20-1708173673) | Combine `mapping`s referenced in the same function by the same key | 2 | 84 |
| [GAS-21](#GAS-21-1706544439) | Counting down in for statements is more gas efficient | 1 | - |
| [GAS-22](#GAS-22-1693312114) | Divisions which do not divide by -X cannot overflow or overflow so such operations can be unchecked to save gas | 40 | - |
| [GAS-23](#GAS-23-1693312130) | Do not calculate constants | 4 | 1600 |
| [GAS-24](#GAS-24-1694877823) | Use `do while` loops instead of `for` loops | 8 | 968 |
| [GAS-25](#GAS-25-1693312160) | Stack variable cost less while used in emiting event | 16 | 1600 |
| [GAS-26](#GAS-26-1693312222) | Events should be emitted outside of loops | 4 | 1500 |
| [GAS-27](#GAS-27-1693312354) | The result of function calls should be cached rather than re-calling the function | 2 | - |
| [GAS-28](#GAS-28-1693312400) | Don't initialize `uint` variables with default value | 2 | - |
| [GAS-29](#GAS-29-1693312433) | `internal` functions only called once can be inlined to save gas | 5 | 100 |
| [GAS-30](#GAS-30-1709377588) | Avoid emitting event on every iteration | 2 | 750 |
| [GAS-31](#GAS-31-1702129464) | Refactor modifiers to call a local function | 6 | 6000 |
| [GAS-32](#GAS-32-1693312642) | Multiple `address`/ID mappings can be combined into a single `mapping` of an `address`/ID to a `struct`, where appropriate | 13 | - |
| [GAS-33](#GAS-33-1693312655) | Optimize names to save gas | 12 | 264 |
| [GAS-34](#GAS-34-1693312684) | Not using the named return variables anywhere in the function wast gas | 19 | 57 |
| [GAS-35](#GAS-35-1693312698) | Enable Solidity's optimizer | 1 | - |
| [GAS-36](#GAS-36-1694875070) | State variables can be packed into fewer storage slots | 2 | 4000 |
| [GAS-37](#GAS-37-1694793490) | Structs can be packed into fewer storage slots by truncating timestamp bytes | 1 | - |
| [GAS-38](#GAS-38-1693312741) | Constructors can be marked `payable` | 16 | 336 |
| [GAS-39](#GAS-39-1699444393) | Initializer can be marked `payable` | 1 | 21 |
| [GAS-40](#GAS-40-1693316170) | `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too) | 1 | - |
| [GAS-41](#GAS-41-1696084477) | `++i`/`i++` should be `unchecked{++i}`/`unchecked{i++}` when it is not possible for them to overflow, as is the case when used in `for`- and `while`-loops | 1 | - |
| [GAS-42](#GAS-42-1709377106) | Consider pre-calculating the address of `address(this)` to save gas | 49 | - |
| [GAS-43](#GAS-43-1693312824) | Using `private` rather than `public` for constants, saves gas | 8 | - |
| [GAS-44](#GAS-44-1709385583) | Reduce deployment costs by tweaking contracts' metadata | 24 | - |
| [GAS-45](#GAS-45-1693312940) | Redundant else statement | 4 | - |
| [GAS-46](#GAS-46-1693312958) | Functions guaranteed to revert when called by normal users can be marked `payable` | 66 | 1386 |
| [GAS-47](#GAS-47-1693312972) | Avoid updating storage when the value hasn't changed to save gas | 12 | 9600 |
| [GAS-48](#GAS-48-1693312984) | Use shift Right instead of division if possible to save gas | 3 | 60 |
| [GAS-49](#GAS-49-1693312999) | Use shift Left instead of multiplication if possible to save gas | 6 | - |
| [GAS-50](#GAS-50-1693313015) | Usage of `uints`/`ints` smaller than 32 bytes (256 bits) incurs overhead | 8 | - |
| [GAS-51](#GAS-51-1693313026) | The use of a logical AND in place of double if is slightly less gas efficient in instances where there isn't a corresponding else statement for the given if statement | 11 | 165 |
| [GAS-52](#GAS-52-1709389408) | Split `revert` checks to save gas | 12 | 24 |
| [GAS-53](#GAS-53-1693313099) | Cache state variables outside of loop to avoid reading storage on every iteration | 3 | - |
| [GAS-54](#GAS-54-1693311457) | State variable read in a loop | 4 | - |
| [GAS-55](#GAS-55-1693313054) | State variables only set in the constructor should be declared `immutable` | 1 | 2097 |
| [GAS-56](#GAS-56-1693313071) | Stack variable used as a cheaper cache for a state variable is only used once | 35 | 105 |
| [GAS-57](#GAS-57-1708099671) | State variable written in a loop | 2 | 5800 |
| [GAS-58](#GAS-58-1693313130) | `>=`/`<=` costs less gas than `>`/`<` | 74 | 222 |
| [GAS-59](#GAS-59-1695857615) | Avoid transferring amounts of zero in order to save gas | 12 | - |
| [GAS-60](#GAS-60-1694790859) | Unnecessary casting as variable is already of the same type | 23 | 506 |
| [GAS-61](#GAS-61-1693313275) | Use assembly to validate `msg.sender` | 2 | 24 |
| [GAS-62](#GAS-62-1709392376) | Use the inputs/results of assignments rather than re-reading state variables | 9 | 873 |
| [GAS-63](#GAS-63-1699451597) | Using `constant`s instead of `enum` can save gas | 2 | - |
| [GAS-64](#GAS-64-1705427608) | Consider using solady's 'FixedPointMathLib' | 96 | - |
| [GAS-65](#GAS-65-1694794906) | Using mappings instead of arrays to avoid length checks save gas | 4 | - |
| [GAS-66](#GAS-66-1699443465) | Using `private` for constants saves gas | 23 | - |
| [GAS-67](#GAS-67-1702131709) | Use `solady` library where possible to save gas | 9 | - |
| [GAS-68](#GAS-68-1707922603) | Use Array.unsafeAccess() to avoid repeated array length checks | 28 | 58800 |
| [GAS-69](#GAS-69-1693313317) | Can make the variable outside the loop to save gas | 16 | - |
| [GAS-70](#GAS-70-1693313355) | Consider activating via-ir for deploying | 1 | 250 |

Total: 1053 instances over 70 issues with ** 374495 gas ** saved



### <a name="GAS-1-1705424649"></a>[GAS-1] Consider using OZ EnumerateSet in place of nested mappings
Nested data in Solidity uses expensive double hashing for storage. to avoid this you can use a cheaper option (combining keys for one hash), but risks collisions with other similar structures. Solidity prioritizes safety, leading to less efficient storage. OpenZeppelin's EnumerableSet offers a solution, it combines set features with internal collision protection, making it potentially more gas-efficient for specific cases.

*Instances (4)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

41:     mapping(address user => mapping(address token => Balances)) public balances;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L41-L41)

```solidity
File: /src/mimswap/periphery/Factory.sol

35:     mapping(address base => mapping(address quote => address[] pools)) public pools;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L35-L35)

```solidity
File: /src/staking/LockingMultiRewards.sol

94:     mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;

95:     mapping(address user => mapping(address token => uint256 amount)) public rewards;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L95-L95)

</details>

### <a name="GAS-2-1706546944"></a>[GAS-2] Optimize Deployment Size by Fine-tuning IPFS Hash
Optimizing the deployment size of a smart contract is vital to minimize gas costs, and one way to achieve this is by fine-tuning the IPFS hash appended by the Solidity compiler as metadata. This metadata, consisting of 53 bytes, increases the gas required for contract deployment by approximately 10,600 gas due to bytecode costs, and additionally, up to 848 gas due to calldata costs, depending on the proportion of zero and non-zero bytes. Utilize the --no-cbor-metadata compiler flag to prevent the compiler from appending metadata. However, this approach has a drawback as it can complicate the contract verification process on block explorers like Etherscan, potentially reducing transparency.

*Instances (24)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L13)

```solidity
File: /src/blast/BlastDapp.sol

6: contract BlastDapp {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastDapp.sol#L6)

```solidity
File: /src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastGovernor.sol#L7)

```solidity
File: /src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L10)

```solidity
File: /src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L64)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L34)

```solidity
File: /src/blast/BlastTokenRegistry.sol

6: contract BlastTokenRegistry is Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastTokenRegistry.sol#L6)

```solidity
File: /src/blast/BlastWrappers.sol

19: contract BlastMIMSwapRouter is Router {

28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastWrappers.sol#L42)

```solidity
File: /src/blast/libraries/BlastPoints.sol

6: library BlastPoints {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastPoints.sol#L6)

```solidity
File: /src/blast/libraries/BlastYields.sol

7: library BlastYields {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastYields.sol#L7)

```solidity
File: /src/mimswap/MagicLP.sol

25: contract MagicLP is ERC20, ReentrancyGuard, Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L25)

```solidity
File: /src/mimswap/auxiliary/FeeRateModel.sol

13: contract FeeRateModel is Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModel.sol#L13)

```solidity
File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

7: contract FeeRateModelImpl {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModelImpl.sol#L7)

```solidity
File: /src/mimswap/libraries/DecimalMath.sol

17: library DecimalMath {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/DecimalMath.sol#L17)

```solidity
File: /src/mimswap/libraries/Math.sol

16: library Math {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L16)

```solidity
File: /src/mimswap/libraries/PMMPricing.sol

20: library PMMPricing {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/PMMPricing.sol#L20)

```solidity
File: /src/mimswap/periphery/Factory.sol

11: contract Factory is Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L11)

```solidity
File: /src/mimswap/periphery/Router.sol

12: contract Router {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L12)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

9: contract MagicLpAggregator is IAggregator {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L9)

```solidity
File: /src/staking/LockingMultiRewards.sol

14: contract LockingMultiRewards is OperatableV2, Pausable {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L14)

</details>

### <a name="GAS-3-1706545887"></a>[GAS-3] Trade-offs Between Modifiers and Internal Functions
In Solidity, both modifiers and internal functions can be used to modularize and reuse code, but they have different trade-offs.

Modifiers are primarily used to augment the behavior of functions, often for checks or validations.They can access parameters of the function they modify and are integrated into the functionâ€™s code at compile time.This makes them syntactically cleaner for repetitive precondition checks.However, modifiers can sometimes lead to less readable code, especially when the logic is complex or when multiple modifiers are used on a single function.

Internal functions, on the other hand, offer more flexibility.They can contain complex logic, return values, and be called from other functions.This makes them more suitable for reusable chunks of business logic.Since internal functions are separate entities, they can be more readable and easier to test in isolation compared to modifiers.

Using internal functions can result in slightly more gas consumption, as it involves an internal function call.However, this cost is usually minimal and can be a worthwhile trade- off for increased code clarity and maintainability.

In summary, while modifiers offer a concise way to include checks and simple logic across multiple functions, internal functions provide more flexibility and are better suited for complex and reusable code.The choice between the two should be based on the specific use case, considering factors like code complexity, readability, and gas efficiency.

*Instances (67)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

36:     function _onBeforeDeposit(

98:     function _configure() internal override {

103:     function isOwner(address _account) internal view override returns (bool) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L103)

```solidity
File: /src/blast/BlastMagicLP.sol

98:     function _afterInitialized() internal override {

104:     function _updateTokenClaimables() internal {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L104)

```solidity
File: /src/blast/BlastOnboarding.sol

226:     function _implementation() internal view override returns (address) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L226)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

155:     function _claimable(address user) internal view returns (uint256 shares) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L155)

```solidity
File: /src/blast/libraries/BlastPoints.sol

10:     function configure() internal {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastPoints.sol#L10)

```solidity
File: /src/blast/libraries/BlastYields.sol

20:     function enableTokenClaimable(address token) internal {

29:     function configureDefaultClaimables(address governor_) internal {

38:     function claimMaxGasYields(address recipient) internal returns (uint256) {

42:     function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {

51:     function claimAllNativeYields(address recipient) internal returns (uint256 amount) {

55:     function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {

60:     function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {

70:     function claimAllTokenYields(address token, address recipient) internal returns (uint256 amount) {

75:     function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {

86:     function callPrecompile(bytes calldata data) internal {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastYields.sol#L86)

```solidity
File: /src/mimswap/MagicLP.sol

528:     function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {

545:     function _twapUpdate() internal {

560:     function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {

567:     function _sync() internal {

581:     function _transferBaseOut(address to, uint256 amount) internal {

587:     function _transferQuoteOut(address to, uint256 amount) internal {

593:     function _mint(address to, uint256 amount) internal override {

601:     function _afterInitialized() internal virtual {}

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L601)

```solidity
File: /src/mimswap/libraries/DecimalMath.sol

23:     function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {

27:     function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {

31:     function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {

35:     function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {

39:     function reciprocalFloor(uint256 target) internal pure returns (uint256) {

43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {

47:     function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/DecimalMath.sol#L47)

```solidity
File: /src/mimswap/libraries/Math.sol

19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

29:     function sqrt(uint256 x) internal pure returns (uint256 y) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L131)

```solidity
File: /src/mimswap/libraries/PMMPricing.sol

39:     function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {

76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {

104:     function _ROneSellBaseToken(

119:     function _ROneSellQuoteToken(

134:     function _RBelowSellQuoteToken(

147:     function _RBelowSellBaseToken(

162:     function _RAboveSellBaseToken(

175:     function _RAboveSellQuoteToken(

190:     function adjustedTarget(PMMState memory state) internal pure {

203:     function getMidPrice(PMMState memory state) internal pure returns (uint256) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/PMMPricing.sol#L203)

```solidity
File: /src/mimswap/periphery/Factory.sol

148:     function _addPool(address creator, address baseToken, address quoteToken, address pool) internal {

155:     function _computeSalt(

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L155)

```solidity
File: /src/mimswap/periphery/Router.sol

499:     function _addLiquidity(address lp, address to, uint256 minimumShares) internal returns (uint256 shares) {

509:     function _adjustAddLiquidity(

541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

586:     function _validatePath(address[] calldata path) internal pure {

598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L598)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

33:     function _getReserves() internal view virtual returns (uint256, uint256) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L33)

```solidity
File: /src/staking/LockingMultiRewards.sol

292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

458:     function _stakeFor(address account, uint256 amount, bool lock_) internal {

479:     function _createLock(address user, uint256 amount) internal {

528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

544:     function _updateRewards() internal {

557:     function _updateRewardsForUser(address user) internal {

572:     function _updateRewardsForUsers(address[] memory users) internal {

597:     function _getRewards(address user) internal {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L597)

</details>

### <a name="GAS-4-1705426850"></a>[GAS-4] Avoid emitting event on every iteration
Emitting events within a loop can cause significant gas consumption due to repeated I/O operations. Instead, accumulate changes in memory and emit a single event post-loop with aggregated data. This approach improves contract efficiency, reduces gas costs, and simplifies event tracking for event listeners.

*Instances (2)*:
<details><summary> see instances </summary>

```solidity
File: /src/staking/LockingMultiRewards.sol

405:         for (uint256 i; i < users.length; ) {
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

614:         for (uint256 i; i < rewardTokens.length; ) {
                 address rewardToken = rewardTokens[i];
                 uint256 rewardAmount = rewards[user][rewardToken];
     
                 // in all scenario, reset the reward amount immediately
                 rewards[user][rewardToken] = 0;
     
                 // don't assume the rewardTokens array is always the same length as the items array
                 // as new reward tokens can be added by the owner
                 if (i < rewardItemLength) {
                     RewardLockItem storage item = _rewardLock.items[i];
     
                     // expired lock, claim existing unlocked rewards if any
                     if (expired) {
                         uint256 amount = item.amount;
     
                         // since this current lock is expired and that item index
                         // matches the reward index, override the current amount
                         // with the new locked amount.
                         item.amount = rewardAmount;
     
                         // use cached amount
                         if (amount > 0) {
                             rewardToken.safeTransfer(user, amount);
                             emit LogRewardPaid(user, rewardToken, amount);
                         }
                     } else {
                         // not expired, just add to the existing lock
                         item.amount += rewardAmount;
                     }
                 }
                 // new reward token, create a new lock item
                 // could mean it's adding to an existing lock or creating a new one
                 else {
                     _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
                 }
     
                 emit LogRewardLocked(user, rewardToken, rewardAmount);
     
                 unchecked {
                     ++i;
                 }
             }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L614-L656)

</details>

### <a name="GAS-5-1693311630"></a>[GAS-5] Use assembly to check for `address(0)`
*Saves 6 gas per instance*

*Instances (29)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

25:         if (feeTo_ == address(0)) {

28:         if (address(registry_) == address(0)) {

73:         if (feeTo_ == address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L73)

```solidity
File: /src/blast/BlastGovernor.sol

16:         if (feeTo_ == address(0)) {

41:         if(_feeTo == address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastGovernor.sol#L41)

```solidity
File: /src/blast/BlastMagicLP.sol

24:         if (feeTo_ == address(0)) {

27:         if (address(registry_) == address(0)) {

81:         if (feeTo_ == address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L81)

```solidity
File: /src/blast/BlastOnboarding.sol

85:         if (address(registry_) == address(0)) {

89:         if (feeTo_ == address(0)) {

148:         if (feeTo_ == address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L148)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

97:         if (pool != address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L97)

```solidity
File: /src/blast/BlastTokenRegistry.sol

15:         if (token == address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastTokenRegistry.sol#L15)

```solidity
File: /src/blast/BlastWrappers.sol

21:         if (governor_ == address(0)) {

35:         if (governor_ == address(0)) {

48:         if (governor_ == address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastWrappers.sol#L48)

```solidity
File: /src/mimswap/MagicLP.sol

102:         if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {

102:         if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {

102:         if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L102)

```solidity
File: /src/mimswap/auxiliary/FeeRateModel.sol

23:         if (maintainer_ == address(0)) {

35:         if (implementation == address(0)) {

47:         if (maintainer_ == address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModel.sol#L47)

```solidity
File: /src/mimswap/periphery/Factory.sol

39:         if (implementation_ == address(0)) {

42:         if (address(maintainerFeeRateModel_) == address(0)) {

97:         if (implementation_ == address(0)) {

106:         if (address(maintainerFeeRateModel_) == address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L106)

```solidity
File: /src/mimswap/periphery/Router.sol

39:         if (address(weth_) == address(0) || address(factory_) == address(0)) {

39:         if (address(weth_) == address(0) || address(factory_) == address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L39)

```solidity
File: /src/staking/LockingMultiRewards.sol

301:         if (rewardToken == address(0)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L301)

</details>

### <a name="GAS-6-1693311540"></a>[GAS-6] Multiple accesses of a mapping/array should use a local variable cache
The instances below point to the second+ access of a value inside a mapping/array, within a function. Caching a mapping's value in a local `storage` or `calldata` variable when the value is accessed [multiple times](https://gist.github.com/IllIllI000/ec23a57daa30a8f8ca8b9681c8ccefb0), saves **~42 gas per access** due to not having to recalculate the key's keccak256 hash (Gkeccak256 - **30 gas**) and that calculation's associated stack operations. Caching an array's struct avoids recalculating the array offsets into memory/calldata

*Instances (29)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

105:             totals[token].locked += amount;

108:             totals[token].unlocked += amount;

114:         if (caps[token] > 0 && totals[token].total > caps[token]) {

114:         if (caps[token] > 0 && totals[token].total > caps[token]) {

127:         totals[token].locked += amount;

136:         totals[token].total -= amount;

166:             if (!supportedTokens[tokens[i]]) {

170:                 BlastYields.claimAllTokenYields(tokens[i], feeTo);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L170-L170)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

162:         uint256 userLocked = balances[user][MIM].locked + balances[user][USDB].locked;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L162-L162)

```solidity
File: /src/mimswap/periphery/Factory.sol

131:         _pools[poolIndex] = _pools[_pools.length - 1];

138:         _userPools[userPoolIndex] = _userPools[_userPools.length - 1];

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L138-L138)

```solidity
File: /src/mimswap/periphery/Router.sol

547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));

561:             amountOut = IMagicLP(path[iterations]).sellBase(to);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L561-L561)

```solidity
File: /src/staking/LockingMultiRewards.sol

279:             return _rewardData[rewardToken].rewardPerTokenStored;

283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

285:         return _rewardData[rewardToken].rewardPerTokenStored + pendingRewardsPerToken;

314:         _rewardData[rewardToken].exists = true;

362:         if (!_rewardData[rewardToken].exists) {

417:             if (index == lastLockIndex[user] && locks.length > 1) {

422:             if (locks[index].unlockTime > block.timestamp) {

431:                 lastLockIndex[user] = index;

435:                 locks[index] = locks[lastIndex];

490:         if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {

501:             _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));

502:             lastLockIndex[user] = lockCount;

510:             _userLocks[user][_lastLockIndex].amount += amount;

533:         _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow

619:             rewards[user][rewardToken] = 0;

648:                 _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L648-L648)

</details>

### <a name="GAS-7-1706548063"></a>[GAS-7] Use assembly scratch space to build calldata for external calls
Using Solidity's assembly scratch space for constructing calldata in external calls with one or two arguments can be a gas-efficient approach. This method leverages the designated memory area (the first 64 bytes of memory) for temporary data storage during assembly operations. By directly writing arguments into this scratch space, it eliminates the need for additional memory allocation typically required for calldata preparation. This technique can lead to notable gas savings, especially in high-frequency or gas-sensitive operations. However, it requires careful implementation to avoid data corruption and should be used with a thorough understanding of low-level EVM operations and memory handling. Proper testing and validation are crucial when employing such optimizations.

*Instances (37)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

57:         if (!registry.nativeYieldTokens(token_)) {

86:         if (registry.nativeYieldTokens(token)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L86-L86)

```solidity
File: /src/blast/BlastMagicLP.sol

56:         if (registry.nativeYieldTokens(_BASE_TOKEN_)) {

59:         if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {

105:         if (registry.nativeYieldTokens(_BASE_TOKEN_)) {

109:         if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {

119:         if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L119-L119)

```solidity
File: /src/blast/BlastOnboarding.sol

169:             if (registry.nativeYieldTokens(tokens[i])) {

178:         if (registry.nativeYieldTokens(token)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L178-L178)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

118:         staking.setOperator(address(this), true);

119:         staking.transferOwnership(owner);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L119-L119)

```solidity
File: /src/blast/BlastWrappers.sol

66:         super.init(data);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastWrappers.sol#L66-L66)

```solidity
File: /src/blast/libraries/BlastPoints.sol

11:         BLAST_POINTS.configurePointsOperator(BLAST_POINTS_OPERATOR);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastPoints.sol#L11-L11)

```solidity
File: /src/blast/libraries/BlastYields.sol

21:         if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {

25:         IERC20Rebasing(token).configure(YieldMode.CLAIMABLE);

43:         amount = BLAST_YIELD_PRECOMPILE.claimMaxGas(contractAddress, recipient);

56:         amount = BLAST_YIELD_PRECOMPILE.claimAllYield(contractAddress, recipient);

71:         amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));

71:         amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));

76:         amount = IERC20Rebasing(token).claim(recipient, amount);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastYields.sol#L76-L76)

```solidity
File: /src/mimswap/MagicLP.sol

174:         (uint256 lpFeeRate, uint256 mtFeeRate) = _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_);

187:         (uint256 lpFeeRate, uint256 mtFeeRate) = _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_);

225:         return _MT_FEE_RATE_MODEL_.getFeeRate(user, _LP_FEE_RATE_);

598:         super._mint(to, amount);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L598-L598)

```solidity
File: /src/mimswap/periphery/Router.sol

70:         (shares, , ) = IMagicLP(clone).buyShares(to);

93:         (shares, , ) = IMagicLP(clone).buyShares(to);

308:         weth.withdraw(ethAmountOut);

399:         weth.withdraw(amountOut);

445:         weth.withdraw(amountOut);

491:         weth.withdraw(amountOut);

500:         (shares, , ) = IMagicLP(lp).buyShares(to);

547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));

550:                 IMagicLP(path[i]).sellQuote(address(path[i + 1]));

561:             amountOut = IMagicLP(path[iterations]).sellBase(to);

563:             amountOut = IMagicLP(path[iterations]).sellQuote(to);

572:         amountOut = IMagicLP(lp).sellBase(to);

579:         amountOut = IMagicLP(lp).sellQuote(to);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L579-L579)

</details>

### <a name="GAS-8-1693311599"></a>[GAS-8] Use assembly to calculate hashes to save gas
Using assembly to calculate hashes can save *** 80 gas *** per instance

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/periphery/Factory.sol

163:         return keccak256(abi.encodePacked(sender_, implementation, baseToken_, quoteToken_, lpFeeRate_, i_, k_));

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L163)

</details>

### <a name="GAS-9-1693311695"></a>[GAS-9] Optimize Address Storage Value Management with `assembly`
As the following instances does not pack address variables with others, then using Assembly will save gas when storing address value

*Instances (15)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

33:         feeTo = feeTo_;

77:         feeTo = feeTo_;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L77-L77)

```solidity
File: /src/blast/BlastGovernor.sol

20:         feeTo = feeTo_;

45:         feeTo = _feeTo;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastGovernor.sol#L45-L45)

```solidity
File: /src/blast/BlastOnboarding.sol

94:         feeTo = feeTo_;

152:         feeTo = feeTo_;

191:         bootstrapper = bootstrapper_;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L191-L191)

```solidity
File: /src/blast/BlastWrappers.sol

55:         _governor = governor_;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastWrappers.sol#L55-L55)

```solidity
File: /src/mimswap/MagicLP.sol

119:         _BASE_TOKEN_ = baseTokenAddress;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L119-L119)

```solidity
File: /src/mimswap/auxiliary/FeeRateModel.sol

27:         maintainer = maintainer_;

51:         maintainer = maintainer_;

58:         implementation = implementation_;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModel.sol#L58-L58)

```solidity
File: /src/mimswap/periphery/Factory.sol

45:         implementation = implementation_;

101:         implementation = implementation_;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L101-L101)

```solidity
File: /src/staking/LockingMultiRewards.sol

135:         stakingToken = _stakingToken;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L135-L135)

</details>

### <a name="GAS-10-1693311732"></a>[GAS-10] Use assembly to emit events
We can use assembly to emit events efficiently by utilizing `scratch space` and the `free memory pointer`. This will allow us to potentially avoid memory expansion costs. Note: In order to do this optimization safely, we will need to cache and restore the free memory pointer.

*Instances (59)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

78:         emit LogFeeToChanged(feeTo_);

90:         emit LogTokenDepositEnabled(token, enabled);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L90)

```solidity
File: /src/blast/BlastGovernor.sol

46:         emit LogFeeToChanged(_feeTo);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastGovernor.sol#L46)

```solidity
File: /src/blast/BlastMagicLP.sol

86:         emit LogFeeToChanged(feeTo_);

91:         emit LogOperatorChanged(operator, status);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L91)

```solidity
File: /src/blast/BlastOnboarding.sol

120:         emit LogDeposit(msg.sender, token, amount, lock_);

129:         emit LogLock(msg.sender, token, amount);

140:         emit LogWithdraw(msg.sender, token, amount);

153:         emit LogFeeToChanged(feeTo_);

182:         emit LogTokenSupported(token, supported);

187:         emit LogTokenCapChanged(token, cap);

192:         emit LogBootstrapperChanged(bootstrapper_);

197:         emit LogStateChange(State.Opened);

202:         emit LogStateChange(State.Closed);

211:         emit LogTokenRescue(token, to, amount);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L211)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

71:         emit LogClaimed(msg.sender, shares, lock);

124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

132:         emit LogInitialized(_router);

143:         emit LogStakingChanged(address(_staking));

148:         emit LogReadyChanged(ready);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L148)

```solidity
File: /src/blast/BlastTokenRegistry.sol

20:         emit LogNativeYieldTokenEnabled(token, enabled);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastTokenRegistry.sol#L20)

```solidity
File: /src/blast/libraries/BlastYields.sol

26:         emit LogBlastTokenClaimableEnabled(address(this), token);

31:         emit LogBlastNativeClaimableEnabled(address(this));

44:         emit LogBlastGasClaimed(recipient, amount);

57:         emit LogBlastETHClaimed(recipient, amount);

62:         emit LogBlastETHClaimed(recipient, amount);

72:         emit LogBlastTokenClaimed(recipient, address(token), amount);

77:         emit LogBlastTokenClaimed(recipient, address(token), amount);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastYields.sol#L77)

```solidity
File: /src/mimswap/MagicLP.sol

259:             emit RChange(newRState);

264:         emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

282:             emit RChange(newRState);

287:         emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

323:                 emit RChange(newRState);

325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

345:                 emit RChange(newRState);

347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

352:         emit FlashLoan(msg.sender, assetTo, baseAmount, quoteAmount);

409:         emit BuyShares(to, shares, balanceOf(to));

454:         emit SellShares(msg.sender, to, shareAmount, balanceOf(msg.sender));

467:         emit TokenRescue(token, to, amount);

501:         emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L501)

```solidity
File: /src/mimswap/auxiliary/FeeRateModel.sol

52:         emit LogMaintainerChanged(maintainer_);

59:         emit LogImplementationChanged(implementation_);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModel.sol#L59)

```solidity
File: /src/mimswap/periphery/Factory.sol

88:         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);

102:         emit LogSetImplementation(implementation_);

111:         emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);

141:         emit LogPoolRemoved(pool);

152:         emit LogPoolAdded(baseToken, quoteToken, creator, pool);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L152)

```solidity
File: /src/staking/LockingMultiRewards.sol

183:         emit LogWithdrawn(msg.sender, amount);

318:         emit LogSetMinLockAmount(minLockAmount, _minLockAmount);

331:         emit LogRecovered(tokenAddress, tokenAmount);

392:         emit LogRewardAdded(amount);

436:                 emit LogLockIndexChanged(user, lastIndex, index);

447:             emit LogUnlocked(user, amount, index);

475:             emit LogStaked(account, amount);

513:         emit LogLocked(user, amount, _nextUnlockTime, lockCount);

611:             emit LogRewardLockCreated(user, _rewardLock.unlockTime);

638:                         emit LogRewardPaid(user, rewardToken, amount);

651:             emit LogRewardLocked(user, rewardToken, rewardAmount);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L651)

</details>

### <a name="GAS-11-1693311856"></a>[GAS-11] Using bools for storage incurs overhead
Use uint256(1) and uint256(2) for true/false to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from 'false' to 'true', after having been 'true' in the past. See [source](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27).

*Instances (8)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

//@audit avoid using `bool` type for mapping values
21:     mapping(address => bool) public enabledTokens;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L21)

```solidity
File: /src/blast/BlastMagicLP.sol

//@audit avoid using `bool` type for mapping values
21:     mapping(address => bool) public operators;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L21)

```solidity
File: /src/blast/BlastOnboarding.sol

//@audit avoid using `bool` type for mapping values
36:     mapping(address token => bool) public supportedTokens;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L36)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

//@audit avoid using `bool` type for ready
28:     bool public ready;

//@audit avoid using `bool` type for mapping values
30:     mapping(address user => bool claimed) public claimed;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L30)

```solidity
File: /src/blast/BlastTokenRegistry.sol

//@audit avoid using `bool` type for mapping values
10:     mapping(address => bool) public nativeYieldTokens;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastTokenRegistry.sol#L10)

```solidity
File: /src/mimswap/MagicLP.sol

//@audit avoid using `bool` type for _INITIALIZED_
68:     bool internal _INITIALIZED_;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L68)

```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit change `exists` to `uint256`
50:     struct Reward {
            uint256 periodFinish;
            uint256 rewardRate;
            uint256 rewardPerTokenStored;
            bool exists;
            uint248 lastUpdateTime;
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L50-L56)

</details>

### <a name="GAS-12-1693311904"></a>[GAS-12] Cache array length outside of loop
If not cached, the solidity compiler will always read the length of the array during each iteration. That is, if it is a storage array, this is an extra sload operation (100 additional extra gas for each iteration except for the first) and if it is a memory array, this is an extra mload operation (3 additional gas for each iteration except for the first).

*Instances (7)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

165:         for (uint256 i = 0; i < tokens.length; i++) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L165)

```solidity
File: /src/staking/LockingMultiRewards.sol

405:         for (uint256 i; i < users.length; ) {

547:         for (uint256 i; i < rewardTokens.length; ) {

561:         for (uint256 i; i < rewardTokens.length; ) {

575:         for (uint256 i; i < rewardTokens.length; ) {

580:             for (uint256 j; j < users.length; ) {

614:         for (uint256 i; i < rewardTokens.length; ) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L614)

</details>

### <a name="GAS-13-1693311936"></a>[GAS-13] State variables should be cached in stack variables rather than re-reading them from storage
The instances below point to the second+ access of a state variable within a function. Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.

*Saves 100 gas per instance*

*Instances (11)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/MagicLP.sol

146:             _BASE_TARGET_ = _BASE_RESERVE_;

147:             _QUOTE_TARGET_ = _QUOTE_RESERVE_;

331:             uint256 baseInput = baseBalance - uint256(_BASE_RESERVE_);

337:             if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {

347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

381:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;

402:             _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

403:             _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();

438:         _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));

439:         _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L439)

</details>

### <a name="GAS-14-1699447317"></a>[GAS-14] Avoid caching global special variables
It's better not to cache the global special variables, because it's cheaper to use them directly (e.g. `msg.sender`).

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/periphery/Factory.sol

82:         address creator = tx.origin;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L82)

</details>

### <a name="GAS-15-1693311965"></a>[GAS-15] With assembly, `.call (bool success)` transfer can be done gas-optimized
`return` data `(bool success,)` has to be stored due to EVM architecture, but in a usage like below, `out` and `outsize` values are given (0,0), this storage disappears and gas optimization is provided.

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastGovernor.sol

54:         (success, result) = to.call{value: value}(data);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastGovernor.sol#L54)

</details>

### <a name="GAS-16-1693311951"></a>[GAS-16] Use calldata instead of memory for function arguments that do not get mutated
Mark data types as `calldata` instead of `memory` where possible. This makes it so that the data is not automatically loaded into memory. If the data passed into the function does not need to be changed (like updating values in an array), it can be passed in as `calldata`. The one exception to this is if the argument must later be passed into another function that takes an argument that specifies `memory` storage.

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

//@audit Make `tokens` as a calldata
164:     function claimTokenYields(address[] memory tokens) external onlyOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L164)

</details>

### <a name="GAS-17-1693312015"></a>[GAS-17] Add `unchecked {}` for subtractions where the operands cannot underflow because of a previous `require()` or `if`-statement
`require(a <= b); x = b - a` => `require(a <= b); unchecked { x = b - a }`

*Instances (5)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/libraries/Math.sol

175:             bAbs = bAbs - part2;

178:             bAbs = part2 - bAbs;

203:             return V1 - V2;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L203)

```solidity
File: /src/mimswap/libraries/PMMPricing.sol

65:                 receiveQuoteAmount = backToOneReceiveQuote + _ROneSellBaseToken(state, payBaseAmount - backToOnePayBase);

96:                 receiveBaseAmount = backToOneReceiveBase + _ROneSellQuoteToken(state, payQuoteAmount - backToOnePayQuote);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/PMMPricing.sol#L96)

</details>

### <a name="GAS-18-1693312028"></a>[GAS-18] `x += y` costs more gas than `x = x + y` for state variables
Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.

*Instances (9)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/MagicLP.sol

553:                 _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L553)

```solidity
File: /src/staking/LockingMultiRewards.sol

163:         unlockedSupply -= amount;

178:         unlockedSupply -= amount;

181:         stakingTokenBalance -= amount;

441:             unlockedSupply += amount;

442:             lockedSupply -= amount;

465:         stakingTokenBalance += amount;

473:             unlockedSupply += amount;

486:         lockedSupply += amount;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L486)

</details>

### <a name="GAS-19-1696084432"></a>[GAS-19] Simple checks for zero `uint` can be done using assembly to save gas

*Instances (37)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboardingBoot.sol

64:         if (shares == 0) {

158:         if (totalLocked == 0) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L158)

```solidity
File: /src/mimswap/MagicLP.sol

108:         if (i == 0 || i > MAX_I) {

369:         if (baseInput == 0) {

375:         if (totalSupply() == 0) {

377:             if (quoteBalance == 0) {

385:             if (_QUOTE_TARGET_ == 0) {

483:         if (newI == 0 || newI > MAX_I) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L483)

```solidity
File: /src/mimswap/libraries/DecimalMath.sol

48:         if (e == 0) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/DecimalMath.sol#L48)

```solidity
File: /src/mimswap/libraries/Math.sol

52:         if (V0 == 0) {

58:         if (k == 0) {

80:         if (k == 0) {

89:         if (V1 == 0) {

94:         if (ki == 0) {

132:         if (V0 == 0) {

136:         if (delta == 0) {

140:         if (k == 0) {

153:             if (idelta == 0) {

192:             if (numerator == 0) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L192)

```solidity
File: /src/mimswap/periphery/Router.sol

125:         if (baseInAmount == 0) {

131:         if (totalSupply == 0) {

132:             if (quoteBalance == 0) {

327:         if (directions & 1 == 0) {

348:         if (directions & 1 == 0) {

379:         if ((directions >> lastLpIndex) & 1 == 0) {

392:         if (directions & 1 == 0) {

521:         if (IERC20(lp).totalSupply() == 0) {

545:             if (directions & 1 == 0) {

560:         if ((directions & 1 == 0)) {

599:         if (baseDecimals == 0 || quoteDecimals == 0) {

599:         if (baseDecimals == 0 || quoteDecimals == 0) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L599)

```solidity
File: /src/staking/LockingMultiRewards.sol

156:         if (amount == 0) {

171:         if (amount == 0) {

278:         if (totalSupply_ == 0) {

410:             if (locks.length == 0) {

459:         if (amount == 0) {

490:         if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L490)

</details>

### <a name="GAS-20-1708173673"></a>[GAS-20] Combine `mapping`s referenced in the same function by the same key
Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot (i.e. runtime gas savings). Even if the values can't be packed, if both fields are accessed in the same function (as is the case for these instances), combining them can save **~42 gas per access** due to [not having to recalculate the key's keccak256 hash](https://gist.github.com/IllIllI000/639032d73e35d7e968ff58d8784bc445) (Gkeccak256 - 30 gas) and that calculation's associated stack operations.

*Instances (2)*:
<details><summary> see instances </summary>

```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit the following two maps should be combined : `userRewardPerTokenPaid` and `rewards`
292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {
             uint256 pendingUserRewardsPerToken = rewardPerToken_ - userRewardPerTokenPaid[user][rewardToken];
             return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];
         }

//@audit the following two maps should be combined : `rewards` and `userRewardPerTokenPaid`
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
             rewards[user_][token_] = _earned(user_, balance_, token_, rewardPerToken_);
             userRewardPerTokenPaid[user_][token_] = rewardPerToken_;
         }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L536-L539)

</details>

### <a name="GAS-21-1706544439"></a>[GAS-21] Counting down in for statements is more gas efficient
Looping downwards in Solidity is more gas efficient due to how the EVM compares variables. In a 'for' loop that counts down, the end condition is usually to compare with zero, which is cheaper than comparing with another number. As such, restructure your loops to count downwards where possible.

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

165:         for (uint256 i = 0; i < tokens.length; i++) {
                 if (!supportedTokens[tokens[i]]) {
                     revert ErrUnsupportedToken();
                 }
                 if (registry.nativeYieldTokens(tokens[i])) {
                     BlastYields.claimAllTokenYields(tokens[i], feeTo);
                 }
             }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L165-L172)

</details>

### <a name="GAS-22-1693312114"></a>[GAS-22] Divisions which do not divide by -X cannot overflow or overflow so such operations can be unchecked to save gas
Make such found divisions are unchecked when ensured it is safe to do so

*Instances (40)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboardingBoot.sol

163:         return (userLocked * totalPoolShares) / totalLocked;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L163)

```solidity
File: /src/mimswap/MagicLP.sol

435:         baseAmount = (baseBalance * shareAmount) / totalShares;

436:         quoteAmount = (quoteBalance * shareAmount) / totalShares;

513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L517)

```solidity
File: /src/mimswap/libraries/DecimalMath.sol

24:         return (target * d) / ONE;

32:         return (target * ONE) / d;

40:         return ONE2 / target;

53:             uint p = powFloor(target, e / 2);

54:             p = (p * p) / ONE;

56:                 p = (p * target) / ONE;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/DecimalMath.sol#L56)

```solidity
File: /src/mimswap/libraries/Math.sol

20:         uint256 quotient = a / b;

30:         uint256 z = x / 2 + 1;

34:             z = (x / z + z) / 2;

34:             z = (x / z + z) / 2;

59:             return fairAmount / DecimalMath.ONE;

62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

64:         return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;

96:         } else if ((ki * delta) / ki == delta) {

97:             _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);

99:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);

155:             } else if ((idelta * V1) / idelta == V1) {

156:                 temp = (idelta * V1) / (V0 * V0);

158:                 temp = (((delta * V1) / V0) * i) / V0;

158:                 temp = (((delta * V1) / V0) * i) / V0;

160:             return (V1 * temp) / (temp + DecimalMath.ONE);

170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB

181:         bAbs = bAbs / DecimalMath.ONE;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L181)

```solidity
File: /src/mimswap/libraries/PMMPricing.sol

205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);

209:             uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/PMMPricing.sol#L209)

```solidity
File: /src/mimswap/periphery/Router.sol

257:         baseAmountOut = (baseBalance * sharesIn) / totalShares;

258:         quoteAmountOut = (quoteBalance * sharesIn) / totalShares;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L258)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

45:         return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L45)

```solidity
File: /src/staking/LockingMultiRewards.sol

144:         maxLocks = _lockDuration / _rewardsDuration;

236:         return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);

241:         return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);

258:         return (block.timestamp / rewardsDuration) * rewardsDuration;

283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

294:         return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];

388:         reward.rewardRate = amount / _remainingRewardTime;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L388)

</details>

### <a name="GAS-23-1693312130"></a>[GAS-23] Do not calculate constants
Due to how constant variables are implemented (replacements at compile-time), an expression assigned to a constant variable is recomputed each time that the variable is used, which wastes some gas. Even with optimizer enabled, gas consumtion is reduced when the constant is already calculated.

*Instances (4)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/MagicLP.sol

63:     uint256 public constant MAX_I = 10 ** 36;

64:     uint256 public constant MAX_K = 10 ** 18;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L64-L64)

```solidity
File: /src/mimswap/libraries/DecimalMath.sol

20:     uint256 internal constant ONE = 10 ** 18;

21:     uint256 internal constant ONE2 = 10 ** 36;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/DecimalMath.sol#L21-L21)

</details>

### <a name="GAS-24-1694877823"></a>[GAS-24] Use `do while` loops instead of `for` loops
A `do while` loop will cost less gas since the condition is not being checked for the first iteration, Check my example on [github](https://github.com/he110-1/gasOptimization/blob/main/forToDoWhileOptimizationProof.sol). Actually, `do while` alwayse cast less gas compared to `For` check my second example [github](https://github.com/he110-1/gasOptimization/blob/main/forToDoWhileOptimizationProof2.sol)

*Instances (8)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

165:         for (uint256 i = 0; i < tokens.length; i++) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L165)

```solidity
File: /src/mimswap/periphery/Router.sol

544:         for (uint256 i = 0; i < iterations; ) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L544)

```solidity
File: /src/staking/LockingMultiRewards.sol

405:         for (uint256 i; i < users.length; ) {

547:         for (uint256 i; i < rewardTokens.length; ) {

561:         for (uint256 i; i < rewardTokens.length; ) {

575:         for (uint256 i; i < rewardTokens.length; ) {

580:             for (uint256 j; j < users.length; ) {

614:         for (uint256 i; i < rewardTokens.length; ) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L614)

</details>

### <a name="GAS-25-1693312160"></a>[GAS-25] Stack variable cost less while used in emiting event
Even if the variable is going to be used only one time, caching a state variable and use its cache in an emit would help you reduce the cost by at least ***9 gas***

*Instances (16)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboardingBoot.sol

// @audit `pool` is a state variable
124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

// @audit `totalPoolShares` is a state variable
124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

// @audit `staking` is a state variable
124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

// @audit `ready` is a state variable
148:         emit LogReadyChanged(ready);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L148)

```solidity
File: /src/mimswap/MagicLP.sol

// @audit `_BASE_TOKEN_` is a state variable
264:         emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

// @audit `_QUOTE_TOKEN_` is a state variable
264:         emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

// @audit `_QUOTE_TOKEN_` is a state variable
287:         emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

// @audit `_BASE_TOKEN_` is a state variable
287:         emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

// @audit `_QUOTE_TOKEN_` is a state variable
325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

// @audit `_BASE_TOKEN_` is a state variable
325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

// @audit `_BASE_TOKEN_` is a state variable
347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

// @audit `_QUOTE_TOKEN_` is a state variable
347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L347)

```solidity
File: /src/mimswap/periphery/Factory.sol

// @audit `maintainerFeeRateModel` is a state variable
88:         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);

// @audit `pool` is a state variable
141:         emit LogPoolRemoved(pool);

// @audit `pool` is a state variable
152:         emit LogPoolAdded(baseToken, quoteToken, creator, pool);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L152)

```solidity
File: /src/staking/LockingMultiRewards.sol

// @audit `minLockAmount` is a state variable
318:         emit LogSetMinLockAmount(minLockAmount, _minLockAmount);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L318)

</details>

### <a name="GAS-26-1693312222"></a>[GAS-26] Events should be emitted outside of loops
Emitting an event has an overhead of **375 gas**, which will be incurred on every iteration of the loop. It is cheaper to `emit` only [once](https://github.com/ethereum/EIPs/blob/adad5968fd6de29902174e0cb51c8fc3dceb9ab5/EIPS/eip-1155.md?plain=1#L68) after the loop has finished.

*Instances (4)*:
<details><summary> see instances </summary>

```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit LogUnlocked is emited inside this loop
405:         for (uint256 i; i < users.length; ) {
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

//@audit LogLockIndexChanged is emited inside this loop
405:         for (uint256 i; i < users.length; ) {
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

//@audit LogRewardLocked is emited inside this loop
614:         for (uint256 i; i < rewardTokens.length; ) {
                 address rewardToken = rewardTokens[i];
                 uint256 rewardAmount = rewards[user][rewardToken];
     
                 // in all scenario, reset the reward amount immediately
                 rewards[user][rewardToken] = 0;
     
                 // don't assume the rewardTokens array is always the same length as the items array
                 // as new reward tokens can be added by the owner
                 if (i < rewardItemLength) {
                     RewardLockItem storage item = _rewardLock.items[i];
     
                     // expired lock, claim existing unlocked rewards if any
                     if (expired) {
                         uint256 amount = item.amount;
     
                         // since this current lock is expired and that item index
                         // matches the reward index, override the current amount
                         // with the new locked amount.
                         item.amount = rewardAmount;
     
                         // use cached amount
                         if (amount > 0) {
                             rewardToken.safeTransfer(user, amount);
                             emit LogRewardPaid(user, rewardToken, amount);
                         }
                     } else {
                         // not expired, just add to the existing lock
                         item.amount += rewardAmount;
                     }
                 }
                 // new reward token, create a new lock item
                 // could mean it's adding to an existing lock or creating a new one
                 else {
                     _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
                 }
     
                 emit LogRewardLocked(user, rewardToken, rewardAmount);

//@audit LogRewardPaid is emited inside this loop
614:         for (uint256 i; i < rewardTokens.length; ) {
                 address rewardToken = rewardTokens[i];
                 uint256 rewardAmount = rewards[user][rewardToken];
     
                 // in all scenario, reset the reward amount immediately
                 rewards[user][rewardToken] = 0;
     
                 // don't assume the rewardTokens array is always the same length as the items array
                 // as new reward tokens can be added by the owner
                 if (i < rewardItemLength) {
                     RewardLockItem storage item = _rewardLock.items[i];
     
                     // expired lock, claim existing unlocked rewards if any
                     if (expired) {
                         uint256 amount = item.amount;
     
                         // since this current lock is expired and that item index
                         // matches the reward index, override the current amount
                         // with the new locked amount.
                         item.amount = rewardAmount;
     
                         // use cached amount
                         if (amount > 0) {
                             rewardToken.safeTransfer(user, amount);
                             emit LogRewardPaid(user, rewardToken, amount);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L614-L638)

</details>

### <a name="GAS-27-1693312354"></a>[GAS-27] The result of function calls should be cached rather than re-calling the function
The instances below point to the second+ call of the function within a single function

*Instances (2)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/MagicLP.sol

// @audit _MT_FEE_RATE_MODEL_.maintainer() is called 2 times in the function `flashLoan`
290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
             _transferBaseOut(assetTo, baseAmount);
             _transferQuoteOut(assetTo, quoteAmount);
     
             if (data.length > 0) {
                 ICallee(assetTo).FlashLoanCall(msg.sender, baseAmount, quoteAmount, data);
             }
     
             uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
             uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
     
             // no input -> pure loss
             if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
                 revert ErrFlashLoanFailed();
             }
     
             // sell quote case
             // quote input + base output
             if (baseBalance < _BASE_RESERVE_) {
                 uint256 quoteInput = quoteBalance - uint256(_QUOTE_RESERVE_);
                 (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) = querySellQuote(
                     tx.origin,
                     quoteInput
                 );
     
                 if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {
                     revert ErrFlashLoanFailed();
                 }
     
                 _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
                 if (_RState_ != uint32(newRState)) {
                     _QUOTE_TARGET_ = newQuoteTarget.toUint112();
                     _RState_ = uint32(newRState);
                     emit RChange(newRState);
                 }
                 emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);
             }
     
             // sell base case
             // base input + quote output
             if (quoteBalance < _QUOTE_RESERVE_) {
                 uint256 baseInput = baseBalance - uint256(_BASE_RESERVE_);
                 (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) = querySellBase(
                     tx.origin,
                     baseInput
                 );
     
                 if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {
                     revert ErrFlashLoanFailed();
                 }
     
                 _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
                 if (_RState_ != uint32(newRState)) {
                     _BASE_TARGET_ = newBaseTarget.toUint112();
                     _RState_ = uint32(newRState);
                     emit RChange(newRState);
                 }
                 emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
             }
     
             _sync();
     
             emit FlashLoan(msg.sender, assetTo, baseAmount, quoteAmount);
         }

// @audit totalSupply() is called 2 times in the function `buyShares`
360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
             uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
             uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
             uint256 baseReserve = _BASE_RESERVE_;
             uint256 quoteReserve = _QUOTE_RESERVE_;
     
             baseInput = baseBalance - baseReserve;
             quoteInput = quoteBalance - quoteReserve;
     
             if (baseInput == 0) {
                 revert ErrNoBaseInput();
             }
     
             // Round down when withdrawing. Therefore, never be a situation occurring balance is 0 but totalsupply is not 0
             // But May Happenoe 0 But totalSupply = 0
             if (totalSupply() == 0) {
                 // case 1. initial supply
                 if (quoteBalance == 0) {
                     revert ErrZeroQuoteAmount();
                 }
     
                 shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;
                 _BASE_TARGET_ = shares.toUint112();
                 _QUOTE_TARGET_ = DecimalMath.mulFloor(shares, _I_).toUint112();
     
                 if (_QUOTE_TARGET_ == 0) {
                     revert ErrZeroQuoteTarget();
                 }
     
                 if (shares <= 2001) {
                     revert ErrMintAmountNotEnough();
                 }
     
                 _mint(address(0), 1001);
                 shares -= 1001;
             } else if (baseReserve > 0 && quoteReserve > 0) {
                 // case 2. normal case
                 uint256 baseInputRatio = DecimalMath.divFloor(baseInput, baseReserve);
                 uint256 quoteInputRatio = DecimalMath.divFloor(quoteInput, quoteReserve);
                 uint256 mintRatio = quoteInputRatio < baseInputRatio ? quoteInputRatio : baseInputRatio;
                 shares = DecimalMath.mulFloor(totalSupply(), mintRatio);
     
                 _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();
                 _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
             }
     
             _mint(to, shares);
             _setReserve(baseBalance, quoteBalance);
     
             emit BuyShares(to, shares, balanceOf(to));
         }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L360-L410)

</details>

### <a name="GAS-28-1693312400"></a>[GAS-28] Don't initialize `uint` variables with default value
The default value for variables is zero, so initializing them to zero is superfluous.

*Instances (2)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

165:         for (uint256 i = 0; i < tokens.length; i++) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L165)

```solidity
File: /src/mimswap/periphery/Router.sol

544:         for (uint256 i = 0; i < iterations; ) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L544)

</details>

### <a name="GAS-29-1693312433"></a>[GAS-29] `internal` functions only called once can be inlined to save gas
Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.

*Instances (5)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/MagicLP.sol

528:     function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {

601:     function _afterInitialized() internal virtual {}

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L601)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

33:     function _getReserves() internal view virtual returns (uint256, uint256) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L33)

```solidity
File: /src/staking/LockingMultiRewards.sol

544:     function _updateRewards() internal {

572:     function _updateRewardsForUsers(address[] memory users) internal {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L572)

</details>

### <a name="GAS-30-1709377588"></a>[GAS-30] Avoid emitting event on every iteration
Emitting events within a loop can cause significant gas consumption due to repeated I/O operations. Instead, accumulate changes in memory and emit a single event post-loop with aggregated data. This approach improves contract efficiency, reduces gas costs, and simplifies event tracking for event listeners.

*Instances (2)*:
<details><summary> see instances </summary>

```solidity
File: /src/staking/LockingMultiRewards.sol

405:         for (uint256 i; i < users.length; ) {
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

614:         for (uint256 i; i < rewardTokens.length; ) {
                 address rewardToken = rewardTokens[i];
                 uint256 rewardAmount = rewards[user][rewardToken];
     
                 // in all scenario, reset the reward amount immediately
                 rewards[user][rewardToken] = 0;
     
                 // don't assume the rewardTokens array is always the same length as the items array
                 // as new reward tokens can be added by the owner
                 if (i < rewardItemLength) {
                     RewardLockItem storage item = _rewardLock.items[i];
     
                     // expired lock, claim existing unlocked rewards if any
                     if (expired) {
                         uint256 amount = item.amount;
     
                         // since this current lock is expired and that item index
                         // matches the reward index, override the current amount
                         // with the new locked amount.
                         item.amount = rewardAmount;
     
                         // use cached amount
                         if (amount > 0) {
                             rewardToken.safeTransfer(user, amount);
                             emit LogRewardPaid(user, rewardToken, amount);
                         }
                     } else {
                         // not expired, just add to the existing lock
                         item.amount += rewardAmount;
                     }
                 }
                 // new reward token, create a new lock item
                 // could mean it's adding to an existing lock or creating a new one
                 else {
                     _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
                 }
     
                 emit LogRewardLocked(user, rewardToken, rewardAmount);
     
                 unchecked {
                     ++i;
                 }
             }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L614-L656)

</details>

### <a name="GAS-31-1702129464"></a>[GAS-31] Refactor modifiers to call a local function
Modifiers code is copied in all instances where it's used, increasing bytecode size. By doing a refractor to the internal function, one can reduce bytecode size significantly at the cost of one JUMP.

*Instances (6)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

43:     modifier onlyState(State _state) {
            if (state != _state) {
                revert ErrWrongState();
            }
            _;
        }

50:     modifier onlySupportedTokens(address token) {
            if (!supportedTokens[token]) {
                revert ErrUnsupportedToken();
            }
    
            _;
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L50-L56)

```solidity
File: /src/mimswap/MagicLP.sol

607:     modifier onlyImplementationOwner() {
             if (msg.sender != implementation.owner()) {
                 revert ErrNotImplementationOwner();
             }
             _;
         }

614:     modifier onlyClones() {
             if (address(this) == address(implementation)) {
                 revert ErrNotClone();
             }
             _;
         }

621:     modifier onlyImplementation() {
             if (address(this) != address(implementation)) {
                 revert ErrNotImplementation();
             }
             _;
         }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L621-L626)

```solidity
File: /src/mimswap/periphery/Router.sol

47:     modifier ensureDeadline(uint256 deadline) {
            if (block.timestamp > deadline) {
                revert ErrExpired();
            }
            _;
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L47-L52)

</details>

### <a name="GAS-32-1693312642"></a>[GAS-32] Multiple `address`/ID mappings can be combined into a single `mapping` of an `address`/ID to a `struct`, where appropriate
Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (**20000 gas**) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save **~42 gas per access** due to [not having to recalculate the key's keccak256 hash](https://gist.github.com/IllIllI000/ec23a57daa30a8f8ca8b9681c8ccefb0) (Gkeccak256 - 30 gas) and that calculation's associated stack operations.

*Instances (13)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

36:     mapping(address token => bool) public supportedTokens;

37:     mapping(address token => Balances) public totals;

38:     mapping(address token => uint256 cap) public caps;

41:     mapping(address user => mapping(address token => Balances)) public balances;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L41)

```solidity
File: /src/mimswap/periphery/Factory.sol

35:     mapping(address base => mapping(address quote => address[] pools)) public pools;

36:     mapping(address creator => address[] pools) public userPools;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L36)

```solidity
File: /src/staking/LockingMultiRewards.sol

89:     mapping(address token => Reward info) private _rewardData;

90:     mapping(address user => Balances balances) private _balances;

91:     mapping(address user => LockedBalance[] locks) private _userLocks;

92:     mapping(address user => RewardLock rewardLock) private _userRewardLock;

94:     mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;

95:     mapping(address user => mapping(address token => uint256 amount)) public rewards;

96:     mapping(address user => uint256 index) public lastLockIndex;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L96)

</details>

### <a name="GAS-33-1693312655"></a>[GAS-33] Optimize names to save gas
`public`/`external` function names and `public` member variable names can be optimized to save gas. See [this](https://gist.github.com/IllIllI000/a5d8b486a8259f9f77891a919febd1a9) link for an example of how it works. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save **128 gas** each during deployment, and renaming functions to have lower method IDs will save **22 gas** per call, [per sorted position shifted](https://medium.com/joyso/solidity-how-does-function-name-affect-gas-consumption-in-smart-contract-47d270d8ac92)

*Instances (12)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

// @audit claimGasYields() ==> claimGasYields_Aq4(),00007334
// @audit claimTokenYields(address) ==> claimTokenYields_T1S(address),000000c3
// @audit callBlastPrecompile(bytes) ==> callBlastPrecompile_7mf(bytes),000081ea
// @audit setFeeTo(address) ==> setFeeTo_i9Q(address),00002f43
// @audit setTokenEnabled(address,bool) ==> setTokenEnabled_Ehy(address,bool),00009659
13: contract BlastBox is DegenBox, OperatableV3 {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L13)

```solidity
File: /src/blast/BlastGovernor.sol

// @audit claimMaxGasYields(address) ==> claimMaxGasYields_nQ(address),000052d7
// @audit setFeeTo(address) ==> setFeeTo_i9Q(address),00002f43
// @audit callBlastPrecompile(bytes) ==> callBlastPrecompile_7mf(bytes),000081ea
// @audit execute(address,uint256,bytes) ==> execute_ncC(address,uint256,bytes),0000189a
7: contract BlastGovernor is OperatableV2 {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastGovernor.sol#L7)

```solidity
File: /src/blast/BlastMagicLP.sol

// @audit claimGasYields() ==> claimGasYields_Aq4(),00007334
// @audit claimTokenYields() ==> claimTokenYields_i5S(),00005a04
// @audit updateTokenClaimables() ==> updateTokenClaimables_Y6t(),00008151
// @audit callBlastPrecompile(bytes) ==> callBlastPrecompile_7mf(bytes),000081ea
// @audit setFeeTo(address) ==> setFeeTo_i9Q(address),00002f43
// @audit setOperator(address,bool) ==> setOperator_Z3U(address,bool),00000423
10: contract BlastMagicLP is MagicLP {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L10)

```solidity
File: /src/blast/BlastOnboarding.sol

// @audit deposit(address,uint256,bool) ==> deposit_T3W(address,uint256,bool),0000b291
// @audit lock(address,uint256) ==> lock_xhR(address,uint256),0000e7cd
// @audit withdraw(address,uint256) ==> withdraw_i8W(address,uint256),000009ff
// @audit setFeeTo(address) ==> setFeeTo_i9Q(address),00002f43
// @audit callBlastPrecompile(bytes) ==> callBlastPrecompile_7mf(bytes),000081ea
// @audit claimGasYields() ==> claimGasYields_Aq4(),00007334
// @audit claimTokenYields(address[]) ==> claimTokenYields_e2B(address[]),0000a326
// @audit setTokenSupported(address,bool) ==> setTokenSupported_A2U(address,bool),0000ef8a
// @audit setCap(address,uint256) ==> setCap_Jdl(address,uint256),0000e87e
// @audit setBootstrapper(address) ==> setBootstrapper_8cm(address),0000e894
// @audit open() ==> open_LsM(),00007b50
// @audit close() ==> close_A2E(),00007593
// @audit rescue(address,address,uint256) ==> rescue_Evi(address,address,uint256),000087c5
// @audit pause() ==> pause_yiS(),00002a4b
// @audit unpause() ==> unpause_88B(),000051b7
64: contract BlastOnboarding is BlastOnboardingData, Proxy {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L64)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

// @audit claim(bool) ==> claim_0co(bool),00001873
// @audit claimable(address) ==> claimable_aqs(address),0000f45e
// @audit previewTotalPoolShares() ==> previewTotalPoolShares_UCY(),0000e752
// @audit setReady(bool) ==> setReady_x1P(bool),00002b58
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L34)

```solidity
File: /src/blast/BlastTokenRegistry.sol

// @audit setNativeYieldTokenEnabled(address,bool) ==> setNativeYieldTokenEnabled_na7(address,bool),000067ab
6: contract BlastTokenRegistry is Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastTokenRegistry.sol#L6)

```solidity
File: /src/mimswap/MagicLP.sol

// @audit init(address,address,uint256,address,uint256,uint256) ==> init_nfr(address,address,uint256,address,uint256,uint256),0000296a
// @audit sync() ==> sync_KhJ(),0000d426
// @audit correctRState() ==> correctRState_F5G(),0000351d
// @audit querySellBase(address,uint256) ==> querySellBase_wA(address,uint256),000006dd
// @audit querySellQuote(address,uint256) ==> querySellQuote_81C(address,uint256),000025f7
// @audit getPMMState() ==> getPMMState_hM1H(),0000629b
// @audit getPMMStateForCall() ==> getPMMStateForCall_3lo(),0000e373
// @audit getMidPrice() ==> getMidPrice_43s(),00004bab
// @audit getReserves() ==> getReserves_j97(),00006651
// @audit getUserFeeRate(address) ==> getUserFeeRate_uqo(address),00009353
// @audit getBaseInput() ==> getBaseInput_U7z(),00002060
// @audit getQuoteInput() ==> getQuoteInput_gbv(),0000b101
// @audit version() ==> version_Z5x(),00005021
// @audit sellBase(address) ==> sellBase_Sl7(address),0000724d
// @audit sellQuote(address) ==> sellQuote_9Vj(address),00005fe6
// @audit flashLoan(uint256,uint256,address,bytes) ==> flashLoan_LFn(uint256,uint256,address,bytes),00006cc8
// @audit buyShares(address) ==> buyShares_doK(address),0000f61a
// @audit sellShares(uint256,address,uint256,uint256,bytes,uint256) ==> sellShares_8jA(uint256,address,uint256,uint256,bytes,uint256),00000680
// @audit rescue(address,address,uint256) ==> rescue_Evi(address,address,uint256),000087c5
// @audit setParameters(address,uint256,uint256,uint256,uint256,uint256,uint256,uint256) ==> setParameters_lfW(address,uint256,uint256,uint256,uint256,uint256,uint256,uint256),00005c61
// @audit ratioSync() ==> ratioSync_h8a(),00004e63
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L25)

```solidity
File: /src/mimswap/auxiliary/FeeRateModel.sol

// @audit getFeeRate(address,uint256) ==> getFeeRate_T59(address,uint256),00006649
// @audit setMaintainer(address) ==> setMaintainer_YpH(address),0000d7d1
// @audit setImplementation(address) ==> setImplementation_j4P(address),00007fc5
13: contract FeeRateModel is Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModel.sol#L13)

```solidity
File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

// @audit getFeeRate(address,address,uint256) ==> getFeeRate_ccU(address,address,uint256),00003433
7: contract FeeRateModelImpl {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModelImpl.sol#L7)

```solidity
File: /src/mimswap/periphery/Factory.sol

// @audit getPoolCount(address,address) ==> getPoolCount_W6p(address,address),00005650
// @audit getUserPoolCount(address) ==> getUserPoolCount_775(address),000062ca
// @audit predictDeterministicAddress(address,address,address,uint256,uint256,uint256) ==> predictDeterministicAddress_17l(address,address,address,uint256,uint256,uint256),0000b4ae
// @audit create(address,address,uint256,uint256,uint256) ==> create_du(address,address,uint256,uint256,uint256),00009bc4
// @audit addPool(address,address,address,address) ==> addPool_Var(address,address,address,address),00001a67
// @audit removePool(address,address,address,uint256,uint256) ==> removePool_P5b(address,address,address,uint256,uint256),00005631
11: contract Factory is Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L11)

```solidity
File: /src/mimswap/periphery/Router.sol

// @audit createPool(address,address,uint256,uint256,uint256,address,uint256,uint256) ==> createPool_W2d(address,address,uint256,uint256,uint256,address,uint256,uint256),0000eb7c
// @audit createPoolETH(address,bool,uint256,uint256,uint256,address,uint256) ==> createPoolETH_7cB(address,bool,uint256,uint256,uint256,address,uint256),0000bd6f
// @audit previewCreatePool(uint256,uint256,uint256) ==> previewCreatePool_a1I(uint256,uint256,uint256),0000b618
// @audit previewAddLiquidity(address,uint256,uint256) ==> previewAddLiquidity_57h(address,uint256,uint256),0000baf7
// @audit addLiquidity(address,address,uint256,uint256,uint256,uint256) ==> addLiquidity_Rhl(address,address,uint256,uint256,uint256,uint256),00005988
// @audit addLiquidityUnsafe(address,address,uint256,uint256,uint256,uint256) ==> addLiquidityUnsafe_FkP(address,address,uint256,uint256,uint256,uint256),0000e18d
// @audit addLiquidityETHUnsafe(address,address,uint256,uint256,uint256) ==> addLiquidityETHUnsafe_a44(address,address,uint256,uint256,uint256),00008b75
// @audit previewRemoveLiquidity(address,uint256) ==> previewRemoveLiquidity_I8P(address,uint256),000097f9
// @audit removeLiquidity(address,address,uint256,uint256,uint256,uint256) ==> removeLiquidity_MkT(address,address,uint256,uint256,uint256,uint256),0000570f
// @audit removeLiquidityETH(address,address,uint256,uint256,uint256,uint256) ==> removeLiquidityETH_WCn(address,address,uint256,uint256,uint256,uint256),000039e6
// @audit swapTokensForTokens(address,uint256,address[],uint256,uint256,uint256) ==> swapTokensForTokens_r8L(address,uint256,address[],uint256,uint256,uint256),0000b0c7
// @audit swapETHForTokens(address,address[],uint256,uint256,uint256) ==> swapETHForTokens_d2E(address,address[],uint256,uint256,uint256),0000912f
// @audit swapTokensForETH(address,uint256,address[],uint256,uint256,uint256) ==> swapTokensForETH_ao3(address,uint256,address[],uint256,uint256,uint256),00008a4b
// @audit sellBaseTokensForTokens(address,address,uint256,uint256,uint256) ==> sellBaseTokensForTokens_Ra5(address,address,uint256,uint256,uint256),0000f559
// @audit sellBaseETHForTokens(address,address,uint256,uint256) ==> sellBaseETHForTokens_Yeq(address,address,uint256,uint256),0000e03d
// @audit sellBaseTokensForETH(address,address,uint256,uint256,uint256) ==> sellBaseTokensForETH_yxQ(address,address,uint256,uint256,uint256),0000a523
// @audit sellQuoteTokensForTokens(address,address,uint256,uint256,uint256) ==> sellQuoteTokensForTokens_BlF(address,address,uint256,uint256,uint256),0000897f
// @audit sellQuoteETHForTokens(address,address,uint256,uint256) ==> sellQuoteETHForTokens_n3H(address,address,uint256,uint256),0000bc49
// @audit sellQuoteTokensForETH(address,address,uint256,uint256,uint256) ==> sellQuoteTokensForETH_n3p(address,address,uint256,uint256,uint256),0000621d
12: contract Router {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L12)

```solidity
File: /src/staking/LockingMultiRewards.sol

// @audit stake(uint256,bool) ==> stake_Djg(uint256,bool),00009218
// @audit lock(uint256) ==> lock_UK8(uint256),00009065
// @audit withdraw(uint256) ==> withdraw_6BK(uint256),0000b293
// @audit withdrawWithRewards(uint256) ==> withdrawWithRewards_kc8(uint256),000027ce
// @audit getRewards() ==> getRewards_l54(),0000f498
// @audit rewardData(address) ==> rewardData_cl5(address),0000725f
// @audit rewardsForDuration(address) ==> rewardsForDuration_U6b(address),0000ed6e
// @audit rewardTokensLength() ==> rewardTokensLength_Vy9(),0000f4cc
// @audit balances(address) ==> balances_R1t(address),00006c5c
// @audit userRewardLock(address) ==> userRewardLock_u8r(address),00007281
// @audit userLocks(address) ==> userLocks_ilf(address),0000ed99
// @audit userLocksLength(address) ==> userLocksLength_mnQ(address),0000c00a
// @audit locked(address) ==> locked_r5q(address),00004ad7
// @audit unlocked(address) ==> unlocked_G3u(address),00006452
// @audit totalSupply() ==> totalSupply_B6A(),00005a30
// @audit balanceOf(address) ==> balanceOf_qzn(address),000030d8
// @audit nextUnlockTime() ==> nextUnlockTime_Z4T(),00004508
// @audit epoch() ==> epoch_z5q(),0000fd6c
// @audit nextEpoch() ==> nextEpoch_X6y(),0000c503
// @audit remainingEpochTime() ==> remainingEpochTime_5dw(),00006be3
// @audit lastTimeRewardApplicable(address) ==> lastTimeRewardApplicable_imK(address),00009f9e
// @audit rewardPerToken(address) ==> rewardPerToken_TfB(address),000049f2
// @audit _rewardPerToken(address,uint256,uint256) ==> _rewardPerToken_q4M(address,uint256,uint256),000053f5
// @audit earned(address,address) ==> earned_rrn(address,address),0000d854
// @audit addReward(address) ==> addReward_e2H(address),000072a1
// @audit setMinLockAmount(uint256) ==> setMinLockAmount_j9Z(uint256),0000898e
// @audit recover(address,uint256) ==> recover_0sI(address,uint256),00004f5a
// @audit pause() ==> pause_yiS(),00002a4b
// @audit unpause() ==> unpause_88B(),000051b7
// @audit stakeFor(address,uint256,bool) ==> stakeFor_Zwq(address,uint256,bool),0000f6b3
// @audit notifyRewardAmount(address,uint256,uint256) ==> notifyRewardAmount_q62(address,uint256,uint256),00009155
// @audit processExpiredLocks(address[],uint256[]) ==> processExpiredLocks_n4S(address[],uint256[]),00000df4
14: contract LockingMultiRewards is OperatableV2, Pausable {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L14)

</details>

### <a name="GAS-34-1693312684"></a>[GAS-34] Not using the named return variables anywhere in the function wast gas
Consider changing the variable to be an unnamed one, since the variable is never assigned, nor is it returned by name. If the optimizer is not turned on, leaving the code as it is will also waste gas for the stack variable.

*Instances (19)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboardingBoot.sol

// @audit shares
78:     function claimable(address user) external view returns (uint256 shares) {

// @audit baseAdjustedInAmount
// @audit quoteAdjustedInAmount
// @audit shares
86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

// @audit shares
155:     function _claimable(address user) internal view returns (uint256 shares) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L155)

```solidity
File: /src/blast/libraries/BlastYields.sol

// @audit amount
51:     function claimAllNativeYields(address recipient) internal returns (uint256 amount) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastYields.sol#L51)

```solidity
File: /src/mimswap/MagicLP.sol

// @audit midPrice
215:     function getMidPrice() public view returns (uint256 midPrice) {

// @audit lpFeeRate
// @audit mtFeeRate
224:     function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {

// @audit input
228:     function getBaseInput() public view returns (uint256 input) {

// @audit input
232:     function getQuoteInput() public view returns (uint256 input) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L232)

```solidity
File: /src/mimswap/auxiliary/FeeRateModel.sol

// @audit adjustedLpFeeRate
// @audit mtFeeRate
34:     function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModel.sol#L34)

```solidity
File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

// @audit adjustedLpFeeRate
9:     function getFeeRate(

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModelImpl.sol#L9)

```solidity
File: /src/mimswap/periphery/Router.sol

// @audit shares
178:     function addLiquidityUnsafe(

// @audit shares
229:     function addLiquidityETHUnsafe(

// @audit baseAmountOut
// @audit quoteAmountOut
261:     function removeLiquidity(

// @audit amountOut
314:     function swapTokensForTokens(

// @audit amountOut
336:     function swapETHForTokens(

// @audit amountOut
404:     function sellBaseTokensForTokens(

// @audit amountOut
415:     function sellBaseETHForTokens(

// @audit amountOut
449:     function sellQuoteTokensForTokens(

// @audit amountOut
461:     function sellQuoteETHForTokens(

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L461)

</details>

### <a name="GAS-35-1693312698"></a>[GAS-35] Enable Solidity's optimizer
Make sure Solidity's optimizer is enabled. It reduces gas costs. If you want to gas optimize for contract deployment (costs less to deploy a contract) then set the Solidity optimizer at a low number. If you want to optimize for run-time gas costs (when functions are called on a contract) then set the optimizer to a high number.
Set the optimization value higher than 800 in your hardhat.config.ts file.

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: hardhat.config.ts

//@audit c4/competitions/2024-03-abracadabra-money/lib/safe-contracts/hardhat.config.ts
1: 

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/hardhat.config.ts#L1)

</details>

### <a name="GAS-36-1694875070"></a>[GAS-36] State variables can be packed into fewer storage slots
If variables occupying the same slot are both written the same function or by the constructor, avoids a separate Gsset (**20000 gas**). Reads of the variables can also be cheaper

*Instances (2)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboardingBoot.sol

// @audit from 4 to 3 you need to change the structure elements order to: , uint256, mapping, address, bool, IFactory, LockingMultiRewards, Router
23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
        address public pool;
        Router public router;
        IFactory public factory;
        uint256 public totalPoolShares;
        bool public ready;
        LockingMultiRewards public staking;
        mapping(address user => bool claimed) public claimed;
    }

// @audit from 4 to 3 you need to change the structure elements order to: , uint256, mapping, address, bool, IFactory, LockingMultiRewards, Router
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
        using SafeTransferLib for address;
    
        event LogReadyChanged(bool ready);
        event LogClaimed(address indexed user, uint256 shares, bool lock);
        event LogInitialized(Router indexed router);
        event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);
        event LogStakingChanged(address indexed staking);
    
        error ErrInsufficientAmountOut();
        error ErrNotReady();
        error ErrAlreadyClaimed();
        error ErrWrongFeeRateModel();
        error ErrAlreadyBootstrapped();
        error ErrNothingToClaim();
        error ErrCannotChangeOnceReady();
    
        //////////////////////////////////////////////////////////////////////////////////////
        /// PUBLIC
        //////////////////////////////////////////////////////////////////////////////////////
    
        function claim(bool lock) external returns (uint256 shares) {
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
    
        //////////////////////////////////////////////////////////////////////////////////////
        /// VIEWS
        //////////////////////////////////////////////////////////////////////////////////////
    
        function claimable(address user) external view returns (uint256 shares) {
            if (!ready || claimed[user]) {
                return 0;
            }
    
            return _claimable(user);
        }
    
        function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
            uint256 baseAmount = totals[MIM].locked;
            uint256 quoteAmount = totals[USDB].locked;
            return router.previewCreatePool(I, baseAmount, quoteAmount);
        }
    
        //////////////////////////////////////////////////////////////////////////////////////
        /// ADMIN
        //////////////////////////////////////////////////////////////////////////////////////
    
        function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
            if (pool != address(0)) {
                revert ErrAlreadyBootstrapped();
            }
    
            uint256 baseAmount = totals[MIM].locked;
            uint256 quoteAmount = totals[USDB].locked;
            MIM.safeApprove(address(router), type(uint256).max);
            USDB.safeApprove(address(router), type(uint256).max);
    
            (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
    
            if (totalPoolShares < minAmountOut) {
                revert ErrInsufficientAmountOut();
            }
    
            // Create staking contract
            // 3x boosting for locker, 7 days reward duration, 13 weeks lp locking
            // make this contract temporary the owner the set it as an operator
            // for permissionned `stakeFor` during the claiming process and then
            // transfer the ownership to the onboarding owner.
            staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
            staking.setOperator(address(this), true);
            staking.transferOwnership(owner);
    
            // Approve staking contract
            pool.safeApprove(address(staking), totalPoolShares);
    
            emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);
    
            return (pool, address(staking), totalPoolShares);
        }
    
        function initialize(Router _router) external onlyOwner {
            router = Router(payable(_router));
            factory = IFactory(router.factory());
            emit LogInitialized(_router);
        }
    
        // Just in case we need to change the staking contract after
        // the automatic bootstrapping process
        function setStaking(LockingMultiRewards _staking) external onlyOwner {
            if (ready) {
                revert ErrCannotChangeOnceReady();
            }
    
            staking = _staking;
            emit LogStakingChanged(address(_staking));
        }
    
        function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
            ready = _ready;
            emit LogReadyChanged(ready);
        }
    
        //////////////////////////////////////////////////////////////////////////////////////
        /// INTERNALS
        //////////////////////////////////////////////////////////////////////////////////////
    
        function _claimable(address user) internal view returns (uint256 shares) {
            uint256 totalLocked = totals[MIM].locked + totals[USDB].locked;
    
            if (totalLocked == 0) {
                return 0;
            }
    
            uint256 userLocked = balances[user][MIM].locked + balances[user][USDB].locked;
            return (userLocked * totalPoolShares) / totalLocked;
        }
    }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L34-L165)

</details>

### <a name="GAS-37-1694793490"></a>[GAS-37] Structs can be packed into fewer storage slots by truncating timestamp bytes
By using a `uint32` or lower rather than a larger type for variables that track timestamps, one can save gas by using fewer storage slots per struct, at the expense of the protocol breaking after the year 2106 (when `uint32` wraps). If this is an acceptable tradeoff, each slot saved can avoid an extra Gsset (**20000 gas**) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit the following variables: periodFinish,  could be packed
50:     struct Reward {
            uint256 periodFinish;
            uint256 rewardRate;
            uint256 rewardPerTokenStored;
            bool exists;
            uint248 lastUpdateTime;
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L50-L56)

</details>

### <a name="GAS-38-1693312741"></a>[GAS-38] Constructors can be marked `payable`
Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn't provided.A constructor can safely be marked as payable, since only the deployer would be able to pass funds, and the project itself would not pass any funds.

*Instances (16)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
            if (feeTo_ == address(0)) {
                revert ErrZeroAddress();
            }
            if (address(registry_) == address(0)) {
                revert ErrZeroAddress();
            }
    
            registry = registry_;
            feeTo = feeTo_;
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L24-L34)

```solidity
File: /src/blast/BlastDapp.sol

7:     constructor() {
           BlastPoints.configure();
       }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastDapp.sol#L7-L9)

```solidity
File: /src/blast/BlastGovernor.sol

15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {
            if (feeTo_ == address(0)) {
                revert ErrZeroAddress();
            }
    
            feeTo = feeTo_;
            BlastYields.configureDefaultClaimables(address(this));
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastGovernor.sol#L15-L22)

```solidity
File: /src/blast/BlastMagicLP.sol

23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
            if (feeTo_ == address(0)) {
                revert ErrZeroAddress();
            }
            if (address(registry_) == address(0)) {
                revert ErrZeroAddress();
            }
    
            registry = registry_;
            feeTo = feeTo_;
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L23-L33)

```solidity
File: /src/blast/BlastOnboarding.sol

58:     constructor() Owned(msg.sender) {
            BlastYields.configureDefaultClaimables(address(this));
            BlastPoints.configure();
        }

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {
            if (address(registry_) == address(0)) {
                revert ErrZeroAddress();
            }
    
            if (feeTo_ == address(0)) {
                revert ErrZeroAddress();
            }
    
            registry = registry_;
            feeTo = feeTo_;
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L84-L95)

```solidity
File: /src/blast/BlastTokenRegistry.sol

12:     constructor(address _owner) Owned(_owner) {}

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastTokenRegistry.sol#L12-L12)

```solidity
File: /src/blast/BlastWrappers.sol

20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
            if (governor_ == address(0)) {
                revert ErrZeroAddress();
            }
            BlastYields.configureDefaultClaimables(governor_);
        }

29:     constructor(
            address implementation_,
            IFeeRateModel maintainerFeeRateModel_,
            address owner_,
            address governor_
        ) Factory(implementation_, maintainerFeeRateModel_, owner_) {
            if (governor_ == address(0)) {
                revert ErrZeroAddress();
            }
            BlastYields.configureDefaultClaimables(governor_);
        }

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
            if (governor_ == address(0)) {
                revert ErrZeroAddress();
            }
            if (governor_ == address(this)) {
                revert ErrInvalidGovernorAddress();
            }
    
            _governor = governor_;
            _setupBlacklist();
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastWrappers.sol#L47-L57)

```solidity
File: /src/mimswap/MagicLP.sol

84:     constructor(address owner_) Owned(owner_) {
            implementation = this;
    
            // prevents the implementation contract initialization
            _INITIALIZED_ = true;
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L84-L89)

```solidity
File: /src/mimswap/auxiliary/FeeRateModel.sol

22:     constructor(address maintainer_, address owner_) Owned(owner_) {
            if (maintainer_ == address(0)) {
                revert ErrZeroAddress();
            }
    
            maintainer = maintainer_;
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModel.sol#L22-L28)

```solidity
File: /src/mimswap/periphery/Factory.sol

38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
            if (implementation_ == address(0)) {
                revert ErrZeroAddress();
            }
            if (address(maintainerFeeRateModel_) == address(0)) {
                revert ErrZeroAddress();
            }
            implementation = implementation_;
            maintainerFeeRateModel = maintainerFeeRateModel_;
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L38-L47)

```solidity
File: /src/mimswap/periphery/Router.sol

38:     constructor(IWETH weth_, IFactory factory_) {
            if (address(weth_) == address(0) || address(factory_) == address(0)) {
                revert ErrZeroAddress();
            }
    
            weth = weth_;
            factory = factory_;
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L38-L45)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
            pair = pair_;
            baseOracle = baseOracle_;
            quoteOracle = quoteOracle_;
            baseDecimals = IERC20Metadata(pair_._BASE_TOKEN_()).decimals();
            quoteDecimals = IERC20Metadata(pair_._QUOTE_TOKEN_()).decimals();
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L21-L27)

```solidity
File: /src/staking/LockingMultiRewards.sol

112:     constructor(
             address _stakingToken,
             uint256 _lockingBoostMultiplerInBips,
             uint256 _rewardsDuration,
             uint256 _lockDuration,
             address _owner
         ) OperatableV2(_owner) {
             if (_lockingBoostMultiplerInBips <= BIPS) {
                 revert ErrInvalidBoostMultiplier();
             }
     
             if (_lockDuration < MIN_LOCK_DURATION) {
                 revert ErrInvalidLockDuration();
             }
     
             if (_rewardsDuration < MIN_REWARDS_DURATION) {
                 revert ErrInvalidRewardDuration();
             }
     
             if (_lockDuration % _rewardsDuration != 0) {
                 revert ErrInvalidDurationRatio();
             }
     
             stakingToken = _stakingToken;
             lockingBoostMultiplerInBips = _lockingBoostMultiplerInBips;
             rewardsDuration = _rewardsDuration;
             lockDuration = _lockDuration;
     
             // kocks are combined into the same `rewardsDuration` epoch. So, if
             // a user stake with locking every `rewardsDuration` this should reach the
             // maximum number of possible simultaneous because the first lock gets expired,
             // freeing up a slot.
             maxLocks = _lockDuration / _rewardsDuration;
         }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L112-L145)

</details>

### <a name="GAS-39-1699444393"></a>[GAS-39] Initializer can be marked `payable`
Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn't provided.An Initializer can safely be marked as payable, since only the allowed user would be able to pass funds, and the project itself would not pass any funds.

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboardingBoot.sol

129:     function initialize(Router _router) external onlyOwner {
             router = Router(payable(_router));

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L129-L130)

</details>

### <a name="GAS-40-1693316170"></a>[GAS-40] `++i` costs less gas than `i++`, especially when it's used in `for`-loops (`--i`/`i--` too)
*Saves 5 gas per loop*

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

165:         for (uint256 i = 0; i < tokens.length; i++) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L165)

</details>

### <a name="GAS-41-1696084477"></a>[GAS-41] `++i`/`i++` should be `unchecked{++i}`/`unchecked{i++}` when it is not possible for them to overflow, as is the case when used in `for`- and `while`-loops
The `unchecked` keyword is new in solidity version 0.8.0, so this only applies to that version or higher, which these instances are. This saves **30-40 gas [per loop](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#the-increment-in-for-loop-post-condition-can-be-made-unchecked)**

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

165:         for (uint256 i = 0; i < tokens.length; i++) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L165)

</details>

### <a name="GAS-42-1709377106"></a>[GAS-42] Consider pre-calculating the address of `address(this)` to save gas
Use `foundry`'s [`script.sol`](https://book.getfoundry.sh/reference/forge-std/compute-create-address) or `solady`'s [`LibRlp.sol`](https://github.com/Vectorized/solady/blob/main/src/utils/LibRLP.sol) to save the value in a constant, which will avoid having to spend gas to push the value on the stack every time it's used.

*Instances (49)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

99:         BlastYields.configureDefaultClaimables(address(this));

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L99-L99)

```solidity
File: /src/blast/BlastGovernor.sol

21:         BlastYields.configureDefaultClaimables(address(this));

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastGovernor.sol#L21-L21)

```solidity
File: /src/blast/BlastMagicLP.sol

99:         BlastYields.configureDefaultClaimables(address(this));

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L99-L99)

```solidity
File: /src/blast/BlastOnboarding.sol

59:         BlastYields.configureDefaultClaimables(address(this));

102:         token.safeTransferFrom(msg.sender, address(this), amount);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L102-L102)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

106:         (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

117:         staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));

118:         staking.setOperator(address(this), true);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L118-L118)

```solidity
File: /src/blast/BlastWrappers.sol

51:         if (governor_ == address(this)) {

60:         if (_governor == address(this)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastWrappers.sol#L60-L60)

```solidity
File: /src/blast/libraries/BlastYields.sol

21:         if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {

26:         emit LogBlastTokenClaimableEnabled(address(this), token);

31:         emit LogBlastNativeClaimableEnabled(address(this));

39:         return claimMaxGasYields(address(this), recipient);

52:         return claimAllNativeYields(address(this), recipient);

71:         amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastYields.sol#L71-L71)

```solidity
File: /src/mimswap/MagicLP.sol

229:         return _BASE_TOKEN_.balanceOf(address(this)) - uint256(_BASE_RESERVE_);

233:         return _QUOTE_TOKEN_.balanceOf(address(this)) - uint256(_QUOTE_RESERVE_);

245:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

262:         _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));

268:         uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

285:         _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);

298:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

299:         uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

361:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

362:         uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

427:         if (to == address(this)) {

431:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

432:         uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

505:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

506:         uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

529:         baseBalance = _BASE_TOKEN_.balanceOf(address(this));

530:         quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

568:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

569:         uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

615:         if (address(this) == address(implementation)) {

622:         if (address(this) != address(implementation)) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L622-L622)

```solidity
File: /src/mimswap/periphery/Factory.sol

77:                 address(this)

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L77-L77)

```solidity
File: /src/mimswap/periphery/Router.sol

92:         address(weth).safeTransferFrom(address(this), clone, msg.value);

269:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

282:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

289:                 address(this),

298:                 address(this),

398:         amountOut = _swap(address(this), path, directions, minimumOut);

444:         amountOut = _sellBase(lp, address(this), minimumOut);

490:         amountOut = _sellQuote(lp, address(this), minimumOut);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L490-L490)

```solidity
File: /src/staking/LockingMultiRewards.sol

326:         if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

367:         rewardToken.safeTransferFrom(msg.sender, address(this), amount);

464:         stakingToken.safeTransferFrom(msg.sender, address(this), amount);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L464-L464)

</details>

### <a name="GAS-43-1693312824"></a>[GAS-43] Using `private` rather than `public` for constants, saves gas
If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that [returns a tuple](https://github.com/code-423n4/2022-08-frax/blob/90f55a9ce4e25bceed3a74290b854341d8de6afa/src/contracts/FraxlendPair.sol#L156-L178) of the values of all currently-public constants. Saves **3406-3606 gas** in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table

*Instances (8)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/libraries/BlastPoints.sol

7:     address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;

8:     IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastPoints.sol#L8)

```solidity
File: /src/mimswap/MagicLP.sol

63:     uint256 public constant MAX_I = 10 ** 36;

64:     uint256 public constant MAX_K = 10 ** 18;

65:     uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%

66:     uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L66)

```solidity
File: /src/mimswap/periphery/Router.sol

31:     uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L31)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

16:     uint256 public constant WAD = 18;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L16)

</details>

### <a name="GAS-44-1709385583"></a>[GAS-44] Reduce deployment costs by tweaking contracts' metadata
See [this](https://www.rareskills.io/post/solidity-metadata) link, at its bottom, for full details

*Instances (24)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L13)

```solidity
File: /src/blast/BlastDapp.sol

6: contract BlastDapp {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastDapp.sol#L6)

```solidity
File: /src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastGovernor.sol#L7)

```solidity
File: /src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L10)

```solidity
File: /src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L64)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L34)

```solidity
File: /src/blast/BlastTokenRegistry.sol

6: contract BlastTokenRegistry is Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastTokenRegistry.sol#L6)

```solidity
File: /src/blast/BlastWrappers.sol

19: contract BlastMIMSwapRouter is Router {

28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastWrappers.sol#L42)

```solidity
File: /src/blast/libraries/BlastPoints.sol

6: library BlastPoints {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastPoints.sol#L6)

```solidity
File: /src/blast/libraries/BlastYields.sol

7: library BlastYields {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastYields.sol#L7)

```solidity
File: /src/mimswap/MagicLP.sol

25: contract MagicLP is ERC20, ReentrancyGuard, Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L25)

```solidity
File: /src/mimswap/auxiliary/FeeRateModel.sol

13: contract FeeRateModel is Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModel.sol#L13)

```solidity
File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

7: contract FeeRateModelImpl {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModelImpl.sol#L7)

```solidity
File: /src/mimswap/libraries/DecimalMath.sol

17: library DecimalMath {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/DecimalMath.sol#L17)

```solidity
File: /src/mimswap/libraries/Math.sol

16: library Math {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L16)

```solidity
File: /src/mimswap/libraries/PMMPricing.sol

20: library PMMPricing {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/PMMPricing.sol#L20)

```solidity
File: /src/mimswap/periphery/Factory.sol

11: contract Factory is Owned {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L11)

```solidity
File: /src/mimswap/periphery/Router.sol

12: contract Router {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L12)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

9: contract MagicLpAggregator is IAggregator {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L9)

```solidity
File: /src/staking/LockingMultiRewards.sol

14: contract LockingMultiRewards is OperatableV2, Pausable {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L14)

</details>

### <a name="GAS-45-1693312940"></a>[GAS-45] Redundant else statement

*Instances (4)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/libraries/DecimalMath.sol

50:         } else if (e == 1) {
                return target;
            } else {
                uint p = powFloor(target, e / 2);
                p = (p * p) / ONE;
                if (e % 2 == 1) {
                    p = (p * target) / ONE;
                }
                return p;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/DecimalMath.sol#L50-L58)

```solidity
File: /src/mimswap/libraries/Math.sol

22:         if (remainder > 0) {
                return quotient + 1;
            } else {
                return quotient;

200:         if (V2 > V1) {
                 return 0;
             } else {
                 return V1 - V2;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L200-L203)

```solidity
File: /src/mimswap/libraries/PMMPricing.sol

204:         if (state.R == RState.BELOW_ONE) {
                 uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);
                 R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);
                 return DecimalMath.divFloor(state.i, R);
             } else {
                 uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
                 R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);
                 return DecimalMath.mulFloor(state.i, R);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/PMMPricing.sol#L204-L211)

</details>

### <a name="GAS-46-1693312958"></a>[GAS-46] Functions guaranteed to revert when called by normal users can be marked `payable`
If a function modifier such as `onlyOwner` is used, the function will revert if a normal user tries to pay the function. Marking the function as `payable` will lower the gas cost for legitimate callers because the compiler will not include checks for whether a payment was provided.The extra opcodes avoided are `CALLVALUE`(2), `DUP1`(3), `ISZERO`(3), `PUSH2`(3), `JUMPI`(10), `PUSH1`(3), `DUP1`(3), `REVERT`(0), `JUMPDEST`(1), `POP`(2), which costs an average of about ** 21 gas per call ** to the function, in addition to the extra deployment cost

*Instances (66)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

52:     function claimGasYields() external onlyOperators returns (uint256) {

56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

68:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

72:     function setFeeTo(address feeTo_) external onlyOwner {

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L81)

```solidity
File: /src/blast/BlastGovernor.sol

28:     function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

40:     function setFeeTo(address _feeTo) external onlyOwner {

49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastGovernor.sol#L53)

```solidity
File: /src/blast/BlastMagicLP.sol

47:     function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {

47:     function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {

53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {

53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

72:     function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {

72:     function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {

80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {

80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L89)

```solidity
File: /src/blast/BlastOnboarding.sol

101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {

147:     function setFeeTo(address feeTo_) external onlyOwner {

156:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

160:     function claimGasYields() external onlyOwner returns (uint256) {

164:     function claimTokenYields(address[] memory tokens) external onlyOwner {

175:     function setTokenSupported(address token, bool supported) external onlyOwner {

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {

195:     function open() external onlyOwner onlyState(State.Idle) {

195:     function open() external onlyOwner onlyState(State.Idle) {

200:     function close() external onlyOwner onlyState(State.Opened) {

200:     function close() external onlyOwner onlyState(State.Opened) {

205:     function rescue(address token, address to, uint256 amount) external onlyOwner {

214:     function pause() external onlyOwner {

218:     function unpause() external onlyOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L218)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {

96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {

129:     function initialize(Router _router) external onlyOwner {

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L146)

```solidity
File: /src/blast/BlastTokenRegistry.sol

14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastTokenRegistry.sol#L14)

```solidity
File: /src/mimswap/MagicLP.sol

461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {

470:     function setParameters(
             address assetTo,
             uint256 newLpFeeRate,
             uint256 newI,
             uint256 newK,
             uint256 baseOutAmount,
             uint256 quoteOutAmount,
             uint256 minBaseReserve,
             uint256 minQuoteReserve
         ) public nonReentrant onlyImplementationOwner {

504:     function ratioSync() external nonReentrant onlyImplementationOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L504)

```solidity
File: /src/mimswap/auxiliary/FeeRateModel.sol

46:     function setMaintainer(address maintainer_) external onlyOwner {

57:     function setImplementation(address implementation_) public onlyOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModel.sol#L57)

```solidity
File: /src/mimswap/periphery/Factory.sol

96:     function setLpImplementation(address implementation_) external onlyOwner {

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

116:     function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {

120:     function removePool(
             address creator,
             address baseToken,
             address quoteToken,
             uint256 poolIndex,
             uint256 userPoolIndex
         ) external onlyOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L120-L126)

```solidity
File: /src/staking/LockingMultiRewards.sol

300:     function addReward(address rewardToken) public onlyOwner {

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

324:     function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {

337:     function pause() external onlyOwner {

341:     function unpause() external onlyOwner {

349:     function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {

361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {

397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L397)

</details>

### <a name="GAS-47-1693312972"></a>[GAS-47] Avoid updating storage when the value hasn't changed to save gas
If the old value is equal to the new value, not re-storing the value will avoid a Gsreset (**2900 gas**), potentially at the expense of a Gcoldsload (**2100 gas**) or a Gwarmaccess (**100 gas**)

*Instances (12)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L81)

```solidity
File: /src/blast/BlastMagicLP.sol

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L89)

```solidity
File: /src/blast/BlastOnboarding.sol

175:     function setTokenSupported(address token, bool supported) external onlyOwner {

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L190)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L146)

```solidity
File: /src/mimswap/auxiliary/FeeRateModel.sol

57:     function setImplementation(address implementation_) public onlyOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/auxiliary/FeeRateModel.sol#L57)

```solidity
File: /src/mimswap/periphery/Router.sol

404:     function sellBaseTokensForTokens(

432:     function sellBaseTokensForETH(

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L432)

```solidity
File: /src/staking/LockingMultiRewards.sol

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L317)

</details>

### <a name="GAS-48-1693312984"></a>[GAS-48] Use shift Right instead of division if possible to save gas

*Instances (3)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/libraries/DecimalMath.sol

53:             uint p = powFloor(target, e / 2);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/DecimalMath.sol#L53)

```solidity
File: /src/mimswap/libraries/Math.sol

30:         uint256 z = x / 2 + 1;

34:             z = (x / z + z) / 2;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L34)

</details>

### <a name="GAS-49-1693312999"></a>[GAS-49] Use shift Left instead of multiplication if possible to save gas

*Instances (6)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/MagicLP.sol

125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

546:         uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L546)

```solidity
File: /src/mimswap/libraries/Math.sol

93:         uint256 ki = (4 * k) * i;

101:         uint256 premium = DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2) + DecimalMath.ONE;

184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2

188:         uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L188)

</details>

### <a name="GAS-50-1693313015"></a>[GAS-50] Usage of `uints`/`ints` smaller than 32 bytes (256 bits) incurs overhead
> When using elements that are smaller than 32 bytes, your contract's gas usage may be higher. This is because the EVM operates on 32 bytes at a time. Therefore, if the element is smaller than that, the EVM must use more operations in order to reduce the size of the element from 32 bytes to the desired size.
https://docs.soliditylang.org/en/v0.8.11/internals/layout_in_storage.html
Each operation involving a `uint8` costs an extra [** 22 - 28 gas **](https://gist.github.com/IllIllI000/9388d20c70f9a4632eb3ca7836f54977) (depending on whether the other operand is also a variable of type `uint8`) as compared to ones involving `uint256`, due to the compiler having to clear the higher bits of the memory word before operating on the `uint8`, as well as the associated stack operations of doing so. Use a larger size then downcast where needed

*Instances (8)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/MagicLP.sol

//@audit `` is `uint8`
163:     function decimals() public view override returns (uint8) {

//@audit `blockTimestamp` is `uint32`
546:         uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);

//@audit `timeElapsed` is `uint32`
547:         uint32 timeElapsed = blockTimestamp - _BLOCK_TIMESTAMP_LAST_;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L547)

```solidity
File: /src/mimswap/periphery/Router.sol

//@audit `baseDecimals` is `uint8`
598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {

//@audit `quoteDecimals` is `uint8`
598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L598)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

//@audit `` is `uint8`
29:     function decimals() external pure override returns (uint8) {

//@audit `` is `uint80`
48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {

//@audit `` is `uint80`
48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L48)

</details>

### <a name="GAS-51-1693313026"></a>[GAS-51] The use of a logical AND in place of double if is slightly less gas efficient in instances where there isn't a corresponding else statement for the given if statement
Using a double if statement instead of logical AND (&&) can provide similar short-circuiting behavior whereas double if is slightly more efficient.

*Instances (11)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastMagicLP.sol

119:         if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
                 revert ErrNotAllowedImplementationOperator();
             }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L119-L121)

```solidity
File: /src/blast/BlastOnboarding.sol

114:         if (caps[token] > 0 && totals[token].total > caps[token]) {
                 revert ErrCapReached();
             }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L114-L116)

```solidity
File: /src/mimswap/MagicLP.sol

139:         if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
                 _RState_ = uint32(PMMPricing.RState.ONE);
                 _BASE_TARGET_ = _BASE_RESERVE_;
                 _QUOTE_TARGET_ = _QUOTE_RESERVE_;
             }

144:         if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
                 _RState_ = uint32(PMMPricing.RState.ONE);
                 _BASE_TARGET_ = _BASE_RESERVE_;
                 _QUOTE_TARGET_ = _QUOTE_RESERVE_;
             }

302:         if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
                 revert ErrFlashLoanFailed();
             }

395:         } else if (baseReserve > 0 && quoteReserve > 0) {
                 // case 2. normal case
                 uint256 baseInputRatio = DecimalMath.divFloor(baseInput, baseReserve);
                 uint256 quoteInputRatio = DecimalMath.divFloor(quoteInput, quoteReserve);
                 uint256 mintRatio = quoteInputRatio < baseInputRatio ? quoteInputRatio : baseInputRatio;
                 shares = DecimalMath.mulFloor(totalSupply(), mintRatio);
     
                 _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();
                 _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
             }

549:         if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
                 /// @dev It is desired and expected for this value to
                 /// overflow once it has hit the max of `type.uint256`.
                 unchecked {
                     _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
                 }
             }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L549-L555)

```solidity
File: /src/mimswap/periphery/Router.sol

147:         } else if (baseReserve > 0 && quoteReserve > 0) {
                 uint256 baseInputRatio = DecimalMath.divFloor(baseInAmount, baseReserve);
                 uint256 quoteInputRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);
                 if (baseInputRatio <= quoteInputRatio) {
                     baseAdjustedInAmount = baseInAmount;
                     quoteAdjustedInAmount = DecimalMath.mulCeil(quoteReserve, baseInputRatio);
                     shares = DecimalMath.mulFloor(totalSupply, baseInputRatio);
                 } else {
                     quoteAdjustedInAmount = quoteInAmount;
                     baseAdjustedInAmount = DecimalMath.mulCeil(baseReserve, quoteInputRatio);
                     shares = DecimalMath.mulFloor(totalSupply, quoteInputRatio);
                 }
             }

527:             if (quoteReserve > 0 && baseReserve > 0) {
                     uint256 baseIncreaseRatio = DecimalMath.divFloor(baseInAmount, baseReserve);
                     uint256 quoteIncreaseRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);
                     if (baseIncreaseRatio <= quoteIncreaseRatio) {
                         baseAdjustedInAmount = baseInAmount;
                         quoteAdjustedInAmount = DecimalMath.mulFloor(quoteReserve, baseIncreaseRatio);
                     } else {
                         quoteAdjustedInAmount = quoteInAmount;
                         baseAdjustedInAmount = DecimalMath.mulFloor(baseReserve, quoteIncreaseRatio);
                     }
                 }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L527-L537)

```solidity
File: /src/staking/LockingMultiRewards.sol

326:         if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {
                 revert ErrSkimmingTooMuch();
             }

417:             if (index == lastLockIndex[user] && locks.length > 1) {
                     revert ErrInvalidLockIndex();
                 }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L417-L419)

</details>

### <a name="GAS-52-1709389408"></a>[GAS-52] Split `revert` checks to save gas
Splitting the conditions into two separate checks [saves](https://gist.github.com/IllIllI000/7e25b0fca6bd9d57d9b9bcb9d2018959) **2 gas**

*Instances (12)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/MagicLP.sol

102:         if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
                 revert ErrZeroAddress();
             }

108:         if (i == 0 || i > MAX_I) {
                 revert ErrInvalidI();
             }

114:         if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {
                 revert ErrInvalidLPFeeRate();
             }

441:         if (baseAmount < baseMinAmount || quoteAmount < quoteMinAmount) {
                 revert ErrWithdrawNotEnough();
             }

462:         if (token == _BASE_TOKEN_ || token == _QUOTE_TOKEN_) {
                 revert ErrNotAllowed();
             }

480:         if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
                 revert ErrReserveAmountNotEnough();
             }

483:         if (newI == 0 || newI > MAX_I) {
                 revert ErrInvalidI();
             }

489:         if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {
                 revert ErrInvalidLPFeeRate();
             }

508:         if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
                 revert ErrOverflow();
             }

532:         if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
                 revert ErrOverflow();
             }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L532-L534)

```solidity
File: /src/mimswap/periphery/Router.sol

39:         if (address(weth_) == address(0) || address(factory_) == address(0)) {
                revert ErrZeroAddress();
            }

599:         if (baseDecimals == 0 || quoteDecimals == 0) {
                 revert ErrZeroDecimals();
             }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L599-L601)

</details>

### <a name="GAS-53-1693313099"></a>[GAS-53] Cache state variables outside of loop to avoid reading storage on every iteration
Reading from storage should always try to be avoided within loops.In the following instances, we are able to cache state variables outside of the loop to save a Gwarmaccess(100 gas) per loop iteration.

Note: Due to stack too deep errors, we will not be able to cache all the state variables read within the loops.

*Instances (3)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

//@audit `feeTo` is a state variable, try to cache it outside the loop
170:                 BlastYields.claimAllTokenYields(tokens[i], feeTo);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L170)

```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit `unlockedSupply` is a state variable, try to cache it outside the loop
441:             unlockedSupply += amount;

//@audit `lockedSupply` is a state variable, try to cache it outside the loop
442:             lockedSupply -= amount;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L442)

</details>

### <a name="GAS-54-1693311457"></a>[GAS-54] State variable read in a loop
The state variable should be cached in a local variable rather than reading it on every iteration of the for-loop, which will replace each Gwarmaccess (**100 gas**) with a much cheaper stack read.

*Instances (4)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

//@audit `registry` is read in this loop
165:         for (uint256 i = 0; i < tokens.length; i++) {
                 if (!supportedTokens[tokens[i]]) {
                     revert ErrUnsupportedToken();
                 }
                 if (registry.nativeYieldTokens(tokens[i])) {

//@audit `feeTo` is read in this loop
165:         for (uint256 i = 0; i < tokens.length; i++) {
                 if (!supportedTokens[tokens[i]]) {
                     revert ErrUnsupportedToken();
                 }
                 if (registry.nativeYieldTokens(tokens[i])) {
                     BlastYields.claimAllTokenYields(tokens[i], feeTo);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L165-L170)

```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit `unlockedSupply` is read in this loop
405:         for (uint256 i; i < users.length; ) {
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

//@audit `lockedSupply` is read in this loop
405:         for (uint256 i; i < users.length; ) {
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

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L405-L442)

</details>

### <a name="GAS-55-1693313054"></a>[GAS-55] State variables only set in the constructor should be declared `immutable`
Avoids a Gsset(** 20000 gas**) in the constructor, and replaces the first access in each transaction(Gcoldsload - ** 2100 gas **) and each access thereafter(Gwarmacces - ** 100 gas **) with a`PUSH32`(** 3 gas **).

While`string`s are not value types, and therefore cannot be`immutable` / `constant` if not hard - coded outside of the constructor, the same behavior can be achieved by making the current contract `abstract` with `virtual` functions for the`string` accessors, and having a child contract override the functions with the hard - coded implementation - specific values.

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

32:         registry = registry_;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L32)

</details>

### <a name="GAS-56-1693313071"></a>[GAS-56] Stack variable used as a cheaper cache for a state variable is only used once
If the variable is only accessed once, it's cheaper to use the state variable directly that one time, and save the **3 gas** the extra stack assignment would spend. However, if it used as a parameter in an event emit, then caching it will help reduce gas by at least ***10 gas***

*Instances (35)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastMagicLP.sol

/// @audit `feeTo_`,  are used only once
48:         address feeTo_ = BlastMagicLP(address(implementation)).feeTo();

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L48-L48)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

/// @audit `baseAmount`,  are used only once
87:         uint256 baseAmount = totals[MIM].locked;

/// @audit `quoteAmount`,  are used only once
88:         uint256 quoteAmount = totals[USDB].locked;

/// @audit `baseAmount`,  are used only once
101:         uint256 baseAmount = totals[MIM].locked;

/// @audit `quoteAmount`,  are used only once
102:         uint256 quoteAmount = totals[USDB].locked;

/// @audit `userLocked`,  are used only once
162:         uint256 userLocked = balances[user][MIM].locked + balances[user][USDB].locked;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L162-L162)

```solidity
File: /src/mimswap/MagicLP.sol

/// @audit `lpFeeRate`, `mtFeeRate`,  are used only once
174:         (uint256 lpFeeRate, uint256 mtFeeRate) = _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_);

/// @audit `lpFeeRate`, `mtFeeRate`,  are used only once
187:         (uint256 lpFeeRate, uint256 mtFeeRate) = _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_);

/// @audit `newQuoteTarget`,  are used only once
310:             (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) = querySellQuote(
                     tx.origin,
                     quoteInput
                 );

/// @audit `newBaseTarget`,  are used only once
332:             (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) = querySellBase(
                     tx.origin,
                     baseInput
                 );

/// @audit `baseBalance`,  are used only once
431:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

/// @audit `quoteBalance`,  are used only once
432:         uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

/// @audit `newBaseBalance`, `newQuoteBalance`,  are used only once
499:         (uint256 newBaseBalance, uint256 newQuoteBalance) = _resetTargetAndReserve();

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L499-L499)

```solidity
File: /src/mimswap/libraries/Math.sol

/// @audit `remainder`,  are used only once
21:         uint256 remainder = a - quotient * b;

/// @audit `V0V0V1V2`,  are used only once
62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

/// @audit `penalty`,  are used only once
63:         uint256 penalty = DecimalMath.mulFloor(k, V0V0V1V2); // k(V0^2/V1/V2)

/// @audit `premium`,  are used only once
101:         uint256 premium = DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2) + DecimalMath.ONE;

/// @audit `denominator`,  are used only once
188:         uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L188-L188)

```solidity
File: /src/mimswap/periphery/Factory.sol

/// @audit `salt`,  are used only once
84:         bytes32 salt = _computeSalt(creator, baseToken_, quoteToken_, lpFeeRate_, i_, k_);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L84-L84)

```solidity
File: /src/mimswap/periphery/Router.sol

/// @audit `baseBalance`,  are used only once
252:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp));

/// @audit `quoteBalance`,  are used only once
253:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp));

/// @audit `baseBalance`,  are used only once
515:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;

/// @audit `quoteBalance`,  are used only once
516:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L516-L516)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

/// @audit `baseReserve`, `quoteReserve`,  are used only once
34:         (uint256 baseReserve, uint256 quoteReserve) = pair.getReserves();

/// @audit `minAnswer`,  are used only once
40:         uint256 minAnswer = baseAnswerNomalized < quoteAnswerNormalized ? baseAnswerNomalized : quoteAnswerNormalized;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L40-L40)

```solidity
File: /src/staking/LockingMultiRewards.sol

/// @audit `timeElapsed`,  are used only once
282:         uint256 timeElapsed = lastTimeRewardApplicable_ - _rewardData[rewardToken].lastUpdateTime;

/// @audit `pendingRewardsPerToken`,  are used only once
283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

/// @audit `pendingUserRewardsPerToken`,  are used only once
293:         uint256 pendingUserRewardsPerToken = rewardPerToken_ - userRewardPerTokenPaid[user][rewardToken];

/// @audit `bal`,  are used only once
480:         Balances storage bal = _balances[user];

/// @audit `totalSupply_`,  are used only once
545:         uint256 totalSupply_ = totalSupply();

/// @audit `balance`,  are used only once
558:         uint256 balance = balanceOf(user);

/// @audit `totalSupply_`,  are used only once
559:         uint256 totalSupply_ = totalSupply();

/// @audit `totalSupply_`,  are used only once
573:         uint256 totalSupply_ = totalSupply();

/// @audit `rewardPerToken_`,  are used only once
577:             uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);

/// @audit `rewardItemLength`,  are used only once
605:         uint256 rewardItemLength = _rewardLock.items.length;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L605-L605)

</details>

### <a name="GAS-57-1708099671"></a>[GAS-57] State variable written in a loop
The code should be refactored such that updates made to the state variable are instead accumulated/tracked in a local variable, then be written a single time outside the loop, converting a Gsreset (`2900 gas`) to a stack write for each iteration

*Instances (2)*:
<details><summary> see instances </summary>

```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit `unlockedSupply` is a state variable written in loop
405:         for (uint256 i; i < users.length; ) {
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

//@audit `lockedSupply` is a state variable written in loop
405:         for (uint256 i; i < users.length; ) {
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
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L405-L452)

</details>

### <a name="GAS-58-1693313130"></a>[GAS-58] `>=`/`<=` costs less gas than `>`/`<`
The compiler uses opcodes `GT` and `ISZERO` for solidity code that uses `>`, but only requires `LT` for `>=`, [which saves **3 gas**](https://gist.github.com/IllIllI000/3dc79d25acccfa16dee4e83ffdc6ffde)

*Instances (74)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

114:         if (caps[token] > 0 && totals[token].total > caps[token]) {

114:         if (caps[token] > 0 && totals[token].total > caps[token]) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L114)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

108:         if (totalPoolShares < minAmountOut) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L108)

```solidity
File: /src/mimswap/MagicLP.sol

108:         if (i == 0 || i > MAX_I) {

111:         if (k > MAX_K) {

114:         if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {

114:         if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {

139:         if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {

144:         if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

294:         if (data.length > 0) {

302:         if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {

302:         if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {

308:         if (baseBalance < _BASE_RESERVE_) {

315:             if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {

330:         if (quoteBalance < _QUOTE_RESERVE_) {

337:             if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {

381:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;

395:         } else if (baseReserve > 0 && quoteReserve > 0) {

395:         } else if (baseReserve > 0 && quoteReserve > 0) {

399:             uint256 mintRatio = quoteInputRatio < baseInputRatio ? quoteInputRatio : baseInputRatio;

421:         if (deadline < block.timestamp) {

424:         if (shareAmount > balanceOf(msg.sender)) {

441:         if (baseAmount < baseMinAmount || quoteAmount < quoteMinAmount) {

441:         if (baseAmount < baseMinAmount || quoteAmount < quoteMinAmount) {

450:         if (data.length > 0) {

480:         if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {

480:         if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {

483:         if (newI == 0 || newI > MAX_I) {

486:         if (newK > MAX_K) {

489:         if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {

489:         if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {

508:         if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {

508:         if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {

532:         if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {

532:         if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {

549:         if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {

582:         if (amount > 0) {

588:         if (amount > 0) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L588)

```solidity
File: /src/mimswap/libraries/Math.sol

22:         if (remainder > 0) {

32:         while (z < y) {

141:             return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);

200:         if (V2 > V1) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L200)

```solidity
File: /src/mimswap/libraries/PMMPricing.sol

50:             if (payBaseAmount < backToOnePayBase) {

54:                 if (receiveQuoteAmount > backToOneReceiveQuote) {

86:             if (payQuoteAmount < backToOnePayQuote) {

89:                 if (receiveBaseAmount > backToOneReceiveBase) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/PMMPricing.sol#L89)

```solidity
File: /src/mimswap/periphery/Router.sol

48:         if (block.timestamp > deadline) {

101:         shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

138:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;

147:         } else if (baseReserve > 0 && quoteReserve > 0) {

147:         } else if (baseReserve > 0 && quoteReserve > 0) {

220:         if (msg.value > wethAdjustedAmount) {

502:         if (shares < minimumShares) {

523:             uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

527:             if (quoteReserve > 0 && baseReserve > 0) {

527:             if (quoteReserve > 0 && baseReserve > 0) {

566:         if (amountOut < minimumOut) {

573:         if (amountOut < minimumOut) {

581:         if (amountOut < minimumOut) {

590:         if (pathLength > 256) {

602:         if (quoteDecimals - baseDecimals > MAX_BASE_QUOTE_DECIMALS_DIFFERENCE) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L602)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

40:         uint256 minAnswer = baseAnswerNomalized < quoteAnswerNormalized ? baseAnswerNomalized : quoteAnswerNormalized;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L40)

```solidity
File: /src/staking/LockingMultiRewards.sol

123:         if (_lockDuration < MIN_LOCK_DURATION) {

127:         if (_rewardsDuration < MIN_REWARDS_DURATION) {

326:         if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

374:         if (_remainingRewardTime < minRemainingTime) {

379:         if (block.timestamp < reward.periodFinish) {

384:         if (amount < _remainingRewardTime) {

417:             if (index == lastLockIndex[user] && locks.length > 1) {

422:             if (locks[index].unlockTime > block.timestamp) {

490:         if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {

497:             if (amount < minLockAmount) {

623:             if (i < rewardItemLength) {

636:                     if (amount > 0) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L636)

</details>

### <a name="GAS-59-1695857615"></a>[GAS-59] Avoid transferring amounts of zero in order to save gas
Skipping the external call when nothing will be transferred, will save at least **100 gas**

*Instances (12)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/MagicLP.sol

466:         token.safeTransfer(to, amount);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L466-L466)

```solidity
File: /src/mimswap/periphery/Router.sol

68:         baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);

69:         quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);

91:         token.safeTransferFrom(msg.sender, clone, tokenInAmount);

224:         token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);

246:         token.safeTransferFrom(msg.sender, lp, tokenInAmount);

269:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

282:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

311:         token.safeTransfer(to, tokenAmountOut);

360:         inToken.safeTransfer(address(firstLp), msg.value);

428:         baseToken.safeTransfer(lp, msg.value);

474:         quoteToken.safeTransfer(lp, msg.value);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L474-L474)

</details>

### <a name="GAS-60-1694790859"></a>[GAS-60] Unnecessary casting as variable is already of the same type

*Instances (23)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

//@audit `bootstrapper` is getting converted from `address` to `address`
227:         return address(bootstrapper);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L227)

```solidity
File: /src/blast/libraries/BlastYields.sol

//@audit `token` is getting converted from `address` to `address`
72:         emit LogBlastTokenClaimed(recipient, address(token), amount);

//@audit `token` is getting converted from `address` to `address`
77:         emit LogBlastTokenClaimed(recipient, address(token), amount);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastYields.sol#L77)

```solidity
File: /src/mimswap/MagicLP.sol

//@audit `_BASE_TOKEN_` is getting converted from `address` to `address`
264:         emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

//@audit `_QUOTE_TOKEN_` is getting converted from `address` to `address`
264:         emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

//@audit `_QUOTE_TOKEN_` is getting converted from `address` to `address`
287:         emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

//@audit `_BASE_TOKEN_` is getting converted from `address` to `address`
287:         emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

//@audit `_QUOTE_TOKEN_` is getting converted from `address` to `address`
325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

//@audit `_BASE_TOKEN_` is getting converted from `address` to `address`
325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

//@audit `_BASE_TOKEN_` is getting converted from `address` to `address`
347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

//@audit `_QUOTE_TOKEN_` is getting converted from `address` to `address`
347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L347)

```solidity
File: /src/mimswap/periphery/Factory.sol

//@audit `implementation` is getting converted from `address` to `address`
85:         clone = LibClone.cloneDeterministic(address(implementation), salt);

//@audit `baseToken_` is getting converted from `address` to `address`
86:         IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);

//@audit `quoteToken_` is getting converted from `address` to `address`
86:         IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L86)

```solidity
File: /src/mimswap/periphery/Router.sol

//@audit `lp` is getting converted from `address` to `address`
119:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;

//@audit `lp` is getting converted from `address` to `address`
120:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;

//@audit `lp` is getting converted from `address` to `address`
252:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp));

//@audit `lp` is getting converted from `address` to `address`
253:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp));

//@audit `firstLp` is getting converted from `address` to `address`
328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

//@audit `firstLp` is getting converted from `address` to `address`
330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

//@audit `firstLp` is getting converted from `address` to `address`
360:         inToken.safeTransfer(address(firstLp), msg.value);

//@audit `lp` is getting converted from `address` to `address`
515:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;

//@audit `lp` is getting converted from `address` to `address`
516:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L516)

</details>

### <a name="GAS-61-1693313275"></a>[GAS-61] Use assembly to validate `msg.sender`
We can use assembly to efficiently validate msg.sender with the least amount of opcodes necessary. For more details check the following report [Here](https://code4rena.com/reports/2023-05-juicebox#g-06-use-assembly-to-validate-msgsender)

*Instances (2)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastMagicLP.sol

119:         if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L119-L119)

```solidity
File: /src/mimswap/MagicLP.sol

608:         if (msg.sender != implementation.owner()) {

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L608-L608)

</details>

### <a name="GAS-62-1709392376"></a>[GAS-62] Use the inputs/results of assignments rather than re-reading state variables
When a state variable is assigned, it saves gas to use the value being assigned, later in the function, rather than re-reading the state variable itself. If needed, it can also be stored to a local variable, and be used in that way. Both options avoid a Gwarmaccess (**100 gas**). Note that if the operation is, say `+=`, the assignment also results in a value which can be used. The instances below point to the first reference after the assignment, since later references are already covered by issues describing the caching of state variable values.

*Instances (9)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboardingBoot.sol

//@audit use result of assignment of staking, here
118:         staking.setOperator(address(this), true);

//@audit use result of assignment of router, here
131:         factory = IFactory(router.factory());

//@audit use result of assignment of ready, here
148:         emit LogReadyChanged(ready);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L148)

```solidity
File: /src/mimswap/MagicLP.sol

//@audit use result of assignment of _RState_, here
144:         if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

//@audit use result of assignment of _QUOTE_TARGET_, here
144:         if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

//@audit use result of assignment of _BASE_TARGET_, here
146:             _BASE_TARGET_ = _BASE_RESERVE_;

//@audit use result of assignment of _RState_, here
342:             if (_RState_ != uint32(newRState)) {

//@audit use result of assignment of _QUOTE_TARGET_, here
385:             if (_QUOTE_TARGET_ == 0) {

//@audit use result of assignment of _BASE_TARGET_, here
402:             _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L402)

</details>

### <a name="GAS-63-1699451597"></a>[GAS-63] Using `constant`s instead of `enum` can save gas
`Enum` is expensive and it is [more efficient to use constants](https://www.codehawks.com/finding/clm84992q02j9w9ruebun36d9) instead. An illustrative example of this approach can be found in the [ReentrancyGuard.sol](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/181d518609a9f006fcb97af63e6952e603cf100e/contracts/utils/ReentrancyGuard.sol#L34-L35).

*Instances (2)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

18:     enum State {
            Idle,
            Opened,
            Closed
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L18-L22)

```solidity
File: /src/mimswap/libraries/PMMPricing.sol

21:     enum RState {
            ONE,
            ABOVE_ONE,
            BELOW_ONE
        }

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/PMMPricing.sol#L21-L25)

</details>

### <a name="GAS-64-1705427608"></a>[GAS-64] Consider using solady's 'FixedPointMathLib'
Using Solady's 'FixedPointMathLib' for multiplication or division operations in Solidity can lead to significant gas savings. This library is designed to optimize fixed-point arithmetic operations, which are common in financial calculations involving tokens or currencies. By implementing more efficient algorithms and assembly optimizations, 'FixedPointMathLib' minimizes the computational resources required for these operations. For contracts that frequently perform such calculations, integrating this library can reduce transaction costs, thereby enhancing overall performance and cost-effectiveness. However, developers must ensure compatibility with their existing codebase and thoroughly test for accuracy and expected behavior to avoid any unintended consequences.

*Instances (96)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboardingBoot.sol

//@audit for: `/`
163:         return (userLocked * totalPoolShares) / totalLocked;

//@audit for: `*`
163:         return (userLocked * totalPoolShares) / totalLocked;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L163-L163)

```solidity
File: /src/mimswap/MagicLP.sol

//@audit for: `/`
435:         baseAmount = (baseBalance * shareAmount) / totalShares;

//@audit for: `*`
435:         baseAmount = (baseBalance * shareAmount) / totalShares;

//@audit for: `/`
436:         quoteAmount = (quoteBalance * shareAmount) / totalShares;

//@audit for: `*`
436:         quoteAmount = (quoteBalance * shareAmount) / totalShares;

//@audit for: `*`
438:         _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));

//@audit for: `*`
439:         _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));

//@audit for: `/`
513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

//@audit for: `*`
513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

//@audit for: `/`
517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));

//@audit for: `*`
517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));

//@audit for: `*`
553:                 _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L553-L553)

```solidity
File: /src/mimswap/libraries/DecimalMath.sol

//@audit for: `/`
24:         return (target * d) / ONE;

//@audit for: `*`
24:         return (target * d) / ONE;

//@audit for: `*`
28:         return (target * d).divCeil(ONE);

//@audit for: `/`
32:         return (target * ONE) / d;

//@audit for: `*`
32:         return (target * ONE) / d;

//@audit for: `*`
36:         return (target * ONE).divCeil(d);

//@audit for: `/`
40:         return ONE2 / target;

//@audit for: `/`
53:             uint p = powFloor(target, e / 2);

//@audit for: `/`
54:             p = (p * p) / ONE;

//@audit for: `*`
54:             p = (p * p) / ONE;

//@audit for: `/`
56:                 p = (p * target) / ONE;

//@audit for: `*`
56:                 p = (p * target) / ONE;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/DecimalMath.sol#L56-L56)

```solidity
File: /src/mimswap/libraries/Math.sol

//@audit for: `/`
20:         uint256 quotient = a / b;

//@audit for: `*`
21:         uint256 remainder = a - quotient * b;

//@audit for: `/`
30:         uint256 z = x / 2 + 1;

//@audit for: `/`
34:             z = (x / z + z) / 2;

//@audit for: `/`
34:             z = (x / z + z) / 2;

//@audit for: `*`
56:         uint256 fairAmount = i * (V1 - V2); // i*delta

//@audit for: `/`
59:             return fairAmount / DecimalMath.ONE;

//@audit for: `/`
62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

//@audit for: `*`
62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

//@audit for: `/`
64:         return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;

//@audit for: `*`
64:         return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;

//@audit for: `*`
93:         uint256 ki = (4 * k) * i;

//@audit for: `*`
93:         uint256 ki = (4 * k) * i;

//@audit for: `/`
96:         } else if ((ki * delta) / ki == delta) {

//@audit for: `*`
96:         } else if ((ki * delta) / ki == delta) {

//@audit for: `/`
97:             _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);

//@audit for: `*`
97:             _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);

//@audit for: `*`
99:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);

//@audit for: `/`
99:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);

//@audit for: `*`
101:         uint256 premium = DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2) + DecimalMath.ONE;

//@audit for: `*`
152:             uint256 idelta = i * delta;

//@audit for: `/`
155:             } else if ((idelta * V1) / idelta == V1) {

//@audit for: `*`
155:             } else if ((idelta * V1) / idelta == V1) {

//@audit for: `/`
156:                 temp = (idelta * V1) / (V0 * V0);

//@audit for: `*`
156:                 temp = (idelta * V1) / (V0 * V0);

//@audit for: `*`
156:                 temp = (idelta * V1) / (V0 * V0);

//@audit for: `/`
158:                 temp = (((delta * V1) / V0) * i) / V0;

//@audit for: `*`
158:                 temp = (((delta * V1) / V0) * i) / V0;

//@audit for: `/`
158:                 temp = (((delta * V1) / V0) * i) / V0;

//@audit for: `*`
158:                 temp = (((delta * V1) / V0) * i) / V0;

//@audit for: `/`
160:             return (V1 * temp) / (temp + DecimalMath.ONE);

//@audit for: `*`
160:             return (V1 * temp) / (temp + DecimalMath.ONE);

//@audit for: `*`
170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB

//@audit for: `*`
170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB

//@audit for: `/`
170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB

//@audit for: `*`
170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB

//@audit for: `*`
171:         uint256 bAbs = (DecimalMath.ONE - k) * V1; // (1-k)Q1

//@audit for: `/`
181:         bAbs = bAbs / DecimalMath.ONE;

//@audit for: `*`
184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2

//@audit for: `*`
184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2

//@audit for: `*`
185:         squareRoot = sqrt((bAbs * bAbs) + squareRoot); // sqrt(b*b+4(1-k)kQ0*Q0)

//@audit for: `*`
188:         uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/Math.sol#L188-L188)

```solidity
File: /src/mimswap/libraries/PMMPricing.sol

//@audit for: `/`
205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);

//@audit for: `*`
205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);

//@audit for: `/`
209:             uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);

//@audit for: `*`
209:             uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/libraries/PMMPricing.sol#L209-L209)

```solidity
File: /src/mimswap/periphery/Router.sol

//@audit for: `/`
257:         baseAmountOut = (baseBalance * sharesIn) / totalShares;

//@audit for: `*`
257:         baseAmountOut = (baseBalance * sharesIn) / totalShares;

//@audit for: `/`
258:         quoteAmountOut = (quoteBalance * sharesIn) / totalShares;

//@audit for: `*`
258:         quoteAmountOut = (quoteBalance * sharesIn) / totalShares;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L258-L258)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

//@audit for: `*`
38:         uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));

//@audit for: `*`
39:         uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));

//@audit for: `*`
43:         baseReserve = baseReserve * (10 ** (WAD - baseDecimals));

//@audit for: `*`
44:         quoteReserve = quoteReserve * (10 ** (WAD - quoteDecimals));

//@audit for: `/`
45:         return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());

//@audit for: `*`
45:         return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L45-L45)

```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit for: `/`
144:         maxLocks = _lockDuration / _rewardsDuration;

//@audit for: `*`
204:         return _rewardData[rewardToken].rewardRate * rewardsDuration;

//@audit for: `/`
236:         return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);

//@audit for: `*`
236:         return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);

//@audit for: `/`
241:         return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);

//@audit for: `*`
241:         return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);

//@audit for: `*`
258:         return (block.timestamp / rewardsDuration) * rewardsDuration;

//@audit for: `/`
258:         return (block.timestamp / rewardsDuration) * rewardsDuration;

//@audit for: `/`
283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

//@audit for: `*`
283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

//@audit for: `*`
283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

//@audit for: `/`
294:         return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];

//@audit for: `*`
294:         return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];

//@audit for: `*`
380:             amount += _remainingRewardTime * reward.rewardRate;

//@audit for: `/`
388:         reward.rewardRate = amount / _remainingRewardTime;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L388-L388)

</details>

### <a name="GAS-65-1694794906"></a>[GAS-65] Using mappings instead of arrays to avoid length checks save gas
Just by using a mapping, we get a gas saving of 2102 gas. When you read the value of an index of an array, solidity adds bytecode that checks that you are reading from a valid index (i.e an index strictly less than the length of the array) else it reverts with a panic error (Panic(0x32) to be precise). This prevents from reading unallocated or worse, allocated storage/memory locations.
Due to the way mappings are(simply a key => value pair), no check like that exists and we are able to read from the a storage slot directly.Itâ€™s important to note that when using mappings in this manner, your code should ensure that you are not reading an out of bound index of your canonical array.

*Instances (4)*:
<details><summary> see instances </summary>

```solidity
File: /src/mimswap/periphery/Factory.sol

35:     mapping(address base => mapping(address quote => address[] pools)) public pools;

36:     mapping(address creator => address[] pools) public userPools;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L36-L36)

```solidity
File: /src/staking/LockingMultiRewards.sol

91:     mapping(address user => LockedBalance[] locks) private _userLocks;

98:     address[] public rewardTokens;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L98-L98)

</details>

### <a name="GAS-66-1699443465"></a>[GAS-66] Using `private` for constants saves gas
If needed, the values can be read from the verified contract source code, or if there are multiple values there can be a single getter function that [returns a tuple](https://github.com/code-423n4/2022-08-frax/blob/90f55a9ce4e25bceed3a74290b854341d8de6afa/src/contracts/FraxlendPair.sol#L156-L178) of the values of all currently-public constants. Saves **3406-3606 gas** in deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table

*Instances (23)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastBox.sol

20:     BlastTokenRegistry public immutable registry;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastBox.sol#L20-L20)

```solidity
File: /src/blast/BlastMagicLP.sol

17:     BlastTokenRegistry public immutable registry;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastMagicLP.sol#L17-L17)

```solidity
File: /src/blast/libraries/BlastPoints.sol

7:     address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;

8:     IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/libraries/BlastPoints.sol#L8-L8)

```solidity
File: /src/mimswap/MagicLP.sol

61:     MagicLP public immutable implementation;

63:     uint256 public constant MAX_I = 10 ** 36;

64:     uint256 public constant MAX_K = 10 ** 18;

65:     uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%

66:     uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L66-L66)

```solidity
File: /src/mimswap/periphery/Router.sol

31:     uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;

33:     IWETH public immutable weth;

34:     IFactory public immutable factory;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L34-L34)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

10:     IMagicLP public immutable pair;

11:     IAggregator public immutable baseOracle;

12:     IAggregator public immutable quoteOracle;

13:     uint8 public immutable baseDecimals;

14:     uint8 public immutable quoteDecimals;

16:     uint256 public constant WAD = 18;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L16-L16)

```solidity
File: /src/staking/LockingMultiRewards.sol

83:     uint256 public immutable maxLocks;

84:     uint256 public immutable lockingBoostMultiplerInBips;

85:     uint256 public immutable rewardsDuration;

86:     uint256 public immutable lockDuration;

87:     address public immutable stakingToken;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L87-L87)

</details>

### <a name="GAS-67-1702131709"></a>[GAS-67] Use `solady` library where possible to save gas
[Solady](https://github.com/Vectorized/solady) is a Solidity library inspired by [Solmate](https://github.com/rari-capital/solmate), optimized heavily for gas optimizations and battle tested by [hundreds of developers](https://www.alchemy.com/dapps/solady). Consider implementing solady contracts where possible to reduce runtime gas fees.

*Instances (9)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

8: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L8-L8)

```solidity
File: /src/blast/BlastOnboardingBoot.sol

9: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboardingBoot.sol#L9-L9)

```solidity
File: /src/mimswap/MagicLP.sol

12: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

14: import {ERC20} from "solady/tokens/ERC20.sol";

15: import {SafeCastLib} from "solady/utils/SafeCastLib.sol";

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/MagicLP.sol#L15-L15)

```solidity
File: /src/mimswap/periphery/Factory.sol

5: import {LibClone} from "solady/utils/LibClone.sol";

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L5-L5)

```solidity
File: /src/mimswap/periphery/Router.sol

4: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L4-L4)

```solidity
File: /src/oracles/aggregators/MagicLpAggregator.sol

4: import {FixedPointMathLib} from "solady/utils/FixedPointMathLib.sol";

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/oracles/aggregators/MagicLpAggregator.sol#L4-L4)

```solidity
File: /src/staking/LockingMultiRewards.sol

6: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L6-L6)

</details>

### <a name="GAS-68-1707922603"></a>[GAS-68] Use Array.unsafeAccess() to avoid repeated array length checks
When using storage arrays, solidity adds an internal lookup of the array's length (a Gcoldsload 2100 gas) to ensure you don't read past the array's end. You can avoid this lookup by using `Array.unsafeAccess()` in cases where the length has already been checked, as is the case with the instances below

*Instances (28)*:
<details><summary> see instances </summary>

```solidity
File: /src/blast/BlastOnboarding.sol

166:             if (!supportedTokens[tokens[i]]) {

169:             if (registry.nativeYieldTokens(tokens[i])) {

170:                 BlastYields.claimAllTokenYields(tokens[i], feeTo);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/blast/BlastOnboarding.sol#L170-L170)

```solidity
File: /src/mimswap/periphery/Factory.sol

128:         address pool = _pools[poolIndex];

131:         _pools[poolIndex] = _pools[_pools.length - 1];

131:         _pools[poolIndex] = _pools[_pools.length - 1];

134:         if (_userPools[userPoolIndex] != pool) {

138:         _userPools[userPoolIndex] = _userPools[_userPools.length - 1];

138:         _userPools[userPoolIndex] = _userPools[_userPools.length - 1];

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Factory.sol#L138-L138)

```solidity
File: /src/mimswap/periphery/Router.sol

376:         address lastLp = path[lastLpIndex];

389:         address firstLp = path[0];

547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));

547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));

550:                 IMagicLP(path[i]).sellQuote(address(path[i + 1]));

550:                 IMagicLP(path[i]).sellQuote(address(path[i + 1]));

561:             amountOut = IMagicLP(path[iterations]).sellBase(to);

563:             amountOut = IMagicLP(path[iterations]).sellQuote(to);

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/mimswap/periphery/Router.sol#L563-L563)

```solidity
File: /src/staking/LockingMultiRewards.sol

406:             address user = users[i];

414:             uint256 index = lockIndexes[i];

422:             if (locks[index].unlockTime > block.timestamp) {

426:             uint256 amount = locks[index].amount;

435:                 locks[index] = locks[lastIndex];

435:                 locks[index] = locks[lastIndex];

548:             _updateRewardsGlobal(rewardTokens[i], totalSupply_);

562:             address token = rewardTokens[i];

576:             address token = rewardTokens[i];

581:                 address user = users[j];

615:             address rewardToken = rewardTokens[i];

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L615-L615)

</details>

### <a name="GAS-69-1693313317"></a>[GAS-69] Can make the variable outside the loop to save gas
Creating variables inside the loop consum more gas compared to declaring them outside and just reaffecting values to them inside the loop.

*Instances (16)*:
<details><summary> see instances </summary>

```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit variable `user` is created inside a loop.
406:             address user = users[i];

//@audit variable `bal` is created inside a loop.
407:             Balances storage bal = _balances[user];

//@audit variable `locks` is created inside a loop.
408:             LockedBalance[] storage locks = _userLocks[user];

//@audit variable `index` is created inside a loop.
414:             uint256 index = lockIndexes[i];

//@audit variable `amount` is created inside a loop.
426:             uint256 amount = locks[index].amount;

//@audit variable `lastIndex` is created inside a loop.
427:             uint256 lastIndex = locks.length - 1;

//@audit variable `token` is created inside a loop.
562:             address token = rewardTokens[i];

//@audit variable `token` is created inside a loop.
576:             address token = rewardTokens[i];

//@audit variable `rewardPerToken_` is created inside a loop.
577:             uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);

//@audit variable `j` is created inside a loop.
580:             for (uint256 j; j < users.length; ) {

//@audit variable `user` is created inside a loop.
581:                 address user = users[j];

//@audit variable `user` is created inside a loop.
581:                 address user = users[j];

//@audit variable `rewardToken` is created inside a loop.
615:             address rewardToken = rewardTokens[i];

//@audit variable `rewardAmount` is created inside a loop.
616:             uint256 rewardAmount = rewards[user][rewardToken];

//@audit variable `item` is created inside a loop.
624:                 RewardLockItem storage item = _rewardLock.items[i];

//@audit variable `amount` is created inside a loop.
628:                     uint256 amount = item.amount;

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//src/staking/LockingMultiRewards.sol#L628)

</details>

### <a name="GAS-70-1693313355"></a>[GAS-70] Consider activating via-ir for deploying
The Solidity compiler's Intermediate Representation (IR) based code generator, which can be activated using --via-ir on the command line or {""viaIR"": true} in the options, serves a dual purpose. Firstly, it boosts the transparency and audibility of code generation, which enhances developers' comprehension and control over the contract's final bytecode. Secondly, it enables more sophisticated optimization passes that span multiple functions, thereby potentially leading to more efficient bytecode.
It's important to note that using the IR- based code generator may lengthen compile times due to the extra optimization steps.Therefore, it's advised to test your contract with and without this option enabled to measure the performance and gas cost implications.If the IR- based code generator significantly enhances your contract's performance or reduces gas costs, consider using the --via-ir flag during deployment.This way, you can leverage more advanced compiler optimizations without hindering your development workflow.

*Instances (1)*:
<details><summary> see instances </summary>

```solidity
File: hardhat.config.ts

//@audit /2024-03-abracadabra-money/lib/safe-contracts/hardhat.config.ts
1: 

```
[Link to code](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/hardhat.config.ts#L1)

</details>
