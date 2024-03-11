
## Low Findings

|    | Issue | Instances |
|----|-------|:---------:|
| [L-01] | Addition/multiplication in `unchecked` block is unsafe | 1 |
| [L-02] | Low Level Calls to Custom Addresses | 1 |
| [L-03] | Potential DoS Risk with Loops Iterating Over Large State Arrays | 4 |
| [L-04] | Centralization risk for privileged functions | 53 |
| [L-05] | Unused/empty `receive()/fallback()` function | 2 |
| [L-06] | Unauthorized `receive()/fallback()` Functions | 2 |
| [L-07] | Subtraction may underflow if multiplication is too large | 3 |
| [L-08] | `decimals()` is not part of the ERC20 standard | 9 |
| [L-09] | Some tokens may revert on large transfers | 37 |
| [L-10] | Code does not follow the best practice of check-effects-interaction | 3 |
| [L-11] | Initializers can be front-run | 2 |
| [L-12] | Consider adding a time delay to upgrade implementation functions | 4 |
| [L-13] | Prefer skip over `revert` model in loops | 4 |
| [L-14] | Unbounded loop may run out of gas | 7 |
| [L-15] | Lack of index element validation in external/public function | 52 |
| [L-16] | Consider checking that transfer to `address(this)` is disabled | 2 |
| [L-17] | Prevent Division by Zero | 22 |
| [L-18] | Usage of Deprecated `latestAnswer()` Function | 2 |
| [L-19] | Solidity version 0.8.20 may not work on other chains due to `PUSH0` | 20 |
| [L-20] | Initializer missing `address(0)` Check before assignment | 1 |
| [L-21] | Missing checks for `address(0x0)` when updating address state variables | 8 |
| [L-22] | Risk of Renouncing Ownership While System is Paused | 2 |
| [L-23] | Input Validation Missing in Setter Functions | 1 |
| [L-24] | Avoid using `tx.origin` | 5 |
| [L-25] | Unhandled Zero `totalSupply` Division Case | 2 |
| [L-26] | Large approvals may not work with some ERC20 tokens | 1 |
| [L-27] | Lack of Parameter Validation in Constructor/Initializer | 3 |
| [L-28] | Mint to zero address | 1 |
| [L-29] | State variables are not limited to a reasonable range | 5 |
| [L-30] | Missing Contract-Existence Checks Before Low-Level Calls | 1 |
| [L-31] | Events may be emitted out of order due to reentrancy | 10 |
| [L-32] | External calls in an un-bounded `for-`loop may result in a revert | 5 |
| [L-33] | Critical functions should be a two step procedure | 18 |
| [L-34] | Upper Limits for Fees/Rates Should Be Implemented | 10 |
| [L-35] | Deprecated Function `safeApprove` Usage | 3 |
| [L-36] | Implement two-step ownership transfers | 1 |
| [L-37] | Loss of precision | 40 |
| [L-38] | Array is `push()`ed but not `pop()`ed | 1 |
| [L-39] | Mapping arrays can grow in size without a way to shrink them | 2 |
| [L-40] | Unbounded Gas Consumption on External Calls | 1 |
| [L-41] | Unsafe downcast from larger to smaller integer types | 14 |
| [L-42] | Consider implementing two-step procedure for updating protocol addresses | 24 |
| [L-43] | Possible Revert ERC20 Transfers with Zero Value | 14 |
| [L-44] | Potential Re-org Attack Vector | 1 |
| [L-45] | Function Parameters in Public Accessible Functions Need `address(0)` Check | 70 |
| [L-46] | Missing `address(0)` Check in Constructor | 2 |
| [L-47] | Functions calling tokens with transfer hooks are missing reentrancy guards | 37 |
| [L-48] | Casting `block.timestamp` to Smaller Integer Types Limit Contract Lifespan | 2 |
| [L-49] | Solady/Solmate's SafeTransferLib Doesn't Check Existence of ERC20 Contract | 11 |


## NonCritical Findings

|    | Issue | Instances |
|----|-------|:---------:|
| [N-01] | `internal/private` Function calls within for loops | 10 |
| [N-02] | Non-library/interface files should use fixed compiler versions, not floating ones | 15 |
| [N-03] | Array indices should be referenced via `enum`s rather than via numeric literals | 3 |
| [N-04] | Consider splitting long calculations | 2 |
| [N-05] | Missing Event Emission After Critical Initialize() Function | 2 |
| [N-06] | Mixed usage of `int/uint` with `int256/uint256` | 2 |
| [N-07] | Avoid Hard-Coded Addresses | 5 |
| [N-08] | Variables need not be initialized to zero | 2 |
| [N-09] | Multiple `address`/ID mappings can be combined into a single `mapping` of an `address`/ID to a `struct`, for readability | 13 |
| [N-10] | Consider returning a `struct` rather than having multiple `return` values | 11 |
| [N-11] | Consider using a `struct` rather than having many function input parameters | 26 |
| [N-12] | Avoid using constant decimals in expressions | 3 |
| [N-13] | Avoid Empty Blocks in Code | 2 |
| [N-14] | Multiple Contracts Declared in Single File | 7 |
| [N-15] | Custom error has no error details | 78 |
| [N-16] | Consider using OpenZeppelin's SafeCast for any casting | 54 |
| [N-17] | `uint/int` variables should have the bit size defined explicitly | 2 |
| [N-18] | Consider using `delete` rather than assigning `false` to clear values | 1 |
| [N-19] | Consider using `delete` rather than assigning `zero` to clear values | 2 |
| [N-20] | Avoid external calls in modifiers | 3 |
| [N-21] | Consider emitting an event at the end of the constructor | 16 |
| [N-22] | Consider moving duplicated strings to constants | 3 |
| [N-23] | Consider providing a ranged getter for array state variables | 1 |
| [N-24] | Consider using named returns | 62 |
| [N-25] | Style guide: Initialisms should be capitalized | 20 |
| [N-26] | Expressions for constant values should use `immutable` rather than `constant` | 6 |
| [N-27] | Consider using named function arguments | 127 |
| [N-28] | Contract/Library Names Not in `CapWords` Style (CamelCase) | 5 |
| [N-29] | Events are missing sender information | 35 |
| [N-30] | Non-constant/non-immutable variables using all capital letters | 25 |
| [N-31] | Leverage Recent Solidity Features with `0.8.23` | 20 |
| [N-32] | NatSpec: Function `@param` tag is missing | 157 |
| [N-33] | High cyclomatic complexity | 10 |
| [N-34] | Contract should expose an `interface` | 124 |
| [N-35] | NatSpec: Function declarations should have descriptions | 135 |
| [N-36] | Contract uses both `require()`/`revert()` as well as custom errors | 12 |
| [N-37] | Modifiers Missing NatSpec `@param` Tag | 3 |
| [N-38] | Inconsistent spacing in comments | 195 |
| [N-39] | Unused `error` definition | 5 |
| [N-40] | Critical system parameter changes should be behind a timelock | 18 |
| [N-41] | Outdated Solidity Version | 20 |
| [N-42] | Ensure Non-Empty Check for Bytes in Function Parameters | 6 |
| [N-43] | Adding a `return` statement when the function defines a named return variable, is redundant | 1 |
| [N-44] | Use `bytes.concat()` instead of `abi.encodePacked()` | 2 |
| [N-45] | Function/Constructor Argument Names Not in mixedCase | 40 |
| [N-46] | NatSpec: Function `@return` tag is missing | 119 |
| [N-47] | State-Altering Functions Should Emit Events | 8 |
| [N-48] | Upgrade `openzeppelin` to the Latest Version - 5.0.0 | 8 |
| [N-49] | Duplicated `require()`/`revert()` checks should be refactored to a modifier or function | 25 |
| [N-50] | Event is not properly `indexed` | 39 |
| [N-51] | Consider Adding Emergency-Stop Functionality | 13 |
| [N-52] | Missing NatSpec Descriptions for Modifier Declarations | 7 |
| [N-53] | NatSpec: Public State variable declarations should have descriptions | 70 |
| [N-54] | Consider adding a block/deny-list | 4 |
| [N-55] | Non-uppercase/Constant-case Naming for `immutable` Variables | 16 |
| [N-56] | Not using the named return variables anywhere in the function is confusing | 26 |
| [N-57] | Function Names Not in mixedCase | 19 |
| [N-58] | Use scientific notation(1e18) instead of exponentiation(10**18) | 5 |
| [N-59] | Insufficient Comments in Complex Functions | 6 |
| [N-60] | Common functions should be refactored to a common base contract | 13 |
| [N-61] | NatSpec: Error declarations should have descriptions | 77 |
| [N-62] | NatSpec: Non-public state variable declarations should use `@dev` tags | 18 |
| [N-63] | `constant`s should be defined rather than using magic numbers | 23 |
| [N-64] | Variable Names Not in mixedCase | 10 |
| [N-65] | Consider moving `msg.sender` checks to a common authorization `modifier` | 2 |
| [N-66] | NatSpec: Contract declarations should have descriptions | 17 |
| [N-67] | NatSpec: Contract declarations should have `@author` tag | 19 |
| [N-68] | Inconsistent method of specifying a floating pragma | 20 |
| [N-69] | Style guide: Non-`external`/`public` function names should begin with an underscore | 25 |
| [N-70] | Missing NatSpec Descriptions for Event Declarations | 52 |
| [N-71] | Consider defining system-wide constants in a single file | 17 |
| [N-72] | Consider making contracts `Upgradeable` | 19 |
| [N-73] | Events that mark critical parameter changes should contain both the old and the new value | 15 |
| [N-74] | Style guide: Non-`external`/`public` variable names should begin with an underscore | 14 |
| [N-75] | Style guide: Contract does not follow the Solidity style guide's suggested layout ordering | 14 |
| [N-76] | Style guide: Control structures do not follow the Solidity Style Guide | 1 |
| [N-77] | Using Low-Level Call for Transfers | 1 |
| [N-78] | Consider bounding input array length | 3 |
| [N-79] | NatSpec: Function declarations should have `@notice` tag | 137 |
| [N-80] | Constants in comparisons should appear on the left side | 53 |
| [N-81] | NatSpec: Contract declarations should have `@notice` tag | 19 |
| [N-82] | Large numeric literals should use underscores for readability | 15 |
| [N-83] | Long functions should be refactored into multiple, smaller, functions | 6 |
| [N-84] | NatSpec: Contract declarations should have `@dev` tags | 23 |
| [N-85] | `public` functions not called by the contract should be declared `external` instead | 11 |
| [N-86] | Large multiples of ten should use scientific notation | 3 |
| [N-87] | Complex casting | 2 |
| [N-88] | Unused Event Declarations | 2 |
| [N-89] | Equal `block.timestamp` Cases Not Handled | 4 |
| [N-90] | `else`-block not required | 4 |
| [N-91] | Polymorphic functions make security audits more time-consuming and error-prone | 4 |
| [N-92] | Style guide: Function ordering does not follow the Solidity style guide | 30 |
| [N-93] | Avoid Using Pragma Without Upper Bound | 20 |
| [N-94] | Style guide: Lines are too long | 54 |
| [N-95] | Style guide: Extraneous whitespace | 15 |
| [N-96] | Misplaced or Missing SPDX identifier | 5 |
| [N-97] | Contract/Libraries Names Do Not Match Their Filenames | 3 |
| [N-98] | Avoid the use of sensitive terms | 4 |
| [N-99] | Unused import | 8 |
| [N-100] | `if`-statement can be converted to a ternary | 5 |
| [N-101] | Consider using named mappings | 3 |
| [N-102] | Use of `override` is unnecessary | 13 |
| [N-103] | Setters should prevent re-setting of the same value | 19 |
| [N-104] | NatSpec: Contract declarations should have `@title` tags | 21 |
| [N-105] | Use Unchecked for Divisions on Constant or Immutable Values | 8 |
| [N-106] | Explicit Visibility Recommended in Variable/Function Definitions | 8 |
| [N-107] | Contracts should have full test coverage | 1 |
| [N-108] | Large or complicated code bases should implement invariant tests | 1 |
| [N-109] | Implement Formal Verification Proofs to Improve Security | 1 |


## Low Findings Details

### [L-01] Addition/multiplication in `unchecked` block is unsafe

In Solidity, the `unchecked` block is used to disable automatic overflow/underflow checks for the arithmetic operations inside the block.
This can be dangerous as it might allow `underflow` (or `overflow`) to occur silently, potentially leading to unexpected behaviors or vulnerabilities in the contract. 

It is recommended to manually implement appropriate checks inside `unchecked` blocks to prevent `underflow` and `overflow`, ensuring the contract's correctness and security.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

/// @audit Unchecked block containing subtraction/addition/multiplication which may underflow.
553: _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;

```
[553](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L553)
</details>

### [L-02] Low Level Calls to Custom Addresses

Contracts should avoid making low-level calls to custom addresses, especially if these calls are based on address parameters in the function. 
Such behavior can lead to unexpected execution of untrusted code. Instead, consider using Solidity's high-level function calls or contract interactions.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastGovernor.sol

54: (success, result) = to.call{value: value}(data);
```
[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L54)
</details>

### [L-03] Potential DoS Risk with Loops Iterating Over Large State Arrays

Looping through state arrays can lead to denial of service (DoS) vulnerabilities if the array grows too large. 
If the computations within the loop are extensive enough to expend the entire transaction's gas, the function may fail.
Consider implementing mechanisms to check or limit the size of state arrays or to reduce the computational work within loops.

<details>
<summary><i>4 issue instances in 1 files:</i></summary>

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit state `rewardTokens[]` is `push()`ed and may grow too large to iterate over. | 313: rewardTokens.push(rewardToken);
547: for (uint256 i; i < rewardTokens.length; ) {
/// @audit state `rewardTokens[]` is `push()`ed and may grow too large to iterate over. | 313: rewardTokens.push(rewardToken);
561: for (uint256 i; i < rewardTokens.length; ) {
/// @audit state `rewardTokens[]` is `push()`ed and may grow too large to iterate over. | 313: rewardTokens.push(rewardToken);
575: for (uint256 i; i < rewardTokens.length; ) {
/// @audit state `rewardTokens[]` is `push()`ed and may grow too large to iterate over. | 313: rewardTokens.push(rewardToken);
614: for (uint256 i; i < rewardTokens.length; ) {
```
[547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547) | [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561) | [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575) | [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614)
</details>

### [L-04] Centralization risk for privileged functions

Functions that grant centralized privileges introduce a notable security risk.
Such functions can act as a single point of vulnerability, especially if they control critical operations or access to sensitive data.
        
If the account or entity with these privileges gets compromised, it could lead to the unauthorized alteration of the contract's state, asset misappropriation, or other malicious activities.
It's essential to implement robust access controls, frequent audits, and potentially decentralize critical functions to mitigate this risk.

<details>
<summary><i>53 issue instances in 10 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

52: function claimGasYields() external onlyOperators returns (uint256)
56: function claimTokenYields(address token_) external onlyOperators returns (uint256 amount)
68: function callBlastPrecompile(bytes calldata data) external onlyOwner
72: function setFeeTo(address feeTo_) external onlyOwner
81: function setTokenEnabled(address token, bool enabled) external onlyOwner
```
[52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L52) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L56) | [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L68) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81)

```solidity
File: src/blast/BlastGovernor.sol

28: function claimNativeYields(address contractAddress) external onlyOperators returns (uint256)
32: function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256)
40: function setFeeTo(address _feeTo) external onlyOwner
49: function callBlastPrecompile(bytes calldata data) external onlyOwner
53: function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result)
```
[28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L28) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L32) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L49) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)

```solidity
File: src/blast/BlastMagicLP.sol

47: function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256)
53: function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount)
64: function updateTokenClaimables() external onlyClones onlyImplementationOperators
72: function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner
80: function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner
89: function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner
```
[47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L47) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L53) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L64) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L72) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89)

```solidity
File: src/blast/BlastOnboarding.sol

101: function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token)
123: function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token)
132: function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token)
147: function setFeeTo(address feeTo_) external onlyOwner
156: function callBlastPrecompile(bytes calldata data) external onlyOwner
160: function claimGasYields() external onlyOwner returns (uint256)
164: function claimTokenYields(address[] memory tokens) external onlyOwner
175: function setTokenSupported(address token, bool supported) external onlyOwner
185: function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token)
190: function setBootstrapper(address bootstrapper_) external onlyOwner
195: function open() external onlyOwner onlyState(State.Idle)
200: function close() external onlyOwner onlyState(State.Opened)
205: function rescue(address token, address to, uint256 amount) external onlyOwner
214: function pause() external onlyOwner
218: function unpause() external onlyOwner
```
[101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101) | [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L156) | [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L160) | [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164) | [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185) | [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190) | [195](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L195) | [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L200) | [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L205) | [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L214) | [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L218)

```solidity
File: src/blast/BlastOnboardingBoot.sol

96: function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256)
129: function initialize(Router _router) external onlyOwner
137: function setStaking(LockingMultiRewards _staking) external onlyOwner
146: function setReady(bool _ready) external onlyOwner onlyState(State.Closed)
```
[96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96) | [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129) | [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146)

```solidity
File: src/blast/BlastTokenRegistry.sol

14: function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14)

```solidity
File: src/mimswap/MagicLP.sol

461: function rescue(address token, address to, uint256 amount) external onlyImplementationOwner
470: function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner
504: function ratioSync() external nonReentrant onlyImplementationOwner
```
[461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L461) | [470](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470) | [504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L504)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

46: function setMaintainer(address maintainer_) external onlyOwner
57: function setImplementation(address implementation_) public onlyOwner
```
[46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)

```solidity
File: src/mimswap/periphery/Factory.sol

96: function setLpImplementation(address implementation_) external onlyOwner
105: function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner
116: function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner
120: function removePool(
        address creator,
        address baseToken,
        address quoteToken,
        uint256 poolIndex,
        uint256 userPoolIndex
    ) external onlyOwner
```
[96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96) | [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105) | [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L116) | [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L120)

```solidity
File: src/staking/LockingMultiRewards.sol

300: function addReward(address rewardToken) public onlyOwner
317: function setMinLockAmount(uint256 _minLockAmount) external onlyOwner
324: function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner
337: function pause() external onlyOwner
341: function unpause() external onlyOwner
349: function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators
361: function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators
397: function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators
```
[300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300) | [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317) | [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L324) | [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337) | [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L341) | [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L349) | [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361) | [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397)
</details>

### [L-05] Unused/empty `receive()/fallback()` function

If the intention is for the Ether to be used, the function should call another function, otherwise it should revert (e.g. require(msg.sender == address(weth))).

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastGovernor.sol

13: receive() external payable
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L13)

```solidity
File: src/mimswap/periphery/Router.sol

36: receive() external payable
```
[36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L36)
</details>

### [L-06] Unauthorized `receive()/fallback()` Functions

Empty receive() or payable fallback() functions without proper authorization can result in a loss of funds. If the intention is for the Ether to be used, the function should call another function, otherwise, it should revert (e.g. require(msg.sender == address(weth))).

Having no access control on the function means that someone may send Ether to the contract and have no way to get anything back out. Even if the concern is spending a small amount of gas to check the sender, the code should at least have a function to rescue unused Ether, ensuring funds are not trapped within the contract.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastGovernor.sol

13: receive() external payable
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L13)

```solidity
File: src/mimswap/periphery/Router.sol

36: receive() external payable
```
[36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L36)
</details>

### [L-07] Subtraction may underflow if multiplication is too large

In scenarios where a large multiplication precedes a subtraction, there is a heightened risk of underflow. This can occur if the multiplication results in a significantly large value, potentially leading to an underflow when it is subsequently subtracted.
Such underflows can cause critical miscalculations, affecting the contract's logic and integrity.

<details>
<summary><i>3 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

438: _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
439: _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
```
[438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439)

```solidity
File: src/mimswap/libraries/Math.sol

21: uint256 remainder = a - quotient * b;
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L21)
</details>

### [L-08] `decimals()` is not part of the ERC20 standard

It's often used, but `decimals()` is not part of the original ERC-20 standard. It was added later as an optional extension. 
Some valid ERC-20 tokens do not support this function, so casting all tokens to an interface that includes `decimals()` can be unsafe.
Consider revising your code to account for tokens that may not implement the `decimals()` function.

<details>
<summary><i>9 issue instances in 3 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

164: return IERC20Metadata(_BASE_TOKEN_).decimals();
```
[164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L164)

```solidity
File: src/mimswap/periphery/Router.sol

64: _validateDecimals(IERC20Metadata(baseToken).decimals(), IERC20Metadata(quoteToken).decimals());
64: _validateDecimals(IERC20Metadata(baseToken).decimals(), IERC20Metadata(quoteToken).decimals());
83: _validateDecimals(18, IERC20Metadata(token).decimals());
85: _validateDecimals(IERC20Metadata(token).decimals(), 18);
```
[64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L64) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L64) | [83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L83) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L85)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

25: baseDecimals = IERC20Metadata(pair_._BASE_TOKEN_()).decimals();
26: quoteDecimals = IERC20Metadata(pair_._QUOTE_TOKEN_()).decimals();
38: uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
39: uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L25) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L26) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L38) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L39)
</details>

### [L-09] Some tokens may revert on large transfers

Transfers that approach or exceed this limit will revert.
Be cautious of such transfers, especially if batching is not implemented to handle these scenarios.

<details>
<summary><i>37 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

102: token.safeTransferFrom(msg.sender, address(this), amount)
138: token.safeTransfer(msg.sender, amount)
210: token.safeTransfer(to, amount)
```
[102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L102) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L138) | [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L210)

```solidity
File: src/mimswap/MagicLP.sol

466: token.safeTransfer(to, amount)
583: _BASE_TOKEN_.safeTransfer(to, amount)
589: _QUOTE_TOKEN_.safeTransfer(to, amount)
```
[466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L466) | [583](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L583) | [589](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L589)

```solidity
File: src/mimswap/periphery/Router.sol

68: baseToken.safeTransferFrom(msg.sender, clone, baseInAmount)
69: quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount)
91: token.safeTransferFrom(msg.sender, clone, tokenInAmount)
92: address(weth).safeTransferFrom(address(this), clone, msg.value)
172: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount)
173: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount)
186: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount)
187: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount)
217: address(weth).safeTransfer(lp, wethAdjustedAmount)
224: token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount)
244: address(weth).safeTransfer(lp, msg.value)
246: token.safeTransferFrom(msg.sender, lp, tokenInAmount)
269: lp.safeTransferFrom(msg.sender, address(this), sharesIn)
282: lp.safeTransferFrom(msg.sender, address(this), sharesIn)
311: token.safeTransfer(to, tokenAmountOut)
328: IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn)
330: IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn)
360: inToken.safeTransfer(address(firstLp), msg.value)
393: IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn)
395: IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn)
411: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn)
428: baseToken.safeTransfer(lp, msg.value)
443: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn)
456: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn)
474: quoteToken.safeTransfer(lp, msg.value)
489: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn)
```
[68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L68) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L69) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L91) | [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92) | [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L172) | [173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L173) | [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L186) | [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L187) | [217](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L217) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L224) | [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L244) | [246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L246) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L269) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282) | [311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L311) | [328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L328) | [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L330) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L360) | [393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L393) | [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L395) | [411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L411) | [428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L428) | [443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L443) | [456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L456) | [474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L474) | [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L489)

```solidity
File: src/staking/LockingMultiRewards.sol

180: stakingToken.safeTransfer(msg.sender, amount)
330: tokenAddress.safeTransfer(owner, tokenAmount)
367: rewardToken.safeTransferFrom(msg.sender, address(this), amount)
464: stakingToken.safeTransferFrom(msg.sender, address(this), amount)
637: rewardToken.safeTransfer(user, amount)
```
[180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L180) | [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L330) | [367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367) | [464](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L464) | [637](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L637)
</details>

### [L-10] Code does not follow the best practice of check-effects-interaction

Code should follow the best-practice of [check-effects-interaction](https://blockchain-academy.hs-mittweida.de/courses/solidity-coding-beginners-to-intermediate/lessons/solidity-11-coding-patterns/topic/checks-effects-interactions/), where state variables are updated before any external calls are made. Doing so prevents a large class of reentrancy bugs.

<details>
<summary><i>3 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit - State change after external call: `token.safeTransferFrom(msg.sender, address(this), amount)`
105: totals[token].locked += amount
```
[105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L105)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit - State change after external call: `stakingToken.safeTransfer(msg.sender, amount)`
181: stakingTokenBalance -= amount
/// @audit - State change after external call: `stakingToken.safeTransferFrom(msg.sender, address(this), amount)`
465: stakingTokenBalance += amount
```
[181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L181) | [465](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L465)
</details>

### [L-11] Initializers can be front-run

Initializers could be vulnerable to front-running attacks.
This might allow an attacker to set their own values, take ownership of the contract, or force a redeployment in the best-case scenario.
Be cautious of potential front-running risks in the following instances found in the code.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastWrappers.sol

59: function init(bytes calldata data) public payable override
```
[59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59)

```solidity
File: src/mimswap/MagicLP.sol

91: function init(
        address baseTokenAddress,
        address quoteTokenAddress,
        uint256 lpFeeRate,
        address mtFeeRateModel,
        uint256 i,
        uint256 k
    ) external
```
[91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L91)
</details>

### [L-12] Consider adding a time delay to upgrade implementation functions

Implementing a timelock mechanism on sensitive functions, such as contract upgrades, is a crucial practice in smart contract development, particularly for those handling user funds or critical aspects of a system.
A timelock introduces a mandatory delay between the initial scheduling of a critical action (like an upgrade) and its actual execution.
This delay serves as a protective window, allowing users and governance participants to review and assess the proposed changes.
In cases of disagreement or detection of potential issues, this period provides an opportunity to intervene or prepare for the change, enhancing trust and security in the contract's operations.

<details>
<summary><i>4 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastWrappers.sol

29: constructor(
        address implementation_,
        IFeeRateModel maintainerFeeRateModel_,
        address owner_,
        address governor_
    ) Factory(implementation_, maintainerFeeRateModel_, owner_)
```
[29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L29)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

57: function setImplementation(address implementation_) public onlyOwner
```
[57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)

```solidity
File: src/mimswap/periphery/Factory.sol

38: constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_)
96: function setLpImplementation(address implementation_) external onlyOwner
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96)
</details>

### [L-13] Prefer skip over `revert` model in loops

When dealing with array operations in Solidity, it's often wiser to opt for skipping over reverting.
Instead of halting the entire transaction when a condition isn't met, suggests simply moving on to the next array index.
The reason behind this choice is to reduce the risk of malicious actors intentionally introducing array objects that fail conditional checks within loops, causing group operations to fail.
Unless there's a compelling security or logical justification for reverting, it's recommended to embrace the skip-over approach for a more robust codebase.

<details>
<summary><i>4 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

167: revert ErrUnsupportedToken()
```
[167](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L167)

```solidity
File: src/staking/LockingMultiRewards.sol

411: revert ErrNoLocks()
418: revert ErrInvalidLockIndex()
423: revert ErrLockNotExpired()
```
[411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L411) | [418](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L418) | [423](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L423)
</details>

### [L-14] Unbounded loop may run out of gas

Unbounded loops in smart contracts pose a risk because they iterate over an unknown number of elements, potentially consuming all available gas for a transaction.
This can result in unintended transaction failures. Gas consumption increases linearly with the number of iterations, and if it surpasses the gas limit, the transaction reverts, wasting the gas spent.
To mitigate this, developers should either set a maximum limit on loop iterations.

<details>
<summary><i>7 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

165: for (uint256 i = 0; i < tokens.length; i++)
```
[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)

```solidity
File: src/staking/LockingMultiRewards.sol

405: for (uint256 i; i < users.length; )
547: for (uint256 i; i < rewardTokens.length; )
561: for (uint256 i; i < rewardTokens.length; )
575: for (uint256 i; i < rewardTokens.length; )
580: for (uint256 j; j < users.length; )
614: for (uint256 i; i < rewardTokens.length; )
```
[405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405) | [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547) | [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561) | [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575) | [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580) | [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614)
</details>

### [L-15] Lack of index element validation in external/public function

There's no validation to check whether the index element provided as an argument actually exists in the call. This omission could lead to unintended behavior if an element that does not exist in the call is passed to the function.

The function should validate that the provided index element exists in the call before proceeding.

Without this validation, the function could cause unintended behaviour as it will call an non-existing index element. This could lead to inconsistencies in data and potentially affect the integrity of the call structure.

<details>
<summary><i>52 issue instances in 7 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

82: enabledTokens[token]
```
[82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L82)

```solidity
File: src/blast/BlastMagicLP.sol

90: operators[operator]
```
[90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L90)

```solidity
File: src/blast/BlastOnboarding.sol

105: totals[token]
106: balances[msg.sender][token]
108: totals[token]
109: balances[msg.sender][token]
112: totals[token]
114: caps[token]
114: totals[token]
114: caps[token]
118: balances[msg.sender][token]
124: balances[msg.sender][token]
125: balances[msg.sender][token]
126: totals[token]
127: totals[token]
133: balances[msg.sender][token]
134: balances[msg.sender][token]
135: totals[token]
136: totals[token]
176: supportedTokens[token]
186: caps[token]
206: supportedTokens[token]
```
[105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L105) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L106) | [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L108) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L109) | [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L112) | [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114) | [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114) | [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L118) | [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L124) | [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L125) | [126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L126) | [127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L127) | [133](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L133) | [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L134) | [135](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L135) | [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L136) | [176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L176) | [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L186) | [206](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L206)

```solidity
File: src/blast/BlastOnboardingBoot.sol

79: claimed[user]
```
[79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L79)

```solidity
File: src/blast/BlastTokenRegistry.sol

19: nativeYieldTokens[token]
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L19)

```solidity
File: src/mimswap/periphery/Factory.sol

54: pools[token0][token1]
54: pools[token0]
58: userPools[creator]
127: pools[baseToken][quoteToken]
127: pools[baseToken]
128: _pools[poolIndex]
129: userPools[creator]
131: _pools[poolIndex]
134: _userPools[userPoolIndex]
138: _userPools[userPoolIndex]
```
[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L54) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L54) | [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L58) | [127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L127) | [127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L127) | [128](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L128) | [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L129) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L131) | [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L134) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L138)

```solidity
File: src/staking/LockingMultiRewards.sol

200: _rewardData[token]
204: _rewardData[rewardToken]
212: _balances[user]
216: _userRewardLock[user]
220: _userLocks[user]
224: _userLocks[user]
228: _balances[user]
232: _balances[user]
240: _balances[user]
270: _rewardData[rewardToken]
279: _rewardData[rewardToken]
282: _rewardData[rewardToken]
283: _rewardData[rewardToken]
285: _rewardData[rewardToken]
305: _rewardData[rewardToken]
314: _rewardData[rewardToken]
362: _rewardData[rewardToken]
369: _rewardData[rewardToken]
```
[200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L200) | [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L204) | [212](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L212) | [216](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L216) | [220](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L220) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L224) | [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L228) | [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L232) | [240](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L240) | [270](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L270) | [279](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L279) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L282) | [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283) | [285](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L285) | [305](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L305) | [314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L314) | [362](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L362) | [369](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L369)
</details>

### [L-16] Consider checking that transfer to `address(this)` is disabled

Functions allowing users to specify the receiving address should check whether the referenced address is not `address(this)`.

This would prevent tokens to remain lock inside the contract due to an incorrect `transfer` or `mint`.

<details>
<summary><i>2 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

406: _mint(to, shares)
598: super._mint(to, amount)
```
[406](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L406) | [598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L598)
</details>

### [L-17] Prevent Division by Zero

On several locations in the code, precautions are not being taken for not dividing by 0. This will revert the code.
These functions can be called with a 0 value in the input, this value is not checked for being bigger than 0,
that means in some scenarios this can potentially trigger a division by zero.

<details>
<summary><i>22 issue instances in 7 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit totalLockd - can be zero
163: return (userLocked * totalPoolShares) / totalLocked;
```
[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L163)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit totalShars - can be zero
435: baseAmount = (baseBalance * shareAmount) / totalShares;
/// @audit totalShars - can be zero
436: quoteAmount = (quoteBalance * shareAmount) / totalShares;
/// @audit uint256 - can be zero
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
/// @audit uint256 - can be zero
517: _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
```
[435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L435) | [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L436) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

/// @audit d - can be zero
32: return (target * ONE) / d;
/// @audit targt - can be zero
40: return ONE2 / target;
```
[32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L32) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L40)

```solidity
File: src/mimswap/libraries/Math.sol

/// @audit b - can be zero
20: uint256 quotient = a / b;
/// @audit z - can be zero
34: z = (x / z + z) / 2;
/// @audit DcimalMath - can be zero
59: return fairAmount / DecimalMath.ONE;
/// @audit DcimalMath - can be zero
64: return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;
/// @audit ki - can be zero
96: } else if ((ki * delta) / ki == delta) {
/// @audit idlta - can be zero
155: } else if ((idelta * V1) / idelta == V1) {
/// @audit tmp - can be zero
160: return (V1 * temp) / (temp + DecimalMath.ONE);
/// @audit DcimalMath - can be zero
181: bAbs = bAbs / DecimalMath.ONE;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L20) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L59) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L96) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L155) | [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L160) | [181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L181)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

/// @audit stat - can be zero
205: uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);
/// @audit stat - can be zero
209: uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
```
[205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205) | [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit totalShars - can be zero
257: baseAmountOut = (baseBalance * sharesIn) / totalShares;
/// @audit totalShars - can be zero
258: quoteAmountOut = (quoteBalance * sharesIn) / totalShares;
```
[257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L257) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L258)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit rwardsDuration - can be zero
258: return (block.timestamp / rewardsDuration) * rewardsDuration;
/// @audit totalSupply - can be zero
283: uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
/// @audit rmainingRwardTim - can be zero
388: reward.rewardRate = amount / _remainingRewardTime;
```
[258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L258) | [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283) | [388](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L388)
</details>

### [L-18] Usage of Deprecated `latestAnswer()` Function

The function `latestAnswer` has been deprecated and is now considered unsafe to use.
It is recommended to use `latestRoundData` function instead.
The deprecated `latestAnswer` function returns zero if it fails to fetch data.
This can occur if the API, such as ChainLink, which the function depends on, discontinues its support.
As the `latestAnswer` function and its deprecation message have even been removed from the ChainLink website, the continued usage of this function in the contract poses a significant risk.

<details>
<summary><i>2 issue instances in 1 files:</i></summary>

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

38: uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
39: uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L38) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L39)
</details>

### [L-19] Solidity version 0.8.20 may not work on other chains due to `PUSH0`

Solidity 0.8.20, by default, targets the Shanghai version of the EVM, which includes the new `PUSH0` opcode.
However, this opcode may not yet be implemented on all Layer-2 chains.
For instance Arbitrum does not yet support `PUSH0`. See [Documentation](https://developer.arbitrum.io/solidity-support) for more information.
As such, deploying contracts compiled with Solidity 0.8.20 on these chains could lead to failures.

To avoid this, consider specifying an older EVM version as the target, or ensure that the Layer-2 chain used supports the Shanghai EVM.

<details>
<summary><i>20 issue instances in 20 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2)

```solidity
File: src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L3)

```solidity
File: src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L2)

```solidity
File: src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L3)

```solidity
File: src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L2)

```solidity
File: src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L2)

```solidity
File: src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L2)

```solidity
File: src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L2)

```solidity
File: src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L2)

```solidity
File: src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L2)

```solidity
File: src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L7)

```solidity
File: src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L8)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L8)

```solidity
File: src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L2)

```solidity
File: src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L2)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L2)

```solidity
File: src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L2)
</details>

### [L-20] Initializer missing `address(0)` Check before assignment

The initializer does not include a check for `address(0)` when initializing state variables that hold addresses.
Initializing a state variable with `address(0)` can lead to unintended behavior and vulnerabilities in the contract, 
such as sending funds to an inaccessible address. 
It is recommended to include a validation step to ensure that address parameters are not set to `address(0)`.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit `_router` has lack of `address(0)` check before use
128: function initialize(Router _router) external onlyOwner {
```
[128](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L128)
</details>

### [L-21] Missing checks for `address(0x0)` when updating address state variables

State variables that are of type `address` should always be checked to ensure that they are not being assigned the null address (address(0x0)).
A null address often implies an error or omission in the code.
Without proper checks, such a scenario can lead to unexpected behavior and potential vulnerabilities in the smart contract.
Therefore, it is considered good practice to implement checks for `address(0x0)` prior to assigning new values to address state variables.

<details>
<summary><i>8 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

191: bootstrapper = bootstrapper_;
196: state = State.Opened;
201: state = State.Closed;
```
[191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L191) | [196](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L196) | [201](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L201)

```solidity
File: src/blast/BlastOnboardingBoot.sol

117: staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
130: router = Router(payable(_router));
131: factory = IFactory(router.factory());
142: staking = _staking;
```
[117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117) | [130](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L130) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L131) | [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L142)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

58: implementation = implementation_;
```
[58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L58)
</details>

### [L-22] Risk of Renouncing Ownership While System is Paused

If the owner or a role-holder renounce or loses their role/ownership while the system is paused, it can lead to user assets becoming permanently locked.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

213: function pause() external onlyOwner {
```
[213](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L213)

```solidity
File: src/staking/LockingMultiRewards.sol

337: function pause() external onlyOwner {
```
[337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337)
</details>

### [L-23] Input Validation Missing in Setter Functions

Setter functions are utilized to update the state variables of a contract.
It is critical to ensure these functions have adequate input sanitization to prevent unwanted alterations or malicious attacks.
Without input validation, there's a potential risk of enabling vulnerabilities like overflow/underflow, unauthorized access, or insertion of invalid data.
Consider incorporating appropriate validation mechanisms, such as checking the range or type of inputs, to enhance the security of your contract.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit `setReady` function does not validate `_ready` input
145: function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
```
[145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L145)
</details>

### [L-24] Avoid using `tx.origin`

The use of `tx.origin` can potentially make a contract vulnerable if an authorized account calls a malicious contract.

It is recommended to avoid using `tx.origin` as it can lead to easier impersonation of users via third party contracts.

<details>
<summary><i>5 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

250: (receiveQuoteAmount, mtFee, newRState, newBaseTarget) = querySellBase(tx.origin, baseInput);
273: (receiveBaseAmount, mtFee, newRState, newQuoteTarget) = querySellQuote(tx.origin, quoteInput);
311: tx.origin,
333: tx.origin,
```
[250](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L250) | [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L273) | [311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L311) | [333](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L333)

```solidity
File: src/mimswap/periphery/Factory.sol

82: address creator = tx.origin;
```
[82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L82)
</details>

### [L-25] Unhandled Zero `totalSupply` Division Case

The code may encounter a division by zero error if the `totalSupply` is zero.

It is important to consider and handle this edge case properly to prevent any possible disruption to contract functionality.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

45: return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45)

```solidity
File: src/staking/LockingMultiRewards.sol

283: uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
```
[283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283)
</details>

### [L-26] Large approvals may not work with some ERC20 tokens

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

122: pool.safeApprove(address(staking), totalPoolShares);
```
[122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L122)
</details>

### [L-27] Lack of Parameter Validation in Constructor/Initializer

The constructor/initializer doesn't validate input parameters before assigning them to state variables.
It is crucial to ensure that input parameters meet certain conditions to avoid unexpected states or behaviors in the contract.
Consider adding appropriate checks or constraints.

<details>
<summary><i>3 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

/// @audit `weth_` passed to inherited constructor is not validated
24: constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24)

```solidity
File: src/blast/BlastWrappers.sol

