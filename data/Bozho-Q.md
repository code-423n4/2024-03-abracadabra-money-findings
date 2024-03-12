### Low

|Number|Issue|Instances|
|-|:-|:-:|
| [L&#x2011;1](#L1-avoid-using-txorigin) | Avoid using `tx.origin` | 5 |
| [L&#x2011;2](#L2-consider-bounding-input-array-length) | Consider bounding input array length | 1 |
| [L&#x2011;3](#L3-consider-implementing-two-step-procedure-for-updating-protocol-addresses) | Consider implementing two-step procedure for updating protocol addresses | 8 |
| [L&#x2011;4](#L4-constructor/initialize-function-lacks-parameter-validation) | `constructor`/`initialize` function lacks parameter validation | 6 |
| [L&#x2011;5](#L5-contracts-use-infinite-approvals-with-no-means-to-revoke) | Contracts use infinite approvals with no means to revoke | 2 |
| [L&#x2011;6](#L6-critical-functions-should-be-controlled-by-time-locks) | Critical functions should be controlled by time locks | 12 |
| [L&#x2011;7](#L7-decimals-is-not-a-part-of-the-erc-20-standard) | `decimals()` is not a part of the ERC-20 standard | 9 |
| [L&#x2011;8](#L8-division-by-zero-not-prevented) | Division by zero not prevented | 9 |
| [L&#x2011;9](#L9-do-not-use-deprecated-library-functions) | Do not use deprecated library functions | 3 |
| [L&#x2011;10](#L10-external-calls-in-an-un-bounded-for-loop-may-result-in-a-dos) | External calls in an un-bounded `for`-loop may result in a DOS | 2 |
| [L&#x2011;11](#L11-functions-calling-contracts/addresses-with-transfer-hooks-are-missing-reentrancy-guards) | Functions calling contracts/addresses with transfer hooks are missing reentrancy guards | 31 |
| [L&#x2011;12](#L12-latestanswer-is-deprecated) | `latestAnswer()` is deprecated | 4 |
| [L&#x2011;13](#L13-low-level-calls-to-custom-addresses) | Low level calls to custom `address`es | 1 |
| [L&#x2011;14](#L14-missing-checks-for-address0-when-assigning-values-to-address-state-variables) | Missing checks for `address(0)` when assigning values to address state variables | 2 |
| [L&#x2011;15](#L15-missing-contract-existence-checks-before-low-level-calls) | Missing contract-existence checks before low-level calls | 1 |
| [L&#x2011;16](#L16-missing-zero-address-check-in-functions-with-address-parameters) | Missing zero address check in functions with address parameters | 97 |
| [L&#x2011;17](#L17-multiplication-on-the-result-of-a-division) | Multiplication on the result of a division | 4 |
| [L&#x2011;18](#L18-owner-or-single-user-with-a-role-can-renounce-while-system-is-paused) | Owner or single user with a role can renounce while system is paused | 2 |
| [L&#x2011;19](#L19-safetransferlib-does-not-ensure-that-the-token-contract-exists) | `SafeTransferLib` does not ensure that the token contract exists | 5 |
| [L&#x2011;20](#L20-setters-should-prevent-re-setting-of-the-same-value) | Setters should prevent re-setting of the same value | 5 |
| [L&#x2011;21](#L21-some-tokens-may-revert-when-zero-value-transfers-are-made) | Some tokens may revert when zero value transfers are made | 26 |
| [L&#x2011;22](#L22-state-variables-not-capped-at-reasonable-values) | State variables not capped at reasonable values | 1 |
| [L&#x2011;23](#L23-symbol-is-not-a-part-of-the-erc-20-standard) | `symbol()` is not a part of the ERC-20 standard | 2 |
| [L&#x2011;24](#L24-transferownership-should-be-two-step) | TransferOwnership should be two step | 1 |
| [L&#x2011;25](#L25-unchecked-blocks-with-additions/multiplications-may-overflow) | `unchecked` blocks with additions/multiplications may overflow | 1 |
| [L&#x2011;26](#L26-unused/empty-receive/fallback-function) | Unused/empty `receive()/fallback()` function | 2 |
| [L&#x2011;27](#L27-using->/>=-without-specifying-an-upper-bound-is-unsafe) | Using `>`/`>=` without specifying an upper bound is unsafe | 20 |


### NonCritical

|Number|Issue|Instances|
|-|:-|:-:|
| [NC&#x2011;1](#NC1-2**<n>---1-should-be-re-written-as-typeuint<n>max) | `2**<n> - 1` should be re-written as `type(uint<n>).max` | 2 |
| [NC&#x2011;2](#NC2-adding-a-return-statement-when-the-function-defines-a-named-return-variable-is-redundant) | Adding a `return` statement when the function defines a named return variable, is redundant | 1 |
| [NC&#x2011;3](#NC3-address-shouldnt-be-hard-coded) | `address` shouldn't be hard-coded | 5 |
| [NC&#x2011;4](#NC4-avoid-external-calls-in-modifiers) | Avoid external calls in modifiers | 3 |
| [NC&#x2011;5](#NC5-avoid-mutating-function/modifier-parameters) | Avoid mutating `function`/`modifier` parameters | 8 |
| [NC&#x2011;6](#NC6-complicated-functions-should-have-explicit-comments) | Complicated functions should have explicit comments | 1 |
| [NC&#x2011;7](#NC7-consider-disallowing-transfers-to-addressthis) | Consider disallowing transfers to `address(this)` | 1 |
| [NC&#x2011;8](#NC8-consider-making-contracts-upgradeable) | Consider making contracts `Upgradeable` | 19 |
| [NC&#x2011;9](#NC9-consider-providing-a-ranged-getter-for-array-state-variables) | Consider providing a ranged getter for array state variables | 2 |
| [NC&#x2011;10](#NC10-consider-using-delete-rather-than-assigning-zero-to-clear-values) | Consider using `delete` rather than assigning zero to clear values | 2 |
| [NC&#x2011;11](#NC11-consider-using-named-function-arguments) | Consider using named function arguments | 14 |
| [NC&#x2011;12](#NC12-consider-using-named-mappings) | Consider using named mappings | 3 |
| [NC&#x2011;13](#NC13-constants-in-comparisons-should-appear-on-the-left-side) | Constants in comparisons should appear on the left side | 42 |
| [NC&#x2011;14](#NC14-constants-should-be-defined-rather-than-using-magic-numbers) | `constant`s should be defined rather than using magic numbers | 22 |
| [NC&#x2011;15](#NC15-constants/immutables-redefined-elsewhere) | `constant`s/`immutable`s redefined elsewhere | 31 |
| [NC&#x2011;16](#NC16-constructor-should-emit-an-event) | `constructor` should emit an event | 15 |
| [NC&#x2011;17](#NC17-contracts-containing-only-utility-functions-should-be-made-into-libraries) | Contracts containing only utility functions should be made into libraries | 1 |
| [NC&#x2011;18](#NC18-contracts-should-each-be-defined-in-separate-files) | Contracts should each be defined in separate files | 7 |
| [NC&#x2011;19](#NC19-contracts-should-have-all-public/external-functions-exposed-by-interfaces) | Contracts should have all `public`/`external` functions exposed by `interface`s | 14 |
| [NC&#x2011;20](#NC20-contracts/libraries/interfaces-should-each-be-defined-in-separate-files) | Contracts/libraries/interfaces should each be defined in separate files | 7 |
| [NC&#x2011;21](#NC21-control-structures-do-not-follow-the-solidity-style-guide) | Control structures do not follow the Solidity Style Guide | 15 |
| [NC&#x2011;22](#NC22-do-not-use-underscore-at-the-end-of-variable-name) | Do not use underscore at the end of variable name | 75 |
| [NC&#x2011;23](#NC23-else-block-not-required) | `else`-block not required | 4 |
| [NC&#x2011;24](#NC24-empty-bytes-check-is-missing) | Empty bytes check is missing | 9 |
| [NC&#x2011;25](#NC25-enum-values-should-be-used-instead-of-constant-array-indexes) | Enum values should be used instead of constant array indexes | 3 |
| [NC&#x2011;26](#NC26-events-are-missing-sender-information) | Events are missing sender information | 26 |
| [NC&#x2011;27](#NC27-events-should-be-emitted-before-external-calls) | Events should be emitted before external calls | 38 |
| [NC&#x2011;28](#NC28-events-that-mark-critical-parameter-changes-should-contain-both-the-old-and-the-new-value) | Events that mark critical parameter changes should contain both the old and the new value | 11 |
| [NC&#x2011;29](#NC29-expressions-for-constant-values-should-use-immutable-rather-than-constant) | Expressions for `constant` values should use `immutable` rather than constant | 6 |
| [NC&#x2011;30](#NC30-extraneous-whitespace) | Extraneous whitespace | 3 |
| [NC&#x2011;31](#NC31-for-loops-in-public-or-external-functions-should-be-avoided-due-to-high-gas-costs-and-possible-dos) | For loops in `public` or `external` functions should be avoided due to high gas costs and possible DOS | 2 |
| [NC&#x2011;32](#NC32-function-ordering-in-the-contract-does-not-follow-the-solidity-style-guide) | Function ordering in the contract does not follow the Solidity style guide | 100 |
| [NC&#x2011;33](#NC33-functions-contain-the-same-code) | Functions contain the same code | 11 |
| [NC&#x2011;34](#NC34-functions-should-be-named-in-mixedcase-style) | Functions should be named in mixedCase style | 23 |
| [NC&#x2011;35](#NC35-high-cyclomatic-complexity) | High cyclomatic complexity | 15 |
| [NC&#x2011;36](#NC36-if-statement-can-be-converted-to-a-ternary) | `if`-statement can be converted to a ternary | 9 |
| [NC&#x2011;37](#NC37-imports-could-be-organized-more-systematically) | Imports could be organized more systematically | 7 |
| [NC&#x2011;38](#NC38-inconsistent-spacing-in-comments) | Inconsistent spacing in comments | 17 |
| [NC&#x2011;39](#NC39-large-multiples-of-ten-should-use-scientific-notation) | Large multiples of ten should use scientific notation | 3 |
| [NC&#x2011;40](#NC40-large-numeric-literals-should-use-underscores-for-readability) | Large numeric literals should use underscores for readability | 8 |
| [NC&#x2011;41](#NC41-layout-order-does-not-comply-with-best-practices) | Layout order does not comply with best practices | 61 |
| [NC&#x2011;42](#NC42-lines-are-too-long) | Lines are too long | 54 |
| [NC&#x2011;43](#NC43-long-functions-should-be-refactored-into-multiple-smaller-functions) | Long functions should be refactored into multiple, smaller, functions | 5 |
| [NC&#x2011;44](#NC44-make-use-of-soliditys-using-keyword) | Make use of Solidity's `using` keyword | 97 |
| [NC&#x2011;45](#NC45-misplaced-spdx-identifier) | Misplaced SPDX identifier | 5 |
| [NC&#x2011;46](#NC46-mixed-usage-of-int/uint-with-int256/uint256) | Mixed usage of `int/uint` with `int256/uint256` | 2 |
| [NC&#x2011;47](#NC47-multiple-mappings-with-same-keys-can-be-combined-into-a-single-struct-mapping-for-readability) | Multiple mappings with same keys can be combined into a single struct mapping for readability | 17 |
| [NC&#x2011;48](#NC48-named-imports-of-parent-contracts-are-missing) | Named imports of parent contracts are missing | 2 |
| [NC&#x2011;49](#NC49-names-of-structs-events-enums-and-errors-should-use-capwords-style) | Names of structs, events, enums and errors should use CapWords style | 2 |
| [NC&#x2011;50](#NC50-non-external/public-function-names-should-begin-with-an-underscore) | Non-`external`/`public` function names should begin with an underscore | 25 |
| [NC&#x2011;51](#NC51-not-using-the-latest-versions-of-project-dependencies) | Not using the latest versions of project dependencies | 1 |
| [NC&#x2011;52](#NC52-not-using-the-named-return-variables-anywhere-in-the-function-is-confusing) | Not using the named return variables anywhere in the function is confusing | 19 |
| [NC&#x2011;53](#NC53-outdated-solidity-version) | Outdated Solidity version | 20 |
| [NC&#x2011;54](#NC54-overly-complicated-arithmetic) | Overly complicated arithmetic | 3 |
| [NC&#x2011;55](#NC55-overridden-function-has-no-body) | Overridden function has no body | 1 |
| [NC&#x2011;56](#NC56-parameter-change-does-not-emit-event) | Parameter change does not emit event | 2 |
| [NC&#x2011;57](#NC57-polymorphic-functions-make-security-audits-more-time-consuming-and-error-prone) | Polymorphic functions make security audits more time-consuming and error-prone | 4 |
| [NC&#x2011;58](#NC58-prefer-skip-over-revert-model-in-iteration) | Prefer skip over revert model in iteration | 2 |
| [NC&#x2011;59](#NC59-public-functions-not-called-by-the-contract-should-be-declared-external-instead) | `public` functions not called by the contract should be declared `external` instead | 17 |
| [NC&#x2011;60](#NC60-public-functions-shouldnt-have-a-preceding-_-in-their-name) | Public functions shouldn't have a preceding `_` in their name | 1 |
| [NC&#x2011;61](#NC61-public-state-variables-shouldnt-have-a-preceding-_-in-their-name) | Public state variables shouldn't have a preceding `_` in their name | 13 |
| [NC&#x2011;62](#NC62-returning-a-struct-instead-of-a-bunch-of-variables-is-better) | Returning a struct instead of a bunch of variables is better | 11 |
| [NC&#x2011;63](#NC63-some-contracts-can-be-abstract) | Some contracts can be abstract | 1 |
| [NC&#x2011;64](#NC64-some-events-are-never-emitted) | Some events are never emitted | 3 |
| [NC&#x2011;65](#NC65-some-variables-have-a-implicit-default-visibility) | Some variables have a implicit default visibility | 1 |
| [NC&#x2011;66](#NC66-top-level-declarations-should-be-separated-by-at-least-two-lines) | Top-level declarations should be separated by at least two lines | 168 |
| [NC&#x2011;67](#NC67-typos) | Typos | 1 |
| [NC&#x2011;68](#NC68-unnecessary-cast) | Unnecessary cast | 29 |
| [NC&#x2011;69](#NC69-unnecessary-struct-attribute-prefix) | Unnecessary struct attribute prefix | 2 |
| [NC&#x2011;70](#NC70-unspecific-compiler-version-pragma) | Unspecific compiler version pragma | 20 |
| [NC&#x2011;71](#NC71-unused-error-definition) | Unused `error` definition | 6 |
| [NC&#x2011;72](#NC72-unused-event-definition) | Unused `event` definition | 3 |
| [NC&#x2011;73](#NC73-unused-modifier-definition) | Unused `modifier` definition | 2 |
| [NC&#x2011;74](#NC74-use-a-single-file-for-system-wide-constants) | Use a single file for system wide constants | 15 |
| [NC&#x2011;75](#NC75-use-a-struct-to-encapsulate-multiple-function-parameters) | Use a struct to encapsulate multiple function parameters | 25 |
| [NC&#x2011;76](#NC76-use-camelcase-for-contract-and-library-names) | Use CamelCase for contract and library names | 3 |
| [NC&#x2011;77](#NC77-use-delete-instead-of-assigning-values-to-false) | Use delete instead of assigning values to `false` | 1 |
| [NC&#x2011;78](#NC78-use-scientific-notation-eg-1e18-rather-than-exponentiation-eg-10**18) | Use scientific notation (e.g. `1e18`) rather than exponentiation (e.g. `10**18`) | 5 |
| [NC&#x2011;79](#NC79-use-upper_case-for-immutable) | Use UPPER_CASE for `immutable` | 16 |
| [NC&#x2011;80](#NC80-variable-names-that-consist-of-all-capital-letters-should-be-reserved-for-constant/immutable-variables) | Variable names that consist of all capital letters should be reserved for `constant`/`immutable` variables | 22 |
| [NC&#x2011;81](#NC81-variables-need-not-be-initialized-to-zero) | Variables need not be initialized to zero | 2 |
| [NC&#x2011;82](#NC82-variables-should-be-named-in-mixedcase-style) | Variables should be named in mixedCase style | 164 |

---
# FULL REPORT @ https://gist.github.com/notbozho/d220e0f58fe1756d458f277cbf12f0f5
---

---
### [L&#x2011;1] Avoid using `tx.origin`
`tx.origin` is a global variable in Solidity that returns the address of the account that sent the transaction.
Using the variable could make a contract vulnerable if an authorized account calls a malicious contract. You can impersonate a user using a third party contract.
This can make it easier to create a vault on behalf of another user with an external administrator (by receiving it as an argument).

<details>
<summary><i>There are 5 instances of this issue:</i></summary>

```solidity
📁 File: src/mimswap/MagicLP.sol

250:         (receiveQuoteAmount, mtFee, newRState, newBaseTarget) = querySellBase(tx.origin, baseInput); 

273:         (receiveBaseAmount, mtFee, newRState, newQuoteTarget) = querySellQuote(tx.origin, quoteInput); 

311:                 tx.origin, 

333:                 tx.origin, 
```
[250](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L250), [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L273), [311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L311), [333](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L333)

```solidity
📁 File: src/mimswap/periphery/Factory.sol

82:         address creator = tx.origin; 
```
[82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L82)

</details>


---
### [L&#x2011;2] Consider bounding input array length
The functions below take in an unbounded array, and make function calls for entries in the array. While the function will revert if it eventually runs out of gas, it may be a nicer user experience to `require()` that the length of the array is below some reasonable maximum, so that the user doesn't have to use up a full transaction's gas only to see that the transaction reverts.


<i>There is one instance of this issue:</i>

```solidity
📁 File: src/blast/BlastOnboarding.sol

/// @audit tokens.length not bounded
165:         for (uint256 i = 0; i < tokens.length; i++) { 
166:             if (!supportedTokens[tokens[i]]) {
167:                 revert ErrUnsupportedToken();
168:             }
169:             if (registry.nativeYieldTokens(tokens[i])) {
170:                 BlastYields.claimAllTokenYields(tokens[i], feeTo);
171:             }
172:         }
```
[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L165-L172)


---
### [L&#x2011;3] Consider implementing two-step procedure for updating protocol addresses
A copy-paste error or a typo may end up bricking protocol functionality, or sending tokens to an address with no known private key. Consider implementing a two-step procedure for updating protocol addresses, where the recipient is set as pending, and must 'accept' the assignment by making an affirmative call. A straight forward way of doing this would be to have the target contracts implement [EIP-165](https://eips.ethereum.org/EIPS/eip-165), and to have the 'set' functions ensure that the recipient is of the right interface type.

<details>
<summary><i>There are 8 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastBox.sol

/// @audit line 77
72:     function setFeeTo(address feeTo_) external onlyOwner { 
73:         if (feeTo_ == address(0)) {
74:             revert ErrZeroAddress();
75:         }
76: 
77:         feeTo = feeTo_;
78:         emit LogFeeToChanged(feeTo_);
79:     }
```
[72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol/#L72-L79)

```solidity
📁 File: src/blast/BlastGovernor.sol

/// @audit line 45
40:     function setFeeTo(address _feeTo) external onlyOwner { 
41:         if(_feeTo == address(0)) {
42:             revert ErrZeroAddress();
43:         }
44:         
45:         feeTo = _feeTo;
46:         emit LogFeeToChanged(_feeTo);
47:     }
```
[40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol/#L40-L47)

```solidity
📁 File: src/blast/BlastMagicLP.sol

/// @audit line 85
80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner { 
81:         if (feeTo_ == address(0)) {
82:             revert ErrZeroAddress();
83:         }
84: 
85:         feeTo = feeTo_;
86:         emit LogFeeToChanged(feeTo_);
87:     }
```
[80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol/#L80-L87)

```solidity
📁 File: src/blast/BlastOnboarding.sol

/// @audit line 152
147:     function setFeeTo(address feeTo_) external onlyOwner { 
148:         if (feeTo_ == address(0)) {
149:             revert ErrZeroAddress();
150:         }
151: 
152:         feeTo = feeTo_;
153:         emit LogFeeToChanged(feeTo_);
154:     }

/// @audit line 191
190:     function setBootstrapper(address bootstrapper_) external onlyOwner { 
191:         bootstrapper = bootstrapper_;
192:         emit LogBootstrapperChanged(bootstrapper_);
193:     }
```
[147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L147-L154), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L190-L193)

```solidity
📁 File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit line 51
46:     function setMaintainer(address maintainer_) external onlyOwner { 
47:         if (maintainer_ == address(0)) {
48:             revert ErrZeroAddress();
49:         }
50: 
51:         maintainer = maintainer_;
52:         emit LogMaintainerChanged(maintainer_);
53:     }

/// @audit line 58
57:     function setImplementation(address implementation_) public onlyOwner { 
58:         implementation = implementation_;
59:         emit LogImplementationChanged(implementation_);
60:     }
```
[46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol/#L46-L53), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol/#L57-L60)

```solidity
📁 File: src/mimswap/periphery/Factory.sol

/// @audit line 101
96:     function setLpImplementation(address implementation_) external onlyOwner { 
97:         if (implementation_ == address(0)) {
98:             revert ErrZeroAddress();
99:         }
100: 
101:         implementation = implementation_;
102:         emit LogSetImplementation(implementation_);
103:     }
```
[96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L96-L103)

</details>