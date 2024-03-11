# QA Report

## Summary

### Low Issues

Total **355 instances** over **33 issues**:

|ID|Issue|Instances|
|:--:|:---|:--:|
| [[L-01]](#l-01-array-length-is-not-checked-before-access-its-index) | Array length is not checked before access its index | 2 |
| [[L-02]](#l-02-dividing-by-totalsupply-can-result-in-a-zero-division-error) | Dividing by `totalSupply()` can result in a zero division error | 1 |
| [[L-03]](#l-03-multiplication-on-the-result-of-a-division) | Multiplication on the result of a division | 3 |
| [[L-04]](#l-04-events-may-be-emitted-out-of-order-due-to-reentrancy) | Events may be emitted out of order due to reentrancy | 34 |
| [[L-05]](#l-05-variables-shadowing-other-definitions) | Variables shadowing other definitions | 1 |
| [[L-06]](#l-06-missing-zero-address-check-in-constructor) | Missing zero address check in constructor | 4 |
| [[L-07]](#l-07-missing-zero-address-check-in-initializer) | Missing zero address check in initializer | 1 |
| [[L-08]](#l-08-function-receivepayable-fallback-does-not-authorize-sender) | Function `receive()`/`payable fallback()` does not authorize sender | 3 |
| [[L-09]](#l-09-revert-on-transfer-to-the-zero-address) | Revert on transfer to the zero address | 23 |
| [[L-10]](#l-10-using--without-specifying-an-upper-bound-in-version-pragma-is-unsafe) | Using `>`/`>=` without specifying an upper bound in version pragma is unsafe | 20 |
| [[L-11]](#l-11-array-is-pushed-but-not-poped) | Array is `push()`ed but not `pop()`ed | 5 |
| [[L-12]](#l-12-state-variables-not-limited-to-reasonable-values) | State variables not limited to reasonable values | 1 |
| [[L-13]](#l-13-consider-implementing-two-step-procedure-for-updating-protocol-addresses) | Consider implementing two-step procedure for updating protocol addresses | 16 |
| [[L-14]](#l-14-unsafe-conversion-from-unsigned-to-signed-values) | Unsafe conversion from unsigned to signed values | 1 |
| [[L-15]](#l-15-vulnerable-versions-of-packages-are-being-used) | Vulnerable versions of packages are being used | 1 |
| [[L-16]](#l-16-constructor--initialization-function-lacks-parameter-validation) | Constructor / initialization function lacks parameter validation | 1 |
| [[L-17]](#l-17-missing-checks-for-address0-when-setting-address-state-variables) | Missing checks for `address(0)` when setting address state variables | 3 |
| [[L-18]](#l-18-unsafe-solidity-low-level-call-can-cause-gas-grief-attack) | Unsafe solidity low-level call can cause gas grief attack | 1 |
| [[L-19]](#l-19-contracts-are-vulnerable-to-fee-on-transfer-accounting-related-issues) | Contracts are vulnerable to fee-on-transfer accounting-related issues | 32 |
| [[L-20]](#l-20-functions-calling-contractsaddresses-with-transfer-hooks-should-be-protected-by-reentrancy-guard) | Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard | 34 |
| [[L-21]](#l-21-critical-functions-should-be-controlled-by-time-locks) | Critical functions should be controlled by time locks | 26 |
| [[L-22]](#l-22-missing-contract-existence-checks-before-low-level-calls) | Missing contract existence checks before low-level calls | 1 |
| [[L-23]](#l-23-external-function-calls-within-loops) | External function calls within loops | 5 |
| [[L-24]](#l-24-tokens-may-be-minted-to-the-zero-address) | Tokens may be minted to the zero address | 3 |
| [[L-25]](#l-25-sending-tokens-within-loops) | Sending tokens within loops | 1 |
| [[L-26]](#l-26-some-tokens-may-revert-when-zero-value-transfers-are-made) | Some tokens may revert when zero value transfers are made | 27 |
| [[L-27]](#l-27-use-safecast-to-downcast-safely) | Use `SafeCast` to downcast safely | 6 |
| [[L-28]](#l-28-use-descriptive-constant-instead-of-0-as-a-parameter) | Use descriptive constant instead of 0 as a parameter | 1 |
| [[L-29]](#l-29-large-approvals-may-not-work-with-some-erc20-tokens) | Large approvals may not work with some `ERC20` tokens | 3 |
| [[L-30]](#l-30-code-does-not-follow-the-best-practice-of-check-effects-interaction) | Code does not follow the best practice of check-effects-interaction | 38 |
| [[L-31]](#l-31-some-tokens-may-revert-when-large-transfers-are-made) | Some tokens may revert when large transfers are made | 32 |
| [[L-32]](#l-32-unchecked-blocks-with-additionsmultiplications-may-overflow) | `unchecked` blocks with additions/multiplications may overflow | 3 |
| [[L-33]](#l-33-contracts-are-vulnerable-to-rebasing-accounting-related-issues) | Contracts are vulnerable to rebasing accounting-related issues | 22 |

### Non Critical Issues

Total **2930 instances** over **109 issues**:

|ID|Issue|Instances|
|:--:|:---|:--:|
| [[N-01]](#n-01-visibility-of-state-variables-is-not-explicitly-defined) | Visibility of state variables is not explicitly defined | 1 |
| [[N-02]](#n-02-names-of-privateinternal-functions-should-be-prefixed-with-an-underscore) | Names of `private`/`internal` functions should be prefixed with an underscore | 25 |
| [[N-03]](#n-03-names-of-privateinternal-state-variables-should-be-prefixed-with-an-underscore) | Names of `private`/`internal` state variables should be prefixed with an underscore | 4 |
| [[N-04]](#n-04-order-of-functions-does-not-follow-the-solidity-style-guide) | Order of functions does not follow the Solidity Style Guide | 65 |
| [[N-05]](#n-05-use-of-override-is-unnecessary) | Use of `override` is unnecessary | 13 |
| [[N-06]](#n-06-unused-errors) | Unused errors | 6 |
| [[N-07]](#n-07-unused-events) | Unused events | 3 |
| [[N-08]](#n-08-consider-providing-a-ranged-getter-for-array-state-variables) | Consider providing a ranged getter for array state variables | 3 |
| [[N-09]](#n-09-consider-splitting-complex-checks-into-multiple-steps) | Consider splitting complex checks into multiple steps | 2 |
| [[N-10]](#n-10-complex-casting) | Complex casting | 4 |
| [[N-11]](#n-11-complex-math-should-be-split-into-multiple-steps) | Complex math should be split into multiple steps | 4 |
| [[N-12]](#n-12-consider-adding-a-blockdeny-list) | Consider adding a block/deny-list | 4 |
| [[N-13]](#n-13-constantsimmutables-redefined-elsewhere) | Constants/Immutables redefined elsewhere | 2 |
| [[N-14]](#n-14-convert-simple-if-statements-to-ternary-expressions) | Convert simple `if`-statements to ternary expressions | 5 |
| [[N-15]](#n-15-contracts-should-each-be-defined-in-separate-files) | Contracts should each be defined in separate files | 3 |
| [[N-16]](#n-16-contract-name-does-not-match-its-filename) | Contract name does not match its filename | 3 |
| [[N-17]](#n-17-upper_case-names-should-be-reserved-for-constantimmutable-variables) | UPPER_CASE names should be reserved for `constant`/`immutable` variables | 25 |
| [[N-18]](#n-18-do-not-use-literal-numbers-for-array-indexes) | Do not use literal numbers for array indexes | 3 |
| [[N-19]](#n-19-contract-timekeeping-will-break-earlier-than-the-ethereum-network-itself-will-stop-working) | Contract timekeeping will break earlier than the Ethereum network itself will stop working | 2 |
| [[N-20]](#n-20-consider-emitting-an-event-at-the-end-of-the-constructor) | Consider emitting an event at the end of the constructor | 16 |
| [[N-21]](#n-21-empty-function-body-without-comments) | Empty function body without comments | 3 |
| [[N-22]](#n-22-events-are-emitted-without-the-sender-information) | Events are emitted without the sender information | 10 |
| [[N-23]](#n-23-event-is-missing-indexed-fields) | Event is missing `indexed` fields | 19 |
| [[N-24]](#n-24-function-state-mutability-can-be-restricted-to-pure) | Function state mutability can be restricted to pure | 1 |
| [[N-25]](#n-25-imports-could-be-organized-more-systematically) | Imports could be organized more systematically | 13 |
| [[N-26]](#n-26-openzeppelincontracts-should-be-upgraded-to-a-newer-version) | @openzeppelin/contracts should be upgraded to a newer version | 8 |
| [[N-27]](#n-27-safe-contracts-should-be-upgraded-to-a-newer-version) | safe-contracts should be upgraded to a newer version | 1 |
| [[N-28]](#n-28-lib-solady-should-be-upgraded-to-a-newer-version) | Lib solady should be upgraded to a newer version | 10 |
| [[N-29]](#n-29-lines-are-too-long) | Lines are too long | 54 |
| [[N-30]](#n-30-functions-not-used-internally-could-be-marked-external) | Functions not used internally could be marked external | 17 |
| [[N-31]](#n-31-contracts-containing-only-utility-functions-should-be-made-into-libraries) | Contracts containing only utility functions should be made into libraries | 2 |
| [[N-32]](#n-32-use-inheritdoc-for-overridden-functions) | Use `@inheritdoc` for overridden functions | 14 |
| [[N-33]](#n-33-contracts-should-have-natspec-author-tags) | Contracts should have NatSpec `@author` tags | 19 |
| [[N-34]](#n-34-contracts-should-have-notice-tags) | Contracts should have `@notice` tags | 17 |
| [[N-35]](#n-35-contracts-should-have-natspec-title-tags) | Contracts should have NatSpec `@title` tags | 21 |
| [[N-36]](#n-36-events-missing-natspec-param-tag) | Events missing NatSpec `@param` tag | 123 |
| [[N-37]](#n-37-constructors-missing-natspec-param-tag) | Constructors missing NatSpec `@param` tag | 29 |
| [[N-38]](#n-38-functions-missing-natspec-param-tag) | Functions missing NatSpec `@param` tag | 359 |
| [[N-39]](#n-39-modifiers-missing-natspec-param-tag) | Modifiers missing NatSpec `@param` tag | 3 |
| [[N-40]](#n-40-natspec-non-public-state-variable-declarations-should-use-dev-tags) | NatSpec: Non-public state variable declarations should use `@dev` tags | 13 |
| [[N-41]](#n-41-functions-missing-natspec-return-tag) | Functions missing NatSpec `@return` tag | 119 |
| [[N-42]](#n-42-state-variables-should-have-natspec-descriptions) | State variables should have NatSpec descriptions | 52 |
| [[N-43]](#n-43-structs-missing-natspec-param-tag) | Structs missing NatSpec `@param` tag | 23 |
| [[N-44]](#n-44-functions-should-be-named-in-mixedcase-style) | Functions should be named in mixedCase style | 12 |
| [[N-45]](#n-45-variable-names-for-immutables-should-use-upper_case_with_underscores) | Variable names for `immutable`s should use UPPER_CASE_WITH_UNDERSCORES | 16 |
| [[N-46]](#n-46-variables-should-be-named-in-mixedcase-style) | Variables should be named in mixedCase style | 36 |
| [[N-47]](#n-47-names-of-publicexternal-functions-and-state-variables-should-not-be-prefixed-with-underscore) | Names of `public`/`external` functions and state variables should NOT be prefixed with underscore | 14 |
| [[N-48]](#n-48-order-of-contract-layout-does-not-follow-the-solidity-style-guide) | Order of contract layout does not follow the Solidity Style Guide | 15 |
| [[N-49]](#n-49-consider-adding-validation-of-user-inputs) | Consider adding validation of user inputs | 55 |
| [[N-50]](#n-50-constants-should-be-put-on-the-left-side-of-comparisons) | Constants should be put on the left side of comparisons | 61 |
| [[N-51]](#n-51-put-all-system-wide-constants-in-one-file) | Put all system-wide constants in one file | 8 |
| [[N-52]](#n-52-else-block-not-required) | `else`-block not required | 5 |
| [[N-53]](#n-53-large-multiples-of-ten-should-use-scientific-notation) | Large multiples of ten should use scientific notation | 3 |
| [[N-54]](#n-54-spdx-identifier-should-be-the-in-the-first-line-of-a-solidity-file) | SPDX identifier should be the in the first line of a solidity file | 5 |
| [[N-55]](#n-55-high-cyclomatic-complexity) | High cyclomatic complexity | 2 |
| [[N-56]](#n-56-typos) | Typos | 12 |
| [[N-57]](#n-57-consider-bounding-input-array-length) | Consider bounding input array length | 5 |
| [[N-58]](#n-58-unnecessary-casting) | Unnecessary casting | 28 |
| [[N-59]](#n-59-unused-import) | Unused import | 47 |
| [[N-60]](#n-60-unused-local-variables) | Unused local variables | 2 |
| [[N-61]](#n-61-unused-modifiers) | Unused modifiers | 2 |
| [[N-62]](#n-62-unused-named-return) | Unused named return | 24 |
| [[N-63]](#n-63-use-delete-instead-of-assigning-values-to-false) | Use delete instead of assigning values to `false` | 1 |
| [[N-64]](#n-64-consider-using-delete-rather-than-assigning-zero-to-clear-values) | Consider using `delete` rather than assigning zero to clear values | 2 |
| [[N-65]](#n-65-use-the-latest-solidity-version) | Use the latest Solidity version | 20 |
| [[N-66]](#n-66-consider-using-named-function-arguments) | Consider using named function arguments | 14 |
| [[N-67]](#n-67-named-returns-are-recommended) | Named returns are recommended | 62 |
| [[N-68]](#n-68-use-typexmax-instead-of-constant-formulas-like-2n) | Use `type(X).max` instead of constant formulas like `2**n` | 2 |
| [[N-69]](#n-69-consider-using-the-using-for-syntax) | Consider using the `using`-`for` syntax | 96 |
| [[N-70]](#n-70-using-underscore-at-the-end-of-variable-name) | Using underscore at the end of variable name | 98 |
| [[N-71]](#n-71-use-a-struct-to-encapsulate-multiple-function-parameters) | Use a struct to encapsulate multiple function parameters | 8 |
| [[N-72]](#n-72-returning-a-struct-instead-of-a-bunch-of-variables-is-better) | Returning a struct instead of a bunch of variables is better | 6 |
| [[N-73]](#n-73-events-that-mark-critical-parameter-changes-should-contain-both-the-old-and-the-new-value) | Events that mark critical parameter changes should contain both the old and the new value | 15 |
| [[N-74]](#n-74-contract-variables-should-have-comments) | Contract variables should have comments | 6 |
| [[N-75]](#n-75-missing-event-when-a-state-variables-is-set-in-constructor) | Missing event when a state variables is set in constructor | 9 |
| [[N-76]](#n-76-file-is-missing-natspec) | File is missing NatSpec | 8 |
| [[N-77]](#n-77-empty-bytes-check-is-missing) | Empty bytes check is missing | 6 |
| [[N-78]](#n-78-dont-define-functions-with-the-same-name-in-a-contract) | Don't define functions with the same name in a contract | 2 |
| [[N-79]](#n-79-multiple-mappings-with-same-keys-can-be-combined-into-a-single-struct-mapping-for-readability) | Multiple mappings with same keys can be combined into a single struct mapping for readability | 13 |
| [[N-80]](#n-80-function-state-mutability-can-be-restricted-to-view) | Function state mutability can be restricted to view | 1 |
| [[N-81]](#n-81-functions-contain-the-same-code) | Functions contain the same code | 10 |
| [[N-82]](#n-82-inconsistent-spacing-in-comments) | Inconsistent spacing in comments | 88 |
| [[N-83]](#n-83-missing-event-for-critical-changes) | Missing event for critical changes | 1 |
| [[N-84]](#n-84-duplicated-requirerevert-checks-should-be-refactored) | Duplicated `require()`/`revert()` checks should be refactored | 29 |
| [[N-85]](#n-85-consider-adding-emergency-stop-functionality) | Consider adding emergency-stop functionality | 14 |
| [[N-86]](#n-86-enable-ir-based-code-generation) | Enable IR-based code generation | 1 |
| [[N-87]](#n-87-missing-checks-for-uint-state-variable-assignments) | Missing checks for uint state variable assignments | 3 |
| [[N-88]](#n-88-use-the-modern-upgradeable-contract-paradigm) | Use the Modern Upgradeable Contract Paradigm | 17 |
| [[N-89]](#n-89-contracts-should-have-natspec-dev-tags) | Contracts should have NatSpec `@dev` tags | 23 |
| [[N-90]](#n-90-error-declarations-should-have-natspec-descriptions) | Error declarations should have NatSpec descriptions | 78 |
| [[N-91]](#n-91-missing-natspec-dev-from-event-declaration) | Missing NatSpec `@dev` from event declaration | 53 |
| [[N-92]](#n-92-missing-natspec-notice-from-event-declaration) | Missing NatSpec `@notice` from event declaration | 53 |
| [[N-93]](#n-93-missing-natspec-dev-from-constructor) | Missing NatSpec `@dev` from constructor | 15 |
| [[N-94]](#n-94-missing-natspec-notice-from-constructor) | Missing NatSpec `@notice` from constructor | 16 |
| [[N-95]](#n-95-missing-natspec-dev-from-receive-function-declaration) | Missing NatSpec `@dev` from receive function declaration | 3 |
| [[N-96]](#n-96-missing-natspec-notice-from-receive-function-declaration) | Missing NatSpec `@notice` from receive function declaration | 3 |
| [[N-97]](#n-97-missing-natspec-dev-from-function-declaration) | Missing NatSpec `@dev` from function declaration | 194 |
| [[N-98]](#n-98-missing-natspec-notice-from-function-declaration) | Missing NatSpec `@notice` from function declaration | 191 |
| [[N-99]](#n-99-missing-natspec-dev-from-modifier-declaration) | Missing NatSpec `@dev` from modifier declaration | 7 |
| [[N-100]](#n-100-missing-natspec-notice-from-modifier-declaration) | Missing NatSpec `@notice` from modifier declaration | 7 |
| [[N-101]](#n-101-missing-natspec-dev-from-struct-declaration) | Missing NatSpec `@dev` from struct declaration | 7 |
| [[N-102]](#n-102-missing-natspec-notice-from-struct-declaration) | Missing NatSpec `@notice` from struct declaration | 7 |
| [[N-103]](#n-103-large-or-complicated-code-bases-should-implement-invariant-tests) | Large or complicated code bases should implement invariant tests | 1 |
| [[N-104]](#n-104-the-default-value-is-manually-set-when-it-is-declared) | The default value is manually set when it is declared | 2 |
| [[N-105]](#n-105-contracts-should-have-all-publicexternal-functions-exposed-by-interfaces) | Contracts should have all `public`/`external` functions exposed by `interface`s | 12 |
| [[N-106]](#n-106-top-level-declarations-should-be-separated-by-at-least-two-lines) | Top-level declarations should be separated by at least two lines | 171 |
| [[N-107]](#n-107-consider-adding-formal-verification-proofs) | Consider adding formal verification proofs | 20 |
| [[N-108]](#n-108-prevent-re-setting-a-state-variable-with-the-same-value) | Prevent re-setting a state variable with the same value | 47 |
| [[N-109]](#n-109-whitespace-in-expressions) | Whitespace in Expressions | 13 |


## Low Issues

### [L-01] Array length is not checked before access its index

Accessing the elements of the array without checking or ensuring the validity of the access index in advance. It may result in an unexpected out-of-bounds error, or may result in missing elements when trying to traverse the entire array.

There are 2 instances:

- *Router.sol* ( [324-324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L324-L324), [345-345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L345-L345) ):

```solidity
324:         address firstLp = path[0];

345:         address firstLp = path[0];
```

### [L-02] Dividing by `totalSupply()` can result in a zero division error

The `totalSupply()` being zero will result in a division by zero, causing the transaction to fail.

There is 1 instance:

- *MagicLpAggregator.sol* ( [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L45-L45) ):

```solidity
45:         return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
```

### [L-03] Multiplication on the result of a division

Dividing a number by another often results in a loss of precision. Multiplying the result by another number increases the loss of precision, often significantly.
For example: `x*(y/z)` should be re-written as `(x*z)/y`.

There are 3 instances:

- *Math.sol* ( [99-99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L99-L99), [158-158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L158-L158), [170-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L170-L170) ):

```solidity
99:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);

158:                 temp = (((delta * V1) / V0) * i) / V0;

170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
```

### [L-04] Events may be emitted out of order due to reentrancy

Ensure that events follow the best practice of check-effects-interaction, and are emitted before external calls.

<details>
<summary>There are 34 instances (click to show):</summary>

- *BlastBox.sol* ( [90-90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L90-L90) ):

```solidity
/// @audit nativeYieldTokens() is called prior to this emission in setTokenEnabled()
90:         emit LogTokenDepositEnabled(token, enabled);
```

- *BlastOnboarding.sol* ( [120-120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L120-L120), [140-140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L140-L140), [182-182](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L182-L182), [211-211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L211-L211) ):

```solidity
/// @audit safeTransferFrom() is called prior to this emission in deposit()
120:         emit LogDeposit(msg.sender, token, amount, lock_);

/// @audit safeTransfer() is called prior to this emission in withdraw()
140:         emit LogWithdraw(msg.sender, token, amount);

/// @audit nativeYieldTokens() is called prior to this emission in setTokenSupported()
182:         emit LogTokenSupported(token, supported);

/// @audit safeTransfer() is called prior to this emission in rescue()
211:         emit LogTokenRescue(token, to, amount);
```

- *BlastOnboardingBoot.sol* ( [71-71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L71-L71), [124-124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L124-L124), [132-132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L132-L132) ):

```solidity
/// @audit stakeFor() is called prior to this emission in claim()
71:         emit LogClaimed(msg.sender, shares, lock);

/// @audit safeApprove() is called prior to this emission in bootstrap()
124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

/// @audit factory() is called prior to this emission in initialize()
132:         emit LogInitialized(_router);
```

- *BlastYields.sol* ( [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L26-L26), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L31-L31), [44-44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L44-L44), [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L57-L57), [62-62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L62-L62), [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L72-L72), [77-77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L77-L77) ):

```solidity
/// @audit configure() is called prior to this emission in enableTokenClaimable()
26:         emit LogBlastTokenClaimableEnabled(address(this), token);

/// @audit configure() is called prior to this emission in configureDefaultClaimables()
31:         emit LogBlastNativeClaimableEnabled(address(this));

/// @audit claimMaxGas() is called prior to this emission in claimMaxGasYields()
44:         emit LogBlastGasClaimed(recipient, amount);

/// @audit claimAllYield() is called prior to this emission in claimAllNativeYields()
57:         emit LogBlastETHClaimed(recipient, amount);

/// @audit claimYield() is called prior to this emission in claimNativeYields()
62:         emit LogBlastETHClaimed(recipient, amount);

/// @audit claim() is called prior to this emission in claimAllTokenYields()
72:         emit LogBlastTokenClaimed(recipient, address(token), amount);

/// @audit claim() is called prior to this emission in claimTokenYields()
77:         emit LogBlastTokenClaimed(recipient, address(token), amount);
```

- *MagicLP.sol* ( [259-259](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L259-L259), [264-264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L264-L264), [282-282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L282-L282), [287-287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L287-L287), [323-323](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L323-L323), [325-325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L325-L325), [345-345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L345-L345), [347-347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L347-L347), [352-352](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L352-L352), [454-454](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L454-L454), [467-467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L467-L467), [501-501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L501-L501) ):

```solidity
/// @audit _transferQuoteOut() is called prior to this emission in sellBase(), which will call `safeTransfer()`
259:             emit RChange(newRState);

/// @audit _transferQuoteOut() is called prior to this emission in sellBase(), which will call `safeTransfer()`
264:         emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

/// @audit _transferBaseOut() is called prior to this emission in sellQuote(), which will call `safeTransfer()`
282:             emit RChange(newRState);

/// @audit _transferBaseOut() is called prior to this emission in sellQuote(), which will call `safeTransfer()`
287:         emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

/// @audit _transferBaseOut() is called prior to this emission in flashLoan(), which will call `safeTransfer()`
323:                 emit RChange(newRState);

/// @audit _transferBaseOut() is called prior to this emission in flashLoan(), which will call `safeTransfer()`
325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

/// @audit _transferBaseOut() is called prior to this emission in flashLoan(), which will call `safeTransfer()`
345:                 emit RChange(newRState);

/// @audit _transferBaseOut() is called prior to this emission in flashLoan(), which will call `safeTransfer()`
347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

/// @audit _transferBaseOut() is called prior to this emission in flashLoan(), which will call `safeTransfer()`
352:         emit FlashLoan(msg.sender, assetTo, baseAmount, quoteAmount);

/// @audit _transferBaseOut() is called prior to this emission in sellShares(), which will call `safeTransfer()`
454:         emit SellShares(msg.sender, to, shareAmount, balanceOf(msg.sender));

/// @audit safeTransfer() is called prior to this emission in rescue()
467:         emit TokenRescue(token, to, amount);

/// @audit _transferBaseOut() is called prior to this emission in setParameters(), which will call `safeTransfer()`
501:         emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);
```

- *Factory.sol* ( [88-88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L88-L88) ):

```solidity
/// @audit init() is called prior to this emission in create()
88:         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
```

- *LockingMultiRewards.sol* ( [183-183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L183-L183), [331-331](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L331-L331), [392-392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L392-L392), [475-475](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L475-L475), [638-638](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L638-L638), [651-651](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L651-L651) ):

```solidity
/// @audit safeTransfer() is called prior to this emission in withdraw()
183:         emit LogWithdrawn(msg.sender, amount);

/// @audit safeTransfer() is called prior to this emission in recover()
331:         emit LogRecovered(tokenAddress, tokenAmount);

/// @audit safeTransferFrom() is called prior to this emission in notifyRewardAmount()
392:         emit LogRewardAdded(amount);

/// @audit safeTransferFrom() is called prior to this emission in _stakeFor()
475:             emit LogStaked(account, amount);

/// @audit safeTransfer() is called prior to this emission in _getRewards()
638:                         emit LogRewardPaid(user, rewardToken, amount);

/// @audit safeTransfer() is called prior to this emission in _getRewards()
651:             emit LogRewardLocked(user, rewardToken, rewardAmount);
```

</details>

### [L-05] Variables shadowing other definitions

A variable declaration shadowing any other existing definition is error-prone. It can cause confusion for developers, potentially introduce bugs, and reduce the readability and maintainability.

There is 1 instance:

- *BlastWrappers.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L20-L20) ):

```solidity
/// @audit Shadows `state variable factory`
20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
```

### [L-06] Missing zero address check in constructor

Constructors often take address parameters to initialize important components of a contract, such as owner or linked contracts. However, without a checking, there's a risk that an address parameter could be mistakenly set to the zero address (0x0). This could be due to an error or oversight during contract deployment. A zero address in a crucial role can cause serious issues, as it cannot perform actions like a normal address, and any funds sent to it will be irretrievable. It's therefore crucial to include a zero address check in constructors to prevent such potential problems. If a zero address is detected, the constructor should revert the transaction.

There are 4 instances:

- *MagicLpAggregator.sol* ( [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L21-L21) ):

```solidity
/// @audit `pair_ not checked`
/// @audit `baseOracle_ not checked`
/// @audit `quoteOracle_ not checked`
21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```

- *LockingMultiRewards.sol* ( [112-118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L112-L118) ):

```solidity
/// @audit `_stakingToken not checked`
112:     constructor(
113:         address _stakingToken,
114:         uint256 _lockingBoostMultiplerInBips,
115:         uint256 _rewardsDuration,
116:         uint256 _lockDuration,
117:         address _owner
118:     ) OperatableV2(_owner) {
```

### [L-07] Missing zero address check in initializer

Consider adding a zero address check for each address type parameter in initializer.

There is 1 instance:

- *BlastOnboardingBoot.sol* ( [129-129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L129-L129) ):

```solidity
/// @audit `_router not checked`
129:     function initialize(Router _router) external onlyOwner {
```

### [L-08] Function `receive()`/`payable fallback()` does not authorize sender

Users may send ETH by mistake to these contracts. As there is no access control on these functions, the funds will be permanently lost.

There are 3 instances:

- *BlastGovernor.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L13) ):

```solidity
13:     receive() external payable {}
```

- *BlastOnboarding.sol* ( [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L80) ):

```solidity
80:     receive() external payable override {
```

- *Router.sol* ( [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L36) ):

```solidity
36:     receive() external payable {}
```

### [L-09] Revert on transfer to the zero address

It's good practice to revert a token transfer transaction if the recipient's address is the zero address. This can prevent unintentional transfers to the zero address due to accidental operations or programming errors. Many token contracts implement such a safeguard, such as [OpenZeppelin - ERC20](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/9e3f4d60c581010c4a3979480e07cc7752f124cc/contracts/token/ERC20/ERC20.sol#L232), [OpenZeppelin - ERC721](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/9e3f4d60c581010c4a3979480e07cc7752f124cc/contracts/token/ERC721/ERC721.sol#L142).

<details>
<summary>There are 23 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [210-210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L210-L210) ):

```solidity
210:         token.safeTransfer(to, amount);
```

- *MagicLP.sol* ( [466-466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L466-L466), [583-583](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L583-L583), [589-589](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L589-L589) ):

```solidity
466:         token.safeTransfer(to, amount);

583:             _BASE_TOKEN_.safeTransfer(to, amount);

589:             _QUOTE_TOKEN_.safeTransfer(to, amount);
```

- *Router.sol* ( [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L68-L68), [69-69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L69-L69), [91-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L91-L91), [172-172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L172-L172), [173-173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L173-L173), [186-186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L186-L186), [187-187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L187-L187), [311-311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L311-L311), [328-328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L328-L328), [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L330-L330), [360-360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L360-L360), [393-393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L393-L393), [395-395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L395-L395), [411-411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L411-L411), [428-428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L428-L428), [456-456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L456-L456), [474-474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L474-L474) ):

```solidity
68:         baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);

69:         quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);

91:         token.safeTransferFrom(msg.sender, clone, tokenInAmount);

172:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);

173:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);

186:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);

187:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);

311:         token.safeTransfer(to, tokenAmountOut);

328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

360:         inToken.safeTransfer(address(firstLp), msg.value);

393:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

395:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

411:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

428:         baseToken.safeTransfer(lp, msg.value);

456:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

474:         quoteToken.safeTransfer(lp, msg.value);
```

- *LockingMultiRewards.sol* ( [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L330-L330), [637-637](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L637-L637) ):

```solidity
330:         tokenAddress.safeTransfer(owner, tokenAmount);

637:                         rewardToken.safeTransfer(user, amount);
```

</details>

### [L-10] Using `>`/`>=` without specifying an upper bound in version pragma is unsafe

There **will** be breaking changes in future versions of solidity, and at that point your code will no longer be compatible. While you may have the specific version to use in a configuration file, others that include your source files may not.

<details>
<summary>There are 20 instances (click to show):</summary>

- *BlastBox.sol* ( [3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L3) ):

```solidity
3: pragma solidity >=0.8.0;
```

- *BlastDapp.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastGovernor.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastMagicLP.sol* ( [3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L3) ):

```solidity
3: pragma solidity >=0.8.0;
```

- *BlastOnboarding.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastOnboardingBoot.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastTokenRegistry.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastWrappers.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastPoints.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastYields.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *MagicLP.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L8) ):

```solidity
8: pragma solidity >=0.8.0;
```

- *FeeRateModel.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L8) ):

```solidity
8: pragma solidity >=0.8.0;
```

- *FeeRateModelImpl.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *DecimalMath.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L7) ):

```solidity
7: pragma solidity >=0.8.0;
```

- *Math.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L8) ):

```solidity
8: pragma solidity >=0.8.0;
```

- *PMMPricing.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L8) ):

```solidity
8: pragma solidity >=0.8.0;
```

- *Factory.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *Router.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *MagicLpAggregator.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *LockingMultiRewards.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

</details>

### [L-11] Array is `push()`ed but not `pop()`ed

Array entries are added but are never removed. Consider whether this should be the case, or whether there should be a maximum, or whether old entries should be removed. Cases where there are specific potential problems will be flagged separately under a different issue.

There are 5 instances:

- *Factory.sol* ( [149-149](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L149-L149), [150-150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L150-L150) ):

```solidity
149:         pools[baseToken][quoteToken].push(pool);

150:         userPools[creator].push(pool);
```

- *LockingMultiRewards.sol* ( [313-313](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L313-L313), [501-501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L501-L501), [648-648](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L648-L648) ):

```solidity
313:         rewardTokens.push(rewardToken);

501:             _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));

648:                 _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
```

### [L-12] State variables not limited to reasonable values

Consider adding appropriate minimum/maximum value checks to ensure that the following state variables can never be used to excessively harm users, including via griefing.

There is 1 instance:

- *LockingMultiRewards.sol* ( [319-319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L319-L319) ):

```solidity
319:         minLockAmount = _minLockAmount;
```

### [L-13] Consider implementing two-step procedure for updating protocol addresses

A copy-paste error or a typo may end up bricking protocol functionality, or sending tokens to an address with no known private key. Consider implementing a two-step procedure for updating protocol addresses, where the recipient is set as pending, and must 'accept' the assignment by making an affirmative call. A straight forward way of doing this would be to have the target contracts implement [EIP-165](https://eips.ethereum.org/EIPS/eip-165), and to have the 'set' functions ensure that the recipient is of the right interface type.

<details>
<summary>There are 16 instances (click to show):</summary>

- *BlastBox.sol* ( [72-79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L72-L79), [81-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L81-L91) ):

```solidity
72:     function setFeeTo(address feeTo_) external onlyOwner {
73:         if (feeTo_ == address(0)) {
74:             revert ErrZeroAddress();
75:         }
76: 
77:         feeTo = feeTo_;
78:         emit LogFeeToChanged(feeTo_);
79:     }

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {
82:         enabledTokens[token] = enabled;
83: 
84:         // enable native yields if token is recognized
85:         // no matter if it's enabled or not
86:         if (registry.nativeYieldTokens(token)) {
87:             BlastYields.enableTokenClaimable(token);
88:         }
89: 
90:         emit LogTokenDepositEnabled(token, enabled);
91:     }
```

- *BlastGovernor.sol* ( [40-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L40-L47) ):

```solidity
40:     function setFeeTo(address _feeTo) external onlyOwner {
41:         if(_feeTo == address(0)) {
42:             revert ErrZeroAddress();
43:         }
44:         
45:         feeTo = _feeTo;
46:         emit LogFeeToChanged(_feeTo);
47:     }
```

- *BlastMagicLP.sol* ( [80-87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L80-L87), [89-92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L89-L92) ):

```solidity
80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
81:         if (feeTo_ == address(0)) {
82:             revert ErrZeroAddress();
83:         }
84: 
85:         feeTo = feeTo_;
86:         emit LogFeeToChanged(feeTo_);
87:     }

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
90:         operators[operator] = status;
91:         emit LogOperatorChanged(operator, status);
92:     }
```

- *BlastOnboarding.sol* ( [147-154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L147-L154), [175-183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L175-L183), [185-188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L185-L188), [190-193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L190-L193) ):

```solidity
147:     function setFeeTo(address feeTo_) external onlyOwner {
148:         if (feeTo_ == address(0)) {
149:             revert ErrZeroAddress();
150:         }
151: 
152:         feeTo = feeTo_;
153:         emit LogFeeToChanged(feeTo_);
154:     }

175:     function setTokenSupported(address token, bool supported) external onlyOwner {
176:         supportedTokens[token] = supported;
177: 
178:         if (registry.nativeYieldTokens(token)) {
179:             BlastYields.enableTokenClaimable(token);
180:         }
181: 
182:         emit LogTokenSupported(token, supported);
183:     }

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
186:         caps[token] = cap;
187:         emit LogTokenCapChanged(token, cap);
188:     }

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {
191:         bootstrapper = bootstrapper_;
192:         emit LogBootstrapperChanged(bootstrapper_);
193:     }
```

- *BlastOnboardingBoot.sol* ( [137-144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L137-L144) ):

```solidity
137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {
138:         if (ready) {
139:             revert ErrCannotChangeOnceReady();
140:         }
141: 
142:         staking = _staking;
143:         emit LogStakingChanged(address(_staking));
144:     }
```

- *BlastTokenRegistry.sol* ( [14-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L14-L21) ):

```solidity
14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
15:         if (token == address(0)) {
16:             revert ErrZeroAddress();
17:         }
18: 
19:         nativeYieldTokens[token] = enabled;
20:         emit LogNativeYieldTokenEnabled(token, enabled);
21:     }
```

- *MagicLP.sol* ( [470-502](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L470-L502) ):

```solidity
470:     function setParameters(
471:         address assetTo,
472:         uint256 newLpFeeRate,
473:         uint256 newI,
474:         uint256 newK,
475:         uint256 baseOutAmount,
476:         uint256 quoteOutAmount,
477:         uint256 minBaseReserve,
478:         uint256 minQuoteReserve
479:     ) public nonReentrant onlyImplementationOwner {
480:         if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
481:             revert ErrReserveAmountNotEnough();
482:         }
483:         if (newI == 0 || newI > MAX_I) {
484:             revert ErrInvalidI();
485:         }
486:         if (newK > MAX_K) {
487:             revert ErrInvalidK();
488:         }
489:         if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {
490:             revert ErrInvalidLPFeeRate();
491:         }
492: 
493:         _LP_FEE_RATE_ = uint64(newLpFeeRate);
494:         _K_ = uint64(newK);
495:         _I_ = uint128(newI);
496: 
497:         _transferBaseOut(assetTo, baseOutAmount);
498:         _transferQuoteOut(assetTo, quoteOutAmount);
499:         (uint256 newBaseBalance, uint256 newQuoteBalance) = _resetTargetAndReserve();
500: 
501:         emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);
502:     }
```

- *FeeRateModel.sol* ( [46-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L46-L53), [57-60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L57-L60) ):

```solidity
46:     function setMaintainer(address maintainer_) external onlyOwner {
47:         if (maintainer_ == address(0)) {
48:             revert ErrZeroAddress();
49:         }
50: 
51:         maintainer = maintainer_;
52:         emit LogMaintainerChanged(maintainer_);
53:     }

57:     function setImplementation(address implementation_) public onlyOwner {
58:         implementation = implementation_;
59:         emit LogImplementationChanged(implementation_);
60:     }
```

- *Factory.sol* ( [96-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L96-L103), [105-112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L105-L112) ):

```solidity
96:     function setLpImplementation(address implementation_) external onlyOwner {
97:         if (implementation_ == address(0)) {
98:             revert ErrZeroAddress();
99:         }
100: 
101:         implementation = implementation_;
102:         emit LogSetImplementation(implementation_);
103:     }

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
106:         if (address(maintainerFeeRateModel_) == address(0)) {
107:             revert ErrZeroAddress();
108:         }
109: 
110:         maintainerFeeRateModel = maintainerFeeRateModel_;
111:         emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);
112:     }
```

</details>

### [L-14] Unsafe conversion from unsigned to signed values

The `int` type in Solidity uses the [two's complement system](https://en.wikipedia.org/wiki/Two%27s_complement), so it is possible to accidentally overflow a very large `uint` to an `int`, even if they share the same number of bytes (e.g. a `uint256 number > type(uint128).max` will overflow a `int256` cast).

Consider using the [SafeCast](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/utils/math/SafeCast.sol) library to prevent any overflows.

There is 1 instance:

- *MagicLpAggregator.sol* ( [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L45-L45) ):

```solidity
/// @audit uint -> int
45:         return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
```

### [L-15] Vulnerable versions of packages are being used

This project is using specific package versions which are vulnerable to the specific CVEs listed below. Consider switching to more recent versions of these packages that don't have these vulnerabilities.
- [CVE-2023-40014](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2023-40014) - **MEDIUM** - (`openzeppelin-solidity >=4.0.0 <4.9.3`): OpenZeppelin Contracts is a library for secure smart contract development. Starting in version 4.0.0 and prior to version 4.9.3, contracts using `ERC2771Context` along with a custom trusted forwarder may see `_msgSender` return `address(0)` in calls that originate from the forwarder with calldata shorter than 20 bytes. This combination of circumstances does not appear to be common, in particular it is not the case for `MinimalForwarder` from OpenZeppelin Contracts, or any deployed forwarder the team is aware of, given that the signer address is appended to all calls that originate from these forwarders. The problem has been patched in v4.9.3.

There is 1 instance:

- Global finding

### [L-16] Constructor / initialization function lacks parameter validation

Constructors and initialization functions play a critical role in contracts by setting important initial states when the contract is first deployed before the system starts. The parameters passed to the constructor and initialization functions directly affect the behavior of the contract / protocol. If incorrect parameters are provided, the system may fail to run, behave abnormally, be unstable, or lack security. Therefore, it's crucial to carefully check each parameter in the constructor and initialization functions. If an exception is found, the transaction should be rolled back.

There is 1 instance:

- *BlastWrappers.sol* ( [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L59-L59) ):

```solidity
/// @audit `data`
59:     function init(bytes calldata data) public payable override {
```

### [L-17] Missing checks for `address(0)` when setting address state variables

Consider adding a zero address check when setting address state variables.

There are 3 instances:

- *BlastOnboarding.sol* ( [191-191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L191-L191) ):

```solidity
191:         bootstrapper = bootstrapper_;
```

- *BlastOnboardingBoot.sol* ( [142-142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L142-L142) ):

```solidity
142:         staking = _staking;
```

- *FeeRateModel.sol* ( [58-58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L58-L58) ):

```solidity
58:         implementation = implementation_;
```

### [L-18] Unsafe solidity low-level call can cause gas grief attack

Using the low-level calls of a solidity address can leave the contract open to gas grief attacks. These attacks occur when the called contract returns a large amount of data.
So when calling an external contract, it is necessary to check the length of the return data before reading/copying it (using `returndatasize()`).

There is 1 instance:

- *BlastGovernor.sol* ( [54-54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L54-L54) ):

```solidity
54:         (success, result) = to.call{value: value}(data);
```

### [L-19] Contracts are vulnerable to fee-on-transfer accounting-related issues

Some tokens take a transfer fee (e.g. STA, PAXG), some do not currently charge a fee but may do so in the future (e.g. USDT, USDC).
The functions below transfer funds from the caller to the receiver via `transferFrom()`, but do not ensure that the actual number of tokens received is the same as the input amount to the transfer. If the token is a fee-on-transfer token, the balance after the transfer will be smaller than expected, leading to accounting issues. Even if there are checks later, related to a secondary transfer, an attacker may be able to use latent funds (e.g. mistakenly sent by another user) in order to get a free credit.
One way to solve this problem is to measure the balance before and after the transfer, and use the difference as the amount, rather than the stated amount.

<details>
<summary>There are 32 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [102-102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L102-L102), [138-138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L138-L138), [210-210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L210-L210) ):

```solidity
102:         token.safeTransferFrom(msg.sender, address(this), amount);

138:         token.safeTransfer(msg.sender, amount);

210:         token.safeTransfer(to, amount);
```

- *MagicLP.sol* ( [466-466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L466-L466), [583-583](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L583-L583), [589-589](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L589-L589) ):

```solidity
466:         token.safeTransfer(to, amount);

583:             _BASE_TOKEN_.safeTransfer(to, amount);

589:             _QUOTE_TOKEN_.safeTransfer(to, amount);
```

- *Router.sol* ( [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L68-L68), [69-69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L69-L69), [91-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L91-L91), [172-172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L172-L172), [173-173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L173-L173), [186-186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L186-L186), [187-187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L187-L187), [224-224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L224-L224), [246-246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L246-L246), [311-311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L311-L311), [328-328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L328-L328), [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L330-L330), [360-360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L360-L360), [393-393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L393-L393), [395-395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L395-L395), [411-411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L411-L411), [428-428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L428-L428), [443-443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L443-L443), [456-456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L456-L456), [474-474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L474-L474), [489-489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L489-L489) ):

```solidity
68:         baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);

69:         quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);

91:         token.safeTransferFrom(msg.sender, clone, tokenInAmount);

172:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);

173:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);

186:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);

187:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);

224:         token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);

246:         token.safeTransferFrom(msg.sender, lp, tokenInAmount);

311:         token.safeTransfer(to, tokenAmountOut);

328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

360:         inToken.safeTransfer(address(firstLp), msg.value);

393:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

395:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

411:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

428:         baseToken.safeTransfer(lp, msg.value);

443:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

456:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

474:         quoteToken.safeTransfer(lp, msg.value);

489:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
```

- *LockingMultiRewards.sol* ( [180-180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L180-L180), [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L330-L330), [367-367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L367-L367), [464-464](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L464-L464), [637-637](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L637-L637) ):

```solidity
180:         stakingToken.safeTransfer(msg.sender, amount);

330:         tokenAddress.safeTransfer(owner, tokenAmount);

367:         rewardToken.safeTransferFrom(msg.sender, address(this), amount);

464:         stakingToken.safeTransferFrom(msg.sender, address(this), amount);

637:                         rewardToken.safeTransfer(user, amount);
```

</details>

### [L-20] Functions calling contracts/addresses with transfer hooks should be protected by reentrancy guard

Even if the function follows the best practice of check-effects-interaction, not using a reentrancy guard when there may be transfer hooks opens the users of this protocol up to [read-only reentrancy vulnerability](https://chainsecurity.com/curve-lp-oracle-manipulation-post-mortem/) with no way to protect them except by block-listing the entire protocol.

<details>
<summary>There are 34 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [102-102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L102-L102), [138-138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L138-L138), [210-210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L210-L210) ):

```solidity
102:         token.safeTransferFrom(msg.sender, address(this), amount);

138:         token.safeTransfer(msg.sender, amount);

210:         token.safeTransfer(to, amount);
```

- *MagicLP.sol* ( [466-466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L466-L466), [583-583](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L583-L583), [589-589](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L589-L589) ):

```solidity
466:         token.safeTransfer(to, amount);

583:             _BASE_TOKEN_.safeTransfer(to, amount);

589:             _QUOTE_TOKEN_.safeTransfer(to, amount);
```

- *Router.sol* ( [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L68-L68), [69-69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L69-L69), [91-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L91-L91), [172-172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L172-L172), [173-173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L173-L173), [186-186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L186-L186), [187-187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L187-L187), [224-224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L224-L224), [246-246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L246-L246), [269-269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L269-L269), [282-282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L282-L282), [311-311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L311-L311), [328-328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L328-L328), [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L330-L330), [360-360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L360-L360), [393-393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L393-L393), [395-395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L395-L395), [411-411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L411-L411), [428-428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L428-L428), [443-443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L443-L443), [456-456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L456-L456), [474-474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L474-L474), [489-489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L489-L489) ):

```solidity
68:         baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);

69:         quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);

91:         token.safeTransferFrom(msg.sender, clone, tokenInAmount);

172:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);

173:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);

186:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);

187:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);

224:         token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);

246:         token.safeTransferFrom(msg.sender, lp, tokenInAmount);

269:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

282:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

311:         token.safeTransfer(to, tokenAmountOut);

328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

360:         inToken.safeTransfer(address(firstLp), msg.value);

393:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

395:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

411:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

428:         baseToken.safeTransfer(lp, msg.value);

443:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

456:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

474:         quoteToken.safeTransfer(lp, msg.value);

489:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
```

- *LockingMultiRewards.sol* ( [180-180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L180-L180), [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L330-L330), [367-367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L367-L367), [464-464](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L464-L464), [637-637](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L637-L637) ):

```solidity
180:         stakingToken.safeTransfer(msg.sender, amount);

330:         tokenAddress.safeTransfer(owner, tokenAmount);

367:         rewardToken.safeTransferFrom(msg.sender, address(this), amount);

464:         stakingToken.safeTransferFrom(msg.sender, address(this), amount);

637:                         rewardToken.safeTransfer(user, amount);
```

</details>

### [L-21] Critical functions should be controlled by time locks

It is a good practice to give time for users to react and adjust to critical changes. A timelock provides more guarantees and reduces the level of trust required, thus decreasing risk for users. It also indicates that the project is legitimate (less risk of a malicious owner making a sandwich attack on a user).

<details>
<summary>There are 26 instances (click to show):</summary>

- *BlastBox.sol* ( [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L72-L72), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L81-L81) ):

```solidity
72:     function setFeeTo(address feeTo_) external onlyOwner {

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {
```

- *BlastGovernor.sol* ( [40-40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L40-L40) ):

```solidity
40:     function setFeeTo(address _feeTo) external onlyOwner {
```

- *BlastMagicLP.sol* ( [80-80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L80-L80), [89-89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L89-L89) ):

```solidity
80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```

- *BlastOnboarding.sol* ( [147-147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L147-L147), [175-175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L175-L175), [185-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L185-L185), [190-190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L190-L190) ):

```solidity
147:     function setFeeTo(address feeTo_) external onlyOwner {

175:     function setTokenSupported(address token, bool supported) external onlyOwner {

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {
```

- *BlastOnboardingBoot.sol* ( [137-137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L137-L137) ):

```solidity
137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {
```

- *BlastTokenRegistry.sol* ( [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L14-L14) ):

```solidity
14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```

- *MagicLP.sol* ( [470-479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L470-L479) ):

```solidity
470:     function setParameters(
471:         address assetTo,
472:         uint256 newLpFeeRate,
473:         uint256 newI,
474:         uint256 newK,
475:         uint256 baseOutAmount,
476:         uint256 quoteOutAmount,
477:         uint256 minBaseReserve,
478:         uint256 minQuoteReserve
479:     ) public nonReentrant onlyImplementationOwner {
```

- *FeeRateModel.sol* ( [46-46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L46-L46), [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L57-L57) ):

```solidity
46:     function setMaintainer(address maintainer_) external onlyOwner {

57:     function setImplementation(address implementation_) public onlyOwner {
```

- *Factory.sol* ( [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L96-L96), [105-105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L105-L105), [116-116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L116-L116), [120-126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L120-L126) ):

```solidity
96:     function setLpImplementation(address implementation_) external onlyOwner {

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

116:     function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {

120:     function removePool(
121:         address creator,
122:         address baseToken,
123:         address quoteToken,
124:         uint256 poolIndex,
125:         uint256 userPoolIndex
126:     ) external onlyOwner {
```

- *Router.sol* ( [162-169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L162-L169), [178-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L178-L185), [192-199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L192-L199), [229-235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L229-L235), [261-268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L261-L268), [274-281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L274-L281), [499-499](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L499-L499) ):

```solidity
162:     function addLiquidity(
163:         address lp,
164:         address to,
165:         uint256 baseInAmount,
166:         uint256 quoteInAmount,
167:         uint256 minimumShares,
168:         uint256 deadline
169:     ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

178:     function addLiquidityUnsafe(
179:         address lp,
180:         address to,
181:         uint256 baseInAmount,
182:         uint256 quoteInAmount,
183:         uint256 minimumShares,
184:         uint256 deadline
185:     ) external ensureDeadline(deadline) returns (uint256 shares) {

192:     function addLiquidityETH(
193:         address lp,
194:         address to,
195:         address payable refundTo,
196:         uint256 tokenInAmount,
197:         uint256 minimumShares,
198:         uint256 deadline
199:     ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

229:     function addLiquidityETHUnsafe(
230:         address lp,
231:         address to,
232:         uint256 tokenInAmount,
233:         uint256 minimumShares,
234:         uint256 deadline
235:     ) external payable ensureDeadline(deadline) returns (uint256 shares) {

261:     function removeLiquidity(
262:         address lp,
263:         address to,
264:         uint256 sharesIn,
265:         uint256 minimumBaseAmount,
266:         uint256 minimumQuoteAmount,
267:         uint256 deadline
268:     ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

274:     function removeLiquidityETH(
275:         address lp,
276:         address to,
277:         uint256 sharesIn,
278:         uint256 minimumETHAmount,
279:         uint256 minimumTokenAmount,
280:         uint256 deadline
281:     ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {

499:     function _addLiquidity(address lp, address to, uint256 minimumShares) internal returns (uint256 shares) {
```

- *LockingMultiRewards.sol* ( [300-300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L300-L300) ):

```solidity
300:     function addReward(address rewardToken) public onlyOwner {
```

</details>

### [L-22] Missing contract existence checks before low-level calls

Low-level calls return success if there is no code present at the specified address. In addition to the zero-address checks, add a check to verify that `<address>.code.length > 0`.

There is 1 instance:

- *BlastGovernor.sol* ( [54-54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L54-L54) ):

```solidity
54:         (success, result) = to.call{value: value}(data);
```

### [L-23] External function calls within loops

Calling external functions within loops can easily result in insufficient gas. This greatly increases the likelihood of transaction failures, DOS attacks, and other unexpected actions. It is recommended to limit the number of loops within loops that call external functions, and to limit the gas line for each external call.

There are 5 instances:

- *BlastOnboarding.sol* ( [169-169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L169-L169), [170-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L170-L170) ):

```solidity
/// @audit Calling `nativeYieldTokens()` within `for` loop
169:             if (registry.nativeYieldTokens(tokens[i])) {

/// @audit Calling `claimAllTokenYields()` within `for` loop, it will trigger an external call - `claim()`
170:                 BlastYields.claimAllTokenYields(tokens[i], feeTo);
```

- *Router.sol* ( [547-547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L547-L547), [550-550](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L550-L550) ):

```solidity
/// @audit Calling `sellBase()` within `for` loop
547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));

/// @audit Calling `sellQuote()` within `for` loop
550:                 IMagicLP(path[i]).sellQuote(address(path[i + 1]));
```

- *LockingMultiRewards.sol* ( [637-637](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L637-L637) ):

```solidity
/// @audit Calling `safeTransfer()` within `for` loop
637:                         rewardToken.safeTransfer(user, amount);
```

### [L-24] Tokens may be minted to the zero address

Neither the listed functions, nor `_mint()` prevent minting to `address(0x0)`

There are 3 instances:

- *MagicLP.sol* ( [393-393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L393-L393), [406-406](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L406-L406), [593-593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L593-L593) ):

```solidity
393:             _mint(address(0), 1001);

406:         _mint(to, shares);

593:     function _mint(address to, uint256 amount) internal override {
```

### [L-25] Sending tokens within loops

Performing token transfers in a loop is not recommended due to the "Fail-Silently" issue. If one transfer fails, the entire transaction fails, which can be problematic when dealing with multiple transfers. This can prevent subsequent recipients from receiving their transfers. Additionally, it can be exploited by malicious contracts to disrupt transfers. To mitigate this, the "withdraw pattern" is recommended, where each recipient triggers their own payment, separating transfer operations and reducing the chance of interference.

<details>
<summary>There is 1 instance (click to show):</summary>

- *LockingMultiRewards.sol* ( [614-656](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L614-L656) ):

```solidity
614:         for (uint256 i; i < rewardTokens.length; ) {
615:             address rewardToken = rewardTokens[i];
616:             uint256 rewardAmount = rewards[user][rewardToken];
617: 
618:             // in all scenario, reset the reward amount immediately
619:             rewards[user][rewardToken] = 0;
620: 
621:             // don't assume the rewardTokens array is always the same length as the items array
622:             // as new reward tokens can be added by the owner
623:             if (i < rewardItemLength) {
624:                 RewardLockItem storage item = _rewardLock.items[i];
625: 
626:                 // expired lock, claim existing unlocked rewards if any
627:                 if (expired) {
628:                     uint256 amount = item.amount;
629: 
630:                     // since this current lock is expired and that item index
631:                     // matches the reward index, override the current amount
632:                     // with the new locked amount.
633:                     item.amount = rewardAmount;
634: 
635:                     // use cached amount
636:                     if (amount > 0) {
637:                         rewardToken.safeTransfer(user, amount);
638:                         emit LogRewardPaid(user, rewardToken, amount);
639:                     }
640:                 } else {
641:                     // not expired, just add to the existing lock
642:                     item.amount += rewardAmount;
643:                 }
644:             }
645:             // new reward token, create a new lock item
646:             // could mean it's adding to an existing lock or creating a new one
647:             else {
648:                 _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
649:             }
650: 
651:             emit LogRewardLocked(user, rewardToken, rewardAmount);
652: 
653:             unchecked {
654:                 ++i;
655:             }
656:         }
```

</details>

### [L-26] Some tokens may revert when zero value transfers are made

Despite the fact that [EIP-20 states](https://github.com/ethereum/EIPs/blob/7500ac4fc1bbdfaf684e7ef851f798f6b667b2fe/EIPS/eip-20.md?plain=1#L116) that zero-value transfers must be accepted, some tokens, such as LEND, will revert if this is attempted, which may cause transactions that involve other tokens (such as batch operations) to fully revert. Consider skipping the transfer if the amount is zero, which will also save gas.

<details>
<summary>There are 27 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [102-102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L102-L102), [138-138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L138-L138), [210-210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L210-L210) ):

```solidity
102:         token.safeTransferFrom(msg.sender, address(this), amount);

138:         token.safeTransfer(msg.sender, amount);

210:         token.safeTransfer(to, amount);
```

- *MagicLP.sol* ( [466-466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L466-L466) ):

```solidity
466:         token.safeTransfer(to, amount);
```

- *Router.sol* ( [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L68-L68), [69-69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L69-L69), [91-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L91-L91), [172-172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L172-L172), [173-173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L173-L173), [186-186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L186-L186), [187-187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L187-L187), [224-224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L224-L224), [246-246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L246-L246), [311-311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L311-L311), [328-328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L328-L328), [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L330-L330), [360-360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L360-L360), [393-393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L393-L393), [395-395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L395-L395), [411-411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L411-L411), [428-428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L428-L428), [443-443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L443-L443), [456-456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L456-L456), [474-474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L474-L474), [489-489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L489-L489) ):

```solidity
68:         baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);

69:         quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);

91:         token.safeTransferFrom(msg.sender, clone, tokenInAmount);

172:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);

173:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);

186:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);

187:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);

224:         token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);

246:         token.safeTransferFrom(msg.sender, lp, tokenInAmount);

311:         token.safeTransfer(to, tokenAmountOut);

328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

360:         inToken.safeTransfer(address(firstLp), msg.value);

393:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

395:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

411:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

428:         baseToken.safeTransfer(lp, msg.value);

443:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

456:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

474:         quoteToken.safeTransfer(lp, msg.value);

489:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
```

- *LockingMultiRewards.sol* ( [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L330-L330), [367-367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L367-L367) ):

```solidity
330:         tokenAddress.safeTransfer(owner, tokenAmount);

367:         rewardToken.safeTransferFrom(msg.sender, address(this), amount);
```

</details>

### [L-27] Use `SafeCast` to downcast safely

When a type is downcast to a smaller type, the higher order bits are truncated, effectively applying a modulo to the original value. The loss of data may cause incorrect calculations, unexpected state changes, or other unexpected behavior.
It is recommended to use the [SafeCast library](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/utils/math/SafeCast.sol).

There are 6 instances:

- *MagicLP.sol* ( [125-125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L125-L125), [438-438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L438-L438), [439-439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L439-L439), [513-513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L513-L513), [517-517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L517-L517), [546-546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L546-L546) ):

```solidity
/// @audit uint256 -> uint32
125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

/// @audit uint256 -> uint112
438:         _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));

/// @audit uint256 -> uint112
439:         _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));

/// @audit uint256 -> uint112
513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

/// @audit uint256 -> uint112
517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));

/// @audit uint256 -> uint32
546:         uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
```

### [L-28] Use descriptive constant instead of 0 as a parameter

Passing `0` or `0x0` as a function argument can sometimes result in a security issue(e.g. passing zero as the slippage parameter). A historical example is the infamous `0x0` address bug where numerous tokens were lost. This happens because `0` can be interpreted as an uninitialized `address`, leading to transfers to the `0x0` `address`, effectively burning tokens. Moreover, `0` as a denominator in division operations would cause a runtime exception. It's also often indicative of a logical error in the caller's code.

Consider using a constant variable with a descriptive name, so it's clear that the argument is intentionally being used, and for the right reasons.

There is 1 instance:

- *MagicLP.sol* ( [393-393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L393-L393) ):

```solidity
393:             _mint(address(0), 1001);
```

### [L-29] Large approvals may not work with some `ERC20` tokens

Some tokens such as [COMP](https://github.com/compound-finance/compound-protocol/blob/a3214f67b73310d547e00fc578e8355911c9d376/contracts/Governance/Comp.sol#L89-L91) downcast such approvals to `uint96` and use that as a raw value rather than interpreting it as an infinite approval. Eventually these approvals will reach zero, at which point the calling contract will no longer function properly.

There are 3 instances:

- *BlastOnboardingBoot.sol* ( [103-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L103-L103), [104-104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L104-L104), [122-122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L122-L122) ):

```solidity
103:         MIM.safeApprove(address(router), type(uint256).max);

104:         USDB.safeApprove(address(router), type(uint256).max);

122:         pool.safeApprove(address(staking), totalPoolShares);
```

### [L-30] Code does not follow the best practice of check-effects-interaction

Code should follow the best-practice of [check-effects-interaction](https://blockchain-academy.hs-mittweida.de/courses/solidity-coding-beginners-to-intermediate/lessons/solidity-11-coding-patterns/topic/checks-effects-interactions/), where state variables are updated before any external calls are made. Doing so prevents a large class of reentrancy bugs.

<details>
<summary>There are 38 instances (click to show):</summary>

- *BlastBox.sol* ( [61-61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L61-L61) ):

```solidity
/// @audit `nativeYieldTokens()` is called on line 57
61:         amount = BlastYields.claimAllTokenYields(token_, feeTo);
```

- *BlastMagicLP.sol* ( [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L57-L57), [60-60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L60-L60) ):

```solidity
/// @audit `feeTo()` is called on line 54
57:             token0Amount = BlastYields.claimAllTokenYields(_BASE_TOKEN_, feeTo_);

/// @audit `feeTo()` is called on line 54
60:             token1Amount = BlastYields.claimAllTokenYields(_QUOTE_TOKEN_, feeTo_);
```

- *BlastOnboarding.sol* ( [105-105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L105-L105), [106-106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L106-L106), [108-108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L108-L108), [109-109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L109-L109), [112-112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L112-L112), [118-118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L118-L118) ):

```solidity
/// @audit `safeTransferFrom()` is called on line 102
105:             totals[token].locked += amount;

/// @audit `safeTransferFrom()` is called on line 102
106:             balances[msg.sender][token].locked += amount;

/// @audit `safeTransferFrom()` is called on line 102
108:             totals[token].unlocked += amount;

/// @audit `safeTransferFrom()` is called on line 102
109:             balances[msg.sender][token].unlocked += amount;

/// @audit `safeTransferFrom()` is called on line 102
112:         totals[token].total += amount;

/// @audit `safeTransferFrom()` is called on line 102
118:         balances[msg.sender][token].total += amount;
```

- *BlastOnboardingBoot.sol* ( [106-106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L106-L106), [117-117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L117-L117) ):

```solidity
/// @audit `safeApprove()` is called on line 103
106:         (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

/// @audit `safeApprove()` is called on line 103
117:         staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
```

- *MagicLP.sol* ( [257-257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L257-L257), [258-258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L258-L258), [280-280](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L280-L280), [281-281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L281-L281), [321-321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L321-L321), [322-322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L322-L322), [343-343](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L343-L343), [344-344](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L344-L344) ):

```solidity
/// @audit `_transferQuoteOut()` is called on line 252, triggering an external call - `safeTransfer()`
257:             _BASE_TARGET_ = newBaseTarget.toUint112();

/// @audit `_transferQuoteOut()` is called on line 252, triggering an external call - `safeTransfer()`
258:             _RState_ = uint32(newRState);

/// @audit `_transferBaseOut()` is called on line 275, triggering an external call - `safeTransfer()`
280:             _QUOTE_TARGET_ = newQuoteTarget.toUint112();

/// @audit `_transferBaseOut()` is called on line 275, triggering an external call - `safeTransfer()`
281:             _RState_ = uint32(newRState);

/// @audit `_transferBaseOut()` is called on line 291, triggering an external call - `safeTransfer()`
321:                 _QUOTE_TARGET_ = newQuoteTarget.toUint112();

/// @audit `_transferBaseOut()` is called on line 291, triggering an external call - `safeTransfer()`
322:                 _RState_ = uint32(newRState);

/// @audit `_transferBaseOut()` is called on line 291, triggering an external call - `safeTransfer()`
343:                 _BASE_TARGET_ = newBaseTarget.toUint112();

/// @audit `_transferBaseOut()` is called on line 291, triggering an external call - `safeTransfer()`
344:                 _RState_ = uint32(newRState);
```

- *Router.sol* ( [70-70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L70-L70), [93-93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L93-L93), [175-175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L175-L175), [226-226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L226-L226), [286-286](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L286-L286), [287-294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L287-L294), [296-303](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L296-L303), [444-444](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L444-L444), [490-490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L490-L490) ):

```solidity
/// @audit `safeTransferFrom()` is called on line 68
70:         (shares, , ) = IMagicLP(clone).buyShares(to);

/// @audit `deposit()` is called on line 90
93:         (shares, , ) = IMagicLP(clone).buyShares(to);

/// @audit `safeTransferFrom()` is called on line 172
175:         shares = _addLiquidity(lp, to, minimumShares);

/// @audit `_BASE_TOKEN_()` is called on line 202
226:         shares = _addLiquidity(lp, to, minimumShares);

/// @audit `safeTransferFrom()` is called on line 282
286:             token = IMagicLP(lp)._QUOTE_TOKEN_();

/// @audit `safeTransferFrom()` is called on line 282
287:             (ethAmountOut, tokenAmountOut) = IMagicLP(lp).sellShares(
288:                 sharesIn,
289:                 address(this),
290:                 minimumETHAmount,
291:                 minimumTokenAmount,
292:                 "",
293:                 deadline
294:             );

/// @audit `safeTransferFrom()` is called on line 282
296:             (tokenAmountOut, ethAmountOut) = IMagicLP(lp).sellShares(
297:                 sharesIn,
298:                 address(this),
299:                 minimumTokenAmount,
300:                 minimumETHAmount,
301:                 "",
302:                 deadline
303:             );

/// @audit `safeTransferFrom()` is called on line 443
444:         amountOut = _sellBase(lp, address(this), minimumOut);

/// @audit `safeTransferFrom()` is called on line 489
490:         amountOut = _sellQuote(lp, address(this), minimumOut);
```

- *LockingMultiRewards.sol* ( [181-181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L181-L181), [380-380](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L380-L380), [388-388](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L388-L388), [389-389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L389-L389), [390-390](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L390-L390), [465-465](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L465-L465), [472-472](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L472-L472), [473-473](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L473-L473), [642-642](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L642-L642), [654-654](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L654-L654) ):

```solidity
/// @audit `safeTransfer()` is called on line 180
181:         stakingTokenBalance -= amount;

/// @audit `safeTransferFrom()` is called on line 367
380:             amount += _remainingRewardTime * reward.rewardRate;

/// @audit `safeTransferFrom()` is called on line 367
388:         reward.rewardRate = amount / _remainingRewardTime;

/// @audit `safeTransferFrom()` is called on line 367
389:         reward.lastUpdateTime = uint248(block.timestamp);

/// @audit `safeTransferFrom()` is called on line 367
390:         reward.periodFinish = _nextEpoch;

/// @audit `safeTransferFrom()` is called on line 464
465:         stakingTokenBalance += amount;

/// @audit `safeTransferFrom()` is called on line 464
472:             _balances[account].unlocked += amount;

/// @audit `safeTransferFrom()` is called on line 464
473:             unlockedSupply += amount;

/// @audit `safeTransfer()` is called on line 637
642:                     item.amount += rewardAmount;

/// @audit `safeTransfer()` is called on line 637
654:                 ++i;
```

</details>

### [L-31] Some tokens may revert when large transfers are made

Tokens such as COMP or UNI will revert when an address' balance reaches [`type(uint96).max`](https://github.com/compound-finance/compound-protocol/blob/a3214f67b73310d547e00fc578e8355911c9d376/contracts/Governance/Comp.sol#L238). Ensure that the calls below can be broken up into smaller batches if necessary.

<details>
<summary>There are 32 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [102-102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L102-L102), [138-138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L138-L138), [210-210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L210-L210) ):

```solidity
102:         token.safeTransferFrom(msg.sender, address(this), amount);

138:         token.safeTransfer(msg.sender, amount);

210:         token.safeTransfer(to, amount);
```

- *MagicLP.sol* ( [466-466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L466-L466), [583-583](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L583-L583), [589-589](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L589-L589) ):

```solidity
466:         token.safeTransfer(to, amount);

583:             _BASE_TOKEN_.safeTransfer(to, amount);

589:             _QUOTE_TOKEN_.safeTransfer(to, amount);
```

- *Router.sol* ( [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L68-L68), [69-69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L69-L69), [91-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L91-L91), [172-172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L172-L172), [173-173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L173-L173), [186-186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L186-L186), [187-187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L187-L187), [224-224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L224-L224), [246-246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L246-L246), [311-311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L311-L311), [328-328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L328-L328), [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L330-L330), [360-360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L360-L360), [393-393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L393-L393), [395-395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L395-L395), [411-411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L411-L411), [428-428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L428-L428), [443-443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L443-L443), [456-456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L456-L456), [474-474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L474-L474), [489-489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L489-L489) ):

```solidity
68:         baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);

69:         quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);

91:         token.safeTransferFrom(msg.sender, clone, tokenInAmount);

172:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);

173:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);

186:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);

187:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);

224:         token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);

246:         token.safeTransferFrom(msg.sender, lp, tokenInAmount);

311:         token.safeTransfer(to, tokenAmountOut);

328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

360:         inToken.safeTransfer(address(firstLp), msg.value);

393:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

395:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

411:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

428:         baseToken.safeTransfer(lp, msg.value);

443:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

456:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

474:         quoteToken.safeTransfer(lp, msg.value);

489:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
```

- *LockingMultiRewards.sol* ( [180-180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L180-L180), [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L330-L330), [367-367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L367-L367), [464-464](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L464-L464), [637-637](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L637-L637) ):

```solidity
180:         stakingToken.safeTransfer(msg.sender, amount);

330:         tokenAddress.safeTransfer(owner, tokenAmount);

367:         rewardToken.safeTransferFrom(msg.sender, address(this), amount);

464:         stakingToken.safeTransferFrom(msg.sender, address(this), amount);

637:                         rewardToken.safeTransfer(user, amount);
```

</details>

### [L-32] `unchecked` blocks with additions/multiplications may overflow

There aren't any checks to avoid an overflow which can happen inside an `unchecked` block, so the following calculations may overflow silently.

There are 3 instances:

- *MagicLP.sol* ( [553-553](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L553-L553), [553-553](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L553-L553) ):

```solidity
553:                 _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;

553:                 _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
```

- *LockingMultiRewards.sol* ( [505-505](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L505-L505) ):

```solidity
505:                 ++lockCount;
```

### [L-33] Contracts are vulnerable to rebasing accounting-related issues

Rebasing tokens are tokens that have each holder's `balanceof()` increase over time. Aave aTokens are an example of such tokens. If rebasing tokens are used, rewards accrue to the contract holding the tokens, and cannot be withdrawn by the original depositor. To address the issue, track 'shares' deposited on a pro-rata basis, and let shares be redeemed for their proportion of the current balance at the time of the withdrawal.

<details>
<summary>There are 22 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [101-101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L101-L101), [132-132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L132-L132), [205-205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L205-L205) ):

```solidity
101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {

205:     function rescue(address token, address to, uint256 amount) external onlyOwner {
```

- *MagicLP.sol* ( [461-461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L461-L461), [581-581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L581-L581), [587-587](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L587-L587) ):

```solidity
461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {

581:     function _transferBaseOut(address to, uint256 amount) internal {

587:     function _transferQuoteOut(address to, uint256 amount) internal {
```

- *Router.sol* ( [54-63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L54-L63), [162-169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L162-L169), [178-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L178-L185), [314-321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L314-L321), [336-342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L336-L342), [365-372](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L365-L372), [404-410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L404-L410), [415-420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L415-L420), [432-438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L432-L438), [449-455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L449-L455), [461-466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L461-L466), [478-484](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L478-L484) ):

```solidity
54:     function createPool(
55:         address baseToken,
56:         address quoteToken,
57:         uint256 lpFeeRate,
58:         uint256 i,
59:         uint256 k,
60:         address to,
61:         uint256 baseInAmount,
62:         uint256 quoteInAmount
63:     ) external returns (address clone, uint256 shares) {

162:     function addLiquidity(
163:         address lp,
164:         address to,
165:         uint256 baseInAmount,
166:         uint256 quoteInAmount,
167:         uint256 minimumShares,
168:         uint256 deadline
169:     ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

178:     function addLiquidityUnsafe(
179:         address lp,
180:         address to,
181:         uint256 baseInAmount,
182:         uint256 quoteInAmount,
183:         uint256 minimumShares,
184:         uint256 deadline
185:     ) external ensureDeadline(deadline) returns (uint256 shares) {

314:     function swapTokensForTokens(
315:         address to,
316:         uint256 amountIn,
317:         address[] calldata path,
318:         uint256 directions,
319:         uint256 minimumOut,
320:         uint256 deadline
321:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

336:     function swapETHForTokens(
337:         address to,
338:         address[] calldata path,
339:         uint256 directions,
340:         uint256 minimumOut,
341:         uint256 deadline
342:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

365:     function swapTokensForETH(
366:         address to,
367:         uint256 amountIn,
368:         address[] calldata path,
369:         uint256 directions,
370:         uint256 minimumOut,
371:         uint256 deadline
372:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

404:     function sellBaseTokensForTokens(
405:         address lp,
406:         address to,
407:         uint256 amountIn,
408:         uint256 minimumOut,
409:         uint256 deadline
410:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

415:     function sellBaseETHForTokens(
416:         address lp,
417:         address to,
418:         uint256 minimumOut,
419:         uint256 deadline
420:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

432:     function sellBaseTokensForETH(
433:         address lp,
434:         address to,
435:         uint256 amountIn,
436:         uint256 minimumOut,
437:         uint256 deadline
438:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

449:     function sellQuoteTokensForTokens(
450:         address lp,
451:         address to,
452:         uint256 amountIn,
453:         uint256 minimumOut,
454:         uint256 deadline
455:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

461:     function sellQuoteETHForTokens(
462:         address lp,
463:         address to,
464:         uint256 minimumOut,
465:         uint256 deadline
466:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

478:     function sellQuoteTokensForETH(
479:         address lp,
480:         address to,
481:         uint256 amountIn,
482:         uint256 minimumOut,
483:         uint256 deadline
484:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {
```

- *LockingMultiRewards.sol* ( [170-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L170-L170), [361-361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L361-L361), [458-458](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L458-L458), [597-597](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L597-L597) ):

```solidity
170:     function withdraw(uint256 amount) public virtual {

361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {

458:     function _stakeFor(address account, uint256 amount, bool lock_) internal {

597:     function _getRewards(address user) internal {
```

</details>

## Non Critical Issues

### [N-01] Visibility of state variables is not explicitly defined

To avoid misunderstandings and unexpected state accesses, it is recommended to explicitly define the visibility of each state variable.

There is 1 instance:

- *BlastYields.sol* ( [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L14-L14) ):

```solidity
14:     IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);
```

### [N-02] Names of `private`/`internal` functions should be prefixed with an underscore

It is recommended by the [Solidity Style Guide](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#underscore-prefix-for-non-external-functions-and-variables).

<details>
<summary>There are 25 instances (click to show):</summary>

- *BlastBox.sol* ( [103-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L103-L103) ):

```solidity
103:     function isOwner(address _account) internal view override returns (bool) {
```

- *BlastPoints.sol* ( [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L10-L10) ):

```solidity
10:     function configure() internal {
```

- *BlastYields.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L20-L20), [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L29-L29), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L38-L38), [42-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L42-L42), [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L51-L51), [55-55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L55-L55), [60-60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L60-L60), [70-70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L70-L70), [75-75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L75-L75), [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L86-L86) ):

```solidity
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

- *DecimalMath.sol* ( [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L23-L23), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L27-L27), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L31-L31), [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L35-L35), [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L39-L39), [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L43-L43), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L47-L47) ):

```solidity
23:     function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {

27:     function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {

31:     function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {

35:     function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {

39:     function reciprocalFloor(uint256 target) internal pure returns (uint256) {

43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {

47:     function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```

- *Math.sol* ( [19-19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L19-L19), [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L29-L29) ):

```solidity
19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

29:     function sqrt(uint256 x) internal pure returns (uint256 y) {
```

- *PMMPricing.sol* ( [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L39-L39), [76-76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L76-L76), [190-190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L190-L190), [203-203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L203-L203) ):

```solidity
39:     function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {

76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {

190:     function adjustedTarget(PMMState memory state) internal pure {

203:     function getMidPrice(PMMState memory state) internal pure returns (uint256) {
```

</details>

### [N-03] Names of `private`/`internal` state variables should be prefixed with an underscore

It is recommended by the [Solidity Style Guide](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#underscore-prefix-for-non-external-functions-and-variables).

There are 4 instances:

- *LockingMultiRewards.sol* ( [78-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L78-L78), [79-79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L79-L79), [80-80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L80-L80), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L81-L81) ):

```solidity
78:     uint256 private constant BIPS = 10_000;

79:     uint256 private constant MAX_NUM_REWARDS = 5;

80:     uint256 private constant MIN_LOCK_DURATION = 1 weeks;

81:     uint256 private constant MIN_REWARDS_DURATION = 1 days;
```

### [N-04] Order of functions does not follow the Solidity Style Guide

According to the [Solidity Style Guide](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#order-of-functions), functions should be grouped according to their visibility and ordered: `constructor`, `receive`, `fallback`, `external`, `public`, `internal`, `private`. Within a grouping, place the view and pure functions last.

<details>
<summary>There are 65 instances (click to show):</summary>

- *BlastBox.sol* ( [36-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L36-L42), [52-52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L52-L52) ):

```solidity
/// @audit ↓↓ Out of order with `claimGasYields()`
36:     function _onBeforeDeposit(
37:         IERC20 token,
38:         address /*from*/,
39:         address /*to*/,
40:         uint256 /*amount*/,
41:         uint256 /*share*/
42:     ) internal view override {

/// @audit ↑↑ Out of order with `_onBeforeDeposit()`
52:     function claimGasYields() external onlyOperators returns (uint256) {
```

- *BlastGovernor.sol* ( [13-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L13-L13), [15-15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L15-L15) ):

```solidity
/// @audit ↓↓ Out of order with `constructor()`
13:     receive() external payable {}

/// @audit ↑↑ Out of order with `receive()`
15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```

- *BlastOnboarding.sol* ( [80-80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L80-L80), [84-84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L84-L84) ):

```solidity
/// @audit ↓↓ Out of order with `constructor()`
80:     receive() external payable override {

/// @audit ↑↑ Out of order with `receive()`
84:     constructor(BlastTokenRegistry registry_, address feeTo_) {
```

- *BlastOnboardingBoot.sol* ( [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L86-L86), [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L96-L96), [129-129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L129-L129), [137-137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L137-L137), [146-146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L146-L146) ):

```solidity
/// @audit ↓↓ Out of order with `bootstrap()`
86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

/// @audit ↑↑ Out of order with `previewTotalPoolShares()`
96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {

/// @audit ↑↑ Out of order with `bootstrap()`
129:     function initialize(Router _router) external onlyOwner {

/// @audit ↑↑ Out of order with `initialize()`
137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

/// @audit ↑↑ Out of order with `setStaking()`
146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
```

- *MagicLP.sol* ( [193-193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L193-L193), [204-204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204-L204), [215-215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L215-L215), [219-219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L219-L219), [232-232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L232-L232), [236-236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L236-L236), [244-244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L244-L244), [267-267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L267-L267), [290-290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L290-L290), [360-360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L360-L360), [413-420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L413-L420), [461-461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L461-L461), [470-479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L470-L479), [504-504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L504-L504), [528-528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L528-L528), [545-545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L545-L545), [560-560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L560-L560), [567-567](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L567-L567), [581-581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L581-L581), [587-587](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L587-L587), [593-593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L593-L593), [601-601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L601-L601) ):

```solidity
/// @audit ↓↓ Out of order with `getPMMStateForCall()`
193:     function getPMMState() public view returns (PMMPricing.PMMState memory state) {

/// @audit ↑↑ Out of order with `getPMMState()`
204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

/// @audit ↓↓ Out of order with `getReserves()`
215:     function getMidPrice() public view returns (uint256 midPrice) {

/// @audit ↑↑ Out of order with `getMidPrice()`
219:     function getReserves() external view returns (uint256 baseReserve, uint256 quoteReserve) {

/// @audit ↓↓ Out of order with `version()`
232:     function getQuoteInput() public view returns (uint256 input) {

/// @audit ↑↑ Out of order with `getQuoteInput()`
236:     function version() external pure virtual returns (string memory) {

/// @audit ↑↑ Out of order with `version()`
244:     function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {

/// @audit ↑↑ Out of order with `sellBase()`
267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

/// @audit ↑↑ Out of order with `sellQuote()`
290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

/// @audit ↑↑ Out of order with `flashLoan()`
360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {

/// @audit ↑↑ Out of order with `buyShares()`
413:     function sellShares(
414:         uint256 shareAmount,
415:         address to,
416:         uint256 baseMinAmount,
417:         uint256 quoteMinAmount,
418:         bytes calldata data,
419:         uint256 deadline
420:     ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {

/// @audit ↑↑ Out of order with `sellShares()`
461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {

/// @audit ↓↓ Out of order with `ratioSync()`
470:     function setParameters(
471:         address assetTo,
472:         uint256 newLpFeeRate,
473:         uint256 newI,
474:         uint256 newK,
475:         uint256 baseOutAmount,
476:         uint256 quoteOutAmount,
477:         uint256 minBaseReserve,
478:         uint256 minQuoteReserve
479:     ) public nonReentrant onlyImplementationOwner {

/// @audit ↑↑ Out of order with `setParameters()`
504:     function ratioSync() external nonReentrant onlyImplementationOwner {

/// @audit ↓↓ Out of order with `_twapUpdate()`
528:     function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {

/// @audit ↑↑ Out of order with `_resetTargetAndReserve()`
545:     function _twapUpdate() internal {

/// @audit ↑↑ Out of order with `_twapUpdate()`
560:     function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {

/// @audit ↑↑ Out of order with `_setReserve()`
567:     function _sync() internal {

/// @audit ↑↑ Out of order with `_sync()`
581:     function _transferBaseOut(address to, uint256 amount) internal {

/// @audit ↑↑ Out of order with `_transferBaseOut()`
587:     function _transferQuoteOut(address to, uint256 amount) internal {

/// @audit ↑↑ Out of order with `_transferQuoteOut()`
593:     function _mint(address to, uint256 amount) internal override {

/// @audit ↑↑ Out of order with `_mint()`
601:     function _afterInitialized() internal virtual {}
```

- *Factory.sol* ( [65-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L65-L72), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81-L81), [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L96-L96), [105-105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L105-L105), [116-116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L116-L116), [120-126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L120-L126) ):

```solidity
/// @audit ↓↓ Out of order with `create()`
65:     function predictDeterministicAddress(
66:         address creator,
67:         address baseToken_,
68:         address quoteToken_,
69:         uint256 lpFeeRate_,
70:         uint256 i_,
71:         uint256 k_
72:     ) public view returns (address) {

/// @audit ↑↑ Out of order with `predictDeterministicAddress()`
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

/// @audit ↑↑ Out of order with `create()`
96:     function setLpImplementation(address implementation_) external onlyOwner {

/// @audit ↑↑ Out of order with `setLpImplementation()`
105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

/// @audit ↑↑ Out of order with `setMaintainerFeeRateModel()`
116:     function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {

/// @audit ↑↑ Out of order with `addPool()`
120:     function removePool(
121:         address creator,
122:         address baseToken,
123:         address quoteToken,
124:         uint256 poolIndex,
125:         uint256 userPoolIndex
126:     ) external onlyOwner {
```

- *Router.sol* ( [36-36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L36-L36), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L38-L38), [112-116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L112-L116), [162-169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L162-L169), [178-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L178-L185), [192-199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L192-L199), [229-235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L229-L235), [251-251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L251-L251), [261-268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L261-L268), [274-281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L274-L281), [314-321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L314-L321), [336-342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L336-L342), [365-372](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L365-L372), [404-410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L404-L410), [415-420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L415-L420), [432-438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L432-L438), [449-455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L449-L455), [461-466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L461-L466), [478-484](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L478-L484), [509-513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L509-L513), [541-541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L541-L541), [571-571](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L571-L571), [578-578](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L578-L578) ):

```solidity
/// @audit ↓↓ Out of order with `constructor()`
36:     receive() external payable {}

/// @audit ↑↑ Out of order with `receive()`
38:     constructor(IWETH weth_, IFactory factory_) {

/// @audit ↓↓ Out of order with `addLiquidity()`
112:     function previewAddLiquidity(
113:         address lp,
114:         uint256 baseInAmount,
115:         uint256 quoteInAmount
116:     ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

/// @audit ↑↑ Out of order with `previewAddLiquidity()`
162:     function addLiquidity(
163:         address lp,
164:         address to,
165:         uint256 baseInAmount,
166:         uint256 quoteInAmount,
167:         uint256 minimumShares,
168:         uint256 deadline
169:     ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

/// @audit ↑↑ Out of order with `addLiquidity()`
178:     function addLiquidityUnsafe(
179:         address lp,
180:         address to,
181:         uint256 baseInAmount,
182:         uint256 quoteInAmount,
183:         uint256 minimumShares,
184:         uint256 deadline
185:     ) external ensureDeadline(deadline) returns (uint256 shares) {

/// @audit ↑↑ Out of order with `addLiquidityUnsafe()`
192:     function addLiquidityETH(
193:         address lp,
194:         address to,
195:         address payable refundTo,
196:         uint256 tokenInAmount,
197:         uint256 minimumShares,
198:         uint256 deadline
199:     ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

/// @audit ↑↑ Out of order with `addLiquidityETH()`
229:     function addLiquidityETHUnsafe(
230:         address lp,
231:         address to,
232:         uint256 tokenInAmount,
233:         uint256 minimumShares,
234:         uint256 deadline
235:     ) external payable ensureDeadline(deadline) returns (uint256 shares) {

/// @audit ↓↓ Out of order with `removeLiquidity()`
251:     function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

/// @audit ↑↑ Out of order with `previewRemoveLiquidity()`
261:     function removeLiquidity(
262:         address lp,
263:         address to,
264:         uint256 sharesIn,
265:         uint256 minimumBaseAmount,
266:         uint256 minimumQuoteAmount,
267:         uint256 deadline
268:     ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

/// @audit ↑↑ Out of order with `removeLiquidity()`
274:     function removeLiquidityETH(
275:         address lp,
276:         address to,
277:         uint256 sharesIn,
278:         uint256 minimumETHAmount,
279:         uint256 minimumTokenAmount,
280:         uint256 deadline
281:     ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {

/// @audit ↑↑ Out of order with `removeLiquidityETH()`
314:     function swapTokensForTokens(
315:         address to,
316:         uint256 amountIn,
317:         address[] calldata path,
318:         uint256 directions,
319:         uint256 minimumOut,
320:         uint256 deadline
321:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit ↑↑ Out of order with `swapTokensForTokens()`
336:     function swapETHForTokens(
337:         address to,
338:         address[] calldata path,
339:         uint256 directions,
340:         uint256 minimumOut,
341:         uint256 deadline
342:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit ↑↑ Out of order with `swapETHForTokens()`
365:     function swapTokensForETH(
366:         address to,
367:         uint256 amountIn,
368:         address[] calldata path,
369:         uint256 directions,
370:         uint256 minimumOut,
371:         uint256 deadline
372:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit ↑↑ Out of order with `swapTokensForETH()`
404:     function sellBaseTokensForTokens(
405:         address lp,
406:         address to,
407:         uint256 amountIn,
408:         uint256 minimumOut,
409:         uint256 deadline
410:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit ↑↑ Out of order with `sellBaseTokensForTokens()`
415:     function sellBaseETHForTokens(
416:         address lp,
417:         address to,
418:         uint256 minimumOut,
419:         uint256 deadline
420:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit ↑↑ Out of order with `sellBaseETHForTokens()`
432:     function sellBaseTokensForETH(
433:         address lp,
434:         address to,
435:         uint256 amountIn,
436:         uint256 minimumOut,
437:         uint256 deadline
438:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit ↑↑ Out of order with `sellBaseTokensForETH()`
449:     function sellQuoteTokensForTokens(
450:         address lp,
451:         address to,
452:         uint256 amountIn,
453:         uint256 minimumOut,
454:         uint256 deadline
455:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit ↑↑ Out of order with `sellQuoteTokensForTokens()`
461:     function sellQuoteETHForTokens(
462:         address lp,
463:         address to,
464:         uint256 minimumOut,
465:         uint256 deadline
466:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit ↑↑ Out of order with `sellQuoteETHForTokens()`
478:     function sellQuoteTokensForETH(
479:         address lp,
480:         address to,
481:         uint256 amountIn,
482:         uint256 minimumOut,
483:         uint256 deadline
484:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit ↓↓ Out of order with `_swap()`
509:     function _adjustAddLiquidity(
510:         address lp,
511:         uint256 baseInAmount,
512:         uint256 quoteInAmount
513:     ) internal view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount) {

/// @audit ↑↑ Out of order with `_adjustAddLiquidity()`
541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

/// @audit ↑↑ Out of order with `_swap()`
571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

/// @audit ↑↑ Out of order with `_sellBase()`
578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {
```

- *MagicLpAggregator.sol* ( [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L33-L33), [37-37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L37-L37), [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L48-L48) ):

```solidity
/// @audit ↓↓ Out of order with `latestAnswer()`
33:     function _getReserves() internal view virtual returns (uint256, uint256) {

/// @audit ↑↑ Out of order with `_getReserves()`
37:     function latestAnswer() public view override returns (int256) {

/// @audit ↑↑ Out of order with `latestAnswer()`
48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```

- *LockingMultiRewards.sol* ( [191-191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L191-L191), [199-199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L199-L199), [292-292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L292-L292), [300-300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L300-L300), [317-317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L317-L317), [324-324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L324-L324), [337-337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L337-L337), [341-341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L341-L341), [349-349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L349-L349), [361-361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L361-L361), [397-397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L397-L397), [458-458](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L458-L458), [479-479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L479-L479), [528-528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L528-L528), [536-536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L536-L536), [544-544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L544-L544), [557-557](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L557-L557), [572-572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L572-L572), [597-597](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L597-L597) ):

```solidity
/// @audit ↓↓ Out of order with `rewardData()`
191:     function getRewards() public virtual {

/// @audit ↑↑ Out of order with `getRewards()`
199:     function rewardData(address token) external view returns (Reward memory) {

/// @audit ↓↓ Out of order with `addReward()`
292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

/// @audit ↑↑ Out of order with `_earned()`
300:     function addReward(address rewardToken) public onlyOwner {

/// @audit ↑↑ Out of order with `addReward()`
317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

/// @audit ↑↑ Out of order with `setMinLockAmount()`
324:     function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {

/// @audit ↑↑ Out of order with `recover()`
337:     function pause() external onlyOwner {

/// @audit ↑↑ Out of order with `pause()`
341:     function unpause() external onlyOwner {

/// @audit ↑↑ Out of order with `unpause()`
349:     function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {

/// @audit ↓↓ Out of order with `processExpiredLocks()`
361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {

/// @audit ↑↑ Out of order with `notifyRewardAmount()`
397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {

/// @audit ↓↓ Out of order with `_createLock()`
458:     function _stakeFor(address account, uint256 amount, bool lock_) internal {

/// @audit ↑↑ Out of order with `_stakeFor()`
479:     function _createLock(address user, uint256 amount) internal {

/// @audit ↑↑ Out of order with `_createLock()`
528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

/// @audit ↑↑ Out of order with `_updateRewardsGlobal()`
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

/// @audit ↑↑ Out of order with `_udpateUserRewards()`
544:     function _updateRewards() internal {

/// @audit ↑↑ Out of order with `_updateRewards()`
557:     function _updateRewardsForUser(address user) internal {

/// @audit ↑↑ Out of order with `_updateRewardsForUser()`
572:     function _updateRewardsForUsers(address[] memory users) internal {

/// @audit ↑↑ Out of order with `_updateRewardsForUsers()`
597:     function _getRewards(address user) internal {
```

</details>

### [N-05] Use of `override` is unnecessary

[Starting from Solidity 0.8.8](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding), the override keyword is not required when overriding an interface function, except for the case where the function is defined in multiple bases.

<details>
<summary>There are 13 instances (click to show):</summary>

- *BlastBox.sol* ( [36-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L36-L42), [98-98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L98-L98), [103-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L103-L103) ):

```solidity
36:     function _onBeforeDeposit(
37:         IERC20 token,
38:         address /*from*/,
39:         address /*to*/,
40:         uint256 /*amount*/,
41:         uint256 /*share*/
42:     ) internal view override {

98:     function _configure() internal override {

103:     function isOwner(address _account) internal view override returns (bool) {
```

- *BlastMagicLP.sol* ( [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L39-L39), [98-98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L98-L98) ):

```solidity
39:     function version() external pure override returns (string memory) {

98:     function _afterInitialized() internal override {
```

- *BlastOnboarding.sol* ( [226-226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L226-L226) ):

```solidity
226:     function _implementation() internal view override returns (address) {
```

- *BlastWrappers.sol* ( [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L59-L59) ):

```solidity
59:     function init(bytes calldata data) public payable override {
```

- *MagicLP.sol* ( [155-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L155-L155), [159-159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L159-L159), [163-163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L163-L163), [593-593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L593-L593) ):

```solidity
155:     function name() public view override returns (string memory) {

159:     function symbol() public pure override returns (string memory) {

163:     function decimals() public view override returns (uint8) {

593:     function _mint(address to, uint256 amount) internal override {
```

- *MagicLpAggregator.sol* ( [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L29-L29), [37-37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L37-L37) ):

```solidity
29:     function decimals() external pure override returns (uint8) {

37:     function latestAnswer() public view override returns (int256) {
```

</details>

### [N-06] Unused errors

The following `error`s are defined but not used. It is recommended to check the code for logical omissions that cause them not to be used. If it's determined that they are not needed anywhere, it's best to remove them from the codebase to improve code clarity and minimize confusion.
Note that there may be cases where an error appears to be used because it has multiple definitions in different files. In such cases, the definitions should be moved to a separate file.

There are 6 instances:

- *BlastOnboardingBoot.sol* ( [46-46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L46-L46) ):

```solidity
46:     error ErrWrongFeeRateModel();
```

- *MagicLP.sol* ( [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L43-L43) ):

```solidity
43:     error ErrInvalidSignature();
```

- *Router.sol* ( [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L21-L21), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L27-L27) ):

```solidity
21:     error ErrBadPath();

27:     error ErrInvalidQuoteTarget();
```

- *LockingMultiRewards.sol* ( [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L34-L34), [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L35-L35) ):

```solidity
34:     error ErrNotExpired();

35:     error ErrInvalidUser();
```

### [N-07] Unused events

The following `event`s are defined but not used. It is recommended to check the code for logical omissions that cause them not to be used. If it's determined that they are not needed anywhere, it's best to remove them from the codebase to improve code clarity and minimize confusion.
Note that there may be cases where an event appears to be used because it has multiple definitions in different files. In such cases, the definitions should be moved to a separate file.

There are 3 instances:

- *BlastMagicLP.sol* ( [13-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L13-L13) ):

```solidity
13:     event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);
```

- *Factory.sol* ( [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L26-L26) ):

```solidity
26:     event LogSetMaintainer(address indexed newMaintainer);
```

- *LockingMultiRewards.sol* ( [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L26-L26) ):

```solidity
26:     event LogRewardsDurationUpdated(address token, uint256 newDuration);
```

### [N-08] Consider providing a ranged getter for array state variables

While the compiler automatically provides a getter for accessing single elements within a public state variable array, it doesn't provide a way to fetch the whole array, or subsets thereof. Consider adding a function to allow the fetching of slices of the array, especially if the contract doesn't already have multicall functionality.

There are 3 instances:

- *Factory.sol* ( [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L35-L35), [36-36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L36-L36) ):

```solidity
35:     mapping(address base => mapping(address quote => address[] pools)) public pools;

36:     mapping(address creator => address[] pools) public userPools;
```

- *LockingMultiRewards.sol* ( [98-98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L98-L98) ):

```solidity
98:     address[] public rewardTokens;
```

### [N-09] Consider splitting complex checks into multiple steps

Assign the expression's parts to intermediate local variables, and check against those instead.

There are 2 instances:

- *MagicLP.sol* ( [102-102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L102-L102), [549-549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L549-L549) ):

```solidity
102:         if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {

549:         if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
```

### [N-10] Complex casting

Consider whether the number of casts is really necessary, or whether using a different type would be more appropriate. Alternatively, add comments to explain in detail why the casts are necessary, and any implicit reasons why the cast does not introduce an overflow.

There are 4 instances:

- *MagicLP.sol* ( [438-438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L438-L438), [439-439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L439-L439), [513-513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L513-L513), [517-517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L517-L517) ):

```solidity
438:         _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));

439:         _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));

513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
```

### [N-11] Complex math should be split into multiple steps

Consider splitting long arithmetic calculations into multiple steps to improve the code readability.

There are 4 instances:

- *Math.sol* ( [97-97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L97-L97), [99-99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L99-L99), [158-158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L158-L158), [170-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L170-L170) ):

```solidity
97:             _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);

99:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);

158:                 temp = (((delta * V1) / V0) * i) / V0;

170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
```

### [N-12] Consider adding a block/deny-list

Doing so will significantly increase centralization, but will help to prevent hackers from using stolen tokens

There are 4 instances:

- *BlastOnboarding.sol* ( [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L64) ):

```solidity
64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```

- *MagicLP.sol* ( [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L25) ):

```solidity
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```

- *Router.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L12) ):

```solidity
12: contract Router {
```

- *LockingMultiRewards.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L14) ):

```solidity
14: contract LockingMultiRewards is OperatableV2, Pausable {
```

### [N-13] Constants/Immutables redefined elsewhere

Consider defining in only one contract so that values cannot become out of sync when only one location is updated. A [cheap way](https://medium.com/coinmonks/gas-cost-of-solidity-library-functions-dbe0cedd4678) to store constants/immutables in a single location is to create an `internal constant` in a `library`. If the variable is a local cache of another contract's value, consider making the cache variable internal or private, which will require external users to query the contract with the source of truth, so that callers don't get out of sync.

There are 2 instances:

- *BlastBox.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L20-L20) ):

```solidity
/// @audit Seen in src/blast/BlastMagicLP.sol#17
20:     BlastTokenRegistry public immutable registry;
```

- *BlastMagicLP.sol* ( [17-17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L17-L17) ):

```solidity
/// @audit Seen in src/blast/BlastBox.sol#20
17:     BlastTokenRegistry public immutable registry;
```

### [N-14] Convert simple `if`-statements to ternary expressions

Converting some if statements to ternaries (such as `z = (a < b) ? x : y`) can make the code more concise and easier to read.

<details>
<summary>There are 5 instances (click to show):</summary>

- *Math.sol* ( [96-100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L96-L100), [155-159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L155-L159) ):

```solidity
96:         } else if ((ki * delta) / ki == delta) {
97:             _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);
98:         } else {
99:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);
100:         }

155:             } else if ((idelta * V1) / idelta == V1) {
156:                 temp = (idelta * V1) / (V0 * V0);
157:             } else {
158:                 temp = (((delta * V1) / V0) * i) / V0;
159:             }
```

- *Router.sol* ( [348-352](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L348-L352), [379-383](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L379-L383), [560-564](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L560-L564) ):

```solidity
348:         if (directions & 1 == 0) {
349:             inToken = IMagicLP(firstLp)._BASE_TOKEN_();
350:         } else {
351:             inToken = IMagicLP(firstLp)._QUOTE_TOKEN_();
352:         }

379:         if ((directions >> lastLpIndex) & 1 == 0) {
380:             outToken = IMagicLP(lastLp)._QUOTE_TOKEN_();
381:         } else {
382:             outToken = IMagicLP(lastLp)._BASE_TOKEN_();
383:         }

560:         if ((directions & 1 == 0)) {
561:             amountOut = IMagicLP(path[iterations]).sellBase(to);
562:         } else {
563:             amountOut = IMagicLP(path[iterations]).sellQuote(to);
564:         }
```

</details>

### [N-15] Contracts should each be defined in separate files

Keeping each contract in a separate file makes it easier to work with multiple people, makes the code easier to maintain, and is a common practice on most projects. The following files each contains more than one contract/library/interface.

There are 3 instances:

- [*BlastOnboarding.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol)

- [*BlastOnboardingBoot.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol)

- [*BlastWrappers.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol)

### [N-16] Contract name does not match its filename

According to the [Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html#contract-and-library-names), contract and library names should also match their filenames.

There are 3 instances:

- *BlastWrappers.sol* ( [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L19), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L28), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L42) ):

```solidity
/// @audit Not match filename `BlastWrappers.sol`
19: contract BlastMIMSwapRouter is Router {

/// @audit Not match filename `BlastWrappers.sol`
28: contract BlastMIMSwapFactory is Factory {

/// @audit Not match filename `BlastWrappers.sol`
42: contract BlastCauldronV4 is CauldronV4 {
```

### [N-17] UPPER_CASE names should be reserved for `constant`/`immutable` variables

If the variable needs to be different based on which class it comes from, a `view`/`pure` _function_ should be used instead (e.g. like [this](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/76eee35971c2541585e05cbf258510dda7b2fbc6/contracts/token/ERC20/extensions/draft-IERC20Permit.sol#L59)).

<details>
<summary>There are 25 instances (click to show):</summary>

- *MagicLP.sol* ( [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L68), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L70), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L71), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L74), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L75), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L76), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L77), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L79), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L80), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L81), [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L82), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204) ):

```solidity
68:     bool internal _INITIALIZED_;

70:     address public _BASE_TOKEN_;

71:     address public _QUOTE_TOKEN_;

72:     uint112 public _BASE_RESERVE_;

73:     uint112 public _QUOTE_RESERVE_;

74:     uint32 public _BLOCK_TIMESTAMP_LAST_;

75:     uint256 public _BASE_PRICE_CUMULATIVE_LAST_;

76:     uint112 public _BASE_TARGET_;

77:     uint112 public _QUOTE_TARGET_;

79:     IFeeRateModel public _MT_FEE_RATE_MODEL_;

80:     uint256 public _LP_FEE_RATE_;

81:     uint256 public _K_;

82:     uint256 public _I_;

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
```

- *Math.sol* ( [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51), [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L62), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L79), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131), [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L199) ):

```solidity
51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

199:         uint256 V2 = DecimalMath.divCeil(numerator, denominator);
```

- *PMMPricing.sol* ( [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L33) ):

```solidity
32:         uint256 B0;

33:         uint256 Q0;
```

</details>

### [N-18] Do not use literal numbers for array indexes

Indexing arrays using enums or meaningfully named constants instead of literals can make code easier to read and maintain.

There are 3 instances:

- *Router.sol* ( [324-324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L324-L324), [345-345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L345-L345), [389-389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L389-L389) ):

```solidity
324:         address firstLp = path[0];

345:         address firstLp = path[0];

389:         address firstLp = path[0];
```

### [N-19] Contract timekeeping will break earlier than the Ethereum network itself will stop working

When a timestamp is downcast from `uint256` to `uint32`, the value will wrap in the year 2106, and the contracts will break. Other downcasts will have different endpoints. Consider whether your contract is intended to live past the size of the type being used.

There are 2 instances:

- *MagicLP.sol* ( [125-125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L125-L125), [546-546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L546-L546) ):

```solidity
125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

546:         uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
```

### [N-20] Consider emitting an event at the end of the constructor

This will allow users to easily exactly pinpoint when and by whom a contract was constructed.

<details>
<summary>There are 16 instances (click to show):</summary>

- *BlastBox.sol* ( [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L24-L24) ):

```solidity
24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
```

- *BlastDapp.sol* ( [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L7-L7) ):

```solidity
7:     constructor() {
```

- *BlastGovernor.sol* ( [15-15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L15-L15) ):

```solidity
15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```

- *BlastMagicLP.sol* ( [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L23-L23) ):

```solidity
23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
```

- *BlastOnboarding.sol* ( [58-58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L58-L58), [84-84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L84-L84) ):

```solidity
58:     constructor() Owned(msg.sender) {

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {
```

- *BlastTokenRegistry.sol* ( [12-12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L12-L12) ):

```solidity
12:     constructor(address _owner) Owned(_owner) {}
```

- *BlastWrappers.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L20-L20), [29-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L29-L34), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L47-L47) ):

```solidity
20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

29:     constructor(
30:         address implementation_,
31:         IFeeRateModel maintainerFeeRateModel_,
32:         address owner_,
33:         address governor_
34:     ) Factory(implementation_, maintainerFeeRateModel_, owner_) {

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
```

- *MagicLP.sol* ( [84-84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L84-L84) ):

```solidity
84:     constructor(address owner_) Owned(owner_) {
```

- *FeeRateModel.sol* ( [22-22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L22-L22) ):

```solidity
22:     constructor(address maintainer_, address owner_) Owned(owner_) {
```

- *Factory.sol* ( [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L38-L38) ):

```solidity
38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
```

- *Router.sol* ( [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L38-L38) ):

```solidity
38:     constructor(IWETH weth_, IFactory factory_) {
```

- *MagicLpAggregator.sol* ( [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L21-L21) ):

```solidity
21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```

- *LockingMultiRewards.sol* ( [112-118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L112-L118) ):

```solidity
112:     constructor(
113:         address _stakingToken,
114:         uint256 _lockingBoostMultiplerInBips,
115:         uint256 _rewardsDuration,
116:         uint256 _lockDuration,
117:         address _owner
118:     ) OperatableV2(_owner) {
```

</details>

### [N-21] Empty function body without comments

Empty function body in solidity is not recommended, consider adding some comments to the body.

There are 3 instances:

- *BlastGovernor.sol* ( [13-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L13-L13) ):

```solidity
13:     receive() external payable {}
```

- *MagicLP.sol* ( [601-601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L601-L601) ):

```solidity
601:     function _afterInitialized() internal virtual {}
```

- *Router.sol* ( [36-36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L36-L36) ):

```solidity
36:     receive() external payable {}
```

### [N-22] Events are emitted without the sender information

When an action is triggered based on a user's action, not being able to filter based on who triggered the action makes event processing a lot more cumbersome. Including the `msg.sender` the events of these types of action will make events much more useful to end users, especially when `msg.sender` is not `tx.origin`.

<details>
<summary>There are 10 instances (click to show):</summary>

- *MagicLP.sol* ( [259-259](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L259-L259), [282-282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L282-L282), [323-323](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L323-L323), [345-345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L345-L345), [409-409](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L409-L409) ):

```solidity
259:             emit RChange(newRState);

282:             emit RChange(newRState);

323:                 emit RChange(newRState);

345:                 emit RChange(newRState);

409:         emit BuyShares(to, shares, balanceOf(to));
```

- *Factory.sol* ( [88-88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L88-L88) ):

```solidity
88:         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
```

- *LockingMultiRewards.sol* ( [392-392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L392-L392), [436-436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L436-L436), [447-447](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L447-L447), [475-475](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L475-L475) ):

```solidity
392:         emit LogRewardAdded(amount);

436:                 emit LogLockIndexChanged(user, lastIndex, index);

447:             emit LogUnlocked(user, amount, index);

475:             emit LogStaked(account, amount);
```

</details>

### [N-23] Event is missing `indexed` fields

Index event fields makes the field more quickly accessible to [off-chain tools](https://ethereum.stackexchange.com/questions/40396/can-somebody-please-explain-the-concept-of-event-indexing) that parse events. However, note that each indexed field costs extra gas during emission, so it's not necessarily best to index the maximum allowed per event (three fields). Each event should use three indexed fields if there are three or more fields, and gas usage is not particularly of concern for the events in question. If there are fewer than three fields, all of the fields should be indexed.

<details>
<summary>There are 19 instances (click to show):</summary>

- *BlastBox.sol* ( [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L14-L14) ):

```solidity
14:     event LogTokenDepositEnabled(address indexed token, bool enabled);
```

- *BlastMagicLP.sol* ( [12-12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L12-L12) ):

```solidity
12:     event LogOperatorChanged(address indexed, bool);
```

- *BlastOnboarding.sol* ( [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L68-L68), [69-69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L69-L69), [74-74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L74-L74) ):

```solidity
68:     event LogTokenSupported(address indexed token, bool supported);

69:     event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);

74:     event LogStateChange(State state);
```

- *BlastOnboardingBoot.sol* ( [37-37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L37-L37), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L38-L38) ):

```solidity
37:     event LogReadyChanged(bool ready);

38:     event LogClaimed(address indexed user, uint256 shares, bool lock);
```

- *BlastTokenRegistry.sol* ( [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L7-L7) ):

```solidity
7:     event LogNativeYieldTokenEnabled(address indexed token, bool enabled);
```

- *MagicLP.sol* ( [30-30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L30-L30), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L31-L31), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L32-L32), [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L33-L33), [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L34-L34), [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L35-L35) ):

```solidity
30:     event BuyShares(address to, uint256 increaseShares, uint256 totalShares);

31:     event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);

32:     event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);

33:     event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);

34:     event RChange(PMMPricing.RState newRState);

35:     event TokenRescue(address indexed token, address to, uint256 amount);
```

- *Factory.sol* ( [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L23-L23), [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L24-L24), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L27-L27) ):

```solidity
23:     event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);

24:     event LogPoolRemoved(address pool);

27:     event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);
```

- *LockingMultiRewards.sol* ( [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L26-L26), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L27-L27) ):

```solidity
26:     event LogRewardsDurationUpdated(address token, uint256 newDuration);

27:     event LogRecovered(address token, uint256 amount);
```

</details>

### [N-24] Function state mutability can be restricted to pure

Function state mutability can be restricted to pure

There is 1 instance:

- *MagicLP.sol* ( [601-601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L601-L601) ):

```solidity
601:     function _afterInitialized() internal virtual {}
```

### [N-25] Imports could be organized more systematically

The contract's interface should be imported first, followed by each of the interfaces it uses, followed by all other files. The examples below do not follow this layout.

<details>
<summary>There are 13 instances (click to show):</summary>

- *BlastBox.sol* ( [9-9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L9-L9), [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L11-L11) ):

```solidity
/// @audit Out of order with the prev import️ ⬆
9: import {IERC20} from "BoringSolidity/interfaces/IERC20.sol";

/// @audit Out of order with the prev import️ ⬆
11: import {IWETH} from "interfaces/IWETH.sol";
```

- *BlastOnboardingBoot.sol* ( [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L7-L7) ):

```solidity
/// @audit Out of order with the prev import️ ⬆
7: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";
```

- *BlastWrappers.sol* ( [8-8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L8-L8), [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L10-L10) ):

```solidity
/// @audit Out of order with the prev import️ ⬆
8: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";

/// @audit Out of order with the prev import️ ⬆
10: import {IWETH} from "interfaces/IWETH.sol";
```

- *BlastYields.sol* ( [4-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L4-L4) ):

```solidity
/// @audit Out of order with the prev import️ ⬆
4: import {IBlast, IERC20Rebasing, YieldMode, GasMode} from "interfaces/IBlast.sol";
```

- *MagicLP.sol* ( [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L11-L11), [19-19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L19-L19) ):

```solidity
/// @audit Out of order with the prev import️ ⬆
11: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";

/// @audit Out of order with the prev import️ ⬆
19: import {ICallee} from "/mimswap/interfaces/ICallee.sol";
```

- *FeeRateModel.sol* ( [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L11-L11) ):

```solidity
/// @audit Out of order with the prev import️ ⬆
11: import {IFeeRateImpl} from "../interfaces/IFeeRateModel.sol";
```

- *Factory.sol* ( [6-6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L6-L6) ):

```solidity
/// @audit Out of order with the prev import️ ⬆
6: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";
```

- *Router.sol* ( [5-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L5-L5), [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L7-L7) ):

```solidity
/// @audit Out of order with the prev import️ ⬆
5: import {IERC20} from "openzeppelin-contracts/interfaces/IERC20.sol";

/// @audit Out of order with the prev import️ ⬆
7: import {IWETH} from "interfaces/IWETH.sol";
```

- *MagicLpAggregator.sol* ( [5-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L5-L5) ):

```solidity
/// @audit Out of order with the prev import️ ⬆
5: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```

</details>

### [N-26] @openzeppelin/contracts should be upgraded to a newer version

These contracts import contracts from `@openzeppelin/contracts`, but they are not using [the latest version](https://github.com/OpenZeppelin/openzeppelin-contracts/releases). Using the latest version ensures contract security with fixes for known vulnerabilities, access to the latest feature updates, and enhanced community support and engagement.

The imported version is `4.9.2`.

<details>
<summary>There are 8 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L7), [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L10) ):

```solidity
7: import {Proxy} from "openzeppelin-contracts/proxy/Proxy.sol";

10: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";
```

- *BlastYields.sol* ( [5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L5) ):

```solidity
5: import {Address} from "openzeppelin-contracts/utils/Address.sol";
```

- *MagicLP.sol* ( [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L11) ):

```solidity
11: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```

- *Router.sol* ( [5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L5), [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L10) ):

```solidity
5: import {IERC20} from "openzeppelin-contracts/interfaces/IERC20.sol";

10: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```

- *MagicLpAggregator.sol* ( [5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L5) ):

```solidity
5: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```

- *LockingMultiRewards.sol* ( [5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L5) ):

```solidity
5: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";
```

</details>

### [N-27] safe-contracts should be upgraded to a newer version

These contracts import contracts from `@gnosis.pm/safe-contracts`, but they are not using [the latest version](https://github.com/safe-global/safe-contracts/releases). Using the latest version ensures contract security with fixes for known vulnerabilities, access to the latest feature updates, and enhanced community support and engagement.

The imported version is `1.3.0`.

There is 1 instance:

- Global finding

### [N-28] Lib solady should be upgraded to a newer version

These contracts import contracts from lib solady, but they are not using [the latest version](https://github.com/Vectorized/solady/tags). Using the latest version ensures contract security with fixes for known vulnerabilities, access to the latest feature updates, and enhanced community support and engagement.

The imported version is `0.0.168`.

<details>
<summary>There are 10 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L8) ):

```solidity
8: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";
```

- *BlastOnboardingBoot.sol* ( [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L9) ):

```solidity
9: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";
```

- *MagicLP.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L12), [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L13), [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L14), [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L15) ):

```solidity
12: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

13: import {ReentrancyGuard} from "solady/utils/ReentrancyGuard.sol";

14: import {ERC20} from "solady/tokens/ERC20.sol";

15: import {SafeCastLib} from "solady/utils/SafeCastLib.sol";
```

- *Factory.sol* ( [5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L5) ):

```solidity
5: import {LibClone} from "solady/utils/LibClone.sol";
```

- *Router.sol* ( [4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L4) ):

```solidity
4: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";
```

- *MagicLpAggregator.sol* ( [4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L4) ):

```solidity
4: import {FixedPointMathLib} from "solady/utils/FixedPointMathLib.sol";
```

- *LockingMultiRewards.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L6) ):

```solidity
6: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";
```

</details>

### [N-29] Lines are too long

The [solidity style guide](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#maximum-line-length) recommends a maximum line length of 120 characters. Lines of code that are longer than 120 should be wrapped.

<details>
<summary>There are 54 instances (click to show):</summary>

- *BlastGovernor.sol* ( [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L53) ):

```solidity
53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

- *BlastMagicLP.sol* ( [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L53) ):

```solidity
53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {
```

- *BlastOnboarding.sol* ( [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L101), [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L123) ):

```solidity
101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
```

- *BlastOnboardingBoot.sol* ( [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L86), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L96) ):

```solidity
86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
```

- *MagicLP.sol* ( [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L32), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L36), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L156), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L170), [183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L183), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204), [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L290), [310](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L310), [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L325), [332](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L332), [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L347), [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L360), [381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L381), [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L402), [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L403), [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L439) ):

```solidity
32:     event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);

36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);

156:         return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));

170:     ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {

183:     ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

310:             (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) = querySellQuote(

325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

332:             (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) = querySellBase(

347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {

381:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;

402:             _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

403:             _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();

439:         _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
```

- *FeeRateModel.sol* ( [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L34) ):

```solidity
34:     function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```

- *Math.sol* ( [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L79), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131), [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L184) ):

```solidity
51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
```

- *PMMPricing.sol* ( [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L39), [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L55), [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L65), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L76), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L96), [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L129), [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L144), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L185) ):

```solidity
39:     function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {

55:                     // [Important corner case!] may enter this branch when some precision problem happens. And consequently contribute to negative spare quote amount

65:                 receiveQuoteAmount = backToOneReceiveQuote + _ROneSellBaseToken(state, payBaseAmount - backToOnePayBase);

76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {

96:                 receiveBaseAmount = backToOneReceiveBase + _ROneSellQuoteToken(state, payQuoteAmount - backToOnePayQuote);

129:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);

144:         return Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K);

185:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);
```

- *Factory.sol* ( [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L86) ):

```solidity
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

86:         IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
```

- *Router.sol* ( [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L88), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L101), [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L138), [169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L169), [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L199), [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L251), [523](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L523), [541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L541) ):

```solidity
88:         clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);

101:         shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

138:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;

169:     ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

199:     ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

251:     function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

523:             uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {
```

- *LockingMultiRewards.sol* ( [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L11), [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L12), [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L13), [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L109), [252](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L252), [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L277), [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L292), [322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L322), [533](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L533) ):

```solidity
11: /// @author Based from Curve Finance's MultiRewards contract https://github.com/curvefi/multi-rewards/blob/master/contracts/MultiRewards.sol

12: /// @author Based from Ellipsis Finance's EpsStaker https://github.com/ellipsis-finance/ellipsis/blob/master/contracts/EpsStaker.sol

13: /// @author Based from Convex Finance's CvxLockerV2 https://github.com/convex-eth/platform/blob/main/contracts/contracts/CvxLockerV2.sol

109:     /// @param _lockingBoostMultiplerInBips The multiplier for the locking boost. 30000 means if you stake 100, you get 300 locked

252:     // |                             ^ lock starts (adjusted)                                    ^ unlock ends (nextUnlockTime)

277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

322:     /// @notice This function can recover any token except for the staking token beyond the balance necessary for rewards.

533:         _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow
```

</details>

### [N-30] Functions not used internally could be marked external

If desired, sub contracts can change the visibility from `external` to `public` by [overriding](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding) the functions of their parents.

<details>
<summary>There are 17 instances (click to show):</summary>

- *BlastWrappers.sol* ( [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L59-L59) ):

```solidity
59:     function init(bytes calldata data) public payable override {
```

- *MagicLP.sol* ( [155-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L155-L155), [159-159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L159-L159), [163-163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L163-L163), [228-228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L228-L228), [232-232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L232-L232), [470-479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L470-L479) ):

```solidity
155:     function name() public view override returns (string memory) {

159:     function symbol() public pure override returns (string memory) {

163:     function decimals() public view override returns (uint8) {

228:     function getBaseInput() public view returns (uint256 input) {

232:     function getQuoteInput() public view returns (uint256 input) {

470:     function setParameters(
471:         address assetTo,
472:         uint256 newLpFeeRate,
473:         uint256 newI,
474:         uint256 newK,
475:         uint256 baseOutAmount,
476:         uint256 quoteOutAmount,
477:         uint256 minBaseReserve,
478:         uint256 minQuoteReserve
479:     ) public nonReentrant onlyImplementationOwner {
```

- *FeeRateModel.sol* ( [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L57-L57) ):

```solidity
57:     function setImplementation(address implementation_) public onlyOwner {
```

- *Factory.sol* ( [65-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L65-L72) ):

```solidity
65:     function predictDeterministicAddress(
66:         address creator,
67:         address baseToken_,
68:         address quoteToken_,
69:         uint256 lpFeeRate_,
70:         uint256 i_,
71:         uint256 k_
72:     ) public view returns (address) {
```

- *LockingMultiRewards.sol* ( [150-150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L150-L150), [155-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L155-L155), [186-186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L186-L186), [191-191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L191-L191), [265-265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L265-L265), [288-288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L288-L288), [300-300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L300-L300), [361-361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L361-L361) ):

```solidity
150:     function stake(uint256 amount, bool lock_) public whenNotPaused {

155:     function lock(uint256 amount) public whenNotPaused {

186:     function withdrawWithRewards(uint256 amount) public virtual {

191:     function getRewards() public virtual {

265:     function remainingEpochTime() public view returns (uint256) {

288:     function earned(address user, address rewardToken) public view returns (uint256) {

300:     function addReward(address rewardToken) public onlyOwner {

361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
```

</details>

### [N-31] Contracts containing only utility functions should be made into libraries

Consider using a `library` instead of a `contract` to provide utility functions.

There are 2 instances:

- *BlastDapp.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L6) ):

```solidity
6: contract BlastDapp {
```

- *FeeRateModelImpl.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L7) ):

```solidity
7: contract FeeRateModelImpl {
```

### [N-32] Use `@inheritdoc` for overridden functions

It is recommended to use `@inheritdoc` for overridden functions.

<details>
<summary>There are 14 instances (click to show):</summary>

- *BlastBox.sol* ( [36-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L36-L42), [97-98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L97-L98), [103-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L103-L103) ):

```solidity
36:     function _onBeforeDeposit(
37:         IERC20 token,
38:         address /*from*/,
39:         address /*to*/,
40:         uint256 /*amount*/,
41:         uint256 /*share*/
42:     ) internal view override {

97:     /// @dev Called on DegenBox's constructor
98:     function _configure() internal override {

103:     function isOwner(address _account) internal view override returns (bool) {
```

- *BlastMagicLP.sol* ( [36-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L36-L39), [95-98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L95-L98) ):

```solidity
36:     /// VIEWS
37:     //////////////////////////////////////////////////////////////////////////////////////
38: 
39:     function version() external pure override returns (string memory) {

95:     /// INTERNALS
96:     //////////////////////////////////////////////////////////////////////////////////////
97: 
98:     function _afterInitialized() internal override {
```

- *BlastOnboarding.sol* ( [80-80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L80-L80), [223-226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L223-L226) ):

```solidity
80:     receive() external payable override {

223:     /// PROXY IMPLEMENTATION
224:     //////////////////////////////////////////////////////////////////////////////////////
225: 
226:     function _implementation() internal view override returns (address) {
```

- *BlastWrappers.sol* ( [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L59-L59) ):

```solidity
59:     function init(bytes calldata data) public payable override {
```

- *MagicLP.sol* ( [152-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L152-L155), [159-159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L159-L159), [163-163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L163-L163), [593-593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L593-L593) ):

```solidity
152:     /// VIEWS
153:     //////////////////////////////////////////////////////////////////////////////////////
154: 
155:     function name() public view override returns (string memory) {

159:     function symbol() public pure override returns (string memory) {

163:     function decimals() public view override returns (uint8) {

593:     function _mint(address to, uint256 amount) internal override {
```

- *MagicLpAggregator.sol* ( [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L29-L29), [37-37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L37-L37) ):

```solidity
29:     function decimals() external pure override returns (uint8) {

37:     function latestAnswer() public view override returns (int256) {
```

</details>

### [N-33] Contracts should have NatSpec `@author` tags

Contracts should have NatSpec `@author` tags

<details>
<summary>There are 19 instances (click to show):</summary>

- *BlastBox.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L13) ):

```solidity
13: contract BlastBox is DegenBox, OperatableV3 {
```

- *BlastDapp.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L6) ):

```solidity
6: contract BlastDapp {
```

- *BlastGovernor.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L7) ):

```solidity
7: contract BlastGovernor is OperatableV2 {
```

- *BlastMagicLP.sol* ( [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L10) ):

```solidity
10: contract BlastMagicLP is MagicLP {
```

- *BlastOnboarding.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L12), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L64) ):

```solidity
12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```

- *BlastOnboardingBoot.sol* ( [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L23), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L34) ):

```solidity
23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```

- *BlastTokenRegistry.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L6) ):

```solidity
6: contract BlastTokenRegistry is Owned {
```

- *BlastWrappers.sol* ( [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L19), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L28), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L42) ):

```solidity
19: contract BlastMIMSwapRouter is Router {

28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {
```

- *BlastPoints.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L6) ):

```solidity
6: library BlastPoints {
```

- *BlastYields.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L7) ):

```solidity
7: library BlastYields {
```

- *FeeRateModel.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L13) ):

```solidity
13: contract FeeRateModel is Owned {
```

- *FeeRateModelImpl.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L7) ):

```solidity
7: contract FeeRateModelImpl {
```

- *Factory.sol* ( [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L11) ):

```solidity
11: contract Factory is Owned {
```

- *Router.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L12) ):

```solidity
12: contract Router {
```

- *MagicLpAggregator.sol* ( [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L9) ):

```solidity
9: contract MagicLpAggregator is IAggregator {
```

</details>

### [N-34] Contracts should have `@notice` tags

The `@notice` is used to explain to users what the contract does. The compiler interprets `///` or `/**` comments [as this tag](https://docs.soliditylang.org/en/latest/natspec-format.html#tags) if one wasn't explicitly provided.

<details>
<summary>There are 17 instances (click to show):</summary>

- *BlastBox.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L13) ):

```solidity
13: contract BlastBox is DegenBox, OperatableV3 {
```

- *BlastDapp.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L6) ):

```solidity
6: contract BlastDapp {
```

- *BlastGovernor.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L7) ):

```solidity
7: contract BlastGovernor is OperatableV2 {
```

- *BlastMagicLP.sol* ( [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L10) ):

```solidity
10: contract BlastMagicLP is MagicLP {
```

- *BlastOnboarding.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L12), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L64) ):

```solidity
12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```

- *BlastOnboardingBoot.sol* ( [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L23) ):

```solidity
23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
```

- *BlastTokenRegistry.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L6) ):

```solidity
6: contract BlastTokenRegistry is Owned {
```

- *BlastWrappers.sol* ( [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L19), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L28), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L42) ):

```solidity
19: contract BlastMIMSwapRouter is Router {

28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {
```

- *BlastPoints.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L6) ):

```solidity
6: library BlastPoints {
```

- *BlastYields.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L7) ):

```solidity
7: library BlastYields {
```

- *FeeRateModel.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L13) ):

```solidity
13: contract FeeRateModel is Owned {
```

- *FeeRateModelImpl.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L7) ):

```solidity
7: contract FeeRateModelImpl {
```

- *Router.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L12) ):

```solidity
12: contract Router {
```

- *MagicLpAggregator.sol* ( [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L9) ):

```solidity
9: contract MagicLpAggregator is IAggregator {
```

</details>

### [N-35] Contracts should have NatSpec `@title` tags

Some contract definitions have an incomplete NatSpec: add a `@title` notation to describe the contract to improve the code documentation.

<details>
<summary>There are 21 instances (click to show):</summary>

- *BlastBox.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L13) ):

```solidity
13: contract BlastBox is DegenBox, OperatableV3 {
```

- *BlastDapp.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L6) ):

```solidity
6: contract BlastDapp {
```

- *BlastGovernor.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L7) ):

```solidity
7: contract BlastGovernor is OperatableV2 {
```

- *BlastMagicLP.sol* ( [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L10) ):

```solidity
10: contract BlastMagicLP is MagicLP {
```

- *BlastOnboarding.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L12), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L64) ):

```solidity
12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```

- *BlastOnboardingBoot.sol* ( [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L23), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L34) ):

```solidity
23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```

- *BlastTokenRegistry.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L6) ):

```solidity
6: contract BlastTokenRegistry is Owned {
```

- *BlastWrappers.sol* ( [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L19), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L28), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L42) ):

```solidity
19: contract BlastMIMSwapRouter is Router {

28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {
```

- *BlastPoints.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L6) ):

```solidity
6: library BlastPoints {
```

- *BlastYields.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L7) ):

```solidity
7: library BlastYields {
```

- *FeeRateModel.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L13) ):

```solidity
13: contract FeeRateModel is Owned {
```

- *FeeRateModelImpl.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L7) ):

```solidity
7: contract FeeRateModelImpl {
```

- *Math.sol* ( [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L16) ):

```solidity
16: library Math {
```

- *Factory.sol* ( [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L11) ):

```solidity
11: contract Factory is Owned {
```

- *Router.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L12) ):

```solidity
12: contract Router {
```

- *MagicLpAggregator.sol* ( [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L9) ):

```solidity
9: contract MagicLpAggregator is IAggregator {
```

- *LockingMultiRewards.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L14) ):

```solidity
14: contract LockingMultiRewards is OperatableV2, Pausable {
```

</details>

### [N-36] Events missing NatSpec `@param` tag

Each event parameter should have a `@param` notation to improve the code documentation.

<details>
<summary>There are 123 instances (click to show):</summary>

- *BlastBox.sol* ( [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L14-L14), [15-15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L15-L15) ):

```solidity
/// @audit Missing @param for `token`, `enabled`
14:     event LogTokenDepositEnabled(address indexed token, bool enabled);

/// @audit Missing @param for `feeTo`
15:     event LogFeeToChanged(address indexed feeTo);
```

- *BlastGovernor.sol* ( [8-8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L8-L8) ):

```solidity
/// @audit Missing @param for `feeTo`
8:     event LogFeeToChanged(address indexed feeTo);
```

- *BlastMagicLP.sol* ( [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L11-L11), [13-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L13-L13) ):

```solidity
/// @audit Missing @param for `feeTo`
11:     event LogFeeToChanged(address indexed feeTo);

/// @audit Missing @param for `gasAmount`, `nativeAmount`, `token0Amount`, `token1Amount`
13:     event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);
```

- *BlastOnboarding.sol* ( [67-67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L67-L67), [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L68-L68), [69-69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L69-L69), [70-70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L70-L70), [71-71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L71-L71), [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L72-L72), [73-73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L73-L73), [74-74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L74-L74), [75-75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L75-L75) ):

```solidity
/// @audit Missing @param for `bootstrapper`
67:     event LogBootstrapperChanged(address indexed bootstrapper);

/// @audit Missing @param for `token`, `supported`
68:     event LogTokenSupported(address indexed token, bool supported);

/// @audit Missing @param for `user`, `token`, `amount`, `lock`
69:     event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);

/// @audit Missing @param for `user`, `token`, `amount`
70:     event LogLock(address indexed user, address indexed token, uint256 amount);

/// @audit Missing @param for `feeTo`
71:     event LogFeeToChanged(address indexed feeTo);

/// @audit Missing @param for `user`, `token`, `amount`
72:     event LogWithdraw(address indexed user, address indexed token, uint256 amount);

/// @audit Missing @param for `token`, `cap`
73:     event LogTokenCapChanged(address indexed token, uint256 cap);

/// @audit Missing @param for `state`
74:     event LogStateChange(State state);

/// @audit Missing @param for `token`, `to`, `amount`
75:     event LogTokenRescue(address indexed token, address indexed to, uint256 amount);
```

- *BlastOnboardingBoot.sol* ( [37-37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L37-L37), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L38-L38), [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L39-L39), [40-40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L40-L40), [41-41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L41-L41) ):

```solidity
/// @audit Missing @param for `ready`
37:     event LogReadyChanged(bool ready);

/// @audit Missing @param for `user`, `shares`, `lock`
38:     event LogClaimed(address indexed user, uint256 shares, bool lock);

/// @audit Missing @param for `router`
39:     event LogInitialized(Router indexed router);

/// @audit Missing @param for `pool`, `staking`, `amountOut`
40:     event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);

/// @audit Missing @param for `staking`
41:     event LogStakingChanged(address indexed staking);
```

- *BlastTokenRegistry.sol* ( [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L7-L7) ):

```solidity
/// @audit Missing @param for `token`, `enabled`
7:     event LogNativeYieldTokenEnabled(address indexed token, bool enabled);
```

- *BlastYields.sol* ( [8-8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L8-L8), [9-9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L9-L9), [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L10-L10), [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L11-L11), [12-12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L12-L12) ):

```solidity
/// @audit Missing @param for `recipient`, `amount`
8:     event LogBlastGasClaimed(address indexed recipient, uint256 amount);

/// @audit Missing @param for `recipient`, `amount`
9:     event LogBlastETHClaimed(address indexed recipient, uint256 amount);

/// @audit Missing @param for `recipient`, `token`, `amount`
10:     event LogBlastTokenClaimed(address indexed recipient, address indexed token, uint256 amount);

/// @audit Missing @param for `contractAddress`, `token`
11:     event LogBlastTokenClaimableEnabled(address indexed contractAddress, address indexed token);

/// @audit Missing @param for `contractAddress`
12:     event LogBlastNativeClaimableEnabled(address indexed contractAddress);
```

- *MagicLP.sol* ( [30-30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L30-L30), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L31-L31), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L32-L32), [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L33-L33), [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L34-L34), [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L35-L35), [36-36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L36-L36) ):

```solidity
/// @audit Missing @param for `to`, `increaseShares`, `totalShares`
30:     event BuyShares(address to, uint256 increaseShares, uint256 totalShares);

/// @audit Missing @param for `payer`, `to`, `decreaseShares`, `totalShares`
31:     event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);

/// @audit Missing @param for `fromToken`, `toToken`, `fromAmount`, `toAmount`, `trader`, `receiver`
32:     event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);

/// @audit Missing @param for `borrower`, `assetTo`, `baseAmount`, `quoteAmount`
33:     event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);

/// @audit Missing @param for `newRState`
34:     event RChange(PMMPricing.RState newRState);

/// @audit Missing @param for `token`, `to`, `amount`
35:     event TokenRescue(address indexed token, address to, uint256 amount);

/// @audit Missing @param for `newLpFeeRate`, `newI`, `newK`, `newBaseReserve`, `newQuoteReserve`
36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);
```

- *FeeRateModel.sol* ( [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L14-L14), [15-15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L15-L15) ):

```solidity
/// @audit Missing @param for `implementation`
14:     event LogImplementationChanged(address indexed implementation);

/// @audit Missing @param for `maintainer`
15:     event LogMaintainerChanged(address indexed maintainer);
```

- *Factory.sol* ( [12-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L12-L21), [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L23-L23), [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L24-L24), [25-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L25-L25), [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L26-L26), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L27-L27) ):

```solidity
/// @audit Missing @param for `clone_`, `baseToken_`, `quoteToken_`, `creator_`, `lpFeeRate_`, `maintainerFeeRateModel`, `i_`, `k_`
12:     event LogCreated(
13:         address clone_,
14:         address indexed baseToken_,
15:         address indexed quoteToken_,
16:         address indexed creator_,
17:         uint256 lpFeeRate_,
18:         IFeeRateModel maintainerFeeRateModel,
19:         uint256 i_,
20:         uint256 k_
21:     );

/// @audit Missing @param for `baseToken`, `quoteToken`, `creator`, `pool`
23:     event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);

/// @audit Missing @param for `pool`
24:     event LogPoolRemoved(address pool);

/// @audit Missing @param for `implementation`
25:     event LogSetImplementation(address indexed implementation);

/// @audit Missing @param for `newMaintainer`
26:     event LogSetMaintainer(address indexed newMaintainer);

/// @audit Missing @param for `newMaintainerFeeRateModel`
27:     event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);
```

- *LockingMultiRewards.sol* ( [17-17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L17-L17), [18-18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L18-L18), [19-19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L19-L19), [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L20-L20), [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L21-L21), [22-22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L22-L22), [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L23-L23), [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L24-L24), [25-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L25-L25), [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L26-L26), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L27-L27), [28-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L28-L28) ):

```solidity
/// @audit Missing @param for `reward`
17:     event LogRewardAdded(uint256 reward);

/// @audit Missing @param for `user`, `amount`
18:     event LogStaked(address indexed user, uint256 amount);

/// @audit Missing @param for `user`, `amount`, `unlockTime`, `lockCount`
19:     event LogLocked(address indexed user, uint256 amount, uint256 unlockTime, uint256 lockCount);

/// @audit Missing @param for `user`, `amount`, `index`
20:     event LogUnlocked(address indexed user, uint256 amount, uint256 index);

/// @audit Missing @param for `user`, `fromIndex`, `toIndex`
21:     event LogLockIndexChanged(address indexed user, uint256 fromIndex, uint256 toIndex);

/// @audit Missing @param for `user`, `amount`
22:     event LogWithdrawn(address indexed user, uint256 amount);

/// @audit Missing @param for `user`, `unlockTime`
23:     event LogRewardLockCreated(address indexed user, uint256 unlockTime);

/// @audit Missing @param for `user`, `rewardsToken`, `reward`
24:     event LogRewardLocked(address indexed user, address indexed rewardsToken, uint256 reward);

/// @audit Missing @param for `user`, `rewardsToken`, `reward`
25:     event LogRewardPaid(address indexed user, address indexed rewardsToken, uint256 reward);

/// @audit Missing @param for `token`, `newDuration`
26:     event LogRewardsDurationUpdated(address token, uint256 newDuration);

/// @audit Missing @param for `token`, `amount`
27:     event LogRecovered(address token, uint256 amount);

/// @audit Missing @param for `previous`, `current`
28:     event LogSetMinLockAmount(uint256 previous, uint256 current);
```

</details>

### [N-37] Constructors missing NatSpec `@param` tag

<details>
<summary>There are 29 instances (click to show):</summary>

- *BlastBox.sol* ( [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L24-L24) ):

```solidity
/// @audit Missing @param for `weth_`, `registry_`, `feeTo_`
24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
```

- *BlastGovernor.sol* ( [15-15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L15-L15) ):

```solidity
/// @audit Missing @param for `feeTo_`, `_owner`
15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```

- *BlastMagicLP.sol* ( [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L23-L23) ):

```solidity
/// @audit Missing @param for `registry_`, `feeTo_`, `owner_`
23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
```

- *BlastOnboarding.sol* ( [84-84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L84-L84) ):

```solidity
/// @audit Missing @param for `registry_`, `feeTo_`
84:     constructor(BlastTokenRegistry registry_, address feeTo_) {
```

- *BlastTokenRegistry.sol* ( [12-12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L12-L12) ):

```solidity
/// @audit Missing @param for `_owner`
12:     constructor(address _owner) Owned(_owner) {}
```

- *BlastWrappers.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L20-L20), [29-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L29-L34), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L47-L47) ):

```solidity
/// @audit Missing @param for `weth_`, `factory`, `governor_`
20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

/// @audit Missing @param for `implementation_`, `maintainerFeeRateModel_`, `owner_`, `governor_`
29:     constructor(
30:         address implementation_,
31:         IFeeRateModel maintainerFeeRateModel_,
32:         address owner_,
33:         address governor_
34:     ) Factory(implementation_, maintainerFeeRateModel_, owner_) {

/// @audit Missing @param for `box_`, `mim_`, `governor_`
47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
```

- *MagicLP.sol* ( [84-84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L84-L84) ):

```solidity
/// @audit Missing @param for `owner_`
84:     constructor(address owner_) Owned(owner_) {
```

- *FeeRateModel.sol* ( [22-22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L22-L22) ):

```solidity
/// @audit Missing @param for `maintainer_`, `owner_`
22:     constructor(address maintainer_, address owner_) Owned(owner_) {
```

- *Factory.sol* ( [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L38-L38) ):

```solidity
/// @audit Missing @param for `implementation_`, `maintainerFeeRateModel_`, `owner_`
38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
```

- *Router.sol* ( [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L38-L38) ):

```solidity
/// @audit Missing @param for `weth_`, `factory_`
38:     constructor(IWETH weth_, IFactory factory_) {
```

</details>

### [N-38] Functions missing NatSpec `@param` tag

Each function parameter should have a `@param` notation to improve the code documentation.

<details>
<summary>There are 359 instances (click to show):</summary>

- *BlastBox.sol* ( [36-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L36-L42), [56-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L56-L56), [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L68-L68), [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L72-L72), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L81-L81), [103-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L103-L103) ):

```solidity
/// @audit Missing @param for `token`
36:     function _onBeforeDeposit(
37:         IERC20 token,
38:         address /*from*/,
39:         address /*to*/,
40:         uint256 /*amount*/,
41:         uint256 /*share*/
42:     ) internal view override {

/// @audit Missing @param for `token_`
56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

/// @audit Missing @param for `data`
68:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

/// @audit Missing @param for `feeTo_`
72:     function setFeeTo(address feeTo_) external onlyOwner {

/// @audit Missing @param for `token`, `enabled`
81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {

/// @audit Missing @param for `_account`
103:     function isOwner(address _account) internal view override returns (bool) {
```

- *BlastGovernor.sol* ( [28-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L28-L28), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L32-L32), [40-40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L40-L40), [49-49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L49-L49), [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L53-L53) ):

```solidity
/// @audit Missing @param for `contractAddress`
28:     function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {

/// @audit Missing @param for `contractAddress`
32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

/// @audit Missing @param for `_feeTo`
40:     function setFeeTo(address _feeTo) external onlyOwner {

/// @audit Missing @param for `data`
49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

/// @audit Missing @param for `to`, `value`, `data`
53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

- *BlastMagicLP.sol* ( [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L72-L72), [80-80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L80-L80), [89-89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L89-L89) ):

```solidity
/// @audit Missing @param for `data`
72:     function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {

/// @audit Missing @param for `feeTo_`
80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {

/// @audit Missing @param for `operator`, `status`
89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```

- *BlastOnboarding.sol* ( [101-101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L101-L101), [123-123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L123-L123), [132-132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L132-L132), [147-147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L147-L147), [156-156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L156-L156), [164-164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L164-L164), [175-175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L175-L175), [185-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L185-L185), [190-190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L190-L190), [205-205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L205-L205) ):

```solidity
/// @audit Missing @param for `token`, `amount`, `lock_`
101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

/// @audit Missing @param for `token`, `amount`
123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

/// @audit Missing @param for `token`, `amount`
132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {

/// @audit Missing @param for `feeTo_`
147:     function setFeeTo(address feeTo_) external onlyOwner {

/// @audit Missing @param for `data`
156:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

/// @audit Missing @param for `tokens`
164:     function claimTokenYields(address[] memory tokens) external onlyOwner {

/// @audit Missing @param for `token`, `supported`
175:     function setTokenSupported(address token, bool supported) external onlyOwner {

/// @audit Missing @param for `token`, `cap`
185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

/// @audit Missing @param for `bootstrapper_`
190:     function setBootstrapper(address bootstrapper_) external onlyOwner {

/// @audit Missing @param for `token`, `to`, `amount`
205:     function rescue(address token, address to, uint256 amount) external onlyOwner {
```

- *BlastOnboardingBoot.sol* ( [55-55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L55-L55), [78-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L78-L78), [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L96-L96), [129-129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L129-L129), [137-137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L137-L137), [146-146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L146-L146), [155-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L155-L155) ):

```solidity
/// @audit Missing @param for `lock`
55:     function claim(bool lock) external returns (uint256 shares) {

/// @audit Missing @param for `user`
78:     function claimable(address user) external view returns (uint256 shares) {

/// @audit Missing @param for `minAmountOut`
96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {

/// @audit Missing @param for `_router`
129:     function initialize(Router _router) external onlyOwner {

/// @audit Missing @param for `_staking`
137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

/// @audit Missing @param for `_ready`
146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {

/// @audit Missing @param for `user`
155:     function _claimable(address user) internal view returns (uint256 shares) {
```

- *BlastTokenRegistry.sol* ( [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L14-L14) ):

```solidity
/// @audit Missing @param for `token`, `enabled`
14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```

- *BlastWrappers.sol* ( [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L59-L59) ):

```solidity
/// @audit Missing @param for `data`
59:     function init(bytes calldata data) public payable override {
```

- *BlastYields.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L20-L20), [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L29-L29), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L38-L38), [42-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L42-L42), [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L51-L51), [55-55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L55-L55), [60-60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L60-L60), [70-70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L70-L70), [75-75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L75-L75), [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L86-L86) ):

```solidity
/// @audit Missing @param for `token`
20:     function enableTokenClaimable(address token) internal {

/// @audit Missing @param for `governor_`
29:     function configureDefaultClaimables(address governor_) internal {

/// @audit Missing @param for `recipient`
38:     function claimMaxGasYields(address recipient) internal returns (uint256) {

/// @audit Missing @param for `contractAddress`, `recipient`
42:     function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {

/// @audit Missing @param for `recipient`
51:     function claimAllNativeYields(address recipient) internal returns (uint256 amount) {

/// @audit Missing @param for `contractAddress`, `recipient`
55:     function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {

/// @audit Missing @param for `contractAddress`, `amount`, `recipient`
60:     function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {

/// @audit Missing @param for `token`, `recipient`
70:     function claimAllTokenYields(address token, address recipient) internal returns (uint256 amount) {

/// @audit Missing @param for `token`, `amount`, `recipient`
75:     function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {

/// @audit Missing @param for `data`
86:     function callPrecompile(bytes calldata data) internal {
```

- *MagicLP.sol* ( [91-98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L91-L98), [167-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L167-L170), [180-183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L180-L183), [224-224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L224-L224), [244-244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L244-L244), [267-267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L267-L267), [290-290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L290-L290), [360-360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L360-L360), [413-420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L413-L420), [461-461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L461-L461), [470-479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L470-L479), [560-560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L560-L560), [581-581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L581-L581), [587-587](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L587-L587), [593-593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L593-L593) ):

```solidity
/// @audit Missing @param for `baseTokenAddress`, `quoteTokenAddress`, `lpFeeRate`, `mtFeeRateModel`, `i`, `k`
91:     function init(
92:         address baseTokenAddress,
93:         address quoteTokenAddress,
94:         uint256 lpFeeRate,
95:         address mtFeeRateModel,
96:         uint256 i,
97:         uint256 k
98:     ) external {

/// @audit Missing @param for `trader`, `payBaseAmount`
167:     function querySellBase(
168:         address trader,
169:         uint256 payBaseAmount
170:     ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {

/// @audit Missing @param for `trader`, `payQuoteAmount`
180:     function querySellQuote(
181:         address trader,
182:         uint256 payQuoteAmount
183:     ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {

/// @audit Missing @param for `user`
224:     function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {

/// @audit Missing @param for `to`
244:     function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {

/// @audit Missing @param for `to`
267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

/// @audit Missing @param for `baseAmount`, `quoteAmount`, `assetTo`, `data`
290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

/// @audit Missing @param for `to`
360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {

/// @audit Missing @param for `shareAmount`, `to`, `baseMinAmount`, `quoteMinAmount`, `data`, `deadline`
413:     function sellShares(
414:         uint256 shareAmount,
415:         address to,
416:         uint256 baseMinAmount,
417:         uint256 quoteMinAmount,
418:         bytes calldata data,
419:         uint256 deadline
420:     ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {

/// @audit Missing @param for `token`, `to`, `amount`
461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {

/// @audit Missing @param for `assetTo`, `newLpFeeRate`, `newI`, `newK`, `baseOutAmount`, `quoteOutAmount`, `minBaseReserve`, `minQuoteReserve`
470:     function setParameters(
471:         address assetTo,
472:         uint256 newLpFeeRate,
473:         uint256 newI,
474:         uint256 newK,
475:         uint256 baseOutAmount,
476:         uint256 quoteOutAmount,
477:         uint256 minBaseReserve,
478:         uint256 minQuoteReserve
479:     ) public nonReentrant onlyImplementationOwner {

/// @audit Missing @param for `baseReserve`, `quoteReserve`
560:     function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {

/// @audit Missing @param for `to`, `amount`
581:     function _transferBaseOut(address to, uint256 amount) internal {

/// @audit Missing @param for `to`, `amount`
587:     function _transferQuoteOut(address to, uint256 amount) internal {

/// @audit Missing @param for `to`, `amount`
593:     function _mint(address to, uint256 amount) internal override {
```

- *FeeRateModel.sol* ( [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L34-L34), [46-46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L46-L46) ):

```solidity
/// @audit Missing @param for `trader`, `lpFeeRate`
34:     function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {

/// @audit Missing @param for `maintainer_`
46:     function setMaintainer(address maintainer_) external onlyOwner {
```

- *FeeRateModelImpl.sol* ( [9-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L13) ):

```solidity
/// @audit Missing @param for `lpFeeRate`
9:     function getFeeRate(
10:         address /*pool*/,
11:         address /*trader*/,
12:         uint256 lpFeeRate
13:     ) external pure returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```

- *DecimalMath.sol* ( [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L23-L23), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L27-L27), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L31-L31), [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L35-L35), [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L39-L39), [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L43-L43), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L47-L47) ):

```solidity
/// @audit Missing @param for `target`, `d`
23:     function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {

/// @audit Missing @param for `target`, `d`
27:     function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {

/// @audit Missing @param for `target`, `d`
31:     function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {

/// @audit Missing @param for `target`, `d`
35:     function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {

/// @audit Missing @param for `target`
39:     function reciprocalFloor(uint256 target) internal pure returns (uint256) {

/// @audit Missing @param for `target`
43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {

/// @audit Missing @param for `target`, `e`
47:     function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```

- *Math.sol* ( [19-19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L19-L19), [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L29-L29), [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51-L51), [79-79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L79-L79), [131-131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131-L131) ):

```solidity
/// @audit Missing @param for `a`, `b`
19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

/// @audit Missing @param for `x`
29:     function sqrt(uint256 x) internal pure returns (uint256 y) {

/// @audit Missing @param for `V0`, `V1`, `V2`, `i`, `k`
51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

/// @audit Missing @param for `V1`, `delta`, `i`, `k`
79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

/// @audit Missing @param for `V0`, `V1`, `delta`, `i`, `k`
131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```

- *PMMPricing.sol* ( [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L39-L39), [76-76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L76-L76), [104-107](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L104-L107), [119-122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L119-L122), [134-137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L134-L137), [147-150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L147-L150), [162-165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L162-L165), [175-178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L175-L178), [190-190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L190-L190), [203-203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L203-L203) ):

```solidity
/// @audit Missing @param for `state`, `payBaseAmount`
39:     function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {

/// @audit Missing @param for `state`, `payQuoteAmount`
76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {

/// @audit Missing @param for `state`, `payBaseAmount`
104:     function _ROneSellBaseToken(
105:         PMMState memory state,
106:         uint256 payBaseAmount
107:     )

/// @audit Missing @param for `state`, `payQuoteAmount`
119:     function _ROneSellQuoteToken(
120:         PMMState memory state,
121:         uint256 payQuoteAmount
122:     )

/// @audit Missing @param for `state`, `payQuoteAmount`
134:     function _RBelowSellQuoteToken(
135:         PMMState memory state,
136:         uint256 payQuoteAmount
137:     )

/// @audit Missing @param for `state`, `payBaseAmount`
147:     function _RBelowSellBaseToken(
148:         PMMState memory state,
149:         uint256 payBaseAmount
150:     )

/// @audit Missing @param for `state`, `payBaseAmount`
162:     function _RAboveSellBaseToken(
163:         PMMState memory state,
164:         uint256 payBaseAmount
165:     )

/// @audit Missing @param for `state`, `payQuoteAmount`
175:     function _RAboveSellQuoteToken(
176:         PMMState memory state,
177:         uint256 payQuoteAmount
178:     )

/// @audit Missing @param for `state`
190:     function adjustedTarget(PMMState memory state) internal pure {

/// @audit Missing @param for `state`
203:     function getMidPrice(PMMState memory state) internal pure returns (uint256) {
```

- *Factory.sol* ( [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L53-L53), [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L57-L57), [65-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L65-L72), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81-L81), [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L96-L96), [105-105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L105-L105), [116-116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L116-L116), [120-126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L120-L126), [148-148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L148-L148), [155-162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L155-L162) ):

```solidity
/// @audit Missing @param for `token0`, `token1`
53:     function getPoolCount(address token0, address token1) external view returns (uint256) {

/// @audit Missing @param for `creator`
57:     function getUserPoolCount(address creator) external view returns (uint256) {

/// @audit Missing @param for `creator`, `baseToken_`, `quoteToken_`, `lpFeeRate_`, `i_`, `k_`
65:     function predictDeterministicAddress(
66:         address creator,
67:         address baseToken_,
68:         address quoteToken_,
69:         uint256 lpFeeRate_,
70:         uint256 i_,
71:         uint256 k_
72:     ) public view returns (address) {

/// @audit Missing @param for `baseToken_`, `quoteToken_`, `lpFeeRate_`, `i_`, `k_`
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

/// @audit Missing @param for `implementation_`
96:     function setLpImplementation(address implementation_) external onlyOwner {

/// @audit Missing @param for `maintainerFeeRateModel_`
105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

/// @audit Missing @param for `creator`, `baseToken`, `quoteToken`, `pool`
116:     function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {

/// @audit Missing @param for `creator`, `baseToken`, `quoteToken`, `poolIndex`, `userPoolIndex`
120:     function removePool(
121:         address creator,
122:         address baseToken,
123:         address quoteToken,
124:         uint256 poolIndex,
125:         uint256 userPoolIndex
126:     ) external onlyOwner {

/// @audit Missing @param for `creator`, `baseToken`, `quoteToken`, `pool`
148:     function _addPool(address creator, address baseToken, address quoteToken, address pool) internal {

/// @audit Missing @param for `sender_`, `baseToken_`, `quoteToken_`, `lpFeeRate_`, `i_`, `k_`
155:     function _computeSalt(
156:         address sender_,
157:         address baseToken_,
158:         address quoteToken_,
159:         uint256 lpFeeRate_,
160:         uint256 i_,
161:         uint256 k_
162:     ) internal view returns (bytes32) {
```

- *Router.sol* ( [54-63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L54-L63), [73-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L73-L81), [96-100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L96-L100), [112-116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L112-L116), [162-169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L162-L169), [178-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L178-L185), [192-199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L192-L199), [229-235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L229-L235), [251-251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L251-L251), [261-268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L261-L268), [274-281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L274-L281), [314-321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L314-L321), [336-342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L336-L342), [365-372](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L365-L372), [404-410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L404-L410), [415-420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L415-L420), [432-438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L432-L438), [449-455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L449-L455), [461-466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L461-L466), [478-484](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L478-L484), [499-499](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L499-L499), [509-513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L509-L513), [541-541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L541-L541), [571-571](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L571-L571), [578-578](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L578-L578), [586-586](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L586-L586), [598-598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L598-L598) ):

```solidity
/// @audit Missing @param for `baseToken`, `quoteToken`, `lpFeeRate`, `i`, `k`, `to`, `baseInAmount`, `quoteInAmount`
54:     function createPool(
55:         address baseToken,
56:         address quoteToken,
57:         uint256 lpFeeRate,
58:         uint256 i,
59:         uint256 k,
60:         address to,
61:         uint256 baseInAmount,
62:         uint256 quoteInAmount
63:     ) external returns (address clone, uint256 shares) {

/// @audit Missing @param for `token`, `useTokenAsQuote`, `lpFeeRate`, `i`, `k`, `to`, `tokenInAmount`
73:     function createPoolETH(
74:         address token,
75:         bool useTokenAsQuote,
76:         uint256 lpFeeRate,
77:         uint256 i,
78:         uint256 k,
79:         address to,
80:         uint256 tokenInAmount
81:     ) external payable returns (address clone, uint256 shares) {

/// @audit Missing @param for `i`, `baseInAmount`, `quoteInAmount`
96:     function previewCreatePool(
97:         uint256 i,
98:         uint256 baseInAmount,
99:         uint256 quoteInAmount
100:     ) external pure returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

/// @audit Missing @param for `lp`, `baseInAmount`, `quoteInAmount`
112:     function previewAddLiquidity(
113:         address lp,
114:         uint256 baseInAmount,
115:         uint256 quoteInAmount
116:     ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

/// @audit Missing @param for `lp`, `to`, `baseInAmount`, `quoteInAmount`, `minimumShares`, `deadline`
162:     function addLiquidity(
163:         address lp,
164:         address to,
165:         uint256 baseInAmount,
166:         uint256 quoteInAmount,
167:         uint256 minimumShares,
168:         uint256 deadline
169:     ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

/// @audit Missing @param for `lp`, `to`, `baseInAmount`, `quoteInAmount`, `minimumShares`, `deadline`
178:     function addLiquidityUnsafe(
179:         address lp,
180:         address to,
181:         uint256 baseInAmount,
182:         uint256 quoteInAmount,
183:         uint256 minimumShares,
184:         uint256 deadline
185:     ) external ensureDeadline(deadline) returns (uint256 shares) {

/// @audit Missing @param for `lp`, `to`, `refundTo`, `tokenInAmount`, `minimumShares`, `deadline`
192:     function addLiquidityETH(
193:         address lp,
194:         address to,
195:         address payable refundTo,
196:         uint256 tokenInAmount,
197:         uint256 minimumShares,
198:         uint256 deadline
199:     ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

/// @audit Missing @param for `lp`, `to`, `tokenInAmount`, `minimumShares`, `deadline`
229:     function addLiquidityETHUnsafe(
230:         address lp,
231:         address to,
232:         uint256 tokenInAmount,
233:         uint256 minimumShares,
234:         uint256 deadline
235:     ) external payable ensureDeadline(deadline) returns (uint256 shares) {

/// @audit Missing @param for `lp`, `sharesIn`
251:     function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

/// @audit Missing @param for `lp`, `to`, `sharesIn`, `minimumBaseAmount`, `minimumQuoteAmount`, `deadline`
261:     function removeLiquidity(
262:         address lp,
263:         address to,
264:         uint256 sharesIn,
265:         uint256 minimumBaseAmount,
266:         uint256 minimumQuoteAmount,
267:         uint256 deadline
268:     ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

/// @audit Missing @param for `lp`, `to`, `sharesIn`, `minimumETHAmount`, `minimumTokenAmount`, `deadline`
274:     function removeLiquidityETH(
275:         address lp,
276:         address to,
277:         uint256 sharesIn,
278:         uint256 minimumETHAmount,
279:         uint256 minimumTokenAmount,
280:         uint256 deadline
281:     ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {

/// @audit Missing @param for `to`, `amountIn`, `path`, `directions`, `minimumOut`, `deadline`
314:     function swapTokensForTokens(
315:         address to,
316:         uint256 amountIn,
317:         address[] calldata path,
318:         uint256 directions,
319:         uint256 minimumOut,
320:         uint256 deadline
321:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit Missing @param for `to`, `path`, `directions`, `minimumOut`, `deadline`
336:     function swapETHForTokens(
337:         address to,
338:         address[] calldata path,
339:         uint256 directions,
340:         uint256 minimumOut,
341:         uint256 deadline
342:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit Missing @param for `to`, `amountIn`, `path`, `directions`, `minimumOut`, `deadline`
365:     function swapTokensForETH(
366:         address to,
367:         uint256 amountIn,
368:         address[] calldata path,
369:         uint256 directions,
370:         uint256 minimumOut,
371:         uint256 deadline
372:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit Missing @param for `lp`, `to`, `amountIn`, `minimumOut`, `deadline`
404:     function sellBaseTokensForTokens(
405:         address lp,
406:         address to,
407:         uint256 amountIn,
408:         uint256 minimumOut,
409:         uint256 deadline
410:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit Missing @param for `lp`, `to`, `minimumOut`, `deadline`
415:     function sellBaseETHForTokens(
416:         address lp,
417:         address to,
418:         uint256 minimumOut,
419:         uint256 deadline
420:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit Missing @param for `lp`, `to`, `amountIn`, `minimumOut`, `deadline`
432:     function sellBaseTokensForETH(
433:         address lp,
434:         address to,
435:         uint256 amountIn,
436:         uint256 minimumOut,
437:         uint256 deadline
438:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit Missing @param for `lp`, `to`, `amountIn`, `minimumOut`, `deadline`
449:     function sellQuoteTokensForTokens(
450:         address lp,
451:         address to,
452:         uint256 amountIn,
453:         uint256 minimumOut,
454:         uint256 deadline
455:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit Missing @param for `lp`, `to`, `minimumOut`, `deadline`
461:     function sellQuoteETHForTokens(
462:         address lp,
463:         address to,
464:         uint256 minimumOut,
465:         uint256 deadline
466:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit Missing @param for `lp`, `to`, `amountIn`, `minimumOut`, `deadline`
478:     function sellQuoteTokensForETH(
479:         address lp,
480:         address to,
481:         uint256 amountIn,
482:         uint256 minimumOut,
483:         uint256 deadline
484:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit Missing @param for `lp`, `to`, `minimumShares`
499:     function _addLiquidity(address lp, address to, uint256 minimumShares) internal returns (uint256 shares) {

/// @audit Missing @param for `lp`, `baseInAmount`, `quoteInAmount`
509:     function _adjustAddLiquidity(
510:         address lp,
511:         uint256 baseInAmount,
512:         uint256 quoteInAmount
513:     ) internal view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount) {

/// @audit Missing @param for `to`, `path`, `directions`, `minimumOut`
541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

/// @audit Missing @param for `lp`, `to`, `minimumOut`
571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

/// @audit Missing @param for `lp`, `to`, `minimumOut`
578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

/// @audit Missing @param for `path`
586:     function _validatePath(address[] calldata path) internal pure {

/// @audit Missing @param for `baseDecimals`, `quoteDecimals`
598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {
```

</details>

### [N-39] Modifiers missing NatSpec `@param` tag

Each modifier parameter should have a `@param` notation to improve the code documentation.

There are 3 instances:

- *BlastOnboarding.sol* ( [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L43-L43), [50-50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L50-L50) ):

```solidity
/// @audit Missing @param for `_state`
43:     modifier onlyState(State _state) {

/// @audit Missing @param for `token`
50:     modifier onlySupportedTokens(address token) {
```

- *Router.sol* ( [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L47-L47) ):

```solidity
/// @audit Missing @param for `deadline`
47:     modifier ensureDeadline(uint256 deadline) {
```

### [N-40] NatSpec: Non-public state variable declarations should use `@dev` tags

i.e. `@dev` [tags](https://docs.soliditylang.org/en/latest/natspec-format.html#tags). Note that since they're non-public, `@notice` is not the right tag to use.

<details>
<summary>There are 13 instances (click to show):</summary>

- *BlastWrappers.sol* ( [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L45) ):

```solidity
45:     address private immutable _governor;
```

- *BlastYields.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L14) ):

```solidity
14:     IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);
```

- *MagicLP.sol* ( [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L68) ):

```solidity
68:     bool internal _INITIALIZED_;
```

- *DecimalMath.sol* ( [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L21) ):

```solidity
20:     uint256 internal constant ONE = 10 ** 18;

21:     uint256 internal constant ONE2 = 10 ** 36;
```

- *LockingMultiRewards.sol* ( [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L78), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L79), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L80), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L81), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L89), [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L90), [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L91), [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L92) ):

```solidity
78:     uint256 private constant BIPS = 10_000;

79:     uint256 private constant MAX_NUM_REWARDS = 5;

80:     uint256 private constant MIN_LOCK_DURATION = 1 weeks;

81:     uint256 private constant MIN_REWARDS_DURATION = 1 days;

89:     mapping(address token => Reward info) private _rewardData;

90:     mapping(address user => Balances balances) private _balances;

91:     mapping(address user => LockedBalance[] locks) private _userLocks;

92:     mapping(address user => RewardLock rewardLock) private _userRewardLock;
```

</details>

### [N-41] Functions missing NatSpec `@return` tag

Functions missing NatSpec `@return` tag

<details>
<summary>There are 119 instances (click to show):</summary>

- *BlastBox.sol* ( [52-52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L52-L52), [56-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L56-L56), [103-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L103-L103) ):

```solidity
52:     function claimGasYields() external onlyOperators returns (uint256) {

56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

103:     function isOwner(address _account) internal view override returns (bool) {
```

- *BlastGovernor.sol* ( [28-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L28-L28), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L32-L32), [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L53-L53) ):

```solidity
28:     function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

- *BlastMagicLP.sol* ( [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L39-L39), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L47-L47), [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L53-L53) ):

```solidity
39:     function version() external pure override returns (string memory) {

47:     function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {

53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {
```

- *BlastOnboarding.sol* ( [160-160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L160-L160), [226-226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L226-L226) ):

```solidity
160:     function claimGasYields() external onlyOwner returns (uint256) {

226:     function _implementation() internal view override returns (address) {
```

- *BlastOnboardingBoot.sol* ( [55-55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L55-L55), [78-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L78-L78), [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L86-L86), [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L96-L96), [155-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L155-L155) ):

```solidity
55:     function claim(bool lock) external returns (uint256 shares) {

78:     function claimable(address user) external view returns (uint256 shares) {

86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {

155:     function _claimable(address user) internal view returns (uint256 shares) {
```

- *BlastYields.sol* ( [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L38-L38), [42-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L42-L42), [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L51-L51), [55-55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L55-L55), [60-60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L60-L60), [70-70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L70-L70), [75-75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L75-L75) ):

```solidity
38:     function claimMaxGasYields(address recipient) internal returns (uint256) {

42:     function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {

51:     function claimAllNativeYields(address recipient) internal returns (uint256 amount) {

55:     function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {

60:     function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {

70:     function claimAllTokenYields(address token, address recipient) internal returns (uint256 amount) {

75:     function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {
```

- *MagicLP.sol* ( [155-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L155-L155), [159-159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L159-L159), [163-163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L163-L163), [167-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L167-L170), [180-183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L180-L183), [193-193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L193-L193), [204-204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204-L204), [215-215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L215-L215), [219-219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L219-L219), [224-224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L224-L224), [228-228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L228-L228), [232-232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L232-L232), [236-236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L236-L236), [244-244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L244-L244), [267-267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L267-L267), [360-360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L360-L360), [413-420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L413-L420), [528-528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L528-L528) ):

```solidity
155:     function name() public view override returns (string memory) {

159:     function symbol() public pure override returns (string memory) {

163:     function decimals() public view override returns (uint8) {

167:     function querySellBase(
168:         address trader,
169:         uint256 payBaseAmount
170:     ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {

180:     function querySellQuote(
181:         address trader,
182:         uint256 payQuoteAmount
183:     ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {

193:     function getPMMState() public view returns (PMMPricing.PMMState memory state) {

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

215:     function getMidPrice() public view returns (uint256 midPrice) {

219:     function getReserves() external view returns (uint256 baseReserve, uint256 quoteReserve) {

224:     function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {

228:     function getBaseInput() public view returns (uint256 input) {

232:     function getQuoteInput() public view returns (uint256 input) {

236:     function version() external pure virtual returns (string memory) {

244:     function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {

267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {

413:     function sellShares(
414:         uint256 shareAmount,
415:         address to,
416:         uint256 baseMinAmount,
417:         uint256 quoteMinAmount,
418:         bytes calldata data,
419:         uint256 deadline
420:     ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {

528:     function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {
```

- *FeeRateModel.sol* ( [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L34-L34) ):

```solidity
34:     function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```

- *FeeRateModelImpl.sol* ( [9-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L13) ):

```solidity
9:     function getFeeRate(
10:         address /*pool*/,
11:         address /*trader*/,
12:         uint256 lpFeeRate
13:     ) external pure returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```

- *DecimalMath.sol* ( [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L23-L23), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L27-L27), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L31-L31), [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L35-L35), [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L39-L39), [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L43-L43), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L47-L47) ):

```solidity
23:     function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {

27:     function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {

31:     function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {

35:     function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {

39:     function reciprocalFloor(uint256 target) internal pure returns (uint256) {

43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {

47:     function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```

- *Math.sol* ( [19-19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L19-L19), [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L29-L29), [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51-L51), [79-79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L79-L79), [131-131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131-L131) ):

```solidity
19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

29:     function sqrt(uint256 x) internal pure returns (uint256 y) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```

- *PMMPricing.sol* ( [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L39-L39), [76-76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L76-L76), [104-112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L104-L112), [119-127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L119-L127), [134-142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L134-L142), [147-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L147-L155), [162-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L162-L170), [175-183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L175-L183), [203-203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L203-L203) ):

```solidity
39:     function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {

76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {

104:     function _ROneSellBaseToken(
105:         PMMState memory state,
106:         uint256 payBaseAmount
107:     )
108:         internal
109:         pure
110:         returns (
111:             uint256 // receiveQuoteToken
112:         )

119:     function _ROneSellQuoteToken(
120:         PMMState memory state,
121:         uint256 payQuoteAmount
122:     )
123:         internal
124:         pure
125:         returns (
126:             uint256 // receiveBaseToken
127:         )

134:     function _RBelowSellQuoteToken(
135:         PMMState memory state,
136:         uint256 payQuoteAmount
137:     )
138:         internal
139:         pure
140:         returns (
141:             uint256 // receiveBaseToken
142:         )

147:     function _RBelowSellBaseToken(
148:         PMMState memory state,
149:         uint256 payBaseAmount
150:     )
151:         internal
152:         pure
153:         returns (
154:             uint256 // receiveQuoteToken
155:         )

162:     function _RAboveSellBaseToken(
163:         PMMState memory state,
164:         uint256 payBaseAmount
165:     )
166:         internal
167:         pure
168:         returns (
169:             uint256 // receiveQuoteToken
170:         )

175:     function _RAboveSellQuoteToken(
176:         PMMState memory state,
177:         uint256 payQuoteAmount
178:     )
179:         internal
180:         pure
181:         returns (
182:             uint256 // receiveBaseToken
183:         )

203:     function getMidPrice(PMMState memory state) internal pure returns (uint256) {
```

- *Factory.sol* ( [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L53-L53), [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L57-L57), [65-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L65-L72), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81-L81), [155-162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L155-L162) ):

```solidity
53:     function getPoolCount(address token0, address token1) external view returns (uint256) {

57:     function getUserPoolCount(address creator) external view returns (uint256) {

65:     function predictDeterministicAddress(
66:         address creator,
67:         address baseToken_,
68:         address quoteToken_,
69:         uint256 lpFeeRate_,
70:         uint256 i_,
71:         uint256 k_
72:     ) public view returns (address) {

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

155:     function _computeSalt(
156:         address sender_,
157:         address baseToken_,
158:         address quoteToken_,
159:         uint256 lpFeeRate_,
160:         uint256 i_,
161:         uint256 k_
162:     ) internal view returns (bytes32) {
```

- *Router.sol* ( [54-63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L54-L63), [73-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L73-L81), [96-100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L96-L100), [112-116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L112-L116), [162-169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L162-L169), [178-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L178-L185), [192-199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L192-L199), [229-235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L229-L235), [251-251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L251-L251), [261-268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L261-L268), [274-281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L274-L281), [314-321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L314-L321), [336-342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L336-L342), [365-372](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L365-L372), [404-410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L404-L410), [415-420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L415-L420), [432-438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L432-L438), [449-455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L449-L455), [461-466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L461-L466), [478-484](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L478-L484), [499-499](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L499-L499), [509-513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L509-L513), [541-541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L541-L541), [571-571](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L571-L571), [578-578](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L578-L578) ):

```solidity
54:     function createPool(
55:         address baseToken,
56:         address quoteToken,
57:         uint256 lpFeeRate,
58:         uint256 i,
59:         uint256 k,
60:         address to,
61:         uint256 baseInAmount,
62:         uint256 quoteInAmount
63:     ) external returns (address clone, uint256 shares) {

73:     function createPoolETH(
74:         address token,
75:         bool useTokenAsQuote,
76:         uint256 lpFeeRate,
77:         uint256 i,
78:         uint256 k,
79:         address to,
80:         uint256 tokenInAmount
81:     ) external payable returns (address clone, uint256 shares) {

96:     function previewCreatePool(
97:         uint256 i,
98:         uint256 baseInAmount,
99:         uint256 quoteInAmount
100:     ) external pure returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

112:     function previewAddLiquidity(
113:         address lp,
114:         uint256 baseInAmount,
115:         uint256 quoteInAmount
116:     ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

162:     function addLiquidity(
163:         address lp,
164:         address to,
165:         uint256 baseInAmount,
166:         uint256 quoteInAmount,
167:         uint256 minimumShares,
168:         uint256 deadline
169:     ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

178:     function addLiquidityUnsafe(
179:         address lp,
180:         address to,
181:         uint256 baseInAmount,
182:         uint256 quoteInAmount,
183:         uint256 minimumShares,
184:         uint256 deadline
185:     ) external ensureDeadline(deadline) returns (uint256 shares) {

192:     function addLiquidityETH(
193:         address lp,
194:         address to,
195:         address payable refundTo,
196:         uint256 tokenInAmount,
197:         uint256 minimumShares,
198:         uint256 deadline
199:     ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

229:     function addLiquidityETHUnsafe(
230:         address lp,
231:         address to,
232:         uint256 tokenInAmount,
233:         uint256 minimumShares,
234:         uint256 deadline
235:     ) external payable ensureDeadline(deadline) returns (uint256 shares) {

251:     function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

261:     function removeLiquidity(
262:         address lp,
263:         address to,
264:         uint256 sharesIn,
265:         uint256 minimumBaseAmount,
266:         uint256 minimumQuoteAmount,
267:         uint256 deadline
268:     ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

274:     function removeLiquidityETH(
275:         address lp,
276:         address to,
277:         uint256 sharesIn,
278:         uint256 minimumETHAmount,
279:         uint256 minimumTokenAmount,
280:         uint256 deadline
281:     ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {

314:     function swapTokensForTokens(
315:         address to,
316:         uint256 amountIn,
317:         address[] calldata path,
318:         uint256 directions,
319:         uint256 minimumOut,
320:         uint256 deadline
321:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

336:     function swapETHForTokens(
337:         address to,
338:         address[] calldata path,
339:         uint256 directions,
340:         uint256 minimumOut,
341:         uint256 deadline
342:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

365:     function swapTokensForETH(
366:         address to,
367:         uint256 amountIn,
368:         address[] calldata path,
369:         uint256 directions,
370:         uint256 minimumOut,
371:         uint256 deadline
372:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

404:     function sellBaseTokensForTokens(
405:         address lp,
406:         address to,
407:         uint256 amountIn,
408:         uint256 minimumOut,
409:         uint256 deadline
410:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

415:     function sellBaseETHForTokens(
416:         address lp,
417:         address to,
418:         uint256 minimumOut,
419:         uint256 deadline
420:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

432:     function sellBaseTokensForETH(
433:         address lp,
434:         address to,
435:         uint256 amountIn,
436:         uint256 minimumOut,
437:         uint256 deadline
438:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

449:     function sellQuoteTokensForTokens(
450:         address lp,
451:         address to,
452:         uint256 amountIn,
453:         uint256 minimumOut,
454:         uint256 deadline
455:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

461:     function sellQuoteETHForTokens(
462:         address lp,
463:         address to,
464:         uint256 minimumOut,
465:         uint256 deadline
466:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

478:     function sellQuoteTokensForETH(
479:         address lp,
480:         address to,
481:         uint256 amountIn,
482:         uint256 minimumOut,
483:         uint256 deadline
484:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

499:     function _addLiquidity(address lp, address to, uint256 minimumShares) internal returns (uint256 shares) {

509:     function _adjustAddLiquidity(
510:         address lp,
511:         uint256 baseInAmount,
512:         uint256 quoteInAmount
513:     ) internal view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount) {

541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {
```

- *MagicLpAggregator.sol* ( [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L29-L29), [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L33-L33), [37-37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L37-L37), [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L48-L48) ):

```solidity
29:     function decimals() external pure override returns (uint8) {

33:     function _getReserves() internal view virtual returns (uint256, uint256) {

37:     function latestAnswer() public view override returns (int256) {

48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```

- *LockingMultiRewards.sol* ( [199-199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L199-L199), [203-203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L203-L203), [207-207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L207-L207), [211-211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L211-L211), [215-215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L215-L215), [219-219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L219-L219), [223-223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L223-L223), [227-227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L227-L227), [231-231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L231-L231), [235-235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L235-L235), [239-239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L239-L239), [253-253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L253-L253), [257-257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L257-L257), [261-261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L261-L261), [265-265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L265-L265), [269-269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L269-L269), [273-273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L273-L273), [277-277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L277-L277), [288-288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L288-L288), [292-292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L292-L292), [528-528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L528-L528) ):

```solidity
199:     function rewardData(address token) external view returns (Reward memory) {

203:     function rewardsForDuration(address rewardToken) external view returns (uint256) {

207:     function rewardTokensLength() external view returns (uint256) {

211:     function balances(address user) external view returns (Balances memory) {

215:     function userRewardLock(address user) external view returns (RewardLock memory) {

219:     function userLocks(address user) external view returns (LockedBalance[] memory) {

223:     function userLocksLength(address user) external view returns (uint256) {

227:     function locked(address user) external view returns (uint256) {

231:     function unlocked(address user) external view returns (uint256) {

235:     function totalSupply() public view returns (uint256) {

239:     function balanceOf(address user) public view returns (uint256) {

253:     function nextUnlockTime() public view returns (uint256) {

257:     function epoch() public view returns (uint256) {

261:     function nextEpoch() public view returns (uint256) {

265:     function remainingEpochTime() public view returns (uint256) {

269:     function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {

273:     function rewardPerToken(address rewardToken) public view returns (uint256) {

277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

288:     function earned(address user, address rewardToken) public view returns (uint256) {

292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {
```

</details>

### [N-42] State variables should have NatSpec descriptions

It is [recommended](https://docs.soliditylang.org/en/v0.8.20/natspec-format.html#tags) to use the NatSpec tags `@notice`, `@dev`, `@return`, `@inheritdoc` for public state variables, and `@dev` for non-public state variables.

<details>
<summary>There are 52 instances (click to show):</summary>

- *BlastBox.sol* ( [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L21), [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L22) ):

```solidity
21:     mapping(address => bool) public enabledTokens;

22:     address public feeTo;
```

- *BlastGovernor.sol* ( [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L11) ):

```solidity
11:     address public feeTo;
```

- *BlastMagicLP.sol* ( [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L21) ):

```solidity
21:     mapping(address => bool) public operators;
```

- *BlastOnboarding.sol* ( [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L30), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L31), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L33), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L36), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L37), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L38), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L41) ):

```solidity
30:     State public state;

31:     address public bootstrapper;

32:     address public feeTo;

33:     BlastTokenRegistry public registry;

36:     mapping(address token => bool) public supportedTokens;

37:     mapping(address token => Balances) public totals;

38:     mapping(address token => uint256 cap) public caps;

41:     mapping(address user => mapping(address token => Balances)) public balances;
```

- *BlastOnboardingBoot.sol* ( [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L24), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L26), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L27), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L28), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L29), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L30) ):

```solidity
24:     address public pool;

25:     Router public router;

26:     IFactory public factory;

27:     uint256 public totalPoolShares;

28:     bool public ready;

29:     LockingMultiRewards public staking;

30:     mapping(address user => bool claimed) public claimed;
```

- *BlastTokenRegistry.sol* ( [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L10) ):

```solidity
10:     mapping(address => bool) public nativeYieldTokens;
```

- *MagicLP.sol* ( [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L68), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L70), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L71), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L74), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L75), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L76), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L77), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L78), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L79), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L80), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L81), [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L82) ):

```solidity
68:     bool internal _INITIALIZED_;

70:     address public _BASE_TOKEN_;

71:     address public _QUOTE_TOKEN_;

72:     uint112 public _BASE_RESERVE_;

73:     uint112 public _QUOTE_RESERVE_;

74:     uint32 public _BLOCK_TIMESTAMP_LAST_;

75:     uint256 public _BASE_PRICE_CUMULATIVE_LAST_;

76:     uint112 public _BASE_TARGET_;

77:     uint112 public _QUOTE_TARGET_;

78:     uint32 public _RState_;

79:     IFeeRateModel public _MT_FEE_RATE_MODEL_;

80:     uint256 public _LP_FEE_RATE_;

81:     uint256 public _K_;

82:     uint256 public _I_;
```

- *FeeRateModel.sol* ( [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L19), [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L20) ):

```solidity
19:     address public maintainer;

20:     address public implementation;
```

- *Factory.sol* ( [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L33), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L35), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L36) ):

```solidity
32:     address public implementation;

33:     IFeeRateModel public maintainerFeeRateModel;

35:     mapping(address base => mapping(address quote => address[] pools)) public pools;

36:     mapping(address creator => address[] pools) public userPools;
```

- *LockingMultiRewards.sol* ( [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L89), [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L90), [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L91), [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L92), [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L94), [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L95), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L96), [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L98), [100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L100), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L101), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L102), [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L103) ):

```solidity
89:     mapping(address token => Reward info) private _rewardData;

90:     mapping(address user => Balances balances) private _balances;

91:     mapping(address user => LockedBalance[] locks) private _userLocks;

92:     mapping(address user => RewardLock rewardLock) private _userRewardLock;

94:     mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;

95:     mapping(address user => mapping(address token => uint256 amount)) public rewards;

96:     mapping(address user => uint256 index) public lastLockIndex;

98:     address[] public rewardTokens;

100:     uint256 public lockedSupply; // all locked boosted deposits

101:     uint256 public unlockedSupply; // all unlocked unboosted deposits

102:     uint256 public minLockAmount; // minimum amount allowed to lock

103:     uint256 public stakingTokenBalance; // total staking token balance
```

</details>

### [N-43] Structs missing NatSpec `@param` tag

<details>
<summary>There are 23 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [24-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L24-L28) ):

```solidity
/// @audit Missing @param for `unlocked`, `locked`, `total`
24:     struct Balances {
25:         uint256 unlocked;
26:         uint256 locked;
27:         uint256 total;
28:     }
```

- *PMMPricing.sol* ( [27-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L27-L35) ):

```solidity
/// @audit Missing @param for `i`, `K`, `B`, `Q`, `B0`, `Q0`, `R`
27:     struct PMMState {
28:         uint256 i;
29:         uint256 K;
30:         uint256 B;
31:         uint256 Q;
32:         uint256 B0;
33:         uint256 Q0;
34:         RState R;
35:     }
```

- *LockingMultiRewards.sol* ( [50-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L50-L56), [58-61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L58-L61), [63-66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L63-L66), [68-71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L68-L71), [73-76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L73-L76) ):

```solidity
/// @audit Missing @param for `periodFinish`, `rewardRate`, `rewardPerTokenStored`, `exists`, `lastUpdateTime`
50:     struct Reward {
51:         uint256 periodFinish;
52:         uint256 rewardRate;
53:         uint256 rewardPerTokenStored;
54:         bool exists;
55:         uint248 lastUpdateTime;
56:     }

/// @audit Missing @param for `unlocked`, `locked`
58:     struct Balances {
59:         uint256 unlocked;
60:         uint256 locked;
61:     }

/// @audit Missing @param for `amount`, `unlockTime`
63:     struct LockedBalance {
64:         uint256 amount;
65:         uint256 unlockTime;
66:     }

/// @audit Missing @param for `token`, `amount`
68:     struct RewardLockItem {
69:         address token;
70:         uint256 amount;
71:     }

/// @audit Missing @param for `items`, `unlockTime`
73:     struct RewardLock {
74:         RewardLockItem[] items;
75:         uint256 unlockTime;
76:     }
```

</details>

### [N-44] Functions should be named in mixedCase style

As the [Solidity Style Guide](https://docs.soliditylang.org/en/v0.8.21/style-guide.html#function-names) suggests: functions should be named in mixedCase style.

<details>
<summary>There are 12 instances (click to show):</summary>

- *MagicLP.sol* ( [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L138), [193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L193), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204) ):

```solidity
138:     function correctRState() external {

193:     function getPMMState() public view returns (PMMPricing.PMMState memory state) {

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
```

- *Math.sol* ( [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L79), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131) ):

```solidity
51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```

- *PMMPricing.sol* ( [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L104), [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L119), [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L134), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L147), [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L162), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L175) ):

```solidity
104:     function _ROneSellBaseToken(

119:     function _ROneSellQuoteToken(

134:     function _RBelowSellQuoteToken(

147:     function _RBelowSellBaseToken(

162:     function _RAboveSellBaseToken(

175:     function _RAboveSellQuoteToken(
```

</details>

### [N-45] Variable names for `immutable`s should use UPPER_CASE_WITH_UNDERSCORES

For `immutable` variable names, each word should use all capital letters, with underscores separating each word (UPPER_CASE_WITH_UNDERSCORES)

<details>
<summary>There are 16 instances (click to show):</summary>

- *BlastBox.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L20-L20) ):

```solidity
20:     BlastTokenRegistry public immutable registry;
```

- *BlastMagicLP.sol* ( [17-17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L17-L17) ):

```solidity
17:     BlastTokenRegistry public immutable registry;
```

- *BlastWrappers.sol* ( [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L45-L45) ):

```solidity
45:     address private immutable _governor;
```

- *MagicLP.sol* ( [61-61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L61-L61) ):

```solidity
61:     MagicLP public immutable implementation;
```

- *Router.sol* ( [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L33-L33), [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L34-L34) ):

```solidity
33:     IWETH public immutable weth;

34:     IFactory public immutable factory;
```

- *MagicLpAggregator.sol* ( [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L10-L10), [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L11-L11), [12-12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L12-L12), [13-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L13-L13), [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L14-L14) ):

```solidity
10:     IMagicLP public immutable pair;

11:     IAggregator public immutable baseOracle;

12:     IAggregator public immutable quoteOracle;

13:     uint8 public immutable baseDecimals;

14:     uint8 public immutable quoteDecimals;
```

- *LockingMultiRewards.sol* ( [83-83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L83-L83), [84-84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L84-L84), [85-85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L85-L85), [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L86-L86), [87-87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L87-L87) ):

```solidity
83:     uint256 public immutable maxLocks;

84:     uint256 public immutable lockingBoostMultiplerInBips;

85:     uint256 public immutable rewardsDuration;

86:     uint256 public immutable lockDuration;

87:     address public immutable stakingToken;
```

</details>

### [N-46] Variables should be named in mixedCase style

As the [Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html#naming-styles) suggests: arguments, local variables and mutable state variables should be named in mixedCase style.

<details>
<summary>There are 36 instances (click to show):</summary>

- *MagicLP.sol* ( [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L34-L34), [36-36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L36-L36), [36-36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L36-L36), [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L68-L68), [170-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L170-L170), [183-183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L183-L183), [204-204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204-L204), [204-204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204-L204), [204-204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204-L204), [204-204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204-L204), [204-204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204-L204), [204-204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204-L204), [249-249](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L249-L249), [272-272](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L272-L272), [310-310](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L310-L310), [332-332](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L332-L332), [473-473](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L473-L473), [474-474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L474-L474) ):

```solidity
/// @audit newRState
34:     event RChange(PMMPricing.RState newRState);

/// @audit newI
36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);

/// @audit newK
36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);

/// @audit _INITIALIZED_
68:     bool internal _INITIALIZED_;

/// @audit newRState
170:     ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {

/// @audit newRState
183:     ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {

/// @audit K
204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

/// @audit B
204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

/// @audit Q
204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

/// @audit B0
204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

/// @audit Q0
204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

/// @audit R
204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

/// @audit newRState
249:         PMMPricing.RState newRState;

/// @audit newRState
272:         PMMPricing.RState newRState;

/// @audit newRState
310:             (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) = querySellQuote(

/// @audit newRState
332:             (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) = querySellBase(

/// @audit newI
473:         uint256 newI,

/// @audit newK
474:         uint256 newK,
```

- *Math.sol* ( [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51-L51), [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51-L51), [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51-L51), [62-62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L62-L62), [79-79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L79-L79), [131-131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131-L131), [131-131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131-L131), [199-199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L199-L199) ):

```solidity
/// @audit V0
51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

/// @audit V1
51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

/// @audit V2
51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

/// @audit V0V0V1V2
62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

/// @audit V1
79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

/// @audit V0
131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

/// @audit V1
131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

/// @audit V2
199:         uint256 V2 = DecimalMath.divCeil(numerator, denominator);
```

- *PMMPricing.sol* ( [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L29-L29), [30-30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L30-L30), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L31-L31), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L32-L32), [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L33-L33), [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L34-L34), [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L39-L39), [76-76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L76-L76), [205-205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L205-L205), [209-209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L209-L209) ):

```solidity
/// @audit K
29:         uint256 K;

/// @audit B
30:         uint256 B;

/// @audit Q
31:         uint256 Q;

/// @audit B0
32:         uint256 B0;

/// @audit Q0
33:         uint256 Q0;

/// @audit R
34:         RState R;

/// @audit newR
39:     function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {

/// @audit newR
76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {

/// @audit R
205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);

/// @audit R
209:             uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
```

</details>

### [N-47] Names of `public`/`external` functions and state variables should NOT be prefixed with underscore

It is recommended by the [Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html#underscore-prefix-for-non-external-functions-and-variables).

<details>
<summary>There are 14 instances (click to show):</summary>

- *MagicLP.sol* ( [70-70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L70-L70), [71-71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L71-L71), [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L72-L72), [73-73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L73-L73), [74-74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L74-L74), [75-75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L75-L75), [76-76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L76-L76), [77-77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L77-L77), [78-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L78-L78), [79-79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L79-L79), [80-80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L80-L80), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L81-L81), [82-82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L82-L82) ):

```solidity
70:     address public _BASE_TOKEN_;

71:     address public _QUOTE_TOKEN_;

72:     uint112 public _BASE_RESERVE_;

73:     uint112 public _QUOTE_RESERVE_;

74:     uint32 public _BLOCK_TIMESTAMP_LAST_;

75:     uint256 public _BASE_PRICE_CUMULATIVE_LAST_;

76:     uint112 public _BASE_TARGET_;

77:     uint112 public _QUOTE_TARGET_;

78:     uint32 public _RState_;

79:     IFeeRateModel public _MT_FEE_RATE_MODEL_;

80:     uint256 public _LP_FEE_RATE_;

81:     uint256 public _K_;

82:     uint256 public _I_;
```

- *LockingMultiRewards.sol* ( [277-277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L277-L277) ):

```solidity
277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
```

</details>

### [N-48] Order of contract layout does not follow the Solidity Style Guide

As suggested by the [Solidity Style Guide](https://docs.soliditylang.org/en/v0.8.20/style-guide.html#order-of-layout):
- Layout contract elements in the following order: `pragma statements`, `import statements`, `interfaces`, `libraries`, `contracts`.
- Inside each contract, library or interface, use the following order: `type declarations`, `state variables`, `events`, `errors`, `modifiers`, `functions`.

<details>
<summary>There are 15 instances (click to show):</summary>

- *BlastBox.sol* ( [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L20) ):

```solidity
/// @audit ↑ Out of order with error ErrUnsupportedToken
20:     BlastTokenRegistry public immutable registry;
```

- *BlastGovernor.sol* ( [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L11) ):

```solidity
/// @audit ↑ Out of order with error ErrZeroAddress
11:     address public feeTo;
```

- *BlastMagicLP.sol* ( [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L17), [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L118) ):

```solidity
/// @audit ↑ Out of order with error ErrNotAllowedImplementationOperator
17:     BlastTokenRegistry public immutable registry;

/// @audit ↑ Out of order with function _updateTokenClaimables()
118:     modifier onlyImplementationOperators() {
```

- *BlastOnboarding.sol* ( [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L18) ):

```solidity
/// @audit ↑ Out of order with error ErrNotAllowed
18:     enum State {
```

- *BlastTokenRegistry.sol* ( [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L10) ):

```solidity
/// @audit ↑ Out of order with error ErrZeroAddress
10:     mapping(address => bool) public nativeYieldTokens;
```

- *BlastWrappers.sol* ( [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L45) ):

```solidity
/// @audit ↑ Out of order with error ErrInvalidGovernorAddress
45:     address private immutable _governor;
```

- *BlastYields.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L14) ):

```solidity
/// @audit ↑ Out of order with event LogBlastNativeClaimableEnabled
14:     IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);
```

- *MagicLP.sol* ( [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L61), [607](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L607) ):

```solidity
/// @audit ↑ Out of order with error ErrOverflow
61:     MagicLP public immutable implementation;

/// @audit ↑ Out of order with function _afterInitialized()
607:     modifier onlyImplementationOwner() {
```

- *FeeRateModel.sol* ( [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L19) ):

```solidity
/// @audit ↑ Out of order with error ErrZeroAddress
19:     address public maintainer;
```

- *Factory.sol* ( [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L32) ):

```solidity
/// @audit ↑ Out of order with error ErrZeroAddress
32:     address public implementation;
```

- *Router.sol* ( [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L31), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L47) ):

```solidity
/// @audit ↑ Out of order with error ErrDecimalsDifferenceTooLarge
31:     uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;

/// @audit ↑ Out of order with constructor ()
47:     modifier ensureDeadline(uint256 deadline) {
```

- *LockingMultiRewards.sol* ( [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L78) ):

```solidity
/// @audit ↑ Out of order with error ErrInsufficientRemainingTime
78:     uint256 private constant BIPS = 10_000;
```

</details>

### [N-49] Consider adding validation of user inputs

There are no validations done on the arguments below. Consider that the Solidity [documentation](https://docs.soliditylang.org/en/latest/control-structures.html#panic-via-assert-and-error-via-require) states that `Properly functioning code should never create a Panic, not even on invalid external input. If this happens, then there is a bug in your contract which you should fix`. This means that there should be explicit checks for expected ranges of inputs. Underflows/overflows result in panics should not be used as range checks, and allowing funds to be sent to  `0x0`, which is the default value of address variables and has many gotchas, should be avoided.

<details>
<summary>There are 55 instances (click to show):</summary>

- *BlastBox.sol* ( [56-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L56-L56), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L81-L81) ):

```solidity
/// @audit `token_ not checked`
56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

/// @audit `token not checked`
81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {
```

- *BlastGovernor.sol* ( [28-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L28-L28), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L32-L32), [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L53-L53) ):

```solidity
/// @audit `contractAddress not checked`
28:     function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {

/// @audit `contractAddress not checked`
32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

/// @audit `to not checked`
53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

- *BlastMagicLP.sol* ( [89-89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L89-L89) ):

```solidity
/// @audit `operator not checked`
89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```

- *BlastOnboarding.sol* ( [164-164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L164-L164), [175-175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L175-L175), [190-190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L190-L190), [205-205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L205-L205) ):

```solidity
/// @audit `tokens not checked`
164:     function claimTokenYields(address[] memory tokens) external onlyOwner {

/// @audit `token not checked`
175:     function setTokenSupported(address token, bool supported) external onlyOwner {

/// @audit `bootstrapper_ not checked`
190:     function setBootstrapper(address bootstrapper_) external onlyOwner {

/// @audit `token not checked`
/// @audit `to not checked`
205:     function rescue(address token, address to, uint256 amount) external onlyOwner {
```

- *BlastOnboardingBoot.sol* ( [137-137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L137-L137) ):

```solidity
/// @audit `_staking not checked`
137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {
```

- *MagicLP.sol* ( [244-244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L244-L244), [267-267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L267-L267), [290-290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L290-L290), [360-360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L360-L360), [461-461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L461-L461), [470-479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L470-L479) ):

```solidity
/// @audit `to not checked`
244:     function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {

/// @audit `to not checked`
267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

/// @audit `assetTo not checked`
290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

/// @audit `to not checked`
360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {

/// @audit `to not checked`
461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {

/// @audit `assetTo not checked`
470:     function setParameters(
471:         address assetTo,
472:         uint256 newLpFeeRate,
473:         uint256 newI,
474:         uint256 newK,
475:         uint256 baseOutAmount,
476:         uint256 quoteOutAmount,
477:         uint256 minBaseReserve,
478:         uint256 minQuoteReserve
479:     ) public nonReentrant onlyImplementationOwner {
```

- *FeeRateModel.sol* ( [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L57-L57) ):

```solidity
/// @audit `implementation_ not checked`
57:     function setImplementation(address implementation_) public onlyOwner {
```

- *Factory.sol* ( [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81-L81), [116-116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L116-L116), [120-126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L120-L126) ):

```solidity
/// @audit `baseToken_ not checked`
/// @audit `quoteToken_ not checked`
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

/// @audit `creator not checked`
/// @audit `baseToken not checked`
/// @audit `quoteToken not checked`
/// @audit `pool not checked`
116:     function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {

/// @audit `creator not checked`
/// @audit `baseToken not checked`
/// @audit `quoteToken not checked`
120:     function removePool(
121:         address creator,
122:         address baseToken,
123:         address quoteToken,
124:         uint256 poolIndex,
125:         uint256 userPoolIndex
126:     ) external onlyOwner {
```

- *Router.sol* ( [54-63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L54-L63), [73-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L73-L81), [162-169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L162-L169), [178-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L178-L185), [192-199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L192-L199), [229-235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L229-L235), [261-268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L261-L268), [274-281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L274-L281), [314-321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L314-L321), [336-342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L336-L342), [365-372](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L365-L372), [404-410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L404-L410), [415-420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L415-L420), [432-438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L432-L438), [449-455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L449-L455), [461-466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L461-L466), [478-484](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L478-L484) ):

```solidity
/// @audit `to not checked`
54:     function createPool(
55:         address baseToken,
56:         address quoteToken,
57:         uint256 lpFeeRate,
58:         uint256 i,
59:         uint256 k,
60:         address to,
61:         uint256 baseInAmount,
62:         uint256 quoteInAmount
63:     ) external returns (address clone, uint256 shares) {

/// @audit `to not checked`
73:     function createPoolETH(
74:         address token,
75:         bool useTokenAsQuote,
76:         uint256 lpFeeRate,
77:         uint256 i,
78:         uint256 k,
79:         address to,
80:         uint256 tokenInAmount
81:     ) external payable returns (address clone, uint256 shares) {

/// @audit `lp not checked`
/// @audit `to not checked`
162:     function addLiquidity(
163:         address lp,
164:         address to,
165:         uint256 baseInAmount,
166:         uint256 quoteInAmount,
167:         uint256 minimumShares,
168:         uint256 deadline
169:     ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

/// @audit `lp not checked`
/// @audit `to not checked`
178:     function addLiquidityUnsafe(
179:         address lp,
180:         address to,
181:         uint256 baseInAmount,
182:         uint256 quoteInAmount,
183:         uint256 minimumShares,
184:         uint256 deadline
185:     ) external ensureDeadline(deadline) returns (uint256 shares) {

/// @audit `to not checked`
/// @audit `refundTo not checked`
192:     function addLiquidityETH(
193:         address lp,
194:         address to,
195:         address payable refundTo,
196:         uint256 tokenInAmount,
197:         uint256 minimumShares,
198:         uint256 deadline
199:     ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

/// @audit `to not checked`
229:     function addLiquidityETHUnsafe(
230:         address lp,
231:         address to,
232:         uint256 tokenInAmount,
233:         uint256 minimumShares,
234:         uint256 deadline
235:     ) external payable ensureDeadline(deadline) returns (uint256 shares) {

/// @audit `lp not checked`
/// @audit `to not checked`
261:     function removeLiquidity(
262:         address lp,
263:         address to,
264:         uint256 sharesIn,
265:         uint256 minimumBaseAmount,
266:         uint256 minimumQuoteAmount,
267:         uint256 deadline
268:     ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

/// @audit `to not checked`
274:     function removeLiquidityETH(
275:         address lp,
276:         address to,
277:         uint256 sharesIn,
278:         uint256 minimumETHAmount,
279:         uint256 minimumTokenAmount,
280:         uint256 deadline
281:     ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {

/// @audit `to not checked`
314:     function swapTokensForTokens(
315:         address to,
316:         uint256 amountIn,
317:         address[] calldata path,
318:         uint256 directions,
319:         uint256 minimumOut,
320:         uint256 deadline
321:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit `to not checked`
336:     function swapETHForTokens(
337:         address to,
338:         address[] calldata path,
339:         uint256 directions,
340:         uint256 minimumOut,
341:         uint256 deadline
342:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit `to not checked`
365:     function swapTokensForETH(
366:         address to,
367:         uint256 amountIn,
368:         address[] calldata path,
369:         uint256 directions,
370:         uint256 minimumOut,
371:         uint256 deadline
372:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit `lp not checked`
/// @audit `to not checked`
404:     function sellBaseTokensForTokens(
405:         address lp,
406:         address to,
407:         uint256 amountIn,
408:         uint256 minimumOut,
409:         uint256 deadline
410:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit `lp not checked`
/// @audit `to not checked`
415:     function sellBaseETHForTokens(
416:         address lp,
417:         address to,
418:         uint256 minimumOut,
419:         uint256 deadline
420:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit `to not checked`
432:     function sellBaseTokensForETH(
433:         address lp,
434:         address to,
435:         uint256 amountIn,
436:         uint256 minimumOut,
437:         uint256 deadline
438:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit `lp not checked`
/// @audit `to not checked`
449:     function sellQuoteTokensForTokens(
450:         address lp,
451:         address to,
452:         uint256 amountIn,
453:         uint256 minimumOut,
454:         uint256 deadline
455:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit `lp not checked`
/// @audit `to not checked`
461:     function sellQuoteETHForTokens(
462:         address lp,
463:         address to,
464:         uint256 minimumOut,
465:         uint256 deadline
466:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit `to not checked`
478:     function sellQuoteTokensForETH(
479:         address lp,
480:         address to,
481:         uint256 amountIn,
482:         uint256 minimumOut,
483:         uint256 deadline
484:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {
```

- *LockingMultiRewards.sol* ( [349-349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L349-L349), [361-361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L361-L361) ):

```solidity
/// @audit `account not checked`
349:     function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {

/// @audit `rewardToken not checked`
361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
```

</details>

### [N-50] Constants should be put on the left side of comparisons

Putting constants on the left side of comparison statements is a best practice known as [Yoda conditions](https://en.wikipedia.org/wiki/Yoda_conditions).
Although solidity's static typing system prevents accidental assignments within conditionals, adopting this practice can improve code readability and consistency, especially when working across multiple languages.

<details>
<summary>There are 61 instances (click to show):</summary>

- *BlastBox.sol* ( [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L25), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L73) ):

```solidity
/// @audit put `address(0)` on the left
25:         if (feeTo_ == address(0)) {

/// @audit put `address(0)` on the left
73:         if (feeTo_ == address(0)) {
```

- *BlastGovernor.sol* ( [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L16), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L41) ):

```solidity
/// @audit put `address(0)` on the left
16:         if (feeTo_ == address(0)) {

/// @audit put `address(0)` on the left
41:         if(_feeTo == address(0)) {
```

- *BlastMagicLP.sol* ( [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L24), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L81) ):

```solidity
/// @audit put `address(0)` on the left
24:         if (feeTo_ == address(0)) {

/// @audit put `address(0)` on the left
81:         if (feeTo_ == address(0)) {
```

- *BlastOnboarding.sol* ( [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L89), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L148) ):

```solidity
/// @audit put `address(0)` on the left
89:         if (feeTo_ == address(0)) {

/// @audit put `address(0)` on the left
148:         if (feeTo_ == address(0)) {
```

- *BlastOnboardingBoot.sol* ( [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L64), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L97), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L158) ):

```solidity
/// @audit put `0` on the left
64:         if (shares == 0) {

/// @audit put `address(0)` on the left
97:         if (pool != address(0)) {

/// @audit put `0` on the left
158:         if (totalLocked == 0) {
```

- *BlastTokenRegistry.sol* ( [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L15) ):

```solidity
/// @audit put `address(0)` on the left
15:         if (token == address(0)) {
```

- *BlastWrappers.sol* ( [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L21), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L35), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L48) ):

```solidity
/// @audit put `address(0)` on the left
21:         if (governor_ == address(0)) {

/// @audit put `address(0)` on the left
35:         if (governor_ == address(0)) {

/// @audit put `address(0)` on the left
48:         if (governor_ == address(0)) {
```

- *MagicLP.sol* ( [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L102), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L102), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L102), [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L108), [369](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L369), [377](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L377), [385](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L385), [389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L389), [483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L483), [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L549), [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L549), [594](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L594) ):

```solidity
/// @audit put `address(0)` on the left
102:         if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {

/// @audit put `address(0)` on the left
102:         if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {

/// @audit put `address(0)` on the left
102:         if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {

/// @audit put `0` on the left
108:         if (i == 0 || i > MAX_I) {

/// @audit put `0` on the left
369:         if (baseInput == 0) {

/// @audit put `0` on the left
377:             if (quoteBalance == 0) {

/// @audit put `0` on the left
385:             if (_QUOTE_TARGET_ == 0) {

/// @audit put `2001` on the left
389:             if (shares <= 2001) {

/// @audit put `0` on the left
483:         if (newI == 0 || newI > MAX_I) {

/// @audit put `0` on the left
549:         if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {

/// @audit put `0` on the left
549:         if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {

/// @audit put `1000` on the left
594:         if (amount <= 1000) {
```

- *FeeRateModel.sol* ( [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L23), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L35), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L47) ):

```solidity
/// @audit put `address(0)` on the left
23:         if (maintainer_ == address(0)) {

/// @audit put `address(0)` on the left
35:         if (implementation == address(0)) {

/// @audit put `address(0)` on the left
47:         if (maintainer_ == address(0)) {
```

- *DecimalMath.sol* ( [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L48), [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L50) ):

```solidity
/// @audit put `0` on the left
48:         if (e == 0) {

/// @audit put `1` on the left
50:         } else if (e == 1) {
```

- *Math.sol* ( [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L52), [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L58), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L80), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L89), [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L94), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L132), [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L136), [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L140), [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L153), [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L192) ):

```solidity
/// @audit put `0` on the left
52:         if (V0 == 0) {

/// @audit put `0` on the left
58:         if (k == 0) {

/// @audit put `0` on the left
80:         if (k == 0) {

/// @audit put `0` on the left
89:         if (V1 == 0) {

/// @audit put `0` on the left
94:         if (ki == 0) {

/// @audit put `0` on the left
132:         if (V0 == 0) {

/// @audit put `0` on the left
136:         if (delta == 0) {

/// @audit put `0` on the left
140:         if (k == 0) {

/// @audit put `0` on the left
153:             if (idelta == 0) {

/// @audit put `0` on the left
192:             if (numerator == 0) {
```

- *Factory.sol* ( [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L39), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L97) ):

```solidity
/// @audit put `address(0)` on the left
39:         if (implementation_ == address(0)) {

/// @audit put `address(0)` on the left
97:         if (implementation_ == address(0)) {
```

- *Router.sol* ( [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L105), [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L125), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L131), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L132), [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L142), [593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L593), [599](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L599), [599](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L599) ):

```solidity
/// @audit put `2001` on the left
105:         if (shares <= 2001) {

/// @audit put `0` on the left
125:         if (baseInAmount == 0) {

/// @audit put `0` on the left
131:         if (totalSupply == 0) {

/// @audit put `0` on the left
132:             if (quoteBalance == 0) {

/// @audit put `2001` on the left
142:             if (shares <= 2001) {

/// @audit put `0` on the left
593:         if (pathLength <= 0) {

/// @audit put `0` on the left
599:         if (baseDecimals == 0 || quoteDecimals == 0) {

/// @audit put `0` on the left
599:         if (baseDecimals == 0 || quoteDecimals == 0) {
```

- *LockingMultiRewards.sol* ( [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L119), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L156), [171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L171), [278](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L278), [301](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L301), [309](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L309), [410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L410), [459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L459), [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L490) ):

```solidity
/// @audit put `BIPS` on the left
119:         if (_lockingBoostMultiplerInBips <= BIPS) {

/// @audit put `0` on the left
156:         if (amount == 0) {

/// @audit put `0` on the left
171:         if (amount == 0) {

/// @audit put `0` on the left
278:         if (totalSupply_ == 0) {

/// @audit put `address(0)` on the left
301:         if (rewardToken == address(0)) {

/// @audit put `MAX_NUM_REWARDS` on the left
309:         if (rewardTokens.length == MAX_NUM_REWARDS) {

/// @audit put `0` on the left
410:             if (locks.length == 0) {

/// @audit put `0` on the left
459:         if (amount == 0) {

/// @audit put `0` on the left
490:         if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {
```

</details>

### [N-51] Put all system-wide constants in one file

Putting all the system-wide constants in a single file improves code readability, makes it easier to understand the basic configuration and limitations of the system, and makes maintenance easier.

<details>
<summary>There are 8 instances (click to show):</summary>

- *BlastPoints.sol* ( [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L7-L7), [8-8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L8-L8) ):

```solidity
7:     address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;

8:     IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);
```

- *MagicLP.sol* ( [63-63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L63-L63), [64-64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L64-L64), [65-65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L65-L65), [66-66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L66-L66) ):

```solidity
63:     uint256 public constant MAX_I = 10 ** 36;

64:     uint256 public constant MAX_K = 10 ** 18;

65:     uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%

66:     uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%
```

- *Router.sol* ( [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L31-L31) ):

```solidity
31:     uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;
```

- *MagicLpAggregator.sol* ( [16-16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L16-L16) ):

```solidity
16:     uint256 public constant WAD = 18;
```

</details>

### [N-52] `else`-block not required

One level of nesting can be removed by not having an `else` block when the `if`-block always jumps at the end. For example:
```solidity
if (condition) {
    body1...
    return x;
} else {
    body2...
}
```
can be changed to:
```solidity
if (condition) {
    body1...
    return x;
}
body2...
```

<details>
<summary>There are 5 instances (click to show):</summary>

- *DecimalMath.sol* ( [48-50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L48-L50), [50-52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L50-L52) ):

```solidity
48:         if (e == 0) {
49:             return 10 ** 18;
50:         } else if (e == 1) {

50:         } else if (e == 1) {
51:             return target;
52:         } else {
```

- *Math.sol* ( [22-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L22-L24), [200-202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L200-L202) ):

```solidity
22:         if (remainder > 0) {
23:             return quotient + 1;
24:         } else {

200:         if (V2 > V1) {
201:             return 0;
202:         } else {
```

- *PMMPricing.sol* ( [204-208](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L204-L208) ):

```solidity
204:         if (state.R == RState.BELOW_ONE) {
205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);
206:             R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);
207:             return DecimalMath.divFloor(state.i, R);
208:         } else {
```

</details>

### [N-53] Large multiples of ten should use scientific notation

Use a scientific notation rather than decimal literals (e.g. `1e6` instead of `1000000`), for better code readability.

There are 3 instances:

- *BlastOnboardingBoot.sol* ( [117-117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L117-L117) ):

```solidity
/// @audit 30_000 -> 3e4
117:         staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
```

- *MagicLP.sol* ( [594-594](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L594-L594) ):

```solidity
/// @audit 1000 -> 1e3
594:         if (amount <= 1000) {
```

- *LockingMultiRewards.sol* ( [78-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L78-L78) ):

```solidity
/// @audit 10_000 -> 1e4
78:     uint256 private constant BIPS = 10_000;
```

### [N-54] SPDX identifier should be the in the first line of a solidity file

SPDX identifier should be the in the first line of a solidity file.

There are 5 instances:

- *MagicLP.sol* ( [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L1) ):

```solidity
1: /*
```

- *FeeRateModel.sol* ( [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L1) ):

```solidity
1: /*
```

- *DecimalMath.sol* ( [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L1) ):

```solidity
1: /*
```

- *Math.sol* ( [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L1) ):

```solidity
1: /*
```

- *PMMPricing.sol* ( [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L1) ):

```solidity
1: /*
```

### [N-55] High cyclomatic complexity

Consider breaking down these blocks into more manageable units, by splitting things into utility functions, by reducing nesting, and by using early returns.

<details>
<summary>There are 2 instances (click to show):</summary>

- *PMMPricing.sol* ( [39-74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L39-L74), [76-100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L76-L100) ):

```solidity
39:     function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {
40:         if (state.R == RState.ONE) {
41:             // case 1: R=1
42:             // R falls below one
43:             receiveQuoteAmount = _ROneSellBaseToken(state, payBaseAmount);
44:             newR = RState.BELOW_ONE;
45:         } else if (state.R == RState.ABOVE_ONE) {
46:             uint256 backToOnePayBase = state.B0 - state.B;
47:             uint256 backToOneReceiveQuote = state.Q - state.Q0;
48:             // case 2: R>1
49:             // complex case, R status depends on trading amount
50:             if (payBaseAmount < backToOnePayBase) {
51:                 // case 2.1: R status do not change
52:                 receiveQuoteAmount = _RAboveSellBaseToken(state, payBaseAmount);
53:                 newR = RState.ABOVE_ONE;
54:                 if (receiveQuoteAmount > backToOneReceiveQuote) {
55:                     // [Important corner case!] may enter this branch when some precision problem happens. And consequently contribute to negative spare quote amount
56:                     // to make sure spare quote>=0, mannually set receiveQuote=backToOneReceiveQuote
57:                     receiveQuoteAmount = backToOneReceiveQuote;
58:                 }
59:             } else if (payBaseAmount == backToOnePayBase) {
60:                 // case 2.2: R status changes to ONE
61:                 receiveQuoteAmount = backToOneReceiveQuote;
62:                 newR = RState.ONE;
63:             } else {
64:                 // case 2.3: R status changes to BELOW_ONE
65:                 receiveQuoteAmount = backToOneReceiveQuote + _ROneSellBaseToken(state, payBaseAmount - backToOnePayBase);
66:                 newR = RState.BELOW_ONE;
67:             }
68:         } else {
69:             // state.R == RState.BELOW_ONE
70:             // case 3: R<1
71:             receiveQuoteAmount = _RBelowSellBaseToken(state, payBaseAmount);
72:             newR = RState.BELOW_ONE;
73:         }
74:     }

76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {
77:         if (state.R == RState.ONE) {
78:             receiveBaseAmount = _ROneSellQuoteToken(state, payQuoteAmount);
79:             newR = RState.ABOVE_ONE;
80:         } else if (state.R == RState.ABOVE_ONE) {
81:             receiveBaseAmount = _RAboveSellQuoteToken(state, payQuoteAmount);
82:             newR = RState.ABOVE_ONE;
83:         } else {
84:             uint256 backToOnePayQuote = state.Q0 - state.Q;
85:             uint256 backToOneReceiveBase = state.B - state.B0;
86:             if (payQuoteAmount < backToOnePayQuote) {
87:                 receiveBaseAmount = _RBelowSellQuoteToken(state, payQuoteAmount);
88:                 newR = RState.BELOW_ONE;
89:                 if (receiveBaseAmount > backToOneReceiveBase) {
90:                     receiveBaseAmount = backToOneReceiveBase;
91:                 }
92:             } else if (payQuoteAmount == backToOnePayQuote) {
93:                 receiveBaseAmount = backToOneReceiveBase;
94:                 newR = RState.ONE;
95:             } else {
96:                 receiveBaseAmount = backToOneReceiveBase + _ROneSellQuoteToken(state, payQuoteAmount - backToOnePayQuote);
97:                 newR = RState.ABOVE_ONE;
98:             }
99:         }
100:     }
```

</details>

### [N-56] Typos

All typos should be corrected.

<details>
<summary>There are 12 instances (click to show):</summary>

- *PMMPricing.sol* ( [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L56) ):

```solidity
/// @audit mannually
56:                     // to make sure spare quote>=0, mannually set receiveQuote=backToOneReceiveQuote
```

- *LockingMultiRewards.sol* ( [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L84), [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L109), [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L114), [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L119), [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L136), [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L236), [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L241), [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L536), [563](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L563), [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L582) ):

```solidity
/// @audit Multipler
84:     uint256 public immutable lockingBoostMultiplerInBips;

/// @audit Multipler
109:     /// @param _lockingBoostMultiplerInBips The multiplier for the locking boost. 30000 means if you stake 100, you get 300 locked

/// @audit Multipler
114:         uint256 _lockingBoostMultiplerInBips,

/// @audit Multipler
119:         if (_lockingBoostMultiplerInBips <= BIPS) {

/// @audit Multipler
/// @audit Multipler
136:         lockingBoostMultiplerInBips = _lockingBoostMultiplerInBips;

/// @audit Multipler
236:         return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);

/// @audit Multipler
241:         return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);

/// @audit udpate
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

/// @audit udpate
563:             _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_));

/// @audit udpate
582:                 _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);
```

</details>

### [N-57] Consider bounding input array length

The functions below take in an unbounded array, and make function calls for entries in the array. While the function will revert if it eventually runs out of gas, it may be a nicer user experience to require() that the length of the array is below some reasonable maximum, so that the user doesn't have to use up a full transaction's gas only to see that the transaction reverts.

There are 5 instances:

- *BlastOnboarding.sol* ( [165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L165) ):

```solidity
165:         for (uint256 i = 0; i < tokens.length; i++) {
```

- *Router.sol* ( [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L544) ):

```solidity
544:         for (uint256 i = 0; i < iterations; ) {
```

- *LockingMultiRewards.sol* ( [405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L405), [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L575), [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L580) ):

```solidity
405:         for (uint256 i; i < users.length; ) {

575:         for (uint256 i; i < rewardTokens.length; ) {

580:             for (uint256 j; j < users.length; ) {
```

### [N-58] Unnecessary casting

Unnecessary castings can be removed.

<details>
<summary>There are 28 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [227-227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L227-L227) ):

```solidity
/// @audit address(bootstrapper)
227:         return address(bootstrapper);
```

- *BlastOnboardingBoot.sol* ( [131-131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L131-L131) ):

```solidity
/// @audit IFactory(router.factory())
131:         factory = IFactory(router.factory());
```

- *BlastYields.sol* ( [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L72-L72), [77-77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L77-L77) ):

```solidity
/// @audit address(token)
72:         emit LogBlastTokenClaimed(recipient, address(token), amount);

/// @audit address(token)
77:         emit LogBlastTokenClaimed(recipient, address(token), amount);
```

- *MagicLP.sol* ( [264-264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L264-L264), [264-264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L264-L264), [287-287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L287-L287), [287-287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L287-L287), [325-325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L325-L325), [325-325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L325-L325), [347-347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L347-L347), [347-347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L347-L347) ):

```solidity
/// @audit address(_BASE_TOKEN_)
264:         emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

/// @audit address(_QUOTE_TOKEN_)
264:         emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

/// @audit address(_QUOTE_TOKEN_)
287:         emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

/// @audit address(_BASE_TOKEN_)
287:         emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

/// @audit address(_QUOTE_TOKEN_)
325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

/// @audit address(_BASE_TOKEN_)
325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

/// @audit address(_BASE_TOKEN_)
347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

/// @audit address(_QUOTE_TOKEN_)
347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
```

- *Factory.sol* ( [85-85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L85-L85), [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L86-L86), [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L86-L86) ):

```solidity
/// @audit address(implementation)
85:         clone = LibClone.cloneDeterministic(address(implementation), salt);

/// @audit address(baseToken_)
86:         IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);

/// @audit address(quoteToken_)
86:         IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
```

- *Router.sol* ( [66-66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L66-L66), [88-88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L88-L88), [119-119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L119-L119), [120-120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L120-L120), [252-252](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L252-L252), [253-253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L253-L253), [328-328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L328-L328), [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L330-L330), [360-360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L360-L360), [515-515](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L515-L515), [516-516](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L516-L516), [547-547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L547-L547), [550-550](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L550-L550) ):

```solidity
/// @audit IFactory(factory)
66:         clone = IFactory(factory).create(baseToken, quoteToken, lpFeeRate, i, k);

/// @audit IFactory(factory)
88:         clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);

/// @audit address(lp)
119:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;

/// @audit address(lp)
120:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;

/// @audit address(lp)
252:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp));

/// @audit address(lp)
253:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp));

/// @audit address(firstLp)
328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

/// @audit address(firstLp)
330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

/// @audit address(firstLp)
360:         inToken.safeTransfer(address(firstLp), msg.value);

/// @audit address(lp)
515:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;

/// @audit address(lp)
516:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;

/// @audit address(path[i + 1])
547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));

/// @audit address(path[i + 1])
550:                 IMagicLP(path[i]).sellQuote(address(path[i + 1]));
```

</details>

### [N-59] Unused import

The identifier is imported but never used within the file.

<details>
<summary>There are 47 instances (click to show):</summary>

- *BlastBox.sol* ( [5-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L5-L5), [8-8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L8-L8), [9-9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L9-L9), [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L10-L10), [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L11-L11) ):

```solidity
/// @audit DegenBox
5: import {DegenBox} from "/DegenBox.sol";

/// @audit BlastTokenRegistry
8: import {BlastTokenRegistry} from "/blast/BlastTokenRegistry.sol";

/// @audit IERC20
9: import {IERC20} from "BoringSolidity/interfaces/IERC20.sol";

/// @audit OperatableV3
10: import {OperatableV3} from "mixins/OperatableV3.sol";

/// @audit IWETH
11: import {IWETH} from "interfaces/IWETH.sol";
```

- *BlastGovernor.sol* ( [5-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L5-L5) ):

```solidity
/// @audit OperatableV2
5: import {OperatableV2} from "mixins/OperatableV2.sol";
```

- *BlastMagicLP.sol* ( [5-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L5-L5), [8-8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L8-L8) ):

```solidity
/// @audit MagicLP
5: import {MagicLP} from "/mimswap/MagicLP.sol";

/// @audit BlastTokenRegistry
8: import {BlastTokenRegistry} from "/blast/BlastTokenRegistry.sol";
```

- *BlastOnboarding.sol* ( [4-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L4-L4), [6-6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L6-L6), [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L7-L7), [8-8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L8-L8), [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L10-L10) ):

```solidity
/// @audit Owned
4: import {Owned} from "solmate/auth/Owned.sol";

/// @audit BlastTokenRegistry
6: import {BlastTokenRegistry} from "/blast/BlastTokenRegistry.sol";

/// @audit Proxy
7: import {Proxy} from "openzeppelin-contracts/proxy/Proxy.sol";

/// @audit SafeTransferLib
8: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

/// @audit Pausable
10: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";
```

- *BlastOnboardingBoot.sol* ( [4-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L4-L4), [5-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L5-L5), [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L7-L7), [9-9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L9-L9), [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L10-L10), [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L11-L11) ):

```solidity
/// @audit BlastOnboarding
4: import {BlastOnboarding} from "/blast/BlastOnboarding.sol";

/// @audit BlastOnboardingData
5: import {BlastOnboardingData} from "/blast/BlastOnboarding.sol";

/// @audit IFeeRateModel
7: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";

/// @audit SafeTransferLib
9: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

/// @audit DecimalMath
10: import {DecimalMath} from "/mimswap/libraries/DecimalMath.sol";

/// @audit LockingMultiRewards
11: import {LockingMultiRewards} from "staking/LockingMultiRewards.sol";
```

- *BlastTokenRegistry.sol* ( [4-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L4-L4) ):

```solidity
/// @audit Owned
4: import {Owned} from "solmate/auth/Owned.sol";
```

- *BlastWrappers.sol* ( [6-6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L6-L6), [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L7-L7), [8-8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L8-L8), [9-9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L9-L9), [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L10-L10), [12-12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L12-L12) ):

```solidity
/// @audit Router
6: import {Router} from "/mimswap/periphery/Router.sol";

/// @audit Factory
7: import {Factory} from "/mimswap/periphery/Factory.sol";

/// @audit IFeeRateModel
8: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";

/// @audit CauldronV4
9: import {CauldronV4} from "cauldrons/CauldronV4.sol";

/// @audit IWETH
10: import {IWETH} from "interfaces/IWETH.sol";

/// @audit IFactory
12: import {IFactory} from "/mimswap/interfaces/IFactory.sol";
```

- *MagicLP.sol* ( [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L10-L10), [12-12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L12-L12), [13-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L13-L13), [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L14-L14), [15-15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L15-L15), [17-17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L17-L17), [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L21-L21) ):

```solidity
/// @audit Owned
10: import {Owned} from "solmate/auth/Owned.sol";

/// @audit SafeTransferLib
12: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

/// @audit ReentrancyGuard
13: import {ReentrancyGuard} from "solady/utils/ReentrancyGuard.sol";

/// @audit ERC20
14: import {ERC20} from "solady/tokens/ERC20.sol";

/// @audit SafeCastLib
15: import {SafeCastLib} from "solady/utils/SafeCastLib.sol";

/// @audit Math
17: import {Math} from "/mimswap/libraries/Math.sol";

/// @audit IWETH
21: import {IWETH} from "interfaces/IWETH.sol";
```

- *FeeRateModel.sol* ( [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L10-L10) ):

```solidity
/// @audit Owned
10: import {Owned} from "solmate/auth/Owned.sol";
```

- *FeeRateModelImpl.sol* ( [4-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L4-L4) ):

```solidity
/// @audit IFeeRateImpl
4: import {IFeeRateImpl} from "../interfaces/IFeeRateModel.sol";
```

- *DecimalMath.sol* ( [9-9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L9-L9) ):

```solidity
/// @audit Math
9: import {Math} from "/mimswap/libraries/Math.sol";
```

- *Factory.sol* ( [4-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L4-L4), [6-6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L6-L6), [8-8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L8-L8) ):

```solidity
/// @audit Owned
4: import {Owned} from "solmate/auth/Owned.sol";

/// @audit IFeeRateModel
6: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";

/// @audit MagicLP
8: import {MagicLP} from "/mimswap/MagicLP.sol";
```

- *Router.sol* ( [4-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L4-L4), [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L7-L7) ):

```solidity
/// @audit SafeTransferLib
4: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

/// @audit IWETH
7: import {IWETH} from "interfaces/IWETH.sol";
```

- *MagicLpAggregator.sol* ( [4-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L4-L4), [6-6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L6-L6), [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L7-L7) ):

```solidity
/// @audit FixedPointMathLib
4: import {FixedPointMathLib} from "solady/utils/FixedPointMathLib.sol";

/// @audit IAggregator
6: import {IAggregator} from "interfaces/IAggregator.sol";

/// @audit IMagicLP
7: import {IMagicLP} from "/mimswap/interfaces/IMagicLP.sol";
```

- *LockingMultiRewards.sol* ( [4-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L4-L4), [5-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L5-L5), [6-6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L6-L6) ):

```solidity
/// @audit OperatableV2
4: import {OperatableV2} from "mixins/OperatableV2.sol";

/// @audit Pausable
5: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";

/// @audit SafeTransferLib
6: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";
```

</details>

### [N-60] Unused local variables

The following local variables are not used. It is recommended to check the code for logical omissions that cause them not to be used. If it's determined that they are not needed anywhere, it's best to remove them from the codebase to improve code clarity and minimize confusion.

There are 2 instances:

- *MagicLpAggregator.sol* ( [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L34-L34), [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L34-L34) ):

```solidity
34:         (uint256 baseReserve, uint256 quoteReserve) = pair.getReserves();

34:         (uint256 baseReserve, uint256 quoteReserve) = pair.getReserves();
```

### [N-61] Unused modifiers

The following `modifier`s are not used. It is recommended to check the code for logical omissions that cause them not to be used. If it's determined that they are not needed anywhere, it's best to remove them from the codebase to improve code clarity and minimize confusion.

There are 2 instances:

- *MagicLP.sol* ( [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L614), [621](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L621) ):

```solidity
614:     modifier onlyClones() {

621:     modifier onlyImplementation() {
```

### [N-62] Unused named return

Declaring named returns, but not using them, is confusing to the reader. Consider either completely removing them (by declaring just the type without a name), or remove the return statement and do a variable assignment. This would improve the readability of the code, and it may also help reduce regressions during future code refactors.

<details>
<summary>There are 24 instances (click to show):</summary>

- *BlastOnboardingBoot.sol* ( [78-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L78-L78), [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L86-L86), [155-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L155-L155) ):

```solidity
/// @audit shares
78:     function claimable(address user) external view returns (uint256 shares) {

/// @audit baseAdjustedInAmount
/// @audit quoteAdjustedInAmount
/// @audit shares
86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

/// @audit shares
155:     function _claimable(address user) internal view returns (uint256 shares) {
```

- *BlastYields.sol* ( [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L51-L51) ):

```solidity
/// @audit amount
51:     function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
```

- *MagicLP.sol* ( [215-215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L215-L215), [224-224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L224-L224), [228-228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L228-L228), [232-232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L232-L232) ):

```solidity
/// @audit midPrice
215:     function getMidPrice() public view returns (uint256 midPrice) {

/// @audit lpFeeRate
/// @audit mtFeeRate
224:     function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {

/// @audit input
228:     function getBaseInput() public view returns (uint256 input) {

/// @audit input
232:     function getQuoteInput() public view returns (uint256 input) {
```

- *FeeRateModel.sol* ( [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L34-L34) ):

```solidity
/// @audit adjustedLpFeeRate
/// @audit mtFeeRate
34:     function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```

- *FeeRateModelImpl.sol* ( [9-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L13) ):

```solidity
/// @audit adjustedLpFeeRate
9:     function getFeeRate(
10:         address /*pool*/,
11:         address /*trader*/,
12:         uint256 lpFeeRate
13:     ) external pure returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```

- *Router.sol* ( [178-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L178-L185), [229-235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L229-L235), [261-268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L261-L268), [314-321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L314-L321), [336-342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L336-L342), [404-410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L404-L410), [415-420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L415-L420), [449-455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L449-L455), [461-466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L461-L466) ):

```solidity
/// @audit shares
178:     function addLiquidityUnsafe(
179:         address lp,
180:         address to,
181:         uint256 baseInAmount,
182:         uint256 quoteInAmount,
183:         uint256 minimumShares,
184:         uint256 deadline
185:     ) external ensureDeadline(deadline) returns (uint256 shares) {

/// @audit shares
229:     function addLiquidityETHUnsafe(
230:         address lp,
231:         address to,
232:         uint256 tokenInAmount,
233:         uint256 minimumShares,
234:         uint256 deadline
235:     ) external payable ensureDeadline(deadline) returns (uint256 shares) {

/// @audit baseAmountOut
/// @audit quoteAmountOut
261:     function removeLiquidity(
262:         address lp,
263:         address to,
264:         uint256 sharesIn,
265:         uint256 minimumBaseAmount,
266:         uint256 minimumQuoteAmount,
267:         uint256 deadline
268:     ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

/// @audit amountOut
314:     function swapTokensForTokens(
315:         address to,
316:         uint256 amountIn,
317:         address[] calldata path,
318:         uint256 directions,
319:         uint256 minimumOut,
320:         uint256 deadline
321:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit amountOut
336:     function swapETHForTokens(
337:         address to,
338:         address[] calldata path,
339:         uint256 directions,
340:         uint256 minimumOut,
341:         uint256 deadline
342:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit amountOut
404:     function sellBaseTokensForTokens(
405:         address lp,
406:         address to,
407:         uint256 amountIn,
408:         uint256 minimumOut,
409:         uint256 deadline
410:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit amountOut
415:     function sellBaseETHForTokens(
416:         address lp,
417:         address to,
418:         uint256 minimumOut,
419:         uint256 deadline
420:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit amountOut
449:     function sellQuoteTokensForTokens(
450:         address lp,
451:         address to,
452:         uint256 amountIn,
453:         uint256 minimumOut,
454:         uint256 deadline
455:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {

/// @audit amountOut
461:     function sellQuoteETHForTokens(
462:         address lp,
463:         address to,
464:         uint256 minimumOut,
465:         uint256 deadline
466:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
```

</details>

### [N-63] Use delete instead of assigning values to `false`

The `delete` keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic.

There is 1 instance:

- *Math.sol* ( [176-176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L176-L176) ):

```solidity
176:             bSig = false;
```

### [N-64] Consider using `delete` rather than assigning zero to clear values

The `delete` keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic.

There are 2 instances:

- *Math.sol* ( [154-154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L154-L154) ):

```solidity
154:                 temp = 0;
```

- *LockingMultiRewards.sol* ( [619-619](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L619-L619) ):

```solidity
619:             rewards[user][rewardToken] = 0;
```

### [N-65] Use the latest Solidity version

Upgrading to the [latest solidity version](https://github.com/ethereum/solc-js/tags) (0.8.19 for L2s) can optimize gas usage, take advantage of new features and improve overall contract efficiency. Where possible, based on compatibility requirements, it is recommended to use newer/latest solidity version to take advantage of the latest optimizations and features.

<details>
<summary>There are 20 instances (click to show):</summary>

- *BlastBox.sol* ( [3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L3) ):

```solidity
3: pragma solidity >=0.8.0;
```

- *BlastDapp.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastGovernor.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastMagicLP.sol* ( [3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L3) ):

```solidity
3: pragma solidity >=0.8.0;
```

- *BlastOnboarding.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastOnboardingBoot.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastTokenRegistry.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastWrappers.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastPoints.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *BlastYields.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *MagicLP.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L8) ):

```solidity
8: pragma solidity >=0.8.0;
```

- *FeeRateModel.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L8) ):

```solidity
8: pragma solidity >=0.8.0;
```

- *FeeRateModelImpl.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *DecimalMath.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L7) ):

```solidity
7: pragma solidity >=0.8.0;
```

- *Math.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L8) ):

```solidity
8: pragma solidity >=0.8.0;
```

- *PMMPricing.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L8) ):

```solidity
8: pragma solidity >=0.8.0;
```

- *Factory.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *Router.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *MagicLpAggregator.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

- *LockingMultiRewards.sol* ( [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L2) ):

```solidity
2: pragma solidity >=0.8.0;
```

</details>

### [N-66] Consider using named function arguments

When calling functions with multiple arguments, consider using [named function parameters](https://docs.soliditylang.org/en/latest/control-structures.html#function-calls-with-named-parameters), rather than positional ones.

<details>
<summary>There are 14 instances (click to show):</summary>

- *BlastOnboardingBoot.sol* ( [69-69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L69-L69), [89-89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L89-L89), [106-106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L106-L106) ):

```solidity
69:         staking.stakeFor(msg.sender, shares, lock);

89:         return router.previewCreatePool(I, baseAmount, quoteAmount);

106:         (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
```

- *BlastYields.sol* ( [30-30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L30-L30), [61-61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L61-L61) ):

```solidity
30:         BLAST_YIELD_PRECOMPILE.configure(YieldMode.CLAIMABLE, GasMode.CLAIMABLE, governor_);

61:         amount = BLAST_YIELD_PRECOMPILE.claimYield(contractAddress, recipient, amount);
```

- *MagicLP.sol* ( [295-295](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L295-L295), [451-451](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L451-L451) ):

```solidity
295:             ICallee(assetTo).FlashLoanCall(msg.sender, baseAmount, quoteAmount, data);

451:             ICallee(to).SellShareCall(msg.sender, shareAmount, baseAmount, quoteAmount, data);
```

- *FeeRateModel.sol* ( [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L39-L39) ):

```solidity
39:         return IFeeRateImpl(implementation).getFeeRate(msg.sender, trader, lpFeeRate);
```

- *Factory.sol* ( [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L86-L86) ):

```solidity
86:         IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
```

- *Router.sol* ( [66-66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L66-L66), [88-88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L88-L88), [271-271](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L271-L271), [287-294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L287-L294), [296-303](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L296-L303) ):

```solidity
66:         clone = IFactory(factory).create(baseToken, quoteToken, lpFeeRate, i, k);

88:         clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);

271:         return IMagicLP(lp).sellShares(sharesIn, to, minimumBaseAmount, minimumQuoteAmount, "", deadline);

287:             (ethAmountOut, tokenAmountOut) = IMagicLP(lp).sellShares(
288:                 sharesIn,
289:                 address(this),
290:                 minimumETHAmount,
291:                 minimumTokenAmount,
292:                 "",
293:                 deadline
294:             );

296:             (tokenAmountOut, ethAmountOut) = IMagicLP(lp).sellShares(
297:                 sharesIn,
298:                 address(this),
299:                 minimumTokenAmount,
300:                 minimumETHAmount,
301:                 "",
302:                 deadline
303:             );
```

</details>

### [N-67] Named returns are recommended

Using named returns makes the code more self-documenting, makes it easier to fill out NatSpec, and in some cases can save gas. The cases below are where there currently is at most one return statement, which is ideal for named returns.

<details>
<summary>There are 62 instances (click to show):</summary>

- *BlastBox.sol* ( [52-52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L52-L52), [103-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L103-L103) ):

```solidity
52:     function claimGasYields() external onlyOperators returns (uint256) {

103:     function isOwner(address _account) internal view override returns (bool) {
```

- *BlastGovernor.sol* ( [28-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L28-L28), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L32-L32) ):

```solidity
28:     function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
```

- *BlastMagicLP.sol* ( [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L39-L39), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L47-L47) ):

```solidity
39:     function version() external pure override returns (string memory) {

47:     function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {
```

- *BlastOnboarding.sol* ( [160-160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L160-L160), [226-226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L226-L226) ):

```solidity
160:     function claimGasYields() external onlyOwner returns (uint256) {

226:     function _implementation() internal view override returns (address) {
```

- *BlastOnboardingBoot.sol* ( [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L96-L96) ):

```solidity
96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
```

- *BlastYields.sol* ( [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L38-L38), [60-60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L60-L60), [75-75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L75-L75) ):

```solidity
38:     function claimMaxGasYields(address recipient) internal returns (uint256) {

60:     function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {

75:     function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {
```

- *MagicLP.sol* ( [155-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L155-L155), [159-159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L159-L159), [163-163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L163-L163), [236-236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L236-L236) ):

```solidity
155:     function name() public view override returns (string memory) {

159:     function symbol() public pure override returns (string memory) {

163:     function decimals() public view override returns (uint8) {

236:     function version() external pure virtual returns (string memory) {
```

- *DecimalMath.sol* ( [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L23-L23), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L27-L27), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L31-L31), [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L35-L35), [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L39-L39), [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L43-L43), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L47-L47) ):

```solidity
23:     function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {

27:     function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {

31:     function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {

35:     function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {

39:     function reciprocalFloor(uint256 target) internal pure returns (uint256) {

43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {

47:     function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```

- *Math.sol* ( [19-19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L19-L19), [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51-L51), [79-79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L79-L79), [131-131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131-L131) ):

```solidity
19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```

- *PMMPricing.sol* ( [104-112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L104-L112), [119-127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L119-L127), [134-142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L134-L142), [147-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L147-L155), [162-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L162-L170), [175-183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L175-L183), [203-203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L203-L203) ):

```solidity
104:     function _ROneSellBaseToken(
105:         PMMState memory state,
106:         uint256 payBaseAmount
107:     )
108:         internal
109:         pure
110:         returns (
111:             uint256 // receiveQuoteToken
112:         )

119:     function _ROneSellQuoteToken(
120:         PMMState memory state,
121:         uint256 payQuoteAmount
122:     )
123:         internal
124:         pure
125:         returns (
126:             uint256 // receiveBaseToken
127:         )

134:     function _RBelowSellQuoteToken(
135:         PMMState memory state,
136:         uint256 payQuoteAmount
137:     )
138:         internal
139:         pure
140:         returns (
141:             uint256 // receiveBaseToken
142:         )

147:     function _RBelowSellBaseToken(
148:         PMMState memory state,
149:         uint256 payBaseAmount
150:     )
151:         internal
152:         pure
153:         returns (
154:             uint256 // receiveQuoteToken
155:         )

162:     function _RAboveSellBaseToken(
163:         PMMState memory state,
164:         uint256 payBaseAmount
165:     )
166:         internal
167:         pure
168:         returns (
169:             uint256 // receiveQuoteToken
170:         )

175:     function _RAboveSellQuoteToken(
176:         PMMState memory state,
177:         uint256 payQuoteAmount
178:     )
179:         internal
180:         pure
181:         returns (
182:             uint256 // receiveBaseToken
183:         )

203:     function getMidPrice(PMMState memory state) internal pure returns (uint256) {
```

- *Factory.sol* ( [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L53-L53), [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L57-L57), [65-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L65-L72), [155-162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L155-L162) ):

```solidity
53:     function getPoolCount(address token0, address token1) external view returns (uint256) {

57:     function getUserPoolCount(address creator) external view returns (uint256) {

65:     function predictDeterministicAddress(
66:         address creator,
67:         address baseToken_,
68:         address quoteToken_,
69:         uint256 lpFeeRate_,
70:         uint256 i_,
71:         uint256 k_
72:     ) public view returns (address) {

155:     function _computeSalt(
156:         address sender_,
157:         address baseToken_,
158:         address quoteToken_,
159:         uint256 lpFeeRate_,
160:         uint256 i_,
161:         uint256 k_
162:     ) internal view returns (bytes32) {
```

- *MagicLpAggregator.sol* ( [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L29-L29), [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L33-L33), [37-37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L37-L37), [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L48-L48) ):

```solidity
29:     function decimals() external pure override returns (uint8) {

33:     function _getReserves() internal view virtual returns (uint256, uint256) {

37:     function latestAnswer() public view override returns (int256) {

48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```

- *LockingMultiRewards.sol* ( [199-199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L199-L199), [203-203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L203-L203), [207-207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L207-L207), [211-211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L211-L211), [215-215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L215-L215), [219-219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L219-L219), [223-223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L223-L223), [227-227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L227-L227), [231-231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L231-L231), [235-235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L235-L235), [239-239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L239-L239), [253-253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L253-L253), [257-257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L257-L257), [261-261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L261-L261), [265-265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L265-L265), [269-269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L269-L269), [273-273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L273-L273), [277-277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L277-L277), [288-288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L288-L288), [292-292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L292-L292) ):

```solidity
199:     function rewardData(address token) external view returns (Reward memory) {

203:     function rewardsForDuration(address rewardToken) external view returns (uint256) {

207:     function rewardTokensLength() external view returns (uint256) {

211:     function balances(address user) external view returns (Balances memory) {

215:     function userRewardLock(address user) external view returns (RewardLock memory) {

219:     function userLocks(address user) external view returns (LockedBalance[] memory) {

223:     function userLocksLength(address user) external view returns (uint256) {

227:     function locked(address user) external view returns (uint256) {

231:     function unlocked(address user) external view returns (uint256) {

235:     function totalSupply() public view returns (uint256) {

239:     function balanceOf(address user) public view returns (uint256) {

253:     function nextUnlockTime() public view returns (uint256) {

257:     function epoch() public view returns (uint256) {

261:     function nextEpoch() public view returns (uint256) {

265:     function remainingEpochTime() public view returns (uint256) {

269:     function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {

273:     function rewardPerToken(address rewardToken) public view returns (uint256) {

277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

288:     function earned(address user, address rewardToken) public view returns (uint256) {

292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {
```

</details>

### [N-68] Use `type(X).max` instead of constant formulas like `2**n`

Earlier versions of solidity can use `uint<n>(-1)` instead. Expressions `2**n -1` can often be rewritten to accommodate the change (e.g. by using a `>` instead of a `>=`, which will also saves gas).

There are 2 instances:

- *MagicLP.sol* ( [125-125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L125-L125), [546-546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L546-L546) ):

```solidity
125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

546:         uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
```

### [N-69] Consider using the `using`-`for` syntax

The `using`-`for` [syntax](https://docs.soliditylang.org/en/latest/contracts.html#using-for) is the more common way of calling library functions.

<details>
<summary>There are 96 instances (click to show):</summary>

- *BlastBox.sol* ( [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L53-L53), [61-61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L61-L61), [69-69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L69-L69), [87-87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L87-L87), [99-99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L99-L99), [100-100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L100-L100) ):

```solidity
53:         return BlastYields.claimMaxGasYields(feeTo);

61:         amount = BlastYields.claimAllTokenYields(token_, feeTo);

69:         BlastYields.callPrecompile(data);

87:             BlastYields.enableTokenClaimable(token);

99:         BlastYields.configureDefaultClaimables(address(this));

100:         BlastPoints.configure();
```

- *BlastDapp.sol* ( [8-8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L8-L8) ):

```solidity
8:         BlastPoints.configure();
```

- *BlastGovernor.sol* ( [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L21-L21), [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L29-L29), [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L33-L33), [50-50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L50-L50) ):

```solidity
21:         BlastYields.configureDefaultClaimables(address(this));

29:         return BlastYields.claimAllNativeYields(contractAddress, feeTo);

33:         return BlastYields.claimMaxGasYields(contractAddress, feeTo);

50:         BlastYields.callPrecompile(data);
```

- *BlastMagicLP.sol* ( [50-50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L50-L50), [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L57-L57), [60-60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L60-L60), [73-73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L73-L73), [99-99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L99-L99), [100-100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L100-L100), [106-106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L106-L106), [110-110](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L110-L110) ):

```solidity
50:         return BlastYields.claimMaxGasYields(feeTo_);

57:             token0Amount = BlastYields.claimAllTokenYields(_BASE_TOKEN_, feeTo_);

60:             token1Amount = BlastYields.claimAllTokenYields(_QUOTE_TOKEN_, feeTo_);

73:         BlastYields.callPrecompile(data);

99:         BlastYields.configureDefaultClaimables(address(this));

100:         BlastPoints.configure();

106:             BlastYields.enableTokenClaimable(_BASE_TOKEN_);

110:             BlastYields.enableTokenClaimable(_QUOTE_TOKEN_);
```

- *BlastOnboarding.sol* ( [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L59-L59), [60-60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L60-L60), [157-157](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L157-L157), [161-161](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L161-L161), [170-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L170-L170), [179-179](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L179-L179) ):

```solidity
59:         BlastYields.configureDefaultClaimables(address(this));

60:         BlastPoints.configure();

157:         BlastYields.callPrecompile(data);

161:         return BlastYields.claimMaxGasYields(feeTo);

170:                 BlastYields.claimAllTokenYields(tokens[i], feeTo);

179:             BlastYields.enableTokenClaimable(token);
```

- *BlastWrappers.sol* ( [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L24-L24), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L38-L38), [67-67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L67-L67) ):

```solidity
24:         BlastYields.configureDefaultClaimables(governor_);

38:         BlastYields.configureDefaultClaimables(governor_);

67:         BlastYields.configureDefaultClaimables(_governor);
```

- *BlastYields.sol* ( [87-87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L87-L87) ):

```solidity
87:         Address.functionCall(address(BLAST_YIELD_PRECOMPILE), data);
```

- *MagicLP.sol* ( [172-172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L172-L172), [175-175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L175-L175), [176-176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L176-L176), [185-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L185-L185), [188-188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L188-L188), [189-189](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L189-L189), [201-201](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L201-L201), [216-216](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L216-L216), [381-381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L381-L381), [381-381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L381-L381), [383-383](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L383-L383), [397-397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L397-L397), [398-398](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L398-L398), [400-400](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L400-L400), [402-402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L402-L402), [403-403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L403-L403) ):

```solidity
172:         (receiveQuoteAmount, newRState) = PMMPricing.sellBaseToken(state, payBaseAmount);

175:         mtFee = DecimalMath.mulFloor(receiveQuoteAmount, mtFeeRate);

176:         receiveQuoteAmount = receiveQuoteAmount - DecimalMath.mulFloor(receiveQuoteAmount, lpFeeRate) - mtFee;

185:         (receiveBaseAmount, newRState) = PMMPricing.sellQuoteToken(state, payQuoteAmount);

188:         mtFee = DecimalMath.mulFloor(receiveBaseAmount, mtFeeRate);

189:         receiveBaseAmount = receiveBaseAmount - DecimalMath.mulFloor(receiveBaseAmount, lpFeeRate) - mtFee;

201:         PMMPricing.adjustedTarget(state);

216:         return PMMPricing.getMidPrice(getPMMState());

381:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;

381:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;

383:             _QUOTE_TARGET_ = DecimalMath.mulFloor(shares, _I_).toUint112();

397:             uint256 baseInputRatio = DecimalMath.divFloor(baseInput, baseReserve);

398:             uint256 quoteInputRatio = DecimalMath.divFloor(quoteInput, quoteReserve);

400:             shares = DecimalMath.mulFloor(totalSupply(), mintRatio);

402:             _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

403:             _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
```

- *FeeRateModelImpl.sol* ( [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L14-L14) ):

```solidity
14:         mtFeeRate = Math.divCeil(lpFeeRate, 2);
```

- *Math.sol* ( [62-62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L62-L62), [63-63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L63-L63), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L81-L81), [101-101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L101-L101), [103-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L103-L103), [141-141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L141-L141), [141-141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L141-L141), [184-184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L184-L184), [184-184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L184-L184), [199-199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L199-L199) ):

```solidity
62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

63:         uint256 penalty = DecimalMath.mulFloor(k, V0V0V1V2); // k(V0^2/V1/V2)

81:             return V1 + DecimalMath.mulFloor(i, delta);

101:         uint256 premium = DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2) + DecimalMath.ONE;

103:         return DecimalMath.mulFloor(V1, premium);

141:             return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);

141:             return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);

184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2

184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2

199:         uint256 V2 = DecimalMath.divCeil(numerator, denominator);
```

- *PMMPricing.sol* ( [116-116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L116-L116), [129-129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L129-L129), [129-129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L129-L129), [144-144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L144-L144), [144-144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L144-L144), [157-157](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L157-L157), [172-172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L172-L172), [185-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L185-L185), [185-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L185-L185), [192-192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L192-L192), [194-199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L194-L199), [197-197](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L197-L197), [205-205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L205-L205), [206-206](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L206-L206), [207-207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L207-L207), [209-209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L209-L209), [210-210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L210-L210), [211-211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L211-L211) ):

```solidity
116:         return Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q0, payBaseAmount, state.i, state.K);

129:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);

129:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);

144:         return Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K);

144:         return Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K);

157:         return Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q, payBaseAmount, state.i, state.K);

172:         return Math._GeneralIntegrate(state.B0, state.B + payBaseAmount, state.B, state.i, state.K);

185:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);

185:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);

192:             state.Q0 = Math._SolveQuadraticFunctionForTarget(state.Q, state.B - state.B0, state.i, state.K);

194:             state.B0 = Math._SolveQuadraticFunctionForTarget(
195:                 state.B,
196:                 state.Q - state.Q0,
197:                 DecimalMath.reciprocalFloor(state.i),
198:                 state.K
199:             );

197:                 DecimalMath.reciprocalFloor(state.i),

205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);

206:             R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);

207:             return DecimalMath.divFloor(state.i, R);

209:             uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);

210:             R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);

211:             return DecimalMath.mulFloor(state.i, R);
```

- *Factory.sol* ( [74-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L74-L78), [85-85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L85-L85) ):

```solidity
74:             LibClone.predictDeterministicAddress(
75:                 implementation,
76:                 _computeSalt(creator, baseToken_, quoteToken_, lpFeeRate_, i_, k_),
77:                 address(this)
78:             );

85:         clone = LibClone.cloneDeterministic(address(implementation), salt);
```

- *Router.sol* ( [101-101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L101-L101), [101-101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L101-L101), [103-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L103-L103), [138-138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L138-L138), [138-138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L138-L138), [140-140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L140-L140), [148-148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L148-L148), [149-149](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L149-L149), [152-152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L152-L152), [153-153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L153-L153), [156-156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L156-L156), [157-157](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L157-L157), [523-523](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L523-L523), [523-523](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L523-L523), [525-525](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L525-L525), [528-528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L528-L528), [529-529](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L529-L529), [532-532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L532-L532), [535-535](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L535-L535) ):

```solidity
101:         shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

101:         shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

103:         quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);

138:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;

138:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;

140:             quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);

148:             uint256 baseInputRatio = DecimalMath.divFloor(baseInAmount, baseReserve);

149:             uint256 quoteInputRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);

152:                 quoteAdjustedInAmount = DecimalMath.mulCeil(quoteReserve, baseInputRatio);

153:                 shares = DecimalMath.mulFloor(totalSupply, baseInputRatio);

156:                 baseAdjustedInAmount = DecimalMath.mulCeil(baseReserve, quoteInputRatio);

157:                 shares = DecimalMath.mulFloor(totalSupply, quoteInputRatio);

523:             uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

523:             uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

525:             quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);

528:                 uint256 baseIncreaseRatio = DecimalMath.divFloor(baseInAmount, baseReserve);

529:                 uint256 quoteIncreaseRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);

532:                     quoteAdjustedInAmount = DecimalMath.mulFloor(quoteReserve, baseIncreaseRatio);

535:                     baseAdjustedInAmount = DecimalMath.mulFloor(baseReserve, quoteIncreaseRatio);
```

- *LockingMultiRewards.sol* ( [270-270](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L270-L270) ):

```solidity
270:         return MathLib.min(block.timestamp, _rewardData[rewardToken].periodFinish);
```

</details>

### [N-70] Using underscore at the end of variable name

The use of the underscore at the end of the variable name is unusual, consider refactoring it.

<details>
<summary>There are 98 instances (click to show):</summary>

- *BlastBox.sol* ( [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L24-L24), [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L24-L24), [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L24-L24), [56-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L56-L56), [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L72-L72) ):

```solidity
/// @audit weth_
24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

/// @audit registry_
24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

/// @audit feeTo_
24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

/// @audit token_
56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

/// @audit feeTo_
72:     function setFeeTo(address feeTo_) external onlyOwner {
```

- *BlastGovernor.sol* ( [15-15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L15-L15) ):

```solidity
/// @audit feeTo_
15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```

- *BlastMagicLP.sol* ( [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L23-L23), [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L23-L23), [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L23-L23), [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L48-L48), [54-54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L54-L54), [80-80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L80-L80) ):

```solidity
/// @audit registry_
23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

/// @audit feeTo_
23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

/// @audit owner_
23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

/// @audit feeTo_
48:         address feeTo_ = BlastMagicLP(address(implementation)).feeTo();

/// @audit feeTo_
54:         address feeTo_ = BlastMagicLP(address(implementation)).feeTo();

/// @audit feeTo_
80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
```

- *BlastOnboarding.sol* ( [84-84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L84-L84), [84-84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L84-L84), [101-101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L101-L101), [147-147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L147-L147), [190-190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L190-L190) ):

```solidity
/// @audit registry_
84:     constructor(BlastTokenRegistry registry_, address feeTo_) {

/// @audit feeTo_
84:     constructor(BlastTokenRegistry registry_, address feeTo_) {

/// @audit lock_
101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

/// @audit feeTo_
147:     function setFeeTo(address feeTo_) external onlyOwner {

/// @audit bootstrapper_
190:     function setBootstrapper(address bootstrapper_) external onlyOwner {
```

- *BlastWrappers.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L20-L20), [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L20-L20), [30-30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L30-L30), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L31-L31), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L32-L32), [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L33-L33), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L47-L47), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L47-L47), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L47-L47) ):

```solidity
/// @audit weth_
20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

/// @audit governor_
20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

/// @audit implementation_
30:         address implementation_,

/// @audit maintainerFeeRateModel_
31:         IFeeRateModel maintainerFeeRateModel_,

/// @audit owner_
32:         address owner_,

/// @audit governor_
33:         address governor_

/// @audit box_
47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {

/// @audit mim_
47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {

/// @audit governor_
47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
```

- *BlastYields.sol* ( [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L29-L29) ):

```solidity
/// @audit governor_
29:     function configureDefaultClaimables(address governor_) internal {
```

- *MagicLP.sol* ( [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L68-L68), [70-70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L70-L70), [71-71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L71-L71), [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L72-L72), [73-73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L73-L73), [74-74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L74-L74), [75-75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L75-L75), [76-76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L76-L76), [77-77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L77-L77), [78-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L78-L78), [79-79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L79-L79), [80-80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L80-L80), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L81-L81), [82-82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L82-L82), [84-84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L84-L84) ):

```solidity
/// @audit _INITIALIZED_
68:     bool internal _INITIALIZED_;

/// @audit _BASE_TOKEN_
70:     address public _BASE_TOKEN_;

/// @audit _QUOTE_TOKEN_
71:     address public _QUOTE_TOKEN_;

/// @audit _BASE_RESERVE_
72:     uint112 public _BASE_RESERVE_;

/// @audit _QUOTE_RESERVE_
73:     uint112 public _QUOTE_RESERVE_;

/// @audit _BLOCK_TIMESTAMP_LAST_
74:     uint32 public _BLOCK_TIMESTAMP_LAST_;

/// @audit _BASE_PRICE_CUMULATIVE_LAST_
75:     uint256 public _BASE_PRICE_CUMULATIVE_LAST_;

/// @audit _BASE_TARGET_
76:     uint112 public _BASE_TARGET_;

/// @audit _QUOTE_TARGET_
77:     uint112 public _QUOTE_TARGET_;

/// @audit _RState_
78:     uint32 public _RState_;

/// @audit _MT_FEE_RATE_MODEL_
79:     IFeeRateModel public _MT_FEE_RATE_MODEL_;

/// @audit _LP_FEE_RATE_
80:     uint256 public _LP_FEE_RATE_;

/// @audit _K_
81:     uint256 public _K_;

/// @audit _I_
82:     uint256 public _I_;

/// @audit owner_
84:     constructor(address owner_) Owned(owner_) {
```

- *FeeRateModel.sol* ( [22-22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L22-L22), [22-22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L22-L22), [46-46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L46-L46), [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L57-L57) ):

```solidity
/// @audit maintainer_
22:     constructor(address maintainer_, address owner_) Owned(owner_) {

/// @audit owner_
22:     constructor(address maintainer_, address owner_) Owned(owner_) {

/// @audit maintainer_
46:     function setMaintainer(address maintainer_) external onlyOwner {

/// @audit implementation_
57:     function setImplementation(address implementation_) public onlyOwner {
```

- *Factory.sol* ( [13-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L13-L13), [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L14-L14), [15-15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L15-L15), [16-16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L16-L16), [17-17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L17-L17), [19-19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L19-L19), [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L20-L20), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L38-L38), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L38-L38), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L38-L38), [67-67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L67-L67), [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L68-L68), [69-69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L69-L69), [70-70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L70-L70), [71-71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L71-L71), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81-L81), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81-L81), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81-L81), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81-L81), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81-L81), [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L96-L96), [105-105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L105-L105), [156-156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L156-L156), [157-157](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L157-L157), [158-158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L158-L158), [159-159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L159-L159), [160-160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L160-L160), [161-161](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L161-L161) ):

```solidity
/// @audit clone_
13:         address clone_,

/// @audit baseToken_
14:         address indexed baseToken_,

/// @audit quoteToken_
15:         address indexed quoteToken_,

/// @audit creator_
16:         address indexed creator_,

/// @audit lpFeeRate_
17:         uint256 lpFeeRate_,

/// @audit i_
19:         uint256 i_,

/// @audit k_
20:         uint256 k_

/// @audit implementation_
38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

/// @audit maintainerFeeRateModel_
38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

/// @audit owner_
38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

/// @audit baseToken_
67:         address baseToken_,

/// @audit quoteToken_
68:         address quoteToken_,

/// @audit lpFeeRate_
69:         uint256 lpFeeRate_,

/// @audit i_
70:         uint256 i_,

/// @audit k_
71:         uint256 k_

/// @audit baseToken_
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

/// @audit quoteToken_
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

/// @audit lpFeeRate_
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

/// @audit i_
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

/// @audit k_
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

/// @audit implementation_
96:     function setLpImplementation(address implementation_) external onlyOwner {

/// @audit maintainerFeeRateModel_
105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

/// @audit sender_
156:         address sender_,

/// @audit baseToken_
157:         address baseToken_,

/// @audit quoteToken_
158:         address quoteToken_,

/// @audit lpFeeRate_
159:         uint256 lpFeeRate_,

/// @audit i_
160:         uint256 i_,

/// @audit k_
161:         uint256 k_
```

- *Router.sol* ( [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L38-L38), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L38-L38) ):

```solidity
/// @audit weth_
38:     constructor(IWETH weth_, IFactory factory_) {

/// @audit factory_
38:     constructor(IWETH weth_, IFactory factory_) {
```

- *MagicLpAggregator.sol* ( [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L21-L21), [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L21-L21), [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L21-L21) ):

```solidity
/// @audit pair_
21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {

/// @audit baseOracle_
21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {

/// @audit quoteOracle_
21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```

- *LockingMultiRewards.sol* ( [150-150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L150-L150), [277-277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L277-L277), [277-277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L277-L277), [292-292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L292-L292), [292-292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L292-L292), [349-349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L349-L349), [458-458](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L458-L458), [528-528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L528-L528), [528-528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L528-L528), [528-528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L528-L528), [529-529](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L529-L529), [536-536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L536-L536), [536-536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L536-L536), [536-536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L536-L536), [536-536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L536-L536), [545-545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L545-L545), [559-559](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L559-L559), [573-573](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L573-L573), [577-577](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L577-L577) ):

```solidity
/// @audit lock_
150:     function stake(uint256 amount, bool lock_) public whenNotPaused {

/// @audit lastTimeRewardApplicable_
277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

/// @audit totalSupply_
277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

/// @audit balance_
292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

/// @audit rewardPerToken_
292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

/// @audit lock_
349:     function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {

/// @audit lock_
458:     function _stakeFor(address account, uint256 amount, bool lock_) internal {

/// @audit token_
528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

/// @audit totalSupply_
528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

/// @audit rewardPerToken_
528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

/// @audit lastTimeRewardApplicable_
529:         uint256 lastTimeRewardApplicable_ = lastTimeRewardApplicable(token_);

/// @audit user_
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

/// @audit balance_
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

/// @audit token_
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

/// @audit rewardPerToken_
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

/// @audit totalSupply_
545:         uint256 totalSupply_ = totalSupply();

/// @audit totalSupply_
559:         uint256 totalSupply_ = totalSupply();

/// @audit totalSupply_
573:         uint256 totalSupply_ = totalSupply();

/// @audit rewardPerToken_
577:             uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);
```

</details>

### [N-71] Use a struct to encapsulate multiple function parameters

If a function has too many parameters, replacing them with a struct can improve code readability and maintainability, increase reusability, and reduce the likelihood of errors when passing the parameters.

<details>
<summary>There are 8 instances (click to show):</summary>

- *BlastBox.sol* ( [36-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L36-L42) ):

```solidity
36:     function _onBeforeDeposit(
37:         IERC20 token,
38:         address /*from*/,
39:         address /*to*/,
40:         uint256 /*amount*/,
41:         uint256 /*share*/
42:     ) internal view override {
```

- *MagicLP.sol* ( [91-98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L91-L98), [413-420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L413-L420), [470-479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L470-L479) ):

```solidity
91:     function init(
92:         address baseTokenAddress,
93:         address quoteTokenAddress,
94:         uint256 lpFeeRate,
95:         address mtFeeRateModel,
96:         uint256 i,
97:         uint256 k
98:     ) external {

413:     function sellShares(
414:         uint256 shareAmount,
415:         address to,
416:         uint256 baseMinAmount,
417:         uint256 quoteMinAmount,
418:         bytes calldata data,
419:         uint256 deadline
420:     ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {

470:     function setParameters(
471:         address assetTo,
472:         uint256 newLpFeeRate,
473:         uint256 newI,
474:         uint256 newK,
475:         uint256 baseOutAmount,
476:         uint256 quoteOutAmount,
477:         uint256 minBaseReserve,
478:         uint256 minQuoteReserve
479:     ) public nonReentrant onlyImplementationOwner {
```

- *Factory.sol* ( [65-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L65-L72), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81-L81), [120-126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L120-L126), [155-162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L155-L162) ):

```solidity
65:     function predictDeterministicAddress(
66:         address creator,
67:         address baseToken_,
68:         address quoteToken_,
69:         uint256 lpFeeRate_,
70:         uint256 i_,
71:         uint256 k_
72:     ) public view returns (address) {

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

120:     function removePool(
121:         address creator,
122:         address baseToken,
123:         address quoteToken,
124:         uint256 poolIndex,
125:         uint256 userPoolIndex
126:     ) external onlyOwner {

155:     function _computeSalt(
156:         address sender_,
157:         address baseToken_,
158:         address quoteToken_,
159:         uint256 lpFeeRate_,
160:         uint256 i_,
161:         uint256 k_
162:     ) internal view returns (bytes32) {
```

</details>

### [N-72] Returning a struct instead of a bunch of variables is better

If a function returns [too many variables](https://docs.soliditylang.org/en/v0.8.21/contracts.html#returning-multiple-values), replacing them with a struct can improve code readability, maintainability and reusability.

<details>
<summary>There are 6 instances (click to show):</summary>

- *BlastGovernor.sol* ( [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L53-L53) ):

```solidity
53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

- *BlastMagicLP.sol* ( [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L53-L53) ):

```solidity
53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {
```

- *BlastOnboardingBoot.sol* ( [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L86-L86), [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L96-L96) ):

```solidity
86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
```

- *MagicLP.sol* ( [167-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L167-L170), [180-183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L180-L183) ):

```solidity
167:     function querySellBase(
168:         address trader,
169:         uint256 payBaseAmount
170:     ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {

180:     function querySellQuote(
181:         address trader,
182:         uint256 payQuoteAmount
183:     ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {
```

</details>

### [N-73] Events that mark critical parameter changes should contain both the old and the new value

This should especially be done if the new value is not required to be different from the old value.

<details>
<summary>There are 15 instances (click to show):</summary>

- *BlastBox.sol* ( [78-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L78-L78) ):

```solidity
78:         emit LogFeeToChanged(feeTo_);
```

- *BlastGovernor.sol* ( [46-46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L46-L46) ):

```solidity
46:         emit LogFeeToChanged(_feeTo);
```

- *BlastMagicLP.sol* ( [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L86-L86), [91-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L91-L91) ):

```solidity
86:         emit LogFeeToChanged(feeTo_);

91:         emit LogOperatorChanged(operator, status);
```

- *BlastOnboarding.sol* ( [153-153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L153-L153), [187-187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L187-L187), [192-192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L192-L192), [197-197](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L197-L197), [202-202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L202-L202) ):

```solidity
153:         emit LogFeeToChanged(feeTo_);

187:         emit LogTokenCapChanged(token, cap);

192:         emit LogBootstrapperChanged(bootstrapper_);

197:         emit LogStateChange(State.Opened);

202:         emit LogStateChange(State.Closed);
```

- *BlastOnboardingBoot.sol* ( [143-143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L143-L143), [148-148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L148-L148) ):

```solidity
143:         emit LogStakingChanged(address(_staking));

148:         emit LogReadyChanged(ready);
```

- *FeeRateModel.sol* ( [52-52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L52-L52), [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L59-L59) ):

```solidity
52:         emit LogMaintainerChanged(maintainer_);

59:         emit LogImplementationChanged(implementation_);
```

- *Factory.sol* ( [102-102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L102-L102), [111-111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L111-L111) ):

```solidity
102:         emit LogSetImplementation(implementation_);

111:         emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);
```

</details>

### [N-74] Contract variables should have comments

Consider adding some comments on non-public contract variables to explain what they are supposed to do. This will help for future code reviews.

There are 6 instances:

- *BlastWrappers.sol* ( [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L45-L45) ):

```solidity
45:     address private immutable _governor;
```

- *MagicLP.sol* ( [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L68-L68) ):

```solidity
68:     bool internal _INITIALIZED_;
```

- *LockingMultiRewards.sol* ( [89-89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L89-L89), [90-90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L90-L90), [91-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L91-L91), [92-92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L92-L92) ):

```solidity
89:     mapping(address token => Reward info) private _rewardData;

90:     mapping(address user => Balances balances) private _balances;

91:     mapping(address user => LockedBalance[] locks) private _userLocks;

92:     mapping(address user => RewardLock rewardLock) private _userRewardLock;
```

### [N-75] Missing event when a state variables is set in constructor

The initial states set in a constructor are important and should be recorded in the event.

<details>
<summary>There are 9 instances (click to show):</summary>

- *BlastBox.sol* ( [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L33) ):

```solidity
33:         feeTo = feeTo_;
```

- *BlastGovernor.sol* ( [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L20) ):

```solidity
20:         feeTo = feeTo_;
```

- *BlastMagicLP.sol* ( [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L32) ):

```solidity
32:         feeTo = feeTo_;
```

- *BlastOnboarding.sol* ( [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L93), [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L94) ):

```solidity
93:         registry = registry_;

94:         feeTo = feeTo_;
```

- *MagicLP.sol* ( [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L88) ):

```solidity
88:         _INITIALIZED_ = true;
```

- *FeeRateModel.sol* ( [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L27) ):

```solidity
27:         maintainer = maintainer_;
```

- *Factory.sol* ( [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L45), [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L46) ):

```solidity
45:         implementation = implementation_;

46:         maintainerFeeRateModel = maintainerFeeRateModel_;
```

</details>

### [N-76] File is missing NatSpec

It is recommended that Solidity contracts are fully annotated using NatSpec

There are 8 instances:

- [*BlastDapp.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol)

- [*BlastGovernor.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol)

- [*BlastOnboarding.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol)

- [*BlastTokenRegistry.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol)

- [*BlastPoints.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol)

- [*BlastYields.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol)

- [*FeeRateModelImpl.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol)

- [*Router.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol)

### [N-77] Empty bytes check is missing

Passing empty bytes to a function can cause unexpected behavior, such as certain operations failing, producing incorrect results, or wasting gas. It is recommended to check that all byte parameters are not empty.

<details>
<summary>There are 6 instances (click to show):</summary>

- *BlastBox.sol* ( [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L68-L68) ):

```solidity
/// @audit data
68:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
```

- *BlastGovernor.sol* ( [49-49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L49-L49), [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L53-L53) ):

```solidity
/// @audit data
49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

/// @audit data
53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

- *BlastMagicLP.sol* ( [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L72-L72) ):

```solidity
/// @audit data
72:     function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {
```

- *BlastOnboarding.sol* ( [156-156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L156-L156) ):

```solidity
/// @audit data
156:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
```

- *BlastWrappers.sol* ( [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L59-L59) ):

```solidity
/// @audit data
59:     function init(bytes calldata data) public payable override {
```

</details>

### [N-78] Don't define functions with the same name in a contract

In Solidity, while function overriding allows for functions with the same name to coexist, it is advisable to avoid this practice to enhance code readability and maintainability. Having multiple functions with the same name, even with different parameters or in inherited contracts, can cause confusion and increase the likelihood of errors during development, testing, and debugging. Using distinct and descriptive function names not only clarifies the purpose and behavior of each function, but also helps prevent unintended function calls or incorrect overriding. By adopting a clear and consistent naming convention, developers can create more comprehensible and maintainable smart contracts.

There are 2 instances:

- *BlastYields.sol* ( [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L42), [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L55) ):

```solidity
/// @audit Different function with same name found on line 38
42:     function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {

/// @audit Different function with same name found on line 51
55:     function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {
```

### [N-79] Multiple mappings with same keys can be combined into a single struct mapping for readability

Well-organized data structures make code reviews easier, which may lead to fewer bugs. Consider combining related mappings into mappings to structs, so it's clear what data is related.

<details>
<summary>There are 13 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [36-36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L36-L36), [37-37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L37-L37), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L38-L38), [41-41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L41-L41) ):

```solidity
36:     mapping(address token => bool) public supportedTokens;

37:     mapping(address token => Balances) public totals;

38:     mapping(address token => uint256 cap) public caps;

41:     mapping(address user => mapping(address token => Balances)) public balances;
```

- *Factory.sol* ( [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L35-L35), [36-36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L36-L36) ):

```solidity
35:     mapping(address base => mapping(address quote => address[] pools)) public pools;

36:     mapping(address creator => address[] pools) public userPools;
```

- *LockingMultiRewards.sol* ( [89-89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L89-L89), [90-90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L90-L90), [91-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L91-L91), [92-92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L92-L92), [94-94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L94-L94), [95-95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L95-L95), [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L96-L96) ):

```solidity
89:     mapping(address token => Reward info) private _rewardData;

90:     mapping(address user => Balances balances) private _balances;

91:     mapping(address user => LockedBalance[] locks) private _userLocks;

92:     mapping(address user => RewardLock rewardLock) private _userRewardLock;

94:     mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;

95:     mapping(address user => mapping(address token => uint256 amount)) public rewards;

96:     mapping(address user => uint256 index) public lastLockIndex;
```

</details>

### [N-80] Function state mutability can be restricted to view

Function state mutability can be restricted to view

There is 1 instance:

- *MagicLP.sol* ( [601-601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L601-L601) ):

```solidity
601:     function _afterInitialized() internal virtual {}
```

### [N-81] Functions contain the same code

The functions below have the same implementation as is seen in other files. The functions should be refactored into functions of a common base contract.

<details>
<summary>There are 10 instances (click to show):</summary>

- *BlastBox.sol* ( [68-70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L68-L70), [72-79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L72-L79) ):

```solidity
/// @audit Seen on line 49 of src/blast/BlastGovernor.sol
68:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
69:         BlastYields.callPrecompile(data);
70:     }

/// @audit Seen on line 40 of src/blast/BlastGovernor.sol
72:     function setFeeTo(address feeTo_) external onlyOwner {
73:         if (feeTo_ == address(0)) {
74:             revert ErrZeroAddress();
75:         }
76: 
77:         feeTo = feeTo_;
78:         emit LogFeeToChanged(feeTo_);
79:     }
```

- *BlastGovernor.sol* ( [40-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L40-L47), [49-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L49-L51) ):

```solidity
/// @audit Seen on line 72 of src/blast/BlastBox.sol
40:     function setFeeTo(address _feeTo) external onlyOwner {
41:         if(_feeTo == address(0)) {
42:             revert ErrZeroAddress();
43:         }
44:         
45:         feeTo = _feeTo;
46:         emit LogFeeToChanged(_feeTo);
47:     }

/// @audit Seen on line 68 of src/blast/BlastBox.sol
49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
50:         BlastYields.callPrecompile(data);
51:     }
```

- *BlastOnboarding.sol* ( [147-154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L147-L154), [156-158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L156-L158), [214-216](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L214-L216), [218-220](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L218-L220) ):

```solidity
/// @audit Seen on line 40 of src/blast/BlastGovernor.sol
147:     function setFeeTo(address feeTo_) external onlyOwner {
148:         if (feeTo_ == address(0)) {
149:             revert ErrZeroAddress();
150:         }
151: 
152:         feeTo = feeTo_;
153:         emit LogFeeToChanged(feeTo_);
154:     }

/// @audit Seen on line 49 of src/blast/BlastGovernor.sol
156:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
157:         BlastYields.callPrecompile(data);
158:     }

/// @audit Seen on line 337 of src/staking/LockingMultiRewards.sol
214:     function pause() external onlyOwner {
215:         _pause();
216:     }

/// @audit Seen on line 341 of src/staking/LockingMultiRewards.sol
218:     function unpause() external onlyOwner {
219:         _unpause();
220:     }
```

- *LockingMultiRewards.sol* ( [337-339](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L337-L339), [341-343](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L341-L343) ):

```solidity
/// @audit Seen on line 214 of src/blast/BlastOnboarding.sol
337:     function pause() external onlyOwner {
338:         _pause();
339:     }

/// @audit Seen on line 218 of src/blast/BlastOnboarding.sol
341:     function unpause() external onlyOwner {
342:         _unpause();
343:     }
```

</details>

### [N-82] Inconsistent spacing in comments

The comments below are in the `//x` format, which differs from the commonly used idiomatic comment syntax of `//<space>x`. It is recommended to use a consistent comment syntax throughout.

<details>
<summary>There are 88 instances (click to show):</summary>

- *BlastBox.sol* ( [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L48), [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L50), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L64), [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L66), [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L93), [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L95) ):

```solidity
48:     //////////////////////////////////////////////////////////////////////////////////////

50:     //////////////////////////////////////////////////////////////////////////////////////

64:     //////////////////////////////////////////////////////////////////////////////////////

66:     //////////////////////////////////////////////////////////////////////////////////////

93:     //////////////////////////////////////////////////////////////////////////////////////

95:     //////////////////////////////////////////////////////////////////////////////////////
```

- *BlastGovernor.sol* ( [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L24), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L26), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L36), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L38) ):

```solidity
24:     //////////////////////////////////////////////////////////////////////////////////////

26:     //////////////////////////////////////////////////////////////////////////////////////

36:     //////////////////////////////////////////////////////////////////////////////////////

38:     //////////////////////////////////////////////////////////////////////////////////////
```

- *BlastMagicLP.sol* ( [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L35), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L37), [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L43), [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L45), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L68), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L70), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L76), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L78), [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L94), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L96), [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L114), [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L116) ):

```solidity
35:     //////////////////////////////////////////////////////////////////////////////////////

37:     //////////////////////////////////////////////////////////////////////////////////////

43:     //////////////////////////////////////////////////////////////////////////////////////

45:     //////////////////////////////////////////////////////////////////////////////////////

68:     //////////////////////////////////////////////////////////////////////////////////////

70:     //////////////////////////////////////////////////////////////////////////////////////

76:     //////////////////////////////////////////////////////////////////////////////////////

78:     //////////////////////////////////////////////////////////////////////////////////////

94:     //////////////////////////////////////////////////////////////////////////////////////

96:     //////////////////////////////////////////////////////////////////////////////////////

114:     //////////////////////////////////////////////////////////////////////////////////////

116:     //////////////////////////////////////////////////////////////////////////////////////
```

- *BlastOnboarding.sol* ( [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L97), [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L99), [143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L143), [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L145), [222](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L222), [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L224) ):

```solidity
97:     //////////////////////////////////////////////////////////////////////////////////////

99:     //////////////////////////////////////////////////////////////////////////////////////

143:     //////////////////////////////////////////////////////////////////////////////////////

145:     //////////////////////////////////////////////////////////////////////////////////////

222:     //////////////////////////////////////////////////////////////////////////////////////

224:     //////////////////////////////////////////////////////////////////////////////////////
```

- *BlastOnboardingBoot.sol* ( [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L51), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L53), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L74), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L76), [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L92), [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L94), [151](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L151), [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L153) ):

```solidity
51:     //////////////////////////////////////////////////////////////////////////////////////

53:     //////////////////////////////////////////////////////////////////////////////////////

74:     //////////////////////////////////////////////////////////////////////////////////////

76:     //////////////////////////////////////////////////////////////////////////////////////

92:     //////////////////////////////////////////////////////////////////////////////////////

94:     //////////////////////////////////////////////////////////////////////////////////////

151:     //////////////////////////////////////////////////////////////////////////////////////

153:     //////////////////////////////////////////////////////////////////////////////////////
```

- *BlastYields.sol* ( [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L16), [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L18), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L34), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L36), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L47), [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L49), [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L66), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L68), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L81), [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L84) ):

```solidity
16:     //////////////////////////////////////////////////////////////////////////////////////

18:     //////////////////////////////////////////////////////////////////////////////////////

34:     //////////////////////////////////////////////////////////////////////////////////////

36:     //////////////////////////////////////////////////////////////////////////////////////

47:     //////////////////////////////////////////////////////////////////////////////////////

49:     //////////////////////////////////////////////////////////////////////////////////////<

66:     //////////////////////////////////////////////////////////////////////////////////////

68:     //////////////////////////////////////////////////////////////////////////////////////

81:     //////////////////////////////////////////////////////////////////////////////////////

84:     //////////////////////////////////////////////////////////////////////////////////////
```

- *MagicLP.sol* ( [130](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L130), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L132), [151](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L151), [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L153), [240](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L240), [242](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L242), [355](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L355), [357](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L357), [457](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L457), [459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L459), [524](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L524), [526](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L526), [603](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L603), [605](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L605) ):

```solidity
130:     //////////////////////////////////////////////////////////////////////////////////////

132:     //////////////////////////////////////////////////////////////////////////////////////

151:     //////////////////////////////////////////////////////////////////////////////////////

153:     //////////////////////////////////////////////////////////////////////////////////////

240:     //////////////////////////////////////////////////////////////////////////////////////

242:     //////////////////////////////////////////////////////////////////////////////////////

355:     //////////////////////////////////////////////////////////////////////////////////////

357:     //////////////////////////////////////////////////////////////////////////////////////

457:     //////////////////////////////////////////////////////////////////////////////////////

459:     //////////////////////////////////////////////////////////////////////////////////////

524:     //////////////////////////////////////////////////////////////////////////////////////

526:     //////////////////////////////////////////////////////////////////////////////////////

603:     //////////////////////////////////////////////////////////////////////////////////////

605:     //////////////////////////////////////////////////////////////////////////////////////
```

- *FeeRateModel.sol* ( [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L30), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L32), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L42), [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L44) ):

```solidity
30:     //////////////////////////////////////////////////////////////////////////////////////

32:     //////////////////////////////////////////////////////////////////////////////////////

42:     //////////////////////////////////////////////////////////////////////////////////////

44:     //////////////////////////////////////////////////////////////////////////////////////
```

- *Factory.sol* ( [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L49), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L51), [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L61), [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L63), [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L92), [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L94), [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L144), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L146) ):

```solidity
49:     //////////////////////////////////////////////////////////////////////////////////////

51:     //////////////////////////////////////////////////////////////////////////////////////

61:     //////////////////////////////////////////////////////////////////////////////////////

63:     //////////////////////////////////////////////////////////////////////////////////////

92:     //////////////////////////////////////////////////////////////////////////////////////

94:     //////////////////////////////////////////////////////////////////////////////////////

144:     //////////////////////////////////////////////////////////////////////////////////////

146:     //////////////////////////////////////////////////////////////////////////////////////
```

- *Router.sol* ( [495](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L495), [497](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L497) ):

```solidity
495:     //////////////////////////////////////////////////////////////////////////////////////

497:     //////////////////////////////////////////////////////////////////////////////////////
```

- *LockingMultiRewards.sol* ( [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L105), [196](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L196), [198](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L198), [297](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L297), [299](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L299), [334](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L334), [336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L336), [345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L345), [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L347), [455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L455), [457](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L457), [518](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L518), [521](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L521), [525](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L525) ):

```solidity
105:     ///

196:     //////////////////////////////////////////////////////////////////////////////////////////////

198:     //////////////////////////////////////////////////////////////////////////////////////////////

297:     //////////////////////////////////////////////////////////////////////////////////////////////

299:     //////////////////////////////////////////////////////////////////////////////////////////////

334:     //////////////////////////////////////////////////////////////////////////////////////////////

336:     //////////////////////////////////////////////////////////////////////////////////////////////

345:     //////////////////////////////////////////////////////////////////////////////////////////////

347:     //////////////////////////////////////////////////////////////////////////////////////////////

455:     //////////////////////////////////////////////////////////////////////////////////////////////

457:     //////////////////////////////////////////////////////////////////////////////////////////////

518:     ///

521:     ///

525:     ///
```

</details>

### [N-83] Missing event for critical changes

Events should be emitted when critical changes are made to the contracts.

There is 1 instance:

- *LockingMultiRewards.sol* ( [300-315](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L300-L315) ):

```solidity
300:     function addReward(address rewardToken) public onlyOwner {
301:         if (rewardToken == address(0)) {
302:             revert ErrInvalidTokenAddress();
303:         }
304: 
305:         if (_rewardData[rewardToken].exists) {
306:             revert ErrRewardAlreadyExists();
307:         }
308: 
309:         if (rewardTokens.length == MAX_NUM_REWARDS) {
310:             revert ErrMaxRewardsExceeded();
311:         }
312: 
313:         rewardTokens.push(rewardToken);
314:         _rewardData[rewardToken].exists = true;
315:     }
```

### [N-84] Duplicated `require()`/`revert()` checks should be refactored

Refactoring duplicate `require()`/`revert()` checks into a modifier or function can make the code more concise, readable and maintainable, and less likely to make errors or omissions when modifying the `require()` or `revert()`.

<details>
<summary>There are 29 instances (click to show):</summary>

- *BlastBox.sol* ( [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L26-L26), [44-44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L44-L44) ):

```solidity
/// @audit Duplicated on line 29, 74
26:             revert ErrZeroAddress();

/// @audit Duplicated on line 58
44:             revert ErrUnsupportedToken();
```

- *BlastGovernor.sol* ( [17-17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L17-L17) ):

```solidity
/// @audit Duplicated on line 42
17:             revert ErrZeroAddress();
```

- *BlastMagicLP.sol* ( [25-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L25-L25) ):

```solidity
/// @audit Duplicated on line 28, 82
25:             revert ErrZeroAddress();
```

- *BlastOnboarding.sol* ( [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L86-L86) ):

```solidity
/// @audit Duplicated on line 90, 149
86:             revert ErrZeroAddress();
```

- *BlastWrappers.sol* ( [52-52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L52-L52) ):

```solidity
/// @audit Duplicated on line 61
52:             revert ErrInvalidGovernorAddress();
```

- *MagicLP.sol* ( [109-109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L109-L109), [112-112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L112-L112), [115-115](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L115-L115), [303-303](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L303-L303), [390-390](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L390-L390), [509-509](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L509-L509) ):

```solidity
/// @audit Duplicated on line 484
109:             revert ErrInvalidI();

/// @audit Duplicated on line 487
112:             revert ErrInvalidK();

/// @audit Duplicated on line 490
115:             revert ErrInvalidLPFeeRate();

/// @audit Duplicated on line 316, 338
303:             revert ErrFlashLoanFailed();

/// @audit Duplicated on line 595
390:                 revert ErrMintAmountNotEnough();

/// @audit Duplicated on line 533
509:             revert ErrOverflow();
```

- *FeeRateModel.sol* ( [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L24-L24) ):

```solidity
/// @audit Duplicated on line 48
24:             revert ErrZeroAddress();
```

- *Factory.sol* ( [40-40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L40-L40) ):

```solidity
/// @audit Duplicated on line 43, 98, 107
40:             revert ErrZeroAddress();
```

- *Router.sol* ( [213-213](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L213-L213), [424-424](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L424-L424), [440-440](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L440-L440), [567-567](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L567-L567) ):

```solidity
/// @audit Duplicated on line 240, 305
213:             revert ErrNotETHLP();

/// @audit Duplicated on line 486
424:             revert ErrInvalidBaseToken();

/// @audit Duplicated on line 470
440:             revert ErrInvalidQuoteToken();

/// @audit Duplicated on line 574, 582
567:             revert ErrTooHighSlippage(amountOut);
```

- *LockingMultiRewards.sol* ( [157-157](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L157-L157), [302-302](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L302-L302) ):

```solidity
/// @audit Duplicated on line 172, 460
157:             revert ErrZeroAmount();

/// @audit Duplicated on line 363
302:             revert ErrInvalidTokenAddress();
```

</details>

### [N-85] Consider adding emergency-stop functionality

Adding a way to quickly halt protocol functionality in an emergency, rather than having to pause individual contracts one-by-one, will make in-progress hack mitigation faster and much less stressful.

<details>
<summary>There are 14 instances (click to show):</summary>

- *BlastBox.sol* ( [13-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L13-L13) ):

```solidity
13: contract BlastBox is DegenBox, OperatableV3 {
```

- *BlastGovernor.sol* ( [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L7-L7) ):

```solidity
7: contract BlastGovernor is OperatableV2 {
```

- *BlastMagicLP.sol* ( [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L10-L10) ):

```solidity
10: contract BlastMagicLP is MagicLP {
```

- *BlastOnboarding.sol* ( [12-12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L12-L12), [64-64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L64-L64) ):

```solidity
12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```

- *BlastOnboardingBoot.sol* ( [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L23-L23), [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L34-L34) ):

```solidity
23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```

- *BlastTokenRegistry.sol* ( [6-6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L6-L6) ):

```solidity
6: contract BlastTokenRegistry is Owned {
```

- *BlastWrappers.sol* ( [28-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L28-L28), [42-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L42-L42) ):

```solidity
28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {
```

- *MagicLP.sol* ( [25-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L25-L25) ):

```solidity
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```

- *FeeRateModel.sol* ( [13-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L13-L13) ):

```solidity
13: contract FeeRateModel is Owned {
```

- *Factory.sol* ( [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L11-L11) ):

```solidity
11: contract Factory is Owned {
```

- *LockingMultiRewards.sol* ( [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L14-L14) ):

```solidity
14: contract LockingMultiRewards is OperatableV2, Pausable {
```

</details>

### [N-86] Enable IR-based code generation

The IR-based code generator was introduced with an aim to not only allow code generation to be more transparent and auditable but also to enable more powerful optimization passes that span across functions.
You can enable it on the command line using `--via-ir` or with the option `{"viaIR": true}`.
This will take longer to compile, but you can just simple test it before deploying and if you got a better benchmark then you can add --via-ir to your deploy command
More on: https://docs.soliditylang.org/en/v0.8.17/ir-breaking-changes.html

There is 1 instance:

- Global finding

### [N-87] Missing checks for uint state variable assignments

Consider whether reasonable bounds checks for variables would be useful.

There are 3 instances:

- *MagicLP.sol* ( [561-561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L561-L561), [562-562](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L562-L562) ):

```solidity
561:         _BASE_RESERVE_ = baseReserve.toUint112();

562:         _QUOTE_RESERVE_ = quoteReserve.toUint112();
```

- *LockingMultiRewards.sol* ( [319-319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L319-L319) ):

```solidity
319:         minLockAmount = _minLockAmount;
```

### [N-88] Use the Modern Upgradeable Contract Paradigm

Modern smart contract development often employs upgradeable contract structures, utilizing proxy patterns like OpenZeppelin’s Upgradeable Contracts. This paradigm separates logic and state, allowing developers to amend and enhance the contract's functionality without altering its state or the deployed contract address. Transitioning to this approach enhances long-term maintainability.
Resolution: Adopt a well-established proxy pattern for upgradeability, ensuring proper initialization and employing transparent proxies to mitigate potential risks. Embrace comprehensive testing and audit practices, particularly when updating contract logic, to ensure state consistency and security are preserved across upgrades. This ensures your contract remains robust and adaptable to future requirements.

<details>
<summary>There are 17 instances (click to show):</summary>

- *BlastBox.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L13) ):

```solidity
13: contract BlastBox is DegenBox, OperatableV3 {
```

- *BlastDapp.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L6) ):

```solidity
6: contract BlastDapp {
```

- *BlastGovernor.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L7) ):

```solidity
7: contract BlastGovernor is OperatableV2 {
```

- *BlastMagicLP.sol* ( [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L10) ):

```solidity
10: contract BlastMagicLP is MagicLP {
```

- *BlastOnboarding.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L12), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L64) ):

```solidity
12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```

- *BlastOnboardingBoot.sol* ( [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L23), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L34) ):

```solidity
23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```

- *BlastTokenRegistry.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L6) ):

```solidity
6: contract BlastTokenRegistry is Owned {
```

- *BlastWrappers.sol* ( [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L19), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L42) ):

```solidity
19: contract BlastMIMSwapRouter is Router {

42: contract BlastCauldronV4 is CauldronV4 {
```

- *MagicLP.sol* ( [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L25) ):

```solidity
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```

- *FeeRateModel.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L13) ):

```solidity
13: contract FeeRateModel is Owned {
```

- *FeeRateModelImpl.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L7) ):

```solidity
7: contract FeeRateModelImpl {
```

- *Router.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L12) ):

```solidity
12: contract Router {
```

- *MagicLpAggregator.sol* ( [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L9) ):

```solidity
9: contract MagicLpAggregator is IAggregator {
```

- *LockingMultiRewards.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L14) ):

```solidity
14: contract LockingMultiRewards is OperatableV2, Pausable {
```

</details>

### [N-89] Contracts should have NatSpec `@dev` tags

The `@dev` tag is used to explain extra details to developers.

<details>
<summary>There are 23 instances (click to show):</summary>

- *BlastBox.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L13) ):

```solidity
13: contract BlastBox is DegenBox, OperatableV3 {
```

- *BlastDapp.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L6) ):

```solidity
6: contract BlastDapp {
```

- *BlastGovernor.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L7) ):

```solidity
7: contract BlastGovernor is OperatableV2 {
```

- *BlastMagicLP.sol* ( [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L10) ):

```solidity
10: contract BlastMagicLP is MagicLP {
```

- *BlastOnboarding.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L12), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L64) ):

```solidity
12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```

- *BlastOnboardingBoot.sol* ( [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L23) ):

```solidity
23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
```

- *BlastTokenRegistry.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L6) ):

```solidity
6: contract BlastTokenRegistry is Owned {
```

- *BlastWrappers.sol* ( [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L19), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L28), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L42) ):

```solidity
19: contract BlastMIMSwapRouter is Router {

28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {
```

- *BlastPoints.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L6) ):

```solidity
6: library BlastPoints {
```

- *BlastYields.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L7) ):

```solidity
7: library BlastYields {
```

- *MagicLP.sol* ( [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L25) ):

```solidity
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```

- *FeeRateModel.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L13) ):

```solidity
13: contract FeeRateModel is Owned {
```

- *FeeRateModelImpl.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L7) ):

```solidity
7: contract FeeRateModelImpl {
```

- *DecimalMath.sol* ( [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L17) ):

```solidity
17: library DecimalMath {
```

- *Math.sol* ( [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L16) ):

```solidity
16: library Math {
```

- *PMMPricing.sol* ( [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L20) ):

```solidity
20: library PMMPricing {
```

- *Factory.sol* ( [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L11) ):

```solidity
11: contract Factory is Owned {
```

- *Router.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L12) ):

```solidity
12: contract Router {
```

- *MagicLpAggregator.sol* ( [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L9) ):

```solidity
9: contract MagicLpAggregator is IAggregator {
```

- *LockingMultiRewards.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L14) ):

```solidity
14: contract LockingMultiRewards is OperatableV2, Pausable {
```

</details>

### [N-90] Error declarations should have NatSpec descriptions

Error declarations should have NatSpec descriptions

<details>
<summary>There are 78 instances (click to show):</summary>

- *BlastBox.sol* ( [17-17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L17-L17), [18-18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L18-L18) ):

```solidity
17:     error ErrZeroAddress();

18:     error ErrUnsupportedToken();
```

- *BlastGovernor.sol* ( [9-9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L9-L9) ):

```solidity
9:     error ErrZeroAddress();
```

- *BlastMagicLP.sol* ( [15-15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L15-L15) ):

```solidity
15:     error ErrNotAllowedImplementationOperator();
```

- *BlastOnboarding.sol* ( [13-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L13-L13), [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L14-L14), [15-15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L15-L15), [16-16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L16-L16), [77-77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L77-L77), [78-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L78-L78) ):

```solidity
13:     error ErrZeroAddress();

14:     error ErrWrongState();

15:     error ErrUnsupportedToken();

16:     error ErrNotAllowed();

77:     error ErrUnsupported();

78:     error ErrCapReached();
```

- *BlastOnboardingBoot.sol* ( [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L43-L43), [44-44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L44-L44), [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L45-L45), [46-46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L46-L46), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L47-L47), [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L48-L48), [49-49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L49-L49) ):

```solidity
43:     error ErrInsufficientAmountOut();

44:     error ErrNotReady();

45:     error ErrAlreadyClaimed();

46:     error ErrWrongFeeRateModel();

47:     error ErrAlreadyBootstrapped();

48:     error ErrNothingToClaim();

49:     error ErrCannotChangeOnceReady();
```

- *BlastTokenRegistry.sol* ( [8-8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L8-L8) ):

```solidity
8:     error ErrZeroAddress();
```

- *BlastWrappers.sol* ( [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L43-L43) ):

```solidity
43:     error ErrInvalidGovernorAddress();
```

- *MagicLP.sol* ( [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L38-L38), [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L39-L39), [40-40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L40-L40), [41-41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L41-L41), [42-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L42-L42), [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L43-L43), [44-44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L44-L44), [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L45-L45), [46-46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L46-L46), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L47-L47), [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L48-L48), [49-49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L49-L49), [50-50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L50-L50), [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L51-L51), [52-52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L52-L52), [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L53-L53), [54-54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L54-L54), [55-55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L55-L55), [56-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L56-L56), [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L57-L57), [58-58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L58-L58), [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L59-L59) ):

```solidity
38:     error ErrInitialized();

39:     error ErrBaseQuoteSame();

40:     error ErrInvalidI();

41:     error ErrInvalidK();

42:     error ErrExpired();

43:     error ErrInvalidSignature();

44:     error ErrFlashLoanFailed();

45:     error ErrNoBaseInput();

46:     error ErrZeroAddress();

47:     error ErrZeroQuoteAmount();

48:     error ErrZeroQuoteTarget();

49:     error ErrMintAmountNotEnough();

50:     error ErrNotEnough();

51:     error ErrWithdrawNotEnough();

52:     error ErrSellBackNotAllowed();

53:     error ErrInvalidLPFeeRate();

54:     error ErrNotImplementationOwner();

55:     error ErrNotImplementation();

56:     error ErrNotClone();

57:     error ErrNotAllowed();

58:     error ErrReserveAmountNotEnough();

59:     error ErrOverflow();
```

- *FeeRateModel.sol* ( [17-17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L17-L17) ):

```solidity
17:     error ErrZeroAddress();
```

- *Math.sol* ( [17-17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L17-L17) ):

```solidity
17:     error ErrIsZero();
```

- *Factory.sol* ( [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L29-L29), [30-30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L30-L30) ):

```solidity
29:     error ErrInvalidUserPoolIndex();

30:     error ErrZeroAddress();
```

- *Router.sol* ( [16-16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L16-L16), [17-17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L17-L17), [18-18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L18-L18), [19-19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L19-L19), [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L20-L20), [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L21-L21), [22-22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L22-L22), [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L23-L23), [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L24-L24), [25-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L25-L25), [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L26-L26), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L27-L27), [28-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L28-L28), [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L29-L29) ):

```solidity
16:     error ErrNotETHLP();

17:     error ErrExpired();

18:     error ErrZeroAddress();

19:     error ErrPathTooLong();

20:     error ErrEmptyPath();

21:     error ErrBadPath();

22:     error ErrTooHighSlippage(uint256 amountOut);

23:     error ErrInvalidBaseToken();

24:     error ErrInvalidQuoteToken();

25:     error ErrInTokenNotETH();

26:     error ErrOutTokenNotETH();

27:     error ErrInvalidQuoteTarget();

28:     error ErrZeroDecimals();

29:     error ErrDecimalsDifferenceTooLarge();
```

- *LockingMultiRewards.sol* ( [30-30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L30-L30), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L31-L31), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L32-L32), [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L33-L33), [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L34-L34), [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L35-L35), [36-36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L36-L36), [37-37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L37-L37), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L38-L38), [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L39-L39), [40-40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L40-L40), [41-41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L41-L41), [42-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L42-L42), [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L43-L43), [44-44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L44-L44), [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L45-L45), [46-46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L46-L46), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L47-L47), [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L48-L48) ):

```solidity
30:     error ErrZeroAmount();

31:     error ErrRewardAlreadyExists();

32:     error ErrInvalidTokenAddress();

33:     error ErrMaxUserLocksExceeded();

34:     error ErrNotExpired();

35:     error ErrInvalidUser();

36:     error ErrLockAmountTooSmall();

37:     error ErrLengthMismatch();

38:     error ErrNoLocks();

39:     error ErrLockNotExpired();

40:     error ErrMaxRewardsExceeded();

41:     error ErrSkimmingTooMuch();

42:     error ErrInvalidLockIndex();

43:     error ErrNotEnoughReward();

44:     error ErrInvalidDurationRatio();

45:     error ErrInvalidBoostMultiplier();

46:     error ErrInvalidLockDuration();

47:     error ErrInvalidRewardDuration();

48:     error ErrInsufficientRemainingTime();
```

</details>

### [N-91] Missing NatSpec `@dev` from event declaration

Some events have an incomplete NatSpec: add a `@dev` notation to describe the event to improve the code documentation.

<details>
<summary>There are 53 instances (click to show):</summary>

- *BlastBox.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L14), [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L15) ):

```solidity
14:     event LogTokenDepositEnabled(address indexed token, bool enabled);

15:     event LogFeeToChanged(address indexed feeTo);
```

- *BlastGovernor.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L8) ):

```solidity
8:     event LogFeeToChanged(address indexed feeTo);
```

- *BlastMagicLP.sol* ( [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L11), [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L12), [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L13) ):

```solidity
11:     event LogFeeToChanged(address indexed feeTo);

12:     event LogOperatorChanged(address indexed, bool);

13:     event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);
```

- *BlastOnboarding.sol* ( [67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L67), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L68), [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L69), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L70), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L71), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L74), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L75) ):

```solidity
67:     event LogBootstrapperChanged(address indexed bootstrapper);

68:     event LogTokenSupported(address indexed token, bool supported);

69:     event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);

70:     event LogLock(address indexed user, address indexed token, uint256 amount);

71:     event LogFeeToChanged(address indexed feeTo);

72:     event LogWithdraw(address indexed user, address indexed token, uint256 amount);

73:     event LogTokenCapChanged(address indexed token, uint256 cap);

74:     event LogStateChange(State state);

75:     event LogTokenRescue(address indexed token, address indexed to, uint256 amount);
```

- *BlastOnboardingBoot.sol* ( [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L37), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L38), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L39), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L40), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L41) ):

```solidity
37:     event LogReadyChanged(bool ready);

38:     event LogClaimed(address indexed user, uint256 shares, bool lock);

39:     event LogInitialized(Router indexed router);

40:     event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);

41:     event LogStakingChanged(address indexed staking);
```

- *BlastTokenRegistry.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L7) ):

```solidity
7:     event LogNativeYieldTokenEnabled(address indexed token, bool enabled);
```

- *BlastYields.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L8), [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L9), [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L10), [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L11), [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L12) ):

```solidity
8:     event LogBlastGasClaimed(address indexed recipient, uint256 amount);

9:     event LogBlastETHClaimed(address indexed recipient, uint256 amount);

10:     event LogBlastTokenClaimed(address indexed recipient, address indexed token, uint256 amount);

11:     event LogBlastTokenClaimableEnabled(address indexed contractAddress, address indexed token);

12:     event LogBlastNativeClaimableEnabled(address indexed contractAddress);
```

- *MagicLP.sol* ( [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L30), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L31), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L33), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L34), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L35), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L36) ):

```solidity
30:     event BuyShares(address to, uint256 increaseShares, uint256 totalShares);

31:     event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);

32:     event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);

33:     event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);

34:     event RChange(PMMPricing.RState newRState);

35:     event TokenRescue(address indexed token, address to, uint256 amount);

36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);
```

- *FeeRateModel.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L14), [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L15) ):

```solidity
14:     event LogImplementationChanged(address indexed implementation);

15:     event LogMaintainerChanged(address indexed maintainer);
```

- *Factory.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L12), [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L23), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L24), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L26), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L27) ):

```solidity
12:     event LogCreated(

23:     event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);

24:     event LogPoolRemoved(address pool);

25:     event LogSetImplementation(address indexed implementation);

26:     event LogSetMaintainer(address indexed newMaintainer);

27:     event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);
```

- *LockingMultiRewards.sol* ( [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L17), [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L18), [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L19), [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L21), [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L22), [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L23), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L24), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L26), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L27), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L28) ):

```solidity
17:     event LogRewardAdded(uint256 reward);

18:     event LogStaked(address indexed user, uint256 amount);

19:     event LogLocked(address indexed user, uint256 amount, uint256 unlockTime, uint256 lockCount);

20:     event LogUnlocked(address indexed user, uint256 amount, uint256 index);

21:     event LogLockIndexChanged(address indexed user, uint256 fromIndex, uint256 toIndex);

22:     event LogWithdrawn(address indexed user, uint256 amount);

23:     event LogRewardLockCreated(address indexed user, uint256 unlockTime);

24:     event LogRewardLocked(address indexed user, address indexed rewardsToken, uint256 reward);

25:     event LogRewardPaid(address indexed user, address indexed rewardsToken, uint256 reward);

26:     event LogRewardsDurationUpdated(address token, uint256 newDuration);

27:     event LogRecovered(address token, uint256 amount);

28:     event LogSetMinLockAmount(uint256 previous, uint256 current);
```

</details>

### [N-92] Missing NatSpec `@notice` from event declaration

Some events have an incomplete NatSpec: add a @notice notation to describe the event to improve the code documentation.

<details>
<summary>There are 53 instances (click to show):</summary>

- *BlastBox.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L14), [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L15) ):

```solidity
14:     event LogTokenDepositEnabled(address indexed token, bool enabled);

15:     event LogFeeToChanged(address indexed feeTo);
```

- *BlastGovernor.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L8) ):

```solidity
8:     event LogFeeToChanged(address indexed feeTo);
```

- *BlastMagicLP.sol* ( [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L11), [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L12), [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L13) ):

```solidity
11:     event LogFeeToChanged(address indexed feeTo);

12:     event LogOperatorChanged(address indexed, bool);

13:     event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);
```

- *BlastOnboarding.sol* ( [67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L67), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L68), [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L69), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L70), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L71), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L74), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L75) ):

```solidity
67:     event LogBootstrapperChanged(address indexed bootstrapper);

68:     event LogTokenSupported(address indexed token, bool supported);

69:     event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);

70:     event LogLock(address indexed user, address indexed token, uint256 amount);

71:     event LogFeeToChanged(address indexed feeTo);

72:     event LogWithdraw(address indexed user, address indexed token, uint256 amount);

73:     event LogTokenCapChanged(address indexed token, uint256 cap);

74:     event LogStateChange(State state);

75:     event LogTokenRescue(address indexed token, address indexed to, uint256 amount);
```

- *BlastOnboardingBoot.sol* ( [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L37), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L38), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L39), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L40), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L41) ):

```solidity
37:     event LogReadyChanged(bool ready);

38:     event LogClaimed(address indexed user, uint256 shares, bool lock);

39:     event LogInitialized(Router indexed router);

40:     event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);

41:     event LogStakingChanged(address indexed staking);
```

- *BlastTokenRegistry.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L7) ):

```solidity
7:     event LogNativeYieldTokenEnabled(address indexed token, bool enabled);
```

- *BlastYields.sol* ( [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L8), [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L9), [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L10), [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L11), [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L12) ):

```solidity
8:     event LogBlastGasClaimed(address indexed recipient, uint256 amount);

9:     event LogBlastETHClaimed(address indexed recipient, uint256 amount);

10:     event LogBlastTokenClaimed(address indexed recipient, address indexed token, uint256 amount);

11:     event LogBlastTokenClaimableEnabled(address indexed contractAddress, address indexed token);

12:     event LogBlastNativeClaimableEnabled(address indexed contractAddress);
```

- *MagicLP.sol* ( [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L30), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L31), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L33), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L34), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L35), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L36) ):

```solidity
30:     event BuyShares(address to, uint256 increaseShares, uint256 totalShares);

31:     event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);

32:     event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);

33:     event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);

34:     event RChange(PMMPricing.RState newRState);

35:     event TokenRescue(address indexed token, address to, uint256 amount);

36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);
```

- *FeeRateModel.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L14), [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L15) ):

```solidity
14:     event LogImplementationChanged(address indexed implementation);

15:     event LogMaintainerChanged(address indexed maintainer);
```

- *Factory.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L12), [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L23), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L24), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L26), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L27) ):

```solidity
12:     event LogCreated(

23:     event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);

24:     event LogPoolRemoved(address pool);

25:     event LogSetImplementation(address indexed implementation);

26:     event LogSetMaintainer(address indexed newMaintainer);

27:     event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);
```

- *LockingMultiRewards.sol* ( [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L17), [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L18), [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L19), [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L21), [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L22), [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L23), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L24), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L26), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L27), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L28) ):

```solidity
17:     event LogRewardAdded(uint256 reward);

18:     event LogStaked(address indexed user, uint256 amount);

19:     event LogLocked(address indexed user, uint256 amount, uint256 unlockTime, uint256 lockCount);

20:     event LogUnlocked(address indexed user, uint256 amount, uint256 index);

21:     event LogLockIndexChanged(address indexed user, uint256 fromIndex, uint256 toIndex);

22:     event LogWithdrawn(address indexed user, uint256 amount);

23:     event LogRewardLockCreated(address indexed user, uint256 unlockTime);

24:     event LogRewardLocked(address indexed user, address indexed rewardsToken, uint256 reward);

25:     event LogRewardPaid(address indexed user, address indexed rewardsToken, uint256 reward);

26:     event LogRewardsDurationUpdated(address token, uint256 newDuration);

27:     event LogRecovered(address token, uint256 amount);

28:     event LogSetMinLockAmount(uint256 previous, uint256 current);
```

</details>

### [N-93] Missing NatSpec `@dev` from constructor

<details>
<summary>There are 15 instances (click to show):</summary>

- *BlastBox.sol* ( [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L24) ):

```solidity
24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
```

- *BlastDapp.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L7) ):

```solidity
7:     constructor() {
```

- *BlastGovernor.sol* ( [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L15) ):

```solidity
15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```

- *BlastMagicLP.sol* ( [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L23) ):

```solidity
23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
```

- *BlastOnboarding.sol* ( [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L58), [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L84) ):

```solidity
58:     constructor() Owned(msg.sender) {

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {
```

- *BlastTokenRegistry.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L12) ):

```solidity
12:     constructor(address _owner) Owned(_owner) {}
```

- *BlastWrappers.sol* ( [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L20), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L29), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L47) ):

```solidity
20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

29:     constructor(

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
```

- *MagicLP.sol* ( [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L84) ):

```solidity
84:     constructor(address owner_) Owned(owner_) {
```

- *FeeRateModel.sol* ( [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L22) ):

```solidity
22:     constructor(address maintainer_, address owner_) Owned(owner_) {
```

- *Factory.sol* ( [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L38) ):

```solidity
38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
```

- *Router.sol* ( [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L38) ):

```solidity
38:     constructor(IWETH weth_, IFactory factory_) {
```

- *MagicLpAggregator.sol* ( [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L21) ):

```solidity
21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```

</details>

### [N-94] Missing NatSpec `@notice` from constructor

<details>
<summary>There are 16 instances (click to show):</summary>

- *BlastBox.sol* ( [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L24) ):

```solidity
24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
```

- *BlastDapp.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L7) ):

```solidity
7:     constructor() {
```

- *BlastGovernor.sol* ( [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L15) ):

```solidity
15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```

- *BlastMagicLP.sol* ( [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L23) ):

```solidity
23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
```

- *BlastOnboarding.sol* ( [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L58), [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L84) ):

```solidity
58:     constructor() Owned(msg.sender) {

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {
```

- *BlastTokenRegistry.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L12) ):

```solidity
12:     constructor(address _owner) Owned(_owner) {}
```

- *BlastWrappers.sol* ( [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L20), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L29), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L47) ):

```solidity
20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

29:     constructor(

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
```

- *MagicLP.sol* ( [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L84) ):

```solidity
84:     constructor(address owner_) Owned(owner_) {
```

- *FeeRateModel.sol* ( [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L22) ):

```solidity
22:     constructor(address maintainer_, address owner_) Owned(owner_) {
```

- *Factory.sol* ( [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L38) ):

```solidity
38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
```

- *Router.sol* ( [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L38) ):

```solidity
38:     constructor(IWETH weth_, IFactory factory_) {
```

- *MagicLpAggregator.sol* ( [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L21) ):

```solidity
21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```

- *LockingMultiRewards.sol* ( [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L112) ):

```solidity
112:     constructor(
```

</details>

### [N-95] Missing NatSpec `@dev` from receive function declaration

There are 3 instances:

- *BlastGovernor.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L13) ):

```solidity
13:     receive() external payable {}
```

- *BlastOnboarding.sol* ( [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L80) ):

```solidity
80:     receive() external payable override {
```

- *Router.sol* ( [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L36) ):

```solidity
36:     receive() external payable {}
```

### [N-96] Missing NatSpec `@notice` from receive function declaration

There are 3 instances:

- *BlastGovernor.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L13) ):

```solidity
13:     receive() external payable {}
```

- *BlastOnboarding.sol* ( [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L80) ):

```solidity
80:     receive() external payable override {
```

- *Router.sol* ( [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L36) ):

```solidity
36:     receive() external payable {}
```

### [N-97] Missing NatSpec `@dev` from function declaration

Some functions have an incomplete NatSpec: add a `@dev` notation to describe the function to improve the code documentation.

<details>
<summary>There are 194 instances (click to show):</summary>

- *BlastBox.sol* ( [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L36), [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L52), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L56), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L68), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L72), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L81), [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L103) ):

```solidity
36:     function _onBeforeDeposit(

52:     function claimGasYields() external onlyOperators returns (uint256) {

56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

68:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

72:     function setFeeTo(address feeTo_) external onlyOwner {

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {

103:     function isOwner(address _account) internal view override returns (bool) {
```

- *BlastGovernor.sol* ( [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L28), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L32), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L40), [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L49), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L53) ):

```solidity
28:     function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

40:     function setFeeTo(address _feeTo) external onlyOwner {

49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

- *BlastMagicLP.sol* ( [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L39), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L47), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L53), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L64), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L72), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L80), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L89), [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L98), [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L104) ):

```solidity
39:     function version() external pure override returns (string memory) {

47:     function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {

53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

72:     function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {

80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {

98:     function _afterInitialized() internal override {

104:     function _updateTokenClaimables() internal {
```

- *BlastOnboarding.sol* ( [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L101), [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L123), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L132), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L147), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L156), [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L160), [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L164), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L175), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L185), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L190), [195](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L195), [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L200), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L205), [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L214), [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L218), [226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L226) ):

```solidity
101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {

147:     function setFeeTo(address feeTo_) external onlyOwner {

156:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

160:     function claimGasYields() external onlyOwner returns (uint256) {

164:     function claimTokenYields(address[] memory tokens) external onlyOwner {

175:     function setTokenSupported(address token, bool supported) external onlyOwner {

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {

195:     function open() external onlyOwner onlyState(State.Idle) {

200:     function close() external onlyOwner onlyState(State.Opened) {

205:     function rescue(address token, address to, uint256 amount) external onlyOwner {

214:     function pause() external onlyOwner {

218:     function unpause() external onlyOwner {

226:     function _implementation() internal view override returns (address) {
```

- *BlastOnboardingBoot.sol* ( [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L55), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L78), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L86), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L96), [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L129), [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L137), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L146), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L155) ):

```solidity
55:     function claim(bool lock) external returns (uint256 shares) {

78:     function claimable(address user) external view returns (uint256 shares) {

86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {

129:     function initialize(Router _router) external onlyOwner {

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {

155:     function _claimable(address user) internal view returns (uint256 shares) {
```

- *BlastTokenRegistry.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L14) ):

```solidity
14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```

- *BlastWrappers.sol* ( [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L59), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L70) ):

```solidity
59:     function init(bytes calldata data) public payable override {

70:     function _setupBlacklist() private {
```

- *BlastPoints.sol* ( [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L10) ):

```solidity
10:     function configure() internal {
```

- *BlastYields.sol* ( [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L20), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L29), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L38), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L42), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L51), [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L55), [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L60), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L70), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L75), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L86) ):

```solidity
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

- *MagicLP.sol* ( [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L91), [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L134), [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L138), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L155), [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L159), [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L163), [167](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L167), [180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L180), [193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L193), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204), [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L215), [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L219), [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L224), [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L228), [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L232), [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L236), [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L244), [267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L267), [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L290), [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L360), [413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L413), [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L461), [470](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L470), [504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L504), [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L528), [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L545), [560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L560), [567](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L567), [581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L581), [587](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L587), [593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L593), [601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L601) ):

```solidity
91:     function init(

134:     function sync() external nonReentrant {

138:     function correctRState() external {

155:     function name() public view override returns (string memory) {

159:     function symbol() public pure override returns (string memory) {

163:     function decimals() public view override returns (uint8) {

167:     function querySellBase(

180:     function querySellQuote(

193:     function getPMMState() public view returns (PMMPricing.PMMState memory state) {

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

215:     function getMidPrice() public view returns (uint256 midPrice) {

219:     function getReserves() external view returns (uint256 baseReserve, uint256 quoteReserve) {

224:     function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {

228:     function getBaseInput() public view returns (uint256 input) {

232:     function getQuoteInput() public view returns (uint256 input) {

236:     function version() external pure virtual returns (string memory) {

244:     function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {

267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {

413:     function sellShares(

461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {

470:     function setParameters(

504:     function ratioSync() external nonReentrant onlyImplementationOwner {

528:     function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {

545:     function _twapUpdate() internal {

560:     function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {

567:     function _sync() internal {

581:     function _transferBaseOut(address to, uint256 amount) internal {

587:     function _transferQuoteOut(address to, uint256 amount) internal {

593:     function _mint(address to, uint256 amount) internal override {

601:     function _afterInitialized() internal virtual {}
```

- *FeeRateModel.sol* ( [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L34), [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L46), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L57) ):

```solidity
34:     function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {

46:     function setMaintainer(address maintainer_) external onlyOwner {

57:     function setImplementation(address implementation_) public onlyOwner {
```

- *FeeRateModelImpl.sol* ( [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9) ):

```solidity
9:     function getFeeRate(
```

- *DecimalMath.sol* ( [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L23), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L27), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L31), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L35), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L39), [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L43), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L47) ):

```solidity
23:     function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {

27:     function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {

31:     function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {

35:     function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {

39:     function reciprocalFloor(uint256 target) internal pure returns (uint256) {

43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {

47:     function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```

- *Math.sol* ( [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L19), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L29), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L79), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131) ):

```solidity
19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

29:     function sqrt(uint256 x) internal pure returns (uint256 y) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```

- *PMMPricing.sol* ( [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L39), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L76), [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L104), [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L119), [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L134), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L147), [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L162), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L175), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L190), [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L203) ):

```solidity
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

- *Factory.sol* ( [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L53), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L57), [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L65), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L96), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L105), [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L116), [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L120), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L148), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L155) ):

```solidity
53:     function getPoolCount(address token0, address token1) external view returns (uint256) {

57:     function getUserPoolCount(address creator) external view returns (uint256) {

65:     function predictDeterministicAddress(

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

96:     function setLpImplementation(address implementation_) external onlyOwner {

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

116:     function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {

120:     function removePool(

148:     function _addPool(address creator, address baseToken, address quoteToken, address pool) internal {

155:     function _computeSalt(
```

- *Router.sol* ( [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L54), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L73), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L96), [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L112), [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L162), [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L178), [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L192), [229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L229), [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L251), [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L261), [274](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L274), [314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L314), [336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L336), [365](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L365), [404](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L404), [415](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L415), [432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L432), [449](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L449), [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L461), [478](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L478), [499](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L499), [509](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L509), [541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L541), [571](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L571), [578](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L578), [586](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L586), [598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L598) ):

```solidity
54:     function createPool(

73:     function createPoolETH(

96:     function previewCreatePool(

112:     function previewAddLiquidity(

162:     function addLiquidity(

178:     function addLiquidityUnsafe(

192:     function addLiquidityETH(

229:     function addLiquidityETHUnsafe(

251:     function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

261:     function removeLiquidity(

274:     function removeLiquidityETH(

314:     function swapTokensForTokens(

336:     function swapETHForTokens(

365:     function swapTokensForETH(

404:     function sellBaseTokensForTokens(

415:     function sellBaseETHForTokens(

432:     function sellBaseTokensForETH(

449:     function sellQuoteTokensForTokens(

461:     function sellQuoteETHForTokens(

478:     function sellQuoteTokensForETH(

499:     function _addLiquidity(address lp, address to, uint256 minimumShares) internal returns (uint256 shares) {

509:     function _adjustAddLiquidity(

541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

586:     function _validatePath(address[] calldata path) internal pure {

598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {
```

- *MagicLpAggregator.sol* ( [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L29), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L33), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L37), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L48) ):

```solidity
29:     function decimals() external pure override returns (uint8) {

33:     function _getReserves() internal view virtual returns (uint256, uint256) {

37:     function latestAnswer() public view override returns (int256) {

48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```

- *LockingMultiRewards.sol* ( [150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L150), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L155), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L170), [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L186), [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L191), [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L199), [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L203), [207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L207), [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L211), [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L215), [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L219), [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L223), [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L227), [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L231), [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L235), [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L239), [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L257), [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L261), [265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L265), [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L269), [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L273), [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L277), [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L288), [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L292), [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L300), [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L317), [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L324), [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L337), [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L341), [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L349), [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L361), [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L397), [458](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L458), [479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L479), [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L536), [597](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L597) ):

```solidity
150:     function stake(uint256 amount, bool lock_) public whenNotPaused {

155:     function lock(uint256 amount) public whenNotPaused {

170:     function withdraw(uint256 amount) public virtual {

186:     function withdrawWithRewards(uint256 amount) public virtual {

191:     function getRewards() public virtual {

199:     function rewardData(address token) external view returns (Reward memory) {

203:     function rewardsForDuration(address rewardToken) external view returns (uint256) {

207:     function rewardTokensLength() external view returns (uint256) {

211:     function balances(address user) external view returns (Balances memory) {

215:     function userRewardLock(address user) external view returns (RewardLock memory) {

219:     function userLocks(address user) external view returns (LockedBalance[] memory) {

223:     function userLocksLength(address user) external view returns (uint256) {

227:     function locked(address user) external view returns (uint256) {

231:     function unlocked(address user) external view returns (uint256) {

235:     function totalSupply() public view returns (uint256) {

239:     function balanceOf(address user) public view returns (uint256) {

257:     function epoch() public view returns (uint256) {

261:     function nextEpoch() public view returns (uint256) {

265:     function remainingEpochTime() public view returns (uint256) {

269:     function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {

273:     function rewardPerToken(address rewardToken) public view returns (uint256) {

277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

288:     function earned(address user, address rewardToken) public view returns (uint256) {

292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

300:     function addReward(address rewardToken) public onlyOwner {

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

324:     function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {

337:     function pause() external onlyOwner {

341:     function unpause() external onlyOwner {

349:     function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {

361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {

397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {

458:     function _stakeFor(address account, uint256 amount, bool lock_) internal {

479:     function _createLock(address user, uint256 amount) internal {

536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

597:     function _getRewards(address user) internal {
```

</details>

### [N-98] Missing NatSpec `@notice` from function declaration

Some functions have an incomplete NatSpec: add a `@notice` notation to describe the function to improve the code documentation.

<details>
<summary>There are 191 instances (click to show):</summary>

- *BlastBox.sol* ( [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L36), [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L52), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L56), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L68), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L72), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L81), [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L98), [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L103) ):

```solidity
36:     function _onBeforeDeposit(

52:     function claimGasYields() external onlyOperators returns (uint256) {

56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

68:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

72:     function setFeeTo(address feeTo_) external onlyOwner {

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {

98:     function _configure() internal override {

103:     function isOwner(address _account) internal view override returns (bool) {
```

- *BlastGovernor.sol* ( [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L28), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L32), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L40), [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L49), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L53) ):

```solidity
28:     function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

40:     function setFeeTo(address _feeTo) external onlyOwner {

49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

- *BlastMagicLP.sol* ( [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L39), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L47), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L53), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L64), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L72), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L80), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L89), [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L98), [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L104) ):

```solidity
39:     function version() external pure override returns (string memory) {

47:     function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {

53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

72:     function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {

80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {

98:     function _afterInitialized() internal override {

104:     function _updateTokenClaimables() internal {
```

- *BlastOnboarding.sol* ( [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L101), [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L123), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L132), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L147), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L156), [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L160), [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L164), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L175), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L185), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L190), [195](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L195), [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L200), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L205), [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L214), [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L218), [226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L226) ):

```solidity
101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {

147:     function setFeeTo(address feeTo_) external onlyOwner {

156:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

160:     function claimGasYields() external onlyOwner returns (uint256) {

164:     function claimTokenYields(address[] memory tokens) external onlyOwner {

175:     function setTokenSupported(address token, bool supported) external onlyOwner {

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {

195:     function open() external onlyOwner onlyState(State.Idle) {

200:     function close() external onlyOwner onlyState(State.Opened) {

205:     function rescue(address token, address to, uint256 amount) external onlyOwner {

214:     function pause() external onlyOwner {

218:     function unpause() external onlyOwner {

226:     function _implementation() internal view override returns (address) {
```

- *BlastOnboardingBoot.sol* ( [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L55), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L78), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L86), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L96), [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L129), [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L137), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L146), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L155) ):

```solidity
55:     function claim(bool lock) external returns (uint256 shares) {

78:     function claimable(address user) external view returns (uint256 shares) {

86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {

129:     function initialize(Router _router) external onlyOwner {

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {

155:     function _claimable(address user) internal view returns (uint256 shares) {
```

- *BlastTokenRegistry.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L14) ):

```solidity
14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```

- *BlastWrappers.sol* ( [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L59), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L70) ):

```solidity
59:     function init(bytes calldata data) public payable override {

70:     function _setupBlacklist() private {
```

- *BlastPoints.sol* ( [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L10) ):

```solidity
10:     function configure() internal {
```

- *BlastYields.sol* ( [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L20), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L29), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L38), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L42), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L51), [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L55), [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L60), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L70), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L75), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L86) ):

```solidity
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

- *MagicLP.sol* ( [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L91), [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L134), [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L138), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L155), [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L159), [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L163), [167](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L167), [180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L180), [193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L193), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L204), [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L215), [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L219), [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L224), [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L228), [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L232), [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L236), [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L244), [267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L267), [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L290), [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L360), [413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L413), [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L461), [470](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L470), [504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L504), [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L528), [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L545), [560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L560), [567](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L567), [581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L581), [587](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L587), [593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L593), [601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L601) ):

```solidity
91:     function init(

134:     function sync() external nonReentrant {

138:     function correctRState() external {

155:     function name() public view override returns (string memory) {

159:     function symbol() public pure override returns (string memory) {

163:     function decimals() public view override returns (uint8) {

167:     function querySellBase(

180:     function querySellQuote(

193:     function getPMMState() public view returns (PMMPricing.PMMState memory state) {

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

215:     function getMidPrice() public view returns (uint256 midPrice) {

219:     function getReserves() external view returns (uint256 baseReserve, uint256 quoteReserve) {

224:     function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {

228:     function getBaseInput() public view returns (uint256 input) {

232:     function getQuoteInput() public view returns (uint256 input) {

236:     function version() external pure virtual returns (string memory) {

244:     function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {

267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {

413:     function sellShares(

461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {

470:     function setParameters(

504:     function ratioSync() external nonReentrant onlyImplementationOwner {

528:     function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {

545:     function _twapUpdate() internal {

560:     function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {

567:     function _sync() internal {

581:     function _transferBaseOut(address to, uint256 amount) internal {

587:     function _transferQuoteOut(address to, uint256 amount) internal {

593:     function _mint(address to, uint256 amount) internal override {

601:     function _afterInitialized() internal virtual {}
```

- *FeeRateModel.sol* ( [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L34), [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L46) ):

```solidity
34:     function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {

46:     function setMaintainer(address maintainer_) external onlyOwner {
```

- *FeeRateModelImpl.sol* ( [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9) ):

```solidity
9:     function getFeeRate(
```

- *DecimalMath.sol* ( [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L23), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L27), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L31), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L35), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L39), [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L43), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L47) ):

```solidity
23:     function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {

27:     function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {

31:     function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {

35:     function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {

39:     function reciprocalFloor(uint256 target) internal pure returns (uint256) {

43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {

47:     function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```

- *Math.sol* ( [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L19), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L29), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L51), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L79), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131) ):

```solidity
19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

29:     function sqrt(uint256 x) internal pure returns (uint256 y) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```

- *PMMPricing.sol* ( [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L39), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L76), [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L104), [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L119), [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L134), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L147), [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L162), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L175), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L190), [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L203) ):

```solidity
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

- *Factory.sol* ( [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L53), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L57), [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L65), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L96), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L105), [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L120), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L148), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L155) ):

```solidity
53:     function getPoolCount(address token0, address token1) external view returns (uint256) {

57:     function getUserPoolCount(address creator) external view returns (uint256) {

65:     function predictDeterministicAddress(

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

96:     function setLpImplementation(address implementation_) external onlyOwner {

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

120:     function removePool(

148:     function _addPool(address creator, address baseToken, address quoteToken, address pool) internal {

155:     function _computeSalt(
```

- *Router.sol* ( [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L54), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L73), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L96), [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L112), [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L162), [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L178), [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L192), [229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L229), [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L251), [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L261), [274](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L274), [314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L314), [336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L336), [365](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L365), [404](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L404), [415](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L415), [432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L432), [449](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L449), [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L461), [478](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L478), [499](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L499), [509](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L509), [541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L541), [571](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L571), [578](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L578), [586](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L586), [598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L598) ):

```solidity
54:     function createPool(

73:     function createPoolETH(

96:     function previewCreatePool(

112:     function previewAddLiquidity(

162:     function addLiquidity(

178:     function addLiquidityUnsafe(

192:     function addLiquidityETH(

229:     function addLiquidityETHUnsafe(

251:     function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

261:     function removeLiquidity(

274:     function removeLiquidityETH(

314:     function swapTokensForTokens(

336:     function swapETHForTokens(

365:     function swapTokensForETH(

404:     function sellBaseTokensForTokens(

415:     function sellBaseETHForTokens(

432:     function sellBaseTokensForETH(

449:     function sellQuoteTokensForTokens(

461:     function sellQuoteETHForTokens(

478:     function sellQuoteTokensForETH(

499:     function _addLiquidity(address lp, address to, uint256 minimumShares) internal returns (uint256 shares) {

509:     function _adjustAddLiquidity(

541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

586:     function _validatePath(address[] calldata path) internal pure {

598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {
```

- *MagicLpAggregator.sol* ( [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L29), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L33), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L37), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L48) ):

```solidity
29:     function decimals() external pure override returns (uint8) {

33:     function _getReserves() internal view virtual returns (uint256, uint256) {

37:     function latestAnswer() public view override returns (int256) {

48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```

- *LockingMultiRewards.sol* ( [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L186), [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L191), [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L199), [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L203), [207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L207), [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L211), [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L215), [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L219), [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L223), [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L227), [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L231), [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L235), [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L239), [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L253), [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L257), [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L261), [265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L265), [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L269), [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L273), [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L277), [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L288), [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L292), [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L300), [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L317), [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L337), [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L341), [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L349), [458](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L458), [479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L479), [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L528), [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L536), [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L544), [557](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L557), [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L572) ):

```solidity
186:     function withdrawWithRewards(uint256 amount) public virtual {

191:     function getRewards() public virtual {

199:     function rewardData(address token) external view returns (Reward memory) {

203:     function rewardsForDuration(address rewardToken) external view returns (uint256) {

207:     function rewardTokensLength() external view returns (uint256) {

211:     function balances(address user) external view returns (Balances memory) {

215:     function userRewardLock(address user) external view returns (RewardLock memory) {

219:     function userLocks(address user) external view returns (LockedBalance[] memory) {

223:     function userLocksLength(address user) external view returns (uint256) {

227:     function locked(address user) external view returns (uint256) {

231:     function unlocked(address user) external view returns (uint256) {

235:     function totalSupply() public view returns (uint256) {

239:     function balanceOf(address user) public view returns (uint256) {

253:     function nextUnlockTime() public view returns (uint256) {

257:     function epoch() public view returns (uint256) {

261:     function nextEpoch() public view returns (uint256) {

265:     function remainingEpochTime() public view returns (uint256) {

269:     function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {

273:     function rewardPerToken(address rewardToken) public view returns (uint256) {

277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

288:     function earned(address user, address rewardToken) public view returns (uint256) {

292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

300:     function addReward(address rewardToken) public onlyOwner {

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

337:     function pause() external onlyOwner {

341:     function unpause() external onlyOwner {

349:     function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {

458:     function _stakeFor(address account, uint256 amount, bool lock_) internal {

479:     function _createLock(address user, uint256 amount) internal {

528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

544:     function _updateRewards() internal {

557:     function _updateRewardsForUser(address user) internal {

572:     function _updateRewardsForUsers(address[] memory users) internal {
```

</details>

### [N-99] Missing NatSpec `@dev` from modifier declaration

Some modifiers have an incomplete NatSpec: add a `@dev` notation to describe the modifier to improve the code documentation.

There are 7 instances:

- *BlastMagicLP.sol* ( [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L118) ):

```solidity
118:     modifier onlyImplementationOperators() {
```

- *BlastOnboarding.sol* ( [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L43), [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L50) ):

```solidity
43:     modifier onlyState(State _state) {

50:     modifier onlySupportedTokens(address token) {
```

- *MagicLP.sol* ( [607](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L607), [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L614), [621](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L621) ):

```solidity
607:     modifier onlyImplementationOwner() {

614:     modifier onlyClones() {

621:     modifier onlyImplementation() {
```

- *Router.sol* ( [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L47) ):

```solidity
47:     modifier ensureDeadline(uint256 deadline) {
```

### [N-100] Missing NatSpec `@notice` from modifier declaration

Some modifiers have an incomplete NatSpec: add a `@notice` notation to describe the modifier to improve the code documentation.

There are 7 instances:

- *BlastMagicLP.sol* ( [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L118) ):

```solidity
118:     modifier onlyImplementationOperators() {
```

- *BlastOnboarding.sol* ( [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L43), [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L50) ):

```solidity
43:     modifier onlyState(State _state) {

50:     modifier onlySupportedTokens(address token) {
```

- *MagicLP.sol* ( [607](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L607), [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L614), [621](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L621) ):

```solidity
607:     modifier onlyImplementationOwner() {

614:     modifier onlyClones() {

621:     modifier onlyImplementation() {
```

- *Router.sol* ( [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L47) ):

```solidity
47:     modifier ensureDeadline(uint256 deadline) {
```

### [N-101] Missing NatSpec `@dev` from struct declaration

There are 7 instances:

- *BlastOnboarding.sol* ( [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L24) ):

```solidity
24:     struct Balances {
```

- *PMMPricing.sol* ( [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L27) ):

```solidity
27:     struct PMMState {
```

- *LockingMultiRewards.sol* ( [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L50), [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L58), [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L63), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L68), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L73) ):

```solidity
50:     struct Reward {

58:     struct Balances {

63:     struct LockedBalance {

68:     struct RewardLockItem {

73:     struct RewardLock {
```

### [N-102] Missing NatSpec `@notice` from struct declaration

There are 7 instances:

- *BlastOnboarding.sol* ( [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L24) ):

```solidity
24:     struct Balances {
```

- *PMMPricing.sol* ( [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L27) ):

```solidity
27:     struct PMMState {
```

- *LockingMultiRewards.sol* ( [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L50), [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L58), [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L63), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L68), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L73) ):

```solidity
50:     struct Reward {

58:     struct Balances {

63:     struct LockedBalance {

68:     struct RewardLockItem {

73:     struct RewardLock {
```

### [N-103] Large or complicated code bases should implement invariant tests

This includes: large code bases, or code with lots of inline-assembly, complicated math, or complicated interactions between multiple contracts.
Invariant fuzzers such as Echidna require the test writer to come up with invariants which should not be violated under any circumstances, and the fuzzer tests various inputs and function calls to ensure that the invariants always hold.
Even code with 100% code coverage can still have bugs due to the order of the operations a user performs, and invariant fuzzers may help significantly.

There is 1 instance:

- Global finding

### [N-104] The default value is manually set when it is declared

In instances where a new variable is defined, there is no need to set it to it's default value.

There are 2 instances:

- *BlastOnboarding.sol* ( [165-165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L165-L165) ):

```solidity
165:         for (uint256 i = 0; i < tokens.length; i++) {
```

- *Router.sol* ( [544-544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L544-L544) ):

```solidity
544:         for (uint256 i = 0; i < iterations; ) {
```

### [N-105] Contracts should have all `public`/`external` functions exposed by `interface`s

All `external`/`public` functions should extend an `interface`. This is useful to ensure that the whole API is extracted and can be more easily integrated by other projects.

<details>
<summary>There are 12 instances (click to show):</summary>

- *BlastBox.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L13) ):

```solidity
13: contract BlastBox is DegenBox, OperatableV3 {
```

- *BlastGovernor.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L7) ):

```solidity
7: contract BlastGovernor is OperatableV2 {
```

- *BlastMagicLP.sol* ( [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L10) ):

```solidity
10: contract BlastMagicLP is MagicLP {
```

- *BlastOnboarding.sol* ( [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L64) ):

```solidity
64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```

- *BlastOnboardingBoot.sol* ( [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L34) ):

```solidity
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```

- *BlastTokenRegistry.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L6) ):

```solidity
6: contract BlastTokenRegistry is Owned {
```

- *MagicLP.sol* ( [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L25) ):

```solidity
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```

- *FeeRateModel.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L13) ):

```solidity
13: contract FeeRateModel is Owned {
```

- *FeeRateModelImpl.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L7) ):

```solidity
7: contract FeeRateModelImpl {
```

- *Factory.sol* ( [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L11) ):

```solidity
11: contract Factory is Owned {
```

- *Router.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L12) ):

```solidity
12: contract Router {
```

- *LockingMultiRewards.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L14) ):

```solidity
14: contract LockingMultiRewards is OperatableV2, Pausable {
```

</details>

### [N-106] Top-level declarations should be separated by at least two lines

-

<details>
<summary>There are 171 instances (click to show):</summary>

- *BlastBox.sol* ( [3-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L3-L5), [11-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L11-L13), [34-36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L34-L36), [54-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L54-L56), [70-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L70-L72), [79-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L79-L81), [101-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L101-L103) ):

```solidity
3: pragma solidity >=0.8.0;
4: 
5: import {DegenBox} from "/DegenBox.sol";

11: import {IWETH} from "interfaces/IWETH.sol";
12: 
13: contract BlastBox is DegenBox, OperatableV3 {

34:     }
35: 
36:     function _onBeforeDeposit(

54:     }
55: 
56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

70:     }
71: 
72:     function setFeeTo(address feeTo_) external onlyOwner {

79:     }
80: 
81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {

101:     }
102: 
103:     function isOwner(address _account) internal view override returns (bool) {
```

- *BlastDapp.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L2-L4), [4-6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol#L4-L6) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {BlastPoints} from "/blast/libraries/BlastPoints.sol";

4: import {BlastPoints} from "/blast/libraries/BlastPoints.sol";
5: 
6: contract BlastDapp {
```

- *BlastGovernor.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L2-L4), [5-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L5-L7), [30-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L30-L32), [47-49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L47-L49), [51-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L51-L53) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {BlastYields} from "/blast/libraries/BlastYields.sol";

5: import {OperatableV2} from "mixins/OperatableV2.sol";
6: 
7: contract BlastGovernor is OperatableV2 {

30:     }
31: 
32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

47:     }
48: 
49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

51:     }
52: 
53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

- *BlastMagicLP.sol* ( [3-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L3-L5), [8-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L8-L10), [51-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L51-L53), [62-64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L62-L64), [87-89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L87-L89), [102-104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L102-L104) ):

```solidity
3: pragma solidity >=0.8.0;
4: 
5: import {MagicLP} from "/mimswap/MagicLP.sol";

8: import {BlastTokenRegistry} from "/blast/BlastTokenRegistry.sol";
9: 
10: contract BlastMagicLP is MagicLP {

51:     }
52: 
53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {

62:     }
63: 
64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

87:     }
88: 
89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {

102:     }
103: 
104:     function _updateTokenClaimables() internal {
```

- *BlastOnboarding.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L2-L4), [10-12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L10-L12), [48-50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L48-L50), [62-64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L62-L64), [121-123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L121-L123), [130-132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L130-L132), [154-156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L154-L156), [158-160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L158-L160), [162-164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L162-L164), [173-175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L173-L175), [183-185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L183-L185), [188-190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L188-L190), [193-195](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L193-L195), [198-200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L198-L200), [203-205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L203-L205), [212-214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L212-L214), [216-218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L216-L218) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {Owned} from "solmate/auth/Owned.sol";

10: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";
11: 
12: contract BlastOnboardingData is Owned, Pausable {

48:     }
49: 
50:     modifier onlySupportedTokens(address token) {

62: }
63: 
64: contract BlastOnboarding is BlastOnboardingData, Proxy {

121:     }
122: 
123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

130:     }
131: 
132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {

154:     }
155: 
156:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

158:     }
159: 
160:     function claimGasYields() external onlyOwner returns (uint256) {

162:     }
163: 
164:     function claimTokenYields(address[] memory tokens) external onlyOwner {

173:     }
174: 
175:     function setTokenSupported(address token, bool supported) external onlyOwner {

183:     }
184: 
185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

188:     }
189: 
190:     function setBootstrapper(address bootstrapper_) external onlyOwner {

193:     }
194: 
195:     function open() external onlyOwner onlyState(State.Idle) {

198:     }
199: 
200:     function close() external onlyOwner onlyState(State.Opened) {

203:     }
204: 
205:     function rescue(address token, address to, uint256 amount) external onlyOwner {

212:     }
213: 
214:     function pause() external onlyOwner {

216:     }
217: 
218:     function unpause() external onlyOwner {
```

- *BlastOnboardingBoot.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L2-L4), [84-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L84-L86), [127-129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L127-L129), [144-146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L144-L146) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {BlastOnboarding} from "/blast/BlastOnboarding.sol";

84:     }
85: 
86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

127:     }
128: 
129:     function initialize(Router _router) external onlyOwner {

144:     }
145: 
146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
```

- *BlastTokenRegistry.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L2-L4), [4-6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L4-L6), [12-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L12-L14) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {Owned} from "solmate/auth/Owned.sol";

4: import {Owned} from "solmate/auth/Owned.sol";
5: 
6: contract BlastTokenRegistry is Owned {

12:     constructor(address _owner) Owned(_owner) {}
13: 
14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```

- *BlastWrappers.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L2-L4), [17-19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L17-L19), [26-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L26-L28), [40-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L40-L42), [57-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L57-L59), [68-70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L68-L70) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {IERC20} from "BoringSolidity/interfaces/IERC20.sol";

17: error ErrZeroAddress();
18: 
19: contract BlastMIMSwapRouter is Router {

26: }
27: 
28: contract BlastMIMSwapFactory is Factory {

40: }
41: 
42: contract BlastCauldronV4 is CauldronV4 {

57:     }
58: 
59:     function init(bytes calldata data) public payable override {

68:     }
69: 
70:     function _setupBlacklist() private {
```

- *BlastPoints.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L2-L4), [4-6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L4-L6) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {IBlastPoints} from "interfaces/IBlast.sol";

4: import {IBlastPoints} from "interfaces/IBlast.sol";
5: 
6: library BlastPoints {
```

- *BlastYields.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L2-L4), [5-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L5-L7), [27-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L27-L29), [40-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L40-L42), [53-55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L53-L55), [58-60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L58-L60), [73-75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L73-L75) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {IBlast, IERC20Rebasing, YieldMode, GasMode} from "interfaces/IBlast.sol";

5: import {Address} from "openzeppelin-contracts/utils/Address.sol";
6: 
7: library BlastYields {

27:     }
28: 
29:     function configureDefaultClaimables(address governor_) internal {

40:     }
41: 
42:     function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {

53:     }
54: 
55:     function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {

58:     }
59: 
60:     function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {

73:     }
74: 
75:     function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {
```

- *MagicLP.sol* ( [8-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L8-L10), [89-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L89-L91), [136-138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L136-L138), [157-159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L157-L159), [161-163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L161-L163), [165-167](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L165-L167), [178-180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L178-L180), [191-193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L191-L193), [202-204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L202-L204), [213-215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L213-L215), [217-219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L217-L219), [222-224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L222-L224), [226-228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L226-L228), [230-232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L230-L232), [234-236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L234-L236), [265-267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L265-L267), [288-290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L288-L290), [468-470](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L468-L470), [502-504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L502-L504), [543-545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L543-L545), [558-560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L558-L560), [565-567](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L565-L567), [579-581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L579-L581), [585-587](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L585-L587), [591-593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L591-L593), [599-601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L599-L601), [612-614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L612-L614), [619-621](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L619-L621) ):

```solidity
8: pragma solidity >=0.8.0;
9: 
10: import {Owned} from "solmate/auth/Owned.sol";

89:     }
90: 
91:     function init(

136:     }
137: 
138:     function correctRState() external {

157:     }
158: 
159:     function symbol() public pure override returns (string memory) {

161:     }
162: 
163:     function decimals() public view override returns (uint8) {

165:     }
166: 
167:     function querySellBase(

178:     }
179: 
180:     function querySellQuote(

191:     }
192: 
193:     function getPMMState() public view returns (PMMPricing.PMMState memory state) {

202:     }
203: 
204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

213:     }
214: 
215:     function getMidPrice() public view returns (uint256 midPrice) {

217:     }
218: 
219:     function getReserves() external view returns (uint256 baseReserve, uint256 quoteReserve) {

222:     }
223: 
224:     function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {

226:     }
227: 
228:     function getBaseInput() public view returns (uint256 input) {

230:     }
231: 
232:     function getQuoteInput() public view returns (uint256 input) {

234:     }
235: 
236:     function version() external pure virtual returns (string memory) {

265:     }
266: 
267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

288:     }
289: 
290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

468:     }
469: 
470:     function setParameters(

502:     }
503: 
504:     function ratioSync() external nonReentrant onlyImplementationOwner {

543:     }
544: 
545:     function _twapUpdate() internal {

558:     }
559: 
560:     function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {

565:     }
566: 
567:     function _sync() internal {

579:     }
580: 
581:     function _transferBaseOut(address to, uint256 amount) internal {

585:     }
586: 
587:     function _transferQuoteOut(address to, uint256 amount) internal {

591:     }
592: 
593:     function _mint(address to, uint256 amount) internal override {

599:     }
600: 
601:     function _afterInitialized() internal virtual {}

612:     }
613: 
614:     modifier onlyClones() {

619:     }
620: 
621:     modifier onlyImplementation() {
```

- *FeeRateModel.sol* ( [8-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L8-L10), [11-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L11-L13) ):

```solidity
8: pragma solidity >=0.8.0;
9: 
10: import {Owned} from "solmate/auth/Owned.sol";

11: import {IFeeRateImpl} from "../interfaces/IFeeRateModel.sol";
12: 
13: contract FeeRateModel is Owned {
```

- *FeeRateModelImpl.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L4), [5-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol#L5-L7) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {IFeeRateImpl} from "../interfaces/IFeeRateModel.sol";

5: import {Math} from "/mimswap/libraries/Math.sol";
6: 
7: contract FeeRateModelImpl {
```

- *DecimalMath.sol* ( [7-9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L7-L9), [25-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L25-L27), [29-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L29-L31), [33-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L33-L35), [37-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L37-L39), [41-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L41-L43), [45-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L45-L47) ):

```solidity
7: pragma solidity >=0.8.0;
8: 
9: import {Math} from "/mimswap/libraries/Math.sol";

25:     }
26: 
27:     function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {

29:     }
30: 
31:     function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {

33:     }
34: 
35:     function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {

37:     }
38: 
39:     function reciprocalFloor(uint256 target) internal pure returns (uint256) {

41:     }
42: 
43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {

45:     }
46: 
47:     function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```

- *Math.sol* ( [8-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L8-L10), [27-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L27-L29) ):

```solidity
8: pragma solidity >=0.8.0;
9: 
10: import {DecimalMath} from "/mimswap/libraries/DecimalMath.sol";

27:     }
28: 
29:     function sqrt(uint256 x) internal pure returns (uint256 y) {
```

- *PMMPricing.sol* ( [8-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L8-L10), [74-76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L74-L76), [117-119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L117-L119), [145-147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L145-L147), [173-175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L173-L175), [201-203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L201-L203) ):

```solidity
8: pragma solidity >=0.8.0;
9: 
10: import {DecimalMath} from "/mimswap/libraries/DecimalMath.sol";

74:     }
75: 
76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {

117:     }
118: 
119:     function _ROneSellQuoteToken(

145:     }
146: 
147:     function _RBelowSellBaseToken(

173:     }
174: 
175:     function _RAboveSellQuoteToken(

201:     }
202: 
203:     function getMidPrice(PMMState memory state) internal pure returns (uint256) {
```

- *Factory.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L2-L4), [55-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L55-L57), [79-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L79-L81), [103-105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L103-L105), [118-120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L118-L120), [153-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L153-L155) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {Owned} from "solmate/auth/Owned.sol";

55:     }
56: 
57:     function getUserPoolCount(address creator) external view returns (uint256) {

79:     }
80: 
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

103:     }
104: 
105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

118:     }
119: 
120:     function removePool(

153:     }
154: 
155:     function _computeSalt(
```

- *Router.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L2-L4), [10-12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L10-L12), [45-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L45-L47), [52-54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L52-L54), [71-73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L71-L73), [94-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L94-L96), [110-112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L110-L112), [160-162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L160-L162), [176-178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L176-L178), [190-192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L190-L192), [227-229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L227-L229), [249-251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L249-L251), [259-261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L259-L261), [272-274](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L272-L274), [312-314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L312-L314), [334-336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L334-L336), [363-365](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L363-L365), [402-404](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L402-L404), [413-415](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L413-L415), [430-432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L430-L432), [447-449](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L447-L449), [459-461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L459-L461), [476-478](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L476-L478), [539-541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L539-L541), [569-571](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L569-L571), [576-578](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L576-L578), [584-586](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L584-L586), [596-598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L596-L598) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

10: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
11: 
12: contract Router {

45:     }
46: 
47:     modifier ensureDeadline(uint256 deadline) {

52:     }
53: 
54:     function createPool(

71:     }
72: 
73:     function createPoolETH(

94:     }
95: 
96:     function previewCreatePool(

110:     }
111: 
112:     function previewAddLiquidity(

160:     }
161: 
162:     function addLiquidity(

176:     }
177: 
178:     function addLiquidityUnsafe(

190:     }
191: 
192:     function addLiquidityETH(

227:     }
228: 
229:     function addLiquidityETHUnsafe(

249:     }
250: 
251:     function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

259:     }
260: 
261:     function removeLiquidity(

272:     }
273: 
274:     function removeLiquidityETH(

312:     }
313: 
314:     function swapTokensForTokens(

334:     }
335: 
336:     function swapETHForTokens(

363:     }
364: 
365:     function swapTokensForETH(

402:     }
403: 
404:     function sellBaseTokensForTokens(

413:     }
414: 
415:     function sellBaseETHForTokens(

430:     }
431: 
432:     function sellBaseTokensForETH(

447:     }
448: 
449:     function sellQuoteTokensForTokens(

459:     }
460: 
461:     function sellQuoteETHForTokens(

476:     }
477: 
478:     function sellQuoteTokensForETH(

539:     }
540: 
541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

569:     }
570: 
571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

576:     }
577: 
578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

584:     }
585: 
586:     function _validatePath(address[] calldata path) internal pure {

596:     }
597: 
598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {
```

- *MagicLpAggregator.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L2-L4), [7-9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L7-L9), [27-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L27-L29), [31-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L31-L33), [35-37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L35-L37), [46-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L46-L48) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {FixedPointMathLib} from "solady/utils/FixedPointMathLib.sol";

7: import {IMagicLP} from "/mimswap/interfaces/IMagicLP.sol";
8: 
9: contract MagicLpAggregator is IAggregator {

27:     }
28: 
29:     function decimals() external pure override returns (uint8) {

31:     }
32: 
33:     function _getReserves() internal view virtual returns (uint256, uint256) {

35:     }
36: 
37:     function latestAnswer() public view override returns (int256) {

46:     }
47: 
48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```

- *LockingMultiRewards.sol* ( [2-4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L2-L4), [184-186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L184-L186), [189-191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L189-L191), [201-203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L201-L203), [205-207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L205-L207), [209-211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L209-L211), [213-215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L213-L215), [217-219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L217-L219), [221-223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L221-L223), [225-227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L225-L227), [229-231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L229-L231), [233-235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L233-L235), [237-239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L237-L239), [255-257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L255-L257), [259-261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L259-L261), [263-265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L263-L265), [267-269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L267-L269), [271-273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L271-L273), [275-277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L275-L277), [286-288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L286-L288), [290-292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L290-L292), [315-317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L315-L317), [339-341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L339-L341), [477-479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L477-L479), [534-536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L534-L536) ):

```solidity
2: pragma solidity >=0.8.0;
3: 
4: import {OperatableV2} from "mixins/OperatableV2.sol";

184:     }
185: 
186:     function withdrawWithRewards(uint256 amount) public virtual {

189:     }
190: 
191:     function getRewards() public virtual {

201:     }
202: 
203:     function rewardsForDuration(address rewardToken) external view returns (uint256) {

205:     }
206: 
207:     function rewardTokensLength() external view returns (uint256) {

209:     }
210: 
211:     function balances(address user) external view returns (Balances memory) {

213:     }
214: 
215:     function userRewardLock(address user) external view returns (RewardLock memory) {

217:     }
218: 
219:     function userLocks(address user) external view returns (LockedBalance[] memory) {

221:     }
222: 
223:     function userLocksLength(address user) external view returns (uint256) {

225:     }
226: 
227:     function locked(address user) external view returns (uint256) {

229:     }
230: 
231:     function unlocked(address user) external view returns (uint256) {

233:     }
234: 
235:     function totalSupply() public view returns (uint256) {

237:     }
238: 
239:     function balanceOf(address user) public view returns (uint256) {

255:     }
256: 
257:     function epoch() public view returns (uint256) {

259:     }
260: 
261:     function nextEpoch() public view returns (uint256) {

263:     }
264: 
265:     function remainingEpochTime() public view returns (uint256) {

267:     }
268: 
269:     function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {

271:     }
272: 
273:     function rewardPerToken(address rewardToken) public view returns (uint256) {

275:     }
276: 
277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

286:     }
287: 
288:     function earned(address user, address rewardToken) public view returns (uint256) {

290:     }
291: 
292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

315:     }
316: 
317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

339:     }
340: 
341:     function unpause() external onlyOwner {

477:     }
478: 
479:     function _createLock(address user, uint256 amount) internal {

534:     }
535: 
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
```

</details>

### [N-107] Consider adding formal verification proofs

Formal verification is the act of proving or disproving the correctness of intended algorithms underlying a system with respect to a certain formal specification/property/invariant, using formal methods of mathematics.

Some tools that are currently available to perform these tests on smart contracts are [SMTChecker](https://docs.soliditylang.org/en/latest/smtchecker.html) and [Certora Prover](https://www.certora.com/).

<details>
<summary>There are 20 instances (click to show):</summary>

- [*BlastBox.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol)

- [*BlastDapp.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastDapp.sol)

- [*BlastGovernor.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol)

- [*BlastMagicLP.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol)

- [*BlastOnboarding.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol)

- [*BlastOnboardingBoot.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol)

- [*BlastTokenRegistry.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol)

- [*BlastWrappers.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol)

- [*BlastPoints.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol)

- [*BlastYields.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol)

- [*MagicLP.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol)

- [*FeeRateModel.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol)

- [*FeeRateModelImpl.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModelImpl.sol)

- [*DecimalMath.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol)

- [*Math.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol)

- [*PMMPricing.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol)

- [*Factory.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol)

- [*Router.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol)

- [*MagicLpAggregator.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol)

- [*LockingMultiRewards.sol*](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol)

</details>

### [N-108] Prevent re-setting a state variable with the same value

This especially problematic when the setter also emits the same value, which may be confusing to offline parsers.

<details>
<summary>There are 47 instances (click to show):</summary>

- *BlastBox.sol* ( [77-77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L77-L77) ):

```solidity
77:         feeTo = feeTo_;
```

- *BlastGovernor.sol* ( [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L45-L45) ):

```solidity
45:         feeTo = _feeTo;
```

- *BlastMagicLP.sol* ( [85-85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L85-L85) ):

```solidity
85:         feeTo = feeTo_;
```

- *BlastOnboarding.sol* ( [152-152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L152-L152), [191-191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L191-L191), [196-196](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L196-L196), [201-201](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L201-L201) ):

```solidity
152:         feeTo = feeTo_;

191:         bootstrapper = bootstrapper_;

196:         state = State.Opened;

201:         state = State.Closed;
```

- *BlastOnboardingBoot.sol* ( [142-142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L142-L142), [147-147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L147-L147) ):

```solidity
142:         staking = _staking;

147:         ready = _ready;
```

- *MagicLP.sol* ( [140-140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L140-L140), [141-141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L141-L141), [142-142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L142-L142), [145-145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L145-L145), [146-146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L146-L146), [147-147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L147-L147), [257-257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L257-L257), [258-258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L258-L258), [280-280](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L280-L280), [281-281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L281-L281), [321-321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L321-L321), [322-322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L322-L322), [343-343](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L343-L343), [344-344](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L344-L344), [382-382](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L382-L382), [383-383](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L383-L383), [402-402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L402-L402), [403-403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L403-L403), [493-493](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L493-L493), [494-494](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L494-L494), [495-495](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L495-L495), [514-514](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L514-L514), [518-518](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L518-L518), [536-536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L536-L536), [537-537](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L537-L537), [538-538](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L538-L538), [539-539](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L539-L539), [540-540](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L540-L540), [557-557](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L557-L557), [561-561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L561-L561), [562-562](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L562-L562), [572-572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L572-L572), [575-575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L575-L575) ):

```solidity
140:             _RState_ = uint32(PMMPricing.RState.ONE);

141:             _BASE_TARGET_ = _BASE_RESERVE_;

142:             _QUOTE_TARGET_ = _QUOTE_RESERVE_;

145:             _RState_ = uint32(PMMPricing.RState.ONE);

146:             _BASE_TARGET_ = _BASE_RESERVE_;

147:             _QUOTE_TARGET_ = _QUOTE_RESERVE_;

257:             _BASE_TARGET_ = newBaseTarget.toUint112();

258:             _RState_ = uint32(newRState);

280:             _QUOTE_TARGET_ = newQuoteTarget.toUint112();

281:             _RState_ = uint32(newRState);

321:                 _QUOTE_TARGET_ = newQuoteTarget.toUint112();

322:                 _RState_ = uint32(newRState);

343:                 _BASE_TARGET_ = newBaseTarget.toUint112();

344:                 _RState_ = uint32(newRState);

382:             _BASE_TARGET_ = shares.toUint112();

383:             _QUOTE_TARGET_ = DecimalMath.mulFloor(shares, _I_).toUint112();

402:             _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

403:             _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();

493:         _LP_FEE_RATE_ = uint64(newLpFeeRate);

494:         _K_ = uint64(newK);

495:         _I_ = uint128(newI);

514:             _BASE_RESERVE_ = uint112(baseBalance);

518:             _QUOTE_RESERVE_ = uint112(quoteBalance);

536:         _BASE_RESERVE_ = uint112(baseBalance);

537:         _QUOTE_RESERVE_ = uint112(quoteBalance);

538:         _BASE_TARGET_ = uint112(baseBalance);

539:         _QUOTE_TARGET_ = uint112(quoteBalance);

540:         _RState_ = uint32(PMMPricing.RState.ONE);

557:         _BLOCK_TIMESTAMP_LAST_ = blockTimestamp;

561:         _BASE_RESERVE_ = baseReserve.toUint112();

562:         _QUOTE_RESERVE_ = quoteReserve.toUint112();

572:             _BASE_RESERVE_ = baseBalance.toUint112();

575:             _QUOTE_RESERVE_ = quoteBalance.toUint112();
```

- *FeeRateModel.sol* ( [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L51-L51), [58-58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L58-L58) ):

```solidity
51:         maintainer = maintainer_;

58:         implementation = implementation_;
```

- *Factory.sol* ( [101-101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L101-L101), [110-110](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L110-L110) ):

```solidity
101:         implementation = implementation_;

110:         maintainerFeeRateModel = maintainerFeeRateModel_;
```

- *LockingMultiRewards.sol* ( [319-319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L319-L319) ):

```solidity
319:         minLockAmount = _minLockAmount;
```

</details>

### [N-109] Whitespace in Expressions

See the [whitespace](https://docs.soliditylang.org/en/latest/style-guide.html#whitespace-in-expressions) section of the Solidity Style Guide.

<details>
<summary>There are 13 instances (click to show):</summary>

- *Router.sol* ( [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L70), [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L93), [500](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L500), [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L544) ):

```solidity
/// @audit Whitespace inside parenthesis
/// @audit Whitespace before a comma
70:         (shares, , ) = IMagicLP(clone).buyShares(to);

/// @audit Whitespace inside parenthesis
/// @audit Whitespace before a comma
93:         (shares, , ) = IMagicLP(clone).buyShares(to);

/// @audit Whitespace inside parenthesis
/// @audit Whitespace before a comma
500:         (shares, , ) = IMagicLP(lp).buyShares(to);

/// @audit Whitespace inside parenthesis
544:         for (uint256 i = 0; i < iterations; ) {
```

- *LockingMultiRewards.sol* ( [405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L405), [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L547), [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L561), [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L575), [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L580), [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L614) ):

```solidity
/// @audit Whitespace inside parenthesis
405:         for (uint256 i; i < users.length; ) {

/// @audit Whitespace inside parenthesis
547:         for (uint256 i; i < rewardTokens.length; ) {

/// @audit Whitespace inside parenthesis
561:         for (uint256 i; i < rewardTokens.length; ) {

/// @audit Whitespace inside parenthesis
575:         for (uint256 i; i < rewardTokens.length; ) {

/// @audit Whitespace inside parenthesis
580:             for (uint256 j; j < users.length; ) {

/// @audit Whitespace inside parenthesis
614:         for (uint256 i; i < rewardTokens.length; ) {
```

</details>