/// @audit `weth_` passed to inherited constructor is not validated
/// @audit `factory` passed to inherited constructor is not validated
20: constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

/// @audit `pair_` is not validated before use
/// @audit `pair_` is not validated before use
/// @audit `pair_` is not validated before use
/// @audit `baseOracle_` is not validated before use
/// @audit `quoteOracle_` is not validated before use
21: constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21)
</details>

### [L-28] Mint to zero address

Minting tokens to the zero address should be avoided. In several locations in the code, precautions are not being taken to prevent minting to the zero address. This may lead to unintended consequences.
Consider applying checks in the minting functions to ensure tokens are not minted to the zero address.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

592: function _mint(address to, uint256 amount) internal override {
```
[592](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L592)
</details>

### [L-29] State variables are not limited to a reasonable range

It's advisable to introduce minimum and maximum value constraints for state variables.
By not setting bounds, there's a potential for users to face adverse effects, including potential griefing attacks.
Ensuring that state variables operate within a known range can enhance safety and predictability.

<details>
<summary><i>5 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

186: caps[token] = cap;
```
[186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L186)

```solidity
File: src/mimswap/MagicLP.sol

561: _BASE_RESERVE_ = baseReserve.toUint112();
562: _QUOTE_RESERVE_ = quoteReserve.toUint112();
```
[561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L561) | [562](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L562)

```solidity
File: src/mimswap/libraries/Math.sol

31: y = x;
```
[31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L31)

```solidity
File: src/mimswap/periphery/Router.sol

101: shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
```
[101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L101)
</details>

### [L-30] Missing Contract-Existence Checks Before Low-Level Calls

When making low-level calls, it's crucial to ensure the existence of the contract at the specified address. 
If the contract doesn't exist at the given address, low-level calls will still return success, potentially causing errors in the code execution.
Therefore, alongside zero-address checks, adding an additional check to verify that <address>.code.length > 0 before making low-level calls would be recommended.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastGovernor.sol

54: (success, result) = to.call{value: value}(data);
```
[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L54)
</details>

### [L-31] Events may be emitted out of order due to reentrancy

It's essential to ensure that events follow the best practice of check-effects-interaction and are emitted before any external calls to prevent out-of-order events due to reentrancy.
Emitting events post external interactions may cause them to be out of order due to reentrancy, which can be misleading or erroneous for event listeners.
[Refer to the Solidity Documentation for best practices.](https://solidity.readthedocs.io/en/latest/security-considerations.html#reentrancy)

<details>
<summary><i>10 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit `safeTransferFrom()` before `LogDeposit` event emit
119: emit LogDeposit(msg.sender, token, amount, lock_);
/// @audit `safeTransfer()` before `LogWithdraw` event emit
139: emit LogWithdraw(msg.sender, token, amount);
/// @audit `safeTransfer()` before `LogTokenRescue` event emit
211: emit LogTokenRescue(token, to, amount);
```
[119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L119) | [139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L139) | [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L211)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit `safeTransfer()` before `TokenRescue` event emit
467: emit TokenRescue(token, to, amount);
```
[467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L467)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit `safeTransfer()` before `LogWithdrawn` event emit
182: emit LogWithdrawn(msg.sender, amount);
/// @audit `safeTransfer()` before `LogRecovered` event emit
331: emit LogRecovered(tokenAddress, tokenAmount);
/// @audit `safeTransferFrom()` before `LogRewardAdded` event emit
391: emit LogRewardAdded(amount);
/// @audit `safeTransferFrom()` before `LogStaked` event emit
474: emit LogStaked(account, amount);
/// @audit `safeTransfer()` before `LogRewardPaid` event emit
638: emit LogRewardPaid(user, rewardToken, amount);
/// @audit `safeTransfer()` before `LogRewardLocked` event emit
650: emit LogRewardLocked(user, rewardToken, rewardAmount);
```
[182](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L182) | [331](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L331) | [391](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L391) | [474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L474) | [638](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L638) | [650](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L650)
</details>

### [L-32] External calls in an un-bounded `for-`loop may result in a revert

Executing external calls within unbounded for-loops poses a significant risk of transaction revert.
A failure in one of the iterations can lead to the entire transaction being reverted.
Furthermore, excessive iterations may consume an exorbitant amount of gas, potentially reaching the block gas limit, causing the transaction to fail.
This can result in unintended outcomes, especially if a majority of the iterations would have otherwise succeeded without the problematic call.
To enhance contract reliability and manage gas consumption efficiently, consider limiting the number of iterations in such loops, and implement robust error-handling mechanisms for potential failures in the looped external calls.

<details>
<summary><i>5 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit 2 external calls in unbounded for-loop -> 165: for (uint256 i = 0; i < tokens.length; i++) {
169: if (registry.nativeYieldTokens(tokens[i])) {
170: BlastYields.claimAllTokenYields(tokens[i], feeTo);
```
[169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L169) | [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L170)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit 2 external calls in unbounded for-loop -> 544: for (uint256 i = 0; i < iterations; ) {
547: IMagicLP(path[i]).sellBase(address(path[i + 1]));
550: IMagicLP(path[i]).sellQuote(address(path[i + 1]));
```
[547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L547) | [550](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L550)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit 1 external calls in unbounded for-loop -> 614: for (uint256 i; i < rewardTokens.length; ) {
637: rewardToken.safeTransfer(user, amount);
```
[637](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L637)
</details>

### [L-33] Critical functions should be a two step procedure

Critical functions in Solidity contracts should follow a two-step procedure to enhance security, minimize human error, and ensure proper access control. By dividing sensitive operations into distinct phases, such as initiation and confirmation, developers can introduce a safeguard against unintended actions or unauthorized access.

<details>
<summary><i>18 issue instances in 10 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

71: function setFeeTo(address feeTo_) external onlyOwner {
80: function setTokenEnabled(address token, bool enabled) external onlyOwner {
```
[71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L71) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L80)

```solidity
File: src/blast/BlastGovernor.sol

39: function setFeeTo(address _feeTo) external onlyOwner {
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L39)

```solidity
File: src/blast/BlastMagicLP.sol

79: function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
88: function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```
[79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L79) | [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L88)

```solidity
File: src/blast/BlastOnboarding.sol

146: function setFeeTo(address feeTo_) external onlyOwner {
174: function setTokenSupported(address token, bool supported) external onlyOwner {
184: function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
189: function setBootstrapper(address bootstrapper_) external onlyOwner {
```
[146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L146) | [174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L174) | [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L184) | [189](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L189)

```solidity
File: src/blast/BlastOnboardingBoot.sol

137: function setStaking(LockingMultiRewards _staking) external onlyOwner {
145: function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
```
[137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137) | [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L145)

```solidity
File: src/blast/BlastTokenRegistry.sol

13: function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L13)

```solidity
File: src/mimswap/MagicLP.sol

469: function setParameters(
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
[469](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L469)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

45: function setMaintainer(address maintainer_) external onlyOwner {
57: function setImplementation(address implementation_) public onlyOwner {
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L45) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)

```solidity
File: src/mimswap/periphery/Factory.sol

95: function setLpImplementation(address implementation_) external onlyOwner {
104: function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
```
[95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L95) | [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L104)

```solidity
File: src/staking/LockingMultiRewards.sol

316: function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
```
[316](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L316)
</details>

### [L-34] Upper Limits for Fees/Rates Should Be Implemented

It is critical for the functionality and reliability of a smart contract that any fees or rates are constrained to a sensible range, preferably significantly below 100%.
Such a limitation prevents excessive charges and protects users from unpredictable fee fluctuations.
This measure also enhances the user experience, as they can interact with the protocol without the necessity to constantly check the blockchain for any abrupt changes in fees or rates.

<details>
<summary><i>10 issue instances in 7 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

33: feeTo = feeTo_;
```
[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L33)

```solidity
File: src/blast/BlastGovernor.sol

20: feeTo = feeTo_;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L20)

```solidity
File: src/blast/BlastMagicLP.sol

32: feeTo = feeTo_;
```
[32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L32)

```solidity
File: src/blast/BlastOnboarding.sol

94: feeTo = feeTo_;
```
[94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L94)

```solidity
File: src/blast/BlastOnboardingBoot.sol

15: uint256 constant FEE_RATE = 0.0005 ether; // 0.05%
```
[15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L15)

```solidity
File: src/mimswap/MagicLP.sol

65: uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%
66: uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%
124: _MT_FEE_RATE_MODEL_ = IFeeRateModel(mtFeeRateModel);
123: _LP_FEE_RATE_ = lpFeeRate;
```
[65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L65) | [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L66) | [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L124) | [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L123)

```solidity
File: src/mimswap/periphery/Factory.sol

46: maintainerFeeRateModel = maintainerFeeRateModel_;
```
[46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L46)
</details>

### [L-35] Deprecated Function `safeApprove` Usage

The function `safeApprove` has been deprecated and is not recommended for use. The preferred methods are `increaseAllowance` and `decreaseAllowance`. 

The `safeApprove` method should only be used for setting an initial value. Instead of `safeApprove`, using the `increaseAllowance` and `decreaseAllowance` functions is recommended, as they offer a more secure and efficient way to manage allowances.

<details>
<summary><i>3 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

103: MIM.safeApprove(address(router), type(uint256).max);
104: USDB.safeApprove(address(router), type(uint256).max);
122: pool.safeApprove(address(staking), totalPoolShares);
```
[103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L103) | [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L104) | [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L122)
</details>

### [L-36] Implement two-step ownership transfers

Single-step ownership transfers can be risky due to the potential for errors or wrong address inputs.
In worst-case scenarios, your contract could become `ownerless`.
To mitigate these risks, consider using a two-step ownership transfers.
In this process, a new potential owner is first designated, and then they must accept the ownership to complete the transfer.
This two-step procedure ensures a more secure and reliable transfer of contract ownership.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

119: staking.transferOwnership(owner);
```
[119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L119)
</details>

### [L-37] Loss of precision

Division by large numbers may result in the result being zero, due to Solidity not supporting fractions. Consider requiring a minimum amount for the numerator to ensure that it is always larger than the denominator.

<details>
<summary><i>40 issue instances in 8 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

163: return (userLocked * totalPoolShares) / totalLocked;
```
[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L163)

```solidity
File: src/mimswap/MagicLP.sol

435: baseAmount = (baseBalance * shareAmount) / totalShares;
436: quoteAmount = (quoteBalance * shareAmount) / totalShares;
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
517: _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
```
[435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L435) | [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L436) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

24: return (target * d) / ONE;
32: return (target * ONE) / d;
40: return ONE2 / target;
53: uint p = powFloor(target, e / 2);
54: p = (p * p) / ONE;
56: p = (p * target) / ONE;
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L24) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L32) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L40) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L53) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L54) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L56)

```solidity
File: src/mimswap/libraries/Math.sol

20: uint256 quotient = a / b;
30: uint256 z = x / 2 + 1;
34: z = (x / z + z) / 2;
34: z = (x / z + z) / 2;
59: return fairAmount / DecimalMath.ONE;
62: uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);
64: return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;
96: } else if ((ki * delta) / ki == delta) {
97: _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);
99: _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);
155: } else if ((idelta * V1) / idelta == V1) {
156: temp = (idelta * V1) / (V0 * V0);
158: temp = (((delta * V1) / V0) * i) / V0;
158: temp = (((delta * V1) / V0) * i) / V0;
160: return (V1 * temp) / (temp + DecimalMath.ONE);
170: uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
181: bAbs = bAbs / DecimalMath.ONE;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L20) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L30) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L59) | [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L96) | [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L97) | [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L99) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L155) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L156) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158) | [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L160) | [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170) | [181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L181)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

205: uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);
209: uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
```
[205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205) | [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209)

```solidity
File: src/mimswap/periphery/Router.sol

257: baseAmountOut = (baseBalance * sharesIn) / totalShares;
258: quoteAmountOut = (quoteBalance * sharesIn) / totalShares;
```
[257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L257) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L258)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

45: return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45)

```solidity
File: src/staking/LockingMultiRewards.sol

144: maxLocks = _lockDuration / _rewardsDuration;
236: return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);
241: return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);
258: return (block.timestamp / rewardsDuration) * rewardsDuration;
283: uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
294: return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];
388: reward.rewardRate = amount / _remainingRewardTime;
```
[144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L144) | [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L236) | [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L241) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L258) | [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283) | [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294) | [388](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L388)
</details>

### [L-38] Array is `push()`ed but not `pop()`ed

Arrays in the contract have entries added using the `push` method, but no corresponding `pop` method is found to remove them. 
Ensure to consider whether old entries need to be removed or if there should be a maximum array length.
Cases with specific potential issues might be reported separately under different issue categories.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/staking/LockingMultiRewards.sol

313: rewardTokens.push(rewardToken);
```
[313](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L313)
</details>

### [L-39] Mapping arrays can grow in size without a way to shrink them

In Solidity, it's vital to manage the size of mapping arrays, particularly when they are subject to dynamic updates.
A common issue arises when contracts allow items to be added to an array but lack a corresponding method to remove them.
Unlike some programming languages where arrays automatically resize, Solidity requires explicit resizing. Without a 'pop' function or similar mechanism, arrays can become bloated, leading to inefficiencies.
This bloating can not only increase gas costs, particularly during iterations, but also pose a risk of hitting the block gas limit.
Furthermore, if array elements are flagged for deletion but not actually removed, it can result in the retention of outdated or irrelevant data, potentially causing logical errors in contract execution. To maintain a streamlined and efficient contract, it's advisable to implement methods for removing items from mapping arrays.
Such practices help in keeping the contract's state manageable and guard against issues related to gas limits or data accuracy.
Additionally, it's crucial to handle underflows carefully when implementing removal logic to ensure the contract's robustness.

<details>
<summary><i>2 issue instances in 1 files:</i></summary>

```solidity
File: src/staking/LockingMultiRewards.sol

501: _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));
648: _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
```
[501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L501) | [648](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L648)
</details>

### [L-40] Unbounded Gas Consumption on External Calls

External calls in your code don't specify a gas limit, which can lead to scenarios where the recipient consumes all transaction's gas causing it to revert. 
Consider using `addr.call{gas: <amount>}("")` to set a gas limit and prevent potential reversion due to gas consumption.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastGovernor.sol

54: (success, result) = to.call{value: value}(data);
```
[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L54)
</details>

### [L-41] Unsafe downcast from larger to smaller integer types

Casting from larger types to smaller ones can potentially lead to overflows and thus unexpected behavior.
For instance, when a `uint256` value gets cast to `uint8`, it could end up as an entirely different, much smaller number due to the reduction in bits. 

OpenZeppelin's `SafeCast` library provides functions for safe type conversions, throwing an error whenever an overflow would occur.
It is generally recommended to use `SafeCast` or similar protective measures when performing type conversions to ensure the accuracy of your computations and the security of your contracts.

<details>
<summary><i>14 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

/// @audit casted from `uint256` to `uint112`
438: _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
/// @audit casted from `uint256` to `uint112`
439: _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
/// @audit cast from `uint256` to `uint64`
493: _LP_FEE_RATE_ = uint64(newLpFeeRate);
/// @audit cast from `uint256` to `uint64`
494: _K_ = uint64(newK);
/// @audit cast from `uint256` to `uint128`
495: _I_ = uint128(newI);
/// @audit casted from `uint256` to `uint112`
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
/// @audit cast from `uint256` to `uint112`
514: _BASE_RESERVE_ = uint112(baseBalance);
/// @audit casted from `uint256` to `uint112`
517: _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
/// @audit cast from `uint256` to `uint112`
518: _QUOTE_RESERVE_ = uint112(quoteBalance);
/// @audit cast from `uint256` to `uint112`
536: _BASE_RESERVE_ = uint112(baseBalance);
/// @audit cast from `uint256` to `uint112`
537: _QUOTE_RESERVE_ = uint112(quoteBalance);
/// @audit cast from `uint256` to `uint112`
538: _BASE_TARGET_ = uint112(baseBalance);
/// @audit cast from `uint256` to `uint112`
539: _QUOTE_TARGET_ = uint112(quoteBalance);
```
[438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439) | [493](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L493) | [494](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L494) | [495](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L495) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [514](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L514) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517) | [518](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L518) | [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L536) | [537](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L537) | [538](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L538) | [539](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L539)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit cast from `uint256` to `uint248`
533: _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow
```
[533](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L533)
</details>

### [L-42] Consider implementing two-step procedure for updating protocol addresses

Direct state address changes in a function can be risky, as they don't allow for a verification step before the change is made.
It's safer to implement a two-step process where the new address is first proposed, then later confirmed, allowing for more control and the chance to catch errors or malicious activity.

<details>
<summary><i>24 issue instances in 11 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

/// @audit `feeTo` is changed
76: feeTo = feeTo_;
/// @audit `enabledTokens[token]` is changed
82: enabledTokens[token] = enabled;
```
[76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L76) | [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L82)

```solidity
File: src/blast/BlastGovernor.sol

/// @audit `feeTo` is changed
44: feeTo = _feeTo;
```
[44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L44)

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit `feeTo` is changed
84: feeTo = feeTo_;
/// @audit `operators[operator]` is changed
90: operators[operator] = status;
```
[84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L84) | [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L90)

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit `feeTo` is changed
151: feeTo = feeTo_;
/// @audit `supportedTokens[token]` is changed
176: supportedTokens[token] = supported;
/// @audit `caps[token]` is changed
186: caps[token] = cap;
/// @audit `bootstrapper` is changed
191: bootstrapper = bootstrapper_;
```
[151](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L151) | [176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L176) | [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L186) | [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L191)

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit `staking` is changed
141: staking = _staking;
```
[141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L141)

```solidity
File: src/blast/BlastTokenRegistry.sol

/// @audit `nativeYieldTokens[token]` is changed
18: nativeYieldTokens[token] = enabled;
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L18)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit `_QUOTE_RESERVE_` is changed
562: _QUOTE_RESERVE_ = quoteReserve.toUint112();
```
[562](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L562)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit `maintainer` is changed
50: maintainer = maintainer_;
/// @audit `implementation` is changed
58: implementation = implementation_;
```
[50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L50) | [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L58)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit `implementation` is changed
100: implementation = implementation_;
/// @audit `maintainerFeeRateModel` is changed
109: maintainerFeeRateModel = maintainerFeeRateModel_;
```
[100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L100) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L109)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit `shares` is changed
101: shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
/// @audit `baseAdjustedInAmount` is changed
151: baseAdjustedInAmount = baseInAmount;
/// @audit `quoteAdjustedInAmount` is changed
155: quoteAdjustedInAmount = quoteInAmount;
/// @audit `baseAdjustedInAmount` is changed
531: baseAdjustedInAmount = baseInAmount;
/// @audit `quoteAdjustedInAmount` is changed
534: quoteAdjustedInAmount = quoteInAmount;
```
[101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L101) | [151](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L151) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L155) | [531](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L531) | [534](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L534)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit `update` is changed
402: _updateRewardsForUsers(users);
/// @audit `update` is changed
467: _updateRewardsForUser(account);
/// @audit `userRewardPerTokenPaid[user_][token_]` is changed
538: userRewardPerTokenPaid[user_][token_] = rewardPerToken_;
```
[402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L402) | [467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L467) | [538](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L538)
</details>

### [L-43] Possible Revert ERC20 Transfers with Zero Value

Some ERC20 tokens (for example, LEND) revert on attempts to transfer a zero value.
This can become a problem in any contract that doesn't handle these cases correctly.

If a token transfer fails, any additional logic in a function might also be affected or even fail entirely.
Therefore, contracts interacting with ERC20 tokens should account for the possibility that a zero-value transfer might revert.

<details>
<summary><i>14 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit `amount` has not been checked for zero value before transfer
102: token.safeTransferFrom(msg.sender, address(this), amount);
/// @audit `amount` has not been checked for zero value before transfer
138: token.safeTransfer(msg.sender, amount);
/// @audit `amount` has not been checked for zero value before transfer
210: token.safeTransfer(to, amount);
```
[102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L102) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L138) | [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L210)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit `amount` has not been checked for zero value before transfer
466: token.safeTransfer(to, amount);
```
[466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L466)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit `baseInAmount` has not been checked for zero value before transfer
68: baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);
/// @audit `quoteInAmount` has not been checked for zero value before transfer
69: quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);
/// @audit `tokenInAmount` has not been checked for zero value before transfer
91: token.safeTransferFrom(msg.sender, clone, tokenInAmount);
/// @audit `baseAdjustedInAmount` has not been checked for zero value before transfer
172: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);
/// @audit `quoteAdjustedInAmount` has not been checked for zero value before transfer
173: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);
/// @audit `quoteInAmount` has not been checked for zero value before transfer
187: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);
/// @audit `tokenAdjustedAmount` has not been checked for zero value before transfer
224: token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);
/// @audit `sharesIn` has not been checked for zero value before transfer
269: lp.safeTransferFrom(msg.sender, address(this), sharesIn);
/// @audit `sharesIn` has not been checked for zero value before transfer
282: lp.safeTransferFrom(msg.sender, address(this), sharesIn);
/// @audit `amountIn` has not been checked for zero value before transfer
328: IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
```
[68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L68) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L69) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L91) | [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L172) | [173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L173) | [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L187) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L224) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L269) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282) | [328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L328)
</details>

### [L-44] Potential Re-org Attack Vector

The contract appears to deploy new contracts using the `new` keyword.
In a re-org attack scenario, such deployments can be exploited by a malicious actor who might rewrite the blockchain's history and deploy the contract at an expected address. 

Consider deploying the contract via `CREATE2` opcode with a specific salt that includes `msg.sender` and the existing contract address.
This will ensure a predictable contract address, reducing the chances of such an attack.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

117: staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
```
[117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117)
</details>

### [L-45] Function Parameters in Public Accessible Functions Need `address(0)` Check

Parameters of type `address` in your functions should be checked to ensure that they are not assigned the null address (`address(0x0)`). 
Failure to validate these parameters can lead to transaction reverts, wasted gas, the need for transaction resubmission, and may even require redeployment of contracts within the protocol in certain situations.
Implement checks for `address(0x0)` to avoid these potential issues.

<details>
<summary><i>70 issue instances in 11 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

/// @audit `token_` parameter without address(0) check
56: function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
/// @audit `token` parameter without address(0) check
81: function setTokenEnabled(address token, bool enabled) external onlyOwner {
```
[56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L56) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81)

```solidity
File: src/blast/BlastGovernor.sol

/// @audit `contractAddress` parameter without address(0) check
28: function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
/// @audit `contractAddress` parameter without address(0) check
32: function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
/// @audit `to` parameter without address(0) check
53: function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```
[28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L28) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L32) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit `operator` parameter without address(0) check
89: function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```
[89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89)

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit `token` parameter without address(0) check
101: function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
/// @audit `token` parameter without address(0) check
123: function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
/// @audit `token` parameter without address(0) check
132: function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
/// @audit `tokens` parameter without address(0) check
164: function claimTokenYields(address[] memory tokens) external onlyOwner {
/// @audit `token` parameter without address(0) check
175: function setTokenSupported(address token, bool supported) external onlyOwner {
/// @audit `token` parameter without address(0) check
185: function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
/// @audit `bootstrapper_` parameter without address(0) check
190: function setBootstrapper(address bootstrapper_) external onlyOwner {
/// @audit `token` parameter without address(0) check
/// @audit `to` parameter without address(0) check
205: function rescue(address token, address to, uint256 amount) external onlyOwner {
```
[101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101) | [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132) | [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164) | [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185) | [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190) | [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L205)

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit `user` parameter without address(0) check
78: function claimable(address user) external view returns (uint256 shares) {
```
[78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L78)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit `trader` parameter without address(0) check
167: function querySellBase(
        address trader,
        uint256 payBaseAmount
    ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {
/// @audit `trader` parameter without address(0) check
180: function querySellQuote(
        address trader,
        uint256 payQuoteAmount
    ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {
/// @audit `user` parameter without address(0) check
224: function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
/// @audit `to` parameter without address(0) check
244: function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {
/// @audit `to` parameter without address(0) check
267: function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {
/// @audit `assetTo` parameter without address(0) check
290: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
/// @audit `to` parameter without address(0) check
360: function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
/// @audit `to` parameter without address(0) check
413: function sellShares(
        uint256 shareAmount,
        address to,
        uint256 baseMinAmount,
        uint256 quoteMinAmount,
        bytes calldata data,
        uint256 deadline
    ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {
/// @audit `token` parameter without address(0) check
/// @audit `to` parameter without address(0) check
461: function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {
/// @audit `assetTo` parameter without address(0) check
470: function setParameters(
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
[167](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L167) | [180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L180) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L224) | [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L244) | [267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L267) | [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360) | [413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L413) | [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L461) | [470](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit `trader` parameter without address(0) check
34: function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
/// @audit `implementation_` parameter without address(0) check
57: function setImplementation(address implementation_) public onlyOwner {
```
[34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

/// @audit `/*pool*/` parameter without address(0) check
/// @audit `/*trader*/` parameter without address(0) check
9: function getFeeRate(
        address /*pool*/,
        address /*trader*/,
        uint256 lpFeeRate
    ) external pure returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit `token0` parameter without address(0) check
/// @audit `token1` parameter without address(0) check
53: function getPoolCount(address token0, address token1) external view returns (uint256) {
/// @audit `creator` parameter without address(0) check
57: function getUserPoolCount(address creator) external view returns (uint256) {
/// @audit `creator` parameter without address(0) check
/// @audit `baseToken_` parameter without address(0) check
/// @audit `quoteToken_` parameter without address(0) check
65: function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address) {
/// @audit `baseToken_` parameter without address(0) check
/// @audit `quoteToken_` parameter without address(0) check
81: function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
/// @audit `creator` parameter without address(0) check
/// @audit `baseToken` parameter without address(0) check
/// @audit `quoteToken` parameter without address(0) check
/// @audit `pool` parameter without address(0) check
116: function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {
/// @audit `creator` parameter without address(0) check
/// @audit `baseToken` parameter without address(0) check
/// @audit `quoteToken` parameter without address(0) check
120: function removePool(
        address creator,
        address baseToken,
        address quoteToken,
        uint256 poolIndex,
        uint256 userPoolIndex
    ) external onlyOwner {
```
[53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L53) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L57) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81) | [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L116) | [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L120)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit `baseToken` parameter without address(0) check
/// @audit `quoteToken` parameter without address(0) check
/// @audit `to` parameter without address(0) check
54: function createPool(
        address baseToken,
        address quoteToken,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external returns (address clone, uint256 shares) {
/// @audit `token` parameter without address(0) check
/// @audit `to` parameter without address(0) check
73: function createPoolETH(
        address token,
        bool useTokenAsQuote,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 tokenInAmount
    ) external payable returns (address clone, uint256 shares) {
/// @audit `lp` parameter without address(0) check
112: function previewAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
162: function addLiquidity(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
178: function addLiquidityUnsafe(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 shares) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
/// @audit `refundTo` parameter without address(0) check
192: function addLiquidityETH(
        address lp,
        address to,
        address payable refundTo,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
229: function addLiquidityETHUnsafe(
        address lp,
        address to,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 shares) {
/// @audit `lp` parameter without address(0) check
251: function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
261: function removeLiquidity(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumBaseAmount,
        uint256 minimumQuoteAmount,
        uint256 deadline
    ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
274: function removeLiquidityETH(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumETHAmount,
        uint256 minimumTokenAmount,
        uint256 deadline
    ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {
/// @audit `to` parameter without address(0) check
/// @audit `path` parameter without address(0) check
314: function swapTokensForTokens(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit `to` parameter without address(0) check
/// @audit `path` parameter without address(0) check
336: function swapETHForTokens(
        address to,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit `to` parameter without address(0) check
/// @audit `path` parameter without address(0) check
365: function swapTokensForETH(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
404: function sellBaseTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
415: function sellBaseETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
432: function sellBaseTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
449: function sellQuoteTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
461: function sellQuoteETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit `lp` parameter without address(0) check
/// @audit `to` parameter without address(0) check
478: function sellQuoteTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
```
[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L54) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L73) | [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L112) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L162) | [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L178) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192) | [229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229) | [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L251) | [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L261) | [274](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L274) | [314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L314) | [336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336) | [365](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L365) | [404](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L404) | [415](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L415) | [432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L432) | [449](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L449) | [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L461) | [478](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L478)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit `token` parameter without address(0) check
199: function rewardData(address token) external view returns (Reward memory) {
/// @audit `rewardToken` parameter without address(0) check
203: function rewardsForDuration(address rewardToken) external view returns (uint256) {
/// @audit `user` parameter without address(0) check
211: function balances(address user) external view returns (Balances memory) {
/// @audit `user` parameter without address(0) check
215: function userRewardLock(address user) external view returns (RewardLock memory) {
/// @audit `user` parameter without address(0) check
219: function userLocks(address user) external view returns (LockedBalance[] memory) {
/// @audit `user` parameter without address(0) check
223: function userLocksLength(address user) external view returns (uint256) {
/// @audit `user` parameter without address(0) check
227: function locked(address user) external view returns (uint256) {
/// @audit `user` parameter without address(0) check
231: function unlocked(address user) external view returns (uint256) {
/// @audit `user` parameter without address(0) check
239: function balanceOf(address user) public view returns (uint256) {
/// @audit `rewardToken` parameter without address(0) check
269: function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {
/// @audit `rewardToken` parameter without address(0) check
273: function rewardPerToken(address rewardToken) public view returns (uint256) {
/// @audit `rewardToken` parameter without address(0) check
277: function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
/// @audit `user` parameter without address(0) check
/// @audit `rewardToken` parameter without address(0) check
288: function earned(address user, address rewardToken) public view returns (uint256) {
/// @audit `tokenAddress` parameter without address(0) check
324: function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {
/// @audit `account` parameter without address(0) check
349: function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {
/// @audit `rewardToken` parameter without address(0) check
361: function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
/// @audit `users` parameter without address(0) check
397: function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
```
[199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L203) | [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L211) | [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L215) | [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L219) | [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L223) | [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L227) | [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L231) | [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L239) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L269) | [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L273) | [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277) | [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L288) | [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L324) | [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L349) | [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361) | [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397)
</details>

### [L-46] Missing `address(0)` Check in Constructor

The constructor does not include a check for `address(0)` when set state variables that hold addresses.
Initializing a state variable with `address(0)` can lead to unintended behavior and vulnerabilities in the contract, such as sending funds to an inaccessible address. 
It is recommended to include a validation step to ensure that address parameters are not set to `address(0)`.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

/// @audit `pair_` has lack of `address(0)` check before use
/// @audit `baseOracle_` has lack of `address(0)` check before use
/// @audit `quoteOracle_` has lack of `address(0)` check before use
21: constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit `_stakingToken` has lack of `address(0)` check before use
112: constructor(
        address _stakingToken,
        uint256 _lockingBoostMultiplerInBips,
        uint256 _rewardsDuration,
        uint256 _lockDuration,
        address _owner
    ) OperatableV2(_owner) {
```
[112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L112)
</details>

### [L-47] Functions calling tokens with transfer hooks are missing reentrancy guards

Functions that call contracts or addresses with transfer hooks should use reentrancy guards for protection. 
Even if these functions adhere to the check-effects-interaction best practice, absence of reentrancy guards can expose the protocol users to read-only reentrancies.
Without the guards, the only protective measure is to block-list the entire protocol, which isn't an optimal solution.

<details>
<summary><i>37 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit function `deposit()` 
102: token.safeTransferFrom(msg.sender, address(this), amount);
/// @audit function `withdraw()` 
138: token.safeTransfer(msg.sender, amount);
/// @audit function `rescue()` 
210: token.safeTransfer(to, amount);
```
[102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L102) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L138) | [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L210)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit function `rescue()` 
466: token.safeTransfer(to, amount);
/// @audit function `_transferBaseOut()` 
583: _BASE_TOKEN_.safeTransfer(to, amount);
/// @audit function `_transferQuoteOut()` 
589: _QUOTE_TOKEN_.safeTransfer(to, amount);
```
[466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L466) | [583](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L583) | [589](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L589)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit function `createPool()` 
68: baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);
/// @audit function `createPool()` 
69: quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);
/// @audit function `createPoolETH()` 
91: token.safeTransferFrom(msg.sender, clone, tokenInAmount);
/// @audit function `createPoolETH()` 
92: address(weth).safeTransferFrom(address(this), clone, msg.value);
/// @audit function `addLiquidity()` 
172: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);
/// @audit function `addLiquidity()` 
173: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);
/// @audit function `addLiquidityUnsafe()` 
186: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);
/// @audit function `addLiquidityUnsafe()` 
187: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);
/// @audit function `addLiquidityETH()` 
217: address(weth).safeTransfer(lp, wethAdjustedAmount);
/// @audit function `addLiquidityETH()` 
224: token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);
/// @audit function `addLiquidityETHUnsafe()` 
244: address(weth).safeTransfer(lp, msg.value);
/// @audit function `addLiquidityETHUnsafe()` 
246: token.safeTransferFrom(msg.sender, lp, tokenInAmount);
/// @audit function `removeLiquidity()` 
269: lp.safeTransferFrom(msg.sender, address(this), sharesIn);
/// @audit function `removeLiquidityETH()` 
282: lp.safeTransferFrom(msg.sender, address(this), sharesIn);
/// @audit function `removeLiquidityETH()` 
311: token.safeTransfer(to, tokenAmountOut);
/// @audit function `swapTokensForTokens()` 
328: IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
/// @audit function `swapTokensForTokens()` 
330: IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
/// @audit function `swapETHForTokens()` 
360: inToken.safeTransfer(address(firstLp), msg.value);
/// @audit function `swapTokensForETH()` 
393: IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
/// @audit function `swapTokensForETH()` 
395: IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
/// @audit function `sellBaseTokensForTokens()` 
411: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
/// @audit function `sellBaseETHForTokens()` 
428: baseToken.safeTransfer(lp, msg.value);
/// @audit function `sellBaseTokensForETH()` 
443: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
/// @audit function `sellQuoteTokensForTokens()` 
456: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
/// @audit function `sellQuoteETHForTokens()` 
474: quoteToken.safeTransfer(lp, msg.value);
/// @audit function `sellQuoteTokensForETH()` 
489: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
```
[68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L68) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L69) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L91) | [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92) | [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L172) | [173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L173) | [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L186) | [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L187) | [217](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L217) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L224) | [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L244) | [246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L246) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L269) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282) | [311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L311) | [328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L328) | [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L330) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L360) | [393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L393) | [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L395) | [411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L411) | [428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L428) | [443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L443) | [456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L456) | [474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L474) | [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L489)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit function `withdraw()` 
180: stakingToken.safeTransfer(msg.sender, amount);
/// @audit function `recover()` 
330: tokenAddress.safeTransfer(owner, tokenAmount);
/// @audit function `notifyRewardAmount()` 
367: rewardToken.safeTransferFrom(msg.sender, address(this), amount);
/// @audit function `_stakeFor()` 
464: stakingToken.safeTransferFrom(msg.sender, address(this), amount);
/// @audit function `_getRewards()` 
637: rewardToken.safeTransfer(user, amount);
```
[180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L180) | [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L330) | [367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367) | [464](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L464) | [637](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L637)
</details>

### [L-48] Casting `block.timestamp` to Smaller Integer Types Limit Contract Lifespan

Casting `block.timestamp` to a smaller integer type like uint32 can potentially reduce the lifespan of a contract.
While the current Unix timestamp fits within the uint32 range as of now, it will eventually exceed this range by the year 2106.

At this point, casting the Unix timestamp to a uint32 will lead to overflow errors, resulting in unpredictable contract behavior.
To future-proof your contract, it's advisable to use larger integer types such as uint40 or uint (up to uint256) when dealing with timestamps.

<details>
<summary><i>2 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

125: _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);
546: uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
```
[125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L125) | [546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L546)
</details>

### [L-49] Solady/Solmate's SafeTransferLib Doesn't Check Existence of ERC20 Contract

Solady/Solmate's SafeTransferLib, frequently utilized for interaction with non-compliant or unsafe ERC20 tokens, doesn't validate the existence of the ERC20 contract. As such, it can potentially interact with a nonexistent token without reverting.

As per the Solady/Solmate library documentation, there is no check to ensure that the token exists prior to interaction (source: https://github.com/transmissions11/solmate/blob/main/src/utils/SafeTransferLib.sol#L9).

For safer ERC20 token interaction, consider using OpenZeppelin's SafeERC20 library. It checks for token existence before proceeding with any operation, providing a more secure way of handling ERC20 tokens.

<details>
<summary><i>11 issue instances in 5 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

8: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";
65: using SafeTransferLib for address;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L8) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L65)

```solidity
File: src/blast/BlastOnboardingBoot.sol

9: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";
35: using SafeTransferLib for address;
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L9) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L35)

```solidity
File: src/mimswap/MagicLP.sol

12: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";
28: using SafeTransferLib for address;
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L12) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L28)

```solidity
File: src/mimswap/periphery/Router.sol

4: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";
13: using SafeTransferLib for address;
14: using SafeTransferLib for address payable;
```
[4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L4) | [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L14)

```solidity
File: src/staking/LockingMultiRewards.sol

6: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";
15: using SafeTransferLib for address;
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L6) | [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L15)
</details>


## NonCritical Findings Details

### [N-01] `internal/private` Function calls within for loops

Making function calls or external calls within loops in Solidity can lead to inefficient gas usage, potential bottlenecks, and increased vulnerability to attacks.
Each function call or external call consumes gas, and when executed within a loop, the gas cost multiplies, potentially causing the transaction to run out of gas or exceed block gas limits.
This can result in transaction failure or unpredictable behavior.

<details>
<summary><i>10 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/periphery/Router.sol

547: IMagicLP(path[i])
550: IMagicLP(path[i])
```
[547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L547) | [550](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L550)

```solidity
File: src/staking/LockingMultiRewards.sol

548: _updateRewardsGlobal(rewardTokens[i], totalSupply_)
563: _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_))
563: _updateRewardsGlobal(token, totalSupply_)
577: _updateRewardsGlobal(token, totalSupply_)
582: _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_)
582: balanceOf(user)
582: _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_)
582: balanceOf(user)
```
[548](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L548) | [563](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L563) | [563](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L563) | [577](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L577) | [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L582) | [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L582) | [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L582) | [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L582)
</details>

### [N-02] Non-library/interface files should use fixed compiler versions, not floating ones

Floating pragmas may lead to unintended vulnerabilities due to different compiler versions.
It is recommended to lock the Solidity version in pragma statements.

<details>
<summary><i>15 issue instances in 15 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2)

```solidity
File: src/blast/BlastBox.sol

3: pragma solidity >=0.8.0
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L3)

```solidity
File: src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L2)

```solidity
File: src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L3)

```solidity
File: src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L2)

```solidity
File: src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L2)

```solidity
File: src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L2)

```solidity
File: src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L2)

```solidity
File: src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2)

```solidity
File: src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L2)

```solidity
File: src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L2)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L2)

```solidity
File: src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L2)
</details>

### [N-03] Array indices should be referenced via `enum`s rather than via numeric literals

Using constant array indexes can make your Solidity code harder to read and maintain.
To improve clarity, consider using commented enum values in place of constant array indexes.

Enums provide a way to define a type that has a few pre-defined values, making your code more self-explanatory and easy to understand.
This can be particularly helpful in large codebases or when working with a team.

<details>
<summary><i>3 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/periphery/Router.sol

324: path[0]
345: path[0]
389: path[0]
```
[324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L324) | [345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L345) | [389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L389)
</details>

### [N-04] Consider splitting long calculations

For improved readability and maintainability, it's suggested to limit arithmetic operations to 3 per expression.
Excessive operations can convolute the code, making it more prone to errors and more difficult to debug or review.
Splitting operations across multiple lines is often a good approach.
Special care should be taken with division operations. The number of arithmetic operations per line ideally shouldn't exceed three.

<details>
<summary><i>2 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/libraries/Math.sol

64: (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2
158: (((delta * V1) / V0) * i) / V0
```
[64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158)
</details>

### [N-05] Missing Event Emission After Critical Initialize() Function

Emitting an initialization event offers clear, on-chain evidence of the contract's initialization state, enhancing transparency and auditability.
This practice aids users and developers in accurately tracking the contract's lifecycle, pinpointing the precise moment of its initialization.
Moreover, it aligns with best practices for event logging in smart contracts, ensuring that significant state changes are both observable and verifiable through emitted events.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastWrappers.sol

59: function init(bytes calldata data) public payable override
```
[59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59)

```solidity
File: src/mimswap/MagicLP.sol

91: function init(
        address baseTokenAddress,
        address quoteTokenAddress,
        uint256 lpFeeRate,
        address mtFeeRateModel,
        uint256 i,
        uint256 k
    ) external
```
[91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L91)
</details>

### [N-06] Mixed usage of `int/uint` with `int256/uint256`

In Solidity, int256 and uint256 are the preferred type names, especially since they are used for function signatures. Using int or uint instead can lead to confusion and inconsistency.
Suggest replacing them with int256 or uint256 respectively, for better clarity and uniformity in your codebase. 
Improving this aspect of your code can contribute to its readability, understandability, and thus maintainability in the long term.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/libraries/DecimalMath.sol

53: uint p = powFloor(target, e / 2);
```
[53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L53)

```solidity
File: src/staking/LockingMultiRewards.sol

361: function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
```
[361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361)
</details>

### [N-07] Avoid Hard-Coded Addresses

It's often better to declare these addresses as immutable and assign them via constructor arguments.
This approach allows the code to remain consistent across deployments on different networks and avoids recompilation when addresses change.

Refactoring your code in this manner can improve its maintainability and flexibility.

<details>
<summary><i>5 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

13: address constant USDB = 0x4300000000000000000000000000000000000003;
14: address constant MIM = 0x76DA31D7C9CbEAE102aff34D3398bC450c8374c1;
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L14)

```solidity
File: src/blast/libraries/BlastPoints.sol

7: address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;
8: IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L7) | [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L8)

```solidity
File: src/blast/libraries/BlastYields.sol

14: IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L14)
</details>

### [N-08] Variables need not be initialized to zero

By default, `int/uint` variables in Solidity are initialized to `zero`.
Explicitly setting variables to zero during their declaration is redundant and might cause confusion.
Removing the explicit zero initialization can improve code readability and understanding.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

165: for (uint256 i = 0; i < tokens.length; i++) {
```
[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)

```solidity
File: src/mimswap/periphery/Router.sol

544: for (uint256 i = 0; i < iterations; ) {
```
[544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544)
</details>

### [N-09] Multiple `address`/ID mappings can be combined into a single `mapping` of an `address`/ID to a `struct`, for readability

Combining multiple address/ID mappings into a single mapping to a struct can enhance code clarity and maintainability. 
Consider refactoring multiple mappings into a single mapping with a struct for cleaner code structure.
This arrangement also promotes a more organized contract structure, making it easier for developers to navigate and understand.

<details>
<summary><i>13 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

36: mapping(address token => bool) public supportedTokens
37: mapping(address token => Balances) public totals
38: mapping(address token => uint256 cap) public caps
41: mapping(address user => mapping(address token => Balances)) public balances
```
[36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L37) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L38) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L41)

```solidity
File: src/mimswap/periphery/Factory.sol

35: mapping(address base => mapping(address quote => address[] pools)) public pools
36: mapping(address creator => address[] pools) public userPools
```
[35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L35) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L36)

```solidity
File: src/staking/LockingMultiRewards.sol

89: mapping(address token => Reward info) private _rewardData
90: mapping(address user => Balances balances) private _balances
91: mapping(address user => LockedBalance[] locks) private _userLocks
92: mapping(address user => RewardLock rewardLock) private _userRewardLock
94: mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid
95: mapping(address user => mapping(address token => uint256 amount)) public rewards
96: mapping(address user => uint256 index) public lastLockIndex
```
[89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L89) | [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L90) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L91) | [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L92) | [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L94) | [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L95) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L96)
</details>

### [N-10] Consider returning a `struct` rather than having multiple `return` values

Functions that return many variables can become difficult to read and maintain.
Using a struct to encapsulate these return values can improve code readability, increase reusability, and reduce the likelihood of errors.
Consider refactoring functions that return more than three variables to use a struct instead.

<details>
<summary><i>11 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

86: function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares)
96: function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256)
```
[86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96)

```solidity
File: src/mimswap/MagicLP.sol

167: function querySellBase(
        address trader,
        uint256 payBaseAmount
    ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget)
180: function querySellQuote(
        address trader,
        uint256 payQuoteAmount
    ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget)
204: function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R)
360: function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput)
```
[167](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L167) | [180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L180) | [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360)

```solidity
File: src/mimswap/periphery/Router.sol

96: function previewCreatePool(
        uint256 i,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external pure returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares)
112: function previewAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares)
162: function addLiquidity(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares)
192: function addLiquidityETH(
        address lp,
        address to,
        address payable refundTo,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares)
```
[96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L96) | [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L112) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L162) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

48: function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80)
```
[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L48)
</details>

### [N-11] Consider using a `struct` rather than having many function input parameters

Functions with many parameters can become difficult to read and maintain. 
Using a struct to encapsulate these parameters can improve code readability, increase reusability, and reduce the likelihood of errors.
Consider refactoring functions that take more than three parameters to use a struct instead.

<details>
<summary><i>26 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

36: function _onBeforeDeposit(
        IERC20 token,
        address /*from*/,
        address /*to*/,
        uint256 /*amount*/,
        uint256 /*share*/
    ) internal view override
```
[36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L36)

```solidity
File: src/mimswap/MagicLP.sol

91: function init(
        address baseTokenAddress,
        address quoteTokenAddress,
        uint256 lpFeeRate,
        address mtFeeRateModel,
        uint256 i,
        uint256 k
    ) external
413: function sellShares(
        uint256 shareAmount,
        address to,
        uint256 baseMinAmount,
        uint256 quoteMinAmount,
        bytes calldata data,
        uint256 deadline
    ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount)
470: function setParameters(
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
[91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L91) | [413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L413) | [470](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470)

```solidity
File: src/mimswap/libraries/Math.sol

51: function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256)
131: function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256)
```
[51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)

```solidity
File: src/mimswap/periphery/Factory.sol

65: function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address)
81: function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone)
120: function removePool(
        address creator,
        address baseToken,
        address quoteToken,
        uint256 poolIndex,
        uint256 userPoolIndex
    ) external onlyOwner
155: function _computeSalt(
        address sender_,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) internal view returns (bytes32)
```
[65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81) | [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L120) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L155)

```solidity
File: src/mimswap/periphery/Router.sol

54: function createPool(
        address baseToken,
        address quoteToken,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external returns (address clone, uint256 shares)
73: function createPoolETH(
        address token,
        bool useTokenAsQuote,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 tokenInAmount
    ) external payable returns (address clone, uint256 shares)
162: function addLiquidity(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares)
178: function addLiquidityUnsafe(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 shares)
192: function addLiquidityETH(
        address lp,
        address to,
        address payable refundTo,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares)
229: function addLiquidityETHUnsafe(
        address lp,
        address to,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 shares)
261: function removeLiquidity(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumBaseAmount,
        uint256 minimumQuoteAmount,
        uint256 deadline
    ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut)
274: function removeLiquidityETH(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumETHAmount,
        uint256 minimumTokenAmount,
        uint256 deadline
    ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut)
314: function swapTokensForTokens(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut)
336: function swapETHForTokens(
        address to,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut)
365: function swapTokensForETH(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut)
404: function sellBaseTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut)
432: function sellBaseTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut)
449: function sellQuoteTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut)
478: function sellQuoteTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut)
```
[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L54) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L73) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L162) | [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L178) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192) | [229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229) | [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L261) | [274](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L274) | [314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L314) | [336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336) | [365](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L365) | [404](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L404) | [432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L432) | [449](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L449) | [478](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L478)

```solidity
File: src/staking/LockingMultiRewards.sol

112: constructor(
        address _stakingToken,
        uint256 _lockingBoostMultiplerInBips,
        uint256 _rewardsDuration,
        uint256 _lockDuration,
        address _owner
    ) OperatableV2(_owner)
```
[112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L112)
</details>

### [N-12] Avoid using constant decimals in expressions

The use of fixed decimal values such as `1e18/10 ** 18` in Solidity contracts can lead to bugs, and vulnerabilities, when interacting with tokens having different decimal configurations.
Not all ERC20 tokens follow the standard 18 decimal places, and assumptions about decimal places can lead to miscalculations.
        
Always retrieve and use the `decimals()` function from the token contract itself when performing calculations involving token amounts.
This ensures that your contract correctly handles tokens with any number of decimal places, mitigating the risk of numerical errors or under/overflows.

<details>
<summary><i>3 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/libraries/DecimalMath.sol

49: return 10 ** 18;
```
[49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L49)

```solidity
File: src/staking/LockingMultiRewards.sol

283: uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
294: return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];
```
[283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283) | [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294)
</details>

### [N-13] Avoid Empty Blocks in Code

Empty blocks in code can lead to confusion and the introduction of errors when the code is later modified.
They should be removed, or the block should do something useful, such as emitting an event or reverting. 

For contracts meant to be extended, the contract should be abstract and the function signatures added without any default implementation. 

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastGovernor.sol

13: receive() external payable {}
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L13)

```solidity
File: src/mimswap/periphery/Router.sol

36: receive() external payable {}
```
[36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L36)
</details>

### [N-14] Multiple Contracts Declared in Single File

Declaring multiple contracts within a single file can make code more difficult to understand and maintain. 
It is recommended to declare each contract in its own file, following the one contract per file rule.

<details>
<summary><i>7 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData
64: contract BlastOnboarding
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L12) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L64)

```solidity
File: src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1
34: contract BlastOnboardingBoot
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L34)

```solidity
File: src/blast/BlastWrappers.sol

19: contract BlastMIMSwapRouter
28: contract BlastMIMSwapFactory
42: contract BlastCauldronV4
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L19) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L28) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L42)
</details>

### [N-15] Custom error has no error details

Take advantage of custom error's return value property. 

An important feature of Custom Error is that values such as address, tokenID, msg.value can be written inside the () sign, providing a serious advantage in debugging and examining the revert details of dapps such as Tenderly.

<details>
<summary><i>78 issue instances in 13 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

17: error ErrZeroAddress()
18: error ErrUnsupportedToken()
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L17) | [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L18)

```solidity
File: src/blast/BlastGovernor.sol

9: error ErrZeroAddress()
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L9)

```solidity
File: src/blast/BlastMagicLP.sol

15: error ErrNotAllowedImplementationOperator()
```
[15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L15)

```solidity
File: src/blast/BlastOnboarding.sol

13: error ErrZeroAddress()
14: error ErrWrongState()
15: error ErrUnsupportedToken()
16: error ErrNotAllowed()
77: error ErrUnsupported()
78: error ErrCapReached()
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L14) | [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L15) | [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L16) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L77) | [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L78)

```solidity
File: src/blast/BlastOnboardingBoot.sol

43: error ErrInsufficientAmountOut()
44: error ErrNotReady()
45: error ErrAlreadyClaimed()
46: error ErrWrongFeeRateModel()
47: error ErrAlreadyBootstrapped()
48: error ErrNothingToClaim()
49: error ErrCannotChangeOnceReady()
```
[43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L43) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L44) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L45) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L46) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L47) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L48) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L49)

```solidity
File: src/blast/BlastTokenRegistry.sol

8: error ErrZeroAddress()
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L8)

```solidity
File: src/blast/BlastWrappers.sol

17: error ErrZeroAddress()
43: error ErrInvalidGovernorAddress()
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L17) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L43)

```solidity
File: src/mimswap/MagicLP.sol

38: error ErrInitialized()
39: error ErrBaseQuoteSame()
40: error ErrInvalidI()
41: error ErrInvalidK()
42: error ErrExpired()
43: error ErrInvalidSignature()
44: error ErrFlashLoanFailed()
45: error ErrNoBaseInput()
46: error ErrZeroAddress()
47: error ErrZeroQuoteAmount()
48: error ErrZeroQuoteTarget()
49: error ErrMintAmountNotEnough()
50: error ErrNotEnough()
51: error ErrWithdrawNotEnough()
52: error ErrSellBackNotAllowed()
53: error ErrInvalidLPFeeRate()
54: error ErrNotImplementationOwner()
55: error ErrNotImplementation()
56: error ErrNotClone()
57: error ErrNotAllowed()
58: error ErrReserveAmountNotEnough()
59: error ErrOverflow()
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L38) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L39) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L40) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L41) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L42) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L43) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L44) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L45) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L46) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L47) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L48) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L49) | [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L50) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L51) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L52) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L53) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L54) | [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L55) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L56) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L57) | [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L58) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L59)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

17: error ErrZeroAddress()
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L17)

```solidity
File: src/mimswap/libraries/Math.sol

17: error ErrIsZero()
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L17)

```solidity
File: src/mimswap/periphery/Factory.sol

29: error ErrInvalidUserPoolIndex()
30: error ErrZeroAddress()
```
[29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L29) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L30)

```solidity
File: src/mimswap/periphery/Router.sol

16: error ErrNotETHLP()
17: error ErrExpired()
18: error ErrZeroAddress()
19: error ErrPathTooLong()
20: error ErrEmptyPath()
21: error ErrBadPath()
23: error ErrInvalidBaseToken()
24: error ErrInvalidQuoteToken()
25: error ErrInTokenNotETH()
26: error ErrOutTokenNotETH()
27: error ErrInvalidQuoteTarget()
28: error ErrZeroDecimals()
29: error ErrDecimalsDifferenceTooLarge()
```
[16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L16) | [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L17) | [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L18) | [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L19) | [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L21) | [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L23) | [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L24) | [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L25) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L26) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L27) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L28) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L29)

```solidity
File: src/staking/LockingMultiRewards.sol

30: error ErrZeroAmount()
31: error ErrRewardAlreadyExists()
32: error ErrInvalidTokenAddress()
33: error ErrMaxUserLocksExceeded()
34: error ErrNotExpired()
35: error ErrInvalidUser()
36: error ErrLockAmountTooSmall()
37: error ErrLengthMismatch()
38: error ErrNoLocks()
39: error ErrLockNotExpired()
40: error ErrMaxRewardsExceeded()
41: error ErrSkimmingTooMuch()
42: error ErrInvalidLockIndex()
43: error ErrNotEnoughReward()
44: error ErrInvalidDurationRatio()
45: error ErrInvalidBoostMultiplier()
46: error ErrInvalidLockDuration()
47: error ErrInvalidRewardDuration()
48: error ErrInsufficientRemainingTime()
```
[30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L30) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L31) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L32) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L33) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L34) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L35) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L36) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L37) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L38) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L39) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L40) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L41) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L42) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L43) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L44) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L45) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L46) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L47) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L48)
</details>

### [N-16] Consider using OpenZeppelin's SafeCast for any casting

OpenZeppelin's has `SafeCast` library that provides functions to safely cast. Recommended to use it instead of casting directly in any case.

<details>
<summary><i>54 issue instances in 3 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

125: uint32(block.timestamp % 2 ** 32)
139: uint32(PMMPricing.RState.BELOW_ONE)
140: uint32(PMMPricing.RState.ONE)
144: uint32(PMMPricing.RState.ABOVE_ONE)
145: uint32(PMMPricing.RState.ONE)
212: uint256(state.R)
229: uint256(_BASE_RESERVE_)
233: uint256(_QUOTE_RESERVE_)
246: uint256(_BASE_RESERVE_)
256: uint32(newRState)
258: uint32(newRState)
269: uint256(_QUOTE_RESERVE_)
279: uint32(newRState)
281: uint32(newRState)
309: uint256(_QUOTE_RESERVE_)
315: uint256(_BASE_RESERVE_)
320: uint32(newRState)
322: uint32(newRState)
331: uint256(_BASE_RESERVE_)
337: uint256(_QUOTE_RESERVE_)
342: uint32(newRState)
344: uint32(newRState)
402: uint256(_BASE_TARGET_)
402: uint256(_BASE_TARGET_)
403: uint256(_QUOTE_TARGET_)
403: uint256(_QUOTE_TARGET_)
438: uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares))
438: uint256(_BASE_TARGET_)
438: uint256(_BASE_TARGET_)
439: uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares))
439: uint256(_QUOTE_TARGET_)
439: uint256(_QUOTE_TARGET_)
493: uint64(newLpFeeRate)
494: uint64(newK)
495: uint128(newI)
513: uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_))
513: uint256(_BASE_TARGET_)
513: uint256(_BASE_RESERVE_)
514: uint112(baseBalance)
517: uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_))
517: uint256(_QUOTE_TARGET_)
517: uint256(_QUOTE_RESERVE_)
518: uint112(quoteBalance)
536: uint112(baseBalance)
537: uint112(quoteBalance)
538: uint112(baseBalance)
539: uint112(quoteBalance)
540: uint32(PMMPricing.RState.ONE)
546: uint32(block.timestamp % 2 ** 32)
```
[125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L125) | [139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139) | [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L140) | [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144) | [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L145) | [212](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L212) | [229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L229) | [233](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L233) | [246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L246) | [256](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L256) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L258) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L269) | [279](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L279) | [281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L281) | [309](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L309) | [315](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L315) | [320](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L320) | [322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L322) | [331](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L331) | [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L337) | [342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L342) | [344](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L344) | [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402) | [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402) | [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403) | [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403) | [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439) | [493](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L493) | [494](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L494) | [495](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L495) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [514](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L514) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517) | [518](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L518) | [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L536) | [537](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L537) | [538](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L538) | [539](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L539) | [540](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L540) | [546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L546)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

38: uint256(baseOracle.latestAnswer())
39: uint256(quoteOracle.latestAnswer())
45: int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply())
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L38) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L39) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45)

```solidity
File: src/staking/LockingMultiRewards.sol

389: uint248(block.timestamp)
533: uint248(lastTimeRewardApplicable_)
```
[389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L389) | [533](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L533)
</details>

### [N-17] `uint/int` variables should have the bit size defined explicitly

In Solidity, int256 and uint256 are the preferred type names, especially since they are used for function signatures.
Using int or uint instead can lead to confusion and inconsistency.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/libraries/DecimalMath.sol

53: uint p = powFloor(target, e / 2);
```
[53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L53)

```solidity
File: src/staking/LockingMultiRewards.sol

361: function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
```
[361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361)
</details>

### [N-18] Consider using `delete` rather than assigning `false` to clear values

The use of the delete keyword is recommended over simply assigning values to false when you intend to reset the state of a variable.
The delete keyword more closely aligns with the semantic intent of clearing or resetting a variable.
This practice also makes the code more readable and highlights the change in state, which may encourage a more thorough audit of the surrounding logic.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/libraries/Math.sol

176: bSig = false
```
[176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L176)
</details>

### [N-19] Consider using `delete` rather than assigning `zero` to clear values

Rather than merely setting a variable to zero, you can use the `delete` keyword to reset it to its default value.
This action is especially relevant for complex data types like arrays or mappings where the default is not necessarily zero.
Using `delete` not only provides explicit clarity that you intend to reset a variable, but it can also result in more concise and intuitive code.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/libraries/Math.sol

154: temp = 0
```
[154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L154)

```solidity
File: src/staking/LockingMultiRewards.sol

619: rewards[user][rewardToken] = 0
```
[619](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L619)
</details>

### [N-20] Avoid external calls in modifiers

It is unusual to have external calls in modifiers, and doing so will make reviewers more likely to miss important external interactions.
Consider moving the external call to an internal function, and calling that function from the modifier.

<details>
<summary><i>3 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit - operators()
119: if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
/// @audit - owner()
119: if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
```
[119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit - owner()
608: if (msg.sender != implementation.owner()) {
```
[608](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L608)
</details>

### [N-21] Consider emitting an event at the end of the constructor

This will allow users to easily exactly pinpoint when and by whom a contract was constructed.

<details>
<summary><i>16 issue instances in 13 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

7: constructor()
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L7)

```solidity
File: src/blast/BlastBox.sol

24: constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_)
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24)

```solidity
File: src/blast/BlastGovernor.sol

15: constructor(address feeTo_, address _owner) OperatableV2(_owner)
```
[15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15)

```solidity
File: src/blast/BlastMagicLP.sol

23: constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_)
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23)

```solidity
File: src/blast/BlastOnboarding.sol

58: constructor() Owned(msg.sender)
84: constructor(BlastTokenRegistry registry_, address feeTo_)
```
[58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L58) | [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L84)

```solidity
File: src/blast/BlastTokenRegistry.sol

12: constructor(address _owner) Owned(_owner)
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12)

```solidity
File: src/blast/BlastWrappers.sol

20: constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory)
29: constructor(
        address implementation_,
        IFeeRateModel maintainerFeeRateModel_,
        address owner_,
        address governor_
    ) Factory(implementation_, maintainerFeeRateModel_, owner_)
47: constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_))
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L29) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L47)

```solidity
File: src/mimswap/MagicLP.sol

84: constructor(address owner_) Owned(owner_)
```
[84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

22: constructor(address maintainer_, address owner_) Owned(owner_)
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22)

```solidity
File: src/mimswap/periphery/Factory.sol

38: constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_)
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38)

```solidity
File: src/mimswap/periphery/Router.sol

38: constructor(IWETH weth_, IFactory factory_)
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

21: constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_)
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21)

```solidity
File: src/staking/LockingMultiRewards.sol

112: constructor(
        address _stakingToken,
        uint256 _lockingBoostMultiplerInBips,
        uint256 _rewardsDuration,
        uint256 _lockDuration,
        address _owner
    ) OperatableV2(_owner)
```
[112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L112)
</details>

### [N-22] Consider moving duplicated strings to constants

Reusing string literals in this manner can lead to inconsistencies and makes the code harder to maintain.
It's recommended to define such strings as constants, which promotes easier updates and ensures uniformity across the codebase.

<details>
<summary><i>3 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/periphery/Router.sol

271: ""
292: ""
301: ""
```
[271](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L271) | [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L292) | [301](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L301)
</details>

### [N-23] Consider providing a ranged getter for array state variables

While the compiler automatically provides a getter for accessing single elements within a public state variable array, it doesn't provide a way to fetch the whole array, or subsets thereof.
Consider adding a function to allow the fetching of slices of the array, especially if the contract doesn't already have multicall functionality.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/staking/LockingMultiRewards.sol

98: address[] public rewardTokens
```
[98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L98)
</details>

### [N-24] Consider using named returns

Using named returns makes the code more self-documenting, makes it easier to fill out NatSpec, and in some cases can save gas.
The cases below are where there currently is at most one return statement, which is ideal for named returns.

<details>
<summary><i>62 issue instances in 13 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

52: function claimGasYields() external onlyOperators returns (uint256)
103: function isOwner(address _account) internal view override returns (bool)
```
[52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L52) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L103)

```solidity
File: src/blast/BlastGovernor.sol

28: function claimNativeYields(address contractAddress) external onlyOperators returns (uint256)
32: function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256)
```
[28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L28) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L32)

```solidity
File: src/blast/BlastMagicLP.sol

39: function version() external pure override returns (string memory)
47: function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256)
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L39) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L47)

```solidity
File: src/blast/BlastOnboarding.sol

160: function claimGasYields() external onlyOwner returns (uint256)
226: function _implementation() internal view override returns (address)
```
[160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L160) | [226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L226)

```solidity
File: src/blast/BlastOnboardingBoot.sol

96: function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256)
```
[96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96)

```solidity
File: src/blast/libraries/BlastYields.sol

38: function claimMaxGasYields(address recipient) internal returns (uint256)
60: function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256)
75: function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256)
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L38) | [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L60) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L75)

```solidity
File: src/mimswap/MagicLP.sol

155: function name() public view override returns (string memory)
159: function symbol() public pure override returns (string memory)
163: function decimals() public view override returns (uint8)
236: function version() external pure virtual returns (string memory)
```
[155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155) | [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L159) | [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163) | [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L236)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

23: function mulFloor(uint256 target, uint256 d) internal pure returns (uint256)
27: function mulCeil(uint256 target, uint256 d) internal pure returns (uint256)
31: function divFloor(uint256 target, uint256 d) internal pure returns (uint256)
35: function divCeil(uint256 target, uint256 d) internal pure returns (uint256)
39: function reciprocalFloor(uint256 target) internal pure returns (uint256)
43: function reciprocalCeil(uint256 target) internal pure returns (uint256)
47: function powFloor(uint256 target, uint256 e) internal pure returns (uint256)
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L23) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L27) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L31) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L35) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L39) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L43) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L47)

```solidity
File: src/mimswap/libraries/Math.sol

19: function divCeil(uint256 a, uint256 b) internal pure returns (uint256)
51: function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256)
79: function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256)
131: function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256)
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L19) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L79) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

104: function _ROneSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
119: function _ROneSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
134: function _RBelowSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
147: function _RBelowSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
162: function _RAboveSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
175: function _RAboveSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
203: function getMidPrice(PMMState memory state) internal pure returns (uint256)
```
[104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L104) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L119) | [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L134) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L147) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L162) | [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L175) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L203)

```solidity
File: src/mimswap/periphery/Factory.sol

53: function getPoolCount(address token0, address token1) external view returns (uint256)
57: function getUserPoolCount(address creator) external view returns (uint256)
65: function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address)
155: function _computeSalt(
        address sender_,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) internal view returns (bytes32)
```
[53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L53) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L57) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L155)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

29: function decimals() external pure override returns (uint8)
33: function _getReserves() internal view virtual returns (uint256, uint256)
37: function latestAnswer() public view override returns (int256)
48: function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80)
```
[29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L29) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L33) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L37) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L48)

```solidity
File: src/staking/LockingMultiRewards.sol

199: function rewardData(address token) external view returns (Reward memory)
203: function rewardsForDuration(address rewardToken) external view returns (uint256)
207: function rewardTokensLength() external view returns (uint256)
211: function balances(address user) external view returns (Balances memory)
215: function userRewardLock(address user) external view returns (RewardLock memory)
219: function userLocks(address user) external view returns (LockedBalance[] memory)
223: function userLocksLength(address user) external view returns (uint256)
227: function locked(address user) external view returns (uint256)
231: function unlocked(address user) external view returns (uint256)
235: function totalSupply() public view returns (uint256)
239: function balanceOf(address user) public view returns (uint256)
253: function nextUnlockTime() public view returns (uint256)
257: function epoch() public view returns (uint256)
261: function nextEpoch() public view returns (uint256)
265: function remainingEpochTime() public view returns (uint256)
269: function lastTimeRewardApplicable(address rewardToken) public view returns (uint256)
273: function rewardPerToken(address rewardToken) public view returns (uint256)
277: function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256)
288: function earned(address user, address rewardToken) public view returns (uint256)
292: function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256)
```
[199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L203) | [207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L207) | [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L211) | [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L215) | [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L219) | [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L223) | [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L227) | [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L231) | [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L235) | [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L239) | [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L253) | [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L257) | [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L261) | [265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L265) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L269) | [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L273) | [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277) | [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L288) | [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L292)
</details>

### [N-25] Style guide: Initialisms should be capitalized

According to the Solidity [style guide](https://docs.soliditylang.org/en/latest/style-guide.html#naming-styles) initialisms such as "NFT", "ERC", etc should be capitalized.

<details>
<summary><i>20 issue instances in 9 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

24: IERC20 weth_
52: function claimGasYields() external onlyOperators returns (uint256)
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L52)

```solidity
File: src/blast/BlastGovernor.sol

32: function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256)
```
[32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L32)

```solidity
File: src/blast/BlastMagicLP.sol

47: function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256)
```
[47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L47)

```solidity
File: src/blast/BlastOnboarding.sol

160: function claimGasYields() external onlyOwner returns (uint256)
```
[160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L160)

```solidity
File: src/blast/BlastWrappers.sol

20: IWETH weth_
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20)

```solidity
File: src/blast/libraries/BlastYields.sol

38: function claimMaxGasYields(address recipient) internal returns (uint256)
42: function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount)
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L38) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L42)

```solidity
File: src/mimswap/periphery/Factory.sol

124: uint256 poolIndex
125: uint256 userPoolIndex
```
[124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L124) | [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L125)

```solidity
File: src/mimswap/periphery/Router.sol

33: IWETH public immutable weth
38: IWETH weth_
281: uint256 ethAmountOut
200: uint256 wethAdjustedAmount
375: uint256 lastLpIndex = path.length - 1
```
[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L33) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38) | [281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L281) | [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L200) | [375](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L375)

```solidity
File: src/staking/LockingMultiRewards.sol

96: mapping(address user => uint256 index) public lastLockIndex
397: uint256[] calldata lockIndexes
414: uint256 index = lockIndexes[i]
427: uint256 lastIndex = locks.length - 1
482: uint256 _lastLockIndex = lastLockIndex[user]
```
[96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L96) | [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397) | [414](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L414) | [427](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L427) | [482](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L482)
</details>

### [N-26] Expressions for constant values should use `immutable` rather than `constant`

While it does not save gas for some simple binary expressions because the compiler knows that developers often make this mistake, it's still best to use the right tool for the task at hand. There is a difference between `constant` variables and immutable variables, and they should each be used in their appropriate contexts.
`constant`s should be used for literal values written into the code, and immutable variables should be used for expressions, or values calculated in, or passed into the constructor.

<details>
<summary><i>6 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/libraries/BlastPoints.sol

8: IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800)
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L8)

```solidity
File: src/blast/libraries/BlastYields.sol

14: IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002)
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L14)

```solidity
File: src/mimswap/MagicLP.sol

63: uint256 public constant MAX_I = 10 ** 36
64: uint256 public constant MAX_K = 10 ** 18
```
[63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

20: uint256 internal constant ONE = 10 ** 18
21: uint256 internal constant ONE2 = 10 ** 36
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L21)
</details>

### [N-27] Consider using named function arguments

When calling functions in external contracts with multiple arguments, consider using named function parameters, rather than positional ones.

<details>
<summary><i>127 issue instances in 14 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

61: BlastYields.claimAllTokenYields(token_, feeTo)
```
[61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L61)

```solidity
File: src/blast/BlastGovernor.sol

29: BlastYields.claimAllNativeYields(contractAddress, feeTo)
33: BlastYields.claimMaxGasYields(contractAddress, feeTo)
```
[29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L29) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L33)

```solidity
File: src/blast/BlastMagicLP.sol

57: BlastYields.claimAllTokenYields(_BASE_TOKEN_, feeTo_)
60: BlastYields.claimAllTokenYields(_QUOTE_TOKEN_, feeTo_)
```
[57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L57) | [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L60)

```solidity
File: src/blast/BlastOnboarding.sol

102: token.safeTransferFrom(msg.sender, address(this), amount)
138: token.safeTransfer(msg.sender, amount)
170: BlastYields.claimAllTokenYields(tokens[i], feeTo)
210: token.safeTransfer(to, amount)
```
[102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L102) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L138) | [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L170) | [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L210)

```solidity
File: src/blast/BlastOnboardingBoot.sol

69: staking.stakeFor(msg.sender, shares, lock)
89: router.previewCreatePool(I, baseAmount, quoteAmount)
103: MIM.safeApprove(address(router), type(uint256).max)
104: USDB.safeApprove(address(router), type(uint256).max)
106: router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount)
118: staking.setOperator(address(this), true)
122: pool.safeApprove(address(staking), totalPoolShares)
```
[69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L69) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L89) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L103) | [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L104) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L118) | [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L122)

```solidity
File: src/blast/libraries/BlastYields.sol

30: BLAST_YIELD_PRECOMPILE.configure(YieldMode.CLAIMABLE, GasMode.CLAIMABLE, governor_)
43: BLAST_YIELD_PRECOMPILE.claimMaxGas(contractAddress, recipient)
56: BLAST_YIELD_PRECOMPILE.claimAllYield(contractAddress, recipient)
61: BLAST_YIELD_PRECOMPILE.claimYield(contractAddress, recipient, amount)
71: IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)))
76: IERC20Rebasing(token).claim(recipient, amount)
87: Address.functionCall(address(BLAST_YIELD_PRECOMPILE), data)
```
[30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L30) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L43) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L56) | [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L61) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L71) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L76) | [87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L87)

```solidity
File: src/mimswap/MagicLP.sol

172: PMMPricing.sellBaseToken(state, payBaseAmount)
174: _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_)
175: DecimalMath.mulFloor(receiveQuoteAmount, mtFeeRate)
176: DecimalMath.mulFloor(receiveQuoteAmount, lpFeeRate)
185: PMMPricing.sellQuoteToken(state, payQuoteAmount)
187: _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_)
188: DecimalMath.mulFloor(receiveBaseAmount, mtFeeRate)
189: DecimalMath.mulFloor(receiveBaseAmount, lpFeeRate)
225: _MT_FEE_RATE_MODEL_.getFeeRate(user, _LP_FEE_RATE_)
295: ICallee(assetTo).FlashLoanCall(msg.sender, baseAmount, quoteAmount, data)
381: DecimalMath.mulFloor(baseBalance, _I_)
381: DecimalMath.divFloor(quoteBalance, _I_)
383: DecimalMath.mulFloor(shares, _I_)
397: DecimalMath.divFloor(baseInput, baseReserve)
398: DecimalMath.divFloor(quoteInput, quoteReserve)
400: DecimalMath.mulFloor(totalSupply(), mintRatio)
402: DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)
403: DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)
451: ICallee(to).SellShareCall(msg.sender, shareAmount, baseAmount, quoteAmount, data)
466: token.safeTransfer(to, amount)
583: _BASE_TOKEN_.safeTransfer(to, amount)
589: _QUOTE_TOKEN_.safeTransfer(to, amount)
```
[172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L172) | [174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L174) | [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L175) | [176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L176) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L185) | [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L187) | [188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L188) | [189](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L189) | [225](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L225) | [295](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L295) | [381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L381) | [381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L381) | [383](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L383) | [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L397) | [398](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L398) | [400](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L400) | [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402) | [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403) | [451](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L451) | [466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L466) | [583](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L583) | [589](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L589)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

39: IFeeRateImpl(implementation).getFeeRate(msg.sender, trader, lpFeeRate)
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L39)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

14: Math.divCeil(lpFeeRate, 2)
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L14)

```solidity
File: src/mimswap/libraries/Math.sol

62: DecimalMath.divFloor((V0 * V0) / V1, V2)
63: DecimalMath.mulFloor(k, V0V0V1V2)
81: DecimalMath.mulFloor(i, delta)
101: DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2)
103: DecimalMath.mulFloor(V1, premium)
141: DecimalMath.mulFloor(i, delta)
141: DecimalMath.mulFloor(i, delta)
184: DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0)
184: DecimalMath.mulFloor(k, V0)
199: DecimalMath.divCeil(numerator, denominator)
```
[62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L63) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L81) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L101) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L103) | [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L141) | [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L141) | [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184) | [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184) | [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L199)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

116: Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q0, payBaseAmount, state.i, state.K)
129: Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K)
144: Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K)
157: Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q, payBaseAmount, state.i, state.K)
172: Math._GeneralIntegrate(state.B0, state.B + payBaseAmount, state.B, state.i, state.K)
185: Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K)
192: Math._SolveQuadraticFunctionForTarget(state.Q, state.B - state.B0, state.i, state.K)
194: Math._SolveQuadraticFunctionForTarget(
                state.B,
                state.Q - state.Q0,
                DecimalMath.reciprocalFloor(state.i),
                state.K
            )
205: DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q)
206: DecimalMath.mulFloor(state.K, R)
207: DecimalMath.divFloor(state.i, R)
209: DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B)
210: DecimalMath.mulFloor(state.K, R)
211: DecimalMath.mulFloor(state.i, R)
```
[116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L116) | [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L129) | [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L144) | [157](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L157) | [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L172) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L185) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L192) | [194](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L194) | [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205) | [206](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L206) | [207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L207) | [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209) | [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L210) | [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L211)

```solidity
File: src/mimswap/periphery/Factory.sol

86: IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_)
```
[86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L86)

```solidity
File: src/mimswap/periphery/Router.sol

66: IFactory(factory).create(baseToken, quoteToken, lpFeeRate, i, k)
68: baseToken.safeTransferFrom(msg.sender, clone, baseInAmount)
69: quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount)
88: IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k)
91: token.safeTransferFrom(msg.sender, clone, tokenInAmount)
92: address(weth).safeTransferFrom(address(this), clone, msg.value)
101: DecimalMath.mulFloor(baseInAmount, i)
101: DecimalMath.divFloor(quoteInAmount, i)
103: DecimalMath.mulFloor(shares, i)
138: DecimalMath.mulFloor(baseBalance, i)
138: DecimalMath.divFloor(quoteBalance, i)
140: DecimalMath.mulFloor(shares, i)
148: DecimalMath.divFloor(baseInAmount, baseReserve)
149: DecimalMath.divFloor(quoteInAmount, quoteReserve)
152: DecimalMath.mulCeil(quoteReserve, baseInputRatio)
153: DecimalMath.mulFloor(totalSupply, baseInputRatio)
156: DecimalMath.mulCeil(baseReserve, quoteInputRatio)
157: DecimalMath.mulFloor(totalSupply, quoteInputRatio)
172: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount)
173: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount)
186: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount)
187: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount)
217: address(weth).safeTransfer(lp, wethAdjustedAmount)
224: token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount)
244: address(weth).safeTransfer(lp, msg.value)
246: token.safeTransferFrom(msg.sender, lp, tokenInAmount)
269: lp.safeTransferFrom(msg.sender, address(this), sharesIn)
271: IMagicLP(lp).sellShares(sharesIn, to, minimumBaseAmount, minimumQuoteAmount, "", deadline)
282: lp.safeTransferFrom(msg.sender, address(this), sharesIn)
287: IMagicLP(lp).sellShares(
                sharesIn,
                address(this),
                minimumETHAmount,
                minimumTokenAmount,
                "",
                deadline
            )
296: IMagicLP(lp).sellShares(
                sharesIn,
                address(this),
                minimumTokenAmount,
                minimumETHAmount,
                "",
                deadline
            )
311: token.safeTransfer(to, tokenAmountOut)
328: IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn)
330: IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn)
360: inToken.safeTransfer(address(firstLp), msg.value)
393: IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn)
395: IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn)
411: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn)
428: baseToken.safeTransfer(lp, msg.value)
443: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn)
456: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn)
474: quoteToken.safeTransfer(lp, msg.value)
489: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn)
523: DecimalMath.mulFloor(baseInAmount, i)
523: DecimalMath.divFloor(quoteInAmount, i)
525: DecimalMath.mulFloor(shares, i)
528: DecimalMath.divFloor(baseInAmount, baseReserve)
529: DecimalMath.divFloor(quoteInAmount, quoteReserve)
532: DecimalMath.mulFloor(quoteReserve, baseIncreaseRatio)
535: DecimalMath.mulFloor(baseReserve, quoteIncreaseRatio)
```
[66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L66) | [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L68) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L69) | [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L88) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L91) | [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L101) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L101) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L103) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L138) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L138) | [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L140) | [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L148) | [149](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L149) | [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L152) | [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L153) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L156) | [157](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L157) | [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L172) | [173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L173) | [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L186) | [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L187) | [217](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L217) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L224) | [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L244) | [246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L246) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L269) | [271](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L271) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282) | [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L287) | [296](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L296) | [311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L311) | [328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L328) | [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L330) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L360) | [393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L393) | [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L395) | [411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L411) | [428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L428) | [443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L443) | [456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L456) | [474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L474) | [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L489) | [523](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L523) | [523](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L523) | [525](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L525) | [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L528) | [529](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L529) | [532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L532) | [535](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L535)

```solidity
File: src/staking/LockingMultiRewards.sol

180: stakingToken.safeTransfer(msg.sender, amount)
330: tokenAddress.safeTransfer(owner, tokenAmount)
367: rewardToken.safeTransferFrom(msg.sender, address(this), amount)
464: stakingToken.safeTransferFrom(msg.sender, address(this), amount)
637: rewardToken.safeTransfer(user, amount)
```
[180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L180) | [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L330) | [367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367) | [464](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L464) | [637](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L637)
</details>

### [N-28] Contract/Library Names Not in `CapWords` Style (CamelCase)

Contracts and libraries should be named using the `CapWords` style for better readability and consistency with Solidity style guidelines.
Examples of good practice include: SimpleToken, SmartBank, CertificateHashRepository, Player, Congress, Owned.
[More information in Documentation](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#contract-and-library-names)

<details>
<summary><i>5 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/BlastMagicLP.sol

9: contract BlastMagicLP is MagicLP {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L9)

```solidity
File: src/blast/BlastWrappers.sol

18: contract BlastMIMSwapRouter is Router {
27: contract BlastMIMSwapFactory is Factory {
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L18) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L27)

```solidity
File: src/mimswap/MagicLP.sol

25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L25)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

19: library PMMPricing {
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L19)
</details>

### [N-29] Events are missing sender information

Events should include the sender information when emitted in `public` or `external` functions for better traceability.

<details>
<summary><i>35 issue instances in 10 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

/// @audit external function `setFeeTo()` emits an event without sender information
78: emit LogFeeToChanged(feeTo_);
/// @audit external function `setTokenEnabled()` emits an event without sender information
89: emit LogTokenDepositEnabled(token, enabled);
```
[78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L78) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L89)

```solidity
File: src/blast/BlastGovernor.sol

/// @audit external function `setFeeTo()` emits an event without sender information
46: emit LogFeeToChanged(_feeTo);
```
[46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L46)

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit external function `setFeeTo()` emits an event without sender information
86: emit LogFeeToChanged(feeTo_);
/// @audit external function `setOperator()` emits an event without sender information
91: emit LogOperatorChanged(operator, status);
```
[86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L86) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L91)

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit external function `setFeeTo()` emits an event without sender information
153: emit LogFeeToChanged(feeTo_);
/// @audit external function `setTokenSupported()` emits an event without sender information
181: emit LogTokenSupported(token, supported);
/// @audit external function `setCap()` emits an event without sender information
187: emit LogTokenCapChanged(token, cap);
/// @audit external function `setBootstrapper()` emits an event without sender information
192: emit LogBootstrapperChanged(bootstrapper_);
/// @audit external function `open()` emits an event without sender information
197: emit LogStateChange(State.Opened);
/// @audit external function `close()` emits an event without sender information
202: emit LogStateChange(State.Closed);
/// @audit external function `rescue()` emits an event without sender information
211: emit LogTokenRescue(token, to, amount);
```
[153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L153) | [181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L181) | [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L187) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L192) | [197](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L197) | [202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L202) | [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L211)

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit external function `bootstrap()` emits an event without sender information
123: emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);
/// @audit external function `initialize()` emits an event without sender information
132: emit LogInitialized(_router);
/// @audit external function `setStaking()` emits an event without sender information
143: emit LogStakingChanged(address(_staking));
/// @audit external function `setReady()` emits an event without sender information
148: emit LogReadyChanged(ready);
```
[123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L123) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L132) | [143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L143) | [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148)

```solidity
File: src/blast/BlastTokenRegistry.sol

/// @audit external function `setNativeYieldTokenEnabled()` emits an event without sender information
20: emit LogNativeYieldTokenEnabled(token, enabled);
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L20)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit external function `sellBase()` emits an event without sender information
259: emit RChange(newRState);
/// @audit external function `sellQuote()` emits an event without sender information
282: emit RChange(newRState);
/// @audit external function `flashLoan()` emits an event without sender information
323: emit RChange(newRState);
/// @audit external function `flashLoan()` emits an event without sender information
345: emit RChange(newRState);
/// @audit external function `buyShares()` emits an event without sender information
408: emit BuyShares(to, shares, balanceOf(to));
/// @audit external function `rescue()` emits an event without sender information
467: emit TokenRescue(token, to, amount);
/// @audit public function `setParameters()` emits an event without sender information
500: emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);
```
[259](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L259) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L282) | [323](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L323) | [345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L345) | [408](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L408) | [467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L467) | [500](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L500)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit external function `setMaintainer()` emits an event without sender information
52: emit LogMaintainerChanged(maintainer_);
/// @audit public function `setImplementation()` emits an event without sender information
59: emit LogImplementationChanged(implementation_);
```
[52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L52) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L59)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit external function `create()` emits an event without sender information
87: emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
/// @audit external function `setLpImplementation()` emits an event without sender information
102: emit LogSetImplementation(implementation_);
/// @audit external function `setMaintainerFeeRateModel()` emits an event without sender information
111: emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);
/// @audit external function `removePool()` emits an event without sender information
140: emit LogPoolRemoved(pool);
```
[87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L87) | [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L102) | [111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L111) | [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L140)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit external function `setMinLockAmount()` emits an event without sender information
318: emit LogSetMinLockAmount(minLockAmount, _minLockAmount);
/// @audit external function `recover()` emits an event without sender information
331: emit LogRecovered(tokenAddress, tokenAmount);
/// @audit public function `notifyRewardAmount()` emits an event without sender information
391: emit LogRewardAdded(amount);
/// @audit external function `processExpiredLocks()` emits an event without sender information
436: emit LogLockIndexChanged(user, lastIndex, index);
/// @audit external function `processExpiredLocks()` emits an event without sender information
446: emit LogUnlocked(user, amount, index);
```
[318](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L318) | [331](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L331) | [391](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L391) | [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L436) | [446](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L446)
</details>

### [N-30] Non-constant/non-immutable variables using all capital letters

Variable names that consist of all capital letters should be reserved for constant/immutable variables. If the variable needs to be different based on which class it comes from, a view/pure function should be used instead.

<details>
<summary><i>25 issue instances in 3 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

68: bool internal _INITIALIZED_;
70: address public _BASE_TOKEN_;
71: address public _QUOTE_TOKEN_;
72: uint112 public _BASE_RESERVE_;
73: uint112 public _QUOTE_RESERVE_;
74: uint32 public _BLOCK_TIMESTAMP_LAST_;
75: uint256 public _BASE_PRICE_CUMULATIVE_LAST_;
76: uint112 public _BASE_TARGET_;
77: uint112 public _QUOTE_TARGET_;
79: IFeeRateModel public _MT_FEE_RATE_MODEL_;
80: uint256 public _LP_FEE_RATE_;
81: uint256 public _K_;
82: uint256 public _I_;
```
[68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L68) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L70) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L71) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73) | [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L75) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L79) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L80) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L81) | [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L82)

```solidity
File: src/mimswap/libraries/Math.sol

62: uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);
70: Assume Q2=Q0, Given Q1 and deltaB, solve Q0
115: and Q2=(-b+sqrt(b^2+4(1-k)kQ0^2))/2(1-k)
199: uint256 V2 = DecimalMath.divCeil(numerator, denominator);
```
[62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L70) | [115](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L115) | [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L199)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

29: uint256 K;
30: uint256 B;
31: uint256 Q;
32: uint256 B0;
33: uint256 Q0;
34: RState R;
205: uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);
209: uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
```
[29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L29) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L30) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L31) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L32) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L33) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L34) | [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205) | [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209)
</details>

### [N-31] Leverage Recent Solidity Features with `0.8.23`

The recent updates in Solidity provide several features and optimizations that, when leveraged appropriately, can significantly improve your contract's code clarity and maintainability.
Key enhancements include the use of push0 for placing 0 on the stack for EVM versions starting from "Shanghai", making your code simpler and more straightforward.
Moreover, Solidity has extended NatSpec documentation support to enum and struct definitions, facilitating more comprehensive and insightful code documentation.

Additionally, the re-implementation of the UnusedAssignEliminator and UnusedStoreEliminator in the Solidity optimizer provides the ability to remove unused assignments in deeply nested loops.
This results in a cleaner, more efficient contract code, reducing clutter and potential points of confusion during code review or debugging.
It's recommended to make full use of these features and optimizations to enhance the robustness and readability of your smart contracts.

<details>
<summary><i>20 issue instances in 20 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2)

```solidity
File: src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L3)

```solidity
File: src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L2)

```solidity
File: src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L3)

```solidity
File: src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L2)

```solidity
File: src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L2)

```solidity
File: src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L2)

```solidity
File: src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L2)

```solidity
File: src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L2)

```solidity
File: src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L2)

```solidity
File: src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L7)

```solidity
File: src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L8)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L8)

```solidity
File: src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L2)

```solidity
File: src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L2)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L2)

```solidity
File: src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L2)
</details>

### [N-32] NatSpec: Function `@param` tag is missing

Natural Specification (NatSpec) comments are crucial for understanding the role of function arguments in your Solidity code.
Including `@param` tags will not only improve your code's readability but also its maintainability by clearly defining each argument's purpose.

[More information in Documentation](https://docs.soliditylang.org/en/develop/natspec-format.html)

<details>
<summary><i>157 issue instances in 17 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

/// @audit Missed @param `weth_, registry_, feeTo_`
24: constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
/// @audit Missed @param `token, /*from*/, /*to*/, /*amount*/, /*share*/`
36: function _onBeforeDeposit(
        IERC20 token,
        address /*from*/,
        address /*to*/,
        uint256 /*amount*/,
        uint256 /*share*/
    ) internal view override {
/// @audit Missed @param `token_`
56: function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
/// @audit Missed @param `data`
68: function callBlastPrecompile(bytes calldata data) external onlyOwner {
/// @audit Missed @param `feeTo_`
72: function setFeeTo(address feeTo_) external onlyOwner {
/// @audit Missed @param `token, enabled`
81: function setTokenEnabled(address token, bool enabled) external onlyOwner {
/// @audit Missed @param `_account`
103: function isOwner(address _account) internal view override returns (bool) {
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L36) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L56) | [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L68) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L103)

```solidity
File: src/blast/BlastGovernor.sol

/// @audit Missed @param `feeTo_, _owner`
15: constructor(address feeTo_, address _owner) OperatableV2(_owner) {
/// @audit Missed @param `contractAddress`
28: function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
/// @audit Missed @param `contractAddress`
32: function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
/// @audit Missed @param `_feeTo`
40: function setFeeTo(address _feeTo) external onlyOwner {
/// @audit Missed @param `data`
49: function callBlastPrecompile(bytes calldata data) external onlyOwner {
/// @audit Missed @param `to, value, data`
53: function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```
[15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L28) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L32) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L49) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit Missed @param `registry_, feeTo_, owner_`
23: constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
/// @audit Missed @param `data`
72: function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {
/// @audit Missed @param `feeTo_`
80: function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
/// @audit Missed @param `operator, status`
89: function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L72) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89)

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit Missed @param `token, amount, lock_`
101: function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
/// @audit Missed @param `token, amount`
123: function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
/// @audit Missed @param `token, amount`
132: function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
/// @audit Missed @param `feeTo_`
147: function setFeeTo(address feeTo_) external onlyOwner {
/// @audit Missed @param `data`
156: function callBlastPrecompile(bytes calldata data) external onlyOwner {
/// @audit Missed @param `tokens`
164: function claimTokenYields(address[] memory tokens) external onlyOwner {
/// @audit Missed @param `token, supported`
175: function setTokenSupported(address token, bool supported) external onlyOwner {
/// @audit Missed @param `token, cap`
185: function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
/// @audit Missed @param `bootstrapper_`
190: function setBootstrapper(address bootstrapper_) external onlyOwner {
/// @audit Missed @param `token, to, amount`
205: function rescue(address token, address to, uint256 amount) external onlyOwner {
```
[101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101) | [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L156) | [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164) | [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185) | [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190) | [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L205)

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit Missed @param `lock`
55: function claim(bool lock) external returns (uint256 shares) {
/// @audit Missed @param `user`
78: function claimable(address user) external view returns (uint256 shares) {
/// @audit Missed @param `minAmountOut`
96: function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
/// @audit Missed @param `_router`
129: function initialize(Router _router) external onlyOwner {
/// @audit Missed @param `_staking`
137: function setStaking(LockingMultiRewards _staking) external onlyOwner {
/// @audit Missed @param `_ready`
146: function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
/// @audit Missed @param `user`
155: function _claimable(address user) internal view returns (uint256 shares) {
```
[55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L55) | [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L78) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96) | [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129) | [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L155)

```solidity
File: src/blast/BlastTokenRegistry.sol

/// @audit Missed @param `_owner`
12: constructor(address _owner) Owned(_owner) {}
/// @audit Missed @param `token, enabled`
14: function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14)

```solidity
File: src/blast/BlastWrappers.sol

/// @audit Missed @param `weth_, factory, governor_`
20: constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
/// @audit Missed @param `data`
59: function init(bytes calldata data) public payable override {
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59)

```solidity
File: src/blast/libraries/BlastYields.sol

/// @audit Missed @param `token`
20: function enableTokenClaimable(address token) internal {
/// @audit Missed @param `governor_`
29: function configureDefaultClaimables(address governor_) internal {
/// @audit Missed @param `recipient`
38: function claimMaxGasYields(address recipient) internal returns (uint256) {
/// @audit Missed @param `contractAddress, recipient`
42: function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {
/// @audit Missed @param `recipient`
51: function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
/// @audit Missed @param `contractAddress, recipient`
55: function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {
/// @audit Missed @param `contractAddress, amount, recipient`
60: function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {
/// @audit Missed @param `token, recipient`
70: function claimAllTokenYields(address token, address recipient) internal returns (uint256 amount) {
/// @audit Missed @param `token, amount, recipient`
75: function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {
/// @audit Missed @param `data`
86: function callPrecompile(bytes calldata data) internal {
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L20) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L29) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L38) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L42) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L51) | [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L55) | [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L60) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L70) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L75) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L86)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit Missed @param `owner_`
84: constructor(address owner_) Owned(owner_) {
/// @audit Missed @param `baseTokenAddress, quoteTokenAddress, lpFeeRate, mtFeeRateModel, i, k`
91: function init(
        address baseTokenAddress,
        address quoteTokenAddress,
        uint256 lpFeeRate,
        address mtFeeRateModel,
        uint256 i,
        uint256 k
    ) external {
/// @audit Missed @param `trader, payBaseAmount`
167: function querySellBase(
        address trader,
        uint256 payBaseAmount
    ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {
/// @audit Missed @param `trader, payQuoteAmount`
180: function querySellQuote(
        address trader,
        uint256 payQuoteAmount
    ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {
/// @audit Missed @param `user`
224: function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
/// @audit Missed @param `to`
244: function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {
/// @audit Missed @param `to`
267: function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {
/// @audit Missed @param `baseAmount, quoteAmount, assetTo, data`
290: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
/// @audit Missed @param `to`
360: function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
/// @audit Missed @param `shareAmount, to, baseMinAmount, quoteMinAmount, data, deadline`
413: function sellShares(
        uint256 shareAmount,
        address to,
        uint256 baseMinAmount,
        uint256 quoteMinAmount,
        bytes calldata data,
        uint256 deadline
    ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {
/// @audit Missed @param `token, to, amount`
461: function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {
/// @audit Missed @param `assetTo, newLpFeeRate, newI, newK, baseOutAmount, quoteOutAmount, minBaseReserve, minQuoteReserve`
470: function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner {
/// @audit Missed @param `baseReserve, quoteReserve`
560: function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {
/// @audit Missed @param `to, amount`
581: function _transferBaseOut(address to, uint256 amount) internal {
/// @audit Missed @param `to, amount`
587: function _transferQuoteOut(address to, uint256 amount) internal {
/// @audit Missed @param `to, amount`
593: function _mint(address to, uint256 amount) internal override {
```
[84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L91) | [167](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L167) | [180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L180) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L224) | [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L244) | [267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L267) | [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360) | [413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L413) | [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L461) | [470](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470) | [560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L560) | [581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L581) | [587](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L587) | [593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L593)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit Missed @param `maintainer_, owner_`
22: constructor(address maintainer_, address owner_) Owned(owner_) {
/// @audit Missed @param `trader, lpFeeRate`
34: function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
/// @audit Missed @param `maintainer_`
46: function setMaintainer(address maintainer_) external onlyOwner {
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

/// @audit Missed @param `/*pool*/, /*trader*/, lpFeeRate`
9: function getFeeRate(
        address /*pool*/,
        address /*trader*/,
        uint256 lpFeeRate
    ) external pure returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

/// @audit Missed @param `target, d`
23: function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {
/// @audit Missed @param `target, d`
27: function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {
/// @audit Missed @param `target, d`
31: function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {
/// @audit Missed @param `target, d`
35: function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {
/// @audit Missed @param `target`
39: function reciprocalFloor(uint256 target) internal pure returns (uint256) {
/// @audit Missed @param `target`
43: function reciprocalCeil(uint256 target) internal pure returns (uint256) {
/// @audit Missed @param `target, e`
47: function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L23) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L27) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L31) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L35) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L39) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L43) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L47)

```solidity
File: src/mimswap/libraries/Math.sol

/// @audit Missed @param `a, b`
19: function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {
/// @audit Missed @param `x`
29: function sqrt(uint256 x) internal pure returns (uint256 y) {
/// @audit Missed @param `V0, V1, V2, i, k`
51: function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {
/// @audit Missed @param `V1, delta, i, k`
79: function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
/// @audit Missed @param `V0, V1, delta, i, k`
131: function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L19) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L29) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L79) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

/// @audit Missed @param `state, payBaseAmount`
39: function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {
/// @audit Missed @param `state, payQuoteAmount`
76: function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {
/// @audit Missed @param `state, payBaseAmount`
104: function _ROneSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {
/// @audit Missed @param `state, payQuoteAmount`
119: function _ROneSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {
/// @audit Missed @param `state, payQuoteAmount`
134: function _RBelowSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {
/// @audit Missed @param `state, payBaseAmount`
147: function _RBelowSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {
/// @audit Missed @param `state, payBaseAmount`
162: function _RAboveSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {
/// @audit Missed @param `state, payQuoteAmount`
175: function _RAboveSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {
/// @audit Missed @param `state`
190: function adjustedTarget(PMMState memory state) internal pure {
/// @audit Missed @param `state`
203: function getMidPrice(PMMState memory state) internal pure returns (uint256) {
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L39) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L76) | [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L104) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L119) | [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L134) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L147) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L162) | [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L175) | [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L190) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L203)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit Missed @param `implementation_, maintainerFeeRateModel_, owner_`
38: constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
/// @audit Missed @param `token0, token1`
53: function getPoolCount(address token0, address token1) external view returns (uint256) {
/// @audit Missed @param `creator`
57: function getUserPoolCount(address creator) external view returns (uint256) {
/// @audit Missed @param `creator, baseToken_, quoteToken_, lpFeeRate_, i_, k_`
65: function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address) {
/// @audit Missed @param `baseToken_, quoteToken_, lpFeeRate_, i_, k_`
81: function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
/// @audit Missed @param `implementation_`
96: function setLpImplementation(address implementation_) external onlyOwner {
/// @audit Missed @param `maintainerFeeRateModel_`
105: function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
/// @audit Missed @param `creator, baseToken, quoteToken, pool`
116: function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {
/// @audit Missed @param `creator, baseToken, quoteToken, poolIndex, userPoolIndex`
120: function removePool(
        address creator,
        address baseToken,
        address quoteToken,
        uint256 poolIndex,
        uint256 userPoolIndex
    ) external onlyOwner {
/// @audit Missed @param `creator, baseToken, quoteToken, pool`
148: function _addPool(address creator, address baseToken, address quoteToken, address pool) internal {
/// @audit Missed @param `sender_, baseToken_, quoteToken_, lpFeeRate_, i_, k_`
155: function _computeSalt(
        address sender_,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) internal view returns (bytes32) {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L53) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L57) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96) | [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105) | [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L116) | [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L120) | [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L148) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L155)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit Missed @param `weth_, factory_`
38: constructor(IWETH weth_, IFactory factory_) {
/// @audit Missed @param `baseToken, quoteToken, lpFeeRate, i, k, to, baseInAmount, quoteInAmount`
54: function createPool(
        address baseToken,
        address quoteToken,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external returns (address clone, uint256 shares) {
/// @audit Missed @param `token, useTokenAsQuote, lpFeeRate, i, k, to, tokenInAmount`
73: function createPoolETH(
        address token,
        bool useTokenAsQuote,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 tokenInAmount
    ) external payable returns (address clone, uint256 shares) {
/// @audit Missed @param `i, baseInAmount, quoteInAmount`
96: function previewCreatePool(
        uint256 i,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external pure returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit Missed @param `lp, baseInAmount, quoteInAmount`
112: function previewAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit Missed @param `lp, to, baseInAmount, quoteInAmount, minimumShares, deadline`
162: function addLiquidity(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit Missed @param `lp, to, baseInAmount, quoteInAmount, minimumShares, deadline`
178: function addLiquidityUnsafe(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 shares) {
/// @audit Missed @param `lp, to, refundTo, tokenInAmount, minimumShares, deadline`
192: function addLiquidityETH(
        address lp,
        address to,
        address payable refundTo,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit Missed @param `lp, to, tokenInAmount, minimumShares, deadline`
229: function addLiquidityETHUnsafe(
        address lp,
        address to,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 shares) {
/// @audit Missed @param `lp, sharesIn`
251: function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
/// @audit Missed @param `lp, to, sharesIn, minimumBaseAmount, minimumQuoteAmount, deadline`
261: function removeLiquidity(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumBaseAmount,
        uint256 minimumQuoteAmount,
        uint256 deadline
    ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
/// @audit Missed @param `lp, to, sharesIn, minimumETHAmount, minimumTokenAmount, deadline`
274: function removeLiquidityETH(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumETHAmount,
        uint256 minimumTokenAmount,
        uint256 deadline
    ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {
/// @audit Missed @param `to, amountIn, path, directions, minimumOut, deadline`
314: function swapTokensForTokens(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @param `to, path, directions, minimumOut, deadline`
336: function swapETHForTokens(
        address to,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @param `to, amountIn, path, directions, minimumOut, deadline`
365: function swapTokensForETH(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @param `lp, to, amountIn, minimumOut, deadline`
404: function sellBaseTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @param `lp, to, minimumOut, deadline`
415: function sellBaseETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @param `lp, to, amountIn, minimumOut, deadline`
432: function sellBaseTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @param `lp, to, amountIn, minimumOut, deadline`
449: function sellQuoteTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @param `lp, to, minimumOut, deadline`
461: function sellQuoteETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @param `lp, to, amountIn, minimumOut, deadline`
478: function sellQuoteTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @param `lp, to, minimumShares`
499: function _addLiquidity(address lp, address to, uint256 minimumShares) internal returns (uint256 shares) {
/// @audit Missed @param `lp, baseInAmount, quoteInAmount`
509: function _adjustAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) internal view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount) {
/// @audit Missed @param `to, path, directions, minimumOut`
541: function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {
/// @audit Missed @param `lp, to, minimumOut`
571: function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {
/// @audit Missed @param `lp, to, minimumOut`
578: function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {
/// @audit Missed @param `path`
586: function _validatePath(address[] calldata path) internal pure {
/// @audit Missed @param `baseDecimals, quoteDecimals`
598: function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L54) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L73) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L96) | [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L112) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L162) | [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L178) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192) | [229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229) | [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L251) | [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L261) | [274](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L274) | [314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L314) | [336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336) | [365](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L365) | [404](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L404) | [415](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L415) | [432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L432) | [449](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L449) | [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L461) | [478](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L478) | [499](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L499) | [509](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L509) | [541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L541) | [571](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L571) | [578](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L578) | [586](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L586) | [598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L598)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit Missed @param `amount`
155: function lock(uint256 amount) public whenNotPaused {
/// @audit Missed @param `amount`
186: function withdrawWithRewards(uint256 amount) public virtual {
/// @audit Missed @param `token`
199: function rewardData(address token) external view returns (Reward memory) {
/// @audit Missed @param `rewardToken`
203: function rewardsForDuration(address rewardToken) external view returns (uint256) {
/// @audit Missed @param `user`
211: function balances(address user) external view returns (Balances memory) {
/// @audit Missed @param `user`
215: function userRewardLock(address user) external view returns (RewardLock memory) {
/// @audit Missed @param `user`
219: function userLocks(address user) external view returns (LockedBalance[] memory) {
/// @audit Missed @param `user`
223: function userLocksLength(address user) external view returns (uint256) {
/// @audit Missed @param `user`
227: function locked(address user) external view returns (uint256) {
/// @audit Missed @param `user`
231: function unlocked(address user) external view returns (uint256) {
/// @audit Missed @param `user`
239: function balanceOf(address user) public view returns (uint256) {
/// @audit Missed @param `rewardToken`
269: function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {
/// @audit Missed @param `rewardToken`
273: function rewardPerToken(address rewardToken) public view returns (uint256) {
/// @audit Missed @param `rewardToken, lastTimeRewardApplicable_, totalSupply_`
277: function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
/// @audit Missed @param `user, rewardToken`
288: function earned(address user, address rewardToken) public view returns (uint256) {
/// @audit Missed @param `user, balance_, rewardToken, rewardPerToken_`
292: function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {
/// @audit Missed @param `rewardToken`
300: function addReward(address rewardToken) public onlyOwner {
/// @audit Missed @param `_minLockAmount`
317: function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
/// @audit Missed @param `tokenAddress, tokenAmount`
324: function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {
/// @audit Missed @param `account, amount, lock_`
349: function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {
/// @audit Missed @param `users, lockIndexes`
397: function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
/// @audit Missed @param `account, amount, lock_`
458: function _stakeFor(address account, uint256 amount, bool lock_) internal {
/// @audit Missed @param `user, amount`
479: function _createLock(address user, uint256 amount) internal {
/// @audit Missed @param `token_, totalSupply_`
528: function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {
/// @audit Missed @param `user_, balance_, token_, rewardPerToken_`
536: function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
/// @audit Missed @param `user`
557: function _updateRewardsForUser(address user) internal {
/// @audit Missed @param `users`
572: function _updateRewardsForUsers(address[] memory users) internal {
/// @audit Missed @param `user`
597: function _getRewards(address user) internal {
```
[155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L155) | [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L186) | [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L203) | [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L211) | [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L215) | [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L219) | [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L223) | [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L227) | [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L231) | [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L239) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L269) | [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L273) | [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277) | [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L288) | [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L292) | [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300) | [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317) | [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L324) | [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L349) | [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397) | [458](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L458) | [479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L479) | [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L528) | [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L536) | [557](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L557) | [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L572) | [597](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L597)
</details>

### [N-33] High cyclomatic complexity

Functions with high cyclomatic complexity are harder to understand, test, and maintain.
Consider breaking down these blocks into more manageable units, by splitting things into utility functions,
by reducing nesting, and by using early returns.

[Learn More About Cyclomatic Complexity](https://en.wikipedia.org/wiki/Cyclomatic_complexity)

<details>
<summary><i>10 issue instances in 5 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

/// @audit function `init` has a cyclomatic complexity of 6
90: function init(
        address baseTokenAddress,
        address quoteTokenAddress,
        uint256 lpFeeRate,
        address mtFeeRateModel,
        uint256 i,
        uint256 k
    ) external {
/// @audit function `flashLoan` has a cyclomatic complexity of 8
289: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
/// @audit function `buyShares` has a cyclomatic complexity of 6
360: function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
```
[90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L90) | [289](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L289) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360)

```solidity
File: src/mimswap/libraries/Math.sol

/// @audit function `_SolveQuadraticFunctionForTrade` has a cyclomatic complexity of 14
131: function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```
[131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

/// @audit function `sellBaseToken` has a cyclomatic complexity of 7
38: function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {
/// @audit function `sellQuoteToken` has a cyclomatic complexity of 7
75: function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L38) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L75)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit function `previewAddLiquidity` has a cyclomatic complexity of 7
111: function previewAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit function `_swap` has a cyclomatic complexity of 6
540: function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {
```
[111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L111) | [540](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L540)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit function `processExpiredLocks` has a cyclomatic complexity of 7
397: function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
/// @audit function `_getRewards` has a cyclomatic complexity of 6
597: function _getRewards(address user) internal {
```
[397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397) | [597](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L597)
</details>

### [N-34] Contract should expose an `interface`

Exposing an interface in a smart contract allows for easier integration by other projects and developers.
Without an interface, there's a risk that other projects will have to develop non-standard variants to interact with your contract.
It's highly recommended to define an interface for clearer and more robust collaboration.

<details>
<summary><i>124 issue instances in 11 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

51: function claimGasYields() external onlyOperators returns (uint256) {
55: function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
67: function callBlastPrecompile(bytes calldata data) external onlyOwner {
71: function setFeeTo(address feeTo_) external onlyOwner {
80: function setTokenEnabled(address token, bool enabled) external onlyOwner {
```
[51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L51) | [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L55) | [67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L67) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L71) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L80)

```solidity
File: src/blast/BlastGovernor.sol

27: function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
31: function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
39: function setFeeTo(address _feeTo) external onlyOwner {
48: function callBlastPrecompile(bytes calldata data) external onlyOwner {
52: function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```
[27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L27) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L31) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L39) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L48) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L52)

```solidity
File: src/blast/BlastMagicLP.sol

46: function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {
52: function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {
63: function updateTokenClaimables() external onlyClones onlyImplementationOperators {
71: function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {
79: function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
88: function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
103: function _updateTokenClaimables() internal {
```
[46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L46) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L52) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L63) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L71) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L79) | [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L88) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L103)

```solidity
File: src/blast/BlastOnboarding.sol

100: function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
122: function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
131: function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
146: function setFeeTo(address feeTo_) external onlyOwner {
155: function callBlastPrecompile(bytes calldata data) external onlyOwner {
159: function claimGasYields() external onlyOwner returns (uint256) {
163: function claimTokenYields(address[] memory tokens) external onlyOwner {
174: function setTokenSupported(address token, bool supported) external onlyOwner {
184: function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
189: function setBootstrapper(address bootstrapper_) external onlyOwner {
194: function open() external onlyOwner onlyState(State.Idle) {
199: function close() external onlyOwner onlyState(State.Opened) {
204: function rescue(address token, address to, uint256 amount) external onlyOwner {
213: function pause() external onlyOwner {
217: function unpause() external onlyOwner {
```
[100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L100) | [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L122) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L131) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L146) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L155) | [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L159) | [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L163) | [174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L174) | [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L184) | [189](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L189) | [194](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L194) | [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L199) | [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L204) | [213](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L213) | [217](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L217)

```solidity
File: src/blast/BlastOnboardingBoot.sol

54: function claim(bool lock) external returns (uint256 shares) {
77: function claimable(address user) external view returns (uint256 shares) {
85: function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
95: function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
128: function initialize(Router _router) external onlyOwner {
137: function setStaking(LockingMultiRewards _staking) external onlyOwner {
145: function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
154: function _claimable(address user) internal view returns (uint256 shares) {
```
[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L54) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L77) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L85) | [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L95) | [128](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L128) | [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137) | [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L145) | [154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L154)

```solidity
File: src/blast/BlastTokenRegistry.sol

13: function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L13)

```solidity
File: src/blast/BlastWrappers.sol

69: function _setupBlacklist() private {
```
[69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L69)

```solidity
File: src/mimswap/MagicLP.sol

90: function init(
        address baseTokenAddress,
        address quoteTokenAddress,
        uint256 lpFeeRate,
        address mtFeeRateModel,
        uint256 i,
        uint256 k
    ) external {
133: function sync() external nonReentrant {
137: function correctRState() external {
166: function querySellBase(
        address trader,
        uint256 payBaseAmount
    ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {
179: function querySellQuote(
        address trader,
        uint256 payQuoteAmount
    ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {
192: function getPMMState() public view returns (PMMPricing.PMMState memory state) {
203: function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
214: function getMidPrice() public view returns (uint256 midPrice) {
218: function getReserves() external view returns (uint256 baseReserve, uint256 quoteReserve) {
223: function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
227: function getBaseInput() public view returns (uint256 input) {
231: function getQuoteInput() public view returns (uint256 input) {
235: function version() external pure virtual returns (string memory) {
243: function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {
266: function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {
289: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
360: function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
413: function sellShares(
        uint256 shareAmount,
        address to,
        uint256 baseMinAmount,
        uint256 quoteMinAmount,
        bytes calldata data,
        uint256 deadline
    ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {
460: function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {
469: function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner {
503: function ratioSync() external nonReentrant onlyImplementationOwner {
527: function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {
544: function _twapUpdate() internal {
559: function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {
566: function _sync() internal {
580: function _transferBaseOut(address to, uint256 amount) internal {
586: function _transferQuoteOut(address to, uint256 amount) internal {
600: function _afterInitialized() internal virtual {}
```
[90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L90) | [133](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L133) | [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L137) | [166](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L166) | [179](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L179) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L192) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L203) | [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L214) | [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L218) | [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L223) | [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L227) | [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L231) | [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L235) | [243](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L243) | [266](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L266) | [289](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L289) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360) | [413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L413) | [460](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L460) | [469](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L469) | [503](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L503) | [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L527) | [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L544) | [559](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L559) | [566](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L566) | [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L580) | [586](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L586) | [600](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L600)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

33: function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
45: function setMaintainer(address maintainer_) external onlyOwner {
57: function setImplementation(address implementation_) public onlyOwner {
```
[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L33) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L45) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)

```solidity
File: src/mimswap/periphery/Factory.sol

52: function getPoolCount(address token0, address token1) external view returns (uint256) {
56: function getUserPoolCount(address creator) external view returns (uint256) {
64: function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address) {
80: function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
95: function setLpImplementation(address implementation_) external onlyOwner {
104: function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
116: function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {
119: function removePool(
        address creator,
        address baseToken,
        address quoteToken,
        uint256 poolIndex,
        uint256 userPoolIndex
    ) external onlyOwner {
147: function _addPool(address creator, address baseToken, address quoteToken, address pool) internal {
154: function _computeSalt(
        address sender_,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) internal view returns (bytes32) {
```
[52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L52) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L56) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L64) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L80) | [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L95) | [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L104) | [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L116) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L119) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L147) | [154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L154)

```solidity
File: src/staking/LockingMultiRewards.sol

150: function stake(uint256 amount, bool lock_) public whenNotPaused {
155: function lock(uint256 amount) public whenNotPaused {
170: function withdraw(uint256 amount) public virtual {
185: function withdrawWithRewards(uint256 amount) public virtual {
190: function getRewards() public virtual {
199: function rewardData(address token) external view returns (Reward memory) {
202: function rewardsForDuration(address rewardToken) external view returns (uint256) {
206: function rewardTokensLength() external view returns (uint256) {
210: function balances(address user) external view returns (Balances memory) {
214: function userRewardLock(address user) external view returns (RewardLock memory) {
218: function userLocks(address user) external view returns (LockedBalance[] memory) {
222: function userLocksLength(address user) external view returns (uint256) {
226: function locked(address user) external view returns (uint256) {
230: function unlocked(address user) external view returns (uint256) {
234: function totalSupply() public view returns (uint256) {
238: function balanceOf(address user) public view returns (uint256) {
253: function nextUnlockTime() public view returns (uint256) {
256: function epoch() public view returns (uint256) {
260: function nextEpoch() public view returns (uint256) {
264: function remainingEpochTime() public view returns (uint256) {
268: function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {
272: function rewardPerToken(address rewardToken) public view returns (uint256) {
276: function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
287: function earned(address user, address rewardToken) public view returns (uint256) {
291: function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {
300: function addReward(address rewardToken) public onlyOwner {
316: function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
324: function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {
337: function pause() external onlyOwner {
340: function unpause() external onlyOwner {
348: function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {
361: function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
397: function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
458: function _stakeFor(address account, uint256 amount, bool lock_) internal {
478: function _createLock(address user, uint256 amount) internal {
528: function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {
535: function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
544: function _updateRewards() internal {
557: function _updateRewardsForUser(address user) internal {
572: function _updateRewardsForUsers(address[] memory users) internal {
597: function _getRewards(address user) internal {
```
[150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L150) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L155) | [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L170) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L185) | [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L190) | [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199) | [202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L202) | [206](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L206) | [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L210) | [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L214) | [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L218) | [222](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L222) | [226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L226) | [230](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L230) | [234](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L234) | [238](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L238) | [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L253) | [256](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L256) | [260](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L260) | [264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L264) | [268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L268) | [272](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L272) | [276](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L276) | [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L287) | [291](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L291) | [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300) | [316](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L316) | [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L324) | [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337) | [340](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L340) | [348](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L348) | [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361) | [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397) | [458](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L458) | [478](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L478) | [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L528) | [535](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L535) | [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L544) | [557](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L557) | [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L572) | [597](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L597)
</details>

### [N-35] NatSpec: Function declarations should have descriptions

The Ethereum Natural Specification Format (NatSpec) is an integral part of the Solidity language, serving as a rich, machine-readable, language-agnostic metadata tool.

Documenting all functions, irrespective of their visibility, significantly enhances code readability and auditability.
This is especially vital in complex projects, where clear comprehension of functions, their arguments, and returns is paramount.

Specifically, the `@notice` tag should be used for explanations that anyone should understand, making it a key element in providing a clear understanding of a function's intention.
[More information in Documentation](https://docs.soliditylang.org/en/develop/natspec-format.html)

<details>
<summary><i>135 issue instances in 15 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

7: constructor() {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L7)

```solidity
File: src/blast/BlastBox.sol

24: constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
52: function claimGasYields() external onlyOperators returns (uint256) {
56: function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
68: function callBlastPrecompile(bytes calldata data) external onlyOwner {
72: function setFeeTo(address feeTo_) external onlyOwner {
81: function setTokenEnabled(address token, bool enabled) external onlyOwner {
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L52) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L56) | [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L68) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81)

```solidity
File: src/blast/BlastGovernor.sol

15: constructor(address feeTo_, address _owner) OperatableV2(_owner) {
28: function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
32: function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
40: function setFeeTo(address _feeTo) external onlyOwner {
49: function callBlastPrecompile(bytes calldata data) external onlyOwner {
53: function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```
[15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L28) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L32) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L49) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)

```solidity
File: src/blast/BlastMagicLP.sol

23: constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
39: function version() external pure override returns (string memory) {
47: function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {
53: function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {
64: function updateTokenClaimables() external onlyClones onlyImplementationOperators {
72: function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {
80: function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
89: function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L39) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L47) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L53) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L64) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L72) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89)

```solidity
File: src/blast/BlastOnboarding.sol

58: constructor() Owned(msg.sender) {
101: function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
123: function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
132: function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
147: function setFeeTo(address feeTo_) external onlyOwner {
156: function callBlastPrecompile(bytes calldata data) external onlyOwner {
160: function claimGasYields() external onlyOwner returns (uint256) {
164: function claimTokenYields(address[] memory tokens) external onlyOwner {
175: function setTokenSupported(address token, bool supported) external onlyOwner {
185: function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
190: function setBootstrapper(address bootstrapper_) external onlyOwner {
195: function open() external onlyOwner onlyState(State.Idle) {
200: function close() external onlyOwner onlyState(State.Opened) {
205: function rescue(address token, address to, uint256 amount) external onlyOwner {
214: function pause() external onlyOwner {
218: function unpause() external onlyOwner {
```
[58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L58) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101) | [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L156) | [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L160) | [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164) | [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185) | [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190) | [195](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L195) | [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L200) | [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L205) | [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L214) | [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L218)

```solidity
File: src/blast/BlastOnboardingBoot.sol

55: function claim(bool lock) external returns (uint256 shares) {
78: function claimable(address user) external view returns (uint256 shares) {
86: function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
96: function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
129: function initialize(Router _router) external onlyOwner {
137: function setStaking(LockingMultiRewards _staking) external onlyOwner {
146: function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
```
[55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L55) | [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L78) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96) | [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129) | [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146)

```solidity
File: src/blast/BlastTokenRegistry.sol

12: constructor(address _owner) Owned(_owner) {}
14: function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14)

```solidity
File: src/blast/BlastWrappers.sol

20: constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
59: function init(bytes calldata data) public payable override {
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59)

```solidity
File: src/mimswap/MagicLP.sol

84: constructor(address owner_) Owned(owner_) {
91: function init(
        address baseTokenAddress,
        address quoteTokenAddress,
        uint256 lpFeeRate,
        address mtFeeRateModel,
        uint256 i,
        uint256 k
    ) external {
134: function sync() external nonReentrant {
138: function correctRState() external {
155: function name() public view override returns (string memory) {
159: function symbol() public pure override returns (string memory) {
163: function decimals() public view override returns (uint8) {
167: function querySellBase(
        address trader,
        uint256 payBaseAmount
    ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {
180: function querySellQuote(
        address trader,
        uint256 payQuoteAmount
    ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {
193: function getPMMState() public view returns (PMMPricing.PMMState memory state) {
204: function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
215: function getMidPrice() public view returns (uint256 midPrice) {
219: function getReserves() external view returns (uint256 baseReserve, uint256 quoteReserve) {
224: function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
228: function getBaseInput() public view returns (uint256 input) {
232: function getQuoteInput() public view returns (uint256 input) {
236: function version() external pure virtual returns (string memory) {
244: function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {
267: function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {
290: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
360: function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
413: function sellShares(
        uint256 shareAmount,
        address to,
        uint256 baseMinAmount,
        uint256 quoteMinAmount,
        bytes calldata data,
        uint256 deadline
    ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {
461: function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {
470: function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner {
504: function ratioSync() external nonReentrant onlyImplementationOwner {
```
[84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L91) | [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L134) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L138) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155) | [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L159) | [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163) | [167](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L167) | [180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L180) | [193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L193) | [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204) | [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L215) | [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L219) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L224) | [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L228) | [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L232) | [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L236) | [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L244) | [267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L267) | [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360) | [413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L413) | [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L461) | [470](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470) | [504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L504)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

22: constructor(address maintainer_, address owner_) Owned(owner_) {
34: function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
46: function setMaintainer(address maintainer_) external onlyOwner {
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

9: function getFeeRate(
        address /*pool*/,
        address /*trader*/,
        uint256 lpFeeRate
    ) external pure returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9)

```solidity
File: src/mimswap/periphery/Factory.sol

38: constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
53: function getPoolCount(address token0, address token1) external view returns (uint256) {
57: function getUserPoolCount(address creator) external view returns (uint256) {
65: function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address) {
81: function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
96: function setLpImplementation(address implementation_) external onlyOwner {
105: function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
120: function removePool(
        address creator,
        address baseToken,
        address quoteToken,
        uint256 poolIndex,
        uint256 userPoolIndex
    ) external onlyOwner {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L53) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L57) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96) | [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105) | [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L120)

```solidity
File: src/mimswap/periphery/Router.sol

38: constructor(IWETH weth_, IFactory factory_) {
54: function createPool(
        address baseToken,
        address quoteToken,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external returns (address clone, uint256 shares) {
73: function createPoolETH(
        address token,
        bool useTokenAsQuote,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 tokenInAmount
    ) external payable returns (address clone, uint256 shares) {
96: function previewCreatePool(
        uint256 i,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external pure returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
112: function previewAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
162: function addLiquidity(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
178: function addLiquidityUnsafe(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 shares) {
192: function addLiquidityETH(
        address lp,
        address to,
        address payable refundTo,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
229: function addLiquidityETHUnsafe(
        address lp,
        address to,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 shares) {
251: function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
261: function removeLiquidity(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumBaseAmount,
        uint256 minimumQuoteAmount,
        uint256 deadline
    ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
274: function removeLiquidityETH(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumETHAmount,
        uint256 minimumTokenAmount,
        uint256 deadline
    ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {
314: function swapTokensForTokens(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
336: function swapETHForTokens(
        address to,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
365: function swapTokensForETH(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
404: function sellBaseTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
415: function sellBaseETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
432: function sellBaseTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
449: function sellQuoteTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
461: function sellQuoteETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
478: function sellQuoteTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L54) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L73) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L96) | [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L112) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L162) | [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L178) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192) | [229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229) | [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L251) | [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L261) | [274](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L274) | [314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L314) | [336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336) | [365](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L365) | [404](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L404) | [415](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L415) | [432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L432) | [449](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L449) | [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L461) | [478](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L478)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

21: constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
29: function decimals() external pure override returns (uint8) {
37: function latestAnswer() public view override returns (int256) {
48: function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L29) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L37) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L48)

```solidity
File: src/staking/LockingMultiRewards.sol

186: function withdrawWithRewards(uint256 amount) public virtual {
191: function getRewards() public virtual {
199: function rewardData(address token) external view returns (Reward memory) {
203: function rewardsForDuration(address rewardToken) external view returns (uint256) {
207: function rewardTokensLength() external view returns (uint256) {
211: function balances(address user) external view returns (Balances memory) {
215: function userRewardLock(address user) external view returns (RewardLock memory) {
219: function userLocks(address user) external view returns (LockedBalance[] memory) {
223: function userLocksLength(address user) external view returns (uint256) {
227: function locked(address user) external view returns (uint256) {
231: function unlocked(address user) external view returns (uint256) {
235: function totalSupply() public view returns (uint256) {
239: function balanceOf(address user) public view returns (uint256) {
257: function epoch() public view returns (uint256) {
261: function nextEpoch() public view returns (uint256) {
265: function remainingEpochTime() public view returns (uint256) {
269: function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {
273: function rewardPerToken(address rewardToken) public view returns (uint256) {
277: function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
288: function earned(address user, address rewardToken) public view returns (uint256) {
300: function addReward(address rewardToken) public onlyOwner {
317: function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
337: function pause() external onlyOwner {
341: function unpause() external onlyOwner {
349: function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {
```
[186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L186) | [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L191) | [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L203) | [207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L207) | [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L211) | [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L215) | [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L219) | [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L223) | [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L227) | [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L231) | [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L235) | [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L239) | [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L257) | [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L261) | [265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L265) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L269) | [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L273) | [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277) | [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L288) | [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300) | [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317) | [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337) | [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L341) | [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L349)
</details>

### [N-36] Contract uses both `require()`/`revert()` as well as custom errors

The contract uses both `require()/revert()` and `custom errors` for error handling.

It's recommended to use a consistent approach for error handling in a single file.

<details>
<summary><i>12 issue instances in 12 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

12: contract BlastBox is DegenBox, OperatableV3 {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L12)

```solidity
File: src/blast/BlastGovernor.sol

6: contract BlastGovernor is OperatableV2 {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L6)

```solidity
File: src/blast/BlastMagicLP.sol

9: contract BlastMagicLP is MagicLP {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L9)

```solidity
File: src/blast/BlastOnboarding.sol

11: contract BlastOnboardingData is Owned, Pausable {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L11)

```solidity
File: src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23)

```solidity
File: src/blast/BlastTokenRegistry.sol

5: contract BlastTokenRegistry is Owned {
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L5)

```solidity
File: src/blast/BlastWrappers.sol

18: contract BlastMIMSwapRouter is Router {
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L18)

```solidity
File: src/mimswap/MagicLP.sol

25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L25)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

12: contract FeeRateModel is Owned {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L12)

```solidity
File: src/mimswap/periphery/Factory.sol

11: contract Factory is Owned {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L11)

```solidity
File: src/mimswap/periphery/Router.sol

11: contract Router {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L11)

```solidity
File: src/staking/LockingMultiRewards.sol

14: contract LockingMultiRewards is OperatableV2, Pausable {
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L14)
</details>

### [N-37] Modifiers Missing NatSpec `@param` Tag

Function modifiers should include NatSpec comments with `@param` tags describing each input parameter.
This promotes better code readability and documentation.

<details>
<summary><i>3 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit Missed @param `_state`
43: modifier onlyState(State _state) {
/// @audit Missed @param `token`
50: modifier onlySupportedTokens(address token) {
```
[43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L43) | [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L50)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit Missed @param `deadline`
47: modifier ensureDeadline(uint256 deadline) {
```
[47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L47)
</details>

### [N-38] Inconsistent spacing in comments

Some lines use // x and some use //x. The instances below point out the usages that don't follow the majority, within each file:

<details>
<summary><i>195 issue instances in 13 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

48: //////////////////////////////////////////////////////////////////////////////////////
49: /// OPERATORS
50: //////////////////////////////////////////////////////////////////////////////////////
64: //////////////////////////////////////////////////////////////////////////////////////
65: /// ADMIN
66: //////////////////////////////////////////////////////////////////////////////////////
93: //////////////////////////////////////////////////////////////////////////////////////
94: /// INTERNALS
95: //////////////////////////////////////////////////////////////////////////////////////
97: /// @dev Called on DegenBox's constructor
```
[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L48) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L49) | [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L50) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L64) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L65) | [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L66) | [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L93) | [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L94) | [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L95) | [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L97)

```solidity
File: src/blast/BlastGovernor.sol

24: //////////////////////////////////////////////////////////////////////////////////////
25: /// OPERATORS
26: //////////////////////////////////////////////////////////////////////////////////////
36: //////////////////////////////////////////////////////////////////////////////////////
37: /// ADMIN
38: //////////////////////////////////////////////////////////////////////////////////////
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L24) | [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L25) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L26) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L36) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L37) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L38)

```solidity
File: src/blast/BlastMagicLP.sol

19: /// @dev Implementation storage
35: //////////////////////////////////////////////////////////////////////////////////////
36: /// VIEWS
37: //////////////////////////////////////////////////////////////////////////////////////
43: //////////////////////////////////////////////////////////////////////////////////////
44: /// OPERATORS / CLONES ONLY
45: //////////////////////////////////////////////////////////////////////////////////////
68: //////////////////////////////////////////////////////////////////////////////////////
69: /// ADMIN / CLONES ONLY
70: //////////////////////////////////////////////////////////////////////////////////////
76: //////////////////////////////////////////////////////////////////////////////////////
77: /// ADMIN / IMPLEMENTATION ONLY
78: //////////////////////////////////////////////////////////////////////////////////////
94: //////////////////////////////////////////////////////////////////////////////////////
95: /// INTERNALS
96: //////////////////////////////////////////////////////////////////////////////////////
114: //////////////////////////////////////////////////////////////////////////////////////
115: /// MODIFIERS
116: //////////////////////////////////////////////////////////////////////////////////////
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L19) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L35) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L36) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L37) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L43) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L44) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L45) | [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L68) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L69) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L70) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L76) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L77) | [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L78) | [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L94) | [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L95) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L96) | [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L114) | [115](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L115) | [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L116)

```solidity
File: src/blast/BlastOnboarding.sol

97: //////////////////////////////////////////////////////////////////////////////////////
98: /// PUBLIC
99: //////////////////////////////////////////////////////////////////////////////////////
143: //////////////////////////////////////////////////////////////////////////////////////
144: /// ADMIN
145: //////////////////////////////////////////////////////////////////////////////////////
222: //////////////////////////////////////////////////////////////////////////////////////
223: /// PROXY IMPLEMENTATION
224: //////////////////////////////////////////////////////////////////////////////////////
```
[97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L97) | [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L98) | [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L99) | [143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L143) | [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L144) | [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L145) | [222](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L222) | [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L223) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L224)

```solidity
File: src/blast/BlastOnboardingBoot.sol

33: /// @dev Functions are postfixed with the version number to avoid collisions
51: //////////////////////////////////////////////////////////////////////////////////////
52: /// PUBLIC
53: //////////////////////////////////////////////////////////////////////////////////////
74: //////////////////////////////////////////////////////////////////////////////////////
75: /// VIEWS
76: //////////////////////////////////////////////////////////////////////////////////////
92: //////////////////////////////////////////////////////////////////////////////////////
93: /// ADMIN
94: //////////////////////////////////////////////////////////////////////////////////////
151: //////////////////////////////////////////////////////////////////////////////////////
152: /// INTERNALS
153: //////////////////////////////////////////////////////////////////////////////////////
```
[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L33) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L51) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L52) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L53) | [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L74) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L75) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L76) | [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L92) | [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L93) | [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L94) | [151](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L151) | [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L152) | [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L153)

```solidity
File: src/blast/BlastWrappers.sol

14: /// @dev Collection of Blast wrapped contract that are succecptible to be used
15: /// enough to justify claiming gas yields.
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L14) | [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L15)

```solidity
File: src/blast/libraries/BlastYields.sol

16: //////////////////////////////////////////////////////////////////////////////////////
18: //////////////////////////////////////////////////////////////////////////////////////
34: //////////////////////////////////////////////////////////////////////////////////////
36: //////////////////////////////////////////////////////////////////////////////////////
47: //////////////////////////////////////////////////////////////////////////////////////
49: //////////////////////////////////////////////////////////////////////////////////////<
66: //////////////////////////////////////////////////////////////////////////////////////
68: //////////////////////////////////////////////////////////////////////////////////////
81: //////////////////////////////////////////////////////////////////////////////////////
84: //////////////////////////////////////////////////////////////////////////////////////
```
[16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L16) | [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L18) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L34) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L36) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L47) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L49) | [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L66) | [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L68) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L81) | [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L84)

```solidity
File: src/mimswap/MagicLP.sol

23: /// @title MIMSwap MagicLP
24: /// @author Adapted from DODOEX DSP https://github.com/DODOEX/contractV2/tree/main/contracts/DODOStablePool
130: //////////////////////////////////////////////////////////////////////////////////////
131: /// PUBLIC
132: //////////////////////////////////////////////////////////////////////////////////////
151: //////////////////////////////////////////////////////////////////////////////////////
152: /// VIEWS
153: //////////////////////////////////////////////////////////////////////////////////////
240: //////////////////////////////////////////////////////////////////////////////////////
241: /// TRADE FUNCTIONS
242: //////////////////////////////////////////////////////////////////////////////////////
355: //////////////////////////////////////////////////////////////////////////////////////
356: /// BUY & SELL SHARES
357: //////////////////////////////////////////////////////////////////////////////////////
457: //////////////////////////////////////////////////////////////////////////////////////
458: /// ADMIN
459: //////////////////////////////////////////////////////////////////////////////////////
524: //////////////////////////////////////////////////////////////////////////////////////
525: /// INTERNALS
526: //////////////////////////////////////////////////////////////////////////////////////
550: /// @dev It is desired and expected for this value to
551: /// overflow once it has hit the max of `type.uint256`.
603: //////////////////////////////////////////////////////////////////////////////////////
604: /// MODIFIERS
605: //////////////////////////////////////////////////////////////////////////////////////
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L23) | [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L24) | [130](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L130) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L131) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L132) | [151](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L151) | [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L152) | [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L153) | [240](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L240) | [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L241) | [242](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L242) | [355](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L355) | [356](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L356) | [357](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L357) | [457](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L457) | [458](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L458) | [459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L459) | [524](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L524) | [525](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L525) | [526](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L526) | [550](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L550) | [551](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L551) | [603](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L603) | [604](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L604) | [605](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L605)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

30: //////////////////////////////////////////////////////////////////////////////////////
31: /// VIEWS
32: //////////////////////////////////////////////////////////////////////////////////////
42: //////////////////////////////////////////////////////////////////////////////////////
43: /// ADMIN
44: //////////////////////////////////////////////////////////////////////////////////////
55: /// @notice Set the fee rate implementation and default fee rate
56: /// @param implementation_ The address of the fee rate implementation, use address(0) to disable
```
[30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L30) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L31) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L32) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L42) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L43) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L44) | [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L55) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L56)

```solidity
File: src/mimswap/periphery/Factory.sol

10: /// @notice Create and register MagicLP pools
49: //////////////////////////////////////////////////////////////////////////////////////
50: /// VIEWS
51: //////////////////////////////////////////////////////////////////////////////////////
61: //////////////////////////////////////////////////////////////////////////////////////
62: /// PUBLIC
63: //////////////////////////////////////////////////////////////////////////////////////
92: //////////////////////////////////////////////////////////////////////////////////////
93: /// ADMIN
94: //////////////////////////////////////////////////////////////////////////////////////
114: /// @notice Register a pool to the list
115: /// Note this doesn't check if the pool is valid or if it's already registered.
144: //////////////////////////////////////////////////////////////////////////////////////
145: /// INTERNALS
146: //////////////////////////////////////////////////////////////////////////////////////
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L10) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L49) | [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L50) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L51) | [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L61) | [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L62) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L63) | [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L92) | [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L93) | [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L94) | [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L114) | [115](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L115) | [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L144) | [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L145) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L146)

```solidity
File: src/mimswap/periphery/Router.sol

495: //////////////////////////////////////////////////////////////////////////////////////
496: /// INTERNALS
497: //////////////////////////////////////////////////////////////////////////////////////
507: /// Adapted from: https://github.com/DODOEX/contractV2/blob/main/contracts/SmartRoute/proxies/DODODspProxy.sol
508: /// Copyright 2020 DODO ZOO. Licensed under Apache-2.0.
```
[495](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L495) | [496](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L496) | [497](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L497) | [507](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L507) | [508](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L508)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

18: /// @param pair_ The MagicLP pair address
19: /// @param baseOracle_ The base oracle
20: /// @param quoteOracle_ The quote oracle
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L18) | [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L19) | [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L20)

```solidity
File: src/staking/LockingMultiRewards.sol

9: /// @notice A staking contract that distributes multiple rewards to stakers.
10: /// Stakers can lock their tokens for a period of time to get a boost on their rewards.
11: /// @author Based from Curve Finance's MultiRewards contract https://github.com/curvefi/multi-rewards/blob/master/contracts/MultiRewards.sol
12: /// @author Based from Ellipsis Finance's EpsStaker https://github.com/ellipsis-finance/ellipsis/blob/master/contracts/EpsStaker.sol
13: /// @author Based from Convex Finance's CvxLockerV2 https://github.com/convex-eth/platform/blob/main/contracts/contracts/CvxLockerV2.sol
105: ///
106: /// @dev Constructor
107: /// @param _stakingToken The token that is being staked
108: /// @param _owner The owner of the contract
109: /// @param _lockingBoostMultiplerInBips The multiplier for the locking boost. 30000 means if you stake 100, you get 300 locked
110: /// @param _rewardsDuration The duration of the rewards period in seconds, should be 7 days by default.
111: /// @param _lockDuration The duration of the lock period in seconds, should be 13 weeks by default.
147: /// @notice Stakes the given amount of tokens for the given user.
148: /// @param amount The amount of tokens to stake
149: /// @param lock_ If true, the tokens will be locked for the lock duration for a reward boost
154: /// @notice Locks an existing unlocked balance.
168: /// @notice Withdraws the given amount of unlocked tokens for the given user.
169: /// @param amount The amount of unlocked tokens to withdraw
196: //////////////////////////////////////////////////////////////////////////////////////////////
197: /// VIEWS
198: //////////////////////////////////////////////////////////////////////////////////////////////
244: /// @dev Calculates when the next unlock event will occur given the current epoch.
245: /// It ensures that the unlock timing coincides with the intervals at which rewards are distributed.
246: /// If the current time is within an ongoing reward interval, the function establishes the
247: /// unlock period to begin at the next epoch.
248: /// So, if you stake at week 1 + 4 days, you will be able to unlock at the end of week 14.
297: //////////////////////////////////////////////////////////////////////////////////////////////
298: /// ADMIN
299: //////////////////////////////////////////////////////////////////////////////////////////////
322: /// @notice This function can recover any token except for the staking token beyond the balance necessary for rewards.
323: /// WARNING: Use this function with caution to ensure it does not affect the reward mechanism.
334: //////////////////////////////////////////////////////////////////////////////////////////////
335: /// EMERGENCY FUNCTIONS
336: //////////////////////////////////////////////////////////////////////////////////////////////
345: //////////////////////////////////////////////////////////////////////////////////////////////
346: /// OPERATORS
347: //////////////////////////////////////////////////////////////////////////////////////////////
353: /// @notice Distribute new rewards to the stakers
354: /// @param rewardToken The address of the reward token
355: /// @param amount The amount of reward tokens to distribute
356: /// @param minRemainingTime The minimum remaining time for the current reward period
357: /// Used to avoid distributing rewards on a lower period than the expected one.
358: /// Example: If the reward period is 7 days, and there are 2 days left, `minRemainingTime` higher than
359: /// 2 days will revert the transaction.
360: /// To ignore this check, set `minRemainingTime` to 0.
395: /// @notice Updates the balances of the given user and lock indexes
429: /// Last lock index changed place with the one we just swapped.
455: //////////////////////////////////////////////////////////////////////////////////////////////
456: /// INTERNALS
457: //////////////////////////////////////////////////////////////////////////////////////////////
508: /// It's the same reward period, so we just add the amount to the current lock
516: /// @dev Update the global accumulated rewards from the last update to this point,
517: /// in relation with the `totalSupply`
518: ///
519: /// The idea is to allow everyone that are currently part of that supply to get their allocated
520: /// reward share.
521: ///
522: /// Each user's reward share is taking in account when `rewards[user][token] = _earned(...)`
523: /// is called. And only updated when a user is interacting with `stake`, `lock`, `withdraw`
524: /// or `getRewards`.
525: ///
526: /// Otherwise, if it's yet-to-be-updated, it's going to get considered as part of the pending
527: /// yet-to-receive rewards in the `earned` function.
541: /// @dev Simplest version of updating rewards. Mainly used by `notifyRewardAmount`.
542: /// where we don't need to update any particular user but the global state for
543: /// each reward tokens only.
555: /// @dev More gas efficient version of `_updateRewards` when we
556: /// only need to update the rewards for a single user.
571: /// @dev `_updateRewardsForUser` for multiple users.
595: /// @notice Claim unlocked rewards or create a new reward lock that
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L9) | [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L10) | [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L11) | [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L12) | [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L13) | [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L105) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L106) | [107](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L107) | [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L108) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L109) | [110](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L110) | [111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L111) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L147) | [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L148) | [149](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L149) | [154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L154) | [168](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L168) | [169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L169) | [196](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L196) | [197](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L197) | [198](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L198) | [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L244) | [245](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L245) | [246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L246) | [247](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L247) | [248](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L248) | [297](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L297) | [298](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L298) | [299](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L299) | [322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L322) | [323](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L323) | [334](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L334) | [335](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L335) | [336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L336) | [345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L345) | [346](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L346) | [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L347) | [353](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L353) | [354](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L354) | [355](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L355) | [356](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L356) | [357](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L357) | [358](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L358) | [359](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L359) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L360) | [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L395) | [429](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L429) | [455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L455) | [456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L456) | [457](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L457) | [508](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L508) | [516](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L516) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L517) | [518](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L518) | [519](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L519) | [520](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L520) | [521](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L521) | [522](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L522) | [523](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L523) | [524](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L524) | [525](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L525) | [526](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L526) | [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L527) | [541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L541) | [542](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L542) | [543](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L543) | [555](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L555) | [556](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L556) | [571](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L571) | [595](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L595)
</details>

### [N-39] Unused `error` definition

Custom errors that aren't utilized within the contract add unnecessary complexity to the codebase. 
Cleaning up and removing these unused custom errors can enhance the readability and maintainability of the contract.

<details>
<summary><i>5 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit Custom Error `ErrWrongFeeRateModel` declared but never used
46: error ErrWrongFeeRateModel();
```
[46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L46)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit Custom Error `ErrInvalidSignature` declared but never used
43: error ErrInvalidSignature();
```
[43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L43)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit Custom Error `ErrBadPath` declared but never used
21: error ErrBadPath();
/// @audit Custom Error `ErrInvalidQuoteTarget` declared but never used
27: error ErrInvalidQuoteTarget();
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L21) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L27)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit Custom Error `ErrNotExpired` declared but never used
34: error ErrNotExpired();
```
[34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L34)
</details>

### [N-40] Critical system parameter changes should be behind a timelock

It is a good practice to give time for users to react and adjust to critical changes. A timelock provides more guarantees and reduces the level of trust required, thus decreasing risk for users. It also indicates that the project is legitimate (less risk of a malicious owner making a sandwich attack on a user).

<details>
<summary><i>18 issue instances in 10 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

71: function setFeeTo(address feeTo_) external onlyOwner {
80: function setTokenEnabled(address token, bool enabled) external onlyOwner {
```
[71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L71) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L80)

```solidity
File: src/blast/BlastGovernor.sol

39: function setFeeTo(address _feeTo) external onlyOwner {
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L39)

```solidity
File: src/blast/BlastMagicLP.sol

79: function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
88: function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```
[79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L79) | [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L88)

```solidity
File: src/blast/BlastOnboarding.sol

146: function setFeeTo(address feeTo_) external onlyOwner {
174: function setTokenSupported(address token, bool supported) external onlyOwner {
184: function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
189: function setBootstrapper(address bootstrapper_) external onlyOwner {
```
[146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L146) | [174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L174) | [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L184) | [189](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L189)

```solidity
File: src/blast/BlastOnboardingBoot.sol

137: function setStaking(LockingMultiRewards _staking) external onlyOwner {
145: function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
```
[137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137) | [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L145)

```solidity
File: src/blast/BlastTokenRegistry.sol

13: function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L13)

```solidity
File: src/mimswap/MagicLP.sol

469: function setParameters(
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
[469](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L469)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

45: function setMaintainer(address maintainer_) external onlyOwner {
57: function setImplementation(address implementation_) public onlyOwner {
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L45) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)

```solidity
File: src/mimswap/periphery/Factory.sol

95: function setLpImplementation(address implementation_) external onlyOwner {
104: function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
```
[95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L95) | [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L104)

```solidity
File: src/staking/LockingMultiRewards.sol

316: function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
```
[316](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L316)
</details>

### [N-41] Outdated Solidity Version

The current Solidity version used in the contract is outdated.
Consider using a more recent version for improved features and security.

0.8.4: bytes.concat() instead of abi.encodePacked(,)

0.8.12: string.concat() instead of abi.encodePacked(,)

0.8.13: Ability to use using for with a list of free functions

0.8.14:
    ABI Encoder: When ABI-encoding values from calldata that contain nested arrays, correctly validate the nested array length against calldatasize() in all cases. Override Checker: Allow changing data location for parameters only when overriding external functions.

0.8.15:
    Code Generation: Avoid writing dirty bytes to storage when copying bytes arrays. Yul Optimizer: Keep all memory side-effects of inline assembly blocks.

0.8.16:
    Code Generation: Fix data corruption that affected ABI-encoding of calldata values represented by tuples: structs at any nesting level; argument lists of external functions, events and errors; return value lists of external functions. The 32 leading bytes of the first dynamically-encoded value in the tuple would get zeroed when the last component contained a statically-encoded array.

0.8.17:
    Yul Optimizer: Prevent the incorrect removal of storage writes before calls to Yul functions that conditionally terminate the external EVM call.

<details>
<summary><i>20 issue instances in 20 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2)

```solidity
File: src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L3)

```solidity
File: src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L2)

```solidity
File: src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L3)

```solidity
File: src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L2)

```solidity
File: src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L2)

```solidity
File: src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L2)

```solidity
File: src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L2)

```solidity
File: src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L2)

```solidity
File: src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L2)

```solidity
File: src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L7)

```solidity
File: src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L8)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L8)

```solidity
File: src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L2)

```solidity
File: src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L2)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L2)

```solidity
File: src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L2)
</details>

### [N-42] Ensure Non-Empty Check for Bytes in Function Parameters

To avoid mistakenly accepting empty bytes as valid parameters, it is advisable to implement checks for non-empty bytes within functions.
This ensures that empty bytes are not treated as valid inputs, preventing potential issues.

<details>
<summary><i>6 issue instances in 5 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

67: function callBlastPrecompile(bytes calldata data) external onlyOwner {
```
[67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L67)

```solidity
File: src/blast/BlastGovernor.sol

48: function callBlastPrecompile(bytes calldata data) external onlyOwner {
52: function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```
[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L48) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L52)

```solidity
File: src/blast/BlastMagicLP.sol

71: function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {
```
[71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L71)

```solidity
File: src/blast/BlastOnboarding.sol

155: function callBlastPrecompile(bytes calldata data) external onlyOwner {
```
[155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L155)

```solidity
File: src/blast/BlastWrappers.sol

58: function init(bytes calldata data) public payable override {
```
[58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L58)
</details>

### [N-43] Adding a `return` statement when the function defines a named return variable, is redundant

Functions in Solidity can use named return variables which can enhance readability and reduce the complexity of the code. When using named return variables, a return statement without any parameters is implicitly added to the end of the function.
This means that explicitly writing return in a function that uses named return variables is redundant.
This redundancy could lead to confusion and misinterpretation of the function's behavior, particularly for developers who are new to the Solidity language or to the codebase.

Moreover, explicitly stating the return statement with the named variables might give the impression that the function could have different exit points or that it might return different values, which is not the case here.
Therefore, removing these redundant return statements can lead to cleaner, more maintainable code with reduced cognitive load for developers.
This helps in understanding the flow and the logic of the function at a quick glance and aids in faster debugging and fewer mistakes.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

/// @audit - Redundant `return (lpFeeRate - mtFeeRate, mtFeeRate);` when function has named return variables
9: function getFeeRate(
        address /*pool*/,
        address /*trader*/,
        uint256 lpFeeRate
    ) external pure returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9)
</details>

### [N-44] Use `bytes.concat()` instead of `abi.encodePacked()`

Solidity version 0.8.4 introduces `bytes.concat()` for concatenating byte arrays, which is more efficient than using `abi.encodePacked()`.
It is recommended to use `bytes.concat()` instead of `abi.encodePacked()` and upgrade to at least Solidity version 0.8.4 if required.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

156: return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));
```
[156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L156)

```solidity
File: src/mimswap/periphery/Factory.sol

163: return keccak256(abi.encodePacked(sender_, implementation, baseToken_, quoteToken_, lpFeeRate_, i_, k_));
```
[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L163)
</details>

### [N-45] Function/Constructor Argument Names Not in mixedCase

Underscore before of after function argument names is a common convention in Solidity NOT a documentation requirement.

Function arguments should use mixedCase for better readability and consistency with Solidity style guidelines. 
Examples of good practice include: initialSupply, account, recipientAddress, senderAddress, newOwner. 
[More information in Documentation](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#function-argument-names)

Rule exceptions
- Allow constant variable name/symbol/decimals to be lowercase (ERC20).
- Allow `_` at the beginning of the mixedCase match for `private variables` and `unused parameters`.

<details>
<summary><i>40 issue instances in 13 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

55: function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
71: function setFeeTo(address feeTo_) external onlyOwner {
102: function isOwner(address _account) internal view override returns (bool) {
23: constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
```
[55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L55) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L71) | [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L102) | [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L23)

```solidity
File: src/blast/BlastGovernor.sol

39: function setFeeTo(address _feeTo) external onlyOwner {
14: constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L39) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L14)

```solidity
File: src/blast/BlastMagicLP.sol

79: function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
22: constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
```
[79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L79) | [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L22)

```solidity
File: src/blast/BlastOnboarding.sol

100: function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
146: function setFeeTo(address feeTo_) external onlyOwner {
189: function setBootstrapper(address bootstrapper_) external onlyOwner {
83: constructor(BlastTokenRegistry registry_, address feeTo_) {
```
[100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L100) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L146) | [189](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L189) | [83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L83)

```solidity
File: src/blast/BlastOnboardingBoot.sol

128: function initialize(Router _router) external onlyOwner {
137: function setStaking(LockingMultiRewards _staking) external onlyOwner {
145: function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
```
[128](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L128) | [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137) | [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L145)

```solidity
File: src/blast/BlastWrappers.sol

20: constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
29: constructor(
        address implementation_,
        IFeeRateModel maintainerFeeRateModel_,
        address owner_,
        address governor_
    ) Factory(implementation_, maintainerFeeRateModel_, owner_) {
46: constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L29) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L46)

```solidity
File: src/blast/libraries/BlastYields.sol

28: function configureDefaultClaimables(address governor_) internal {
```
[28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L28)

```solidity
File: src/mimswap/MagicLP.sol

83: constructor(address owner_) Owned(owner_) {
```
[83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L83)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

45: function setMaintainer(address maintainer_) external onlyOwner {
57: function setImplementation(address implementation_) public onlyOwner {
21: constructor(address maintainer_, address owner_) Owned(owner_) {
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L45) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L21)

```solidity
File: src/mimswap/periphery/Factory.sol

64: function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address) {
80: function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
95: function setLpImplementation(address implementation_) external onlyOwner {
104: function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
154: function _computeSalt(
        address sender_,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) internal view returns (bytes32) {
37: constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
```
[64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L64) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L80) | [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L95) | [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L104) | [154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L154) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L37)

```solidity
File: src/mimswap/periphery/Router.sol

37: constructor(IWETH weth_, IFactory factory_) {
```
[37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L37)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

21: constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21)

```solidity
File: src/staking/LockingMultiRewards.sol

150: function stake(uint256 amount, bool lock_) public whenNotPaused {
276: function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
291: function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {
316: function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
348: function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {
458: function _stakeFor(address account, uint256 amount, bool lock_) internal {
528: function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {
535: function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
112: constructor(
        address _stakingToken,
        uint256 _lockingBoostMultiplerInBips,
        uint256 _rewardsDuration,
        uint256 _lockDuration,
        address _owner
    ) OperatableV2(_owner) {
```
[150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L150) | [276](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L276) | [291](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L291) | [316](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L316) | [348](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L348) | [458](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L458) | [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L528) | [535](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L535) | [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L112)
</details>

### [N-46] NatSpec: Function `@return` tag is missing

Natural Specification (NatSpec) comments are crucial for understanding the role of function arguments in your Solidity code.
Including `@return` tag will not only improve your code's readability but also its maintainability by clearly defining each argument's purpose.

[More information in Documentation](https://docs.soliditylang.org/en/develop/natspec-format.html)

<details>
<summary><i>119 issue instances in 16 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

/// @audit Missed @return ``
52: function claimGasYields() external onlyOperators returns (uint256) {
/// @audit Missed @return `amount`
56: function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
/// @audit Missed @return ``
103: function isOwner(address _account) internal view override returns (bool) {
```
[52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L52) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L56) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L103)

```solidity
File: src/blast/BlastGovernor.sol

/// @audit Missed @return ``
28: function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
/// @audit Missed @return ``
32: function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
/// @audit Missed @return `success, result`
53: function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```
[28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L28) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L32) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit Missed @return ``
39: function version() external pure override returns (string memory) {
/// @audit Missed @return ``
47: function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {
/// @audit Missed @return `token0Amount, token1Amount`
53: function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L39) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L47) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L53)

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit Missed @return ``
160: function claimGasYields() external onlyOwner returns (uint256) {
/// @audit Missed @return ``
226: function _implementation() internal view override returns (address) {
```
[160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L160) | [226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L226)

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit Missed @return `shares`
55: function claim(bool lock) external returns (uint256 shares) {
/// @audit Missed @return `shares`
78: function claimable(address user) external view returns (uint256 shares) {
/// @audit Missed @return `baseAdjustedInAmount, quoteAdjustedInAmount, shares`
86: function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit Missed @return `, , `
96: function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
/// @audit Missed @return `shares`
155: function _claimable(address user) internal view returns (uint256 shares) {
```
[55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L55) | [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L78) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L155)

```solidity
File: src/blast/libraries/BlastYields.sol

/// @audit Missed @return ``
38: function claimMaxGasYields(address recipient) internal returns (uint256) {
/// @audit Missed @return `amount`
42: function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {
/// @audit Missed @return `amount`
51: function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
/// @audit Missed @return `amount`
55: function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {
/// @audit Missed @return ``
60: function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {
/// @audit Missed @return `amount`
70: function claimAllTokenYields(address token, address recipient) internal returns (uint256 amount) {
/// @audit Missed @return ``
75: function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L38) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L42) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L51) | [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L55) | [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L60) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L70) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L75)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit Missed @return ``
155: function name() public view override returns (string memory) {
/// @audit Missed @return ``
159: function symbol() public pure override returns (string memory) {
/// @audit Missed @return ``
163: function decimals() public view override returns (uint8) {
/// @audit Missed @return `receiveQuoteAmount, mtFee, newRState, newBaseTarget`
167: function querySellBase(
        address trader,
        uint256 payBaseAmount
    ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {
/// @audit Missed @return `receiveBaseAmount, mtFee, newRState, newQuoteTarget`
180: function querySellQuote(
        address trader,
        uint256 payQuoteAmount
    ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {
/// @audit Missed @return `state`
193: function getPMMState() public view returns (PMMPricing.PMMState memory state) {
/// @audit Missed @return `i, K, B, Q, B0, Q0, R`
204: function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
/// @audit Missed @return `midPrice`
215: function getMidPrice() public view returns (uint256 midPrice) {
/// @audit Missed @return `baseReserve, quoteReserve`
219: function getReserves() external view returns (uint256 baseReserve, uint256 quoteReserve) {
/// @audit Missed @return `lpFeeRate, mtFeeRate`
224: function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
/// @audit Missed @return `input`
228: function getBaseInput() public view returns (uint256 input) {
/// @audit Missed @return `input`
232: function getQuoteInput() public view returns (uint256 input) {
/// @audit Missed @return ``
236: function version() external pure virtual returns (string memory) {
/// @audit Missed @return `receiveQuoteAmount`
244: function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {
/// @audit Missed @return `receiveBaseAmount`
267: function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {
/// @audit Missed @return `shares, baseInput, quoteInput`
360: function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
/// @audit Missed @return `baseAmount, quoteAmount`
413: function sellShares(
        uint256 shareAmount,
        address to,
        uint256 baseMinAmount,
        uint256 quoteMinAmount,
        bytes calldata data,
        uint256 deadline
    ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {
/// @audit Missed @return `baseBalance, quoteBalance`
528: function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {
```
[155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155) | [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L159) | [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163) | [167](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L167) | [180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L180) | [193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L193) | [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204) | [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L215) | [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L219) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L224) | [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L228) | [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L232) | [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L236) | [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L244) | [267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L267) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360) | [413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L413) | [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L528)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit Missed @return `adjustedLpFeeRate, mtFeeRate`
34: function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
[34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

/// @audit Missed @return `adjustedLpFeeRate, mtFeeRate`
9: function getFeeRate(
        address /*pool*/,
        address /*trader*/,
        uint256 lpFeeRate
    ) external pure returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

/// @audit Missed @return ``
23: function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {
/// @audit Missed @return ``
27: function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {
/// @audit Missed @return ``
31: function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {
/// @audit Missed @return ``
35: function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {
/// @audit Missed @return ``
39: function reciprocalFloor(uint256 target) internal pure returns (uint256) {
/// @audit Missed @return ``
43: function reciprocalCeil(uint256 target) internal pure returns (uint256) {
/// @audit Missed @return ``
47: function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L23) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L27) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L31) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L35) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L39) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L43) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L47)

```solidity
File: src/mimswap/libraries/Math.sol

/// @audit Missed @return ``
19: function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {
/// @audit Missed @return `y`
29: function sqrt(uint256 x) internal pure returns (uint256 y) {
/// @audit Missed @return ``
51: function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {
/// @audit Missed @return ``
79: function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
/// @audit Missed @return ``
131: function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L19) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L29) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L79) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

/// @audit Missed @return `receiveQuoteAmount, newR`
39: function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {
/// @audit Missed @return `receiveBaseAmount, newR`
76: function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {
/// @audit Missed @return `receiveQuoteToken`
104: function _ROneSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
/// @audit Missed @return `receiveBaseToken`
119: function _ROneSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
/// @audit Missed @return `receiveBaseToken`
134: function _RBelowSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
/// @audit Missed @return `receiveQuoteToken`
147: function _RBelowSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
/// @audit Missed @return `receiveQuoteToken`
162: function _RAboveSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
/// @audit Missed @return `receiveBaseToken`
175: function _RAboveSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
/// @audit Missed @return ``
203: function getMidPrice(PMMState memory state) internal pure returns (uint256) {
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L39) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L76) | [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L104) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L119) | [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L134) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L147) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L162) | [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L175) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L203)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit Missed @return ``
53: function getPoolCount(address token0, address token1) external view returns (uint256) {
/// @audit Missed @return ``
57: function getUserPoolCount(address creator) external view returns (uint256) {
/// @audit Missed @return ``
65: function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address) {
/// @audit Missed @return `clone`
81: function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
/// @audit Missed @return ``
155: function _computeSalt(
        address sender_,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) internal view returns (bytes32) {
```
[53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L53) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L57) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L155)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit Missed @return `clone, shares`
54: function createPool(
        address baseToken,
        address quoteToken,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external returns (address clone, uint256 shares) {
/// @audit Missed @return `clone, shares`
73: function createPoolETH(
        address token,
        bool useTokenAsQuote,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 tokenInAmount
    ) external payable returns (address clone, uint256 shares) {
/// @audit Missed @return `baseAdjustedInAmount, quoteAdjustedInAmount, shares`
96: function previewCreatePool(
        uint256 i,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external pure returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit Missed @return `baseAdjustedInAmount, quoteAdjustedInAmount, shares`
112: function previewAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit Missed @return `baseAdjustedInAmount, quoteAdjustedInAmount, shares`
162: function addLiquidity(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit Missed @return `shares`
178: function addLiquidityUnsafe(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 shares) {
/// @audit Missed @return `baseAdjustedInAmount, quoteAdjustedInAmount, shares`
192: function addLiquidityETH(
        address lp,
        address to,
        address payable refundTo,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit Missed @return `shares`
229: function addLiquidityETHUnsafe(
        address lp,
        address to,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 shares) {
/// @audit Missed @return `baseAmountOut, quoteAmountOut`
251: function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
/// @audit Missed @return `baseAmountOut, quoteAmountOut`
261: function removeLiquidity(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumBaseAmount,
        uint256 minimumQuoteAmount,
        uint256 deadline
    ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
/// @audit Missed @return `ethAmountOut, tokenAmountOut`
274: function removeLiquidityETH(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumETHAmount,
        uint256 minimumTokenAmount,
        uint256 deadline
    ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {
/// @audit Missed @return `amountOut`
314: function swapTokensForTokens(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @return `amountOut`
336: function swapETHForTokens(
        address to,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @return `amountOut`
365: function swapTokensForETH(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @return `amountOut`
404: function sellBaseTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @return `amountOut`
415: function sellBaseETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @return `amountOut`
432: function sellBaseTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @return `amountOut`
449: function sellQuoteTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @return `amountOut`
461: function sellQuoteETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @return `amountOut`
478: function sellQuoteTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit Missed @return `shares`
499: function _addLiquidity(address lp, address to, uint256 minimumShares) internal returns (uint256 shares) {
/// @audit Missed @return `baseAdjustedInAmount, quoteAdjustedInAmount`
509: function _adjustAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) internal view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount) {
/// @audit Missed @return `amountOut`
541: function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {
/// @audit Missed @return `amountOut`
571: function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {
/// @audit Missed @return `amountOut`
578: function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {
```
[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L54) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L73) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L96) | [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L112) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L162) | [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L178) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192) | [229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229) | [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L251) | [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L261) | [274](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L274) | [314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L314) | [336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336) | [365](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L365) | [404](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L404) | [415](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L415) | [432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L432) | [449](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L449) | [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L461) | [478](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L478) | [499](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L499) | [509](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L509) | [541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L541) | [571](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L571) | [578](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L578)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

/// @audit Missed @return ``
29: function decimals() external pure override returns (uint8) {
/// @audit Missed @return `, `
33: function _getReserves() internal view virtual returns (uint256, uint256) {
/// @audit Missed @return ``
37: function latestAnswer() public view override returns (int256) {
/// @audit Missed @return `, , , , `
48: function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```
[29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L29) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L33) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L37) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L48)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit Missed @return ``
199: function rewardData(address token) external view returns (Reward memory) {
/// @audit Missed @return ``
203: function rewardsForDuration(address rewardToken) external view returns (uint256) {
/// @audit Missed @return ``
207: function rewardTokensLength() external view returns (uint256) {
/// @audit Missed @return ``
211: function balances(address user) external view returns (Balances memory) {
/// @audit Missed @return ``
215: function userRewardLock(address user) external view returns (RewardLock memory) {
/// @audit Missed @return ``
219: function userLocks(address user) external view returns (LockedBalance[] memory) {
/// @audit Missed @return ``
223: function userLocksLength(address user) external view returns (uint256) {
/// @audit Missed @return ``
227: function locked(address user) external view returns (uint256) {
/// @audit Missed @return ``
231: function unlocked(address user) external view returns (uint256) {
/// @audit Missed @return ``
235: function totalSupply() public view returns (uint256) {
/// @audit Missed @return ``
239: function balanceOf(address user) public view returns (uint256) {
/// @audit Missed @return ``
253: function nextUnlockTime() public view returns (uint256) {
/// @audit Missed @return ``
257: function epoch() public view returns (uint256) {
/// @audit Missed @return ``
261: function nextEpoch() public view returns (uint256) {
/// @audit Missed @return ``
265: function remainingEpochTime() public view returns (uint256) {
/// @audit Missed @return ``
269: function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {
/// @audit Missed @return ``
273: function rewardPerToken(address rewardToken) public view returns (uint256) {
/// @audit Missed @return ``
277: function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
/// @audit Missed @return ``
288: function earned(address user, address rewardToken) public view returns (uint256) {
/// @audit Missed @return ``
292: function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {
/// @audit Missed @return `rewardPerToken_`
528: function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {
```
[199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L203) | [207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L207) | [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L211) | [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L215) | [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L219) | [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L223) | [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L227) | [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L231) | [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L235) | [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L239) | [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L253) | [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L257) | [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L261) | [265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L265) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L269) | [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L273) | [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277) | [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L288) | [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L292) | [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L528)
</details>

### [N-47] State-Altering Functions Should Emit Events

Functions that alter state should emit events to inform users of the state change.
This is crucial for functions that modify the state and don't return a value.
The absence of events in such scenarios could lead to lack of transparency and traceability, undermining the contract's reliability.

<details>
<summary><i>8 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

118: _INITIALIZED_ = true;
140: _RState_ = uint32(PMMPricing.RState.ONE);
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
536: _BASE_RESERVE_ = uint112(baseBalance);
553: _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
561: _BASE_RESERVE_ = baseReserve.toUint112();
572: _BASE_RESERVE_ = baseBalance.toUint112();
```
[118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L118) | [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L140) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L536) | [553](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L553) | [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L561) | [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L572)

```solidity
File: src/staking/LockingMultiRewards.sol

163: unlockedSupply -= amount;
```
[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L163)
</details>

### [N-48] Upgrade `openzeppelin` to the Latest Version - 5.0.0

These contracts import contracts from @openzeppelin/contracts but they are not using the latest version.
For more information, please visit: [OpenZeppelin GitHub Releases](https://github.com/OpenZeppelin/openzeppelin-contracts/releases)
It is recommended to always use the latest version to take advantage of updates and security fixes.

<details>
<summary><i>8 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

7: import {Proxy} from "openzeppelin-contracts/proxy/Proxy.sol";
10: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L7) | [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L10)

```solidity
File: src/blast/libraries/BlastYields.sol

5: import {Address} from "openzeppelin-contracts/utils/Address.sol";
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L5)

```solidity
File: src/mimswap/MagicLP.sol

11: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L11)

```solidity
File: src/mimswap/periphery/Router.sol

5: import {IERC20} from "openzeppelin-contracts/interfaces/IERC20.sol";
10: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L5) | [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L10)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

5: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L5)

```solidity
File: src/staking/LockingMultiRewards.sol

5: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L5)
</details>

### [N-49] Duplicated `require()`/`revert()` checks should be refactored to a modifier or function

Duplicated require() or revert() checks should be refactored to a modifier or function.
This helps in maintaining a clean and organized codebase and saves deployment costs.

<details>
<summary><i>25 issue instances in 10 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

25: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
73: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L25) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L73)

```solidity
File: src/blast/BlastMagicLP.sol

24: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
81: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L24) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L81)

```solidity
File: src/blast/BlastOnboarding.sol

89: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
148: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
```
[89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L89) | [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L148)

```solidity
File: src/blast/BlastWrappers.sol

21: if (governor_ == address(0)) {
            revert ErrZeroAddress();
35: if (governor_ == address(0)) {
            revert ErrZeroAddress();
48: if (governor_ == address(0)) {
            revert ErrZeroAddress();
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L21) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L35) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L48)

```solidity
File: src/mimswap/MagicLP.sol

508: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
            revert ErrOverflow();
532: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
            revert ErrOverflow();
```
[508](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508) | [532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L532)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

23: if (maintainer_ == address(0)) {
            revert ErrZeroAddress();
47: if (maintainer_ == address(0)) {
            revert ErrZeroAddress();
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L23) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L47)

```solidity
File: src/mimswap/libraries/Math.sol

52: if (V0 == 0) {
            revert ErrIsZero();
132: if (V0 == 0) {
            revert ErrIsZero();
```
[52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L52) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L132)

```solidity
File: src/mimswap/periphery/Factory.sol

39: if (implementation_ == address(0)) {
            revert ErrZeroAddress();
97: if (implementation_ == address(0)) {
            revert ErrZeroAddress();
42: if (address(maintainerFeeRateModel_) == address(0)) {
            revert ErrZeroAddress();
106: if (address(maintainerFeeRateModel_) == address(0)) {
            revert ErrZeroAddress();
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L39) | [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L97) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L42) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L106)

```solidity
File: src/mimswap/periphery/Router.sol

566: if (amountOut < minimumOut) {
            revert ErrTooHighSlippage(amountOut);
573: if (amountOut < minimumOut) {
            revert ErrTooHighSlippage(amountOut);
581: if (amountOut < minimumOut) {
            revert ErrTooHighSlippage(amountOut);
```
[566](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L566) | [573](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L573) | [581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L581)

```solidity
File: src/staking/LockingMultiRewards.sol

156: if (amount == 0) {
            revert ErrZeroAmount();
171: if (amount == 0) {
            revert ErrZeroAmount();
459: if (amount == 0) {
            revert ErrZeroAmount();
```
[156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L156) | [171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L171) | [459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L459)
</details>

### [N-50] Event is not properly `indexed`

Index event fields make the field more quickly accessible to off-chain tools that parse events.
This is especially useful when it comes to filtering based on an address. However, note that each index field costs extra gas during emission, so it's not necessarily best to index the maximum allowed per event (three fields).
Where applicable, each event should use three indexed fields if there are three or more fields, and gas usage is not particularly of concern for the events in question.
If there are fewer than three applicable fields, all of the applicable fields should be indexed.

<details>
<summary><i>39 issue instances in 9 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

14: event LogTokenDepositEnabled(address indexed token, bool enabled);
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L14)

```solidity
File: src/blast/BlastMagicLP.sol

12: event LogOperatorChanged(address indexed, bool);
13: event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L12) | [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L13)

```solidity
File: src/blast/BlastOnboarding.sol

68: event LogTokenSupported(address indexed token, bool supported);
69: event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);
70: event LogLock(address indexed user, address indexed token, uint256 amount);
72: event LogWithdraw(address indexed user, address indexed token, uint256 amount);
73: event LogTokenCapChanged(address indexed token, uint256 cap);
74: event LogStateChange(State state);
75: event LogTokenRescue(address indexed token, address indexed to, uint256 amount);
```
[68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L68) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L69) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L70) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L72) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L73) | [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L74) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L75)

```solidity
File: src/blast/BlastOnboardingBoot.sol

37: event LogReadyChanged(bool ready);
38: event LogClaimed(address indexed user, uint256 shares, bool lock);
40: event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);
```
[37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L37) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L38) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L40)

```solidity
File: src/blast/BlastTokenRegistry.sol

7: event LogNativeYieldTokenEnabled(address indexed token, bool enabled);
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L7)

```solidity
File: src/blast/libraries/BlastYields.sol

8: event LogBlastGasClaimed(address indexed recipient, uint256 amount);
9: event LogBlastETHClaimed(address indexed recipient, uint256 amount);
10: event LogBlastTokenClaimed(address indexed recipient, address indexed token, uint256 amount);
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L8) | [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L9) | [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L10)

```solidity
File: src/mimswap/MagicLP.sol

30: event BuyShares(address to, uint256 increaseShares, uint256 totalShares);
31: event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);
32: event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);
33: event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);
34: event RChange(PMMPricing.RState newRState);
35: event TokenRescue(address indexed token, address to, uint256 amount);
36: event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);
```
[30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L30) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L31) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L32) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L33) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L34) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L35) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L36)

```solidity
File: src/mimswap/periphery/Factory.sol

23: event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);
24: event LogPoolRemoved(address pool);
27: event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L23) | [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L24) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L27)

```solidity
File: src/staking/LockingMultiRewards.sol

17: event LogRewardAdded(uint256 reward);
18: event LogStaked(address indexed user, uint256 amount);
19: event LogLocked(address indexed user, uint256 amount, uint256 unlockTime, uint256 lockCount);
20: event LogUnlocked(address indexed user, uint256 amount, uint256 index);
21: event LogLockIndexChanged(address indexed user, uint256 fromIndex, uint256 toIndex);
22: event LogWithdrawn(address indexed user, uint256 amount);
23: event LogRewardLockCreated(address indexed user, uint256 unlockTime);
24: event LogRewardLocked(address indexed user, address indexed rewardsToken, uint256 reward);
25: event LogRewardPaid(address indexed user, address indexed rewardsToken, uint256 reward);
26: event LogRewardsDurationUpdated(address token, uint256 newDuration);
27: event LogRecovered(address token, uint256 amount);
28: event LogSetMinLockAmount(uint256 previous, uint256 current);
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L17) | [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L18) | [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L19) | [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L21) | [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L22) | [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L23) | [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L24) | [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L25) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L26) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L27) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L28)
</details>

### [N-51] Consider Adding Emergency-Stop Functionality

Smart contracts that hold significant value, interact with external contracts, or have complex logic should include an emergency-stop mechanism for added security. This allows pausing certain contract functionalities in case of emergencies, mitigating potential damages.

This contract seems to lack such a mechanism. Implementing an emergency stop can enhance contract security and reliability.

<details>
<summary><i>13 issue instances in 13 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L1)

```solidity
File: src/blast/BlastBox.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L1)

```solidity
File: src/blast/BlastGovernor.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L1)

```solidity
File: src/blast/BlastMagicLP.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L1)

```solidity
File: src/blast/BlastOnboardingBoot.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L1)

```solidity
File: src/blast/BlastTokenRegistry.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L1)

```solidity
File: src/blast/BlastWrappers.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L1)

```solidity
File: src/mimswap/MagicLP.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L1)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L1)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L1)

```solidity
File: src/mimswap/periphery/Factory.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L1)

```solidity
File: src/mimswap/periphery/Router.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L1)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

1: No emergency stop pattern found
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L1)
</details>

### [N-52] Missing NatSpec Descriptions for Modifier Declarations

Modifiers in the contract should include NatSpec comments, specifically with the `@dev` or `@notice` tags to elucidate their role and input parameters.
These annotations assist in offering a clearer insight into the contract's operation for developers, auditors, and end-users.
[Additional Details in Solidity Documentation](https://docs.soliditylang.org/en/latest/natspec-format.html)

<details>
<summary><i>7 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/BlastMagicLP.sol

118: modifier onlyImplementationOperators() {
```
[118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L118)

```solidity
File: src/blast/BlastOnboarding.sol

43: modifier onlyState(State _state) {
50: modifier onlySupportedTokens(address token) {
```
[43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L43) | [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L50)

```solidity
File: src/mimswap/MagicLP.sol

607: modifier onlyImplementationOwner() {
614: modifier onlyClones() {
621: modifier onlyImplementation() {
```
[607](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L607) | [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L614) | [621](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L621)

```solidity
File: src/mimswap/periphery/Router.sol

47: modifier ensureDeadline(uint256 deadline) {
```
[47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L47)
</details>

### [N-53] NatSpec: Public State variable declarations should have descriptions

State variables should ideally be accompanied by NatSpec comments to describe their purpose and usage. 
This aids developers in understanding the function and purpose of each variable, especially in large and complex contracts.
Consider adding `@dev` or `@notice` descriptions to your state variables.

<details>
<summary><i>70 issue instances in 13 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

20: BlastTokenRegistry public immutable registry;
21: mapping(address => bool) public enabledTokens;
22: address public feeTo;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21) | [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L22)

```solidity
File: src/blast/BlastGovernor.sol

11: address public feeTo;
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L11)

```solidity
File: src/blast/BlastMagicLP.sol

17: BlastTokenRegistry public immutable registry;
21: mapping(address => bool) public operators;
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L17) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L21)

```solidity
File: src/blast/BlastOnboarding.sol

30: State public state;
31: address public bootstrapper;
32: address public feeTo;
33: BlastTokenRegistry public registry;
36: mapping(address token => bool) public supportedTokens;
37: mapping(address token => Balances) public totals;
38: mapping(address token => uint256 cap) public caps;
41: mapping(address user => mapping(address token => Balances)) public balances;
```
[30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L30) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L31) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L32) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L33) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L37) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L38) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L41)

```solidity
File: src/blast/BlastOnboardingBoot.sol

24: address public pool;
25: Router public router;
26: IFactory public factory;
27: uint256 public totalPoolShares;
28: bool public ready;
29: LockingMultiRewards public staking;
30: mapping(address user => bool claimed) public claimed;
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L24) | [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L25) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L26) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L27) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L28) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L29) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L30)

```solidity
File: src/blast/BlastTokenRegistry.sol

10: mapping(address => bool) public nativeYieldTokens;
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10)

```solidity
File: src/blast/libraries/BlastPoints.sol

7: address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;
8: IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L7) | [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L8)

```solidity
File: src/mimswap/MagicLP.sol

61: MagicLP public immutable implementation;
63: uint256 public constant MAX_I = 10 ** 36;
64: uint256 public constant MAX_K = 10 ** 18;
65: uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%
66: uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%
70: address public _BASE_TOKEN_;
71: address public _QUOTE_TOKEN_;
72: uint112 public _BASE_RESERVE_;
73: uint112 public _QUOTE_RESERVE_;
74: uint32 public _BLOCK_TIMESTAMP_LAST_;
75: uint256 public _BASE_PRICE_CUMULATIVE_LAST_;
76: uint112 public _BASE_TARGET_;
77: uint112 public _QUOTE_TARGET_;
78: uint32 public _RState_;
79: IFeeRateModel public _MT_FEE_RATE_MODEL_;
80: uint256 public _LP_FEE_RATE_;
81: uint256 public _K_;
82: uint256 public _I_;
```
[61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L61) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L65) | [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L66) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L70) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L71) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73) | [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L75) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77) | [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L78) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L79) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L80) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L81) | [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L82)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

19: address public maintainer;
20: address public implementation;
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L19) | [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L20)

```solidity
File: src/mimswap/periphery/Factory.sol

32: address public implementation;
33: IFeeRateModel public maintainerFeeRateModel;
35: mapping(address base => mapping(address quote => address[] pools)) public pools;
36: mapping(address creator => address[] pools) public userPools;
```
[32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L32) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L33) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L35) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L36)

```solidity
File: src/mimswap/periphery/Router.sol

31: uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;
33: IWETH public immutable weth;
34: IFactory public immutable factory;
```
[31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L31) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L33) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L34)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

10: IMagicLP public immutable pair;
11: IAggregator public immutable baseOracle;
12: IAggregator public immutable quoteOracle;
13: uint8 public immutable baseDecimals;
14: uint8 public immutable quoteDecimals;
16: uint256 public constant WAD = 18;
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L10) | [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L11) | [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L12) | [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L14) | [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L16)

```solidity
File: src/staking/LockingMultiRewards.sol

83: uint256 public immutable maxLocks;
84: uint256 public immutable lockingBoostMultiplerInBips;
85: uint256 public immutable rewardsDuration;
86: uint256 public immutable lockDuration;
87: address public immutable stakingToken;
94: mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
95: mapping(address user => mapping(address token => uint256 amount)) public rewards;
96: mapping(address user => uint256 index) public lastLockIndex;
98: address[] public rewardTokens;
100: uint256 public lockedSupply; // all locked boosted deposits
101: uint256 public unlockedSupply; // all unlocked unboosted deposits
102: uint256 public minLockAmount; // minimum amount allowed to lock
103: uint256 public stakingTokenBalance; // total staking token balance
```
[83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L83) | [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L84) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L85) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L86) | [87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L87) | [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L94) | [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L95) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L96) | [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L98) | [100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L100) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L101) | [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L102) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L103)
</details>

### [N-54] Consider adding a block/deny-list

While adding a block or deny-list may increase the level of centralization in the contract, it provides an additional layer of security by preventing hackers from using stolen tokens or carrying out other malicious activities.

Although it's a trade-off, a block or deny-list can help improve the overall security posture of the contract.

<details>
<summary><i>4 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

11: contract BlastOnboardingData is Owned, Pausable {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L11)

```solidity
File: src/mimswap/MagicLP.sol

25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L25)

```solidity
File: src/mimswap/periphery/Router.sol

11: contract Router {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L11)

```solidity
File: src/staking/LockingMultiRewards.sol

14: contract LockingMultiRewards is OperatableV2, Pausable {
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L14)
</details>

### [N-55] Non-uppercase/Constant-case Naming for `immutable` Variables

For better readability and adherence to common naming conventions, variable names declared as immutable should be written in all uppercase letters.

<details>
<summary><i>16 issue instances in 7 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

20: BlastTokenRegistry public immutable registry;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L20)

```solidity
File: src/blast/BlastMagicLP.sol

17: BlastTokenRegistry public immutable registry;
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L17)

```solidity
File: src/blast/BlastWrappers.sol

45: address private immutable _governor;
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L45)

```solidity
File: src/mimswap/MagicLP.sol

61: MagicLP public immutable implementation;
```
[61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L61)

```solidity
File: src/mimswap/periphery/Router.sol

33: IWETH public immutable weth;
34: IFactory public immutable factory;
```
[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L33) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L34)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

10: IMagicLP public immutable pair;
11: IAggregator public immutable baseOracle;
12: IAggregator public immutable quoteOracle;
13: uint8 public immutable baseDecimals;
14: uint8 public immutable quoteDecimals;
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L10) | [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L11) | [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L12) | [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L14)

```solidity
File: src/staking/LockingMultiRewards.sol

83: uint256 public immutable maxLocks;
84: uint256 public immutable lockingBoostMultiplerInBips;
85: uint256 public immutable rewardsDuration;
86: uint256 public immutable lockDuration;
87: address public immutable stakingToken;
```
[83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L83) | [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L84) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L85) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L86) | [87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L87)
</details>

### [N-56] Not using the named return variables anywhere in the function is confusing

Declaring a named return variable but returning a different value within the function is an inconsistent use of named return variables.
This practice can lead to confusion and misinterpretation of the function's intended behavior, as it contradicts the purpose of declaring named return variables, which is to enhance readability and reduce complexity in the code.

This inconsistency might signal an error in the function logic where the declared return variable is not being used as intended.
It is recommended to revisit the function's logic to ensure that the named return variables are being utilized correctly, or to adjust the return statements to reflect the actual values being returned, fostering better clarity and coherence in the code.

<details>
<summary><i>26 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit - `return 0;` statement in functions but `shares` are declared
/// @audit - `return _claimable(user);` statement in functions but `shares` are declared
77: function claimable(address user) external view returns (uint256 shares) {
/// @audit - `return router.previewCreatePool(I, baseAmount, quoteAmount);` statement in functions but `baseAdjustedInAmount, quoteAdjustedInAmount, shares` are declared
85: function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit - `return 0;` statement in functions but `shares` are declared
/// @audit - `return (userLocked * totalPoolShares) / totalLocked;` statement in functions but `shares` are declared
154: function _claimable(address user) internal view returns (uint256 shares) {
```
[77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L77) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L85) | [154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L154)

```solidity
File: src/blast/libraries/BlastYields.sol

/// @audit - `return claimAllNativeYields(address(this), recipient);` statement in functions but `amount` are declared
50: function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
```
[50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L50)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit - `return PMMPricing.getMidPrice(getPMMState());` statement in functions but `midPrice` are declared
214: function getMidPrice() public view returns (uint256 midPrice) {
/// @audit - `return _MT_FEE_RATE_MODEL_.getFeeRate(user, _LP_FEE_RATE_);` statement in functions but `lpFeeRate, mtFeeRate` are declared
223: function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
/// @audit - `return _BASE_TOKEN_.balanceOf(address(this)) - uint256(_BASE_RESERVE_);` statement in functions but `input` are declared
227: function getBaseInput() public view returns (uint256 input) {
/// @audit - `return _QUOTE_TOKEN_.balanceOf(address(this)) - uint256(_QUOTE_RESERVE_);` statement in functions but `input` are declared
231: function getQuoteInput() public view returns (uint256 input) {
```
[214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L214) | [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L223) | [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L227) | [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L231)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit - `return (lpFeeRate, 0);` statement in functions but `adjustedLpFeeRate, mtFeeRate` are declared
/// @audit - `return IFeeRateImpl(implementation).getFeeRate(msg.sender, trader, lpFeeRate);` statement in functions but `adjustedLpFeeRate, mtFeeRate` are declared
33: function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L33)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

/// @audit - `return Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q0, payBaseAmount, state.i, state.K);` statement in functions but `receiveQuoteToken` are declared
103: function _ROneSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {
/// @audit - `return Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);` statement in functions but `receiveBaseToken` are declared
118: function _ROneSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {
/// @audit - `return Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K);` statement in functions but `receiveBaseToken` are declared
133: function _RBelowSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {
/// @audit - `return Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q, payBaseAmount, state.i, state.K);` statement in functions but `receiveQuoteToken` are declared
146: function _RBelowSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {
/// @audit - `return Math._GeneralIntegrate(state.B0, state.B + payBaseAmount, state.B, state.i, state.K);` statement in functions but `receiveQuoteToken` are declared
161: function _RAboveSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {
/// @audit - `return Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);` statement in functions but `receiveBaseToken` are declared
174: function _RAboveSellQuoteToken(
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
[103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L103) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L118) | [133](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L133) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L146) | [161](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L161) | [174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L174)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit - `return (0, 0, 0);` statement in functions but `baseAdjustedInAmount, quoteAdjustedInAmount, shares` are declared
95: function previewCreatePool(
        uint256 i,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external pure returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit - `return (0, 0, 0);` statement in functions but `baseAdjustedInAmount, quoteAdjustedInAmount, shares` are declared
/// @audit - `return (0, 0, 0);` statement in functions but `baseAdjustedInAmount, quoteAdjustedInAmount, shares` are declared
/// @audit - `return (0, 0, 0);` statement in functions but `baseAdjustedInAmount, quoteAdjustedInAmount, shares` are declared
111: function previewAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit - `return _addLiquidity(lp, to, minimumShares);` statement in functions but `shares` are declared
177: function addLiquidityUnsafe(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 shares) {
/// @audit - `return _addLiquidity(lp, to, minimumShares);` statement in functions but `shares` are declared
228: function addLiquidityETHUnsafe(
        address lp,
        address to,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 shares) {
/// @audit - `return IMagicLP(lp).sellShares(sharesIn, to, minimumBaseAmount, minimumQuoteAmount, "", deadline);` statement in functions but `baseAmountOut, quoteAmountOut` are declared
260: function removeLiquidity(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumBaseAmount,
        uint256 minimumQuoteAmount,
        uint256 deadline
    ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
/// @audit - `return _swap(to, path, directions, minimumOut);` statement in functions but `amountOut` are declared
313: function swapTokensForTokens(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit - `return _swap(to, path, directions, minimumOut);` statement in functions but `amountOut` are declared
335: function swapETHForTokens(
        address to,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit - `return _sellBase(lp, to, minimumOut);` statement in functions but `amountOut` are declared
403: function sellBaseTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit - `return _sellBase(lp, to, minimumOut);` statement in functions but `amountOut` are declared
414: function sellBaseETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit - `return _sellQuote(lp, to, minimumOut);` statement in functions but `amountOut` are declared
448: function sellQuoteTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit - `return _sellQuote(lp, to, minimumOut);` statement in functions but `amountOut` are declared
460: function sellQuoteETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
```
[95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L95) | [111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L111) | [177](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L177) | [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L228) | [260](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L260) | [313](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L313) | [335](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L335) | [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L403) | [414](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L414) | [448](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L448) | [460](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L460)
</details>

### [N-57] Function Names Not in mixedCase

Function names should use mixedCase for better readability and consistency with Solidity style guidelines. 
Examples of good practice include: getBalance, transfer, verifyOwner, addMember, changeOwner. 
[More information in Documentation](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#function-names)

<details>
<summary><i>19 issue instances in 3 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

137: function correctRState() external {
192: function getPMMState() public view returns (PMMPricing.PMMState memory state) {
203: function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
```
[137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L137) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L192) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L203)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

103: function _ROneSellBaseToken(
118: function _ROneSellQuoteToken(
133: function _RBelowSellQuoteToken(
146: function _RBelowSellBaseToken(
161: function _RAboveSellBaseToken(
174: function _RAboveSellQuoteToken(
```
[103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L103) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L118) | [133](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L133) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L146) | [161](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L161) | [174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L174)

```solidity
File: src/mimswap/periphery/Router.sol

72: function createPoolETH(
191: function addLiquidityETH(
228: function addLiquidityETHUnsafe(
273: function removeLiquidityETH(
335: function swapETHForTokens(
364: function swapTokensForETH(
414: function sellBaseETHForTokens(
431: function sellBaseTokensForETH(
460: function sellQuoteETHForTokens(
477: function sellQuoteTokensForETH(
```
[72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L72) | [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L191) | [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L228) | [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L273) | [335](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L335) | [364](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L364) | [414](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L414) | [431](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L431) | [460](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L460) | [477](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L477)
</details>

### [N-58] Use scientific notation(1e18) instead of exponentiation(10**18)

Consider using scientific notation (e.g. 1e18) rather than exponentiation (e.g. 10**18) for better coding practice and readability.

<details>
<summary><i>5 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

/// @audit `10 ** 36` should be replaced with `1e36`
63: uint256 public constant MAX_I = 10 ** 36;
/// @audit `10 ** 18` should be replaced with `1e18`
64: uint256 public constant MAX_K = 10 ** 18;
```
[63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

/// @audit `10 ** 18` should be replaced with `1e18`
20: uint256 internal constant ONE = 10 ** 18;
/// @audit `10 ** 36` should be replaced with `1e36`
21: uint256 internal constant ONE2 = 10 ** 36;
/// @audit `10 ** 18` should be replaced with `1e18`
49: return 10 ** 18;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L21) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L49)
</details>

### [N-59] Insufficient Comments in Complex Functions

Complex functions spanning multiple lines should have more comments to better explain the purpose of each logic step.
Proper commenting can greatly improve the readability and maintainability of the codebase. Consider adding explicit comments
to provide insights into the function's operation.

<details>
<summary><i>6 issue instances in 4 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

/// @audit function with 46 lines has only 5 comment lines
289: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
/// @audit function with 35 lines has only 4 comment lines
360: function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
```
[289](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L289) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360)

```solidity
File: src/mimswap/libraries/Math.sol

/// @audit function with 50 lines has only 20 comment lines
131: function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```
[131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit function with 34 lines has only 0 comment lines
111: function previewAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
```
[111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L111)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit function with 37 lines has only 4 comment lines
397: function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
/// @audit function with 32 lines has only 16 comment lines
597: function _getRewards(address user) internal {
```
[397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397) | [597](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L597)
</details>

### [N-60] Common functions should be refactored to a common base contract

The codebase contains several functions with the same implementations across multiple files.
To enhance maintainability and reduce potential errors, consider refactoring these common functions into a shared base contract.
This practice promotes code reuse and easier future upgrades.

<details>
<summary><i>13 issue instances in 5 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

51: function claimGasYields() external onlyOperators returns (uint256) {
        return BlastYields.claimMaxGasYields(feeTo);
    }
67: function callBlastPrecompile(bytes calldata data) external onlyOwner {
        BlastYields.callPrecompile(data);
    }
71: function setFeeTo(address feeTo_) external onlyOwner {
        if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
        }

        feeTo = feeTo_;
        emit LogFeeToChanged(feeTo_);
    }
```
[51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L51) | [67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L67) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L71)

```solidity
File: src/blast/BlastOnboarding.sol

159: function claimGasYields() external onlyOwner returns (uint256) {
        return BlastYields.claimMaxGasYields(feeTo);
    }
155: function callBlastPrecompile(bytes calldata data) external onlyOwner {
        BlastYields.callPrecompile(data);
    }
146: function setFeeTo(address feeTo_) external onlyOwner {
        if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
        }

        feeTo = feeTo_;
        emit LogFeeToChanged(feeTo_);
    }
213: function pause() external onlyOwner {
        _pause();
    }
217: function unpause() external onlyOwner {
        _unpause();
    }
```
[159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L159) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L155) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L146) | [213](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L213) | [217](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L217)

```solidity
File: src/blast/BlastGovernor.sol

48: function callBlastPrecompile(bytes calldata data) external onlyOwner {
        BlastYields.callPrecompile(data);
    }
```
[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L48)

```solidity
File: src/blast/BlastMagicLP.sol

71: function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {
        BlastYields.callPrecompile(data);
    }
79: function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
        if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
        }

        feeTo = feeTo_;
        emit LogFeeToChanged(feeTo_);
    }
```
[71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L71) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L79)

```solidity
File: src/staking/LockingMultiRewards.sol

337: function pause() external onlyOwner {
        _pause();
    }
340: function unpause() external onlyOwner {
        _unpause();
    }
```
[337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337) | [340](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L340)
</details>

### [N-61] NatSpec: Error declarations should have descriptions

NatSpec comments are essential for understanding the purpose and functionality of error declarations. 
Adding descriptive comments improves readability and can aid in debugging.
It's a best practice to provide NatSpec comments for all error declarations in your Solidity contract.

<details>
<summary><i>77 issue instances in 12 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

17: error ErrZeroAddress();
18: error ErrUnsupportedToken();
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L17) | [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L18)

```solidity
File: src/blast/BlastGovernor.sol

9: error ErrZeroAddress();
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L9)

```solidity
File: src/blast/BlastMagicLP.sol

15: error ErrNotAllowedImplementationOperator();
```
[15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L15)

```solidity
File: src/blast/BlastOnboarding.sol

13: error ErrZeroAddress();
14: error ErrWrongState();
15: error ErrUnsupportedToken();
16: error ErrNotAllowed();
77: error ErrUnsupported();
78: error ErrCapReached();
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L14) | [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L15) | [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L16) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L77) | [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L78)

```solidity
File: src/blast/BlastOnboardingBoot.sol

43: error ErrInsufficientAmountOut();
44: error ErrNotReady();
45: error ErrAlreadyClaimed();
46: error ErrWrongFeeRateModel();
47: error ErrAlreadyBootstrapped();
48: error ErrNothingToClaim();
49: error ErrCannotChangeOnceReady();
```
[43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L43) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L44) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L45) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L46) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L47) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L48) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L49)

```solidity
File: src/blast/BlastTokenRegistry.sol

8: error ErrZeroAddress();
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L8)

```solidity
File: src/blast/BlastWrappers.sol

43: error ErrInvalidGovernorAddress();
```
[43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L43)

```solidity
File: src/mimswap/MagicLP.sol

38: error ErrInitialized();
39: error ErrBaseQuoteSame();
40: error ErrInvalidI();
41: error ErrInvalidK();
42: error ErrExpired();
43: error ErrInvalidSignature();
44: error ErrFlashLoanFailed();
45: error ErrNoBaseInput();
46: error ErrZeroAddress();
47: error ErrZeroQuoteAmount();
48: error ErrZeroQuoteTarget();
49: error ErrMintAmountNotEnough();
50: error ErrNotEnough();
51: error ErrWithdrawNotEnough();
52: error ErrSellBackNotAllowed();
53: error ErrInvalidLPFeeRate();
54: error ErrNotImplementationOwner();
55: error ErrNotImplementation();
56: error ErrNotClone();
57: error ErrNotAllowed();
58: error ErrReserveAmountNotEnough();
59: error ErrOverflow();
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L38) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L39) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L40) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L41) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L42) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L43) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L44) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L45) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L46) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L47) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L48) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L49) | [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L50) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L51) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L52) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L53) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L54) | [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L55) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L56) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L57) | [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L58) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L59)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

17: error ErrZeroAddress();
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L17)

```solidity
File: src/mimswap/periphery/Factory.sol

29: error ErrInvalidUserPoolIndex();
30: error ErrZeroAddress();
```
[29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L29) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L30)

```solidity
File: src/mimswap/periphery/Router.sol

16: error ErrNotETHLP();
17: error ErrExpired();
18: error ErrZeroAddress();
19: error ErrPathTooLong();
20: error ErrEmptyPath();
21: error ErrBadPath();
22: error ErrTooHighSlippage(uint256 amountOut);
23: error ErrInvalidBaseToken();
24: error ErrInvalidQuoteToken();
25: error ErrInTokenNotETH();
26: error ErrOutTokenNotETH();
27: error ErrInvalidQuoteTarget();
28: error ErrZeroDecimals();
29: error ErrDecimalsDifferenceTooLarge();
```
[16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L16) | [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L17) | [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L18) | [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L19) | [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L21) | [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L22) | [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L23) | [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L24) | [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L25) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L26) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L27) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L28) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L29)

```solidity
File: src/staking/LockingMultiRewards.sol

30: error ErrZeroAmount();
31: error ErrRewardAlreadyExists();
32: error ErrInvalidTokenAddress();
33: error ErrMaxUserLocksExceeded();
34: error ErrNotExpired();
35: error ErrInvalidUser();
36: error ErrLockAmountTooSmall();
37: error ErrLengthMismatch();
38: error ErrNoLocks();
39: error ErrLockNotExpired();
40: error ErrMaxRewardsExceeded();
41: error ErrSkimmingTooMuch();
42: error ErrInvalidLockIndex();
43: error ErrNotEnoughReward();
44: error ErrInvalidDurationRatio();
45: error ErrInvalidBoostMultiplier();
46: error ErrInvalidLockDuration();
47: error ErrInvalidRewardDuration();
48: error ErrInsufficientRemainingTime();
```
[30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L30) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L31) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L32) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L33) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L34) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L35) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L36) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L37) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L38) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L39) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L40) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L41) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L42) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L43) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L44) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L45) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L46) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L47) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L48)
</details>

### [N-62] NatSpec: Non-public state variable declarations should use `@dev` tags

Non-public state variables in smart contracts often have specialized purposes that may not be immediately clear to developers who did not write the original code.
Adding comments to explain the role and functionality of these variables can greatly aid in code readability and maintainability.
This is especially beneficial for future code reviews and audits.

<details>
<summary><i>18 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

13: address constant USDB = 0x4300000000000000000000000000000000000003;
16: uint256 constant K = 0.00025 ether; // 0.00025, 1.25% price fluctuation, similar to A2000 in curve
17: uint256 constant I = 0.998 ether; // 1 MIM = 0.998 USDB
18: uint256 constant USDB_TO_MIN = 1.002 ether; // 1 USDB = 1.002 MIM
19: uint256 constant MIM_TO_MIN = I;
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L13) | [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L16) | [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L17) | [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L18) | [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L19)

```solidity
File: src/blast/BlastWrappers.sol

45: address private immutable _governor;
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L45)

```solidity
File: src/blast/libraries/BlastYields.sol

14: IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L14)

```solidity
File: src/mimswap/MagicLP.sol

68: bool internal _INITIALIZED_;
```
[68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L68)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

20: uint256 internal constant ONE = 10 ** 18;
21: uint256 internal constant ONE2 = 10 ** 36;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L21)

```solidity
File: src/staking/LockingMultiRewards.sol

78: uint256 private constant BIPS = 10_000;
79: uint256 private constant MAX_NUM_REWARDS = 5;
80: uint256 private constant MIN_LOCK_DURATION = 1 weeks;
81: uint256 private constant MIN_REWARDS_DURATION = 1 days;
89: mapping(address token => Reward info) private _rewardData;
90: mapping(address user => Balances balances) private _balances;
91: mapping(address user => LockedBalance[] locks) private _userLocks;
92: mapping(address user => RewardLock rewardLock) private _userRewardLock;
```
[78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L78) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L79) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L80) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L81) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L89) | [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L90) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L91) | [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L92)
</details>

### [N-63] `constant`s should be defined rather than using magic numbers

Magic numbers are hardcoded numerical values used directly in the code, making it harder to read and maintain.
Consider using constants instead of magic numbers.

<details>
<summary><i>23 issue instances in 9 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit 30_000
117: staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
/// @audit 13
117: staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
```
[117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117) | [117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit 2020
3: Copyright 2020 DODO ZOO.
/// @audit 2 ** 32
125: _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);
/// @audit 2001
389: if (shares <= 2001) {
/// @audit 1001
393: _mint(address(0), 1001);
/// @audit 1001
394: shares -= 1001;
/// @audit 2 ** 32
546: uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
/// @audit 1000
594: if (amount <= 1000) {
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L3) | [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L125) | [389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L389) | [393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L393) | [394](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L394) | [546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L546) | [594](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L594)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit 2020
3: Copyright 2020 DODO ZOO.
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L3)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

/// @audit 2020
3: Copyright 2020 DODO ZOO.
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L3)

```solidity
File: src/mimswap/libraries/Math.sol

/// @audit 2020
3: Copyright 2020 DODO ZOO.
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L3)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

/// @audit 2020
3: Copyright 2020 DODO ZOO.
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L3)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit 18
83: _validateDecimals(18, IERC20Metadata(token).decimals());
/// @audit 18
85: _validateDecimals(IERC20Metadata(token).decimals(), 18);
/// @audit 2001
105: if (shares <= 2001) {
/// @audit 1001
109: shares -= 1001;
/// @audit 2001
142: if (shares <= 2001) {
/// @audit 1001
146: shares -= 1001;
/// @audit 256
590: if (pathLength > 256) {
```
[83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L83) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L85) | [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L105) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L109) | [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L142) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L146) | [590](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L590)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

/// @audit 18
30: return 18;
```
[30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L30)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit 1e18
283: uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
/// @audit 1e18
294: return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];
```
[283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283) | [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294)
</details>

### [N-64] Variable Names Not in mixedCase

State or Local Variable names in your contract don't align with the Solidity naming convention.
For clarity and code consistency, it's recommended to use mixedCase for local and state variables that are not constants, and add a trailing underscore for internal variables.
Adhering to this convention helps in improving code readability and maintenance.
[More information in Documentation](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#function-names)

<details>
<summary><i>10 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

/// @audit - Variable name `_BASE_TOKEN_` should be in mixedCase
70: address public _BASE_TOKEN_;
/// @audit - Variable name `_QUOTE_TOKEN_` should be in mixedCase
71: address public _QUOTE_TOKEN_;
/// @audit - Variable name `_BASE_RESERVE_` should be in mixedCase
72: uint112 public _BASE_RESERVE_;
/// @audit - Variable name `_QUOTE_RESERVE_` should be in mixedCase
73: uint112 public _QUOTE_RESERVE_;
/// @audit - Variable name `_BLOCK_TIMESTAMP_LAST_` should be in mixedCase
74: uint32 public _BLOCK_TIMESTAMP_LAST_;
/// @audit - Variable name `_BASE_PRICE_CUMULATIVE_LAST_` should be in mixedCase
75: uint256 public _BASE_PRICE_CUMULATIVE_LAST_;
/// @audit - Variable name `_BASE_TARGET_` should be in mixedCase
76: uint112 public _BASE_TARGET_;
/// @audit - Variable name `_QUOTE_TARGET_` should be in mixedCase
77: uint112 public _QUOTE_TARGET_;
/// @audit - Variable name `_MT_FEE_RATE_MODEL_` should be in mixedCase
79: IFeeRateModel public _MT_FEE_RATE_MODEL_;
/// @audit - Variable name `_LP_FEE_RATE_` should be in mixedCase
80: uint256 public _LP_FEE_RATE_;
```
[70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L70) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L71) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73) | [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L75) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L79) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L80)
</details>

### [N-65] Consider moving `msg.sender` checks to a common authorization `modifier`

Functions that are only allowed to be called by a specific actor should use a modifier to check if the caller is the specified actor (e.g., owner, specific role, etc.).
Using `require` to check `msg.sender` in the function body is less efficient and less clear.

Consider refactoring these `require` statements into a modifier for better readability, organization, and gas efficiency.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

59: if (claimed[msg.sender]) {
```
[59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L59)

```solidity
File: src/mimswap/MagicLP.sol

424: if (shareAmount > balanceOf(msg.sender)) {
```
[424](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L424)
</details>

### [N-66] NatSpec: Contract declarations should have descriptions

NatSpec descriptions are crucial for self-documenting smart contracts. They provide vital information 
about the contract's purpose and behavior.

Specifically, the `@dev` or `@notice` tags are quintessential 
for detailed explanations about the contract. 

Ensure these descriptions are present directly above the contract definition braces. 
This positioning allows the compiler to correctly identify and associate the descriptions with the contract.

[Learn More about Proper NatSpec Formatting](https://docs.soliditylang.org/en/develop/natspec-format.html)

<details>
<summary><i>17 issue instances in 14 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

5: contract BlastDapp {
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L5)

```solidity
File: src/blast/BlastBox.sol

12: contract BlastBox is DegenBox, OperatableV3 {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L12)

```solidity
File: src/blast/BlastGovernor.sol

6: contract BlastGovernor is OperatableV2 {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L6)

```solidity
File: src/blast/BlastMagicLP.sol

9: contract BlastMagicLP is MagicLP {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L9)

```solidity
File: src/blast/BlastOnboarding.sol

11: contract BlastOnboardingData is Owned, Pausable {
63: contract BlastOnboarding is BlastOnboardingData, Proxy {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L11) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L63)

```solidity
File: src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23)

```solidity
File: src/blast/BlastTokenRegistry.sol

5: contract BlastTokenRegistry is Owned {
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L5)

```solidity
File: src/blast/BlastWrappers.sol

18: contract BlastMIMSwapRouter is Router {
27: contract BlastMIMSwapFactory is Factory {
41: contract BlastCauldronV4 is CauldronV4 {
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L18) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L27) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L41)

```solidity
File: src/blast/libraries/BlastPoints.sol

5: library BlastPoints {
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L5)

```solidity
File: src/blast/libraries/BlastYields.sol

6: library BlastYields {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L6)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

12: contract FeeRateModel is Owned {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L12)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

6: contract FeeRateModelImpl {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L6)

```solidity
File: src/mimswap/periphery/Router.sol

11: contract Router {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L11)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

8: contract MagicLpAggregator is IAggregator {
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L8)
</details>

### [N-67] NatSpec: Contract declarations should have `@author` tag

In the world of decentralized code, giving credit is key. NatSpec's `@author` tag acknowledges the minds behind the code.
It appears this Solidity contract omits the `@author` directive in its NatSpec annotations.
Properly attributing code to its contributors not only recognizes effort but also aids in establishing trust and credibility.
[Dive Deeper into NatSpec Guidelines](https://docs.soliditylang.org/en/develop/natspec-format.html)

<details>
<summary><i>19 issue instances in 15 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

6: contract BlastDapp {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L6)

```solidity
File: src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L13)

```solidity
File: src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L7)

```solidity
File: src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L10)

```solidity
File: src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData is Owned, Pausable {
64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L12) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L64)

```solidity
File: src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L34)

```solidity
File: src/blast/BlastTokenRegistry.sol

6: contract BlastTokenRegistry is Owned {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L6)

```solidity
File: src/blast/BlastWrappers.sol

19: contract BlastMIMSwapRouter is Router {
28: contract BlastMIMSwapFactory is Factory {
42: contract BlastCauldronV4 is CauldronV4 {
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L19) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L28) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L42)

```solidity
File: src/blast/libraries/BlastPoints.sol

6: library BlastPoints {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L6)

```solidity
File: src/blast/libraries/BlastYields.sol

7: library BlastYields {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L7)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

13: contract FeeRateModel is Owned {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L13)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

7: contract FeeRateModelImpl {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L7)

```solidity
File: src/mimswap/periphery/Factory.sol

11: contract Factory is Owned {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L11)

```solidity
File: src/mimswap/periphery/Router.sol

12: contract Router {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L12)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

9: contract MagicLpAggregator is IAggregator {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L9)
</details>

### [N-68] Inconsistent method of specifying a floating pragma

The Solidity files in the project use inconsistent methods for specifying the compiler version. Some use `>=` while others use `^`. It's advisable to use `^` to avoid compatibility issues when the major version changes.

Using `>=` without also specifying `<=` can lead to compilation errors or external project incompatibility when there are breaking changes in new major versions of the Solidity compiler.

<details>
<summary><i>20 issue instances in 20 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2)

```solidity
File: src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L3)

```solidity
File: src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L2)

```solidity
File: src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L3)

```solidity
File: src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L2)

```solidity
File: src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L2)

```solidity
File: src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L2)

```solidity
File: src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L2)

```solidity
File: src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L2)

```solidity
File: src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L2)

```solidity
File: src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L7)

```solidity
File: src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L8)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L8)

```solidity
File: src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L2)

```solidity
File: src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L2)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L2)

```solidity
File: src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L2)
</details>

### [N-69] Style guide: Non-`external`/`public` function names should begin with an underscore

In Solidity, it is suggested to use a leading underscore for non-public (private and internal) function names.
This convention helps to distinguish clearly between public/external and non-public functions, improving code clarity.
By adhering to this convention, developers can mitigate potential misinterpretation or errors, thus making the code more comprehensible and easier to maintain.

<details>
<summary><i>25 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

102: function isOwner(address _account) internal view override returns (bool) {
```
[102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L102)

```solidity
File: src/blast/libraries/BlastPoints.sol

9: function configure() internal {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L9)

```solidity
File: src/blast/libraries/BlastYields.sol

19: function enableTokenClaimable(address token) internal {
28: function configureDefaultClaimables(address governor_) internal {
37: function claimMaxGasYields(address recipient) internal returns (uint256) {
41: function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {
50: function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
54: function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {
59: function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {
69: function claimAllTokenYields(address token, address recipient) internal returns (uint256 amount) {
74: function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {
85: function callPrecompile(bytes calldata data) internal {
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L19) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L28) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L37) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L41) | [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L50) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L54) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L59) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L69) | [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L74) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L85)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

22: function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {
26: function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {
30: function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {
34: function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {
38: function reciprocalFloor(uint256 target) internal pure returns (uint256) {
42: function reciprocalCeil(uint256 target) internal pure returns (uint256) {
46: function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L22) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L26) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L30) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L34) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L38) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L42) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L46)

```solidity
File: src/mimswap/libraries/Math.sol

18: function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {
28: function sqrt(uint256 x) internal pure returns (uint256 y) {
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L18) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L28)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

38: function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {
75: function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {
189: function adjustedTarget(PMMState memory state) internal pure {
202: function getMidPrice(PMMState memory state) internal pure returns (uint256) {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L38) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L75) | [189](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L189) | [202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L202)
</details>

### [N-70] Missing NatSpec Descriptions for Event Declarations

Event declarations should have accompanying NatSpec comments with `@dev` or `@notice` tag to describe their purpose and the meaning of emitted parameters. 
These comments provide clarity for developers, reviewers, and users of the contract.
[More information in Documentation](https://docs.soliditylang.org/en/latest/natspec-format.html)

<details>
<summary><i>52 issue instances in 11 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

14: event LogTokenDepositEnabled(address indexed token, bool enabled);
15: event LogFeeToChanged(address indexed feeTo);
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L14) | [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L15)

```solidity
File: src/blast/BlastGovernor.sol

8: event LogFeeToChanged(address indexed feeTo);
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L8)

```solidity
File: src/blast/BlastMagicLP.sol

11: event LogFeeToChanged(address indexed feeTo);
12: event LogOperatorChanged(address indexed, bool);
13: event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L11) | [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L12) | [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L13)

```solidity
File: src/blast/BlastOnboarding.sol

67: event LogBootstrapperChanged(address indexed bootstrapper);
68: event LogTokenSupported(address indexed token, bool supported);
69: event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);
70: event LogLock(address indexed user, address indexed token, uint256 amount);
71: event LogFeeToChanged(address indexed feeTo);
72: event LogWithdraw(address indexed user, address indexed token, uint256 amount);
73: event LogTokenCapChanged(address indexed token, uint256 cap);
74: event LogStateChange(State state);
75: event LogTokenRescue(address indexed token, address indexed to, uint256 amount);
```
[67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L67) | [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L68) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L69) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L70) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L71) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L72) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L73) | [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L74) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L75)

```solidity
File: src/blast/BlastOnboardingBoot.sol

37: event LogReadyChanged(bool ready);
38: event LogClaimed(address indexed user, uint256 shares, bool lock);
39: event LogInitialized(Router indexed router);
40: event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);
41: event LogStakingChanged(address indexed staking);
```
[37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L37) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L38) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L39) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L40) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L41)

```solidity
File: src/blast/BlastTokenRegistry.sol

7: event LogNativeYieldTokenEnabled(address indexed token, bool enabled);
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L7)

```solidity
File: src/blast/libraries/BlastYields.sol

8: event LogBlastGasClaimed(address indexed recipient, uint256 amount);
9: event LogBlastETHClaimed(address indexed recipient, uint256 amount);
10: event LogBlastTokenClaimed(address indexed recipient, address indexed token, uint256 amount);
11: event LogBlastTokenClaimableEnabled(address indexed contractAddress, address indexed token);
12: event LogBlastNativeClaimableEnabled(address indexed contractAddress);
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L8) | [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L9) | [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L10) | [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L11) | [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L12)

```solidity
File: src/mimswap/MagicLP.sol

30: event BuyShares(address to, uint256 increaseShares, uint256 totalShares);
31: event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);
32: event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);
33: event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);
34: event RChange(PMMPricing.RState newRState);
35: event TokenRescue(address indexed token, address to, uint256 amount);
36: event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);
```
[30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L30) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L31) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L32) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L33) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L34) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L35) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L36)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

14: event LogImplementationChanged(address indexed implementation);
15: event LogMaintainerChanged(address indexed maintainer);
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L14) | [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L15)

```solidity
File: src/mimswap/periphery/Factory.sol

23: event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);
24: event LogPoolRemoved(address pool);
25: event LogSetImplementation(address indexed implementation);
26: event LogSetMaintainer(address indexed newMaintainer);
27: event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L23) | [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L24) | [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L25) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L26) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L27)

```solidity
File: src/staking/LockingMultiRewards.sol

17: event LogRewardAdded(uint256 reward);
18: event LogStaked(address indexed user, uint256 amount);
19: event LogLocked(address indexed user, uint256 amount, uint256 unlockTime, uint256 lockCount);
20: event LogUnlocked(address indexed user, uint256 amount, uint256 index);
21: event LogLockIndexChanged(address indexed user, uint256 fromIndex, uint256 toIndex);
22: event LogWithdrawn(address indexed user, uint256 amount);
23: event LogRewardLockCreated(address indexed user, uint256 unlockTime);
24: event LogRewardLocked(address indexed user, address indexed rewardsToken, uint256 reward);
25: event LogRewardPaid(address indexed user, address indexed rewardsToken, uint256 reward);
26: event LogRewardsDurationUpdated(address token, uint256 newDuration);
27: event LogRecovered(address token, uint256 amount);
28: event LogSetMinLockAmount(uint256 previous, uint256 current);
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L17) | [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L18) | [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L19) | [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L21) | [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L22) | [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L23) | [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L24) | [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L25) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L26) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L27) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L28)
</details>

### [N-71] Consider defining system-wide constants in a single file

System-wide constants should be declared in a single file for better maintainability and readability.
This contract seems to contain constants which could potentially be system-wide and could be better managed if they were centralized in a single location.

<details>
<summary><i>17 issue instances in 5 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

13: address constant USDB = 0x4300000000000000000000000000000000000003;
14: address constant MIM = 0x76DA31D7C9CbEAE102aff34D3398bC450c8374c1;
15: uint256 constant FEE_RATE = 0.0005 ether; // 0.05%
16: uint256 constant K = 0.00025 ether; // 0.00025, 1.25% price fluctuation, similar to A2000 in curve
17: uint256 constant I = 0.998 ether; // 1 MIM = 0.998 USDB
18: uint256 constant USDB_TO_MIN = 1.002 ether; // 1 USDB = 1.002 MIM
19: uint256 constant MIM_TO_MIN = I;
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L14) | [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L15) | [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L16) | [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L17) | [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L18) | [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L19)

```solidity
File: src/mimswap/MagicLP.sol

63: uint256 public constant MAX_I = 10 ** 36;
64: uint256 public constant MAX_K = 10 ** 18;
65: uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%
66: uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%
```
[63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L65) | [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L66)

```solidity
File: src/mimswap/periphery/Router.sol

31: uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;
```
[31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L31)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

16: uint256 public constant WAD = 18;
```
[16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L16)

```solidity
File: src/staking/LockingMultiRewards.sol

78: uint256 private constant BIPS = 10_000;
79: uint256 private constant MAX_NUM_REWARDS = 5;
80: uint256 private constant MIN_LOCK_DURATION = 1 weeks;
81: uint256 private constant MIN_REWARDS_DURATION = 1 days;
```
[78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L78) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L79) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L80) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L81)
</details>

### [N-72] Consider making contracts `Upgradeable`

Contract uses a non-upgradeable design.
Transitioning to an upgradeable contract structure is more aligned with contemporary smart contract practices.
This approach not only enhances flexibility but also allows for continuous improvement and adaptation, ensuring the contract stays relevant and robust in an ever-evolving ecosystem.

<details>
<summary><i>19 issue instances in 15 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

/// @audit - Contract `BlastDapp` is not upgradeable
5: contract BlastDapp {
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L5)

```solidity
File: src/blast/BlastBox.sol

/// @audit - Contract `BlastBox` is not upgradeable
12: contract BlastBox is DegenBox, OperatableV3 {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L12)

```solidity
File: src/blast/BlastGovernor.sol

/// @audit - Contract `BlastGovernor` is not upgradeable
6: contract BlastGovernor is OperatableV2 {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L6)

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit - Contract `BlastMagicLP` is not upgradeable
9: contract BlastMagicLP is MagicLP {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L9)

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit - Contract `BlastOnboardingData` is not upgradeable
11: contract BlastOnboardingData is Owned, Pausable {
/// @audit - Contract `BlastOnboarding` is not upgradeable
63: contract BlastOnboarding is BlastOnboardingData, Proxy {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L11) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L63)

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit - Contract `BlastOnboardingBootDataV1` is not upgradeable
23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
/// @audit - Contract `BlastOnboardingBoot` is not upgradeable
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L34)

```solidity
File: src/blast/BlastTokenRegistry.sol

/// @audit - Contract `BlastTokenRegistry` is not upgradeable
5: contract BlastTokenRegistry is Owned {
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L5)

```solidity
File: src/blast/BlastWrappers.sol

/// @audit - Contract `BlastMIMSwapRouter` is not upgradeable
18: contract BlastMIMSwapRouter is Router {
/// @audit - Contract `BlastMIMSwapFactory` is not upgradeable
27: contract BlastMIMSwapFactory is Factory {
/// @audit - Contract `BlastCauldronV4` is not upgradeable
41: contract BlastCauldronV4 is CauldronV4 {
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L18) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L27) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L41)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit - Contract `MagicLP` is not upgradeable
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L25)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit - Contract `FeeRateModel` is not upgradeable
12: contract FeeRateModel is Owned {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L12)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

/// @audit - Contract `FeeRateModelImpl` is not upgradeable
6: contract FeeRateModelImpl {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L6)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit - Contract `Factory` is not upgradeable
11: contract Factory is Owned {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L11)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit - Contract `Router` is not upgradeable
11: contract Router {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L11)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

/// @audit - Contract `MagicLpAggregator` is not upgradeable
8: contract MagicLpAggregator is IAggregator {
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L8)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit - Contract `LockingMultiRewards` is not upgradeable
14: contract LockingMultiRewards is OperatableV2, Pausable {
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L14)
</details>

### [N-73] Events that mark critical parameter changes should contain both the old and the new value

When emitting events that signify critical changes in parameters, it's important to include both the old and new values. 

This aids in auditability, providing more complete information about the state change. It's especially necessary when the new value isn't required to be different from the old one, as this prevents ambiguity in event logs.

<details>
<summary><i>15 issue instances in 9 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

78: emit LogFeeToChanged(feeTo_);
```
[78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L78)

```solidity
File: src/blast/BlastGovernor.sol

46: emit LogFeeToChanged(_feeTo);
```
[46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L46)

```solidity
File: src/blast/BlastMagicLP.sol

86: emit LogFeeToChanged(feeTo_);
```
[86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L86)

```solidity
File: src/blast/BlastOnboarding.sol

153: emit LogFeeToChanged(feeTo_);
```
[153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L153)

```solidity
File: src/blast/BlastOnboardingBoot.sol

132: emit LogInitialized(_router);
143: emit LogStakingChanged(address(_staking));
```
[132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L132) | [143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L143)

```solidity
File: src/mimswap/MagicLP.sol

259: emit RChange(newRState);
282: emit RChange(newRState);
323: emit RChange(newRState);
345: emit RChange(newRState);
```
[259](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L259) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L282) | [323](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L323) | [345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L345)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

52: emit LogMaintainerChanged(maintainer_);
```
[52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L52)

```solidity
File: src/mimswap/periphery/Factory.sol

102: emit LogSetImplementation(implementation_);
111: emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);
141: emit LogPoolRemoved(pool);
```
[102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L102) | [111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L111) | [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L141)

```solidity
File: src/staking/LockingMultiRewards.sol

392: emit LogRewardAdded(amount);
```
[392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L392)
</details>

### [N-74] Style guide: Non-`external`/`public` variable names should begin with an underscore

The naming convention for non-public (private and internal) variables in Solidity recommends the use of a leading underscore.

Since `constants` can be public, to avoid confusion, they should also be prefixed with an underscore.

This practice clearly differentiates between public/external and non-public variables, enhancing code clarity and reducing the likelihood of misinterpretation or errors.
Following this convention improves code readability and maintainability.

<details>
<summary><i>14 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

13: address constant USDB = 0x4300000000000000000000000000000000000003;
14: address constant MIM = 0x76DA31D7C9CbEAE102aff34D3398bC450c8374c1;
15: uint256 constant FEE_RATE = 0.0005 ether; // 0.05%
16: uint256 constant K = 0.00025 ether; // 0.00025, 1.25% price fluctuation, similar to A2000 in curve
17: uint256 constant I = 0.998 ether; // 1 MIM = 0.998 USDB
18: uint256 constant USDB_TO_MIN = 1.002 ether; // 1 USDB = 1.002 MIM
19: uint256 constant MIM_TO_MIN = I;
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L14) | [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L15) | [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L16) | [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L17) | [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L18) | [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L19)

```solidity
File: src/blast/libraries/BlastYields.sol

14: IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L14)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

20: uint256 internal constant ONE = 10 ** 18;
21: uint256 internal constant ONE2 = 10 ** 36;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L21)

```solidity
File: src/staking/LockingMultiRewards.sol

78: uint256 private constant BIPS = 10_000;
79: uint256 private constant MAX_NUM_REWARDS = 5;
80: uint256 private constant MIN_LOCK_DURATION = 1 weeks;
81: uint256 private constant MIN_REWARDS_DURATION = 1 days;
```
[78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L78) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L79) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L80) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L81)
</details>

### [N-75] Style guide: Contract does not follow the Solidity style guide's suggested layout ordering

Adhering to a recommended order in Solidity contracts enhances code readability and maintenance.
[More information in Documentation](https://docs.soliditylang.org/en/latest/style-guide.html#order-of-layout)
It's recommended to use the following order:
1. Type declarations
2. State variables
3. Events
4. Errors
5. Modifiers
6. Functions

<details>
<summary><i>14 issue instances in 11 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

/// @audit `state variable` declared after `error`
20: BlastTokenRegistry public immutable registry;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L20)

```solidity
File: src/blast/BlastGovernor.sol

/// @audit `state variable` declared after `error`
11: address public feeTo;
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L11)

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit `state variable` declared after `error`
17: BlastTokenRegistry public immutable registry;
/// @audit `modifier` declared after `function`
117: modifier onlyImplementationOperators() {
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L17) | [117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L117)

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit `type` declared after `error`
17: enum State {
        Idle,
        Opened,
        Closed
    }
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L17)

```solidity
File: src/blast/BlastTokenRegistry.sol

/// @audit `state variable` declared after `error`
10: mapping(address => bool) public nativeYieldTokens;
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10)

```solidity
File: src/blast/BlastWrappers.sol

/// @audit `state variable` declared after `error`
45: address private immutable _governor;
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L45)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit `state variable` declared after `error`
61: MagicLP public immutable implementation;
/// @audit `modifier` declared after `function`
606: modifier onlyImplementationOwner() {
```
[61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L61) | [606](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L606)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit `state variable` declared after `error`
19: address public maintainer;
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L19)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit `state variable` declared after `error`
32: address public implementation;
```
[32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L32)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit `state variable` declared after `error`
31: uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;
/// @audit `modifier` declared after `constructor`
46: modifier ensureDeadline(uint256 deadline) {
```
[31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L31) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L46)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit `type` declared after `error`
49: struct Reward {
        uint256 periodFinish;
        uint256 rewardRate;
        uint256 rewardPerTokenStored;
        bool exists;
        uint248 lastUpdateTime;
    }
```
[49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L49)
</details>

### [N-76] Style guide: Control structures do not follow the Solidity Style Guide

Following best practices for control structures in solidity code is vital for readability and maintainability. The control structures in contracts, libraries, functions, and structs should adhere to the following standards:

- Braces denoting the body should open on the same line as the declaration and close on their own line at the same indentation level as the beginning of the declaration. 
- A single space should precede the opening brace. 
- Control structures such as 'if', 'else', 'while', and 'for' should also follow these spacing and brace placement recommendations.

It is advised to revisit the [control structures](https://docs.soliditylang.org/en/latest/style-guide.html#control-structures) sections in documentation to ensure conformity with these best practices, fostering cleaner and more maintainable code.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastGovernor.sol

/// @audit `Space missing between "if" keyword and condition.`
41: if(_feeTo == address(0)) {
```
[41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L41)
</details>

### [N-77] Using Low-Level Call for Transfers

Directly using low-level calls for Ether transfers can introduce vulnerabilities and obscure the intent of your transfers.
Adopt modern Solidity best practices by switching to recognized libraries like `SafeTransferLib.safeTransferETH` or `Address.sendValue`.
This ensures safer transactions, enhances code clarity, and aligns with the standards of the Solidity community.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastGovernor.sol

54: (success, result) = to.call{value: value}(data);
```
[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L54)
</details>

### [N-78] Consider bounding input array length

The functions in question operate on arrays without established boundaries, executing function calls for each of their entries.
If these arrays become excessively long, a function might revert due to gas constraints.
To enhance user experience, consider incorporating a `require()` statement that enforces a sensible maximum array length.
This approach can avoid unnecessary computational work and ensure smoother transactions.

<details>
<summary><i>3 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit `tokens` is a function array parameter and `tokens.length` is not bounded
165: for (uint256 i = 0; i < tokens.length; i++) {
```
[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit `iterations` equal to `path.length - 1` and it not bounded
544: for (uint256 i = 0; i < iterations; ) {
```
[544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit `users` is a function array parameter and `users.length` is not bounded
580: for (uint256 j; j < users.length; ) {
```
[580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580)
</details>

### [N-79] NatSpec: Function declarations should have `@notice` tag

In Solidity, the `@notice` tag in NatSpec comments is used to provide important explanations to end users about what a function does. 
It appears that this contract's function declarations are missing `@notice` tags in their NatSpec annotations.

The absence of `@notice` tags reduces the contract's transparency and could lead to misunderstandings about a function's purpose and behavior.
Note that the Solidity compiler treats comments beginning with `///` or `/**` as `@notice` tags if one wasn't explicitly provided.
[Learn More About NatSpec Guidelines](https://docs.soliditylang.org/en/develop/natspec-format.html)

<details>
<summary><i>137 issue instances in 15 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

7: constructor() {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L7)

```solidity
File: src/blast/BlastBox.sol

24: constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
52: function claimGasYields() external onlyOperators returns (uint256) {
56: function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
68: function callBlastPrecompile(bytes calldata data) external onlyOwner {
72: function setFeeTo(address feeTo_) external onlyOwner {
81: function setTokenEnabled(address token, bool enabled) external onlyOwner {
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L52) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L56) | [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L68) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81)

```solidity
File: src/blast/BlastGovernor.sol

15: constructor(address feeTo_, address _owner) OperatableV2(_owner) {
28: function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
32: function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
40: function setFeeTo(address _feeTo) external onlyOwner {
49: function callBlastPrecompile(bytes calldata data) external onlyOwner {
53: function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```
[15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L28) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L32) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L49) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)

```solidity
File: src/blast/BlastMagicLP.sol

23: constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
39: function version() external pure override returns (string memory) {
47: function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {
53: function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {
64: function updateTokenClaimables() external onlyClones onlyImplementationOperators {
72: function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {
80: function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
89: function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L39) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L47) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L53) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L64) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L72) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89)

```solidity
File: src/blast/BlastOnboarding.sol

58: constructor() Owned(msg.sender) {
101: function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
123: function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
132: function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
147: function setFeeTo(address feeTo_) external onlyOwner {
156: function callBlastPrecompile(bytes calldata data) external onlyOwner {
160: function claimGasYields() external onlyOwner returns (uint256) {
164: function claimTokenYields(address[] memory tokens) external onlyOwner {
175: function setTokenSupported(address token, bool supported) external onlyOwner {
185: function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
190: function setBootstrapper(address bootstrapper_) external onlyOwner {
195: function open() external onlyOwner onlyState(State.Idle) {
200: function close() external onlyOwner onlyState(State.Opened) {
205: function rescue(address token, address to, uint256 amount) external onlyOwner {
214: function pause() external onlyOwner {
218: function unpause() external onlyOwner {
```
[58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L58) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101) | [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L156) | [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L160) | [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164) | [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185) | [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190) | [195](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L195) | [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L200) | [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L205) | [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L214) | [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L218)

```solidity
File: src/blast/BlastOnboardingBoot.sol

55: function claim(bool lock) external returns (uint256 shares) {
78: function claimable(address user) external view returns (uint256 shares) {
86: function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
96: function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
129: function initialize(Router _router) external onlyOwner {
137: function setStaking(LockingMultiRewards _staking) external onlyOwner {
146: function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
```
[55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L55) | [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L78) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96) | [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129) | [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146)

```solidity
File: src/blast/BlastTokenRegistry.sol

12: constructor(address _owner) Owned(_owner) {}
14: function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14)

```solidity
File: src/blast/BlastWrappers.sol

20: constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
59: function init(bytes calldata data) public payable override {
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59)

```solidity
File: src/mimswap/MagicLP.sol

84: constructor(address owner_) Owned(owner_) {
91: function init(
        address baseTokenAddress,
        address quoteTokenAddress,
        uint256 lpFeeRate,
        address mtFeeRateModel,
        uint256 i,
        uint256 k
    ) external {
134: function sync() external nonReentrant {
138: function correctRState() external {
155: function name() public view override returns (string memory) {
159: function symbol() public pure override returns (string memory) {
163: function decimals() public view override returns (uint8) {
167: function querySellBase(
        address trader,
        uint256 payBaseAmount
    ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {
180: function querySellQuote(
        address trader,
        uint256 payQuoteAmount
    ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {
193: function getPMMState() public view returns (PMMPricing.PMMState memory state) {
204: function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
215: function getMidPrice() public view returns (uint256 midPrice) {
219: function getReserves() external view returns (uint256 baseReserve, uint256 quoteReserve) {
224: function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
228: function getBaseInput() public view returns (uint256 input) {
232: function getQuoteInput() public view returns (uint256 input) {
236: function version() external pure virtual returns (string memory) {
244: function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {
267: function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {
290: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
360: function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
413: function sellShares(
        uint256 shareAmount,
        address to,
        uint256 baseMinAmount,
        uint256 quoteMinAmount,
        bytes calldata data,
        uint256 deadline
    ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {
461: function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {
470: function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner {
504: function ratioSync() external nonReentrant onlyImplementationOwner {
```
[84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L91) | [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L134) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L138) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155) | [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L159) | [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163) | [167](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L167) | [180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L180) | [193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L193) | [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204) | [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L215) | [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L219) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L224) | [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L228) | [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L232) | [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L236) | [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L244) | [267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L267) | [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360) | [413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L413) | [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L461) | [470](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470) | [504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L504)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

22: constructor(address maintainer_, address owner_) Owned(owner_) {
34: function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
46: function setMaintainer(address maintainer_) external onlyOwner {
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

9: function getFeeRate(
        address /*pool*/,
        address /*trader*/,
        uint256 lpFeeRate
    ) external pure returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9)

```solidity
File: src/mimswap/periphery/Factory.sol

38: constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
53: function getPoolCount(address token0, address token1) external view returns (uint256) {
57: function getUserPoolCount(address creator) external view returns (uint256) {
65: function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address) {
81: function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
96: function setLpImplementation(address implementation_) external onlyOwner {
105: function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
120: function removePool(
        address creator,
        address baseToken,
        address quoteToken,
        uint256 poolIndex,
        uint256 userPoolIndex
    ) external onlyOwner {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L53) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L57) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96) | [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105) | [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L120)

```solidity
File: src/mimswap/periphery/Router.sol

38: constructor(IWETH weth_, IFactory factory_) {
54: function createPool(
        address baseToken,
        address quoteToken,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external returns (address clone, uint256 shares) {
73: function createPoolETH(
        address token,
        bool useTokenAsQuote,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 tokenInAmount
    ) external payable returns (address clone, uint256 shares) {
96: function previewCreatePool(
        uint256 i,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external pure returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
112: function previewAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
162: function addLiquidity(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
178: function addLiquidityUnsafe(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 shares) {
192: function addLiquidityETH(
        address lp,
        address to,
        address payable refundTo,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
229: function addLiquidityETHUnsafe(
        address lp,
        address to,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 shares) {
251: function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
261: function removeLiquidity(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumBaseAmount,
        uint256 minimumQuoteAmount,
        uint256 deadline
    ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
274: function removeLiquidityETH(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumETHAmount,
        uint256 minimumTokenAmount,
        uint256 deadline
    ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {
314: function swapTokensForTokens(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
336: function swapETHForTokens(
        address to,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
365: function swapTokensForETH(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
404: function sellBaseTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
415: function sellBaseETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
432: function sellBaseTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
449: function sellQuoteTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
461: function sellQuoteETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
478: function sellQuoteTokensForETH(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L54) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L73) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L96) | [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L112) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L162) | [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L178) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192) | [229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229) | [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L251) | [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L261) | [274](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L274) | [314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L314) | [336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336) | [365](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L365) | [404](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L404) | [415](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L415) | [432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L432) | [449](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L449) | [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L461) | [478](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L478)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

21: constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
29: function decimals() external pure override returns (uint8) {
37: function latestAnswer() public view override returns (int256) {
48: function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L29) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L37) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L48)

```solidity
File: src/staking/LockingMultiRewards.sol

112: constructor(
        address _stakingToken,
        uint256 _lockingBoostMultiplerInBips,
        uint256 _rewardsDuration,
        uint256 _lockDuration,
        address _owner
    ) OperatableV2(_owner) {
186: function withdrawWithRewards(uint256 amount) public virtual {
191: function getRewards() public virtual {
199: function rewardData(address token) external view returns (Reward memory) {
203: function rewardsForDuration(address rewardToken) external view returns (uint256) {
207: function rewardTokensLength() external view returns (uint256) {
211: function balances(address user) external view returns (Balances memory) {
215: function userRewardLock(address user) external view returns (RewardLock memory) {
219: function userLocks(address user) external view returns (LockedBalance[] memory) {
223: function userLocksLength(address user) external view returns (uint256) {
227: function locked(address user) external view returns (uint256) {
231: function unlocked(address user) external view returns (uint256) {
235: function totalSupply() public view returns (uint256) {
239: function balanceOf(address user) public view returns (uint256) {
253: function nextUnlockTime() public view returns (uint256) {
257: function epoch() public view returns (uint256) {
261: function nextEpoch() public view returns (uint256) {
265: function remainingEpochTime() public view returns (uint256) {
269: function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {
273: function rewardPerToken(address rewardToken) public view returns (uint256) {
277: function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
288: function earned(address user, address rewardToken) public view returns (uint256) {
300: function addReward(address rewardToken) public onlyOwner {
317: function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
337: function pause() external onlyOwner {
341: function unpause() external onlyOwner {
349: function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {
```
[112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L112) | [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L186) | [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L191) | [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L203) | [207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L207) | [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L211) | [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L215) | [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L219) | [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L223) | [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L227) | [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L231) | [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L235) | [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L239) | [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L253) | [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L257) | [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L261) | [265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L265) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L269) | [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L273) | [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277) | [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L288) | [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300) | [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317) | [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337) | [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L341) | [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L349)
</details>

### [N-80] Constants in comparisons should appear on the left side

Placing constants on the left side of comparison statements can help prevent accidental assignments and improve code readability.
In languages like C, placing constants on the left can protect against unintended assignments that would be treated as true conditions, leading to bugs.
Although Solidity does not have this specific issue, using the same practice can still be beneficial for code readability and consistency.

Consider placing constants on the left side of comparison operators like `==`, `!=`, `<`, `>`, `<=`, and `>=`."

<details>
<summary><i>53 issue instances in 7 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

114: if (caps[token] > 0 && totals[token].total > caps[token]) {
```
[114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114)

```solidity
File: src/blast/BlastOnboardingBoot.sol

64: if (shares == 0) {
158: if (totalLocked == 0) {
```
[64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L64) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L158)

```solidity
File: src/mimswap/MagicLP.sol

108: if (i == 0 || i > MAX_I) {
294: if (data.length > 0) {
369: if (baseInput == 0) {
377: if (quoteBalance == 0) {
385: if (_QUOTE_TARGET_ == 0) {
389: if (shares <= 2001) {
395: } else if (baseReserve > 0 && quoteReserve > 0) {
450: if (data.length > 0) {
483: if (newI == 0 || newI > MAX_I) {
549: if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
582: if (amount > 0) {
588: if (amount > 0) {
594: if (amount <= 1000) {
```
[108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L108) | [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L294) | [369](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L369) | [377](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L377) | [385](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L385) | [389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L389) | [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395) | [450](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L450) | [483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L483) | [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549) | [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L582) | [588](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L588) | [594](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L594)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

48: if (e == 0) {
50: } else if (e == 1) {
55: if (e % 2 == 1) {
```
[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L48) | [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L50) | [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L55)

```solidity
File: src/mimswap/libraries/Math.sol

22: if (remainder > 0) {
52: if (V0 == 0) {
58: if (k == 0) {
80: if (k == 0) {
89: if (V1 == 0) {
94: if (ki == 0) {
132: if (V0 == 0) {
136: if (delta == 0) {
140: if (k == 0) {
153: if (idelta == 0) {
192: if (numerator == 0) {
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L22) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L52) | [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L58) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L80) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L89) | [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L94) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L132) | [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L136) | [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L140) | [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L153) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L192)

```solidity
File: src/mimswap/periphery/Router.sol

105: if (shares <= 2001) {
125: if (baseInAmount == 0) {
131: if (totalSupply == 0) {
132: if (quoteBalance == 0) {
142: if (shares <= 2001) {
147: } else if (baseReserve > 0 && quoteReserve > 0) {
327: if (directions & 1 == 0) {
348: if (directions & 1 == 0) {
392: if (directions & 1 == 0) {
527: if (quoteReserve > 0 && baseReserve > 0) {
545: if (directions & 1 == 0) {
560: if ((directions & 1 == 0)) {
590: if (pathLength > 256) {
593: if (pathLength <= 0) {
599: if (baseDecimals == 0 || quoteDecimals == 0) {
```
[105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L105) | [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L125) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L131) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L132) | [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L142) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147) | [327](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L327) | [348](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L348) | [392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L392) | [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527) | [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L545) | [560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L560) | [590](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L590) | [593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L593) | [599](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L599)

```solidity
File: src/staking/LockingMultiRewards.sol

131: if (_lockDuration % _rewardsDuration != 0) {
156: if (amount == 0) {
171: if (amount == 0) {
278: if (totalSupply_ == 0) {
410: if (locks.length == 0) {
459: if (amount == 0) {
490: if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {
636: if (amount > 0) {
```
[131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L131) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L156) | [171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L171) | [278](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L278) | [410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L410) | [459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L459) | [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L490) | [636](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L636)
</details>

### [N-81] NatSpec: Contract declarations should have `@notice` tag

The `@notice` tag in NatSpec annotations serves to provide information about the contract's functionality that is visible to end-users.
Including `@notice` comments helps to improve the contract's transparency and ease of understanding, contributing to the overall trust and credibility of the code.
[NatSpec Guidelines](https://docs.soliditylang.org/en/develop/natspec-format.html)

<details>
<summary><i>19 issue instances in 15 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

6: contract BlastDapp {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L6)

```solidity
File: src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L13)

```solidity
File: src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L7)

```solidity
File: src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L10)

```solidity
File: src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData is Owned, Pausable {
64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L12) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L64)

```solidity
File: src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L34)

```solidity
File: src/blast/BlastTokenRegistry.sol

6: contract BlastTokenRegistry is Owned {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L6)

```solidity
File: src/blast/BlastWrappers.sol

19: contract BlastMIMSwapRouter is Router {
28: contract BlastMIMSwapFactory is Factory {
42: contract BlastCauldronV4 is CauldronV4 {
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L19) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L28) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L42)

```solidity
File: src/blast/libraries/BlastPoints.sol

6: library BlastPoints {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L6)

```solidity
File: src/blast/libraries/BlastYields.sol

7: library BlastYields {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L7)

```solidity
File: src/mimswap/MagicLP.sol

25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L25)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

13: contract FeeRateModel is Owned {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L13)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

7: contract FeeRateModelImpl {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L7)

```solidity
File: src/mimswap/periphery/Router.sol

12: contract Router {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L12)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

9: contract MagicLpAggregator is IAggregator {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L9)
</details>

### [N-82] Large numeric literals should use underscores for readability

Large numeric literals are often hard to read and prone to mistakes.
To improve readability and reduce the likelihood of errors, it is recommended to separate the digits of large numeric literals using underscores.
For example, instead of '1000000', use '1_000_000'.

<details>
<summary><i>15 issue instances in 7 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

15: uint256 constant FEE_RATE = 0.0005 ether; // 0.05%
16: uint256 constant K = 0.00025 ether; // 0.00025, 1.25% price fluctuation, similar to A2000 in curve
```
[15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L15) | [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L16)

```solidity
File: src/mimswap/MagicLP.sol

3: Copyright 2020 DODO ZOO.
389: if (shares <= 2001) {
393: _mint(address(0), 1001);
394: shares -= 1001;
594: if (amount <= 1000) {
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L3) | [389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L389) | [393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L393) | [394](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L394) | [594](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L594)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

3: Copyright 2020 DODO ZOO.
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L3)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

3: Copyright 2020 DODO ZOO.
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L3)

```solidity
File: src/mimswap/libraries/Math.sol

3: Copyright 2020 DODO ZOO.
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L3)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

3: Copyright 2020 DODO ZOO.
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L3)

```solidity
File: src/mimswap/periphery/Router.sol

105: if (shares <= 2001) {
109: shares -= 1001;
142: if (shares <= 2001) {
146: shares -= 1001;
```
[105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L105) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L109) | [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L142) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L146)
</details>

### [N-83] Long functions should be refactored into multiple, smaller, functions

Functions that span many lines can be hard to understand and maintain.
It is often beneficial to refactor long functions into multiple smaller functions.
This improves readability, makes testing easier, and can even lead to gas optimization if it eliminates the need for variables that would otherwise have to be stored in memory.

<details>
<summary><i>6 issue instances in 4 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

 /// @audit 46 lines (excluding comments)
289: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
 /// @audit 35 lines (excluding comments)
360: function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
```
[289](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L289) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360)

```solidity
File: src/mimswap/libraries/Math.sol

 /// @audit 50 lines (excluding comments)
131: function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```
[131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)

```solidity
File: src/mimswap/periphery/Router.sol

 /// @audit 34 lines (excluding comments)
111: function previewAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
```
[111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L111)

```solidity
File: src/staking/LockingMultiRewards.sol

 /// @audit 37 lines (excluding comments)
397: function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
 /// @audit 32 lines (excluding comments)
597: function _getRewards(address user) internal {
```
[397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397) | [597](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L597)
</details>

### [N-84] NatSpec: Contract declarations should have `@dev` tags

NatSpec comments are a critical part of Solidity's documentation system, designed to help developers and others understand the behavior and purpose of a contract.
The `@dev` tag, in particular, provides context and insight into the contract's development considerations.
A missing `@dev` comment can lead to misunderstandings about the contract, making it harder for others to contribute to or use the contract effectively.
Therefore, it's highly recommended to include `@dev` comments in the documentation to enhance code readability and maintainability.
[Refer to NatSpec Documentation](https://docs.soliditylang.org/en/develop/natspec-format.html)

<details>
<summary><i>23 issue instances in 20 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

6: contract BlastDapp {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L6)

```solidity
File: src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L13)

```solidity
File: src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L7)

```solidity
File: src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L10)

```solidity
File: src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData is Owned, Pausable {
64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L12) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L64)

```solidity
File: src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23)

```solidity
File: src/blast/BlastTokenRegistry.sol

6: contract BlastTokenRegistry is Owned {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L6)

```solidity
File: src/blast/BlastWrappers.sol

19: contract BlastMIMSwapRouter is Router {
28: contract BlastMIMSwapFactory is Factory {
42: contract BlastCauldronV4 is CauldronV4 {
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L19) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L28) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L42)

```solidity
File: src/blast/libraries/BlastPoints.sol

6: library BlastPoints {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L6)

```solidity
File: src/blast/libraries/BlastYields.sol

7: library BlastYields {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L7)

```solidity
File: src/mimswap/MagicLP.sol

25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L25)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

13: contract FeeRateModel is Owned {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L13)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

7: contract FeeRateModelImpl {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L7)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

17: library DecimalMath {
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L17)

```solidity
File: src/mimswap/libraries/Math.sol

16: library Math {
```
[16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L16)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

20: library PMMPricing {
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L20)

```solidity
File: src/mimswap/periphery/Factory.sol

11: contract Factory is Owned {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L11)

```solidity
File: src/mimswap/periphery/Router.sol

12: contract Router {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L12)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

9: contract MagicLpAggregator is IAggregator {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L9)

```solidity
File: src/staking/LockingMultiRewards.sol

14: contract LockingMultiRewards is OperatableV2, Pausable {
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L14)
</details>

### [N-85] `public` functions not called by the contract should be declared `external` instead

Contracts are allowed to override their parents' functions and change the visibility from `external` to `public`.
If a `public` function is not called internally within the contract, it should be declared as `external` to save gas.

<details>
<summary><i>11 issue instances in 3 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

154: function name() public view override returns (string memory) {
227: function getBaseInput() public view returns (uint256 input) {
231: function getQuoteInput() public view returns (uint256 input) {
469: function setParameters(
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
[154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L154) | [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L227) | [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L231) | [469](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L469)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

57: function setImplementation(address implementation_) public onlyOwner {
```
[57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)

```solidity
File: src/staking/LockingMultiRewards.sol

150: function stake(uint256 amount, bool lock_) public whenNotPaused {
155: function lock(uint256 amount) public whenNotPaused {
264: function remainingEpochTime() public view returns (uint256) {
287: function earned(address user, address rewardToken) public view returns (uint256) {
300: function addReward(address rewardToken) public onlyOwner {
361: function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
```
[150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L150) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L155) | [264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L264) | [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L287) | [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300) | [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361)
</details>

### [N-86] Large multiples of ten should use scientific notation

Large multiples of ten should use scientific notation (e.g., 1e4) instead of decimal literals (e.g., 10000)
for better code readability.

<details>
<summary><i>3 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit `30_000` should be written as `3e4`
117: staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
```
[117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit `1000` should be written as `1e3`
594: if (amount <= 1000) {
```
[594](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L594)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit `10_000` should be written as `1e4`
78: uint256 private constant BIPS = 10_000;
```
[78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L78)
</details>

### [N-87] Complex casting

Complex casting in Solidity contracts can introduce both readability issues and potential for overflows. 
Whenever multiple casts are found, consider whether the complexity is necessary.
If so, it is strongly recommended to add inline comments to explain why these casts are needed and to assure that no overflows are introduced.

<details>
<summary><i>2 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

438: _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
439: _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
```
[438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439)
</details>

### [N-88] Unused Event Declarations

Events that aren't emitted in the contract add unnecessary complexity to the codebase. 
Removing these unused events can streamline the contract, enhancing its readability and maintainability.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit `LogYieldClaimed` event declared but never emitted
13: event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L13)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit `LogRewardsDurationUpdated` event declared but never emitted
26: event LogRewardsDurationUpdated(address token, uint256 newDuration);
```
[26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L26)
</details>

### [N-89] Equal `block.timestamp` Cases Not Handled

Solidity code that checks if `block.timestamp` is greater than a certain variable but fails to handle the case when `block.timestamp` is equal to the variable may lead to unintended behaviors and potential vulnerabilities.

To ensure correct and secure function execution, it's recommended to include checks for cases where `block.timestamp` equals the compared variable.

<details>
<summary><i>4 issue instances in 3 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

421: if (deadline < block.timestamp) {
```
[421](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L421)

```solidity
File: src/mimswap/periphery/Router.sol

48: if (block.timestamp > deadline) {
```
[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L48)

```solidity
File: src/staking/LockingMultiRewards.sol

379: if (block.timestamp < reward.periodFinish) {
422: if (locks[index].unlockTime > block.timestamp) {
```
[379](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L379) | [422](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L422)
</details>

### [N-90] `else`-block not required

In Solidity, if an `if` block contains a `return` statement, subsequent `else` blocks become unnecessary.
This is because the `return` statement halts the execution of the function at that point, making any `else` conditions redundant.
Therefore, omitting `else` after such `if` blocks can lead to cleaner and more readable code without any change in the functionality.

<details>
<summary><i>4 issue instances in 3 files:</i></summary>

```solidity
File: src/mimswap/libraries/DecimalMath.sol

48: if (e == 0) {
            return 10 ** 18;
        } else if (e == 1) {
            return target;
        } else {
```
[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L48)

```solidity
File: src/mimswap/libraries/Math.sol

22: if (remainder > 0) {
            return quotient + 1;
        } else {
            return quotient;
        }
200: if (V2 > V1) {
            return 0;
        } else {
            return V1 - V2;
        }
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L22) | [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L200)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

204: if (state.R == RState.BELOW_ONE) {
            uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);
            R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);
            return DecimalMath.divFloor(state.i, R);
        } else {
            uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
            R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);
            return DecimalMath.mulFloor(state.i, R);
        }
```
[204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L204)
</details>

### [N-91] Polymorphic functions make security audits more time-consuming and error-prone

While function overriding allows for functions with the same name to coexist, it's advisable to avoid this practice for the sake of readability and maintainability. 

Having multiple functions with the same name, even with different parameters or in inherited contracts, can cause confusion and increase the chance of errors during development, testing, and debugging.
Using distinct and descriptive function names not only clarifies the purpose and behavior of each function but also helps prevent unintended function calls or incorrect overriding.

<details>
<summary><i>4 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/libraries/BlastYields.sol

38: function claimMaxGasYields(address recipient) internal returns (uint256) {
42: function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {
51: function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
55: function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L38) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L42) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L51) | [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L55)
</details>

### [N-92] Style guide: Function ordering does not follow the Solidity style guide

Ordering helps readers identify which functions they can call and to find the constructor and fallback definitions easier.
But there are contracts in the project that do not comply with this.
Functions should be grouped according to their visibility and ordered:
- constructor 
- receive function (if exists)
- fallback function (if exists)
- external
- public
- internal
- private.

<details>
<summary><i>30 issue instances in 8 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

/// @audit `internal` function `_onBeforeDeposit()` declared before `external` function `claimGasYields()`
35: function _onBeforeDeposit(
        IERC20 token,
        address /*from*/,
        address /*to*/,
        uint256 /*amount*/,
        uint256 /*share*/
    ) internal view override {
51: function claimGasYields() external onlyOperators returns (uint256) {
```
[35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L35) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L51)

```solidity
File: src/blast/BlastGovernor.sol

/// @audit `receive` declared before `constructor`
12: receive() external payable {}
14: constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L12) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L14)

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit `receive` declared before `constructor`
79: receive() external payable override {
83: constructor(BlastTokenRegistry registry_, address feeTo_) {
```
[79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L79) | [83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L83)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit `public` function `getPMMState()` declared before `external` function `getPMMStateForCall()`
192: function getPMMState() public view returns (PMMPricing.PMMState memory state) {
203: function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
/// @audit `public` function `getMidPrice()` declared before `external` function `getReserves()`
214: function getMidPrice() public view returns (uint256 midPrice) {
218: function getReserves() external view returns (uint256 baseReserve, uint256 quoteReserve) {
/// @audit `public` function `getQuoteInput()` declared before `external` function `version()`
231: function getQuoteInput() public view returns (uint256 input) {
235: function version() external pure virtual returns (string memory) {
/// @audit `public` function `setParameters()` declared before `external` function `ratioSync()`
469: function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner {
503: function ratioSync() external nonReentrant onlyImplementationOwner {
```
[192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L192) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L203) | [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L214) | [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L218) | [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L231) | [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L235) | [469](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L469) | [503](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L503)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit `public` function `predictDeterministicAddress()` declared before `external` function `create()`
64: function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address) {
80: function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
```
[64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L64) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L80)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit `receive` declared before `constructor`
35: receive() external payable {}
37: constructor(IWETH weth_, IFactory factory_) {
```
[35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L35) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L37)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

/// @audit `internal` function `_getReserves()` declared before `public` function `latestAnswer()`
32: function _getReserves() internal view virtual returns (uint256, uint256) {
36: function latestAnswer() public view override returns (int256) {
/// @audit `public` function `latestAnswer()` declared before `external` function `latestRoundData()`
36: function latestAnswer() public view override returns (int256) {
47: function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```
[32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L32) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L36) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L36) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L47)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit `public` function `getRewards()` declared before `external` function `rewardData()`
190: function getRewards() public virtual {
199: function rewardData(address token) external view returns (Reward memory) {
/// @audit `internal` function `_earned()` declared before `public` function `addReward()`
291: function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {
300: function addReward(address rewardToken) public onlyOwner {
/// @audit `public` function `addReward()` declared before `external` function `setMinLockAmount()`
300: function addReward(address rewardToken) public onlyOwner {
316: function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
/// @audit `public` function `notifyRewardAmount()` declared before `external` function `processExpiredLocks()`
361: function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
397: function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
```
[190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L190) | [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199) | [291](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L291) | [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300) | [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300) | [316](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L316) | [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361) | [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397)
</details>

### [N-93] Avoid Using Pragma Without Upper Bound

Using `>` or `>=` with the pragma directive without specifying an upper bound can lead to incompatibilities with future versions of Solidity.
These future versions might introduce breaking changes that could affect your code.

While you might have a specific Solidity version set in your configuration file, others who include your source files might not, leading to potential issues.
Therefore, it is safer to specify both a lower and an upper bound for the Solidity version in the pragma directive.

<details>
<summary><i>20 issue instances in 20 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2)

```solidity
File: src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L3)

```solidity
File: src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L2)

```solidity
File: src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L3)

```solidity
File: src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L2)

```solidity
File: src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L2)

```solidity
File: src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L2)

```solidity
File: src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L2)

```solidity
File: src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L2)

```solidity
File: src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L2)

```solidity
File: src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L7)

```solidity
File: src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L8)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L8)

```solidity
File: src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L2)

```solidity
File: src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L2)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L2)

```solidity
File: src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L2)
</details>

### [N-94] Style guide: Lines are too long

It is generally recommended that lines in the source code should not exceed 80-120 characters.
Multiline output parameters and return statements should follow the same style recommended for wrapping long lines found in the Maximum Line Length section.

<details>
<summary><i>54 issue instances in 11 files:</i></summary>

```solidity
File: src/blast/BlastGovernor.sol

53: function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```
[53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)

```solidity
File: src/blast/BlastMagicLP.sol

53: function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {
```
[53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L53)

```solidity
File: src/blast/BlastOnboarding.sol

101: function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
123: function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
```
[101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101) | [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123)

```solidity
File: src/blast/BlastOnboardingBoot.sol

86: function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
96: function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
```
[86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96)

```solidity
File: src/mimswap/MagicLP.sol

32: event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);
36: event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);
156: return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));
170: ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {
183: ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {
204: function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
290: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
310: (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) = querySellQuote(
325: emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);
332: (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) = querySellBase(
347: emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
360: function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
381: shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;
402: _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();
403: _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
439: _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
```
[32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L32) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L36) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L156) | [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L170) | [183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L183) | [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204) | [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290) | [310](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L310) | [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L325) | [332](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L332) | [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L347) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360) | [381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L381) | [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402) | [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

34: function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
[34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34)

```solidity
File: src/mimswap/libraries/Math.sol

51: function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {
79: function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
131: function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
184: uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
```
[51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L79) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131) | [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

39: function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {
55: // [Important corner case!] may enter this branch when some precision problem happens. And consequently contribute to negative spare quote amount
65: receiveQuoteAmount = backToOneReceiveQuote + _ROneSellBaseToken(state, payBaseAmount - backToOnePayBase);
76: function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {
96: receiveBaseAmount = backToOneReceiveBase + _ROneSellQuoteToken(state, payQuoteAmount - backToOnePayQuote);
129: return Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);
144: return Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K);
185: return Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L39) | [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L55) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L65) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L76) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L96) | [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L129) | [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L144) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L185)

```solidity
File: src/mimswap/periphery/Factory.sol

81: function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
86: IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
```
[81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L86)

```solidity
File: src/mimswap/periphery/Router.sol

88: clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);
101: shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
138: shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;
169: ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
199: ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
251: function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
523: uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
541: function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {
```
[88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L88) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L101) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L138) | [169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L169) | [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L199) | [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L251) | [523](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L523) | [541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L541)

```solidity
File: src/staking/LockingMultiRewards.sol

11: /// @author Based from Curve Finance's MultiRewards contract https://github.com/curvefi/multi-rewards/blob/master/contracts/MultiRewards.sol
12: /// @author Based from Ellipsis Finance's EpsStaker https://github.com/ellipsis-finance/ellipsis/blob/master/contracts/EpsStaker.sol
13: /// @author Based from Convex Finance's CvxLockerV2 https://github.com/convex-eth/platform/blob/main/contracts/contracts/CvxLockerV2.sol
109: /// @param _lockingBoostMultiplerInBips The multiplier for the locking boost. 30000 means if you stake 100, you get 300 locked
252: // |                             ^ lock starts (adjusted)                                    ^ unlock ends (nextUnlockTime)
277: function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
292: function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {
322: /// @notice This function can recover any token except for the staking token beyond the balance necessary for rewards.
533: _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L11) | [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L12) | [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L13) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L109) | [252](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L252) | [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277) | [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L292) | [322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L322) | [533](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L533)
</details>

### [N-95] Style guide: Extraneous whitespace

See the [whitespace](https://docs.soliditylang.org/en/v0.8.24/style-guide.html#whitespace-in-expressions) section of the Solidity Style Guide

<details>
<summary><i>15 issue instances in 3 files:</i></summary>

```solidity
File: src/mimswap/libraries/Math.sol

/// @audit `Do not include a whitespace in the receive and fallback functions`
118: if deltaBSig=true, then Q2>Q1, user sell Q and receive B
/// @audit `Do not include a whitespace in the receive and fallback functions`
119: if deltaBSig=false, then Q2<Q1, user sell B and receive Q
```
[118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L118) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L119)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit `Immediately inside parenthesis, brackets or braces, with the exception of single line function declarations.`
70: (shares, , ) = IMagicLP(clone).buyShares(to);
/// @audit `Immediately inside parenthesis, brackets or braces, with the exception of single line function declarations.`
93: (shares, , ) = IMagicLP(clone).buyShares(to);
/// @audit `Immediately inside parenthesis, brackets or braces, with the exception of single line function declarations.`
500: (shares, , ) = IMagicLP(lp).buyShares(to);
/// @audit `Immediately inside parenthesis, brackets or braces, with the exception of single line function declarations.`
544: for (uint256 i = 0; i < iterations; ) {
/// @audit `Immediately before a comma`
70: (shares, , ) = IMagicLP(clone).buyShares(to);
/// @audit `Immediately before a comma`
93: (shares, , ) = IMagicLP(clone).buyShares(to);
/// @audit `Immediately before a comma`
500: (shares, , ) = IMagicLP(lp).buyShares(to);
```
[70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L70) | [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L93) | [500](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L500) | [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L70) | [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L93) | [500](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L500)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit `Immediately inside parenthesis, brackets or braces, with the exception of single line function declarations.`
405: for (uint256 i; i < users.length; ) {
/// @audit `Immediately inside parenthesis, brackets or braces, with the exception of single line function declarations.`
547: for (uint256 i; i < rewardTokens.length; ) {
/// @audit `Immediately inside parenthesis, brackets or braces, with the exception of single line function declarations.`
561: for (uint256 i; i < rewardTokens.length; ) {
/// @audit `Immediately inside parenthesis, brackets or braces, with the exception of single line function declarations.`
575: for (uint256 i; i < rewardTokens.length; ) {
/// @audit `Immediately inside parenthesis, brackets or braces, with the exception of single line function declarations.`
580: for (uint256 j; j < users.length; ) {
/// @audit `Immediately inside parenthesis, brackets or braces, with the exception of single line function declarations.`
614: for (uint256 i; i < rewardTokens.length; ) {
```
[405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405) | [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547) | [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561) | [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575) | [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580) | [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614)
</details>

### [N-96] Misplaced or Missing SPDX identifier

The SPDX identifier was not found on the very first line of the file.
Please ensure the SPDX identifier exists and placed correctly.
For more information, please refer to the [SPDX specification](https://docs.soliditylang.org/en/latest/layout-of-source-files.html#spdx-license-identifier).

<details>
<summary><i>5 issue instances in 5 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

1: /*
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L1)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

1: /*
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L1)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

1: /*
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L1)

```solidity
File: src/mimswap/libraries/Math.sol

1: /*
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L1)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

1: /*
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L1)
</details>

### [N-97] Contract/Libraries Names Do Not Match Their Filenames

According to the Solidity Style Guide, contract names should match their filenames. 
Mismatching contract names and filenames can lead to confusion and make the code harder to maintain and review.

<details>
<summary><i>3 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

11: contract BlastOnboardingData is Owned, Pausable {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L11)

```solidity
File: src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23)

```solidity
File: src/blast/BlastWrappers.sol

18: contract BlastMIMSwapRouter is Router {
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L18)
</details>

### [N-98] Avoid the use of sensitive terms

Inclusive language plays a critical role in fostering an environment where everyone belongs.
Please use alternative terms as suggested below:
master -> source
slave -> replica
blacklist -> blocklist
whitelist -> allowlist

<details>
<summary><i>4 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastWrappers.sol

56: _setupBlacklist();
64: _setupBlacklist();
70: function _setupBlacklist() private {
71: blacklistedCallees[address(BlastYields.BLAST_YIELD_PRECOMPILE)] = true;
```
[56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L56) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L64) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L70) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L71)
</details>

### [N-99] Unused import

The contract contains import statements for libraries or other contracts that are not utilized within the code.
Excessive or unused imports can clutter the codebase, leading to inefficiency and potential confusion.
Consider removing any imports that are not essential to the contract's functionality.

<details>
<summary><i>8 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

/// @audit imported `IWETH` not used)
11: import {IWETH} from "interfaces/IWETH.sol";
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L11)

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit imported `BlastOnboarding` not used)
4: import {BlastOnboarding} from "/blast/BlastOnboarding.sol";
/// @audit imported `IFeeRateModel` not used)
7: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";
/// @audit imported `DecimalMath` not used)
10: import {DecimalMath} from "/mimswap/libraries/DecimalMath.sol";
```
[4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L4) | [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L7) | [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L10)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit imported `IWETH` not used)
21: import {IWETH} from "interfaces/IWETH.sol";
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L21)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

/// @audit imported `IFeeRateImpl` not used)
4: import {IFeeRateImpl} from "../interfaces/IFeeRateModel.sol";
```
[4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L4)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit imported `MagicLP` not used)
8: import {MagicLP} from "/mimswap/MagicLP.sol";
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L8)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

/// @audit imported `FixedPointMathLib` not used)
4: import {FixedPointMathLib} from "solady/utils/FixedPointMathLib.sol";
```
[4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L4)
</details>

### [N-100] `if`-statement can be converted to a ternary

The ternary operator provides a shorthand way to write if / else statements.
It can improve readability and reduce the number of lines of code.
Traditional `if / else` statements, particularly those spanning only a one lines, could potentially be refactored using the ternary operator.

<details>
<summary><i>5 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/libraries/Math.sol

96: } else if ((ki * delta) / ki == delta) {
            _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);
        } else {
            _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);
        }
155: } else if ((idelta * V1) / idelta == V1) {
                temp = (idelta * V1) / (V0 * V0);
            } else {
                temp = (((delta * V1) / V0) * i) / V0;
            }
```
[96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L96) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L155)

```solidity
File: src/mimswap/periphery/Router.sol

347: if (directions & 1 == 0) {
            inToken = IMagicLP(firstLp)._BASE_TOKEN_();
        } else {
            inToken = IMagicLP(firstLp)._QUOTE_TOKEN_();
        }
378: if ((directions >> lastLpIndex) & 1 == 0) {
            outToken = IMagicLP(lastLp)._QUOTE_TOKEN_();
        } else {
            outToken = IMagicLP(lastLp)._BASE_TOKEN_();
        }
559: if ((directions & 1 == 0)) {
            amountOut = IMagicLP(path[iterations]).sellBase(to);
        } else {
            amountOut = IMagicLP(path[iterations]).sellQuote(to);
        }
```
[347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L347) | [378](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L378) | [559](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L559)
</details>

### [N-101] Consider using named mappings

As of Solidity version 0.8.18, it is possible to use named mappings to clarify the purpose of each mapping in the code. 
It is recommended to use this feature for better code readability and maintainability.

More information: [Solidity 0.8.18 Release Announcement](https://blog.soliditylang.org/2023/02/01/solidity-0.8.18-release-announcement/)

<details>
<summary><i>3 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

21: mapping(address => bool) public enabledTokens;
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21)

```solidity
File: src/blast/BlastMagicLP.sol

21: mapping(address => bool) public operators;
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L21)

```solidity
File: src/blast/BlastTokenRegistry.sol

10: mapping(address => bool) public nativeYieldTokens;
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10)
</details>

### [N-102] Use of `override` is unnecessary

In Solidity version 0.8.8 and later, the use of the `override` keyword becomes superfluous when a function is overriding solely from an interface and the function isn't present in multiple base contracts.
Previously, the `override` keyword was required as an explicit indication to the compiler. However, this is no longer the case, and the extraneous use of the keyword can make the code less clean and more verbose.

Solidity documentation on [Function Overriding](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding).

<details>
<summary><i>13 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

35: function _onBeforeDeposit(
        IERC20 token,
        address /*from*/,
        address /*to*/,
        uint256 /*amount*/,
        uint256 /*share*/
    ) internal view override {
98: function _configure() internal override {
102: function isOwner(address _account) internal view override returns (bool) {
```
[35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L35) | [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L98) | [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L102)

```solidity
File: src/blast/BlastMagicLP.sol

38: function version() external pure override returns (string memory) {
97: function _afterInitialized() internal override {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L38) | [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L97)

```solidity
File: src/blast/BlastOnboarding.sol

225: function _implementation() internal view override returns (address) {
```
[225](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L225)

```solidity
File: src/blast/BlastWrappers.sol

58: function init(bytes calldata data) public payable override {
```
[58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L58)

```solidity
File: src/mimswap/MagicLP.sol

154: function name() public view override returns (string memory) {
158: function symbol() public pure override returns (string memory) {
162: function decimals() public view override returns (uint8) {
592: function _mint(address to, uint256 amount) internal override {
```
[154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L154) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L158) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L162) | [592](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L592)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

28: function decimals() external pure override returns (uint8) {
36: function latestAnswer() public view override returns (int256) {
```
[28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L28) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L36)
</details>

### [N-103] Setters should prevent re-setting of the same value

Setter functions should include a condition to check if the new value being assigned is different from the current value. This practice prevents redundant state changes and the emission of unnecessary events, ensuring that changes only occur when actual updates to the values are made.

This not only helps to maintain the integrity of the contract's state but also keeps the event logs cleaner and more meaningful by avoiding the recording of identical consecutive values. Such an approach can improve the clarity and efficiency of debugging and data tracking processes.

<details>
<summary><i>19 issue instances in 10 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

/// @audit Missing `feeTo_` check before state change
76: feeTo = feeTo_;
/// @audit Missing `enabled` check before state change
82: enabledTokens[token] = enabled;
```
[76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L76) | [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L82)

```solidity
File: src/blast/BlastGovernor.sol

/// @audit Missing `_feeTo` check before state change
44: feeTo = _feeTo;
```
[44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L44)

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit Missing `feeTo_` check before state change
84: feeTo = feeTo_;
/// @audit Missing `status` check before state change
90: operators[operator] = status;
```
[84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L84) | [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L90)

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit Missing `feeTo_` check before state change
151: feeTo = feeTo_;
/// @audit Missing `supported` check before state change
176: supportedTokens[token] = supported;
/// @audit Missing `cap` check before state change
186: caps[token] = cap;
/// @audit Missing `bootstrapper_` check before state change
191: bootstrapper = bootstrapper_;
```
[151](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L151) | [176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L176) | [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L186) | [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L191)

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit Missing `_staking` check before state change
141: staking = _staking;
/// @audit Missing `_ready` check before state change
147: ready = _ready;
```
[141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L141) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L147)

```solidity
File: src/blast/BlastTokenRegistry.sol

/// @audit Missing `enabled` check before state change
18: nativeYieldTokens[token] = enabled;
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L18)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit Missing `baseReserve` check before state change
561: _BASE_RESERVE_ = baseReserve.toUint112();
/// @audit Missing `quoteReserve` check before state change
562: _QUOTE_RESERVE_ = quoteReserve.toUint112();
```
[561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L561) | [562](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L562)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit Missing `maintainer_` check before state change
50: maintainer = maintainer_;
/// @audit Missing `implementation_` check before state change
58: implementation = implementation_;
```
[50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L50) | [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L58)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit Missing `implementation_` check before state change
100: implementation = implementation_;
/// @audit Missing `maintainerFeeRateModel_` check before state change
109: maintainerFeeRateModel = maintainerFeeRateModel_;
```
[100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L100) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L109)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit Missing `_minLockAmount` check before state change
319: minLockAmount = _minLockAmount;
```
[319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L319)
</details>

### [N-104] NatSpec: Contract declarations should have `@title` tags

NatSpec comments offer an intuitive way to understand the core purpose of a smart contract. 
Especially, the `@title` tag serves as a brief descriptor of the contract's function or intent.
In this Solidity file, the `@title` directive seems to be overlooked.
Incorporating the `@title` tag gives readers a concise overview, thus enhancing clarity.
[Refer to NatSpec Documentation](https://docs.soliditylang.org/en/develop/natspec-format.html)

<details>
<summary><i>21 issue instances in 17 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

6: contract BlastDapp {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L6)

```solidity
File: src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L13)

```solidity
File: src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L7)

```solidity
File: src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L10)

```solidity
File: src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData is Owned, Pausable {
64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L12) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L64)

```solidity
File: src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L34)

```solidity
File: src/blast/BlastTokenRegistry.sol

6: contract BlastTokenRegistry is Owned {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L6)

```solidity
File: src/blast/BlastWrappers.sol

19: contract BlastMIMSwapRouter is Router {
28: contract BlastMIMSwapFactory is Factory {
42: contract BlastCauldronV4 is CauldronV4 {
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L19) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L28) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L42)

```solidity
File: src/blast/libraries/BlastPoints.sol

6: library BlastPoints {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L6)

```solidity
File: src/blast/libraries/BlastYields.sol

7: library BlastYields {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L7)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

13: contract FeeRateModel is Owned {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L13)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

7: contract FeeRateModelImpl {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L7)

```solidity
File: src/mimswap/libraries/Math.sol

16: library Math {
```
[16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L16)

```solidity
File: src/mimswap/periphery/Factory.sol

11: contract Factory is Owned {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L11)

```solidity
File: src/mimswap/periphery/Router.sol

12: contract Router {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L12)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

9: contract MagicLpAggregator is IAggregator {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L9)

```solidity
File: src/staking/LockingMultiRewards.sol

14: contract LockingMultiRewards is OperatableV2, Pausable {
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L14)
</details>

### [N-105] Use Unchecked for Divisions on Constant or Immutable Values

Unsigned divisions on constant or immutable values do not result in overflow.
Therefore, these operations can be marked as unchecked, optimizing gas usage without compromising safety.

For instance, if `a` is an unsigned integer and `b` is a constant or immutable, a / b can be safely rewritten as: unchecked { a / b }

<details>
<summary><i>8 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

7: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";
8: import {IFactory} from "/mimswap/interfaces/IFactory.sol";
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L7) | [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L8)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

24: return (target * d) / ONE;
54: p = (p * p) / ONE;
56: p = (p * target) / ONE;
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L24) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L54) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L56)

```solidity
File: src/staking/LockingMultiRewards.sol

236: return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);
241: return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);
258: return (block.timestamp / rewardsDuration) * rewardsDuration;
```
[236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L236) | [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L241) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L258)
</details>

### [N-106] Explicit Visibility Recommended in Variable/Function Definitions

In Solidity, variable/function visibility is crucial for controlling access and protecting against unwanted modifications. 
While Solidity functions default to `internal` visibility, it is best practice to explicitly state the visibility for better code readability and avoiding confusion.

The missing visibility could lead to a false sense of security in contract design and potential vulnerabilities.

<details>
<summary><i>8 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

13: address constant USDB = 0x4300000000000000000000000000000000000003;
14: address constant MIM = 0x76DA31D7C9CbEAE102aff34D3398bC450c8374c1;
15: uint256 constant FEE_RATE = 0.0005 ether; // 0.05%
16: uint256 constant K = 0.00025 ether; // 0.00025, 1.25% price fluctuation, similar to A2000 in curve
17: uint256 constant I = 0.998 ether; // 1 MIM = 0.998 USDB
18: uint256 constant USDB_TO_MIN = 1.002 ether; // 1 USDB = 1.002 MIM
19: uint256 constant MIM_TO_MIN = I;
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L14) | [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L15) | [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L16) | [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L17) | [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L18) | [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L19)

```solidity
File: src/blast/libraries/BlastYields.sol

14: IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L14)
</details>

### [N-107] Contracts should have full test coverage

It's recommended to have full test coverage for all contracts.
While 100% code coverage does not guarantee absence of bugs, it can catch simple bugs and reduce regressions during code modifications.
Moreover, to achieve full coverage, authors often have to refactor their code into more modular components, each testable separately.
This leads to lower interdependencies, and results in code that is easier to understand and audit.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: app/2024-03-abracadabra-money

1: All files
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/app/2024-03-abracadabra-money#L1)
</details>

### [N-108] Large or complicated code bases should implement invariant tests

Large or complex code bases should include invariant fuzzing tests, such as those provided by Echidna.
These tests require the identification of invariants that should not be violated under any circumstances, with the fuzzer testing various inputs and function calls to ensure these invariants always hold.
This is especially important for code with a lot of inline-assembly, complicated math, or complex interactions between contracts. Despite having 100% code coverage, bugs can still occur due to the order of operations a user performs.
Extensive and well-written invariant tests can significantly reduce this testing gap.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: app/2024-03-abracadabra-money

1: All files
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/app/2024-03-abracadabra-money#L1)
</details>

### [N-109] Implement Formal Verification Proofs to Improve Security

Formal verification offers a mathematical proof confirming that your code operates as intended and is devoid of edge cases 
that may lead to unintended behavior. By leveraging this rigorous audit technique, you not only enhance the robustness 
of your code but also strengthen the trust of stakeholders in the safety of your contract.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: app/2024-03-abracadabra-money

1: All files
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/app/2024-03-abracadabra-money#L1)
</details>

