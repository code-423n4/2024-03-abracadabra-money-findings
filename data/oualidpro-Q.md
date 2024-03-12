## Summary

### Low Risk Issues

| |Issue|Instances|
|-|:-|:-:|
| [[L&#x2011;1](#l1-vulnerable-versions-of-packages-are-being-used)] | Vulnerable versions of packages are being used | 1 | 
| [[L&#x2011;2](#l2-missing-checks-for-address-0-when-assigning-values-to-address-state-variables)] | Missing checks for `address(0)` when assigning values to address state variables | 4 | 
| [[L&#x2011;3](#l3-for-loops-in-public-or-external-functions-should-be-avoided-due-to-high-gas-costs-and-possible-dos)] | For loops in public or external functions should be avoided due to high gas costs and possible DOS | 2 | 
| [[L&#x2011;4](#l4-decimals-is-not-a-part-of-the-erc-20-standard)] | `decimals()` is not a part of the ERC-20 standard | 2 | 
| [[L&#x2011;5](#l5-division-before-multiplication-can-lead-to-precision-errors)] | Division before multiplication can lead to precision errors | 4 | 
| [[L&#x2011;6](#l6-external-calls-in-an-un-bounded-loop-may-result-in-a-dos)] | `external` calls in an un-bounded loop may result in a DOS | 5 | 
| [[L&#x2011;7](#l7-constant-decimal-values)] | Constant decimal values | 3 | 
| [[L&#x2011;8](#l8-internal-function-calls-within-for-loops)] | `internal` Function calls within for loops | 8 | 
| [[L&#x2011;9](#l9-loss-of-precision)] | Loss of precision | 22 | 
| [[L&#x2011;10](#l10-governance-operations-should-be-behind-a-timelock)] | Governance operations should be behind a timelock | 31 | 
| [[L&#x2011;11](#l11-consider-using-openzeppelin-s-safecast-library-to-prevent-unexpected-overflows-when-casting-from-various-type-int-uint-values)] | Consider using OpenZeppelin’s SafeCast library to prevent unexpected overflows when casting from various type int/uint values | 1 | 
| [[L&#x2011;12](#l12-setters-should-have-initial-value-check)] | Setters should have initial value check | 9 | 
| [[L&#x2011;13](#l13-int-casting-block-timestamp-can-reduce-the-lifespan-of-a-contract)] | Int casting `block.timestamp` can reduce the lifespan of a contract | 1 | 
| [[L&#x2011;14](#l14-large-transfers-may-not-work-with-some-erc20-tokens)] | Large transfers may not work with some `ERC20` tokens | 5 | 
| [[L&#x2011;15](#l15-arrays-can-grow-in-size-without-a-way-to-shrink-them)] | Arrays can grow in size without a way to shrink them | 1 | 
| [[L&#x2011;16](#l16-unsafe-downcast)] | Unsafe downcast | 7 | 
| [[L&#x2011;17](#l17-unspecific-compiler-version-pragma)] | Unspecific compiler version pragma | 20 | 
| [[L&#x2011;18](#l18-unused-empty-receive-fallback-function)] | Unused/empty `receive()`/`fallback()` function | 2 | 
| [[L&#x2011;19](#l19-consider-implementing-two-step-procedure-for-updating-protocol-addresses)] | Consider implementing two-step procedure for updating protocol addresses | 10 | 
| [[L&#x2011;20](#l20-safeapprove-is-deprecated)] | `safeApprove()` is deprecated | 3 | 
| [[L&#x2011;21](#l21-check-of-division-by-zero)] | Check of division by zero | 19 | 
| [[L&#x2011;22](#l22-pausing-withdrawals-is-unfair-to-the-users)] | Pausing withdrawals is unfair to the users | 1 | 
| [[L&#x2011;23](#l23-some-function-should-not-be-marked-as-payable)] | Some function should not be marked as payable | 4 | 
| [[L&#x2011;24](#l24-code-does-not-follow-the-best-practice-of-check-effects-interaction)] | Code does not follow the best practice of check-effects-interaction | 12 | 
| [[L&#x2011;25](#l25-safetransferlib-does-not-ensure-that-the-token-contract-exists)] | `SafeTransferLib` does not ensure that the token contract exists | 9 | 
| [[L&#x2011;26](#l26-prevent-re-setting-a-state-variable-with-the-same-value)] | prevent re-setting a state variable with the same value | 12 | 
| [[L&#x2011;27](#l27-use-forcesafetransfereth-for-dos-protection)] | use `forceSafeTransferETH` for DoS protection. | 5 | 
| [[L&#x2011;28](#l28-use-of-tx-origin-is-unsafe-in-almost-every-context)] | Use of `tx.origin` is unsafe in almost every context | 5 | 
| [[L&#x2011;29](#l29-function-can-return-unassigned-variable)] | Function can return unassigned variable | 1 | 
| [[L&#x2011;30](#l30-using-without-specifying-an-upper-bound-in-version-pragma-is-unsafe)] | Using >/>= without specifying an upper bound in version pragma is unsafe | 20 | 
| [[L&#x2011;31](#l31-variables-shadowing-other-definitions)] | Variables shadowing other definitions | 9 | 
| [[L&#x2011;32](#l32-low-level-calls-to-custom-addresses)] | Low Level Calls to Custom Addresses | 1 | 
| [[L&#x2011;33](#l33-empty-receive-functions-can-cause-gas-issues)] | Empty receive functions can cause gas issues | 2 | 

Total: 241 instances over 33 issues

### Non-critical Issues

| |Issue|Instances|
|-|:-|:-:|
| [[NC&#x2011;1](#nc1-large-or-complicated-code-bases-should-implement-invariant-tests)] | Large or complicated code bases should implement invariant tests | 1 | 
| [[NC&#x2011;2](#nc2-array-is-push-ed-but-not-pop-ed)] | Array is `push()`ed but not `pop()`ed | 2 | 
| [[NC&#x2011;3](#nc3-natspec-natspec-author-is-missing-from-contract)] | [NatSpec] Natspec `@author` is missing from `contract` | 19 | 
| [[NC&#x2011;4](#nc4-avoid-the-use-of-sensitive-terms)] | Avoid the use of sensitive terms | 4 | 
| [[NC&#x2011;5](#nc5-variable-names-that-consist-of-all-capital-letters-should-be-reserved-for-constant-immutable-variables)] | Variable names that consist of all capital letters should be reserved for `constant`/`immutable` variables | 35 | 
| [[NC&#x2011;6](#nc6-common-functions-should-be-refactored-to-a-common-base-contract)] | Common functions should be refactored to a common base contract | 5 | 
| [[NC&#x2011;7](#nc7-overly-complicated-arithmetic)] | Overly complicated arithmetic | 2 | 
| [[NC&#x2011;8](#nc8-constant-redefined-elsewhere)] | Constant redefined elsewhere | 1 | 
| [[NC&#x2011;9](#nc9-constants-in-comparisons-should-appear-on-the-left-side)] | Constants in comparisons should appear on the left side | 76 | 
| [[NC&#x2011;10](#nc10-natspec-natspec-description-is-missing-from-contract)] | [NatSpec] Natspec description is missing from `contract` | 403 | 
| [[NC&#x2011;11](#nc11-contract-does-not-follow-the-solidity-style-guide-s-suggested-layout-ordering)] | Contract does not follow the Solidity style guide's suggested layout ordering | 13 | 
| [[NC&#x2011;12](#nc12-contracts-containing-only-utility-functions-should-be-made-into-libraries)] | Contracts containing only utility functions should be made into libraries | 1 | 
| [[NC&#x2011;13](#nc13-control-structures-do-not-follow-the-solidity-style-guide)] | Control structures do not follow the Solidity Style Guide | 36 | 
| [[NC&#x2011;14](#nc14-custom-error-has-no-error-details)] | Custom error has no error details | 78 | 
| [[NC&#x2011;15](#nc15-consider-using-delete-rather-than-assigning-zero-to-clear-values)] | Consider using `delete` rather than assigning `zero` to clear values | 2 | 
| [[NC&#x2011;16](#nc16-else-block-not-required)] | `else`-block not required | 6 | 
| [[NC&#x2011;17](#nc17-consider-adding-emergency-stop-functionality)] | Consider adding emergency-stop functionality | 1 | 
| [[NC&#x2011;18](#nc18-empty-bytes-check-is-missing)] | Empty bytes check is missing | 7 | 
| [[NC&#x2011;19](#nc19-events-are-missing-sender-information)] | Events are missing sender information | 48 | 
| [[NC&#x2011;20](#nc20-events-may-be-emitted-out-of-order-due-to-reentrancy)] | Events may be emitted out of order due to reentrancy | 23 | 
| [[NC&#x2011;21](#nc21-explicitly-define-visibility-of-state-variables-to-prevent-misconceptions-on-what-can-access-the-variable)] | Explicitly define visibility of state variables to prevent misconceptions on what can access the variable | 1 | 
| [[NC&#x2011;22](#nc22-defining-all-external-public-functions-in-contract-interfaces)] | Defining All External/Public Functions in Contract Interfaces | 107 | 
| [[NC&#x2011;23](#nc23-floating-pragma-should-be-avoided)] | Floating pragma should be avoided | 19 | 
| [[NC&#x2011;24](#nc24-function-definition-do-not-follow-solidity-style-guide)] | Function definition do not follow Solidity style guide | 2 | 
| [[NC&#x2011;25](#nc25-function-ordering-does-not-follow-the-solidity-style-guide)] | Function ordering does not follow the Solidity style guide | 8 | 
| [[NC&#x2011;26](#nc26-address-s-shouldn-t-be-hard-coded)] | `address`s shouldn't be hard-coded | 5 | 
| [[NC&#x2011;27](#nc27-array-indicies-should-be-referenced-via-enum-s-rather-than-via-numeric-literals)] | Array indicies should be referenced via `enum`s rather than via numeric literals | 3 | 
| [[NC&#x2011;28](#nc28-some-if-statement-can-be-converted-to-a-ternary)] | Some if-statement can be converted to a ternary | 12 | 
| [[NC&#x2011;29](#nc29-imports-could-be-organized-more-systematically)] | Imports could be organized more systematically | 8 | 
| [[NC&#x2011;30](#nc30-internal-functions-not-called-by-the-contract-should-be-removed)] | `internal` functions not called by the contract should be removed | 3 | 
| [[NC&#x2011;31](#nc31-large-numeric-literals-should-use-underscores-for-readability)] | Large numeric literals should use underscores for readability | 12 | 
| [[NC&#x2011;32](#nc32-long-functions-should-be-refactored-into-multiple-smaller-functions)] | Long functions should be refactored into multiple, smaller, functions | 7 | 
| [[NC&#x2011;33](#nc33-long-lines-of-code)] | Long lines of code | 54 | 
| [[NC&#x2011;34](#nc34-file-is-missing-natspec)] | File is missing NatSpec | 8 | 
| [[NC&#x2011;35](#nc35-mixed-usage-of-int-uint-with-int256-uint256)] | Mixed usage of `int`/`uint` with `int256`/`uint256` | 2 | 
| [[NC&#x2011;36](#nc36-consider-using-named-mappings)] | Consider using named mappings | 3 | 
| [[NC&#x2011;37](#nc37-consider-using-later-versions-of-solidity-for-more-cappabilities)] | Consider using later versions of solidity for more cappabilities | 20 | 
| [[NC&#x2011;38](#nc38-public-state-variables-shouldn-t-have-a-preceding-in-their-name)] | Public state variables shouldn't have a preceding _ in their name | 13 | 
| [[NC&#x2011;39](#nc39-events-that-mark-critical-parameter-changes-should-contain-both-the-old-and-the-new-value)] | Events that mark critical parameter changes should contain both the old and the new value | 22 | 
| [[NC&#x2011;40](#nc40-use-of-override-is-unnecessary)] | Use of `override` is unnecessary | 10 | 
| [[NC&#x2011;41](#nc41-using-without-specifying-an-upper-bound-is-unsafe)] | Using `>`/`>=` without specifying an upper bound is unsafe | 20 | 
| [[NC&#x2011;42](#nc42-functions-which-are-either-private-or-internal-should-have-a-preceding-in-their-name)] | Functions which are either private or internal should have a preceding _ in their name | 25 | 
| [[NC&#x2011;43](#nc43-public-functions-not-called-by-the-contract-should-be-declared-external-instead)] | `public` functions not called by the contract should be declared `external` instead | 13 | 
| [[NC&#x2011;44](#nc44-setters-should-prevent-re-setting-of-the-same-value)] | Setters should prevent re-setting of the same value | 12 | 
| [[NC&#x2011;45](#nc45-natspec-return-argument-is-missing)] | NatSpec `@return` argument is missing | 21 | 
| [[NC&#x2011;46](#nc46-consider-using-safetransferlib-safetransfereth-or-address-sendvalue-for-clearer-semantic-meaning)] | Consider using `SafeTransferLib.safeTransferETH()` or `Address.sendValue()` for clearer semantic meaning | 1 | 
| [[NC&#x2011;47](#nc47-large-multiples-of-ten-should-use-scientific-notation-e-g-1e6-rather-than-decimal-literals-e-g-1000000-for-readability)] | Large multiples of ten should use scientific notation (e.g. `1e6`) rather than decimal literals (e.g. `1000000`), for readability | 2 | 
| [[NC&#x2011;48](#nc48-misplaced-spdx-identifier)] | Misplaced SPDX identifier | 5 | 
| [[NC&#x2011;49](#nc49-empty-receive-payable-fallback-function-does-not-authorize-requests)] | Empty `receive()`/`payable fallback()` function does not authorize requests | 2 | 
| [[NC&#x2011;50](#nc50-state-variables-should-have-natspec-comments)] | State variables should have `Natspec` comments | 83 | 
| [[NC&#x2011;51](#nc51-contracts-should-have-full-test-coverage)] | Contracts should have full test coverage | 1 | 
| [[NC&#x2011;52](#nc52-natspec-natspec-title-is-missing-from-contract)] | [NatSpec] Natspec `@title` is missing from `contract` | 21 | 
| [[NC&#x2011;53](#nc53-top-level-pragma-declarations-should-be-separated-by-two-blank-lines)] | Top level pragma declarations should be separated by two blank lines | 32 | 
| [[NC&#x2011;54](#nc54-critical-functions-should-be-a-two-step-procedure)] | Critical functions should be a two step procedure | 27 | 
| [[NC&#x2011;55](#nc55-uint-variables-should-have-the-bit-size-defined-explicitly)] | uint variables should have the bit size defined explicitly | 1 | 
| [[NC&#x2011;56](#nc56-2-n-1-should-be-re-written-as-type-uint-n-max)] | `2**<n> - 1` should be re-written as `type(uint<n>).max` | 2 | 
| [[NC&#x2011;57](#nc57-uncommented-fields-in-a-struct)] | Uncommented fields in a struct | 5 | 
| [[NC&#x2011;58](#nc58-using-underscore-at-the-end-of-variable-name)] | Using underscore at the end of variable name | 98 | 
| [[NC&#x2011;59](#nc59-event-is-missing-indexed-fields)] | Event is missing `indexed` fields | 39 | 
| [[NC&#x2011;60](#nc60-unused-error-definition)] | Unused `error` definition | 6 | 
| [[NC&#x2011;61](#nc61-unused-event-definition)] | Unused `event` definition | 3 | 
| [[NC&#x2011;62](#nc62-unused-import)] | Unused Import | 7 | 
| [[NC&#x2011;63](#nc63-missing-upgradability-functionality)] | Missing upgradability functionality | 4 | 
| [[NC&#x2011;64](#nc64-constants-should-be-defined-rather-than-using-magic-numbers)] | Constants should be defined rather than using magic numbers | 25 | 
| [[NC&#x2011;65](#nc65-use-the-latest-solidity-prior-to-0-8-20-if-on-l2s-for-deployment)] | Use the latest solidity (prior to 0.8.20 if on L2s) for deployment | 20 | 
| [[NC&#x2011;66](#nc66-use-a-single-file-for-system-wide-constants)] | Use a single file for system wide constants | 7 | 
| [[NC&#x2011;67](#nc67-consider-using-smtchecker)] | Consider using SMTChecker | 20 | 
| [[NC&#x2011;68](#nc68-variable-name-must-be-in-mixedcase)] | Variable name must be in mixedCase | 10 | 
| [[NC&#x2011;69](#nc69-whitespace-in-expressions)] | Whitespace in Expressions | 13 | 
| [[NC&#x2011;70](#nc70-complex-function-controle-flow)] | Complex function controle flow | 6 | 
| [[NC&#x2011;71](#nc71-consider-bounding-input-array-length)] | Consider bounding input array length | 3 | 
| [[NC&#x2011;72](#nc72-a-function-which-defines-named-returns-in-it-s-declaration-doesn-t-need-to-use-return)] | A function which defines named returns in it's declaration doesn't need to use return | 14 | 
| [[NC&#x2011;73](#nc73-natspec-natspec-dev-is-missing-from-contract)] | [NatSpec] Natspec `@dev` is missing from `contract` | 380 | 
| [[NC&#x2011;74](#nc74-contract-should-expose-an-interface)] | Contract should expose an `interface` | 106 | 
| [[NC&#x2011;75](#nc75-named-imports-of-parent-contracts-are-missing)] | Named imports of parent contracts are missing | 2 | 
| [[NC&#x2011;76](#nc76-natspec-natspec-notice-is-missing-from-contract)] | [NatSpec] Natspec `@notice` is missing from `contract` | 375 | 
| [[NC&#x2011;77](#nc77-function-names-should-use-lowercamelcase)] | `function` names should use lowerCamelCase | 1 | 
| [[NC&#x2011;78](#nc78-expressions-for-constant-values-should-use-immutable-rather-than-constant)] | Expressions for constant values should use `immutable` rather than `constant` | 6 | 
| [[NC&#x2011;79](#nc79-consider-splitting-long-calculations)] | Consider splitting long calculations | 1 | 
| [[NC&#x2011;80](#nc80-immutable-variable-names-don-t-follow-the-solidity-style-guide)] | `immutable` variable names don\'t follow the Solidity style guide | 16 | 
| [[NC&#x2011;81](#nc81-private-public-function-name-should-start-with-underscore)] | `private`/`public` function name should start with underscore | 25 | 
| [[NC&#x2011;82](#nc82-use-the-latest-solidity-version-for-better-security)] | Use the latest Solidity version for better security | 20 | 
| [[NC&#x2011;83](#nc83-consider-adding-formal-verification-proofs)] | Consider adding formal verification proofs | 1 | 
| [[NC&#x2011;84](#nc84-missing-zero-address-check-in-functions-with-address-parameters)] | Missing zero address check in functions with address parameters | 13 | 
| [[NC&#x2011;85](#nc85-use-a-struct-to-encapsulate-multiple-function-parameters)] | Use a struct to encapsulate multiple function parameters | 26 | 
| [[NC&#x2011;86](#nc86-use-inheritdoc-for-overridden-functions)] | Use `@inheritdoc` for overridden functions | 14 | 
| [[NC&#x2011;87](#nc87-multiple-mappings-with-same-keys-can-be-combined-into-a-single-struct-mapping-for-readability)] | Multiple mappings with same keys can be combined into a single struct mapping for readability | 13 | 
| [[NC&#x2011;88](#nc88-constructor-should-emit-an-event)] | constructor should emit an event | 16 | 
| [[NC&#x2011;89](#nc89-complex-functions-should-include-comments)] | Complex functions should include comments | 11 | 
| [[NC&#x2011;90](#nc90-make-use-of-solidiy-s-using-keyword)] | Make use of Solidiy's `using` keyword | 97 | 
| [[NC&#x2011;91](#nc91-avoid-using-underscore-at-the-end-of-a-variable-name)] | Avoid using underscore at the end of a variable name | 98 | 
| [[NC&#x2011;92](#nc92-natspec-natspec-param-is-missing-from-error)] | [NatSpec] Natspec `@param` is missing from `error` | 224 | 
| [[NC&#x2011;93](#nc93-not-using-the-latest-version-of-prb-math-from-dependencies)] | Not using the latest version of `prb-math` from dependencies | 1 | 
| [[NC&#x2011;94](#nc94-enforcing-lowercase-and-underscores-only-in-the-name-field-of-package-json)] | Enforcing Lowercase and Underscores Only in the `name` Field of package.json | 1 | 
| [[NC&#x2011;95](#nc95-non-constant-immutable-state-variables-are-missing-a-setter-post-deployment)] | Non constant/immutable state variables are missing a setter post deployment | 15 | 
| [[NC&#x2011;96](#nc96-consider-making-private-state-variables-internal-to-increase-flexibility)] | Consider making private state variables internal to increase flexibility | 9 | 
| [[NC&#x2011;97](#nc97-using-low-level-call-for-transfers)] | Using Low-Level Call for Transfers | 1 | 
| [[NC&#x2011;98](#nc98-off-by-one-timestamp-error)] | Off-by-one timestamp error | 1 | 
| [[NC&#x2011;99](#nc99-lack-of-space-near-the-operator)] | Lack of space near the operator | 27 | 
| [[NC&#x2011;100](#nc100-incorrect-withdraw-declaration)] | Incorrect withdraw declaration | 2 | 
| [[NC&#x2011;101](#nc101-avoid-mutating-function-parameters)] | Avoid mutating function parameters | 6 | 
| [[NC&#x2011;102](#nc102-a-event-should-be-emitted-if-a-non-immutable-state-variable-is-set-in-a-constructor)] | A event should be emitted if a non immutable state variable is set in a constructor | 25 | 
| [[NC&#x2011;103](#nc103-returning-a-struct-instead-of-returning-many-variables-is-better)] | Returning a struct instead of returning many variables is better | 2 | 
| [[NC&#x2011;104](#nc104-solidity-order-of-argument-evaluation-disrupted-in-non-expression-split-code-by-optimizer-sequences-with-fullinliner)] | [Solidity]: Order of Argument Evaluation Disrupted in Non-Expression-Split Code by Optimizer Sequences with FullInliner | 20 | 
| [[NC&#x2011;105](#nc105-not-using-the-named-return-variables-anywhere-in-the-function-is-confusing)] | Not using the named return variables anywhere in the function is confusing | 19 | 
| [[NC&#x2011;106](#nc106-use-named-return-values)] | Use named return values | 62 | 
| [[NC&#x2011;107](#nc107-consider-moving-duplicated-strings-to-constants)] | Consider moving duplicated strings to constants | 4 | 
| [[NC&#x2011;108](#nc108-missing-checks-for-uint-state-variable-assignments)] | Missing checks for uint state variable assignments | 11 | 
| [[NC&#x2011;109](#nc109-consider-adding-validation-of-user-inputs)] | Consider adding validation of user inputs | 87 | 
| [[NC&#x2011;110](#nc110-consider-allowing-users-access-to-their-funds-at-all-times)] | Consider allowing users access to their funds at all times | 1 | 
| [[NC&#x2011;111](#nc111-consider-using-named-function-calls)] | Consider using named function calls | 69 | 

Total: 3438 instances over 111 issues

## Low Risk Issues

### [L&#x2011;1] Vulnerable versions of packages are being used 
This project's specific package versions are vulnerable to the specific CVEs listed below. Consider switching to more recent versions of these packages that don't have these vulnerabilities


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: package.json



- [CVE-2021-39167](https://github.com/OpenZeppelin/openzeppelin-contracts/security/advisories/GHSA-fg47-3c2x-m2wr) :A vulnerability in TimelockController allowed an actor with the executor role to take immediate control of the timelock, by resetting the delay to 0 and escalating privileges, thus gaining unrestricted access to assets held in the contract. Instances with the executor role set to "open" allow anyone to use the executor role, thus leaving the timelock at risk of being taken over by an attacker.
1: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//package.json#L1-L1) 


</details>


### [L&#x2011;2] Missing checks for `address(0)` when assigning values to address state variables 



*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

191:         bootstrapper = bootstrapper_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L191-L191) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

142:         staking = _staking;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L142-L142) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

58:         implementation = implementation_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L58-L58) 


```solidity

File: /src/staking/LockingMultiRewards.sol

135:         stakingToken = _stakingToken;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L135-L135) 


</details>


### [L&#x2011;3] For loops in public or external functions should be avoided due to high gas costs and possible DOS 
In Solidity, for loops can potentially cause Denial of Service (DoS) attacks if not handled carefully. DoS attacks can occur when an attacker intentionally exploits the gas cost of a function, causing it to run out of gas or making it too expensive for other users to call. Below are some scenarios where for loops can lead to DoS attacks: Nested for loops can become exceptionally gas expensive and should be used sparingly


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

164:     function claimTokenYields(address[] memory tokens) external onlyOwner {
165:         for (uint256 i = 0; i < tokens.length; i++) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L164-L165) 


```solidity

File: /src/staking/LockingMultiRewards.sol

397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
398:         if (users.length != lockIndexes.length) {
399:             revert ErrLengthMismatch();
400:         }
401: 
402:         _updateRewardsForUsers(users);
403: 
404:         // Release all expired users' locks
405:         for (uint256 i; i < users.length; ) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L397-L405) 


</details>


### [L&#x2011;4] `decimals()` is not a part of the ERC-20 standard 
The `decimals()` function is not a part of the [ERC-20 standard](https://eips.ethereum.org/EIPS/eip-20), and was added later as an [optional extension](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/extensions/IERC20Metadata.sol). As such, some valid ERC20 tokens do not support this interface, so it is unsafe to blindly cast all tokens to this interface, and then call this function.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/periphery/Router.sol

83:             _validateDecimals(18, IERC20Metadata(token).decimals());

85:             _validateDecimals(IERC20Metadata(token).decimals(), 18);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L83-L83) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L85-L85)


</details>


### [L&#x2011;5] Division before multiplication can lead to precision errors 
Because Solidity integer division may truncate, it is often preferable to do multiplication before division to prevent precision loss.


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/libraries/Math.sol

99:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);

158:                 temp = (((delta * V1) / V0) * i) / V0;

170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L99-L99) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L158-L158), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L170-L170)


```solidity

File: /src/staking/LockingMultiRewards.sol

258:         return (block.timestamp / rewardsDuration) * rewardsDuration;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L258-L258) 


</details>


### [L&#x2011;6] `external` calls in an un-bounded loop may result in a DOS 
Consider limiting the number of iterations in loops that make external calls


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

169:             if (registry.nativeYieldTokens(tokens[i])) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L169-L169) 


```solidity

File: /src/mimswap/periphery/Router.sol

547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));

550:                 IMagicLP(path[i]).sellQuote(address(path[i + 1]));


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L547-L547) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L550-L550)


```solidity

File: /src/staking/LockingMultiRewards.sol

439:             locks.pop();

648:                 _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L439-L439) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L648-L648)


</details>


### [L&#x2011;7] Constant decimal values 
The use of fixed decimal values such as 1e18 or 1e8 in Solidity contracts can lead to inaccuracies, bugs, and vulnerabilities, particularly when interacting with tokens having different decimal configurations.Not all ERC20 tokens follow the standard 18 decimal places, and assumptions about decimal places can lead to miscalculations.
Always retrieve and use the `decimals()` function from the token contract itself when performing calculations involving token amounts.This ensures that your contract correctly handles tokens with any number of decimal places, mitigating the risk of numerical errors or under / overflows that could jeopardize contract integrity and user funds. 


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/staking/LockingMultiRewards.sol

283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

294:         return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L283-L283) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L283-L283), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L294-L294)


</details>


### [L&#x2011;8] `internal` Function calls within for loops 
Making function calls or external calls within loops in Solidity can lead to inefficient gas usage, potential bottlenecks, and increased vulnerability to attacks. Each function call or external call consumes gas, and when executed within a loop, the gas cost multiplies, potentially causing the transaction to run out of gas or exceed block gas limits. This can result in transaction failure or unpredictable behavior.


*There are 8 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/staking/LockingMultiRewards.sol

548:             _updateRewardsGlobal(rewardTokens[i], totalSupply_);

563:             _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_));

563:             _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_));

577:             uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);

582:                 _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);

582:                 _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);

582:                 _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);

582:                 _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L548-L548) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L563-L563), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L563-L563), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L577-L577), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L582-L582), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L582-L582), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L582-L582), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L582-L582)


</details>


### [L&#x2011;9] Loss of precision 
Division by large numbers may result in the result being zero, due to solidity not supporting fractions. Consider requiring a minimum amount for the numerator to ensure that it is always larger than the denominator


*There are 22 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

435:         baseAmount = (baseBalance * shareAmount) / totalShares;

436:         quoteAmount = (quoteBalance * shareAmount) / totalShares;

513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L435-L435) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L436-L436), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L513-L513), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L517-L517)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

24:         return (target * d) / ONE;

32:         return (target * ONE) / d;

40:         return ONE2 / target;

54:             p = (p * p) / ONE;

56:                 p = (p * target) / ONE;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L24-L24) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L54-L54), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L56-L56)


```solidity

File: /src/mimswap/libraries/Math.sol

20:         uint256 quotient = a / b;

59:             return fairAmount / DecimalMath.ONE;

62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

64:         return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;

181:         bAbs = bAbs / DecimalMath.ONE;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L20-L20) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L59-L59), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L62-L62), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L181-L181)


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);

209:             uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L205-L205) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L209-L209)


```solidity

File: /src/mimswap/periphery/Router.sol

257:         baseAmountOut = (baseBalance * sharesIn) / totalShares;

258:         quoteAmountOut = (quoteBalance * sharesIn) / totalShares;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L257-L257) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L258-L258)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

45:         return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L45-L45) 


```solidity

File: /src/staking/LockingMultiRewards.sol

236:         return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);

241:         return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);

258:         return (block.timestamp / rewardsDuration) * rewardsDuration;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L236-L236) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L241-L241), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L258-L258)


</details>


### [L&#x2011;10] Governance operations should be behind a timelock 
All critical and governance operations should be protected by a timelock. For example from the point of view of a user, the changing of the owner of a contract is a high risk operation that may have outcomes ranging from an attacker gaining control over the protocol, to the function no longer functioning due to a typo in the destination address. To give users plenty of warning so that they can validate any ownership changes, changes of ownership should be behind a timelock.


*There are 31 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

68:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
69:         BlastYields.callPrecompile(data);
70:     }

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L68-L70) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L81-L91)


```solidity

File: /src/blast/BlastGovernor.sol

40:     function setFeeTo(address _feeTo) external onlyOwner {
41:         if(_feeTo == address(0)) {
42:             revert ErrZeroAddress();
43:         }
44:         
45:         feeTo = _feeTo;
46:         emit LogFeeToChanged(_feeTo);
47:     }

49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
50:         BlastYields.callPrecompile(data);
51:     }

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
54:         (success, result) = to.call{value: value}(data);
55:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L40-L47) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L49-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L53-L55)


```solidity

File: /src/blast/BlastOnboarding.sol

147:     function setFeeTo(address feeTo_) external onlyOwner {
148:         if (feeTo_ == address(0)) {
149:             revert ErrZeroAddress();
150:         }
151: 
152:         feeTo = feeTo_;
153:         emit LogFeeToChanged(feeTo_);
154:     }

156:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
157:         BlastYields.callPrecompile(data);
158:     }

160:     function claimGasYields() external onlyOwner returns (uint256) {
161:         return BlastYields.claimMaxGasYields(feeTo);
162:     }

164:     function claimTokenYields(address[] memory tokens) external onlyOwner {
165:         for (uint256 i = 0; i < tokens.length; i++) {
166:             if (!supportedTokens[tokens[i]]) {
167:                 revert ErrUnsupportedToken();
168:             }
169:             if (registry.nativeYieldTokens(tokens[i])) {
170:                 BlastYields.claimAllTokenYields(tokens[i], feeTo);
171:             }
172:         }
173:     }

175:     function setTokenSupported(address token, bool supported) external onlyOwner {
176:         supportedTokens[token] = supported;
177: 
178:         if (registry.nativeYieldTokens(token)) {
179:             BlastYields.enableTokenClaimable(token);
180:         }
181: 
182:         emit LogTokenSupported(token, supported);
183:     }

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {
191:         bootstrapper = bootstrapper_;
192:         emit LogBootstrapperChanged(bootstrapper_);
193:     }

205:     function rescue(address token, address to, uint256 amount) external onlyOwner {
206:         if (supportedTokens[token]) {
207:             revert ErrNotAllowed();
208:         }
209: 
210:         token.safeTransfer(to, amount);
211:         emit LogTokenRescue(token, to, amount);
212:     }

214:     function pause() external onlyOwner {
215:         _pause();
216:     }

218:     function unpause() external onlyOwner {
219:         _unpause();
220:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L147-L154) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L156-L158), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L160-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L164-L173), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L175-L183), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L193), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L205-L212), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L214-L216), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L218-L220)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

096:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
097:         if (pool != address(0)) {
098:             revert ErrAlreadyBootstrapped();
099:         }
100: 
101:         uint256 baseAmount = totals[MIM].locked;
102:         uint256 quoteAmount = totals[USDB].locked;
103:         MIM.safeApprove(address(router), type(uint256).max);
104:         USDB.safeApprove(address(router), type(uint256).max);
105: 
106:         (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
107: 
108:         if (totalPoolShares < minAmountOut) {
109:             revert ErrInsufficientAmountOut();
110:         }
111: 
112:         // Create staking contract
113:         // 3x boosting for locker, 7 days reward duration, 13 weeks lp locking
114:         // make this contract temporary the owner the set it as an operator
115:         // for permissionned `stakeFor` during the claiming process and then
116:         // transfer the ownership to the onboarding owner.
117:         staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
118:         staking.setOperator(address(this), true);
119:         staking.transferOwnership(owner);
120: 
121:         // Approve staking contract
122:         pool.safeApprove(address(staking), totalPoolShares);
123: 
124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);
125: 
126:         return (pool, address(staking), totalPoolShares);
127:     }

129:     function initialize(Router _router) external onlyOwner {
130:         router = Router(payable(_router));
131:         factory = IFactory(router.factory());
132:         emit LogInitialized(_router);
133:     }

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {
138:         if (ready) {
139:             revert ErrCannotChangeOnceReady();
140:         }
141: 
142:         staking = _staking;
143:         emit LogStakingChanged(address(_staking));
144:     }

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
147:         ready = _ready;
148:         emit LogReadyChanged(ready);
149:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L96-L127) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L129-L133), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L144), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L149)


```solidity

File: /src/blast/BlastTokenRegistry.sol

14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
15:         if (token == address(0)) {
16:             revert ErrZeroAddress();
17:         }
18: 
19:         nativeYieldTokens[token] = enabled;
20:         emit LogNativeYieldTokenEnabled(token, enabled);
21:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L14-L21) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L46-L53) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L60)


```solidity

File: /src/mimswap/periphery/Factory.sol

096:     function setLpImplementation(address implementation_) external onlyOwner {
097:         if (implementation_ == address(0)) {
098:             revert ErrZeroAddress();
099:         }
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

116:     function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {
117:         _addPool(creator, baseToken, quoteToken, pool);
118:     }

120:     function removePool(
121:         address creator,
122:         address baseToken,
123:         address quoteToken,
124:         uint256 poolIndex,
125:         uint256 userPoolIndex
126:     ) external onlyOwner {
127:         address[] storage _pools = pools[baseToken][quoteToken];
128:         address pool = _pools[poolIndex];
129:         address[] storage _userPools = userPools[creator];
130: 
131:         _pools[poolIndex] = _pools[_pools.length - 1];
132:         _pools.pop();
133: 
134:         if (_userPools[userPoolIndex] != pool) {
135:             revert ErrInvalidUserPoolIndex();
136:         }
137: 
138:         _userPools[userPoolIndex] = _userPools[_userPools.length - 1];
139:         _userPools.pop();
140: 
141:         emit LogPoolRemoved(pool);
142:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L96-L103) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L112), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L116-L118), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L142)


```solidity

File: /src/staking/LockingMultiRewards.sol

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

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
318:         emit LogSetMinLockAmount(minLockAmount, _minLockAmount);
319:         minLockAmount = _minLockAmount;
320:     }

324:     function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {
325:         // In case it's the staking token, allow to skim the excess
326:         if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {
327:             revert ErrSkimmingTooMuch();
328:         }
329: 
330:         tokenAddress.safeTransfer(owner, tokenAmount);
331:         emit LogRecovered(tokenAddress, tokenAmount);
332:     }

337:     function pause() external onlyOwner {
338:         _pause();
339:     }

341:     function unpause() external onlyOwner {
342:         _unpause();
343:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L300-L315) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L317-L320), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L324-L332), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L337-L339), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L341-L343)


</details>


### [L&#x2011;11] Consider using OpenZeppelin’s SafeCast library to prevent unexpected overflows when casting from various type int/uint values 



*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit `lastTimeRewardApplicable_` is getting converted from `uint256` to `uint248`
533:         _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L533-L533) 


</details>


### [L&#x2011;12] Setters should have initial value check 
Setters should have initial value check to prevent assigning wrong value to the variable. Assginment of wrong value can lead to unexpected behavior of the contract.


*There are 9 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L81-L81) 


```solidity

File: /src/blast/BlastMagicLP.sol

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L89-L89) 


```solidity

File: /src/blast/BlastOnboarding.sol

175:     function setTokenSupported(address token, bool supported) external onlyOwner {

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L175-L175) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L190)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L137) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L146)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

57:     function setImplementation(address implementation_) public onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L57) 


```solidity

File: /src/staking/LockingMultiRewards.sol

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L317-L317) 


</details>


### [L&#x2011;13] Int casting `block.timestamp` can reduce the lifespan of a contract 
Consider removing casting to ensure future functionality.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/staking/LockingMultiRewards.sol

389:         reward.lastUpdateTime = uint248(block.timestamp);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L389-L389) 


</details>


### [L&#x2011;14] Large transfers may not work with some `ERC20` tokens 
Some `IERC20` implementations (e.g `UNI`, `COMP`) may fail if the valued transferred is larger than `uint96`. [Source](https://github.com/d-xo/weird-erc20#revert-on-large-approvals--transfers)


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

138:         token.safeTransfer(msg.sender, amount);

210:         token.safeTransfer(to, amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L138-L138) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L210-L210)


```solidity

File: /src/mimswap/MagicLP.sol

466:         token.safeTransfer(to, amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L466-L466) 


```solidity

File: /src/mimswap/periphery/Router.sol

311:         token.safeTransfer(to, tokenAmountOut);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L311-L311) 


```solidity

File: /src/staking/LockingMultiRewards.sol

330:         tokenAddress.safeTransfer(owner, tokenAmount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L330-L330) 


</details>


### [L&#x2011;15] Arrays can grow in size without a way to shrink them 
It's a good practice to maintain control over the size of array state variables in Solidity, especially if they are dynamically updated.If a contract includes a mechanism to push items into an array, it should ideally also provide a mechanism to remove items.This is because Solidity arrays don't automatically shrink when items are deleted - their length needs to be manually adjusted.
Ignoring this can lead to bloated and inefficient contracts.For instance, iterating over a large array can cause your contract to hit the block gas limit.Additionally, if entries are only marked for deletion but never actually removed, you may end up dealing with stale or irrelevant data, which can cause logical errors.
Therefore, implementing a method to 'pop' items from arrays helps manage contract's state, improve efficiency and prevent potential issues related to gas limits or stale data. Always ensure to handle potential underflow conditions when popping elements from the array.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit the array `rewardTokens` has a `push()` call as shown in the code snippet but without a `pop()` call
313:         rewardTokens.push(rewardToken);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L313-L313) 


</details>


### [L&#x2011;16] Unsafe downcast 
When a type is downcast to a smaller type, the higher order bits are truncated, effectively applying a modulo to the original value. Without any other checks, this wrapping will lead to unexpected behavior and bugs


*There are 7 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

//@audit converting from `uint256` to `uint32`
125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

//@audit converting from `uint256` to `uint112`
438:         _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));

//@audit converting from `uint256` to `uint112`
439:         _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));

//@audit converting from `uint256` to `uint112`
513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

//@audit converting from `uint256` to `uint112`
517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));

//@audit converting from `uint256` to `uint32`
546:         uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L125-L125) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L438-L438), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L439-L439), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L513-L513), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L517-L517), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L546-L546)


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit `lastTimeRewardApplicable_` is getting converted from `uint256` to `uint248`
533:         _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L533-L533) 


</details>


### [L&#x2011;17] Unspecific compiler version pragma 



*There are 20 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L3-L3) 


```solidity

File: /src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L2-L2) 


```solidity

File: /src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L2-L2) 


```solidity

File: /src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L3-L3) 


```solidity

File: /src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L2-L2) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L2-L2) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L2-L2) 


```solidity

File: /src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L2-L2) 


```solidity

File: /src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L2) 


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L7-L7) 


```solidity

File: /src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L8-L8) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L8-L8) 


```solidity

File: /src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L2-L2) 


```solidity

File: /src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L2-L2) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L2-L2) 


```solidity

File: /src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L2-L2) 


</details>


### [L&#x2011;18] Unused/empty `receive()`/`fallback()` function 
If the intention is for the Ether to be used, the function should call another function or emit an event, otherwise it should revert.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastGovernor.sol

13:     receive() external payable {}
14: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L13-L14) 


```solidity

File: /src/mimswap/periphery/Router.sol

36:     receive() external payable {}
37: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L36-L37) 


</details>


### [L&#x2011;19] Consider implementing two-step procedure for updating protocol addresses 
A copy-paste error or a typo may end up bricking protocol functionality, or sending tokens to an address with no known private key. Consider implementing a two-step procedure for updating protocol addresses, where the recipient is set as pending, and must 'accept' the assignment by making an affirmative call. A straight forward way of doing this would be to have the target contracts implement [EIP-165](https://eips.ethereum.org/EIPS/eip-165), and to have the 'set' functions ensure that the recipient is of the right interface type.


*There are 10 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

72:     function setFeeTo(address feeTo_) external onlyOwner {
73:         if (feeTo_ == address(0)) {
74:             revert ErrZeroAddress();
75:         }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L75) 


```solidity

File: /src/blast/BlastGovernor.sol

40:     function setFeeTo(address _feeTo) external onlyOwner {
41:         if(_feeTo == address(0)) {
42:             revert ErrZeroAddress();
43:         }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L40-L43) 


```solidity

File: /src/blast/BlastMagicLP.sol

80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
81:         if (feeTo_ == address(0)) {
82:             revert ErrZeroAddress();
83:         }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L80-L83) 


```solidity

File: /src/blast/BlastOnboarding.sol

147:     function setFeeTo(address feeTo_) external onlyOwner {
148:         if (feeTo_ == address(0)) {
149:             revert ErrZeroAddress();
150:         }

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {
191:         bootstrapper = bootstrapper_;
192:         emit LogBootstrapperChanged(bootstrapper_);
193:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L147-L150) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L193)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {
138:         if (ready) {
139:             revert ErrCannotChangeOnceReady();
140:         }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L140) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

46:     function setMaintainer(address maintainer_) external onlyOwner {
47:         if (maintainer_ == address(0)) {
48:             revert ErrZeroAddress();
49:         }

57:     function setImplementation(address implementation_) public onlyOwner {
58:         implementation = implementation_;
59:         emit LogImplementationChanged(implementation_);
60:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L46-L49) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L60)


```solidity

File: /src/mimswap/periphery/Factory.sol

96:     function setLpImplementation(address implementation_) external onlyOwner {
97:         if (implementation_ == address(0)) {
98:             revert ErrZeroAddress();
99:         }

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
106:         if (address(maintainerFeeRateModel_) == address(0)) {
107:             revert ErrZeroAddress();
108:         }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L96-L99) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L108)


</details>


### [L&#x2011;20] `safeApprove()` is deprecated 
[Deprecated](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/bfff03c0d2a59bcd8e2ead1da9aed9edf0080d05/contracts/token/ERC20/utils/SafeERC20.sol#L38-L45) in favor of `safeIncreaseAllowance()` and `safeDecreaseAllowance()`. If only setting the initial allowance to the value that means infinite, `safeIncreaseAllowance()` can be used instead. The function may currently work, but if a bug is found in this version of OpenZeppelin, and the version that you're forced to upgrade to no longer has this function, you'll encounter unnecessary delays in porting and testing replacement contracts.


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboardingBoot.sol

103:         MIM.safeApprove(address(router), type(uint256).max);

104:         USDB.safeApprove(address(router), type(uint256).max);

122:         pool.safeApprove(address(staking), totalPoolShares);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L103-L103) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L104-L104), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L122-L122)


</details>


### [L&#x2011;21] Check of division by zero 



*There are 19 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboardingBoot.sol

163:         return (userLocked * totalPoolShares) / totalLocked;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L163-L163) 


```solidity

File: /src/mimswap/MagicLP.sol

435:         baseAmount = (baseBalance * shareAmount) / totalShares;

436:         quoteAmount = (quoteBalance * shareAmount) / totalShares;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L435-L435) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L436-L436)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

32:         return (target * ONE) / d;

40:         return ONE2 / target;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L32-L32) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L40-L40)


```solidity

File: /src/mimswap/libraries/Math.sol

20:         uint256 quotient = a / b;

34:             z = (x / z + z) / 2;

62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

96:         } else if ((ki * delta) / ki == delta) {

97:             _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);

99:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);

155:             } else if ((idelta * V1) / idelta == V1) {

158:                 temp = (((delta * V1) / V0) * i) / V0;

158:                 temp = (((delta * V1) / V0) * i) / V0;

170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L20-L20) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L62-L62), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L97-L97), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L99-L99), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L155-L155), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L158-L158), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L158-L158), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L170-L170)


```solidity

File: /src/mimswap/periphery/Router.sol

257:         baseAmountOut = (baseBalance * sharesIn) / totalShares;

258:         quoteAmountOut = (quoteBalance * sharesIn) / totalShares;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L257-L257) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L258-L258)


```solidity

File: /src/staking/LockingMultiRewards.sol

144:         maxLocks = _lockDuration / _rewardsDuration;

283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L144-L144) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L283-L283)


</details>


### [L&#x2011;22] Pausing withdrawals is unfair to the users 
Users should always have the possibility of accessing their own funds, but when these functions are paused, their funds will be locked until the contracts are unpaused.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L132-L132) 


</details>


### [L&#x2011;23] Some function should not be marked as payable 
Some function should not be marked as payable, otherwise the ETH that mistakenly sent along with the function call is locked in the contract


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastGovernor.sol

13:     receive() external payable {}


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L13-L13) 


```solidity

File: /src/blast/BlastOnboarding.sol

80:     receive() external payable override {
81:         revert ErrUnsupported();
82:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L80-L82) 


```solidity

File: /src/blast/BlastWrappers.sol

59:     function init(bytes calldata data) public payable override {
60:         if (_governor == address(this)) {
61:             revert ErrInvalidGovernorAddress();
62:         }
63: 
64:         _setupBlacklist();
65: 
66:         super.init(data);
67:         BlastYields.configureDefaultClaimables(_governor);
68:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L59-L68) 


```solidity

File: /src/mimswap/periphery/Router.sol

36:     receive() external payable {}


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L36-L36) 


</details>


### [L&#x2011;24] Code does not follow the best practice of check-effects-interaction 
Code should follow the best-practice of [check-effects-interaction](https://blockchain-academy.hs-mittweida.de/courses/solidity-coding-beginners-to-intermediate/lessons/solidity-11-coding-patterns/topic/checks-effects-interactions/), where state variables are updated before any external calls are made. Doing so prevents a large class of reentrancy bugs.


*There are 12 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

//@audit the function `safeTransferFrom()` is called before the following assignment
105:             totals[token].locked += amount;

//@audit the function `safeTransferFrom()` is called before the following assignment
108:             totals[token].unlocked += amount;

//@audit the function `safeTransferFrom()` is called before the following assignment
112:         totals[token].total += amount;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L105-L105) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L108-L108), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L112-L112)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

//@audit the function `safeApprove()` is called before the following assignment
117:         staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L117-L117) 


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit the function `safeTransfer()` is called before the following assignment
181:         stakingTokenBalance -= amount;

//@audit the function `push()` is called before the following assignment
314:         _rewardData[rewardToken].exists = true;

//@audit the function `pop()` is called before the following assignment
441:             unlockedSupply += amount;

//@audit the function `pop()` is called before the following assignment
442:             lockedSupply -= amount;

//@audit the function `safeTransferFrom()` is called before the following assignment
465:         stakingTokenBalance += amount;

//@audit the function `safeTransferFrom()` is called before the following assignment
472:             _balances[account].unlocked += amount;

//@audit the function `safeTransferFrom()` is called before the following assignment
473:             unlockedSupply += amount;

//@audit the function `push()` is called before the following assignment
502:             lastLockIndex[user] = lockCount;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L181-L181) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L314-L314), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L441-L441), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L442-L442), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L465-L465), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L472-L472), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L473-L473), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L502-L502)


</details>


### [L&#x2011;25] `SafeTransferLib` does not ensure that the token contract exists 
`SafeTransferLib.sol` has functions named similarly to functions that OpenZeppelin has, but they act differently. At the top of the file is the following comment:
```solidity
/// @dev Note that none of the functions in this library check that a token has code at all! That responsibility is delegated to the caller.
```
https://github.com/transmissions11/solmate/blob/bfc9c25865a274a7827fea5abf6e4fb64fc64e6c/src/utils/SafeTransferLib.sol#L9
This means that if one of the transfer functions is called on a contract that doesn't exist or that got selfdestructed, the call will succeede without any warning/revert, which may cause implicit token holdings validations to be ineffective. Consider using the OpenZeppelin version instead.


*There are 9 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

102:         token.safeTransferFrom(msg.sender, address(this), amount);

138:         token.safeTransfer(msg.sender, amount);

210:         token.safeTransfer(to, amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L102-L102) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L138-L138), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L210-L210)


```solidity

File: /src/mimswap/MagicLP.sol

466:         token.safeTransfer(to, amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L466-L466) 


```solidity

File: /src/mimswap/periphery/Router.sol

91:         token.safeTransferFrom(msg.sender, clone, tokenInAmount);

224:         token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);

246:         token.safeTransferFrom(msg.sender, lp, tokenInAmount);

311:         token.safeTransfer(to, tokenAmountOut);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L91-L91) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L224-L224), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L246-L246), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L311-L311)


```solidity

File: /src/staking/LockingMultiRewards.sol

330:         tokenAddress.safeTransfer(owner, tokenAmount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L330-L330) 


</details>


### [L&#x2011;26] prevent re-setting a state variable with the same value 
Not only is wasteful in terms of gas, but this is especially problematic when an event is emitted and the old and new values set are the same, as listeners might not expect this kind of scenario.


*There are 12 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L81-L81) 


```solidity

File: /src/blast/BlastMagicLP.sol

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L64-L64) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L89-L89)


```solidity

File: /src/blast/BlastOnboarding.sol

175:     function setTokenSupported(address token, bool supported) external onlyOwner {

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L175-L175) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L190)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L137) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L146)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

57:     function setImplementation(address implementation_) public onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L57) 


```solidity

File: /src/mimswap/periphery/Router.sol

404:     function sellBaseTokensForTokens(

432:     function sellBaseTokensForETH(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L404) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L432-L432)


```solidity

File: /src/staking/LockingMultiRewards.sol

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L317-L317) 


</details>


### [L&#x2011;27] use `forceSafeTransferETH` for DoS protection. 
The use of safeTransferETH may in some situations leads to DOS. Therefore, it is recommanded to use the solady forceSafeTransferETH function to avoid such attacks. it is also mentionned in the solady's comments
[Solady Ref](https://github.com/Vectorized/solady/blob/main/src/utils/SafeTransferLib.sol)


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/periphery/Router.sol

221:             refundTo.safeTransferETH(msg.value - wethAdjustedAmount);

309:         to.safeTransferETH(ethAmountOut);

401:         to.safeTransferETH(amountOut);

446:         to.safeTransferETH(amountOut);

492:         to.safeTransferETH(amountOut);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L221-L221) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L309-L309), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L401-L401), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L446-L446), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L492-L492)


</details>


### [L&#x2011;28] Use of `tx.origin` is unsafe in almost every context 
According to [Vitalik Buterin](https://ethereum.stackexchange.com/questions/196/how-do-i-make-my-dapp-serenity-proof), contracts should _not_ `assume that tx.origin will continue to be usable or meaningful`. An example of this is [EIP-3074](https://eips.ethereum.org/EIPS/eip-3074#allowing-txorigin-as-signer-1) which explicitly mentions the intention to change its semantics when it's used with new op codes.There have also been calls to [remove](https://github.com/ethereum/solidity/issues/683) `tx.origin`, and there are [security issues](solidity.readthedocs.io/en/v0.4.24/security-considerations.html#tx-origin) associated with using it for authorization. For these reasons, it's best to completely avoid the feature.Using the variable could make a contract vulnerable if an authorized account calls a malicious contract.You can impersonate a user using a third party contract.


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

250:         (receiveQuoteAmount, mtFee, newRState, newBaseTarget) = querySellBase(tx.origin, baseInput);

273:         (receiveBaseAmount, mtFee, newRState, newQuoteTarget) = querySellQuote(tx.origin, quoteInput);

311:                 tx.origin,

333:                 tx.origin,


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L250-L250) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L273-L273), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L311-L311), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L333-L333)


```solidity

File: /src/mimswap/periphery/Factory.sol

82:         address creator = tx.origin;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L82-L82) 


</details>


### [L&#x2011;29] Function can return unassigned variable 
Make sure that functions with a return value always return a valid and assigned value. Even if the default value is as expected, it should be assigned with the default value for code clarity and to reduce confusion.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/libraries/Math.sol

25:             return quotient;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L25-L25) 


</details>


### [L&#x2011;30] Using >/>= without specifying an upper bound in version pragma is unsafe 



*There are 20 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L3-L3) 


```solidity

File: /src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L2-L2) 


```solidity

File: /src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L2-L2) 


```solidity

File: /src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L3-L3) 


```solidity

File: /src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L2-L2) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L2-L2) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L2-L2) 


```solidity

File: /src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L2-L2) 


```solidity

File: /src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L2) 


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L7-L7) 


```solidity

File: /src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L8-L8) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L8-L8) 


```solidity

File: /src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L2-L2) 


```solidity

File: /src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L2-L2) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L2-L2) 


```solidity

File: /src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L2-L2) 


</details>


### [L&#x2011;31] Variables shadowing other definitions 
A variable declaration shadowing any other existing definition is error-prone. It can cause confusion for developers, potentially introduce bugs, and reduce the readability and maintainability.


*There are 9 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

//@audit this variable is shadowing the `BlastOnboardingData`'s stat variable `bootstrapper`
67:     event LogBootstrapperChanged(address indexed bootstrapper);

//@audit this variable is shadowing the `BlastOnboardingData`'s stat variable `feeTo`
71:     event LogFeeToChanged(address indexed feeTo);

//@audit this variable is shadowing the `BlastOnboardingData`'s stat variable `state`
74:     event LogStateChange(State state);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L67-L67) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L74-L74)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

//@audit this variable is shadowing the `BlastOnboardingBootDataV1`'s stat variable `ready`
37:     event LogReadyChanged(bool ready);

//@audit this variable is shadowing the `BlastOnboardingBootDataV1`'s stat variable `router`
39:     event LogInitialized(Router indexed router);

//@audit this variable is shadowing the `BlastOnboardingBootDataV1`'s stat variable `pool`
40:     event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);

//@audit this variable is shadowing the `BlastOnboardingBootDataV1`'s stat variable `staking`
40:     event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);

//@audit this variable is shadowing the `BlastOnboardingBootDataV1`'s stat variable `staking`
41:     event LogStakingChanged(address indexed staking);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L37-L37) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L41-L41)


```solidity

File: /src/blast/BlastWrappers.sol

//@audit this variable is shadowing the `Router`'s stat variable `factory`
20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L20-L20) 


</details>


### [L&#x2011;32] Low Level Calls to Custom Addresses 
Low-level calls (such as `.call()`, `.delegatecall()`, or `.callcode()`) in Solidity provide a way to interact with other contracts or addresses. However, when these calls are made to addresses that are provided as parameters or are not well-validated, they pose a significant security risk. Untrusted addresses might contain malicious code leading to unexpected behavior, loss of funds, or vulnerabilities.\n\n** Resolution **: Prefer using high- level Solidity function calls or interface - based interactions with known contracts to ensure security.If low - level calls are necessary, rigorously validate the addresses and test all possible interactions.Implementing additional checks and fail - safes can help mitigate potential risks associated with low - level calls.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastGovernor.sol

54:         (success, result) = to.call{value: value}(data);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L54-L54) 


</details>


### [L&#x2011;33] Empty receive functions can cause gas issues 
In Solidity, functions that receive Ether without corresponding functionality to utilize or withdraw these funds can inadvertently lead to a permanent loss of value. This is because if someone sends Ether to the contract, they may be unable to retrieve it. To avoid this, functions receiving Ether should be accompanied by additional methods that process or allow the withdrawal of these funds. If the intent is to use the received Ether, it should trigger a separate function; if not, it should revert the transaction (for instance, via `require(msg.sender == address(weth))`). Access control checks can also prevent unintended Ether transfers, despite the slight gas cost they entail. If concerns over gas costs persist, at minimum, include a rescue function to recover unused Ether. Missteps in handling Ether in smart contracts can lead to irreversible financial losses, hence these precautions are crucial.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastGovernor.sol

13:     receive() external payable {}


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L13-L13) 


```solidity

File: /src/mimswap/periphery/Router.sol

36:     receive() external payable {}


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L36-L36) 


</details>


## Non-critical Issues

### [NC&#x2011;1] Large or complicated code bases should implement invariant tests 
Large code bases, or code with lots of inline-assembly, complicated math, or complicated interactions between multiple contracts, should implement [invariant fuzzing tests](https://medium.com/coinmonks/smart-contract-fuzzing-d9b88e0b0a05). Invariant fuzzers such as Echidna require the test writer to come up with invariants which should not be violated under any circumstances, and the fuzzer tests various inputs and function calls to ensure that the invariants always hold. Even code with 100% code coverage can still have bugs due to the order of the operations a user performs, and invariant fuzzers, with properly and extensively-written invariants, can close this testing gap significantly.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

@audit Should implement invariant tests
1: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L1-L1) 


</details>


### [NC&#x2011;2] Array is `push()`ed but not `pop()`ed 
Array entries are added but are never removed. Consider whether this should be the case, or whether there should be a maximum, or whether old entries should be removed. Cases where there are specific potential problems will be flagged separately under a different issue.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/staking/LockingMultiRewards.sol

648:                 _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));

98:     address[] public rewardTokens;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L648-L648) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L98-L98)


</details>


### [NC&#x2011;3] [NatSpec] Natspec `@author` is missing from `contract` 



*There are 19 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

6: contract BlastDapp {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L6-L6) 


```solidity

File: /src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L13-L13) 


```solidity

File: /src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L7-L7) 


```solidity

File: /src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L10-L10) 


```solidity

File: /src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L64-L64)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

33: /// @dev Functions are postfixed with the version number to avoid collisions
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L33-L34)


```solidity

File: /src/blast/BlastTokenRegistry.sol

6: contract BlastTokenRegistry is Owned {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L6-L6) 


```solidity

File: /src/blast/BlastWrappers.sol

19: contract BlastMIMSwapRouter is Router {

28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L19-L19) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L42-L42)


```solidity

File: /src/blast/libraries/BlastPoints.sol

6: library BlastPoints {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L6-L6) 


```solidity

File: /src/blast/libraries/BlastYields.sol

7: library BlastYields {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L7-L7) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

13: contract FeeRateModel is Owned {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L13-L13) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

7: contract FeeRateModelImpl {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L7-L7) 


```solidity

File: /src/mimswap/periphery/Factory.sol

10: /// @notice Create and register MagicLP pools
11: contract Factory is Owned {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L10-L11) 


```solidity

File: /src/mimswap/periphery/Router.sol

12: contract Router {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L12-L12) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

9: contract MagicLpAggregator is IAggregator {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L9-L9) 


</details>


### [NC&#x2011;4] Avoid the use of sensitive terms 
Use [alternative variants](https://www.zdnet.com/article/mysql-drops-master-slave-and-blacklist-whitelist-terminology/), e.g. allowlist/denylist instead of whitelist/blacklist


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastWrappers.sol

56:         _setupBlacklist();

64:         _setupBlacklist();

70:     function _setupBlacklist() private {

71:         blacklistedCallees[address(BlastYields.BLAST_YIELD_PRECOMPILE)] = true;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L56-L56) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L71-L71)


</details>


### [NC&#x2011;5] Variable names that consist of all capital letters should be reserved for `constant`/`immutable` variables 



*There are 35 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

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

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L68-L68) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L82-L82), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204)


```solidity

File: /src/mimswap/libraries/Math.sol

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

199:         uint256 V2 = DecimalMath.divCeil(numerator, denominator);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L51-L51) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L131-L131), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L131-L131), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L62-L62), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L199-L199)


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

29:         uint256 K;

30:         uint256 B;

31:         uint256 Q;

32:         uint256 B0;

33:         uint256 Q0;

34:         RState R;

209:             uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);

205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L29-L29) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L209-L209), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L205-L205)


</details>


### [NC&#x2011;6] Common functions should be refactored to a common base contract 
The functions below have the same implementation as is seen in other files. The functions should be refactored into functions of a common base contract


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastGovernor.sol

//@audit this function is already seen in `/src/blast/BlastOnboarding.sol`
40:     function setFeeTo(address _feeTo) external onlyOwner {
41:         if(_feeTo == address(0)) {
42:             revert ErrZeroAddress();
43:         }
44:         
45:         feeTo = _feeTo;
46:         emit LogFeeToChanged(_feeTo);
47:     }

//@audit this function is already seen in `/src/blast/BlastGovernor.sol`
49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
50:         BlastYields.callPrecompile(data);
51:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L40-L47) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L49-L51)


```solidity

File: /src/blast/BlastOnboarding.sol

//@audit this function is already seen in `/src/mimswap/periphery/Router.sol`
80:     receive() external payable override {
81:         revert ErrUnsupported();
82:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L80-L82) 


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit this function is already seen in `/src/staking/LockingMultiRewards.sol`
337:     function pause() external onlyOwner {
338:         _pause();
339:     }

//@audit this function is already seen in `/src/staking/LockingMultiRewards.sol`
341:     function unpause() external onlyOwner {
342:         _unpause();
343:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L337-L339) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L341-L343)


</details>


### [NC&#x2011;7] Overly complicated arithmetic 
To maintain readability in code, particularly in Solidity which can involve complex mathematical operations, it is often recommended to limit the number of arithmetic operations to a maximum of 2-3 per line. Too many operations in a single line can make the code difficult to read and understand, increase the likelihood of mistakes, and complicate the process of debugging and reviewing the code. Consider splitting such operations over more than one line, take special care when dealing with division however. Try to limit the number of arithmetic operations to a maximum of 3 per line.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/libraries/Math.sol

64:         return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;
65:     }

170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
171:         uint256 bAbs = (DecimalMath.ONE - k) * V1; // (1-k)Q1


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L64-L65) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L170-L171)


</details>


### [NC&#x2011;8] Constant redefined elsewhere 
Consider defining in only one contract so that values cannot become out of sync when only one location is updated. A [cheap way](https://medium.com/coinmonks/gas-cost-of-solidity-library-functions-dbe0cedd4678) to store constants in a single location is to create an `internal constant` in a `library`. If the variable is a local cache of another contract's value, consider making the cache variable internal or private, which will require external users to query the contract with the source of truth, so that callers don't get out of sync.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastMagicLP.sol

//@audit The same constant is already defined on file : /src/blast/BlastBox.sol
17:     BlastTokenRegistry public immutable registry;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L17-L17) 


</details>


### [NC&#x2011;9] Constants in comparisons should appear on the left side 



*There are 76 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

//@audit `0`
114:         if (caps[token] > 0 && totals[token].total > caps[token]) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L114-L114) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

//@audit `0`
64:         if (shares == 0) {

//@audit `0`
158:         if (totalLocked == 0) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L64-L64) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L158-L158)


```solidity

File: /src/mimswap/MagicLP.sol

//@audit `MAX_K`
111:         if (k > MAX_K) {

//@audit `0`
108:         if (i == 0 || i > MAX_I) {

//@audit `MAX_I`
108:         if (i == 0 || i > MAX_I) {

//@audit `MIN_LP_FEE_RATE`
114:         if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {

//@audit `MAX_LP_FEE_RATE`
114:         if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {

//@audit `0`
294:         if (data.length > 0) {

//@audit `0`
369:         if (baseInput == 0) {

//@audit `0`
375:         if (totalSupply() == 0) {

//@audit `0`
395:         } else if (baseReserve > 0 && quoteReserve > 0) {

//@audit `0`
395:         } else if (baseReserve > 0 && quoteReserve > 0) {

//@audit `0`
377:             if (quoteBalance == 0) {

//@audit `0`
385:             if (_QUOTE_TARGET_ == 0) {

//@audit `2001`
389:             if (shares <= 2001) {

//@audit `0`
450:         if (data.length > 0) {

//@audit `MAX_K`
486:         if (newK > MAX_K) {

//@audit `0`
483:         if (newI == 0 || newI > MAX_I) {

//@audit `MAX_I`
483:         if (newI == 0 || newI > MAX_I) {

//@audit `MIN_LP_FEE_RATE`
489:         if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {

//@audit `MAX_LP_FEE_RATE`
489:         if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {

//@audit `0`
549:         if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {

//@audit `0`
549:         if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {

//@audit `0`
549:         if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {

//@audit `0`
582:         if (amount > 0) {

//@audit `0`
588:         if (amount > 0) {

//@audit `1000`
594:         if (amount <= 1000) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L111-L111) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L108-L108), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L108-L108), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L114-L114), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L114-L114), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L294-L294), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L369-L369), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L375-L375), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L395-L395), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L395-L395), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L377-L377), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L385-L385), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L389-L389), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L450-L450), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L486-L486), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L483-L483), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L483-L483), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L489-L489), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L489-L489), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L549-L549), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L549-L549), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L549-L549), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L582-L582), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L588-L588), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L594-L594)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

//@audit `0`
48:         if (e == 0) {

//@audit `1`
50:         } else if (e == 1) {

//@audit `1`
55:             if (e % 2 == 1) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L48-L48) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L55-L55)


```solidity

File: /src/mimswap/libraries/Math.sol

//@audit `0`
22:         if (remainder > 0) {

//@audit `0`
52:         if (V0 == 0) {

//@audit `0`
58:         if (k == 0) {

//@audit `0`
80:         if (k == 0) {

//@audit `0`
89:         if (V1 == 0) {

//@audit `0`
94:         if (ki == 0) {

//@audit `0`
132:         if (V0 == 0) {

//@audit `0`
136:         if (delta == 0) {

//@audit `0`
140:         if (k == 0) {

//@audit `0`
153:             if (idelta == 0) {

//@audit `0`
192:             if (numerator == 0) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L22-L22) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L52-L52), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L58-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L89-L89), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L94-L94), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L132-L132), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L136-L136), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L140-L140), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L153-L153), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L192-L192)


```solidity

File: /src/mimswap/periphery/Router.sol

//@audit `2001`
105:         if (shares <= 2001) {

//@audit `0`
125:         if (baseInAmount == 0) {

//@audit `0`
131:         if (totalSupply == 0) {

//@audit `0`
147:         } else if (baseReserve > 0 && quoteReserve > 0) {

//@audit `0`
147:         } else if (baseReserve > 0 && quoteReserve > 0) {

//@audit `0`
132:             if (quoteBalance == 0) {

//@audit `2001`
142:             if (shares <= 2001) {

//@audit `0`
327:         if (directions & 1 == 0) {

//@audit `0`
348:         if (directions & 1 == 0) {

//@audit `0`
379:         if ((directions >> lastLpIndex) & 1 == 0) {

//@audit `0`
392:         if (directions & 1 == 0) {

//@audit `0`
521:         if (IERC20(lp).totalSupply() == 0) {

//@audit `0`
527:             if (quoteReserve > 0 && baseReserve > 0) {

//@audit `0`
527:             if (quoteReserve > 0 && baseReserve > 0) {

//@audit `0`
560:         if ((directions & 1 == 0)) {

//@audit `0`
545:             if (directions & 1 == 0) {

//@audit `256`
590:         if (pathLength > 256) {

//@audit `0`
593:         if (pathLength <= 0) {

//@audit `MAX_BASE_QUOTE_DECIMALS_DIFFERENCE`
602:         if (quoteDecimals - baseDecimals > MAX_BASE_QUOTE_DECIMALS_DIFFERENCE) {

//@audit `0`
599:         if (baseDecimals == 0 || quoteDecimals == 0) {

//@audit `0`
599:         if (baseDecimals == 0 || quoteDecimals == 0) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L105-L105) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L125-L125), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L131-L131), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L147-L147), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L147-L147), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L132-L132), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L142-L142), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L327-L327), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L348-L348), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L379-L379), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L392-L392), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L521-L521), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L527-L527), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L527-L527), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L560-L560), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L545-L545), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L590-L590), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L593-L593), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L602-L602), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L599-L599), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L599-L599)


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit `BIPS`
119:         if (_lockingBoostMultiplerInBips <= BIPS) {

//@audit `MIN_LOCK_DURATION`
123:         if (_lockDuration < MIN_LOCK_DURATION) {

//@audit `MIN_REWARDS_DURATION`
127:         if (_rewardsDuration < MIN_REWARDS_DURATION) {

//@audit `0`
131:         if (_lockDuration % _rewardsDuration != 0) {

//@audit `0`
156:         if (amount == 0) {

//@audit `0`
171:         if (amount == 0) {

//@audit `0`
278:         if (totalSupply_ == 0) {

//@audit `MAX_NUM_REWARDS`
309:         if (rewardTokens.length == MAX_NUM_REWARDS) {

//@audit `0`
410:             if (locks.length == 0) {

//@audit `1`
417:             if (index == lastLockIndex[user] && locks.length > 1) {

//@audit `0`
459:         if (amount == 0) {

//@audit `0`
490:         if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {

//@audit `0`
636:                     if (amount > 0) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L119-L119) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L123-L123), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L127-L127), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L131-L131), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L156-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L171-L171), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L278-L278), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L309-L309), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L410-L410), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L417-L417), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L459-L459), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L490-L490), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L636-L636)


</details>


### [NC&#x2011;10] [NatSpec] Natspec description is missing from `contract` 
It is recommended that Solidity contracts are fully annotated using NatSpec for all public interfaces (everything in the ABI). It is clearly stated in the Solidity official documentation. In complex projects such as Defi, the interpretation of all functions and their arguments and returns is important for code readability and auditability.[source](https://docs.soliditylang.org/en/v0.8.15/natspec-format.html)


*There are 403 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

6: contract BlastDapp {

7:     constructor() {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L6-L6) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L7-L7)


```solidity

File: /src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {

14:     event LogTokenDepositEnabled(address indexed token, bool enabled);

15:     event LogFeeToChanged(address indexed feeTo);

17:     error ErrZeroAddress();

18:     error ErrUnsupportedToken();

20:     BlastTokenRegistry public immutable registry;

21:     mapping(address => bool) public enabledTokens;

22:     address public feeTo;

24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

36:     function _onBeforeDeposit(

56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

72:     function setFeeTo(address feeTo_) external onlyOwner {

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {

103:     function isOwner(address _account) internal view override returns (bool) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L13-L13) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L103-L103)


```solidity

File: /src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {

8:     event LogFeeToChanged(address indexed feeTo);

9:     error ErrZeroAddress();

11:     address public feeTo;

13:     receive() external payable {}

15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L8-L8), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L9-L9), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L11-L11), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L53-L53)


```solidity

File: /src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {

11:     event LogFeeToChanged(address indexed feeTo);

12:     event LogOperatorChanged(address indexed, bool);

13:     event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);

15:     error ErrNotAllowedImplementationOperator();

17:     BlastTokenRegistry public immutable registry;

21:     mapping(address => bool) public operators;

23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {

104:     function _updateTokenClaimables() internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L10-L10) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L11-L11), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L53-L53), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L89-L89), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L104-L104)


```solidity

File: /src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {

13:     error ErrZeroAddress();

14:     error ErrWrongState();

15:     error ErrUnsupportedToken();

16:     error ErrNotAllowed();

30:     State public state;

31:     address public bootstrapper;

32:     address public feeTo;

33:     BlastTokenRegistry public registry;

36:     mapping(address token => bool) public supportedTokens;

37:     mapping(address token => Balances) public totals;

38:     mapping(address token => uint256 cap) public caps;

41:     mapping(address user => mapping(address token => Balances)) public balances;

43:     modifier onlyState(State _state) {

50:     modifier onlySupportedTokens(address token) {

58:     constructor() Owned(msg.sender) {

67:     event LogBootstrapperChanged(address indexed bootstrapper);

68:     event LogTokenSupported(address indexed token, bool supported);

69:     event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);

70:     event LogLock(address indexed user, address indexed token, uint256 amount);

71:     event LogFeeToChanged(address indexed feeTo);

72:     event LogWithdraw(address indexed user, address indexed token, uint256 amount);

73:     event LogTokenCapChanged(address indexed token, uint256 cap);

74:     event LogStateChange(State state);

75:     event LogTokenRescue(address indexed token, address indexed to, uint256 amount);

77:     error ErrUnsupported();

78:     error ErrCapReached();

80:     receive() external payable override {

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {

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


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L16-L16), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L58-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L67-L67), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L69-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L78-L78), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L123-L123), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L132-L132), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L156-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L160-L160), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L164-L164), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L195-L195), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L200-L200), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L205-L205), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L214-L214), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L218-L218)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

24:     address public pool;

25:     Router public router;

26:     IFactory public factory;

27:     uint256 public totalPoolShares;

28:     bool public ready;

29:     LockingMultiRewards public staking;

30:     mapping(address user => bool claimed) public claimed;

37:     event LogReadyChanged(bool ready);

38:     event LogClaimed(address indexed user, uint256 shares, bool lock);

39:     event LogInitialized(Router indexed router);

40:     event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);

41:     event LogStakingChanged(address indexed staking);

43:     error ErrInsufficientAmountOut();

44:     error ErrNotReady();

45:     error ErrAlreadyClaimed();

46:     error ErrWrongFeeRateModel();

47:     error ErrAlreadyBootstrapped();

48:     error ErrNothingToClaim();

49:     error ErrCannotChangeOnceReady();

86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

129:     function initialize(Router _router) external onlyOwner {

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L86-L86), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L129-L129), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L137), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L146)


```solidity

File: /src/blast/BlastTokenRegistry.sol

6: contract BlastTokenRegistry is Owned {

7:     event LogNativeYieldTokenEnabled(address indexed token, bool enabled);

8:     error ErrZeroAddress();

10:     mapping(address => bool) public nativeYieldTokens;

12:     constructor(address _owner) Owned(_owner) {}

14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L6-L6) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L7-L7), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L8-L8), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L10-L10), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L14-L14)


```solidity

File: /src/blast/BlastWrappers.sol

19: contract BlastMIMSwapRouter is Router {

28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {

20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

29:     constructor(

43:     error ErrInvalidGovernorAddress();

45:     address private immutable _governor;

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {

59:     function init(bytes calldata data) public payable override {

70:     function _setupBlacklist() private {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L19-L19) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L59-L59), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L70-L70)


```solidity

File: /src/blast/libraries/BlastPoints.sol

6: library BlastPoints {

7:     address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;

8:     IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);

10:     function configure() internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L6-L6) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L7-L7), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L8-L8), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L10-L10)


```solidity

File: /src/blast/libraries/BlastYields.sol

7: library BlastYields {

8:     event LogBlastGasClaimed(address indexed recipient, uint256 amount);

9:     event LogBlastETHClaimed(address indexed recipient, uint256 amount);

10:     event LogBlastTokenClaimed(address indexed recipient, address indexed token, uint256 amount);

11:     event LogBlastTokenClaimableEnabled(address indexed contractAddress, address indexed token);

12:     event LogBlastNativeClaimableEnabled(address indexed contractAddress);

14:     IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L8-L8), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L9-L9), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L10-L10), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L11-L11), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L60-L60), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L86-L86)


```solidity

File: /src/mimswap/MagicLP.sol

30:     event BuyShares(address to, uint256 increaseShares, uint256 totalShares);

31:     event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);

32:     event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);

33:     event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);

34:     event RChange(PMMPricing.RState newRState);

35:     event TokenRescue(address indexed token, address to, uint256 amount);

36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);

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

61:     MagicLP public immutable implementation;

63:     uint256 public constant MAX_I = 10 ** 36;

64:     uint256 public constant MAX_K = 10 ** 18;

65:     uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%

66:     uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%

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

84:     constructor(address owner_) Owned(owner_) {

91:     function init(

138:     function correctRState() external {

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

267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

413:     function sellShares(

470:     function setParameters(

504:     function ratioSync() external nonReentrant onlyImplementationOwner {

545:     function _twapUpdate() internal {

560:     function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {

567:     function _sync() internal {

581:     function _transferBaseOut(address to, uint256 amount) internal {

587:     function _transferQuoteOut(address to, uint256 amount) internal {

593:     function _mint(address to, uint256 amount) internal override {

601:     function _afterInitialized() internal virtual {}

614:     modifier onlyClones() {

621:     modifier onlyImplementation() {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L30-L30) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L52-L52), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L53-L53), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L54-L54), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L58-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L59-L59), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L61-L61), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L63-L63), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L65-L65), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L66-L66), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L78-L78), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L82-L82), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L91-L91), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L138-L138), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L159-L159), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L163-L163), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L167-L167), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L180-L180), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L193-L193), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L219-L219), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L224-L224), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L228-L228), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L232-L232), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L236-L236), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L267-L267), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L290-L290), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L413-L413), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L470), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L504-L504), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L545-L545), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L560-L560), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L567-L567), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L581-L581), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L587-L587), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L593-L593), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L601-L601), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L614-L614), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L621-L621)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

13: contract FeeRateModel is Owned {

14:     event LogImplementationChanged(address indexed implementation);

15:     event LogMaintainerChanged(address indexed maintainer);

17:     error ErrZeroAddress();

19:     address public maintainer;

20:     address public implementation;

22:     constructor(address maintainer_, address owner_) Owned(owner_) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L13-L13) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L22-L22)


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

7: contract FeeRateModelImpl {

9:     function getFeeRate(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L9)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

20:     uint256 internal constant ONE = 10 ** 18;

21:     uint256 internal constant ONE2 = 10 ** 36;

23:     function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {

27:     function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {

31:     function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {

35:     function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {

39:     function reciprocalFloor(uint256 target) internal pure returns (uint256) {

43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {

47:     function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L20-L20) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L47-L47)


```solidity

File: /src/mimswap/libraries/Math.sol

17:     error ErrIsZero();

19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

29:     function sqrt(uint256 x) internal pure returns (uint256 y) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L17-L17) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L131-L131)


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L39-L39) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L104-L104), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L119-L119), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L134-L134), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L147-L147), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L162-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L203-L203)


```solidity

File: /src/mimswap/periphery/Factory.sol

12:     event LogCreated(

23:     event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);

24:     event LogPoolRemoved(address pool);

25:     event LogSetImplementation(address indexed implementation);

26:     event LogSetMaintainer(address indexed newMaintainer);

27:     event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);

29:     error ErrInvalidUserPoolIndex();

30:     error ErrZeroAddress();

32:     address public implementation;

33:     IFeeRateModel public maintainerFeeRateModel;

35:     mapping(address base => mapping(address quote => address[] pools)) public pools;

36:     mapping(address creator => address[] pools) public userPools;

38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

57:     function getUserPoolCount(address creator) external view returns (uint256) {

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

120:     function removePool(

155:     function _computeSalt(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L105), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L120), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L155-L155)


```solidity

File: /src/mimswap/periphery/Router.sol

12: contract Router {

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

31:     uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;

33:     IWETH public immutable weth;

34:     IFactory public immutable factory;

36:     receive() external payable {}

38:     constructor(IWETH weth_, IFactory factory_) {

47:     modifier ensureDeadline(uint256 deadline) {

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

541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

586:     function _validatePath(address[] calldata path) internal pure {

598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L16-L16), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L54-L54), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L112-L112), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L162-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L178-L178), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L192-L192), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L229), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L251-L251), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L274-L274), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L314-L314), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L336-L336), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L365-L365), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L404), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L415-L415), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L432-L432), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L449-L449), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L461-L461), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L478-L478), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L541-L541), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L571-L571), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L578-L578), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L586-L586), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L598-L598)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

9: contract MagicLpAggregator is IAggregator {

10:     IMagicLP public immutable pair;

11:     IAggregator public immutable baseOracle;

12:     IAggregator public immutable quoteOracle;

13:     uint8 public immutable baseDecimals;

14:     uint8 public immutable quoteDecimals;

16:     uint256 public constant WAD = 18;

29:     function decimals() external pure override returns (uint8) {

33:     function _getReserves() internal view virtual returns (uint256, uint256) {

37:     function latestAnswer() public view override returns (int256) {

48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L9-L9) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L10-L10), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L11-L11), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L16-L16), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L48-L48)


```solidity

File: /src/staking/LockingMultiRewards.sol

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

78:     uint256 private constant BIPS = 10_000;

79:     uint256 private constant MAX_NUM_REWARDS = 5;

80:     uint256 private constant MIN_LOCK_DURATION = 1 weeks;

81:     uint256 private constant MIN_REWARDS_DURATION = 1 days;

83:     uint256 public immutable maxLocks;

84:     uint256 public immutable lockingBoostMultiplerInBips;

85:     uint256 public immutable rewardsDuration;

86:     uint256 public immutable lockDuration;

87:     address public immutable stakingToken;

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

186:     function withdrawWithRewards(uint256 amount) public virtual {

191:     function getRewards() public virtual {

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

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

341:     function unpause() external onlyOwner {

479:     function _createLock(address user, uint256 amount) internal {

536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L17-L17) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L78-L78), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L83-L83), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L85-L85), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L86-L86), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L87-L87), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L89-L89), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L90-L90), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L91-L91), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L92-L92), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L94-L94), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L95-L95), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L98-L98), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L100-L100), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L101-L101), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L102-L102), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L103-L103), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L186-L186), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L191-L191), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L203-L203), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L207-L207), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L211-L211), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L219-L219), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L223-L223), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L227-L227), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L231-L231), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L235-L235), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L239-L239), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L257-L257), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L265-L265), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L269-L269), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L273-L273), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L288-L288), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L292-L292), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L317-L317), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L341-L341), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L479-L479), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536)


</details>


### [NC&#x2011;11] Contract does not follow the Solidity style guide's suggested layout ordering 
The [style guide](https://docs.soliditylang.org/en/v0.8.16/style-guide.html#order-of-layout) says that, within a contract, the ordering should be 1) Type declarations, 2) State variables, 3) Events, 4) Modifiers, and 5) Functions, but the contract(s) below do not follow this ordering


*There are 13 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

//@audit the variable definition is misplaced
20:     BlastTokenRegistry public immutable registry;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L20-L20) 


```solidity

File: /src/blast/BlastGovernor.sol

//@audit the variable definition is misplaced
11:     address public feeTo;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L11-L11) 


```solidity

File: /src/blast/BlastMagicLP.sol

//@audit the variable definition is misplaced
17:     BlastTokenRegistry public immutable registry;

//@audit the modifier definition is misplaced
118:     modifier onlyImplementationOperators() {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L17-L17) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L118-L118)


```solidity

File: /src/blast/BlastOnboarding.sol

//@audit the event definition is misplaced
67:     event LogBootstrapperChanged(address indexed bootstrapper);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L67-L67) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

//@audit the variable definition is misplaced
10:     mapping(address => bool) public nativeYieldTokens;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L10-L10) 


```solidity

File: /src/blast/libraries/BlastYields.sol

//@audit the variable definition is misplaced
14:     IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L14-L14) 


```solidity

File: /src/mimswap/MagicLP.sol

//@audit the variable definition is misplaced
61:     MagicLP public immutable implementation;

//@audit the modifier definition is misplaced
607:     modifier onlyImplementationOwner() {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L61-L61) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L607-L607)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

//@audit the variable definition is misplaced
19:     address public maintainer;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L19-L19) 


```solidity

File: /src/mimswap/periphery/Factory.sol

//@audit the variable definition is misplaced
32:     address public implementation;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L32-L32) 


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit the structure definition is misplaced
50:     struct Reward {

//@audit the variable definition is misplaced
78:     uint256 private constant BIPS = 10_000;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L50-L50) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L78-L78)


</details>


### [NC&#x2011;12] Contracts containing only utility functions should be made into libraries 



*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

//@audit the contract `FeeRateModelImpl` contain only utility functions, it should turn to a `library`
7: contract FeeRateModelImpl {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L7-L7) 


</details>


### [NC&#x2011;13] Control structures do not follow the Solidity Style Guide 
See the [control structures](https://docs.soliditylang.org/en/latest/style-guide.html#control-structures) section of the Solidity Style Guide


*There are 36 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

36:     function _onBeforeDeposit(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L36-L36) 


```solidity

File: /src/mimswap/MagicLP.sol

91:     function init(

167:     function querySellBase(

180:     function querySellQuote(

413:     function sellShares(

470:     function setParameters(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L91-L91) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L167-L167), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L180-L180), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L413-L413), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L470)


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

9:     function getFeeRate(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L9) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

104:     function _ROneSellBaseToken(

119:     function _ROneSellQuoteToken(

134:     function _RBelowSellQuoteToken(

147:     function _RBelowSellBaseToken(

162:     function _RAboveSellBaseToken(

175:     function _RAboveSellQuoteToken(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L104-L104) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L119-L119), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L134-L134), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L147-L147), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L162-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L175-L175)


```solidity

File: /src/mimswap/periphery/Factory.sol

65:     function predictDeterministicAddress(

120:     function removePool(

155:     function _computeSalt(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L65-L65) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L120), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L155-L155)


```solidity

File: /src/mimswap/periphery/Router.sol

54:     function createPool(

73:     function createPoolETH(

96:     function previewCreatePool(

112:     function previewAddLiquidity(

162:     function addLiquidity(

178:     function addLiquidityUnsafe(

192:     function addLiquidityETH(

229:     function addLiquidityETHUnsafe(

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

509:     function _adjustAddLiquidity(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L54-L54) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L112-L112), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L162-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L178-L178), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L192-L192), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L229), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L274-L274), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L314-L314), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L336-L336), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L365-L365), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L404), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L415-L415), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L432-L432), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L449-L449), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L461-L461), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L478-L478), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L509-L509)


</details>


### [NC&#x2011;14] Custom error has no error details 
Consider adding parameters to the error to indicate which user or values caused the failure


*There are 78 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

17:     error ErrZeroAddress();

18:     error ErrUnsupportedToken();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L17-L17) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L18-L18)


```solidity

File: /src/blast/BlastGovernor.sol

9:     error ErrZeroAddress();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L9-L9) 


```solidity

File: /src/blast/BlastMagicLP.sol

15:     error ErrNotAllowedImplementationOperator();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L15-L15) 


```solidity

File: /src/blast/BlastOnboarding.sol

13:     error ErrZeroAddress();

14:     error ErrWrongState();

15:     error ErrUnsupportedToken();

16:     error ErrNotAllowed();

77:     error ErrUnsupported();

78:     error ErrCapReached();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L13-L13) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L16-L16), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L78-L78)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

43:     error ErrInsufficientAmountOut();

44:     error ErrNotReady();

45:     error ErrAlreadyClaimed();

46:     error ErrWrongFeeRateModel();

47:     error ErrAlreadyBootstrapped();

48:     error ErrNothingToClaim();

49:     error ErrCannotChangeOnceReady();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L43-L43) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L49-L49)


```solidity

File: /src/blast/BlastTokenRegistry.sol

8:     error ErrZeroAddress();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L8-L8) 


```solidity

File: /src/blast/BlastWrappers.sol

17: error ErrZeroAddress();

43:     error ErrInvalidGovernorAddress();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L17-L17) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L43-L43)


```solidity

File: /src/mimswap/MagicLP.sol

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L38-L38) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L52-L52), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L53-L53), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L54-L54), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L58-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L59-L59)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

17:     error ErrZeroAddress();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L17-L17) 


```solidity

File: /src/mimswap/libraries/Math.sol

17:     error ErrIsZero();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L17-L17) 


```solidity

File: /src/mimswap/periphery/Factory.sol

29:     error ErrInvalidUserPoolIndex();

30:     error ErrZeroAddress();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L29-L29) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L30-L30)


```solidity

File: /src/mimswap/periphery/Router.sol

16:     error ErrNotETHLP();

17:     error ErrExpired();

18:     error ErrZeroAddress();

19:     error ErrPathTooLong();

20:     error ErrEmptyPath();

21:     error ErrBadPath();

23:     error ErrInvalidBaseToken();

24:     error ErrInvalidQuoteToken();

25:     error ErrInTokenNotETH();

26:     error ErrOutTokenNotETH();

27:     error ErrInvalidQuoteTarget();

28:     error ErrZeroDecimals();

29:     error ErrDecimalsDifferenceTooLarge();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L16-L16) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L29-L29)


```solidity

File: /src/staking/LockingMultiRewards.sol

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L30-L30) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L48-L48)


</details>


### [NC&#x2011;15] Consider using `delete` rather than assigning `zero` to clear values 
The `delete` keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/libraries/Math.sol

154:                 temp = 0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L154-L154) 


```solidity

File: /src/staking/LockingMultiRewards.sol

619:             rewards[user][rewardToken] = 0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L619-L619) 


</details>


### [NC&#x2011;16] `else`-block not required 
One level of nesting can be removed by not having an `else` block when the `if`-block returns:


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/libraries/DecimalMath.sol

48:         if (e == 0) {

50:         } else if (e == 1) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L48-L48) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L50-L50)


```solidity

File: /src/mimswap/libraries/Math.sol

22:         if (remainder > 0) {

200:         if (V2 > V1) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L22-L22) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L200-L200)


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

204:         if (state.R == RState.BELOW_ONE) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L204-L204) 


```solidity

File: /src/mimswap/periphery/Router.sol

131:         if (totalSupply == 0) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L131-L131) 


</details>


### [NC&#x2011;17] Consider adding emergency-stop functionality 
In the event of a security breach or any unforeseen emergency, swiftly suspending all protocol operations becomes crucial. Having a mechanism in place to halt all functions collectively, instead of pausing individual contracts separately, substantially enhances the efficiency of mitigating ongoing attacks or vulnerabilities. This not only quickens the response time to potential threats but also reduces operational stress during these critical periods. Therefore, consider integrating a 'circuit breaker' or 'emergency stop' function into the smart contract system architecture. Such a feature would provide the capability to suspend the entire protocol instantly, which could prove invaluable during a time-sensitive crisis management situation.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

//@audit `Pausable`
12: contract BlastOnboardingData is Owned, Pausable {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L12-L12) 


</details>


### [NC&#x2011;18] Empty bytes check is missing 
When developing smart contracts in Solidity, it's crucial to validate the inputs of your functions. This includes ensuring that the bytes parameters are not empty, especially when they represent crucial data such as addresses, identifiers, or raw data that the contract needs to process.
Missing empty bytes checks can lead to unexpected behaviour in your contract.For instance, certain operations might fail, produce incorrect results, or consume unnecessary gas when performed with empty bytes.Moreover, missing input validation can potentially expose your contract to malicious activity, including exploitation of unhandled edge cases.
To mitigate these issues, always validate that bytes parameters are not empty when the logic of your contract requires it.


*There are 7 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

//@audit  ,data are not checked
68:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
69:         BlastYields.callPrecompile(data);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L68-L69) 


```solidity

File: /src/blast/BlastGovernor.sol

//@audit  ,data are not checked
49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
50:         BlastYields.callPrecompile(data);

//@audit  ,data are not checked
53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
54:         (success, result) = to.call{value: value}(data);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L49-L50) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L53-L54)


```solidity

File: /src/blast/BlastMagicLP.sol

//@audit  ,data are not checked
72:     function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {
73:         BlastYields.callPrecompile(data);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L72-L73) 


```solidity

File: /src/blast/BlastOnboarding.sol

//@audit  ,data are not checked
156:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
157:         BlastYields.callPrecompile(data);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L156-L157) 


```solidity

File: /src/blast/BlastWrappers.sol

//@audit  ,data are not checked
59:     function init(bytes calldata data) public payable override {
60:         if (_governor == address(this)) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L59-L60) 


```solidity

File: /src/blast/libraries/BlastYields.sol

//@audit  ,data are not checked
86:     function callPrecompile(bytes calldata data) internal {
87:         Address.functionCall(address(BLAST_YIELD_PRECOMPILE), data);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L86-L87) 


</details>


### [NC&#x2011;19] Events are missing sender information 
When an action is triggered based on a user's action, not being able to filter based on who triggered the action makes event processing a lot more cumbersome. Including the `msg.sender` the events of these types of action will make events much more useful to end users, especially when `msg.sender` is not `tx.origin`.


*There are 48 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

78:         emit LogFeeToChanged(feeTo_);

90:         emit LogTokenDepositEnabled(token, enabled);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L78-L78) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L90-L90)


```solidity

File: /src/blast/BlastGovernor.sol

46:         emit LogFeeToChanged(_feeTo);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L46-L46) 


```solidity

File: /src/blast/BlastMagicLP.sol

86:         emit LogFeeToChanged(feeTo_);

91:         emit LogOperatorChanged(operator, status);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L86-L86) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L91-L91)


```solidity

File: /src/blast/BlastOnboarding.sol

153:         emit LogFeeToChanged(feeTo_);

182:         emit LogTokenSupported(token, supported);

187:         emit LogTokenCapChanged(token, cap);

192:         emit LogBootstrapperChanged(bootstrapper_);

197:         emit LogStateChange(State.Opened);

202:         emit LogStateChange(State.Closed);

211:         emit LogTokenRescue(token, to, amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L153-L153) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L182-L182), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L187-L187), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L192-L192), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L197-L197), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L202-L202), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L211-L211)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

132:         emit LogInitialized(_router);

143:         emit LogStakingChanged(address(_staking));

148:         emit LogReadyChanged(ready);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L124-L124) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L132-L132), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L143-L143), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L148-L148)


```solidity

File: /src/blast/BlastTokenRegistry.sol

20:         emit LogNativeYieldTokenEnabled(token, enabled);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L20-L20) 


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L26-L26) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L62-L62), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L77-L77)


```solidity

File: /src/mimswap/MagicLP.sol

259:             emit RChange(newRState);

282:             emit RChange(newRState);

323:                 emit RChange(newRState);

345:                 emit RChange(newRState);

409:         emit BuyShares(to, shares, balanceOf(to));

467:         emit TokenRescue(token, to, amount);

501:         emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L259-L259) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L282-L282), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L323-L323), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L345-L345), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L409-L409), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L467-L467), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L501-L501)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

52:         emit LogMaintainerChanged(maintainer_);

59:         emit LogImplementationChanged(implementation_);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L52-L52) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L59-L59)


```solidity

File: /src/mimswap/periphery/Factory.sol

88:         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);

102:         emit LogSetImplementation(implementation_);

111:         emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);

141:         emit LogPoolRemoved(pool);

152:         emit LogPoolAdded(baseToken, quoteToken, creator, pool);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L88-L88) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L102-L102), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L111-L111), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L141-L141), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L152-L152)


```solidity

File: /src/staking/LockingMultiRewards.sol

318:         emit LogSetMinLockAmount(minLockAmount, _minLockAmount);

331:         emit LogRecovered(tokenAddress, tokenAmount);

392:         emit LogRewardAdded(amount);

447:             emit LogUnlocked(user, amount, index);

436:                 emit LogLockIndexChanged(user, lastIndex, index);

475:             emit LogStaked(account, amount);

513:         emit LogLocked(user, amount, _nextUnlockTime, lockCount);

611:             emit LogRewardLockCreated(user, _rewardLock.unlockTime);

651:             emit LogRewardLocked(user, rewardToken, rewardAmount);

638:                         emit LogRewardPaid(user, rewardToken, amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L318-L318) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L331-L331), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L392-L392), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L447-L447), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L436-L436), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L475-L475), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L513-L513), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L611-L611), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L651-L651), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L638-L638)


</details>


### [NC&#x2011;20] Events may be emitted out of order due to reentrancy 
Ensure that events follow the best practice of check-effects-interaction, and are emitted before external calls


*There are 23 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

120:         emit LogDeposit(msg.sender, token, amount, lock_);

140:         emit LogWithdraw(msg.sender, token, amount);

211:         emit LogTokenRescue(token, to, amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L120-L120) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L140-L140), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L211-L211)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

71:         emit LogClaimed(msg.sender, shares, lock);

124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

132:         emit LogInitialized(_router);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L71-L71) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L124-L124), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L132-L132)


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L26-L26) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L62-L62), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L77-L77)


```solidity

File: /src/mimswap/MagicLP.sol

467:         emit TokenRescue(token, to, amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L467-L467) 


```solidity

File: /src/mimswap/periphery/Factory.sol

88:         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);

141:         emit LogPoolRemoved(pool);

152:         emit LogPoolAdded(baseToken, quoteToken, creator, pool);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L88-L88) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L141-L141), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L152-L152)


```solidity

File: /src/staking/LockingMultiRewards.sol

183:         emit LogWithdrawn(msg.sender, amount);

331:         emit LogRecovered(tokenAddress, tokenAmount);

392:         emit LogRewardAdded(amount);

447:             emit LogUnlocked(user, amount, index);

475:             emit LogStaked(account, amount);

638:                         emit LogRewardPaid(user, rewardToken, amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L183-L183) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L331-L331), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L392-L392), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L447-L447), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L475-L475), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L638-L638)


</details>


### [NC&#x2011;21] Explicitly define visibility of state variables to prevent misconceptions on what can access the variable 
Such state variables should be marked as private as this is the default visibility


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/libraries/BlastYields.sol

14:     IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L14-L14) 


</details>


### [NC&#x2011;22] Defining All External/Public Functions in Contract Interfaces 
It is preferable to have all the external and public function in an interface to make using them easier by developers. This helps ensure the whole API is extracted in a interface.


*There are 107 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

52:     function claimGasYields() external onlyOperators returns (uint256) {
53:         return BlastYields.claimMaxGasYields(feeTo);

56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
57:         if (!registry.nativeYieldTokens(token_)) {

68:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
69:         BlastYields.callPrecompile(data);

72:     function setFeeTo(address feeTo_) external onlyOwner {
73:         if (feeTo_ == address(0)) {

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {
82:         enabledTokens[token] = enabled;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L52-L53) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L56-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L68-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L81-L82)


```solidity

File: /src/blast/BlastGovernor.sol

28:     function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
29:         return BlastYields.claimAllNativeYields(contractAddress, feeTo);

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
33:         return BlastYields.claimMaxGasYields(contractAddress, feeTo);

40:     function setFeeTo(address _feeTo) external onlyOwner {
41:         if(_feeTo == address(0)) {

49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
50:         BlastYields.callPrecompile(data);

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
54:         (success, result) = to.call{value: value}(data);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L28-L29) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L32-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L40-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L49-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L53-L54)


```solidity

File: /src/blast/BlastMagicLP.sol

47:     function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {
48:         address feeTo_ = BlastMagicLP(address(implementation)).feeTo();

53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {
54:         address feeTo_ = BlastMagicLP(address(implementation)).feeTo();

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {
65:         _updateTokenClaimables();

72:     function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {
73:         BlastYields.callPrecompile(data);

80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
81:         if (feeTo_ == address(0)) {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
90:         operators[operator] = status;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L47-L48) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L53-L54), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L64-L65), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L72-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L80-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L89-L90)


```solidity

File: /src/blast/BlastOnboarding.sol

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
124:         balances[msg.sender][token].unlocked -= amount;

147:     function setFeeTo(address feeTo_) external onlyOwner {
148:         if (feeTo_ == address(0)) {

156:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
157:         BlastYields.callPrecompile(data);

160:     function claimGasYields() external onlyOwner returns (uint256) {
161:         return BlastYields.claimMaxGasYields(feeTo);

164:     function claimTokenYields(address[] memory tokens) external onlyOwner {
165:         for (uint256 i = 0; i < tokens.length; i++) {

175:     function setTokenSupported(address token, bool supported) external onlyOwner {
176:         supportedTokens[token] = supported;

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
186:         caps[token] = cap;

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {
191:         bootstrapper = bootstrapper_;

195:     function open() external onlyOwner onlyState(State.Idle) {
196:         state = State.Opened;

200:     function close() external onlyOwner onlyState(State.Opened) {
201:         state = State.Closed;

205:     function rescue(address token, address to, uint256 amount) external onlyOwner {
206:         if (supportedTokens[token]) {

214:     function pause() external onlyOwner {
215:         _pause();

218:     function unpause() external onlyOwner {
219:         _unpause();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L123-L124) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L147-L148), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L156-L157), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L160-L161), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L164-L165), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L175-L176), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L185-L186), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L191), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L195-L196), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L200-L201), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L205-L206), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L214-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L218-L219)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

78:     function claimable(address user) external view returns (uint256 shares) {
79:         if (!ready || claimed[user]) {

86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
87:         uint256 baseAmount = totals[MIM].locked;

96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
97:         if (pool != address(0)) {

129:     function initialize(Router _router) external onlyOwner {
130:         router = Router(payable(_router));

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {
138:         if (ready) {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
147:         ready = _ready;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L78-L79) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L86-L87), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L96-L97), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L129-L130), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L138), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L147)


```solidity

File: /src/blast/BlastTokenRegistry.sol

14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
15:         if (token == address(0)) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L14-L15) 


```solidity

File: /src/mimswap/MagicLP.sol

134:     function sync() external nonReentrant {
135:         _sync();

138:     function correctRState() external {
139:         if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {

167:     function querySellBase(
168:         address trader,
169:         uint256 payBaseAmount
170:     ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {

180:     function querySellQuote(
181:         address trader,
182:         uint256 payQuoteAmount
183:     ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {

193:     function getPMMState() public view returns (PMMPricing.PMMState memory state) {
194:         state.i = _I_;

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
205:         PMMPricing.PMMState memory state = getPMMState();

215:     function getMidPrice() public view returns (uint256 midPrice) {
216:         return PMMPricing.getMidPrice(getPMMState());

224:     function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
225:         return _MT_FEE_RATE_MODEL_.getFeeRate(user, _LP_FEE_RATE_);

228:     function getBaseInput() public view returns (uint256 input) {
229:         return _BASE_TOKEN_.balanceOf(address(this)) - uint256(_BASE_RESERVE_);

232:     function getQuoteInput() public view returns (uint256 input) {
233:         return _QUOTE_TOKEN_.balanceOf(address(this)) - uint256(_QUOTE_RESERVE_);

236:     function version() external pure virtual returns (string memory) {
237:         return "MagicLP 1.0.0";

461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {
462:         if (token == _BASE_TOKEN_ || token == _QUOTE_TOKEN_) {

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

504:     function ratioSync() external nonReentrant onlyImplementationOwner {
505:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L134-L135) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L138-L139), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L167-L170), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L180-L183), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L193-L194), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L205), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L215-L216), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L224-L225), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L228-L229), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L232-L233), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L236-L237), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L461-L462), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L479), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L504-L505)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

46:     function setMaintainer(address maintainer_) external onlyOwner {
47:         if (maintainer_ == address(0)) {

57:     function setImplementation(address implementation_) public onlyOwner {
58:         implementation = implementation_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L46-L47) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L58)


```solidity

File: /src/mimswap/periphery/Factory.sol

53:     function getPoolCount(address token0, address token1) external view returns (uint256) {
54:         return pools[token0][token1].length;

57:     function getUserPoolCount(address creator) external view returns (uint256) {
58:         return userPools[creator].length;

96:     function setLpImplementation(address implementation_) external onlyOwner {
97:         if (implementation_ == address(0)) {

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
106:         if (address(maintainerFeeRateModel_) == address(0)) {

116:     function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {
117:         _addPool(creator, baseToken, quoteToken, pool);

120:     function removePool(
121:         address creator,
122:         address baseToken,
123:         address quoteToken,
124:         uint256 poolIndex,
125:         uint256 userPoolIndex
126:     ) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L53-L54) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L57-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L96-L97), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L106), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L116-L117), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L126)


```solidity

File: /src/mimswap/periphery/Router.sol

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

096:     function previewCreatePool(
097:         uint256 i,
098:         uint256 baseInAmount,
099:         uint256 quoteInAmount
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
252:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp));

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


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L54-L63) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L73-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L96-L100), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L112-L116), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L162-L169), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L178-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L192-L199), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L235), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L251-L252), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L261-L268), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L274-L281), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L314-L321), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L336-L342), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L365-L372), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L410), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L415-L420), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L432-L438), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L449-L455), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L461-L466), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L478-L484)


```solidity

File: /src/staking/LockingMultiRewards.sol

150:     function stake(uint256 amount, bool lock_) public whenNotPaused {
151:         _stakeFor(msg.sender, amount, lock_);

155:     function lock(uint256 amount) public whenNotPaused {
156:         if (amount == 0) {

186:     function withdrawWithRewards(uint256 amount) public virtual {
187:         withdraw(amount);

191:     function getRewards() public virtual {
192:         _updateRewardsForUser(msg.sender);

199:     function rewardData(address token) external view returns (Reward memory) {
200:         return _rewardData[token];

203:     function rewardsForDuration(address rewardToken) external view returns (uint256) {
204:         return _rewardData[rewardToken].rewardRate * rewardsDuration;

207:     function rewardTokensLength() external view returns (uint256) {
208:         return rewardTokens.length;

211:     function balances(address user) external view returns (Balances memory) {
212:         return _balances[user];

215:     function userRewardLock(address user) external view returns (RewardLock memory) {
216:         return _userRewardLock[user];

219:     function userLocks(address user) external view returns (LockedBalance[] memory) {
220:         return _userLocks[user];

223:     function userLocksLength(address user) external view returns (uint256) {
224:         return _userLocks[user].length;

227:     function locked(address user) external view returns (uint256) {
228:         return _balances[user].locked;

231:     function unlocked(address user) external view returns (uint256) {
232:         return _balances[user].unlocked;

253:     function nextUnlockTime() public view returns (uint256) {
254:         return nextEpoch() + lockDuration;

257:     function epoch() public view returns (uint256) {
258:         return (block.timestamp / rewardsDuration) * rewardsDuration;

261:     function nextEpoch() public view returns (uint256) {
262:         return epoch() + rewardsDuration;

265:     function remainingEpochTime() public view returns (uint256) {
266:         return nextEpoch() - block.timestamp;

269:     function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {
270:         return MathLib.min(block.timestamp, _rewardData[rewardToken].periodFinish);

273:     function rewardPerToken(address rewardToken) public view returns (uint256) {
274:         return _rewardPerToken(rewardToken, lastTimeRewardApplicable(rewardToken), totalSupply());

277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
278:         if (totalSupply_ == 0) {

288:     function earned(address user, address rewardToken) public view returns (uint256) {
289:         return _earned(user, balanceOf(user), rewardToken, rewardPerToken(rewardToken));

300:     function addReward(address rewardToken) public onlyOwner {
301:         if (rewardToken == address(0)) {

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
318:         emit LogSetMinLockAmount(minLockAmount, _minLockAmount);

324:     function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {
325:         // In case it's the staking token, allow to skim the excess

337:     function pause() external onlyOwner {
338:         _pause();

341:     function unpause() external onlyOwner {
342:         _unpause();

349:     function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {
350:         _stakeFor(account, amount, lock_);

361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
362:         if (!_rewardData[rewardToken].exists) {

397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
398:         if (users.length != lockIndexes.length) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L150-L151) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L155-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L186-L187), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L191-L192), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L199-L200), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L203-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L207-L208), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L211-L212), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L215-L216), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L219-L220), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L223-L224), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L227-L228), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L231-L232), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L253-L254), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L257-L258), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L261-L262), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L265-L266), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L269-L270), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L273-L274), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L278), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L288-L289), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L300-L301), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L317-L318), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L324-L325), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L337-L338), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L341-L342), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L349-L350), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L361-L362), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L397-L398)


</details>


### [NC&#x2011;23] Floating pragma should be avoided 
If you leave a floating pragma in your code (pragma solidity 0.4>=0.6. 0. ), you won't know which version was deployed to compile your code, leading to unexpected behavior


*There are 19 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L2-L2) 


```solidity

File: /src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L3-L3) 


```solidity

File: /src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L2-L2) 


```solidity

File: /src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L3-L3) 


```solidity

File: /src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L2-L2) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L2-L2)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L2-L2) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L2-L2)


```solidity

File: /src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L2-L2) 


```solidity

File: /src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;

2: pragma solidity >=0.8.0;

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L2) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L2), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L2)


```solidity

File: /src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L2) 


```solidity

File: /src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L2-L2) 


```solidity

File: /src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L2-L2) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L2-L2) 


```solidity

File: /src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L2-L2) 


</details>


### [NC&#x2011;24] Function definition do not follow Solidity style guide 
See [this](https://docs.soliditylang.org/en/v0.8.19/style-guide.html#function-declaration) link for an explanation of the correct ordering


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboardingBoot.sol

//@audit the function visibility is misplaced
86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L86-L86) 


```solidity

File: /src/mimswap/periphery/Router.sol

//@audit the function visibility is misplaced
251:     function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L251-L251) 


</details>


### [NC&#x2011;25] Function ordering does not follow the Solidity style guide 
According to the [Solidity style guide](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#order-of-functions), functions should be laid out in the following order :`constructor()`, `receive()`, `fallback()`, `external`, `public`, `internal`, `private`, but the cases below do not follow this pattern


*There are 8 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

52:     function claimGasYields() external onlyOperators returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L52-L52) 


```solidity

File: /src/blast/BlastGovernor.sol

15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L15-L15) 


```solidity

File: /src/blast/BlastOnboarding.sol

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L84-L84) 


```solidity

File: /src/mimswap/MagicLP.sol

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204) 


```solidity

File: /src/mimswap/periphery/Factory.sol

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81) 


```solidity

File: /src/mimswap/periphery/Router.sol

36:     receive() external payable {}


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L36-L36) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

37:     function latestAnswer() public view override returns (int256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L37-L37) 


```solidity

File: /src/staking/LockingMultiRewards.sol

199:     function rewardData(address token) external view returns (Reward memory) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L199-L199) 


</details>


### [NC&#x2011;26] `address`s shouldn't be hard-coded 
It is often better to declare `address`es as `immutable`, and assign them via constructor arguments. This allows the code to remain the same across deployments on different networks, and avoids recompilation when addresses need to change.


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboardingBoot.sol

//@audit hardcoded address : 0x4300000000000000000000000000000000000003
13: address constant USDB = 0x4300000000000000000000000000000000000003;

//@audit hardcoded address : 0x76DA31D7C9CbEAE102aff34D3398bC450c8374c1
14: address constant MIM = 0x76DA31D7C9CbEAE102aff34D3398bC450c8374c1;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L13-L13) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L14-L14)


```solidity

File: /src/blast/libraries/BlastPoints.sol

//@audit hardcoded address : 0xD1025F1359422Ca16D9084908d629E0dBa60ff28
7:     address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;

//@audit hardcoded address : 0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800
8:     IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L8-L8)


```solidity

File: /src/blast/libraries/BlastYields.sol

//@audit hardcoded address : 0x4300000000000000000000000000000000000002
14:     IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L14-L14) 


</details>


### [NC&#x2011;27] Array indicies should be referenced via `enum`s rather than via numeric literals 
Consider using an enum instead of hardcoding an index access to make the code easier to understand.


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/periphery/Router.sol

//@audit `path`
324:         address firstLp = path[0];

//@audit `path`
345:         address firstLp = path[0];

//@audit `path`
389:         address firstLp = path[0];


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L324-L324) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L345-L345), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L389-L389)


</details>


### [NC&#x2011;28] Some if-statement can be converted to a ternary 
Improving code readability and compactness is an integral part of optimal programming practices. The use of ternary operators in place of if-else conditions is one such measure. Ternary operators allow us to write conditional statements in a more concise manner, thereby enhancing readability and simplicity. They follow the syntax `condition ? exprIfTrue : exprIfFalse`, which interprets as "if the condition is true, evaluate to `exprIfTrue`, else evaluate to `exprIfFalse`". By adopting this approach, we make our code more streamlined and intuitive, which could potentially aid in better understanding and maintenance of the codebase.


*There are 12 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/libraries/Math.sol

22:         if (remainder > 0) {
23:             return quotient + 1;
24:         } else {
25:             return quotient;
26:         }

200:         if (V2 > V1) {
201:             return 0;
202:         } else {
203:             return V1 - V2;
204:         }

096:         } else if ((ki * delta) / ki == delta) {
097:             _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);
098:         } else {
099:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);
100:         }

155:             } else if ((idelta * V1) / idelta == V1) {
156:                 temp = (idelta * V1) / (V0 * V0);
157:             } else {
158:                 temp = (((delta * V1) / V0) * i) / V0;
159:             }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L22-L26) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L200-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L96-L100), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L155-L159)


```solidity

File: /src/mimswap/periphery/Router.sol

82:         if (useTokenAsQuote) {
83:             _validateDecimals(18, IERC20Metadata(token).decimals());
84:         } else {
85:             _validateDecimals(IERC20Metadata(token).decimals(), 18);
86:         }

327:         if (directions & 1 == 0) {
328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
329:         } else {
330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
331:         }

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

392:         if (directions & 1 == 0) {
393:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
394:         } else {
395:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
396:         }

560:         if ((directions & 1 == 0)) {
561:             amountOut = IMagicLP(path[iterations]).sellBase(to);
562:         } else {
563:             amountOut = IMagicLP(path[iterations]).sellQuote(to);
564:         }

295:         } else if (IMagicLP(lp)._QUOTE_TOKEN_() == address(weth)) {
296:             (tokenAmountOut, ethAmountOut) = IMagicLP(lp).sellShares(
297:                 sharesIn,
298:                 address(this),
299:                 minimumTokenAmount,
300:                 minimumETHAmount,
301:                 "",
302:                 deadline
303:             );
304:         } else {
305:             revert ErrNotETHLP();
306:         }

545:             if (directions & 1 == 0) {
546:                 // Sell base
547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));
548:             } else {
549:                 // Sell quote
550:                 IMagicLP(path[i]).sellQuote(address(path[i + 1]));
551:             }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L82-L86) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L327-L331), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L348-L352), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L379-L383), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L392-L396), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L560-L564), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L295-L306), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L545-L551)


</details>


### [NC&#x2011;29] Imports could be organized more systematically 
The contract used interfaces should be imported first, followed by all other files. The examples below do not follow this layout.


*There are 8 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

9: import {IERC20} from "BoringSolidity/interfaces/IERC20.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L9-L9) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

7: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L7-L7) 


```solidity

File: /src/blast/BlastWrappers.sol

8: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L8-L8) 


```solidity

File: /src/mimswap/MagicLP.sol

11: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L11-L11) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

11: import {IFeeRateImpl} from "../interfaces/IFeeRateModel.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L11-L11) 


```solidity

File: /src/mimswap/periphery/Factory.sol

6: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L6-L6) 


```solidity

File: /src/mimswap/periphery/Router.sol

5: import {IERC20} from "openzeppelin-contracts/interfaces/IERC20.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L5-L5) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

5: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L5-L5) 


</details>


### [NC&#x2011;30] `internal` functions not called by the contract should be removed 
If the functions are required by an interface, the contract should inherit from that interface and use the `override` keyword


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/libraries/BlastYields.sol

60:     function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {

75:     function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L60-L60) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L75-L75)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L43-L43) 


</details>


### [NC&#x2011;31] Large numeric literals should use underscores for readability 



*There are 12 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboardingBoot.sol

15: uint256 constant FEE_RATE = 0.0005 ether; // 0.05%

16: uint256 constant K = 0.00025 ether; // 0.00025, 1.25% price fluctuation, similar to A2000 in curve

17: uint256 constant I = 0.998 ether; // 1 MIM = 0.998 USDB

18: uint256 constant USDB_TO_MIN = 1.002 ether; // 1 USDB = 1.002 MIM


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L15-L15) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L16-L16), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L18-L18)


```solidity

File: /src/mimswap/MagicLP.sol

594:         if (amount <= 1000) {

389:             if (shares <= 2001) {

393:             _mint(address(0), 1001);

394:             shares -= 1001;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L594-L594) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L389-L389), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L393-L393), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L394-L394)


```solidity

File: /src/mimswap/periphery/Router.sol

105:         if (shares <= 2001) {

109:         shares -= 1001;

142:             if (shares <= 2001) {

146:             shares -= 1001;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L105-L105) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L109-L109), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L142-L142), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L146-L146)


</details>


### [NC&#x2011;32] Long functions should be refactored into multiple, smaller, functions 



*There are 7 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L290-L290) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L360-L360)


```solidity

File: /src/mimswap/libraries/Math.sol

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L79-L79) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L131-L131)


```solidity

File: /src/staking/LockingMultiRewards.sol

397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {

479:     function _createLock(address user, uint256 amount) internal {

597:     function _getRewards(address user) internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L397-L397) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L479-L479), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L597-L597)


</details>


### [NC&#x2011;33] Long lines of code 
Usually lines in source code are limited to [80](https://softwareengineering.stackexchange.com/questions/148677/why-is-80-characters-the-standard-limit-for-code-width) characters. Today's screens are much larger so it's reasonable to stretch this in some cases. The solidity style guide recommends a maximumum line length of [120 characters](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#maximum-line-length), so the lines below should be split when they reach that length.


*There are 54 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastGovernor.sol

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L53-L53) 


```solidity

File: /src/blast/BlastMagicLP.sol

53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L53-L53) 


```solidity

File: /src/blast/BlastOnboarding.sol

101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L101-L101) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L123-L123)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L86-L86) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L96-L96)


```solidity

File: /src/mimswap/MagicLP.sol

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L32-L32) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L156-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L170-L170), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L183-L183), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L290-L290), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L310-L310), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L325-L325), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L332-L332), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L347-L347), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L360-L360), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L381-L381), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L402-L402), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L403-L403), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L439-L439)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

34:     function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L34-L34) 


```solidity

File: /src/mimswap/libraries/Math.sol

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L51-L51) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L131-L131), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L184-L184)


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

39:     function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {

55:                     // [Important corner case!] may enter this branch when some precision problem happens. And consequently contribute to negative spare quote amount

65:                 receiveQuoteAmount = backToOneReceiveQuote + _ROneSellBaseToken(state, payBaseAmount - backToOnePayBase);

76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {

96:                 receiveBaseAmount = backToOneReceiveBase + _ROneSellQuoteToken(state, payQuoteAmount - backToOnePayQuote);

129:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);

144:         return Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K);

185:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L39-L39) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L65-L65), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L129-L129), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L144-L144), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L185-L185)


```solidity

File: /src/mimswap/periphery/Factory.sol

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

86:         IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L86-L86)


```solidity

File: /src/mimswap/periphery/Router.sol

88:         clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);

101:         shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

138:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;

169:     ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

199:     ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

251:     function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

523:             uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L88-L88) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L101-L101), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L138-L138), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L169-L169), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L199-L199), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L251-L251), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L523-L523), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L541-L541)


```solidity

File: /src/staking/LockingMultiRewards.sol

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L11-L11) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L109-L109), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L252-L252), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L292-L292), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L322-L322), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L533-L533)


</details>


### [NC&#x2011;34] File is missing NatSpec 



*There are 8 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

0: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L0-L0) 


```solidity

File: /src/blast/BlastGovernor.sol

0: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L0-L0) 


```solidity

File: /src/blast/BlastOnboarding.sol

0: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L0-L0) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

0: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L0-L0) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

0: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L0-L0) 


```solidity

File: /src/blast/libraries/BlastYields.sol

0: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L0-L0) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

0: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L0-L0) 


```solidity

File: /src/mimswap/periphery/Router.sol

0: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L0-L0) 


</details>


### [NC&#x2011;35] Mixed usage of `int`/`uint` with `int256`/`uint256` 
`int256`/`uint256` are the preferred type names (they're what are used for function signatures), so they should be used consistently


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/libraries/DecimalMath.sol

53:             uint p = powFloor(target, e / 2);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L53-L53) 


```solidity

File: /src/staking/LockingMultiRewards.sol

361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L361-L361) 


</details>


### [NC&#x2011;36] Consider using named mappings 
Consider using [named mappings](https://ethereum.stackexchange.com/a/145555) to make it easier to understand the purpose of each mapping


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

21:     mapping(address => bool) public enabledTokens;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L21-L21) 


```solidity

File: /src/blast/BlastMagicLP.sol

21:     mapping(address => bool) public operators;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L21-L21) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

10:     mapping(address => bool) public nativeYieldTokens;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L10-L10) 


</details>


### [NC&#x2011;37] Consider using later versions of solidity for more cappabilities 
Consider using solidity 0.8.18 or later to benefit from multiple things including the named mappings [named mappings](https://ethereum.stackexchange.com/a/145555) to make it easier to understand the purpose of each mapping


*There are 20 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L2-L2) 


```solidity

File: /src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L3-L3) 


```solidity

File: /src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L2-L2) 


```solidity

File: /src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L3-L3) 


```solidity

File: /src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L2-L2) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L2-L2) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L2-L2) 


```solidity

File: /src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L2-L2) 


```solidity

File: /src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L2) 


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L7-L7) 


```solidity

File: /src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L8-L8) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L8-L8) 


```solidity

File: /src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L2-L2) 


```solidity

File: /src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L2-L2) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L2-L2) 


```solidity

File: /src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L2-L2) 


</details>


### [NC&#x2011;38] Public state variables shouldn't have a preceding _ in their name 
Remove the _ from the state variable name, ensure you also refactor where these state variables are internally called


*There are 13 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L70-L70) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L78-L78), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L82-L82)


</details>


### [NC&#x2011;39] Events that mark critical parameter changes should contain both the old and the new value 
This should especially be done if the new value is not required to be different from the old value


*There are 22 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

15:     event LogFeeToChanged(address indexed feeTo);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L15-L15) 


```solidity

File: /src/blast/BlastGovernor.sol

8:     event LogFeeToChanged(address indexed feeTo);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L8-L8) 


```solidity

File: /src/blast/BlastMagicLP.sol

11:     event LogFeeToChanged(address indexed feeTo);

12:     event LogOperatorChanged(address indexed, bool);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L11-L11) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L12-L12)


```solidity

File: /src/blast/BlastOnboarding.sol

67:     event LogBootstrapperChanged(address indexed bootstrapper);

71:     event LogFeeToChanged(address indexed feeTo);

73:     event LogTokenCapChanged(address indexed token, uint256 cap);

74:     event LogStateChange(State state);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L67-L67) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L74-L74)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

37:     event LogReadyChanged(bool ready);

41:     event LogStakingChanged(address indexed staking);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L37-L37) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L41-L41)


```solidity

File: /src/mimswap/MagicLP.sol

34:     event RChange(PMMPricing.RState newRState);

36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L34-L34) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L36-L36)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

14:     event LogImplementationChanged(address indexed implementation);

15:     event LogMaintainerChanged(address indexed maintainer);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L14-L14) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L15-L15)


```solidity

File: /src/mimswap/periphery/Factory.sol

23:     event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);

25:     event LogSetImplementation(address indexed implementation);

26:     event LogSetMaintainer(address indexed newMaintainer);

27:     event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L27-L27)


```solidity

File: /src/staking/LockingMultiRewards.sol

17:     event LogRewardAdded(uint256 reward);

21:     event LogLockIndexChanged(address indexed user, uint256 fromIndex, uint256 toIndex);

26:     event LogRewardsDurationUpdated(address token, uint256 newDuration);

28:     event LogSetMinLockAmount(uint256 previous, uint256 current);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L17-L17) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L28-L28)


</details>


### [NC&#x2011;40] Use of `override` is unnecessary 
Starting with Solidity version [0.8.8](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding), using the `override` keyword when the function solely overrides an interface function, and the function doesn't exist in multiple base contracts, is unnecessary.


*There are 10 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L36-L42) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L98-L98), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L103-L103)


```solidity

File: /src/blast/BlastOnboarding.sol

226:     function _implementation() internal view override returns (address) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L226-L226) 


```solidity

File: /src/mimswap/MagicLP.sol

155:     function name() public view override returns (string memory) {

159:     function symbol() public pure override returns (string memory) {

163:     function decimals() public view override returns (uint8) {

593:     function _mint(address to, uint256 amount) internal override {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L155-L155) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L159-L159), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L163-L163), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L593-L593)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

29:     function decimals() external pure override returns (uint8) {

37:     function latestAnswer() public view override returns (int256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L29-L29) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L37-L37)


</details>


### [NC&#x2011;41] Using `>`/`>=` without specifying an upper bound is unsafe 
There _will_ be breaking changes in future versions of solidity, and at that point your code will no longer be compatable. While you may have the specific version to use in a configuration file, others that include your source files may not.


*There are 20 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L2-L2) 


```solidity

File: /src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L3-L3) 


```solidity

File: /src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L2-L2) 


```solidity

File: /src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L3-L3) 


```solidity

File: /src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L2-L2) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L2-L2) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L2-L2) 


```solidity

File: /src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L2-L2) 


```solidity

File: /src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L2) 


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L7-L7) 


```solidity

File: /src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L8-L8) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L8-L8) 


```solidity

File: /src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L2-L2) 


```solidity

File: /src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L2-L2) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L2-L2) 


```solidity

File: /src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L2-L2) 


</details>


### [NC&#x2011;42] Functions which are either private or internal should have a preceding _ in their name 
Add a preceding underscore to the function name, take care to refactor where there functions are called 


*There are 25 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

103:     function isOwner(address _account) internal view override returns (bool) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L103-L103) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

10:     function configure() internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L10-L10) 


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L20-L20) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L60-L60), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L86-L86)


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L47-L47)


```solidity

File: /src/mimswap/libraries/Math.sol

19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

29:     function sqrt(uint256 x) internal pure returns (uint256 y) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L19-L19) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L29-L29)


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

39:     function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {

76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {

190:     function adjustedTarget(PMMState memory state) internal pure {

203:     function getMidPrice(PMMState memory state) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L39-L39) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L203-L203)


</details>


### [NC&#x2011;43] `public` functions not called by the contract should be declared `external` instead 
Contracts [are allowed](https://docs.soliditylang.org/en/latest/contracts.html#function-overriding) to override their parents' functions and change the visibility from `external` to `public`.


*There are 13 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

228:     function getBaseInput() public view returns (uint256 input) {

232:     function getQuoteInput() public view returns (uint256 input) {

470:     function setParameters(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L228-L228) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L232-L232), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L470)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

57:     function setImplementation(address implementation_) public onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L57) 


```solidity

File: /src/mimswap/periphery/Factory.sol

65:     function predictDeterministicAddress(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L65-L65) 


```solidity

File: /src/staking/LockingMultiRewards.sol

150:     function stake(uint256 amount, bool lock_) public whenNotPaused {

155:     function lock(uint256 amount) public whenNotPaused {

186:     function withdrawWithRewards(uint256 amount) public virtual {

191:     function getRewards() public virtual {

265:     function remainingEpochTime() public view returns (uint256) {

288:     function earned(address user, address rewardToken) public view returns (uint256) {

300:     function addReward(address rewardToken) public onlyOwner {

361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L150-L150) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L155-L155), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L186-L186), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L191-L191), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L265-L265), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L288-L288), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L300-L300), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L361-L361)


</details>


### [NC&#x2011;44] Setters should prevent re-setting of the same value 
This especially problematic when the setter also emits the same value, which may be confusing to offline parsers


*There are 12 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

//@audit `feeTo` and `feeTo_` are never checked for the same value setting
72:     function setFeeTo(address feeTo_) external onlyOwner {
73:         if (feeTo_ == address(0)) {
74:             revert ErrZeroAddress();
75:         }
76: 
77:         feeTo = feeTo_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L77) 


```solidity

File: /src/blast/BlastGovernor.sol

//@audit `feeTo` and `_feeTo` are never checked for the same value setting
40:     function setFeeTo(address _feeTo) external onlyOwner {
41:         if(_feeTo == address(0)) {
42:             revert ErrZeroAddress();
43:         }
44:         
45:         feeTo = _feeTo;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L40-L45) 


```solidity

File: /src/blast/BlastMagicLP.sol

//@audit `feeTo` and `feeTo_` are never checked for the same value setting
80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
81:         if (feeTo_ == address(0)) {
82:             revert ErrZeroAddress();
83:         }
84: 
85:         feeTo = feeTo_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L80-L85) 


```solidity

File: /src/blast/BlastOnboarding.sol

//@audit `feeTo` and `feeTo_` are never checked for the same value setting
147:     function setFeeTo(address feeTo_) external onlyOwner {
148:         if (feeTo_ == address(0)) {
149:             revert ErrZeroAddress();
150:         }
151: 
152:         feeTo = feeTo_;

//@audit `bootstrapper` and `bootstrapper_` are never checked for the same value setting
190:     function setBootstrapper(address bootstrapper_) external onlyOwner {
191:         bootstrapper = bootstrapper_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L147-L152) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L191)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

//@audit `staking` and `_staking` are never checked for the same value setting
137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {
138:         if (ready) {
139:             revert ErrCannotChangeOnceReady();
140:         }
141: 
142:         staking = _staking;

//@audit `ready` and `_ready` are never checked for the same value setting
146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
147:         ready = _ready;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L142) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L147)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

//@audit `maintainer` and `maintainer_` are never checked for the same value setting
46:     function setMaintainer(address maintainer_) external onlyOwner {
47:         if (maintainer_ == address(0)) {
48:             revert ErrZeroAddress();
49:         }
50: 
51:         maintainer = maintainer_;

//@audit `implementation` and `implementation_` are never checked for the same value setting
57:     function setImplementation(address implementation_) public onlyOwner {
58:         implementation = implementation_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L46-L51) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L58)


```solidity

File: /src/mimswap/periphery/Factory.sol

//@audit `implementation` and `implementation_` are never checked for the same value setting
096:     function setLpImplementation(address implementation_) external onlyOwner {
097:         if (implementation_ == address(0)) {
098:             revert ErrZeroAddress();
099:         }
100: 
101:         implementation = implementation_;

//@audit `maintainerFeeRateModel` and `maintainerFeeRateModel_` are never checked for the same value setting
105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
106:         if (address(maintainerFeeRateModel_) == address(0)) {
107:             revert ErrZeroAddress();
108:         }
109: 
110:         maintainerFeeRateModel = maintainerFeeRateModel_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L96-L101) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L110)


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit `minLockAmount` and `_minLockAmount` are never checked for the same value setting
317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
318:         emit LogSetMinLockAmount(minLockAmount, _minLockAmount);
319:         minLockAmount = _minLockAmount;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L317-L319) 


</details>


### [NC&#x2011;45] NatSpec `@return` argument is missing 



*There are 21 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

// @audit the @return is missing
OPERATORS


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L52-L1) 


```solidity

File: /src/blast/BlastGovernor.sol

// @audit the @return is missing
OPERATORS


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L28-L1) 


```solidity

File: /src/blast/BlastMagicLP.sol

// @audit the @return is missing
VIEWS

// @audit the @return is missing
OPERATORS / CLONES ONLY


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L39-L1) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L47-L1)


```solidity

File: /src/blast/BlastOnboarding.sol

// @audit the @return is missing
PROXY IMPLEMENTATION


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L226-L1) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

// @audit the @return is missing
PUBLIC

// @audit the @return is missing
VIEWS

// @audit the @return is missing
ADMIN

// @audit the @return is missing
INTERNALS


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L55-L1) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L78-L1), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L96-L1), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L155-L1)


```solidity

File: /src/mimswap/MagicLP.sol

// @audit the @return is missing
VIEWS

// @audit the @return is missing
TRADE FUNCTIONS

// @audit the @return is missing
BUY & SELL SHARES

// @audit the @return is missing
INTERNALS


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L155-L1) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L244-L1), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L360-L1), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L528-L1)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

// @audit the @return is missing
VIEWS


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L34-L1) 


```solidity

File: /src/mimswap/periphery/Factory.sol

// @audit the @return is missing
VIEWS

// @audit the @return is missing
PUBLIC


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L53-L1) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L65-L1)


```solidity

File: /src/mimswap/periphery/Router.sol

// @audit the @return is missing
INTERNALS

// @audit the @return is missing
Adapted from: https://github.com/DODOEX/contractV2/blob/main/contracts/SmartRoute/proxies/DODODspProxy.sol
 Copyright 2020 DODO ZOO. Licensed under Apache-2.0.


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L499-L1) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L509-L1)


```solidity

File: /src/staking/LockingMultiRewards.sol

// @audit the @return is missing
VIEWS

// @audit the @return is missing
@dev Calculates when the next unlock event will occur given the current epoch.
 It ensures that the unlock timing coincides with the intervals at which rewards are distributed.
 If the current time is within an ongoing reward interval, the function establishes the
 unlock period to begin at the next epoch.
 So, if you stake at week 1 + 4 days, you will be able to unlock at the end of week 14.

// @audit the @return is missing
@dev Update the global accumulated rewards from the last update to this point,
 in relation with the `totalSupply`
 The idea is to allow everyone that are currently part of that supply to get their allocated
 reward share.
 Each user's reward share is taking in account when `rewards[user][token] = _earned(...)`
 is called. And only updated when a user is interacting with `stake`, `lock`, `withdraw`
 or `getRewards`.
 Otherwise, if it's yet-to-be-updated, it's going to get considered as part of the pending
 yet-to-receive rewards in the `earned` function.


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L199-L1) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L253-L1), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L528-L1)


</details>


### [NC&#x2011;46] Consider using `SafeTransferLib.safeTransferETH()` or `Address.sendValue()` for clearer semantic meaning 
These Functions indicate their purpose with their name more clearly than using low-level calls.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastGovernor.sol

54:         (success, result) = to.call{value: value}(data);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L54-L54) 


</details>


### [NC&#x2011;47] Large multiples of ten should use scientific notation (e.g. `1e6`) rather than decimal literals (e.g. `1000000`), for readability 
While the compiler knows to optimize away the exponentiation, it's still better coding practice to use idioms that do not require compiler optimization, if they exist


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

//@audit `1000`
594:         if (amount <= 1000) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L594-L594) 


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit `10_000`
78:     uint256 private constant BIPS = 10_000;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L78-L78) 


</details>


### [NC&#x2011;48] Misplaced SPDX identifier 
The SPDX identifier should be on the very first line of each source file.


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

3:     Copyright 2020 DODO ZOO.


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L3-L3) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

3:     Copyright 2020 DODO ZOO.


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L3-L3) 


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

3:     Copyright 2020 DODO ZOO.


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L3-L3) 


```solidity

File: /src/mimswap/libraries/Math.sol

3:     Copyright 2020 DODO ZOO.


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L3-L3) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

3:     Copyright 2020 DODO ZOO.


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L3-L3) 


</details>


### [NC&#x2011;49] Empty `receive()`/`payable fallback()` function does not authorize requests 
If the intention is for the Ether to be used, the function should call another function, otherwise it should revert (e.g. `require(msg.sender == address(weth))`). Having no access control on the function means that someone may send Ether to the contract, and have no way to get anything back out, which is a loss of funds. If the concern is having to spend a small amount of gas to check the sender against an immutable address, the code should at least have a function to rescue unused Ether.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastGovernor.sol

13:     receive() external payable {}
14: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L13-L14) 


```solidity

File: /src/mimswap/periphery/Router.sol

36:     receive() external payable {}
37: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L36-L37) 


</details>


### [NC&#x2011;50] State variables should have `Natspec` comments 
Consider adding some `Natspec` comments on critical state variables to explain what they are supposed to do: this will help for future code reviews.


*There are 83 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

//@audit registry need comments
20:     BlastTokenRegistry public immutable registry;

//@audit enabledTokens need comments
21:     mapping(address => bool) public enabledTokens;

//@audit feeTo need comments
22:     address public feeTo;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L20-L20) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L22-L22)


```solidity

File: /src/blast/BlastGovernor.sol

//@audit feeTo need comments
11:     address public feeTo;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L11-L11) 


```solidity

File: /src/blast/BlastMagicLP.sol

//@audit registry need comments
17:     BlastTokenRegistry public immutable registry;

//@audit operators need comments
21:     mapping(address => bool) public operators;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L17-L17) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L21-L21)


```solidity

File: /src/blast/BlastOnboarding.sol

//@audit state need comments
30:     State public state;

//@audit bootstrapper need comments
31:     address public bootstrapper;

//@audit feeTo need comments
32:     address public feeTo;

//@audit registry need comments
33:     BlastTokenRegistry public registry;

//@audit supportedTokens need comments
36:     mapping(address token => bool) public supportedTokens;

//@audit totals need comments
37:     mapping(address token => Balances) public totals;

//@audit caps need comments
38:     mapping(address token => uint256 cap) public caps;

//@audit balances need comments
41:     mapping(address user => mapping(address token => Balances)) public balances;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L30-L30) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L41-L41)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

//@audit pool need comments
24:     address public pool;

//@audit router need comments
25:     Router public router;

//@audit factory need comments
26:     IFactory public factory;

//@audit totalPoolShares need comments
27:     uint256 public totalPoolShares;

//@audit ready need comments
28:     bool public ready;

//@audit staking need comments
29:     LockingMultiRewards public staking;

//@audit claimed need comments
30:     mapping(address user => bool claimed) public claimed;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L24-L24) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L30-L30)


```solidity

File: /src/blast/BlastTokenRegistry.sol

//@audit nativeYieldTokens need comments
10:     mapping(address => bool) public nativeYieldTokens;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L10-L10) 


```solidity

File: /src/blast/BlastWrappers.sol

//@audit _governor need comments
45:     address private immutable _governor;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L45-L45) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

//@audit BLAST_POINTS_OPERATOR need comments
7:     address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;

//@audit BLAST_POINTS need comments
8:     IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L8-L8)


```solidity

File: /src/blast/libraries/BlastYields.sol

//@audit BLAST_YIELD_PRECOMPILE need comments
14:     IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L14-L14) 


```solidity

File: /src/mimswap/MagicLP.sol

//@audit implementation need comments
61:     MagicLP public immutable implementation;

//@audit MAX_I need comments
63:     uint256 public constant MAX_I = 10 ** 36;

//@audit MAX_K need comments
64:     uint256 public constant MAX_K = 10 ** 18;

//@audit MIN_LP_FEE_RATE need comments
65:     uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%

//@audit MAX_LP_FEE_RATE need comments
66:     uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%

//@audit _INITIALIZED_ need comments
68:     bool internal _INITIALIZED_;

//@audit _BASE_TOKEN_ need comments
70:     address public _BASE_TOKEN_;

//@audit _QUOTE_TOKEN_ need comments
71:     address public _QUOTE_TOKEN_;

//@audit _BASE_RESERVE_ need comments
72:     uint112 public _BASE_RESERVE_;

//@audit _QUOTE_RESERVE_ need comments
73:     uint112 public _QUOTE_RESERVE_;

//@audit _BLOCK_TIMESTAMP_LAST_ need comments
74:     uint32 public _BLOCK_TIMESTAMP_LAST_;

//@audit _BASE_PRICE_CUMULATIVE_LAST_ need comments
75:     uint256 public _BASE_PRICE_CUMULATIVE_LAST_;

//@audit _BASE_TARGET_ need comments
76:     uint112 public _BASE_TARGET_;

//@audit _QUOTE_TARGET_ need comments
77:     uint112 public _QUOTE_TARGET_;

//@audit _RState_ need comments
78:     uint32 public _RState_;

//@audit _MT_FEE_RATE_MODEL_ need comments
79:     IFeeRateModel public _MT_FEE_RATE_MODEL_;

//@audit _LP_FEE_RATE_ need comments
80:     uint256 public _LP_FEE_RATE_;

//@audit _K_ need comments
81:     uint256 public _K_;

//@audit _I_ need comments
82:     uint256 public _I_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L61-L61) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L63-L63), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L65-L65), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L66-L66), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L78-L78), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L82-L82)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

//@audit maintainer need comments
19:     address public maintainer;

//@audit implementation need comments
20:     address public implementation;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L19-L19) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L20-L20)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

//@audit ONE need comments
20:     uint256 internal constant ONE = 10 ** 18;

//@audit ONE2 need comments
21:     uint256 internal constant ONE2 = 10 ** 36;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L20-L20) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L21-L21)


```solidity

File: /src/mimswap/periphery/Factory.sol

//@audit implementation need comments
32:     address public implementation;

//@audit maintainerFeeRateModel need comments
33:     IFeeRateModel public maintainerFeeRateModel;

//@audit pools need comments
35:     mapping(address base => mapping(address quote => address[] pools)) public pools;

//@audit userPools need comments
36:     mapping(address creator => address[] pools) public userPools;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L32-L32) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L36-L36)


```solidity

File: /src/mimswap/periphery/Router.sol

//@audit MAX_BASE_QUOTE_DECIMALS_DIFFERENCE need comments
31:     uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;

//@audit weth need comments
33:     IWETH public immutable weth;

//@audit factory need comments
34:     IFactory public immutable factory;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L31-L31) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L34-L34)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

//@audit pair need comments
10:     IMagicLP public immutable pair;

//@audit baseOracle need comments
11:     IAggregator public immutable baseOracle;

//@audit quoteOracle need comments
12:     IAggregator public immutable quoteOracle;

//@audit baseDecimals need comments
13:     uint8 public immutable baseDecimals;

//@audit quoteDecimals need comments
14:     uint8 public immutable quoteDecimals;

//@audit WAD need comments
16:     uint256 public constant WAD = 18;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L10-L10) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L11-L11), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L16-L16)


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit BIPS need comments
78:     uint256 private constant BIPS = 10_000;

//@audit MAX_NUM_REWARDS need comments
79:     uint256 private constant MAX_NUM_REWARDS = 5;

//@audit MIN_LOCK_DURATION need comments
80:     uint256 private constant MIN_LOCK_DURATION = 1 weeks;

//@audit MIN_REWARDS_DURATION need comments
81:     uint256 private constant MIN_REWARDS_DURATION = 1 days;

//@audit maxLocks need comments
83:     uint256 public immutable maxLocks;

//@audit lockingBoostMultiplerInBips need comments
84:     uint256 public immutable lockingBoostMultiplerInBips;

//@audit rewardsDuration need comments
85:     uint256 public immutable rewardsDuration;

//@audit lockDuration need comments
86:     uint256 public immutable lockDuration;

//@audit stakingToken need comments
87:     address public immutable stakingToken;

//@audit _rewardData need comments
89:     mapping(address token => Reward info) private _rewardData;

//@audit _balances need comments
90:     mapping(address user => Balances balances) private _balances;

//@audit _userLocks need comments
91:     mapping(address user => LockedBalance[] locks) private _userLocks;

//@audit _userRewardLock need comments
92:     mapping(address user => RewardLock rewardLock) private _userRewardLock;

//@audit userRewardPerTokenPaid need comments
94:     mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;

//@audit rewards need comments
95:     mapping(address user => mapping(address token => uint256 amount)) public rewards;

//@audit lastLockIndex need comments
96:     mapping(address user => uint256 index) public lastLockIndex;

//@audit rewardTokens need comments
98:     address[] public rewardTokens;

//@audit lockedSupply need comments
100:     uint256 public lockedSupply; // all locked boosted deposits

//@audit unlockedSupply need comments
101:     uint256 public unlockedSupply; // all unlocked unboosted deposits

//@audit minLockAmount need comments
102:     uint256 public minLockAmount; // minimum amount allowed to lock

//@audit stakingTokenBalance need comments
103:     uint256 public stakingTokenBalance; // total staking token balance


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L78-L78) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L83-L83), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L85-L85), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L86-L86), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L87-L87), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L89-L89), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L90-L90), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L91-L91), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L92-L92), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L94-L94), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L95-L95), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L98-L98), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L100-L100), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L101-L101), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L102-L102), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L103-L103)


</details>


### [NC&#x2011;51] Contracts should have full test coverage 
While 100% code coverage does not guarantee that there are no bugs, it often will catch easy-to-find bugs, and will ensure that there are fewer regressions when the code invariably has to be modified. Furthermore, in order to get full coverage, code authors will often have to re-organize their code so that it is more modular, so that each component can be tested separately, which reduces interdependencies between modules and layers, and makes for code that is easier to reason about and audit.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

@audit Multiple files
1: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L1-L1) 


</details>


### [NC&#x2011;52] [NatSpec] Natspec `@title` is missing from `contract` 



*There are 21 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

6: contract BlastDapp {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L6-L6) 


```solidity

File: /src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L13-L13) 


```solidity

File: /src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L7-L7) 


```solidity

File: /src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L10-L10) 


```solidity

File: /src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L64-L64)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

33: /// @dev Functions are postfixed with the version number to avoid collisions
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L33-L34)


```solidity

File: /src/blast/BlastTokenRegistry.sol

6: contract BlastTokenRegistry is Owned {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L6-L6) 


```solidity

File: /src/blast/BlastWrappers.sol

19: contract BlastMIMSwapRouter is Router {

28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L19-L19) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L42-L42)


```solidity

File: /src/blast/libraries/BlastPoints.sol

6: library BlastPoints {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L6-L6) 


```solidity

File: /src/blast/libraries/BlastYields.sol

7: library BlastYields {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L7-L7) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

13: contract FeeRateModel is Owned {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L13-L13) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

7: contract FeeRateModelImpl {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L7-L7) 


```solidity

File: /src/mimswap/libraries/Math.sol

12: /**
13:  * @author Adapted from https://github.com/DODOEX/contractV2/blob/main/contracts/lib/Math.sol
14:  * @notice Functions for complex calculating. Including ONE Integration and TWO Quadratic solutions
15:  */


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L12-L15) 


```solidity

File: /src/mimswap/periphery/Factory.sol

10: /// @notice Create and register MagicLP pools
11: contract Factory is Owned {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L10-L11) 


```solidity

File: /src/mimswap/periphery/Router.sol

12: contract Router {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L12-L12) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

9: contract MagicLpAggregator is IAggregator {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L9-L9) 


```solidity

File: /src/staking/LockingMultiRewards.sol

09: /// @notice A staking contract that distributes multiple rewards to stakers.
10: /// Stakers can lock their tokens for a period of time to get a boost on their rewards.
11: /// @author Based from Curve Finance's MultiRewards contract https://github.com/curvefi/multi-rewards/blob/master/contracts/MultiRewards.sol
12: /// @author Based from Ellipsis Finance's EpsStaker https://github.com/ellipsis-finance/ellipsis/blob/master/contracts/EpsStaker.sol
13: /// @author Based from Convex Finance's CvxLockerV2 https://github.com/convex-eth/platform/blob/main/contracts/contracts/CvxLockerV2.sol
14: contract LockingMultiRewards is OperatableV2, Pausable {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L9-L14) 


</details>


### [NC&#x2011;53] Top level pragma declarations should be separated by two blank lines 



*There are 32 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;
3: 
4: import {BlastPoints} from "/blast/libraries/BlastPoints.sol";

4: import {BlastPoints} from "/blast/libraries/BlastPoints.sol";
5: 
6: contract BlastDapp {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L2-L4) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L4-L6)


```solidity

File: /src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;
4: 
5: import {DegenBox} from "/DegenBox.sol";

11: import {IWETH} from "interfaces/IWETH.sol";
12: 
13: contract BlastBox is DegenBox, OperatableV3 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L3-L5) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L11-L13)


```solidity

File: /src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;
3: 
4: import {BlastYields} from "/blast/libraries/BlastYields.sol";

5: import {OperatableV2} from "mixins/OperatableV2.sol";
6: 
7: contract BlastGovernor is OperatableV2 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L2-L4) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L5-L7)


```solidity

File: /src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;
4: 
5: import {MagicLP} from "/mimswap/MagicLP.sol";

08: import {BlastTokenRegistry} from "/blast/BlastTokenRegistry.sol";
09: 
10: contract BlastMagicLP is MagicLP {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L3-L5) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L8-L10)


```solidity

File: /src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;
3: 
4: import {Owned} from "solmate/auth/Owned.sol";

10: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";
11: 
12: contract BlastOnboardingData is Owned, Pausable {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L2-L4) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L10-L12)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;
3: 
4: import {BlastOnboarding} from "/blast/BlastOnboarding.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L2-L4) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;
3: 
4: import {Owned} from "solmate/auth/Owned.sol";

4: import {Owned} from "solmate/auth/Owned.sol";
5: 
6: contract BlastTokenRegistry is Owned {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L2-L4) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L4-L6)


```solidity

File: /src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;
3: 
4: import {IERC20} from "BoringSolidity/interfaces/IERC20.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L4) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;
3: 
4: import {IBlastPoints} from "interfaces/IBlast.sol";

4: import {IBlastPoints} from "interfaces/IBlast.sol";
5: 
6: library BlastPoints {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L2-L4) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L4-L6)


```solidity

File: /src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;
3: 
4: import {IBlast, IERC20Rebasing, YieldMode, GasMode} from "interfaces/IBlast.sol";

5: import {Address} from "openzeppelin-contracts/utils/Address.sol";
6: 
7: library BlastYields {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L2-L4) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L5-L7)


```solidity

File: /src/mimswap/MagicLP.sol

08: pragma solidity >=0.8.0;
09: 
10: import {Owned} from "solmate/auth/Owned.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L8-L10) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

08: pragma solidity >=0.8.0;
09: 
10: import {Owned} from "solmate/auth/Owned.sol";

11: import {IFeeRateImpl} from "../interfaces/IFeeRateModel.sol";
12: 
13: contract FeeRateModel is Owned {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L8-L10) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L11-L13)


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;
3: 
4: import {IFeeRateImpl} from "../interfaces/IFeeRateModel.sol";

5: import {Math} from "/mimswap/libraries/Math.sol";
6: 
7: contract FeeRateModelImpl {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L4) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L5-L7)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;
8: 
9: import {Math} from "/mimswap/libraries/Math.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L7-L9) 


```solidity

File: /src/mimswap/libraries/Math.sol

08: pragma solidity >=0.8.0;
09: 
10: import {DecimalMath} from "/mimswap/libraries/DecimalMath.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L8-L10) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

08: pragma solidity >=0.8.0;
09: 
10: import {DecimalMath} from "/mimswap/libraries/DecimalMath.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L8-L10) 


```solidity

File: /src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;
3: 
4: import {Owned} from "solmate/auth/Owned.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L2-L4) 


```solidity

File: /src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;
3: 
4: import {SafeTransferLib} from "solady/utils/SafeTransferLib.sol";

10: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
11: 
12: contract Router {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L2-L4) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L10-L12)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;
3: 
4: import {FixedPointMathLib} from "solady/utils/FixedPointMathLib.sol";

7: import {IMagicLP} from "/mimswap/interfaces/IMagicLP.sol";
8: 
9: contract MagicLpAggregator is IAggregator {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L2-L4) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L7-L9)


```solidity

File: /src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;
3: 
4: import {OperatableV2} from "mixins/OperatableV2.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L2-L4) 


</details>


### [NC&#x2011;54] Critical functions should be a two step procedure 
Critical functions in Solidity contracts should follow a two-step procedure to enhance security, minimize human error, and ensure proper access control. By dividing sensitive operations into distinct phases, such as initiation and confirmation, developers can introduce a safeguard against unintended actions or unauthorized access.


*There are 27 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

72:     function setFeeTo(address feeTo_) external onlyOwner {

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L72) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L81-L81)


```solidity

File: /src/blast/BlastGovernor.sol

40:     function setFeeTo(address _feeTo) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L40-L40) 


```solidity

File: /src/blast/BlastMagicLP.sol

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {

80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L64-L64) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L89-L89), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L89-L89)


```solidity

File: /src/blast/BlastOnboarding.sol

147:     function setFeeTo(address feeTo_) external onlyOwner {

175:     function setTokenSupported(address token, bool supported) external onlyOwner {

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L147-L147) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L190)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L137) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L146), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L146)


```solidity

File: /src/blast/BlastTokenRegistry.sol

14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L14-L14) 


```solidity

File: /src/mimswap/MagicLP.sol

470:     function setParameters(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L470) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

46:     function setMaintainer(address maintainer_) external onlyOwner {

57:     function setImplementation(address implementation_) public onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L46-L46) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L57)


```solidity

File: /src/mimswap/periphery/Factory.sol

96:     function setLpImplementation(address implementation_) external onlyOwner {

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

116:     function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {

120:     function removePool(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L96-L96) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L105), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L116-L116), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L120)


```solidity

File: /src/staking/LockingMultiRewards.sol

300:     function addReward(address rewardToken) public onlyOwner {

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L300-L300) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L317-L317)


</details>


### [NC&#x2011;55] uint variables should have the bit size defined explicitly 
Instead of using uint to declare uint258, explicitly define uint258 to ensure there is no confusion


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit `minRemainingTime`
361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L361-L361) 


</details>


### [NC&#x2011;56] `2**<n> - 1` should be re-written as `type(uint<n>).max` 
Earlier versions of solidity can use `uint<n>(-1)` instead. Expressions not including the `- 1` can often be re-written to accomodate the change (e.g. by using a `>` rather than a `>=`, which will also save some gas)


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

546:         uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L125-L125) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L546-L546)


</details>


### [NC&#x2011;57] Uncommented fields in a struct 
Consider adding comments for all the fields in a struct to improve the readability of the codebase.


*There are 5 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

//@audit Add explanational comments to the following items `unlocked`, `locked`, `total`, 
24:     struct Balances {
25:         uint256 unlocked;
26:         uint256 locked;
27:         uint256 total;
28:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L24-L28) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

//@audit Add explanational comments to the following items `K`, `Q`, `B0`, `Q0`, `R`, 
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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L27-L35) 


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit Add explanational comments to the following items `periodFinish`, `rewardRate`, `rewardPerTokenStored`, `exists`, `lastUpdateTime`, 
50:     struct Reward {
51:         uint256 periodFinish;
52:         uint256 rewardRate;
53:         uint256 rewardPerTokenStored;
54:         bool exists;
55:         uint248 lastUpdateTime;
56:     }

//@audit Add explanational comments to the following items `unlockTime`, 
63:     struct LockedBalance {
64:         uint256 amount;
65:         uint256 unlockTime;
66:     }

//@audit Add explanational comments to the following items `items`, `unlockTime`, 
73:     struct RewardLock {
74:         RewardLockItem[] items;
75:         uint256 unlockTime;
76:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L50-L56) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L63-L66), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L73-L76)


</details>


### [NC&#x2011;58] Using underscore at the end of variable name 
The use of underscore at the end of the variable name is uncommon and also suggests that the variable name was not completely changed. Consider refactoring variableName_ to variableName.


*There are 98 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

72:     function setFeeTo(address feeTo_) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L24-L24) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L72)


```solidity

File: /src/blast/BlastGovernor.sol

15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L15-L15) 


```solidity

File: /src/blast/BlastMagicLP.sol

23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {

48:         address feeTo_ = BlastMagicLP(address(implementation)).feeTo();

54:         address feeTo_ = BlastMagicLP(address(implementation)).feeTo();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L54-L54)


```solidity

File: /src/blast/BlastOnboarding.sol

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {

101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

147:     function setFeeTo(address feeTo_) external onlyOwner {

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L84-L84) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L101-L101), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L147-L147), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L190)


```solidity

File: /src/blast/BlastWrappers.sol

20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

30:         address implementation_,

31:         IFeeRateModel maintainerFeeRateModel_,

32:         address owner_,

33:         address governor_

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L20-L20) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L47-L47)


```solidity

File: /src/blast/libraries/BlastYields.sol

29:     function configureDefaultClaimables(address governor_) internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L29-L29) 


```solidity

File: /src/mimswap/MagicLP.sol

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

84:     constructor(address owner_) Owned(owner_) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L68-L68) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L78-L78), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L82-L82), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L84-L84)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

22:     constructor(address maintainer_, address owner_) Owned(owner_) {

22:     constructor(address maintainer_, address owner_) Owned(owner_) {

46:     function setMaintainer(address maintainer_) external onlyOwner {

57:     function setImplementation(address implementation_) public onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L22-L22) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L57)


```solidity

File: /src/mimswap/periphery/Factory.sol

13:         address clone_,

14:         address indexed baseToken_,

15:         address indexed quoteToken_,

16:         address indexed creator_,

17:         uint256 lpFeeRate_,

19:         uint256 i_,

20:         uint256 k_

38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

67:         address baseToken_,

68:         address quoteToken_,

69:         uint256 lpFeeRate_,

70:         uint256 i_,

71:         uint256 k_

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

96:     function setLpImplementation(address implementation_) external onlyOwner {

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

156:         address sender_,

157:         address baseToken_,

158:         address quoteToken_,

159:         uint256 lpFeeRate_,

160:         uint256 i_,

161:         uint256 k_


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L13-L13) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L16-L16), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L67-L67), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L69-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L105), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L156-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L157-L157), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L158-L158), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L159-L159), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L160-L160), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L161-L161)


```solidity

File: /src/mimswap/periphery/Router.sol

38:     constructor(IWETH weth_, IFactory factory_) {

38:     constructor(IWETH weth_, IFactory factory_) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L38-L38) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L38-L38)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {

21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {

21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L21-L21) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L21-L21)


```solidity

File: /src/staking/LockingMultiRewards.sol

150:     function stake(uint256 amount, bool lock_) public whenNotPaused {

277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

349:     function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {

458:     function _stakeFor(address account, uint256 amount, bool lock_) internal {

528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

529:         uint256 lastTimeRewardApplicable_ = lastTimeRewardApplicable(token_);

545:         uint256 totalSupply_ = totalSupply();

559:         uint256 totalSupply_ = totalSupply();

573:         uint256 totalSupply_ = totalSupply();

577:             uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L150-L150) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L292-L292), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L292-L292), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L349-L349), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L458-L458), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L528-L528), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L528-L528), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L528-L528), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L529-L529), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L545-L545), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L559-L559), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L573-L573), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L577-L577)


</details>


### [NC&#x2011;59] Event is missing `indexed` fields 
Index event fields make the field more quickly accessible to off-chain tools that parse events. However, note that each index field costs extra gas during emission, so it's not necessarily best to index the maximum allowed per event (three fields). Each event should use three indexed fields if there are three or more fields, and gas usage is not particularly of concern for the events in question. If there are fewer than three fields, all of the fields should be indexed.


*There are 39 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

14:     event LogTokenDepositEnabled(address indexed token, bool enabled);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L14-L14) 


```solidity

File: /src/blast/BlastMagicLP.sol

12:     event LogOperatorChanged(address indexed, bool);

13:     event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L13-L13)


```solidity

File: /src/blast/BlastOnboarding.sol

68:     event LogTokenSupported(address indexed token, bool supported);

69:     event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);

70:     event LogLock(address indexed user, address indexed token, uint256 amount);

72:     event LogWithdraw(address indexed user, address indexed token, uint256 amount);

73:     event LogTokenCapChanged(address indexed token, uint256 cap);

74:     event LogStateChange(State state);

75:     event LogTokenRescue(address indexed token, address indexed to, uint256 amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L68-L68) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L69-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L75-L75)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

37:     event LogReadyChanged(bool ready);

38:     event LogClaimed(address indexed user, uint256 shares, bool lock);

40:     event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L37-L37) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L40-L40)


```solidity

File: /src/blast/BlastTokenRegistry.sol

7:     event LogNativeYieldTokenEnabled(address indexed token, bool enabled);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L7-L7) 


```solidity

File: /src/blast/libraries/BlastYields.sol

8:     event LogBlastGasClaimed(address indexed recipient, uint256 amount);

9:     event LogBlastETHClaimed(address indexed recipient, uint256 amount);

10:     event LogBlastTokenClaimed(address indexed recipient, address indexed token, uint256 amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L8-L8) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L9-L9), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L10-L10)


```solidity

File: /src/mimswap/MagicLP.sol

30:     event BuyShares(address to, uint256 increaseShares, uint256 totalShares);

31:     event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);

32:     event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);

33:     event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);

34:     event RChange(PMMPricing.RState newRState);

35:     event TokenRescue(address indexed token, address to, uint256 amount);

36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L30-L30) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L36-L36)


```solidity

File: /src/mimswap/periphery/Factory.sol

23:     event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);

24:     event LogPoolRemoved(address pool);

27:     event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L27-L27)


```solidity

File: /src/staking/LockingMultiRewards.sol

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L17-L17) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L28-L28)


</details>


### [NC&#x2011;60] Unused `error` definition 
Note that there may be cases where an error superficially appears to be used, but this is only because there are multiple definitions of the error in different files. In such cases, the error definition should be moved into a separate file. The instances below are the unused definitions.


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboardingBoot.sol

46:     error ErrWrongFeeRateModel();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L46-L46) 


```solidity

File: /src/mimswap/MagicLP.sol

43:     error ErrInvalidSignature();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L43-L43) 


```solidity

File: /src/mimswap/periphery/Router.sol

21:     error ErrBadPath();

27:     error ErrInvalidQuoteTarget();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L21-L21) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L27-L27)


```solidity

File: /src/staking/LockingMultiRewards.sol

34:     error ErrNotExpired();

35:     error ErrInvalidUser();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L34-L34) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L35-L35)


</details>


### [NC&#x2011;61] Unused `event` definition 
The following events are never used, consider to remove them.


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastMagicLP.sol

//@audit LogYieldClaimed is never used
13:     event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L13-L13) 


```solidity

File: /src/mimswap/periphery/Factory.sol

//@audit LogSetMaintainer is never used
26:     event LogSetMaintainer(address indexed newMaintainer);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L26-L26) 


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit LogRewardsDurationUpdated is never used
26:     event LogRewardsDurationUpdated(address token, uint256 newDuration);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L26-L26) 


</details>


### [NC&#x2011;62] Unused Import 
Some files/Items are imported but never used


*There are 7 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

//@audit `IWETH` is not used
11: import {IWETH} from "interfaces/IWETH.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L11-L11) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

//@audit `IFeeRateModel` is not used
7: import {IFeeRateModel} from "/mimswap/interfaces/IFeeRateModel.sol";

//@audit `DecimalMath` is not used
10: import {DecimalMath} from "/mimswap/libraries/DecimalMath.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L10-L10)


```solidity

File: /src/mimswap/MagicLP.sol

//@audit `IWETH` is not used
21: import {IWETH} from "interfaces/IWETH.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L21-L21) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

//@audit `IFeeRateImpl` is not used
4: import {IFeeRateImpl} from "../interfaces/IFeeRateModel.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L4-L4) 


```solidity

File: /src/mimswap/periphery/Factory.sol

//@audit `MagicLP` is not used
8: import {MagicLP} from "/mimswap/MagicLP.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L8-L8) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

//@audit `FixedPointMathLib` is not used
4: import {FixedPointMathLib} from "solady/utils/FixedPointMathLib.sol";


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L4-L4) 


</details>


### [NC&#x2011;63] Missing upgradability functionality 
At the begining of a project, there is always the need to modify of add something to the source code especialy if any vulnerability is discovered. Therefore, having such system is crusial at least at the first stages of the project


*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

6: contract BlastDapp {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L6-L6) 


```solidity

File: /src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L13-L13) 


```solidity

File: /src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L7-L7) 


```solidity

File: /src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L10-L10) 


</details>


### [NC&#x2011;64] Constants should be defined rather than using magic numbers 
Even [assembly](https://github.com/code-423n4/2022-05-opensea-seaport/blob/9d7ce4d08bf3c3010304a0476a785c70c0e90ae7/contracts/lib/TokenTransferrer.sol#L35-L39) can benefit from using readable constants instead of hex/numeric literals


*There are 25 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboardingBoot.sol

//@audit Try to make a `constant` with `30_000` value
117:         staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));

//@audit Try to make a `constant` with `7` value
117:         staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));

//@audit Try to make a `constant` with `13` value
117:         staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L117-L117) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L117-L117), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L117-L117)


```solidity

File: /src/mimswap/MagicLP.sol

//@audit Try to make a `constant` with `32` value
125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

//@audit Try to make a `constant` with `2001` value
389:             if (shares <= 2001) {

//@audit Try to make a `constant` with `1001` value
393:             _mint(address(0), 1001);

//@audit Try to make a `constant` with `1001` value
394:             shares -= 1001;

//@audit Try to make a `constant` with `32` value
546:         uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);

//@audit Try to make a `constant` with `1000` value
594:         if (amount <= 1000) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L125-L125) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L389-L389), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L393-L393), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L394-L394), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L546-L546), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L594-L594)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

//@audit Try to make a `constant` with `10` value
49:             return 10 ** 18;

//@audit Try to make a `constant` with `18` value
49:             return 10 ** 18;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L49-L49) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L49-L49)


```solidity

File: /src/mimswap/libraries/Math.sol

//@audit Try to make a `constant` with `4` value
93:         uint256 ki = (4 * k) * i;

//@audit Try to make a `constant` with `4` value
184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L93-L93) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L184-L184)


```solidity

File: /src/mimswap/periphery/Router.sol

//@audit Try to make a `constant` with `18` value
85:             _validateDecimals(IERC20Metadata(token).decimals(), 18);

//@audit Try to make a `constant` with `18` value
83:             _validateDecimals(18, IERC20Metadata(token).decimals());

//@audit Try to make a `constant` with `2001` value
105:         if (shares <= 2001) {

//@audit Try to make a `constant` with `1001` value
109:         shares -= 1001;

//@audit Try to make a `constant` with `2001` value
142:             if (shares <= 2001) {

//@audit Try to make a `constant` with `1001` value
146:             shares -= 1001;

//@audit Try to make a `constant` with `256` value
590:         if (pathLength > 256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L85-L85) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L83-L83), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L105-L105), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L109-L109), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L142-L142), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L146-L146), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L590-L590)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

//@audit Try to make a `constant` with `18` value
30:         return 18;

//@audit Try to make a `constant` with `10` value
38:         uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));

//@audit Try to make a `constant` with `10` value
39:         uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));

//@audit Try to make a `constant` with `10` value
43:         baseReserve = baseReserve * (10 ** (WAD - baseDecimals));

//@audit Try to make a `constant` with `10` value
44:         quoteReserve = quoteReserve * (10 ** (WAD - quoteDecimals));


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L30-L30) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L44-L44)


</details>


### [NC&#x2011;65] Use the latest solidity (prior to 0.8.20 if on L2s) for deployment 
```
When deploying contracts, you should use the latest released version of Solidity.Apart from exceptional cases, only the latest version receives security fixes.
```
https://docs.soliditylang.org/en/v0.8.20/


*There are 20 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L2-L2) 


```solidity

File: /src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L3-L3) 


```solidity

File: /src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L2-L2) 


```solidity

File: /src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L3-L3) 


```solidity

File: /src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L2-L2) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L2-L2) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L2-L2) 


```solidity

File: /src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L2-L2) 


```solidity

File: /src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L2) 


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L7-L7) 


```solidity

File: /src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L8-L8) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L8-L8) 


```solidity

File: /src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L2-L2) 


```solidity

File: /src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L2-L2) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L2-L2) 


```solidity

File: /src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L2-L2) 


</details>


### [NC&#x2011;66] Use a single file for system wide constants 
Consider grouping all the system constants under a single file. This finding shows only the first constant for each file.


*There are 7 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/libraries/BlastPoints.sol

7:     address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L7-L7) 


```solidity

File: /src/blast/libraries/BlastYields.sol

14:     IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L14-L14) 


```solidity

File: /src/mimswap/MagicLP.sol

63:     uint256 public constant MAX_I = 10 ** 36;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L63-L63) 


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

20:     uint256 internal constant ONE = 10 ** 18;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L20-L20) 


```solidity

File: /src/mimswap/periphery/Router.sol

31:     uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L31-L31) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

16:     uint256 public constant WAD = 18;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L16-L16) 


```solidity

File: /src/staking/LockingMultiRewards.sol

78:     uint256 private constant BIPS = 10_000;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L78-L78) 


</details>


### [NC&#x2011;67] Consider using SMTChecker 
The SMTChecker is a valuable tool for Solidity developers as it helps detect potential vulnerabilities and logical errors in the contract's code. By utilizing Satisfiability Modulo Theories (SMT) solvers, it can reason about the potential states a contract can be in, and therefore, identify conditions that could lead to undesirable behavior. This automatic formal verification can catch issues that might otherwise be missed in manual code reviews or standard testing, enhancing the overall contract's security and reliability.


*There are 20 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L2-L2) 


```solidity

File: /src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L3-L3) 


```solidity

File: /src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L2-L2) 


```solidity

File: /src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L3-L3) 


```solidity

File: /src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L2-L2) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L2-L2) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L2-L2) 


```solidity

File: /src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L2-L2) 


```solidity

File: /src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L2) 


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L7-L7) 


```solidity

File: /src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L8-L8) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L8-L8) 


```solidity

File: /src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L2-L2) 


```solidity

File: /src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L2-L2) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L2-L2) 


```solidity

File: /src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L2-L2) 


</details>


### [NC&#x2011;68] Variable name must be in mixedCase 
Avoid using underscore for variable Names or parameters


*There are 10 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

// @audit _BASE_TOKEN_
70:     address public _BASE_TOKEN_;

// @audit _QUOTE_TOKEN_
71:     address public _QUOTE_TOKEN_;

// @audit _BASE_RESERVE_
72:     uint112 public _BASE_RESERVE_;

// @audit _QUOTE_RESERVE_
73:     uint112 public _QUOTE_RESERVE_;

// @audit _BLOCK_TIMESTAMP_LAST_
74:     uint32 public _BLOCK_TIMESTAMP_LAST_;

// @audit _BASE_PRICE_CUMULATIVE_LAST_
75:     uint256 public _BASE_PRICE_CUMULATIVE_LAST_;

// @audit _BASE_TARGET_
76:     uint112 public _BASE_TARGET_;

// @audit _QUOTE_TARGET_
77:     uint112 public _QUOTE_TARGET_;

// @audit _MT_FEE_RATE_MODEL_
79:     IFeeRateModel public _MT_FEE_RATE_MODEL_;

// @audit _LP_FEE_RATE_
80:     uint256 public _LP_FEE_RATE_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L70-L70) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L80-L80)


</details>


### [NC&#x2011;69] Whitespace in Expressions 
See the [Whitespace in Expressions](https://docs.soliditylang.org/en/latest/style-guide.html#whitespace-in-expressions) section of the Solidity Style Guide


*There are 13 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/periphery/Router.sol

//@audit remove the whiteSpace before the ')' char
70:         (shares, , ) = IMagicLP(clone).buyShares(to);
71:     }

//@audit remove the whiteSpace before the ',' char
70:         (shares, , ) = IMagicLP(clone).buyShares(to);
71:     }

//@audit remove the whiteSpace before the ')' char
93:         (shares, , ) = IMagicLP(clone).buyShares(to);
94:     }

//@audit remove the whiteSpace before the ',' char
93:         (shares, , ) = IMagicLP(clone).buyShares(to);
94:     }

//@audit remove the whiteSpace before the ')' char
500:         (shares, , ) = IMagicLP(lp).buyShares(to);
501: 

//@audit remove the whiteSpace before the ',' char
500:         (shares, , ) = IMagicLP(lp).buyShares(to);
501: 

//@audit remove the whiteSpace before the ')' char
544:         for (uint256 i = 0; i < iterations; ) {
545:             if (directions & 1 == 0) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L70-L71) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L70-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L93-L94), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L93-L94), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L500-L501), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L500-L501), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L544-L545)


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit remove the whiteSpace before the ')' char
405:         for (uint256 i; i < users.length; ) {
406:             address user = users[i];

//@audit remove the whiteSpace before the ')' char
547:         for (uint256 i; i < rewardTokens.length; ) {
548:             _updateRewardsGlobal(rewardTokens[i], totalSupply_);

//@audit remove the whiteSpace before the ')' char
561:         for (uint256 i; i < rewardTokens.length; ) {
562:             address token = rewardTokens[i];

//@audit remove the whiteSpace before the ')' char
575:         for (uint256 i; i < rewardTokens.length; ) {
576:             address token = rewardTokens[i];

//@audit remove the whiteSpace before the ')' char
580:             for (uint256 j; j < users.length; ) {
581:                 address user = users[j];

//@audit remove the whiteSpace before the ')' char
614:         for (uint256 i; i < rewardTokens.length; ) {
615:             address rewardToken = rewardTokens[i];


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L405-L406) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L547-L548), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L561-L562), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L575-L576), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L580-L581), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L614-L615)


</details>


### [NC&#x2011;70] Complex function controle flow 
Due to multiple if, loop and conditions the following functions has a very complex controle flow that could make auditing very difficult to cover all possible path\nTherefore, consider breaking down these blocks into more manageable units, by splitting things into utility functions, by reducing nesting, and by using early returns


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

091:     function init(
092:         address baseTokenAddress,
093:         address quoteTokenAddress,
094:         uint256 lpFeeRate,
095:         address mtFeeRateModel,
096:         uint256 i,
097:         uint256 k
098:     ) external {
099:         if (_INITIALIZED_) {
100:             revert ErrInitialized();
101:         }
102:         if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
103:             revert ErrZeroAddress();
104:         }
105:         if (baseTokenAddress == quoteTokenAddress) {
106:             revert ErrBaseQuoteSame();
107:         }
108:         if (i == 0 || i > MAX_I) {
109:             revert ErrInvalidI();
110:         }
111:         if (k > MAX_K) {
112:             revert ErrInvalidK();
113:         }
114:         if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {
115:             revert ErrInvalidLPFeeRate();
116:         }
117: 
118:         _INITIALIZED_ = true;
119:         _BASE_TOKEN_ = baseTokenAddress;
120:         _QUOTE_TOKEN_ = quoteTokenAddress;
121:         _I_ = i;
122:         _K_ = k;
123:         _LP_FEE_RATE_ = lpFeeRate;
124:         _MT_FEE_RATE_MODEL_ = IFeeRateModel(mtFeeRateModel);
125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);
126: 
127:         _afterInitialized();
128:     }

290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
291:         _transferBaseOut(assetTo, baseAmount);
292:         _transferQuoteOut(assetTo, quoteAmount);
293: 
294:         if (data.length > 0) {
295:             ICallee(assetTo).FlashLoanCall(msg.sender, baseAmount, quoteAmount, data);
296:         }
297: 
298:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
299:         uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
300: 
301:         // no input -> pure loss
302:         if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
303:             revert ErrFlashLoanFailed();
304:         }
305: 
306:         // sell quote case
307:         // quote input + base output
308:         if (baseBalance < _BASE_RESERVE_) {
309:             uint256 quoteInput = quoteBalance - uint256(_QUOTE_RESERVE_);
310:             (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) = querySellQuote(
311:                 tx.origin,
312:                 quoteInput
313:             );
314: 
315:             if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {
316:                 revert ErrFlashLoanFailed();
317:             }
318: 
319:             _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
320:             if (_RState_ != uint32(newRState)) {
321:                 _QUOTE_TARGET_ = newQuoteTarget.toUint112();
322:                 _RState_ = uint32(newRState);
323:                 emit RChange(newRState);
324:             }
325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);
326:         }
327: 
328:         // sell base case
329:         // base input + quote output
330:         if (quoteBalance < _QUOTE_RESERVE_) {
331:             uint256 baseInput = baseBalance - uint256(_BASE_RESERVE_);
332:             (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) = querySellBase(
333:                 tx.origin,
334:                 baseInput
335:             );
336: 
337:             if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {
338:                 revert ErrFlashLoanFailed();
339:             }
340: 
341:             _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
342:             if (_RState_ != uint32(newRState)) {
343:                 _BASE_TARGET_ = newBaseTarget.toUint112();
344:                 _RState_ = uint32(newRState);
345:                 emit RChange(newRState);
346:             }
347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
348:         }
349: 
350:         _sync();
351: 
352:         emit FlashLoan(msg.sender, assetTo, baseAmount, quoteAmount);
353:     }

360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
361:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
362:         uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
363:         uint256 baseReserve = _BASE_RESERVE_;
364:         uint256 quoteReserve = _QUOTE_RESERVE_;
365: 
366:         baseInput = baseBalance - baseReserve;
367:         quoteInput = quoteBalance - quoteReserve;
368: 
369:         if (baseInput == 0) {
370:             revert ErrNoBaseInput();
371:         }
372: 
373:         // Round down when withdrawing. Therefore, never be a situation occurring balance is 0 but totalsupply is not 0
374:         // But May Happenoe 0 But totalSupply = 0
375:         if (totalSupply() == 0) {
376:             // case 1. initial supply
377:             if (quoteBalance == 0) {
378:                 revert ErrZeroQuoteAmount();
379:             }
380: 
381:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;
382:             _BASE_TARGET_ = shares.toUint112();
383:             _QUOTE_TARGET_ = DecimalMath.mulFloor(shares, _I_).toUint112();
384: 
385:             if (_QUOTE_TARGET_ == 0) {
386:                 revert ErrZeroQuoteTarget();
387:             }
388: 
389:             if (shares <= 2001) {
390:                 revert ErrMintAmountNotEnough();
391:             }
392: 
393:             _mint(address(0), 1001);
394:             shares -= 1001;
395:         } else if (baseReserve > 0 && quoteReserve > 0) {
396:             // case 2. normal case
397:             uint256 baseInputRatio = DecimalMath.divFloor(baseInput, baseReserve);
398:             uint256 quoteInputRatio = DecimalMath.divFloor(quoteInput, quoteReserve);
399:             uint256 mintRatio = quoteInputRatio < baseInputRatio ? quoteInputRatio : baseInputRatio;
400:             shares = DecimalMath.mulFloor(totalSupply(), mintRatio);
401: 
402:             _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();
403:             _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
404:         }
405: 
406:         _mint(to, shares);
407:         _setReserve(baseBalance, quoteBalance);
408: 
409:         emit BuyShares(to, shares, balanceOf(to));
410:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L91-L128) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L290-L353), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L360-L410)


```solidity

File: /src/mimswap/libraries/Math.sol

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
132:         if (V0 == 0) {
133:             revert ErrIsZero();
134:         }
135: 
136:         if (delta == 0) {
137:             return 0;
138:         }
139: 
140:         if (k == 0) {
141:             return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);
142:         }
143: 
144:         if (k == DecimalMath.ONE) {
145:             // if k==1
146:             // Q2=Q1/(1+ideltaBQ1/Q0/Q0)
147:             // temp = ideltaBQ1/Q0/Q0
148:             // Q2 = Q1/(1+temp)
149:             // Q1-Q2 = Q1*(1-1/(1+temp)) = Q1*(temp/(1+temp))
150:             // uint256 temp = i.mul(delta).mul(V1).div(V0.mul(V0));
151:             uint256 temp;
152:             uint256 idelta = i * delta;
153:             if (idelta == 0) {
154:                 temp = 0;
155:             } else if ((idelta * V1) / idelta == V1) {
156:                 temp = (idelta * V1) / (V0 * V0);
157:             } else {
158:                 temp = (((delta * V1) / V0) * i) / V0;
159:             }
160:             return (V1 * temp) / (temp + DecimalMath.ONE);
161:         }
162: 
163:         // calculate -b value and sig
164:         // b = kQ0^2/Q1-i*deltaB-(1-k)Q1
165:         // part1 = (1-k)Q1 >=0
166:         // part2 = kQ0^2/Q1-i*deltaB >=0
167:         // bAbs = abs(part1-part2)
168:         // if part1>part2 => b is negative => bSig is false
169:         // if part2>part1 => b is positive => bSig is true
170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
171:         uint256 bAbs = (DecimalMath.ONE - k) * V1; // (1-k)Q1
172: 
173:         bool bSig;
174:         if (bAbs >= part2) {
175:             bAbs = bAbs - part2;
176:             bSig = false;
177:         } else {
178:             bAbs = part2 - bAbs;
179:             bSig = true;
180:         }
181:         bAbs = bAbs / DecimalMath.ONE;
182: 
183:         // calculate sqrt
184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
185:         squareRoot = sqrt((bAbs * bAbs) + squareRoot); // sqrt(b*b+4(1-k)kQ0*Q0)
186: 
187:         // final res
188:         uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
189:         uint256 numerator;
190:         if (bSig) {
191:             numerator = squareRoot - bAbs;
192:             if (numerator == 0) {
193:                 revert ErrIsZero();
194:             }
195:         } else {
196:             numerator = bAbs + squareRoot;
197:         }
198: 
199:         uint256 V2 = DecimalMath.divCeil(numerator, denominator);
200:         if (V2 > V1) {
201:             return 0;
202:         } else {
203:             return V1 - V2;
204:         }
205:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L131-L205) 


```solidity

File: /src/mimswap/periphery/Router.sol

112:     function previewAddLiquidity(
113:         address lp,
114:         uint256 baseInAmount,
115:         uint256 quoteInAmount
116:     ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
117:         (uint256 baseReserve, uint256 quoteReserve) = IMagicLP(lp).getReserves();
118: 
119:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;
120:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;
121: 
122:         baseInAmount = baseBalance - baseReserve;
123:         quoteInAmount = quoteBalance - quoteReserve;
124: 
125:         if (baseInAmount == 0) {
126:             return (0, 0, 0);
127:         }
128: 
129:         uint256 totalSupply = IERC20(lp).totalSupply();
130: 
131:         if (totalSupply == 0) {
132:             if (quoteBalance == 0) {
133:                 return (0, 0, 0);
134:             }
135: 
136:             uint256 i = IMagicLP(lp)._I_();
137: 
138:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;
139:             baseAdjustedInAmount = shares;
140:             quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);
141: 
142:             if (shares <= 2001) {
143:                 return (0, 0, 0);
144:             }
145: 
146:             shares -= 1001;
147:         } else if (baseReserve > 0 && quoteReserve > 0) {
148:             uint256 baseInputRatio = DecimalMath.divFloor(baseInAmount, baseReserve);
149:             uint256 quoteInputRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);
150:             if (baseInputRatio <= quoteInputRatio) {
151:                 baseAdjustedInAmount = baseInAmount;
152:                 quoteAdjustedInAmount = DecimalMath.mulCeil(quoteReserve, baseInputRatio);
153:                 shares = DecimalMath.mulFloor(totalSupply, baseInputRatio);
154:             } else {
155:                 quoteAdjustedInAmount = quoteInAmount;
156:                 baseAdjustedInAmount = DecimalMath.mulCeil(baseReserve, quoteInputRatio);
157:                 shares = DecimalMath.mulFloor(totalSupply, quoteInputRatio);
158:             }
159:         }
160:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L112-L160) 


```solidity

File: /src/staking/LockingMultiRewards.sol

397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
398:         if (users.length != lockIndexes.length) {
399:             revert ErrLengthMismatch();
400:         }
401: 
402:         _updateRewardsForUsers(users);
403: 
404:         // Release all expired users' locks
405:         for (uint256 i; i < users.length; ) {
406:             address user = users[i];
407:             Balances storage bal = _balances[user];
408:             LockedBalance[] storage locks = _userLocks[user];
409: 
410:             if (locks.length == 0) {
411:                 revert ErrNoLocks();
412:             }
413: 
414:             uint256 index = lockIndexes[i];
415: 
416:             // Prevents processing `lastLockIndex` out of order
417:             if (index == lastLockIndex[user] && locks.length > 1) {
418:                 revert ErrInvalidLockIndex();
419:             }
420: 
421:             // prohibit releasing non-expired locks
422:             if (locks[index].unlockTime > block.timestamp) {
423:                 revert ErrLockNotExpired();
424:             }
425: 
426:             uint256 amount = locks[index].amount;
427:             uint256 lastIndex = locks.length - 1;
428: 
429:             /// Last lock index changed place with the one we just swapped.
430:             if (lastLockIndex[user] == lastIndex) {
431:                 lastLockIndex[user] = index;
432:             }
433: 
434:             if (index != lastIndex) {
435:                 locks[index] = locks[lastIndex];
436:                 emit LogLockIndexChanged(user, lastIndex, index);
437:             }
438: 
439:             locks.pop();
440: 
441:             unlockedSupply += amount;
442:             lockedSupply -= amount;
443: 
444:             bal.unlocked += amount;
445:             bal.locked -= amount;
446: 
447:             emit LogUnlocked(user, amount, index);
448: 
449:             unchecked {
450:                 ++i;
451:             }
452:         }
453:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L397-L453) 


</details>


### [NC&#x2011;71] Consider bounding input array length 
The functions below take in an unbounded array, and make function calls for entries in the array. While the function will revert if it eventually runs out of gas, it may be a nicer user experience to `require()` that the length of the array is below some reasonable maximum, so that the user doesn't have to use up a full transaction's gas only to see that the transaction reverts.


*There are 3 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

//@audit array name tokens
164:     function claimTokenYields(address[] memory tokens) external onlyOwner {
165:         for (uint256 i = 0; i < tokens.length; i++) {
166:             if (!supportedTokens[tokens[i]]) {
167:                 revert ErrUnsupportedToken();
168:             }
169:             if (registry.nativeYieldTokens(tokens[i])) {
170:                 BlastYields.claimAllTokenYields(tokens[i], feeTo);
171:             }
172:         }
173:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L164-L173) 


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit array name users
397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
398:         if (users.length != lockIndexes.length) {
399:             revert ErrLengthMismatch();
400:         }
401: 
402:         _updateRewardsForUsers(users);
403: 
404:         // Release all expired users' locks
405:         for (uint256 i; i < users.length; ) {
406:             address user = users[i];
407:             Balances storage bal = _balances[user];
408:             LockedBalance[] storage locks = _userLocks[user];
409: 
410:             if (locks.length == 0) {
411:                 revert ErrNoLocks();
412:             }
413: 
414:             uint256 index = lockIndexes[i];
415: 
416:             // Prevents processing `lastLockIndex` out of order
417:             if (index == lastLockIndex[user] && locks.length > 1) {
418:                 revert ErrInvalidLockIndex();
419:             }
420: 
421:             // prohibit releasing non-expired locks
422:             if (locks[index].unlockTime > block.timestamp) {
423:                 revert ErrLockNotExpired();
424:             }
425: 
426:             uint256 amount = locks[index].amount;
427:             uint256 lastIndex = locks.length - 1;
428: 
429:             /// Last lock index changed place with the one we just swapped.
430:             if (lastLockIndex[user] == lastIndex) {
431:                 lastLockIndex[user] = index;
432:             }
433: 
434:             if (index != lastIndex) {
435:                 locks[index] = locks[lastIndex];
436:                 emit LogLockIndexChanged(user, lastIndex, index);
437:             }
438: 
439:             locks.pop();
440: 
441:             unlockedSupply += amount;
442:             lockedSupply -= amount;
443: 
444:             bal.unlocked += amount;
445:             bal.locked -= amount;
446: 
447:             emit LogUnlocked(user, amount, index);
448: 
449:             unchecked {
450:                 ++i;
451:             }
452:         }
453:     }

//@audit array name lockIndexes
397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
398:         if (users.length != lockIndexes.length) {
399:             revert ErrLengthMismatch();
400:         }
401: 
402:         _updateRewardsForUsers(users);
403: 
404:         // Release all expired users' locks
405:         for (uint256 i; i < users.length; ) {
406:             address user = users[i];
407:             Balances storage bal = _balances[user];
408:             LockedBalance[] storage locks = _userLocks[user];
409: 
410:             if (locks.length == 0) {
411:                 revert ErrNoLocks();
412:             }
413: 
414:             uint256 index = lockIndexes[i];
415: 
416:             // Prevents processing `lastLockIndex` out of order
417:             if (index == lastLockIndex[user] && locks.length > 1) {
418:                 revert ErrInvalidLockIndex();
419:             }
420: 
421:             // prohibit releasing non-expired locks
422:             if (locks[index].unlockTime > block.timestamp) {
423:                 revert ErrLockNotExpired();
424:             }
425: 
426:             uint256 amount = locks[index].amount;
427:             uint256 lastIndex = locks.length - 1;
428: 
429:             /// Last lock index changed place with the one we just swapped.
430:             if (lastLockIndex[user] == lastIndex) {
431:                 lastLockIndex[user] = index;
432:             }
433: 
434:             if (index != lastIndex) {
435:                 locks[index] = locks[lastIndex];
436:                 emit LogLockIndexChanged(user, lastIndex, index);
437:             }
438: 
439:             locks.pop();
440: 
441:             unlockedSupply += amount;
442:             lockedSupply -= amount;
443: 
444:             bal.unlocked += amount;
445:             bal.locked -= amount;
446: 
447:             emit LogUnlocked(user, amount, index);
448: 
449:             unchecked {
450:                 ++i;
451:             }
452:         }
453:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L397-L453) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L397-L453)


</details>


### [NC&#x2011;72] A function which defines named returns in it's declaration doesn't need to use return 
Remove the return statement once ensuring it is safe to do so


*There are 14 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboardingBoot.sol

78:     function claimable(address user) external view returns (uint256 shares) {
79:         if (!ready || claimed[user]) {
80:             return 0;
81:         }
82: 
83:         return _claimable(user);
84:     }

155:     function _claimable(address user) internal view returns (uint256 shares) {
156:         uint256 totalLocked = totals[MIM].locked + totals[USDB].locked;
157: 
158:         if (totalLocked == 0) {
159:             return 0;
160:         }
161: 
162:         uint256 userLocked = balances[user][MIM].locked + balances[user][USDB].locked;
163:         return (userLocked * totalPoolShares) / totalLocked;
164:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L78-L84) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L155-L164)


```solidity

File: /src/blast/libraries/BlastYields.sol

51:     function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
52:         return claimAllNativeYields(address(this), recipient);
53:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L51-L53) 


```solidity

File: /src/mimswap/MagicLP.sol

215:     function getMidPrice() public view returns (uint256 midPrice) {
216:         return PMMPricing.getMidPrice(getPMMState());
217:     }

228:     function getBaseInput() public view returns (uint256 input) {
229:         return _BASE_TOKEN_.balanceOf(address(this)) - uint256(_BASE_RESERVE_);
230:     }

232:     function getQuoteInput() public view returns (uint256 input) {
233:         return _QUOTE_TOKEN_.balanceOf(address(this)) - uint256(_QUOTE_RESERVE_);
234:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L215-L217) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L228-L230), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L232-L234)


```solidity

File: /src/mimswap/periphery/Router.sol

178:     function addLiquidityUnsafe(
179:         address lp,
180:         address to,
181:         uint256 baseInAmount,
182:         uint256 quoteInAmount,
183:         uint256 minimumShares,
184:         uint256 deadline
185:     ) external ensureDeadline(deadline) returns (uint256 shares) {
186:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);
187:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);
188: 
189:         return _addLiquidity(lp, to, minimumShares);
190:     }

229:     function addLiquidityETHUnsafe(
230:         address lp,
231:         address to,
232:         uint256 tokenInAmount,
233:         uint256 minimumShares,
234:         uint256 deadline
235:     ) external payable ensureDeadline(deadline) returns (uint256 shares) {
236:         address token = IMagicLP(lp)._BASE_TOKEN_();
237:         if (token == address(weth)) {
238:             token = IMagicLP(lp)._QUOTE_TOKEN_();
239:         } else if (IMagicLP(lp)._QUOTE_TOKEN_() != address(weth)) {
240:             revert ErrNotETHLP();
241:         }
242: 
243:         weth.deposit{value: msg.value}();
244:         address(weth).safeTransfer(lp, msg.value);
245: 
246:         token.safeTransferFrom(msg.sender, lp, tokenInAmount);
247: 
248:         return _addLiquidity(lp, to, minimumShares);
249:     }

314:     function swapTokensForTokens(
315:         address to,
316:         uint256 amountIn,
317:         address[] calldata path,
318:         uint256 directions,
319:         uint256 minimumOut,
320:         uint256 deadline
321:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {
322:         _validatePath(path);
323: 
324:         address firstLp = path[0];
325: 
326:         // Transfer to the first LP
327:         if (directions & 1 == 0) {
328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
329:         } else {
330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
331:         }
332: 
333:         return _swap(to, path, directions, minimumOut);
334:     }

336:     function swapETHForTokens(
337:         address to,
338:         address[] calldata path,
339:         uint256 directions,
340:         uint256 minimumOut,
341:         uint256 deadline
342:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
343:         _validatePath(path);
344: 
345:         address firstLp = path[0];
346:         address inToken;
347: 
348:         if (directions & 1 == 0) {
349:             inToken = IMagicLP(firstLp)._BASE_TOKEN_();
350:         } else {
351:             inToken = IMagicLP(firstLp)._QUOTE_TOKEN_();
352:         }
353: 
354:         // Transfer to the first LP
355:         if (inToken != address(weth)) {
356:             revert ErrInTokenNotETH();
357:         }
358: 
359:         weth.deposit{value: msg.value}();
360:         inToken.safeTransfer(address(firstLp), msg.value);
361: 
362:         return _swap(to, path, directions, minimumOut);
363:     }

404:     function sellBaseTokensForTokens(
405:         address lp,
406:         address to,
407:         uint256 amountIn,
408:         uint256 minimumOut,
409:         uint256 deadline
410:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {
411:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
412:         return _sellBase(lp, to, minimumOut);
413:     }

415:     function sellBaseETHForTokens(
416:         address lp,
417:         address to,
418:         uint256 minimumOut,
419:         uint256 deadline
420:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
421:         address baseToken = IMagicLP(lp)._BASE_TOKEN_();
422: 
423:         if (baseToken != address(weth)) {
424:             revert ErrInvalidBaseToken();
425:         }
426: 
427:         weth.deposit{value: msg.value}();
428:         baseToken.safeTransfer(lp, msg.value);
429:         return _sellBase(lp, to, minimumOut);
430:     }

449:     function sellQuoteTokensForTokens(
450:         address lp,
451:         address to,
452:         uint256 amountIn,
453:         uint256 minimumOut,
454:         uint256 deadline
455:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {
456:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
457: 
458:         return _sellQuote(lp, to, minimumOut);
459:     }

461:     function sellQuoteETHForTokens(
462:         address lp,
463:         address to,
464:         uint256 minimumOut,
465:         uint256 deadline
466:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
467:         address quoteToken = IMagicLP(lp)._QUOTE_TOKEN_();
468: 
469:         if (quoteToken != address(weth)) {
470:             revert ErrInvalidQuoteToken();
471:         }
472: 
473:         weth.deposit{value: msg.value}();
474:         quoteToken.safeTransfer(lp, msg.value);
475:         return _sellQuote(lp, to, minimumOut);
476:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L178-L190) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L249), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L314-L334), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L336-L363), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L413), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L415-L430), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L449-L459), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L461-L476)


</details>


### [NC&#x2011;73] [NatSpec] Natspec `@dev` is missing from `contract` 



*There are 380 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

6: contract BlastDapp {

7:     constructor() {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L6-L6) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L7-L7)


```solidity

File: /src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {

14:     event LogTokenDepositEnabled(address indexed token, bool enabled);

15:     event LogFeeToChanged(address indexed feeTo);

17:     error ErrZeroAddress();

18:     error ErrUnsupportedToken();

24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

36:     function _onBeforeDeposit(

49:     /// OPERATORS

56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

65:     /// ADMIN

72:     function setFeeTo(address feeTo_) external onlyOwner {

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {

103:     function isOwner(address _account) internal view override returns (bool) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L13-L13) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L65-L65), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L103-L103)


```solidity

File: /src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {

8:     event LogFeeToChanged(address indexed feeTo);

9:     error ErrZeroAddress();

13:     receive() external payable {}

15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {

25:     /// OPERATORS

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

37:     /// ADMIN

49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L8-L8), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L9-L9), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L53-L53)


```solidity

File: /src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {

11:     event LogFeeToChanged(address indexed feeTo);

12:     event LogOperatorChanged(address indexed, bool);

13:     event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);

15:     error ErrNotAllowedImplementationOperator();

23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

36:     /// VIEWS

44:     /// OPERATORS / CLONES ONLY

53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

69:     /// ADMIN / CLONES ONLY

77:     /// ADMIN / IMPLEMENTATION ONLY

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {

95:     /// INTERNALS

104:     function _updateTokenClaimables() internal {

115:     /// MODIFIERS


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L10-L10) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L11-L11), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L53-L53), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L69-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L89-L89), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L95-L95), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L104-L104), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L115-L115)


```solidity

File: /src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {

13:     error ErrZeroAddress();

14:     error ErrWrongState();

15:     error ErrUnsupportedToken();

16:     error ErrNotAllowed();

24:     struct Balances {

43:     modifier onlyState(State _state) {

50:     modifier onlySupportedTokens(address token) {

58:     constructor() Owned(msg.sender) {

67:     event LogBootstrapperChanged(address indexed bootstrapper);

68:     event LogTokenSupported(address indexed token, bool supported);

69:     event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);

70:     event LogLock(address indexed user, address indexed token, uint256 amount);

71:     event LogFeeToChanged(address indexed feeTo);

72:     event LogWithdraw(address indexed user, address indexed token, uint256 amount);

73:     event LogTokenCapChanged(address indexed token, uint256 cap);

74:     event LogStateChange(State state);

75:     event LogTokenRescue(address indexed token, address indexed to, uint256 amount);

77:     error ErrUnsupported();

78:     error ErrCapReached();

80:     receive() external payable override {

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {

98:     /// PUBLIC

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {

144:     /// ADMIN

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

223:     /// PROXY IMPLEMENTATION


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L16-L16), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L58-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L67-L67), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L69-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L78-L78), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L98-L98), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L123-L123), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L132-L132), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L144-L144), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L156-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L160-L160), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L164-L164), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L195-L195), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L200-L200), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L205-L205), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L214-L214), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L218-L218), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L223-L223)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

37:     event LogReadyChanged(bool ready);

38:     event LogClaimed(address indexed user, uint256 shares, bool lock);

39:     event LogInitialized(Router indexed router);

40:     event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);

41:     event LogStakingChanged(address indexed staking);

43:     error ErrInsufficientAmountOut();

44:     error ErrNotReady();

45:     error ErrAlreadyClaimed();

46:     error ErrWrongFeeRateModel();

47:     error ErrAlreadyBootstrapped();

48:     error ErrNothingToClaim();

49:     error ErrCannotChangeOnceReady();

52:     /// PUBLIC

75:     /// VIEWS

86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

93:     /// ADMIN

129:     function initialize(Router _router) external onlyOwner {

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {

152:     /// INTERNALS


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L52-L52), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L86-L86), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L93-L93), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L129-L129), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L137), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L146), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L152-L152)


```solidity

File: /src/blast/BlastTokenRegistry.sol

6: contract BlastTokenRegistry is Owned {

7:     event LogNativeYieldTokenEnabled(address indexed token, bool enabled);

8:     error ErrZeroAddress();

12:     constructor(address _owner) Owned(_owner) {}

14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L6-L6) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L7-L7), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L8-L8), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L14-L14)


```solidity

File: /src/blast/BlastWrappers.sol

19: contract BlastMIMSwapRouter is Router {

28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {

20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

29:     constructor(

43:     error ErrInvalidGovernorAddress();

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {

59:     function init(bytes calldata data) public payable override {

70:     function _setupBlacklist() private {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L19-L19) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L59-L59), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L70-L70)


```solidity

File: /src/blast/libraries/BlastPoints.sol

6: library BlastPoints {

10:     function configure() internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L6-L6) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L10-L10)


```solidity

File: /src/blast/libraries/BlastYields.sol

7: library BlastYields {

8:     event LogBlastGasClaimed(address indexed recipient, uint256 amount);

9:     event LogBlastETHClaimed(address indexed recipient, uint256 amount);

10:     event LogBlastTokenClaimed(address indexed recipient, address indexed token, uint256 amount);

11:     event LogBlastTokenClaimableEnabled(address indexed contractAddress, address indexed token);

12:     event LogBlastNativeClaimableEnabled(address indexed contractAddress);

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L8-L8), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L9-L9), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L10-L10), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L11-L11), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L60-L60), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L86-L86)


```solidity

File: /src/mimswap/MagicLP.sol

23: /// @title MIMSwap MagicLP
24: /// @author Adapted from DODOEX DSP https://github.com/DODOEX/contractV2/tree/main/contracts/DODOStablePool
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {

30:     event BuyShares(address to, uint256 increaseShares, uint256 totalShares);

31:     event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);

32:     event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);

33:     event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);

34:     event RChange(PMMPricing.RState newRState);

35:     event TokenRescue(address indexed token, address to, uint256 amount);

36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);

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

84:     constructor(address owner_) Owned(owner_) {

91:     function init(

131:     /// PUBLIC

138:     function correctRState() external {

152:     /// VIEWS

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

241:     /// TRADE FUNCTIONS

267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

356:     /// BUY & SELL SHARES

413:     function sellShares(

458:     /// ADMIN

470:     function setParameters(

504:     function ratioSync() external nonReentrant onlyImplementationOwner {

525:     /// INTERNALS

545:     function _twapUpdate() internal {

560:     function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {

567:     function _sync() internal {

581:     function _transferBaseOut(address to, uint256 amount) internal {

587:     function _transferQuoteOut(address to, uint256 amount) internal {

593:     function _mint(address to, uint256 amount) internal override {

601:     function _afterInitialized() internal virtual {}

604:     /// MODIFIERS

614:     modifier onlyClones() {

621:     modifier onlyImplementation() {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L23-L25) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L52-L52), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L53-L53), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L54-L54), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L58-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L59-L59), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L91-L91), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L131-L131), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L138-L138), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L152-L152), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L159-L159), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L163-L163), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L167-L167), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L180-L180), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L193-L193), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L219-L219), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L224-L224), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L228-L228), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L232-L232), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L236-L236), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L241-L241), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L267-L267), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L290-L290), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L356-L356), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L413-L413), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L458-L458), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L470), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L504-L504), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L525-L525), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L545-L545), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L560-L560), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L567-L567), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L581-L581), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L587-L587), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L593-L593), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L601-L601), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L604-L604), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L614-L614), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L621-L621)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

13: contract FeeRateModel is Owned {

14:     event LogImplementationChanged(address indexed implementation);

15:     event LogMaintainerChanged(address indexed maintainer);

17:     error ErrZeroAddress();

22:     constructor(address maintainer_, address owner_) Owned(owner_) {

31:     /// VIEWS

43:     /// ADMIN

55:     /// @notice Set the fee rate implementation and default fee rate
56:     /// @param implementation_ The address of the fee rate implementation, use address(0) to disable


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L13-L13) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L55-L56)


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

7: contract FeeRateModelImpl {

9:     function getFeeRate(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L9)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

11: /**
12:  * @title DecimalMath
13:  * @author DODO Breeder
14:  *
15:  * @notice Functions for fixed point number with 18 decimals
16:  */

23:     function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {

27:     function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {

31:     function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {

35:     function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {

39:     function reciprocalFloor(uint256 target) internal pure returns (uint256) {

43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {

47:     function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L11-L16) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L47-L47)


```solidity

File: /src/mimswap/libraries/Math.sol

12: /**
13:  * @author Adapted from https://github.com/DODOEX/contractV2/blob/main/contracts/lib/Math.sol
14:  * @notice Functions for complex calculating. Including ONE Integration and TWO Quadratic solutions
15:  */

17:     error ErrIsZero();

19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

29:     function sqrt(uint256 x) internal pure returns (uint256 y) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L12-L15) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L131-L131)


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

13: /**
14:  * @title Pricing
15:  * @author DODO Breeder
16:  *
17:  * @notice DODO Pricing model
18:  */

27:     struct PMMState {

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L13-L18) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L104-L104), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L119-L119), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L134-L134), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L147-L147), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L162-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L203-L203)


```solidity

File: /src/mimswap/periphery/Factory.sol

10: /// @notice Create and register MagicLP pools
11: contract Factory is Owned {

12:     event LogCreated(

23:     event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);

24:     event LogPoolRemoved(address pool);

25:     event LogSetImplementation(address indexed implementation);

26:     event LogSetMaintainer(address indexed newMaintainer);

27:     event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);

29:     error ErrInvalidUserPoolIndex();

30:     error ErrZeroAddress();

38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

50:     /// VIEWS

57:     function getUserPoolCount(address creator) external view returns (uint256) {

62:     /// PUBLIC

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

93:     /// ADMIN

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

114:     /// @notice Register a pool to the list
115:     /// Note this doesn't check if the pool is valid or if it's already registered.

120:     function removePool(

145:     /// INTERNALS

155:     function _computeSalt(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L10-L11) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L62-L62), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L93-L93), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L105), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L114-L115), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L120), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L145-L145), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L155-L155)


```solidity

File: /src/mimswap/periphery/Router.sol

12: contract Router {

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

36:     receive() external payable {}

38:     constructor(IWETH weth_, IFactory factory_) {

47:     modifier ensureDeadline(uint256 deadline) {

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

496:     /// INTERNALS

507:     /// Adapted from: https://github.com/DODOEX/contractV2/blob/main/contracts/SmartRoute/proxies/DODODspProxy.sol
508:     /// Copyright 2020 DODO ZOO. Licensed under Apache-2.0.

541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

586:     function _validatePath(address[] calldata path) internal pure {

598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L16-L16), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L54-L54), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L112-L112), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L162-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L178-L178), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L192-L192), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L229), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L251-L251), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L274-L274), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L314-L314), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L336-L336), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L365-L365), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L404), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L415-L415), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L432-L432), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L449-L449), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L461-L461), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L478-L478), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L496-L496), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L507-L508), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L541-L541), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L571-L571), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L578-L578), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L586-L586), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L598-L598)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

9: contract MagicLpAggregator is IAggregator {

18:     /// @param pair_ The MagicLP pair address
19:     /// @param baseOracle_ The base oracle
20:     /// @param quoteOracle_ The quote oracle

29:     function decimals() external pure override returns (uint8) {

33:     function _getReserves() internal view virtual returns (uint256, uint256) {

37:     function latestAnswer() public view override returns (int256) {

48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L9-L9) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L18-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L48-L48)


```solidity

File: /src/staking/LockingMultiRewards.sol

09: /// @notice A staking contract that distributes multiple rewards to stakers.
10: /// Stakers can lock their tokens for a period of time to get a boost on their rewards.
11: /// @author Based from Curve Finance's MultiRewards contract https://github.com/curvefi/multi-rewards/blob/master/contracts/MultiRewards.sol
12: /// @author Based from Ellipsis Finance's EpsStaker https://github.com/ellipsis-finance/ellipsis/blob/master/contracts/EpsStaker.sol
13: /// @author Based from Convex Finance's CvxLockerV2 https://github.com/convex-eth/platform/blob/main/contracts/contracts/CvxLockerV2.sol
14: contract LockingMultiRewards is OperatableV2, Pausable {

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

50:     struct Reward {

58:     struct Balances {

63:     struct LockedBalance {

68:     struct RewardLockItem {

73:     struct RewardLock {

147:     /// @notice Stakes the given amount of tokens for the given user.
148:     /// @param amount The amount of tokens to stake
149:     /// @param lock_ If true, the tokens will be locked for the lock duration for a reward boost

154:     /// @notice Locks an existing unlocked balance.

168:     /// @notice Withdraws the given amount of unlocked tokens for the given user.
169:     /// @param amount The amount of unlocked tokens to withdraw

186:     function withdrawWithRewards(uint256 amount) public virtual {

191:     function getRewards() public virtual {

197:     /// VIEWS

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

298:     /// ADMIN

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

322:     /// @notice This function can recover any token except for the staking token beyond the balance necessary for rewards.
323:     /// WARNING: Use this function with caution to ensure it does not affect the reward mechanism.

335:     /// EMERGENCY FUNCTIONS

341:     function unpause() external onlyOwner {

346:     /// OPERATORS

353:     /// @notice Distribute new rewards to the stakers
354:     /// @param rewardToken The address of the reward token
355:     /// @param amount The amount of reward tokens to distribute
356:     /// @param minRemainingTime The minimum remaining time for the current reward period
357:     /// Used to avoid distributing rewards on a lower period than the expected one.
358:     /// Example: If the reward period is 7 days, and there are 2 days left, `minRemainingTime` higher than
359:     /// 2 days will revert the transaction.
360:     /// To ignore this check, set `minRemainingTime` to 0.

395:     /// @notice Updates the balances of the given user and lock indexes

456:     /// INTERNALS

479:     function _createLock(address user, uint256 amount) internal {

536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

595:     /// @notice Claim unlocked rewards or create a new reward lock that


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L9-L14) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L58-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L63-L63), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L147-L149), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L154-L154), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L168-L169), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L186-L186), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L191-L191), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L197-L197), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L203-L203), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L207-L207), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L211-L211), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L219-L219), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L223-L223), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L227-L227), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L231-L231), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L235-L235), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L239-L239), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L257-L257), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L265-L265), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L269-L269), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L273-L273), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L288-L288), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L292-L292), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L298-L298), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L317-L317), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L322-L323), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L335-L335), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L341-L341), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L346-L346), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L353-L360), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L395-L395), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L456-L456), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L479-L479), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L595-L595)


</details>


### [NC&#x2011;74] Contract should expose an `interface` 
The `contract`s should expose an `interface` so that other projects can more easily integrate with it, without having to develop their own non-standard variants.


*There are 106 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

52:     function claimGasYields() external onlyOperators returns (uint256) {

56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

68:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

72:     function setFeeTo(address feeTo_) external onlyOwner {

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L52-L52) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L81-L81)


```solidity

File: /src/blast/BlastGovernor.sol

28:     function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

40:     function setFeeTo(address _feeTo) external onlyOwner {

49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L28-L28) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L53-L53)


```solidity

File: /src/blast/BlastMagicLP.sol

47:     function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {

53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

72:     function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {

80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L47-L47) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L53-L53), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L89-L89)


```solidity

File: /src/blast/BlastOnboarding.sol

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

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


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L123-L123) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L147-L147), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L156-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L160-L160), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L164-L164), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L195-L195), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L200-L200), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L205-L205), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L214-L214), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L218-L218)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

78:     function claimable(address user) external view returns (uint256 shares) {

86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L78-L78) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L86-L86), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L137), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L146)


```solidity

File: /src/blast/BlastTokenRegistry.sol

14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L14-L14) 


```solidity

File: /src/mimswap/MagicLP.sol

134:     function sync() external nonReentrant {

138:     function correctRState() external {

167:     function querySellBase(

180:     function querySellQuote(

193:     function getPMMState() public view returns (PMMPricing.PMMState memory state) {

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {

215:     function getMidPrice() public view returns (uint256 midPrice) {

224:     function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {

228:     function getBaseInput() public view returns (uint256 input) {

232:     function getQuoteInput() public view returns (uint256 input) {

236:     function version() external pure virtual returns (string memory) {

461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {

470:     function setParameters(

504:     function ratioSync() external nonReentrant onlyImplementationOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L134-L134) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L138-L138), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L167-L167), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L180-L180), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L193-L193), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L224-L224), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L228-L228), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L232-L232), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L236-L236), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L461-L461), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L470), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L504-L504)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

46:     function setMaintainer(address maintainer_) external onlyOwner {

57:     function setImplementation(address implementation_) public onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L46-L46) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L57)


```solidity

File: /src/mimswap/periphery/Factory.sol

53:     function getPoolCount(address token0, address token1) external view returns (uint256) {

57:     function getUserPoolCount(address creator) external view returns (uint256) {

96:     function setLpImplementation(address implementation_) external onlyOwner {

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

116:     function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {

120:     function removePool(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L53-L53) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L105), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L116-L116), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L120)


```solidity

File: /src/mimswap/periphery/Router.sol

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


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L54-L54) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L112-L112), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L162-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L178-L178), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L192-L192), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L229), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L251-L251), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L274-L274), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L314-L314), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L336-L336), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L365-L365), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L404), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L415-L415), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L432-L432), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L449-L449), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L461-L461), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L478-L478)


```solidity

File: /src/staking/LockingMultiRewards.sol

150:     function stake(uint256 amount, bool lock_) public whenNotPaused {

155:     function lock(uint256 amount) public whenNotPaused {

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

253:     function nextUnlockTime() public view returns (uint256) {

257:     function epoch() public view returns (uint256) {

261:     function nextEpoch() public view returns (uint256) {

265:     function remainingEpochTime() public view returns (uint256) {

269:     function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {

273:     function rewardPerToken(address rewardToken) public view returns (uint256) {

277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

288:     function earned(address user, address rewardToken) public view returns (uint256) {

300:     function addReward(address rewardToken) public onlyOwner {

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

324:     function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {

337:     function pause() external onlyOwner {

341:     function unpause() external onlyOwner {

349:     function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {

361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {

397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L150-L150) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L155-L155), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L186-L186), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L191-L191), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L199-L199), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L203-L203), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L207-L207), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L211-L211), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L219-L219), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L223-L223), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L227-L227), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L231-L231), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L253-L253), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L257-L257), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L265-L265), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L269-L269), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L273-L273), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L288-L288), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L300-L300), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L317-L317), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L324-L324), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L337-L337), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L341-L341), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L349-L349), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L361-L361), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L397-L397)


</details>


### [NC&#x2011;75] Named imports of parent contracts are missing 



*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

//@audit `BlastOnboardingData`
64: contract BlastOnboarding is BlastOnboardingData, Proxy {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L64-L64) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

//@audit `BlastOnboardingBootDataV1`
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L34-L34) 


</details>


### [NC&#x2011;76] [NatSpec] Natspec `@notice` is missing from `contract` 



*There are 375 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

6: contract BlastDapp {

7:     constructor() {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L6-L6) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L7-L7)


```solidity

File: /src/blast/BlastBox.sol

13: contract BlastBox is DegenBox, OperatableV3 {

14:     event LogTokenDepositEnabled(address indexed token, bool enabled);

15:     event LogFeeToChanged(address indexed feeTo);

17:     error ErrZeroAddress();

18:     error ErrUnsupportedToken();

24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

36:     function _onBeforeDeposit(

49:     /// OPERATORS

56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

65:     /// ADMIN

72:     function setFeeTo(address feeTo_) external onlyOwner {

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {

97:     /// @dev Called on DegenBox's constructor

103:     function isOwner(address _account) internal view override returns (bool) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L13-L13) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L65-L65), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L97-L97), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L103-L103)


```solidity

File: /src/blast/BlastGovernor.sol

7: contract BlastGovernor is OperatableV2 {

8:     event LogFeeToChanged(address indexed feeTo);

9:     error ErrZeroAddress();

13:     receive() external payable {}

15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {

25:     /// OPERATORS

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

37:     /// ADMIN

49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L8-L8), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L9-L9), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L53-L53)


```solidity

File: /src/blast/BlastMagicLP.sol

10: contract BlastMagicLP is MagicLP {

11:     event LogFeeToChanged(address indexed feeTo);

12:     event LogOperatorChanged(address indexed, bool);

13:     event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);

15:     error ErrNotAllowedImplementationOperator();

23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

36:     /// VIEWS

44:     /// OPERATORS / CLONES ONLY

53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {

64:     function updateTokenClaimables() external onlyClones onlyImplementationOperators {

69:     /// ADMIN / CLONES ONLY

77:     /// ADMIN / IMPLEMENTATION ONLY

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {

95:     /// INTERNALS

104:     function _updateTokenClaimables() internal {

115:     /// MODIFIERS


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L10-L10) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L11-L11), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L53-L53), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L69-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L89-L89), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L95-L95), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L104-L104), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L115-L115)


```solidity

File: /src/blast/BlastOnboarding.sol

12: contract BlastOnboardingData is Owned, Pausable {

64: contract BlastOnboarding is BlastOnboardingData, Proxy {

13:     error ErrZeroAddress();

14:     error ErrWrongState();

15:     error ErrUnsupportedToken();

16:     error ErrNotAllowed();

24:     struct Balances {

43:     modifier onlyState(State _state) {

50:     modifier onlySupportedTokens(address token) {

58:     constructor() Owned(msg.sender) {

67:     event LogBootstrapperChanged(address indexed bootstrapper);

68:     event LogTokenSupported(address indexed token, bool supported);

69:     event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);

70:     event LogLock(address indexed user, address indexed token, uint256 amount);

71:     event LogFeeToChanged(address indexed feeTo);

72:     event LogWithdraw(address indexed user, address indexed token, uint256 amount);

73:     event LogTokenCapChanged(address indexed token, uint256 cap);

74:     event LogStateChange(State state);

75:     event LogTokenRescue(address indexed token, address indexed to, uint256 amount);

77:     error ErrUnsupported();

78:     error ErrCapReached();

80:     receive() external payable override {

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {

98:     /// PUBLIC

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {

144:     /// ADMIN

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

223:     /// PROXY IMPLEMENTATION


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L64-L64), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L16-L16), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L58-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L67-L67), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L69-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L78-L78), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L98-L98), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L123-L123), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L132-L132), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L144-L144), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L156-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L160-L160), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L164-L164), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L195-L195), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L200-L200), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L205-L205), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L214-L214), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L218-L218), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L223-L223)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

33: /// @dev Functions are postfixed with the version number to avoid collisions
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {

37:     event LogReadyChanged(bool ready);

38:     event LogClaimed(address indexed user, uint256 shares, bool lock);

39:     event LogInitialized(Router indexed router);

40:     event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);

41:     event LogStakingChanged(address indexed staking);

43:     error ErrInsufficientAmountOut();

44:     error ErrNotReady();

45:     error ErrAlreadyClaimed();

46:     error ErrWrongFeeRateModel();

47:     error ErrAlreadyBootstrapped();

48:     error ErrNothingToClaim();

49:     error ErrCannotChangeOnceReady();

52:     /// PUBLIC

75:     /// VIEWS

86:     function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

93:     /// ADMIN

129:     function initialize(Router _router) external onlyOwner {

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {

152:     /// INTERNALS


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L33-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L52-L52), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L86-L86), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L93-L93), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L129-L129), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L137), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L146), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L152-L152)


```solidity

File: /src/blast/BlastTokenRegistry.sol

6: contract BlastTokenRegistry is Owned {

7:     event LogNativeYieldTokenEnabled(address indexed token, bool enabled);

8:     error ErrZeroAddress();

12:     constructor(address _owner) Owned(_owner) {}

14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L6-L6) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L7-L7), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L8-L8), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L14-L14)


```solidity

File: /src/blast/BlastWrappers.sol

14: /// @dev Collection of Blast wrapped contract that are succecptible to be used
15: /// enough to justify claiming gas yields.
16: 

19: contract BlastMIMSwapRouter is Router {

28: contract BlastMIMSwapFactory is Factory {

42: contract BlastCauldronV4 is CauldronV4 {

20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

29:     constructor(

43:     error ErrInvalidGovernorAddress();

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {

59:     function init(bytes calldata data) public payable override {

70:     function _setupBlacklist() private {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L14-L16) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L59-L59), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L70-L70)


```solidity

File: /src/blast/libraries/BlastPoints.sol

6: library BlastPoints {

10:     function configure() internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L6-L6) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L10-L10)


```solidity

File: /src/blast/libraries/BlastYields.sol

7: library BlastYields {

8:     event LogBlastGasClaimed(address indexed recipient, uint256 amount);

9:     event LogBlastETHClaimed(address indexed recipient, uint256 amount);

10:     event LogBlastTokenClaimed(address indexed recipient, address indexed token, uint256 amount);

11:     event LogBlastTokenClaimableEnabled(address indexed contractAddress, address indexed token);

12:     event LogBlastNativeClaimableEnabled(address indexed contractAddress);

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L8-L8), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L9-L9), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L10-L10), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L11-L11), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L60-L60), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L86-L86)


```solidity

File: /src/mimswap/MagicLP.sol

23: /// @title MIMSwap MagicLP
24: /// @author Adapted from DODOEX DSP https://github.com/DODOEX/contractV2/tree/main/contracts/DODOStablePool
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {

30:     event BuyShares(address to, uint256 increaseShares, uint256 totalShares);

31:     event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);

32:     event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);

33:     event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);

34:     event RChange(PMMPricing.RState newRState);

35:     event TokenRescue(address indexed token, address to, uint256 amount);

36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);

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

84:     constructor(address owner_) Owned(owner_) {

91:     function init(

131:     /// PUBLIC

138:     function correctRState() external {

152:     /// VIEWS

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

241:     /// TRADE FUNCTIONS

267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

356:     /// BUY & SELL SHARES

413:     function sellShares(

458:     /// ADMIN

470:     function setParameters(

504:     function ratioSync() external nonReentrant onlyImplementationOwner {

525:     /// INTERNALS

545:     function _twapUpdate() internal {

560:     function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {

567:     function _sync() internal {

581:     function _transferBaseOut(address to, uint256 amount) internal {

587:     function _transferQuoteOut(address to, uint256 amount) internal {

593:     function _mint(address to, uint256 amount) internal override {

601:     function _afterInitialized() internal virtual {}

604:     /// MODIFIERS

614:     modifier onlyClones() {

621:     modifier onlyImplementation() {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L23-L25) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L52-L52), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L53-L53), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L54-L54), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L58-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L59-L59), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L91-L91), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L131-L131), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L138-L138), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L152-L152), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L159-L159), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L163-L163), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L167-L167), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L180-L180), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L193-L193), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L204), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L219-L219), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L224-L224), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L228-L228), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L232-L232), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L236-L236), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L241-L241), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L267-L267), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L290-L290), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L356-L356), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L413-L413), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L458-L458), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L470), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L504-L504), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L525-L525), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L545-L545), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L560-L560), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L567-L567), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L581-L581), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L587-L587), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L593-L593), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L601-L601), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L604-L604), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L614-L614), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L621-L621)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

13: contract FeeRateModel is Owned {

14:     event LogImplementationChanged(address indexed implementation);

15:     event LogMaintainerChanged(address indexed maintainer);

17:     error ErrZeroAddress();

22:     constructor(address maintainer_, address owner_) Owned(owner_) {

31:     /// VIEWS

43:     /// ADMIN


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L13-L13) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L43-L43)


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

7: contract FeeRateModelImpl {

9:     function getFeeRate(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L9)


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L47-L47)


```solidity

File: /src/mimswap/libraries/Math.sol

17:     error ErrIsZero();

19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

29:     function sqrt(uint256 x) internal pure returns (uint256 y) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L17-L17) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L131-L131)


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

27:     struct PMMState {

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L27-L27) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L104-L104), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L119-L119), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L134-L134), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L147-L147), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L162-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L203-L203)


```solidity

File: /src/mimswap/periphery/Factory.sol

12:     event LogCreated(

23:     event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);

24:     event LogPoolRemoved(address pool);

25:     event LogSetImplementation(address indexed implementation);

26:     event LogSetMaintainer(address indexed newMaintainer);

27:     event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);

29:     error ErrInvalidUserPoolIndex();

30:     error ErrZeroAddress();

38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

50:     /// VIEWS

57:     function getUserPoolCount(address creator) external view returns (uint256) {

62:     /// PUBLIC

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

93:     /// ADMIN

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

120:     function removePool(

145:     /// INTERNALS

155:     function _computeSalt(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L62-L62), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L93-L93), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L105), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L120), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L145-L145), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L155-L155)


```solidity

File: /src/mimswap/periphery/Router.sol

12: contract Router {

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

36:     receive() external payable {}

38:     constructor(IWETH weth_, IFactory factory_) {

47:     modifier ensureDeadline(uint256 deadline) {

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

496:     /// INTERNALS

507:     /// Adapted from: https://github.com/DODOEX/contractV2/blob/main/contracts/SmartRoute/proxies/DODODspProxy.sol
508:     /// Copyright 2020 DODO ZOO. Licensed under Apache-2.0.

541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

586:     function _validatePath(address[] calldata path) internal pure {

598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L16-L16), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L54-L54), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L112-L112), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L162-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L178-L178), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L192-L192), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L229), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L251-L251), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L274-L274), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L314-L314), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L336-L336), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L365-L365), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L404), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L415-L415), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L432-L432), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L449-L449), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L461-L461), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L478-L478), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L496-L496), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L507-L508), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L541-L541), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L571-L571), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L578-L578), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L586-L586), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L598-L598)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

9: contract MagicLpAggregator is IAggregator {

18:     /// @param pair_ The MagicLP pair address
19:     /// @param baseOracle_ The base oracle
20:     /// @param quoteOracle_ The quote oracle

29:     function decimals() external pure override returns (uint8) {

33:     function _getReserves() internal view virtual returns (uint256, uint256) {

37:     function latestAnswer() public view override returns (int256) {

48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L9-L9) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L18-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L48-L48)


```solidity

File: /src/staking/LockingMultiRewards.sol

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

50:     struct Reward {

58:     struct Balances {

63:     struct LockedBalance {

68:     struct RewardLockItem {

73:     struct RewardLock {

105:     ///
106:     /// @dev Constructor
107:     /// @param _stakingToken The token that is being staked
108:     /// @param _owner The owner of the contract
109:     /// @param _lockingBoostMultiplerInBips The multiplier for the locking boost. 30000 means if you stake 100, you get 300 locked
110:     /// @param _rewardsDuration The duration of the rewards period in seconds, should be 7 days by default.
111:     /// @param _lockDuration The duration of the lock period in seconds, should be 13 weeks by default.

186:     function withdrawWithRewards(uint256 amount) public virtual {

191:     function getRewards() public virtual {

197:     /// VIEWS

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

244:     /// @dev Calculates when the next unlock event will occur given the current epoch.
245:     /// It ensures that the unlock timing coincides with the intervals at which rewards are distributed.
246:     /// If the current time is within an ongoing reward interval, the function establishes the
247:     /// unlock period to begin at the next epoch.
248:     /// So, if you stake at week 1 + 4 days, you will be able to unlock at the end of week 14.

257:     function epoch() public view returns (uint256) {

261:     function nextEpoch() public view returns (uint256) {

265:     function remainingEpochTime() public view returns (uint256) {

269:     function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {

273:     function rewardPerToken(address rewardToken) public view returns (uint256) {

277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

288:     function earned(address user, address rewardToken) public view returns (uint256) {

292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

298:     /// ADMIN

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

335:     /// EMERGENCY FUNCTIONS

341:     function unpause() external onlyOwner {

346:     /// OPERATORS

456:     /// INTERNALS

479:     function _createLock(address user, uint256 amount) internal {

516:     /// @dev Update the global accumulated rewards from the last update to this point,
517:     /// in relation with the `totalSupply`
518:     ///
519:     /// The idea is to allow everyone that are currently part of that supply to get their allocated
520:     /// reward share.
521:     ///
522:     /// Each user's reward share is taking in account when `rewards[user][token] = _earned(...)`
523:     /// is called. And only updated when a user is interacting with `stake`, `lock`, `withdraw`
524:     /// or `getRewards`.
525:     ///
526:     /// Otherwise, if it's yet-to-be-updated, it's going to get considered as part of the pending
527:     /// yet-to-receive rewards in the `earned` function.

536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

541:     /// @dev Simplest version of updating rewards. Mainly used by `notifyRewardAmount`.
542:     /// where we don't need to update any particular user but the global state for
543:     /// each reward tokens only.

555:     /// @dev More gas efficient version of `_updateRewards` when we
556:     /// only need to update the rewards for a single user.

571:     /// @dev `_updateRewardsForUser` for multiple users.


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L17-L17) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L45-L45), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L58-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L63-L63), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L105-L111), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L186-L186), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L191-L191), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L197-L197), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L203-L203), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L207-L207), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L211-L211), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L219-L219), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L223-L223), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L227-L227), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L231-L231), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L235-L235), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L239-L239), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L244-L248), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L257-L257), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L265-L265), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L269-L269), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L273-L273), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L288-L288), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L292-L292), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L298-L298), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L317-L317), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L335-L335), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L341-L341), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L346-L346), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L456-L456), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L479-L479), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L516-L527), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L541-L543), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L555-L556), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L571-L571)


</details>


### [NC&#x2011;77] `function` names should use lowerCamelCase 
Here is an example of camelCase/lowerCamelCase and other types:
'helloWorld' is a CamelCase
'HelloWorld' is Not CamelCase (PascalCase)
'hello_world' is Not CamelCase (snake_case)
[For more details](https://khalilstemmler.com/blogs/camel-case-snake-case-pascal-case/)


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/staking/LockingMultiRewards.sol

//@audit `_rewardPerToken` is not in CamelCase
277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277) 


</details>


### [NC&#x2011;78] Expressions for constant values should use `immutable` rather than `constant` 
While it does not save gas for some simple binary expressions because the compiler knows that developers often make this mistake, it's still best to use the right tool for the task at hand. There is a difference between `constant` variables and `immutable` variables, and they should each be used in their appropriate contexts. `constants` should be used for literal values written into the code, and `immutable` variables should be used for expressions, or values calculated in, or passed into the constructor.


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/libraries/BlastPoints.sol

8:     IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L8-L8) 


```solidity

File: /src/blast/libraries/BlastYields.sol

14:     IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L14-L14) 


```solidity

File: /src/mimswap/MagicLP.sol

63:     uint256 public constant MAX_I = 10 ** 36;

64:     uint256 public constant MAX_K = 10 ** 18;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L63-L63) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L64-L64)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

20:     uint256 internal constant ONE = 10 ** 18;

21:     uint256 internal constant ONE2 = 10 ** 36;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L20-L20) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L21-L21)


</details>


### [NC&#x2011;79] Consider splitting long calculations 
The longer a string of operations is, the harder it is to understand it. Consider splitting the full calculation into more steps, with more descriptive temporary variable names, and add extensive comments.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/libraries/Math.sol

158:                 temp = (((delta * V1) / V0) * i) / V0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L158-L158) 


</details>


### [NC&#x2011;80] `immutable` variable names don\'t follow the Solidity style guide 
For `immutable` variable names, each word should use all capital letters, with underscores separating each word (CONSTANT_CASE)


*There are 16 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

20:     BlastTokenRegistry public immutable registry;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L20-L20) 


```solidity

File: /src/blast/BlastMagicLP.sol

17:     BlastTokenRegistry public immutable registry;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L17-L17) 


```solidity

File: /src/blast/BlastWrappers.sol

45:     address private immutable _governor;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L45-L45) 


```solidity

File: /src/mimswap/MagicLP.sol

61:     MagicLP public immutable implementation;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L61-L61) 


```solidity

File: /src/mimswap/periphery/Router.sol

33:     IWETH public immutable weth;

34:     IFactory public immutable factory;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L33-L33) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L34-L34)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

10:     IMagicLP public immutable pair;

11:     IAggregator public immutable baseOracle;

12:     IAggregator public immutable quoteOracle;

13:     uint8 public immutable baseDecimals;

14:     uint8 public immutable quoteDecimals;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L10-L10) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L11-L11), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L14-L14)


```solidity

File: /src/staking/LockingMultiRewards.sol

83:     uint256 public immutable maxLocks;

84:     uint256 public immutable lockingBoostMultiplerInBips;

85:     uint256 public immutable rewardsDuration;

86:     uint256 public immutable lockDuration;

87:     address public immutable stakingToken;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L83-L83) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L85-L85), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L86-L86), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L87-L87)


</details>


### [NC&#x2011;81] `private`/`public` function name should start with underscore 
According to solidity style guide, Private or Public function name should start with underscore.


*There are 25 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

//@audit `isOwner` is not in CamelCase
103:     function isOwner(address _account) internal view override returns (bool) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L103-L103) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

//@audit `configure` is not in CamelCase
10:     function configure() internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L10-L10) 


```solidity

File: /src/blast/libraries/BlastYields.sol

//@audit `enableTokenClaimable` is not in CamelCase
20:     function enableTokenClaimable(address token) internal {

//@audit `configureDefaultClaimables` is not in CamelCase
29:     function configureDefaultClaimables(address governor_) internal {

//@audit `claimMaxGasYields` is not in CamelCase
38:     function claimMaxGasYields(address recipient) internal returns (uint256) {

//@audit `claimMaxGasYields` is not in CamelCase
42:     function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {

//@audit `claimAllNativeYields` is not in CamelCase
51:     function claimAllNativeYields(address recipient) internal returns (uint256 amount) {

//@audit `claimAllNativeYields` is not in CamelCase
55:     function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {

//@audit `claimNativeYields` is not in CamelCase
60:     function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {

//@audit `claimAllTokenYields` is not in CamelCase
70:     function claimAllTokenYields(address token, address recipient) internal returns (uint256 amount) {

//@audit `claimTokenYields` is not in CamelCase
75:     function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {

//@audit `callPrecompile` is not in CamelCase
86:     function callPrecompile(bytes calldata data) internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L20-L20) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L60-L60), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L86-L86)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

//@audit `mulFloor` is not in CamelCase
23:     function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {

//@audit `mulCeil` is not in CamelCase
27:     function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {

//@audit `divFloor` is not in CamelCase
31:     function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {

//@audit `divCeil` is not in CamelCase
35:     function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {

//@audit `reciprocalFloor` is not in CamelCase
39:     function reciprocalFloor(uint256 target) internal pure returns (uint256) {

//@audit `reciprocalCeil` is not in CamelCase
43:     function reciprocalCeil(uint256 target) internal pure returns (uint256) {

//@audit `powFloor` is not in CamelCase
47:     function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L47-L47)


```solidity

File: /src/mimswap/libraries/Math.sol

//@audit `divCeil` is not in CamelCase
19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

//@audit `sqrt` is not in CamelCase
29:     function sqrt(uint256 x) internal pure returns (uint256 y) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L19-L19) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L29-L29)


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

//@audit `sellBaseToken` is not in CamelCase
39:     function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {

//@audit `sellQuoteToken` is not in CamelCase
76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {

//@audit `adjustedTarget` is not in CamelCase
190:     function adjustedTarget(PMMState memory state) internal pure {

//@audit `getMidPrice` is not in CamelCase
203:     function getMidPrice(PMMState memory state) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L39-L39) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L203-L203)


</details>


### [NC&#x2011;82] Use the latest Solidity version for better security 
Using the latest solidity version will help avoid old compiler related vulnerabilities


*There are 20 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L2-L2) 


```solidity

File: /src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L3-L3) 


```solidity

File: /src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L2-L2) 


```solidity

File: /src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L3-L3) 


```solidity

File: /src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L2-L2) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L2-L2) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L2-L2) 


```solidity

File: /src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L2-L2) 


```solidity

File: /src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L2) 


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L7-L7) 


```solidity

File: /src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L8-L8) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L8-L8) 


```solidity

File: /src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L2-L2) 


```solidity

File: /src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L2-L2) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L2-L2) 


```solidity

File: /src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L2-L2) 


</details>


### [NC&#x2011;83] Consider adding formal verification proofs 
Consider using formal verification to mathematically prove that your code does what is intended, and does not have any edge cases with unexpected behavior. The solidity compiler itself has this functionality [built in](https://docs.soliditylang.org/en/latest/smtchecker.html#smtchecker-and-formal-verification)


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

@audit Should implement invariant tests
1: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L1-L1) 


</details>


### [NC&#x2011;84] Missing zero address check in functions with address parameters 
Adding a zero address check for each address type parameter can prevent errors.


*There are 13 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/periphery/Factory.sol

//@audit token0, token1,  are not checked
53:     function getPoolCount(address token0, address token1) external view returns (uint256) {

//@audit creator,  are not checked
57:     function getUserPoolCount(address creator) external view returns (uint256) {

//@audit creator, baseToken, quoteToken,  are not checked
120:     function removePool(
121:         address creator,
122:         address baseToken,
123:         address quoteToken,
124:         uint256 poolIndex,
125:         uint256 userPoolIndex
126:     ) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L53-L53) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L126)


```solidity

File: /src/mimswap/periphery/Router.sol

//@audit path,  are not checked
586:     function _validatePath(address[] calldata path) internal pure {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L586-L586) 


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit _stakingToken,  are not checked
112:     constructor(
113:         address _stakingToken,
114:         uint256 _lockingBoostMultiplerInBips,
115:         uint256 _rewardsDuration,
116:         uint256 _lockDuration,
117:         address _owner
118:     ) OperatableV2(_owner) {

//@audit token,  are not checked
199:     function rewardData(address token) external view returns (Reward memory) {

//@audit user,  are not checked
211:     function balances(address user) external view returns (Balances memory) {

//@audit user,  are not checked
215:     function userRewardLock(address user) external view returns (RewardLock memory) {

//@audit user,  are not checked
219:     function userLocks(address user) external view returns (LockedBalance[] memory) {

//@audit user,  are not checked
223:     function userLocksLength(address user) external view returns (uint256) {

//@audit user,  are not checked
227:     function locked(address user) external view returns (uint256) {

//@audit user,  are not checked
231:     function unlocked(address user) external view returns (uint256) {

//@audit user,  are not checked
239:     function balanceOf(address user) public view returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L112-L118) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L199-L199), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L211-L211), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L219-L219), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L223-L223), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L227-L227), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L231-L231), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L239-L239)


</details>


### [NC&#x2011;85] Use a struct to encapsulate multiple function parameters 
If a function has too many parameters, replacing them with a struct can improve code readability and maintainability, increase reusability, and reduce the likelihood of errors when passing the parameters.


*There are 26 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

36:     function _onBeforeDeposit(
37:         IERC20 token,
38:         address /*from*/,
39:         address /*to*/,
40:         uint256 /*amount*/,
41:         uint256 /*share*/
42:     ) internal view override {
43:         if (!enabledTokens[address(token)]) {
44:             revert ErrUnsupportedToken();
45:         }
46:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L36-L46) 


```solidity

File: /src/mimswap/MagicLP.sol

091:     function init(
092:         address baseTokenAddress,
093:         address quoteTokenAddress,
094:         uint256 lpFeeRate,
095:         address mtFeeRateModel,
096:         uint256 i,
097:         uint256 k
098:     ) external {
099:         if (_INITIALIZED_) {
100:             revert ErrInitialized();
101:         }
102:         if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
103:             revert ErrZeroAddress();
104:         }
105:         if (baseTokenAddress == quoteTokenAddress) {
106:             revert ErrBaseQuoteSame();
107:         }
108:         if (i == 0 || i > MAX_I) {
109:             revert ErrInvalidI();
110:         }
111:         if (k > MAX_K) {
112:             revert ErrInvalidK();
113:         }
114:         if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {
115:             revert ErrInvalidLPFeeRate();
116:         }
117: 
118:         _INITIALIZED_ = true;
119:         _BASE_TOKEN_ = baseTokenAddress;
120:         _QUOTE_TOKEN_ = quoteTokenAddress;
121:         _I_ = i;
122:         _K_ = k;
123:         _LP_FEE_RATE_ = lpFeeRate;
124:         _MT_FEE_RATE_MODEL_ = IFeeRateModel(mtFeeRateModel);
125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);
126: 
127:         _afterInitialized();
128:     }

413:     function sellShares(
414:         uint256 shareAmount,
415:         address to,
416:         uint256 baseMinAmount,
417:         uint256 quoteMinAmount,
418:         bytes calldata data,
419:         uint256 deadline
420:     ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {
421:         if (deadline < block.timestamp) {
422:             revert ErrExpired();
423:         }
424:         if (shareAmount > balanceOf(msg.sender)) {
425:             revert ErrNotEnough();
426:         }
427:         if (to == address(this)) {
428:             revert ErrSellBackNotAllowed();
429:         }
430: 
431:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
432:         uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
433:         uint256 totalShares = totalSupply();
434: 
435:         baseAmount = (baseBalance * shareAmount) / totalShares;
436:         quoteAmount = (quoteBalance * shareAmount) / totalShares;
437: 
438:         _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
439:         _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
440: 
441:         if (baseAmount < baseMinAmount || quoteAmount < quoteMinAmount) {
442:             revert ErrWithdrawNotEnough();
443:         }
444: 
445:         _burn(msg.sender, shareAmount);
446:         _transferBaseOut(to, baseAmount);
447:         _transferQuoteOut(to, quoteAmount);
448:         _sync();
449: 
450:         if (data.length > 0) {
451:             ICallee(to).SellShareCall(msg.sender, shareAmount, baseAmount, quoteAmount, data);
452:         }
453: 
454:         emit SellShares(msg.sender, to, shareAmount, balanceOf(msg.sender));
455:     }

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L91-L128) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L413-L455), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L502)


```solidity

File: /src/mimswap/libraries/Math.sol

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {
52:         if (V0 == 0) {
53:             revert ErrIsZero();
54:         }
55: 
56:         uint256 fairAmount = i * (V1 - V2); // i*delta
57: 
58:         if (k == 0) {
59:             return fairAmount / DecimalMath.ONE;
60:         }
61: 
62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);
63:         uint256 penalty = DecimalMath.mulFloor(k, V0V0V1V2); // k(V0^2/V1/V2)
64:         return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;
65:     }

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
132:         if (V0 == 0) {
133:             revert ErrIsZero();
134:         }
135: 
136:         if (delta == 0) {
137:             return 0;
138:         }
139: 
140:         if (k == 0) {
141:             return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);
142:         }
143: 
144:         if (k == DecimalMath.ONE) {
145:             // if k==1
146:             // Q2=Q1/(1+ideltaBQ1/Q0/Q0)
147:             // temp = ideltaBQ1/Q0/Q0
148:             // Q2 = Q1/(1+temp)
149:             // Q1-Q2 = Q1*(1-1/(1+temp)) = Q1*(temp/(1+temp))
150:             // uint256 temp = i.mul(delta).mul(V1).div(V0.mul(V0));
151:             uint256 temp;
152:             uint256 idelta = i * delta;
153:             if (idelta == 0) {
154:                 temp = 0;
155:             } else if ((idelta * V1) / idelta == V1) {
156:                 temp = (idelta * V1) / (V0 * V0);
157:             } else {
158:                 temp = (((delta * V1) / V0) * i) / V0;
159:             }
160:             return (V1 * temp) / (temp + DecimalMath.ONE);
161:         }
162: 
163:         // calculate -b value and sig
164:         // b = kQ0^2/Q1-i*deltaB-(1-k)Q1
165:         // part1 = (1-k)Q1 >=0
166:         // part2 = kQ0^2/Q1-i*deltaB >=0
167:         // bAbs = abs(part1-part2)
168:         // if part1>part2 => b is negative => bSig is false
169:         // if part2>part1 => b is positive => bSig is true
170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
171:         uint256 bAbs = (DecimalMath.ONE - k) * V1; // (1-k)Q1
172: 
173:         bool bSig;
174:         if (bAbs >= part2) {
175:             bAbs = bAbs - part2;
176:             bSig = false;
177:         } else {
178:             bAbs = part2 - bAbs;
179:             bSig = true;
180:         }
181:         bAbs = bAbs / DecimalMath.ONE;
182: 
183:         // calculate sqrt
184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
185:         squareRoot = sqrt((bAbs * bAbs) + squareRoot); // sqrt(b*b+4(1-k)kQ0*Q0)
186: 
187:         // final res
188:         uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
189:         uint256 numerator;
190:         if (bSig) {
191:             numerator = squareRoot - bAbs;
192:             if (numerator == 0) {
193:                 revert ErrIsZero();
194:             }
195:         } else {
196:             numerator = bAbs + squareRoot;
197:         }
198: 
199:         uint256 V2 = DecimalMath.divCeil(numerator, denominator);
200:         if (V2 > V1) {
201:             return 0;
202:         } else {
203:             return V1 - V2;
204:         }
205:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L51-L65) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L131-L205)


```solidity

File: /src/mimswap/periphery/Factory.sol

65:     function predictDeterministicAddress(
66:         address creator,
67:         address baseToken_,
68:         address quoteToken_,
69:         uint256 lpFeeRate_,
70:         uint256 i_,
71:         uint256 k_
72:     ) public view returns (address) {
73:         return
74:             LibClone.predictDeterministicAddress(
75:                 implementation,
76:                 _computeSalt(creator, baseToken_, quoteToken_, lpFeeRate_, i_, k_),
77:                 address(this)
78:             );
79:     }

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
82:         address creator = tx.origin;
83: 
84:         bytes32 salt = _computeSalt(creator, baseToken_, quoteToken_, lpFeeRate_, i_, k_);
85:         clone = LibClone.cloneDeterministic(address(implementation), salt);
86:         IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
87: 
88:         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
89:         _addPool(creator, baseToken_, quoteToken_, clone);
90:     }

120:     function removePool(
121:         address creator,
122:         address baseToken,
123:         address quoteToken,
124:         uint256 poolIndex,
125:         uint256 userPoolIndex
126:     ) external onlyOwner {
127:         address[] storage _pools = pools[baseToken][quoteToken];
128:         address pool = _pools[poolIndex];
129:         address[] storage _userPools = userPools[creator];
130: 
131:         _pools[poolIndex] = _pools[_pools.length - 1];
132:         _pools.pop();
133: 
134:         if (_userPools[userPoolIndex] != pool) {
135:             revert ErrInvalidUserPoolIndex();
136:         }
137: 
138:         _userPools[userPoolIndex] = _userPools[_userPools.length - 1];
139:         _userPools.pop();
140: 
141:         emit LogPoolRemoved(pool);
142:     }

155:     function _computeSalt(
156:         address sender_,
157:         address baseToken_,
158:         address quoteToken_,
159:         uint256 lpFeeRate_,
160:         uint256 i_,
161:         uint256 k_
162:     ) internal view returns (bytes32) {
163:         return keccak256(abi.encodePacked(sender_, implementation, baseToken_, quoteToken_, lpFeeRate_, i_, k_));
164:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L65-L79) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L90), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L142), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L155-L164)


```solidity

File: /src/mimswap/periphery/Router.sol

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
64:         _validateDecimals(IERC20Metadata(baseToken).decimals(), IERC20Metadata(quoteToken).decimals());
65: 
66:         clone = IFactory(factory).create(baseToken, quoteToken, lpFeeRate, i, k);
67: 
68:         baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);
69:         quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);
70:         (shares, , ) = IMagicLP(clone).buyShares(to);
71:     }

73:     function createPoolETH(
74:         address token,
75:         bool useTokenAsQuote,
76:         uint256 lpFeeRate,
77:         uint256 i,
78:         uint256 k,
79:         address to,
80:         uint256 tokenInAmount
81:     ) external payable returns (address clone, uint256 shares) {
82:         if (useTokenAsQuote) {
83:             _validateDecimals(18, IERC20Metadata(token).decimals());
84:         } else {
85:             _validateDecimals(IERC20Metadata(token).decimals(), 18);
86:         }
87: 
88:         clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);
89: 
90:         weth.deposit{value: msg.value}();
91:         token.safeTransferFrom(msg.sender, clone, tokenInAmount);
92:         address(weth).safeTransferFrom(address(this), clone, msg.value);
93:         (shares, , ) = IMagicLP(clone).buyShares(to);
94:     }

162:     function addLiquidity(
163:         address lp,
164:         address to,
165:         uint256 baseInAmount,
166:         uint256 quoteInAmount,
167:         uint256 minimumShares,
168:         uint256 deadline
169:     ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
170:         (baseAdjustedInAmount, quoteAdjustedInAmount) = _adjustAddLiquidity(lp, baseInAmount, quoteInAmount);
171: 
172:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);
173:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);
174: 
175:         shares = _addLiquidity(lp, to, minimumShares);
176:     }

178:     function addLiquidityUnsafe(
179:         address lp,
180:         address to,
181:         uint256 baseInAmount,
182:         uint256 quoteInAmount,
183:         uint256 minimumShares,
184:         uint256 deadline
185:     ) external ensureDeadline(deadline) returns (uint256 shares) {
186:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);
187:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);
188: 
189:         return _addLiquidity(lp, to, minimumShares);
190:     }

192:     function addLiquidityETH(
193:         address lp,
194:         address to,
195:         address payable refundTo,
196:         uint256 tokenInAmount,
197:         uint256 minimumShares,
198:         uint256 deadline
199:     ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
200:         uint256 wethAdjustedAmount;
201:         uint256 tokenAdjustedAmount;
202:         address token = IMagicLP(lp)._BASE_TOKEN_();
203:         if (token == address(weth)) {
204:             token = IMagicLP(lp)._QUOTE_TOKEN_();
205:             (baseAdjustedInAmount, quoteAdjustedInAmount) = _adjustAddLiquidity(lp, msg.value, tokenInAmount);
206:             wethAdjustedAmount = baseAdjustedInAmount;
207:             tokenAdjustedAmount = quoteAdjustedInAmount;
208:         } else if (IMagicLP(lp)._QUOTE_TOKEN_() == address(weth)) {
209:             (baseAdjustedInAmount, quoteAdjustedInAmount) = _adjustAddLiquidity(lp, tokenInAmount, msg.value);
210:             wethAdjustedAmount = quoteAdjustedInAmount;
211:             tokenAdjustedAmount = baseAdjustedInAmount;
212:         } else {
213:             revert ErrNotETHLP();
214:         }
215: 
216:         weth.deposit{value: wethAdjustedAmount}();
217:         address(weth).safeTransfer(lp, wethAdjustedAmount);
218: 
219:         // Refund unused ETH
220:         if (msg.value > wethAdjustedAmount) {
221:             refundTo.safeTransferETH(msg.value - wethAdjustedAmount);
222:         }
223: 
224:         token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);
225: 
226:         shares = _addLiquidity(lp, to, minimumShares);
227:     }

229:     function addLiquidityETHUnsafe(
230:         address lp,
231:         address to,
232:         uint256 tokenInAmount,
233:         uint256 minimumShares,
234:         uint256 deadline
235:     ) external payable ensureDeadline(deadline) returns (uint256 shares) {
236:         address token = IMagicLP(lp)._BASE_TOKEN_();
237:         if (token == address(weth)) {
238:             token = IMagicLP(lp)._QUOTE_TOKEN_();
239:         } else if (IMagicLP(lp)._QUOTE_TOKEN_() != address(weth)) {
240:             revert ErrNotETHLP();
241:         }
242: 
243:         weth.deposit{value: msg.value}();
244:         address(weth).safeTransfer(lp, msg.value);
245: 
246:         token.safeTransferFrom(msg.sender, lp, tokenInAmount);
247: 
248:         return _addLiquidity(lp, to, minimumShares);
249:     }

261:     function removeLiquidity(
262:         address lp,
263:         address to,
264:         uint256 sharesIn,
265:         uint256 minimumBaseAmount,
266:         uint256 minimumQuoteAmount,
267:         uint256 deadline
268:     ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
269:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);
270: 
271:         return IMagicLP(lp).sellShares(sharesIn, to, minimumBaseAmount, minimumQuoteAmount, "", deadline);
272:     }

274:     function removeLiquidityETH(
275:         address lp,
276:         address to,
277:         uint256 sharesIn,
278:         uint256 minimumETHAmount,
279:         uint256 minimumTokenAmount,
280:         uint256 deadline
281:     ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {
282:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);
283: 
284:         address token = IMagicLP(lp)._BASE_TOKEN_();
285:         if (token == address(weth)) {
286:             token = IMagicLP(lp)._QUOTE_TOKEN_();
287:             (ethAmountOut, tokenAmountOut) = IMagicLP(lp).sellShares(
288:                 sharesIn,
289:                 address(this),
290:                 minimumETHAmount,
291:                 minimumTokenAmount,
292:                 "",
293:                 deadline
294:             );
295:         } else if (IMagicLP(lp)._QUOTE_TOKEN_() == address(weth)) {
296:             (tokenAmountOut, ethAmountOut) = IMagicLP(lp).sellShares(
297:                 sharesIn,
298:                 address(this),
299:                 minimumTokenAmount,
300:                 minimumETHAmount,
301:                 "",
302:                 deadline
303:             );
304:         } else {
305:             revert ErrNotETHLP();
306:         }
307: 
308:         weth.withdraw(ethAmountOut);
309:         to.safeTransferETH(ethAmountOut);
310: 
311:         token.safeTransfer(to, tokenAmountOut);
312:     }

314:     function swapTokensForTokens(
315:         address to,
316:         uint256 amountIn,
317:         address[] calldata path,
318:         uint256 directions,
319:         uint256 minimumOut,
320:         uint256 deadline
321:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {
322:         _validatePath(path);
323: 
324:         address firstLp = path[0];
325: 
326:         // Transfer to the first LP
327:         if (directions & 1 == 0) {
328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
329:         } else {
330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
331:         }
332: 
333:         return _swap(to, path, directions, minimumOut);
334:     }

336:     function swapETHForTokens(
337:         address to,
338:         address[] calldata path,
339:         uint256 directions,
340:         uint256 minimumOut,
341:         uint256 deadline
342:     ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
343:         _validatePath(path);
344: 
345:         address firstLp = path[0];
346:         address inToken;
347: 
348:         if (directions & 1 == 0) {
349:             inToken = IMagicLP(firstLp)._BASE_TOKEN_();
350:         } else {
351:             inToken = IMagicLP(firstLp)._QUOTE_TOKEN_();
352:         }
353: 
354:         // Transfer to the first LP
355:         if (inToken != address(weth)) {
356:             revert ErrInTokenNotETH();
357:         }
358: 
359:         weth.deposit{value: msg.value}();
360:         inToken.safeTransfer(address(firstLp), msg.value);
361: 
362:         return _swap(to, path, directions, minimumOut);
363:     }

365:     function swapTokensForETH(
366:         address to,
367:         uint256 amountIn,
368:         address[] calldata path,
369:         uint256 directions,
370:         uint256 minimumOut,
371:         uint256 deadline
372:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {
373:         _validatePath(path);
374: 
375:         uint256 lastLpIndex = path.length - 1;
376:         address lastLp = path[lastLpIndex];
377:         address outToken;
378: 
379:         if ((directions >> lastLpIndex) & 1 == 0) {
380:             outToken = IMagicLP(lastLp)._QUOTE_TOKEN_();
381:         } else {
382:             outToken = IMagicLP(lastLp)._BASE_TOKEN_();
383:         }
384: 
385:         if (outToken != address(weth)) {
386:             revert ErrOutTokenNotETH();
387:         }
388: 
389:         address firstLp = path[0];
390: 
391:         // Transfer to the first LP
392:         if (directions & 1 == 0) {
393:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
394:         } else {
395:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
396:         }
397: 
398:         amountOut = _swap(address(this), path, directions, minimumOut);
399:         weth.withdraw(amountOut);
400: 
401:         to.safeTransferETH(amountOut);
402:     }

404:     function sellBaseTokensForTokens(
405:         address lp,
406:         address to,
407:         uint256 amountIn,
408:         uint256 minimumOut,
409:         uint256 deadline
410:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {
411:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
412:         return _sellBase(lp, to, minimumOut);
413:     }

432:     function sellBaseTokensForETH(
433:         address lp,
434:         address to,
435:         uint256 amountIn,
436:         uint256 minimumOut,
437:         uint256 deadline
438:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {
439:         if (IMagicLP(lp)._QUOTE_TOKEN_() != address(weth)) {
440:             revert ErrInvalidQuoteToken();
441:         }
442: 
443:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
444:         amountOut = _sellBase(lp, address(this), minimumOut);
445:         weth.withdraw(amountOut);
446:         to.safeTransferETH(amountOut);
447:     }

449:     function sellQuoteTokensForTokens(
450:         address lp,
451:         address to,
452:         uint256 amountIn,
453:         uint256 minimumOut,
454:         uint256 deadline
455:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {
456:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
457: 
458:         return _sellQuote(lp, to, minimumOut);
459:     }

478:     function sellQuoteTokensForETH(
479:         address lp,
480:         address to,
481:         uint256 amountIn,
482:         uint256 minimumOut,
483:         uint256 deadline
484:     ) external ensureDeadline(deadline) returns (uint256 amountOut) {
485:         if (IMagicLP(lp)._BASE_TOKEN_() != address(weth)) {
486:             revert ErrInvalidBaseToken();
487:         }
488: 
489:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
490:         amountOut = _sellQuote(lp, address(this), minimumOut);
491:         weth.withdraw(amountOut);
492:         to.safeTransferETH(amountOut);
493:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L54-L71) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L73-L94), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L162-L176), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L178-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L192-L227), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L249), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L261-L272), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L274-L312), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L314-L334), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L336-L363), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L365-L402), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L413), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L432-L447), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L449-L459), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L478-L493)


```solidity

File: /src/staking/LockingMultiRewards.sol

112:     constructor(
113:         address _stakingToken,
114:         uint256 _lockingBoostMultiplerInBips,
115:         uint256 _rewardsDuration,
116:         uint256 _lockDuration,
117:         address _owner
118:     ) OperatableV2(_owner) {
119:         if (_lockingBoostMultiplerInBips <= BIPS) {
120:             revert ErrInvalidBoostMultiplier();
121:         }
122: 
123:         if (_lockDuration < MIN_LOCK_DURATION) {
124:             revert ErrInvalidLockDuration();
125:         }
126: 
127:         if (_rewardsDuration < MIN_REWARDS_DURATION) {
128:             revert ErrInvalidRewardDuration();
129:         }
130: 
131:         if (_lockDuration % _rewardsDuration != 0) {
132:             revert ErrInvalidDurationRatio();
133:         }
134: 
135:         stakingToken = _stakingToken;
136:         lockingBoostMultiplerInBips = _lockingBoostMultiplerInBips;
137:         rewardsDuration = _rewardsDuration;
138:         lockDuration = _lockDuration;
139: 
140:         // kocks are combined into the same `rewardsDuration` epoch. So, if
141:         // a user stake with locking every `rewardsDuration` this should reach the
142:         // maximum number of possible simultaneous because the first lock gets expired,
143:         // freeing up a slot.
144:         maxLocks = _lockDuration / _rewardsDuration;
145:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L112-L145) 


</details>


### [NC&#x2011;86] Use `@inheritdoc` for overridden functions 



*There are 14 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

36:     function _onBeforeDeposit(

97:     /// @dev Called on DegenBox's constructor

103:     function isOwner(address _account) internal view override returns (bool) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L36-L36) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L97-L97), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L103-L103)


```solidity

File: /src/blast/BlastMagicLP.sol

36:     /// VIEWS

95:     /// INTERNALS


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L36-L36) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L95-L95)


```solidity

File: /src/blast/BlastOnboarding.sol

80:     receive() external payable override {

223:     /// PROXY IMPLEMENTATION


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L80-L80) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L223-L223)


```solidity

File: /src/blast/BlastWrappers.sol

59:     function init(bytes calldata data) public payable override {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L59-L59) 


```solidity

File: /src/mimswap/MagicLP.sol

152:     /// VIEWS

159:     function symbol() public pure override returns (string memory) {

163:     function decimals() public view override returns (uint8) {

593:     function _mint(address to, uint256 amount) internal override {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L152-L152) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L159-L159), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L163-L163), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L593-L593)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

29:     function decimals() external pure override returns (uint8) {

37:     function latestAnswer() public view override returns (int256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L29-L29) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L37-L37)


</details>


### [NC&#x2011;87] Multiple mappings with same keys can be combined into a single struct mapping for readability 
Well-organized data structures make code reviews easier, which may lead to fewer bugs. Consider combining related mappings into mappings to structs, so it's clear what data is related.


*There are 13 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

36:     mapping(address token => bool) public supportedTokens;

37:     mapping(address token => Balances) public totals;

38:     mapping(address token => uint256 cap) public caps;

41:     mapping(address user => mapping(address token => Balances)) public balances;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L36-L36) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L41-L41)


```solidity

File: /src/mimswap/periphery/Factory.sol

35:     mapping(address base => mapping(address quote => address[] pools)) public pools;

36:     mapping(address creator => address[] pools) public userPools;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L35-L35) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L36-L36)


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L89-L89) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L90-L90), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L91-L91), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L92-L92), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L94-L94), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L95-L95), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L96-L96)


</details>


### [NC&#x2011;88] constructor should emit an event 
Use events to signal significant changes to off-chain monitoring tools.


*There are 16 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

7:     constructor() {
8:         BlastPoints.configure();
9:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L7-L9) 


```solidity

File: /src/blast/BlastBox.sol

24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
25:         if (feeTo_ == address(0)) {
26:             revert ErrZeroAddress();
27:         }
28:         if (address(registry_) == address(0)) {
29:             revert ErrZeroAddress();
30:         }
31: 
32:         registry = registry_;
33:         feeTo = feeTo_;
34:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L24-L34) 


```solidity

File: /src/blast/BlastGovernor.sol

15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {
16:         if (feeTo_ == address(0)) {
17:             revert ErrZeroAddress();
18:         }
19: 
20:         feeTo = feeTo_;
21:         BlastYields.configureDefaultClaimables(address(this));
22:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L15-L22) 


```solidity

File: /src/blast/BlastMagicLP.sol

23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
24:         if (feeTo_ == address(0)) {
25:             revert ErrZeroAddress();
26:         }
27:         if (address(registry_) == address(0)) {
28:             revert ErrZeroAddress();
29:         }
30: 
31:         registry = registry_;
32:         feeTo = feeTo_;
33:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L23-L33) 


```solidity

File: /src/blast/BlastOnboarding.sol

58:     constructor() Owned(msg.sender) {
59:         BlastYields.configureDefaultClaimables(address(this));
60:         BlastPoints.configure();
61:     }

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {
85:         if (address(registry_) == address(0)) {
86:             revert ErrZeroAddress();
87:         }
88: 
89:         if (feeTo_ == address(0)) {
90:             revert ErrZeroAddress();
91:         }
92: 
93:         registry = registry_;
94:         feeTo = feeTo_;
95:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L58-L61) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L84-L95)


```solidity

File: /src/blast/BlastTokenRegistry.sol

12:     constructor(address _owner) Owned(_owner) {}


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L12-L12) 


```solidity

File: /src/blast/BlastWrappers.sol

20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
21:         if (governor_ == address(0)) {
22:             revert ErrZeroAddress();
23:         }
24:         BlastYields.configureDefaultClaimables(governor_);
25:     }

29:     constructor(
30:         address implementation_,
31:         IFeeRateModel maintainerFeeRateModel_,
32:         address owner_,
33:         address governor_
34:     ) Factory(implementation_, maintainerFeeRateModel_, owner_) {
35:         if (governor_ == address(0)) {
36:             revert ErrZeroAddress();
37:         }
38:         BlastYields.configureDefaultClaimables(governor_);
39:     }

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
48:         if (governor_ == address(0)) {
49:             revert ErrZeroAddress();
50:         }
51:         if (governor_ == address(this)) {
52:             revert ErrInvalidGovernorAddress();
53:         }
54: 
55:         _governor = governor_;
56:         _setupBlacklist();
57:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L20-L25) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L29-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L47-L57)


```solidity

File: /src/mimswap/MagicLP.sol

84:     constructor(address owner_) Owned(owner_) {
85:         implementation = this;
86: 
87:         // prevents the implementation contract initialization
88:         _INITIALIZED_ = true;
89:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L84-L89) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

22:     constructor(address maintainer_, address owner_) Owned(owner_) {
23:         if (maintainer_ == address(0)) {
24:             revert ErrZeroAddress();
25:         }
26: 
27:         maintainer = maintainer_;
28:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L22-L28) 


```solidity

File: /src/mimswap/periphery/Factory.sol

38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
39:         if (implementation_ == address(0)) {
40:             revert ErrZeroAddress();
41:         }
42:         if (address(maintainerFeeRateModel_) == address(0)) {
43:             revert ErrZeroAddress();
44:         }
45:         implementation = implementation_;
46:         maintainerFeeRateModel = maintainerFeeRateModel_;
47:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L38-L47) 


```solidity

File: /src/mimswap/periphery/Router.sol

38:     constructor(IWETH weth_, IFactory factory_) {
39:         if (address(weth_) == address(0) || address(factory_) == address(0)) {
40:             revert ErrZeroAddress();
41:         }
42: 
43:         weth = weth_;
44:         factory = factory_;
45:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L38-L45) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
22:         pair = pair_;
23:         baseOracle = baseOracle_;
24:         quoteOracle = quoteOracle_;
25:         baseDecimals = IERC20Metadata(pair_._BASE_TOKEN_()).decimals();
26:         quoteDecimals = IERC20Metadata(pair_._QUOTE_TOKEN_()).decimals();
27:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L21-L27) 


```solidity

File: /src/staking/LockingMultiRewards.sol

112:     constructor(
113:         address _stakingToken,
114:         uint256 _lockingBoostMultiplerInBips,
115:         uint256 _rewardsDuration,
116:         uint256 _lockDuration,
117:         address _owner
118:     ) OperatableV2(_owner) {
119:         if (_lockingBoostMultiplerInBips <= BIPS) {
120:             revert ErrInvalidBoostMultiplier();
121:         }
122: 
123:         if (_lockDuration < MIN_LOCK_DURATION) {
124:             revert ErrInvalidLockDuration();
125:         }
126: 
127:         if (_rewardsDuration < MIN_REWARDS_DURATION) {
128:             revert ErrInvalidRewardDuration();
129:         }
130: 
131:         if (_lockDuration % _rewardsDuration != 0) {
132:             revert ErrInvalidDurationRatio();
133:         }
134: 
135:         stakingToken = _stakingToken;
136:         lockingBoostMultiplerInBips = _lockingBoostMultiplerInBips;
137:         rewardsDuration = _rewardsDuration;
138:         lockDuration = _lockDuration;
139: 
140:         // kocks are combined into the same `rewardsDuration` epoch. So, if
141:         // a user stake with locking every `rewardsDuration` this should reach the
142:         // maximum number of possible simultaneous because the first lock gets expired,
143:         // freeing up a slot.
144:         maxLocks = _lockDuration / _rewardsDuration;
145:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L112-L145) 


</details>


### [NC&#x2011;89] Complex functions should include comments 
Large and/or complex functions should include comments to make them easier to understand and reduce margin for error.


*There are 11 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L101-L101) 


```solidity

File: /src/mimswap/MagicLP.sol

91:     function init(

413:     function sellShares(

470:     function setParameters(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L91-L91) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L413-L413), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L470)


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

76:     function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L76-L76) 


```solidity

File: /src/mimswap/periphery/Factory.sol

120:     function removePool(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L120) 


```solidity

File: /src/mimswap/periphery/Router.sol

73:     function createPoolETH(

112:     function previewAddLiquidity(

229:     function addLiquidityETHUnsafe(

274:     function removeLiquidityETH(

509:     function _adjustAddLiquidity(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L73-L73) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L112-L112), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L229), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L274-L274), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L509-L509)


</details>


### [NC&#x2011;90] Make use of Solidiy's `using` keyword 
The directive `using A for B` can be used to attach functions (`A`) as operators to user-defined value types or as member functions to any type (`B`). The member functions receive the object they are called on as their first parameter (like the `self` variable in Python). The operator functions receive operands as parameters.  Doing so improves readability, makes debugging easier, and promotes modularity and reusability in the code.


*There are 97 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

8:         BlastPoints.configure();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L8-L8) 


```solidity

File: /src/blast/BlastBox.sol

53:         return BlastYields.claimMaxGasYields(feeTo);

69:         BlastYields.callPrecompile(data);

99:         BlastYields.configureDefaultClaimables(address(this));

100:         BlastPoints.configure();

61:         amount = BlastYields.claimAllTokenYields(token_, feeTo);

87:             BlastYields.enableTokenClaimable(token);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L53-L53) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L69-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L99-L99), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L100-L100), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L61-L61), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L87-L87)


```solidity

File: /src/blast/BlastGovernor.sol

21:         BlastYields.configureDefaultClaimables(address(this));

29:         return BlastYields.claimAllNativeYields(contractAddress, feeTo);

33:         return BlastYields.claimMaxGasYields(contractAddress, feeTo);

50:         BlastYields.callPrecompile(data);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L21-L21) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L50-L50)


```solidity

File: /src/blast/BlastMagicLP.sol

50:         return BlastYields.claimMaxGasYields(feeTo_);

73:         BlastYields.callPrecompile(data);

99:         BlastYields.configureDefaultClaimables(address(this));

100:         BlastPoints.configure();

106:             BlastYields.enableTokenClaimable(_BASE_TOKEN_);

110:             BlastYields.enableTokenClaimable(_QUOTE_TOKEN_);

57:             token0Amount = BlastYields.claimAllTokenYields(_BASE_TOKEN_, feeTo_);

60:             token1Amount = BlastYields.claimAllTokenYields(_QUOTE_TOKEN_, feeTo_);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L50-L50) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L99-L99), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L100-L100), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L106-L106), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L110-L110), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L60-L60)


```solidity

File: /src/blast/BlastOnboarding.sol

59:         BlastYields.configureDefaultClaimables(address(this));

60:         BlastPoints.configure();

157:         BlastYields.callPrecompile(data);

161:         return BlastYields.claimMaxGasYields(feeTo);

179:             BlastYields.enableTokenClaimable(token);

170:                 BlastYields.claimAllTokenYields(tokens[i], feeTo);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L59-L59) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L60-L60), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L157-L157), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L161-L161), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L179-L179), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L170-L170)


```solidity

File: /src/blast/BlastWrappers.sol

24:         BlastYields.configureDefaultClaimables(governor_);

38:         BlastYields.configureDefaultClaimables(governor_);

67:         BlastYields.configureDefaultClaimables(_governor);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L24-L24) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L67-L67)


```solidity

File: /src/blast/libraries/BlastYields.sol

87:         Address.functionCall(address(BLAST_YIELD_PRECOMPILE), data);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L87-L87) 


```solidity

File: /src/mimswap/MagicLP.sol

201:         PMMPricing.adjustedTarget(state);

216:         return PMMPricing.getMidPrice(getPMMState());

172:         (receiveQuoteAmount, newRState) = PMMPricing.sellBaseToken(state, payBaseAmount);

175:         mtFee = DecimalMath.mulFloor(receiveQuoteAmount, mtFeeRate);

185:         (receiveBaseAmount, newRState) = PMMPricing.sellQuoteToken(state, payQuoteAmount);

188:         mtFee = DecimalMath.mulFloor(receiveBaseAmount, mtFeeRate);

200:         state.R = PMMPricing.RState(_RState_);

176:         receiveQuoteAmount = receiveQuoteAmount - DecimalMath.mulFloor(receiveQuoteAmount, lpFeeRate) - mtFee;

189:         receiveBaseAmount = receiveBaseAmount - DecimalMath.mulFloor(receiveBaseAmount, lpFeeRate) - mtFee;

397:             uint256 baseInputRatio = DecimalMath.divFloor(baseInput, baseReserve);

398:             uint256 quoteInputRatio = DecimalMath.divFloor(quoteInput, quoteReserve);

400:             shares = DecimalMath.mulFloor(totalSupply(), mintRatio);

381:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;

381:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;

383:             _QUOTE_TARGET_ = DecimalMath.mulFloor(shares, _I_).toUint112();

402:             _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

403:             _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L201-L201) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L216-L216), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L172-L172), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L188-L188), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L200-L200), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L176-L176), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L189-L189), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L397-L397), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L398-L398), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L400-L400), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L381-L381), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L381-L381), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L383-L383), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L402-L402), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L403-L403)


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

14:         mtFeeRate = Math.divCeil(lpFeeRate, 2);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L14-L14) 


```solidity

File: /src/mimswap/libraries/Math.sol

62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

63:         uint256 penalty = DecimalMath.mulFloor(k, V0V0V1V2); // k(V0^2/V1/V2)

103:         return DecimalMath.mulFloor(V1, premium);

184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2

199:         uint256 V2 = DecimalMath.divCeil(numerator, denominator);

101:         uint256 premium = DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2) + DecimalMath.ONE;

184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2

81:             return V1 + DecimalMath.mulFloor(i, delta);

141:             return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);

141:             return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L62-L62) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L63-L63), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L103-L103), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L184-L184), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L199-L199), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L101-L101), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L184-L184), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L141-L141), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L141-L141)


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

116:         return Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q0, payBaseAmount, state.i, state.K);

129:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);

144:         return Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K);

157:         return Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q, payBaseAmount, state.i, state.K);

172:         return Math._GeneralIntegrate(state.B0, state.B + payBaseAmount, state.B, state.i, state.K);

185:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);

129:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);

144:         return Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K);

185:         return Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);

209:             uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);

211:             return DecimalMath.mulFloor(state.i, R);

205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);

207:             return DecimalMath.divFloor(state.i, R);

192:             state.Q0 = Math._SolveQuadraticFunctionForTarget(state.Q, state.B - state.B0, state.i, state.K);

194:             state.B0 = Math._SolveQuadraticFunctionForTarget(

210:             R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);

206:             R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);

197:                 DecimalMath.reciprocalFloor(state.i),


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L116-L116) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L129-L129), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L144-L144), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L157-L157), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L172-L172), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L129-L129), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L144-L144), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L209-L209), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L211-L211), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L205-L205), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L207-L207), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L192-L192), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L194-L194), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L210-L210), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L206-L206), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L197-L197)


```solidity

File: /src/mimswap/periphery/Factory.sol

74:             LibClone.predictDeterministicAddress(

85:         clone = LibClone.cloneDeterministic(address(implementation), salt);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L74-L74) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L85-L85)


```solidity

File: /src/mimswap/periphery/Router.sol

103:         quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);

101:         shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

101:         shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

148:             uint256 baseInputRatio = DecimalMath.divFloor(baseInAmount, baseReserve);

149:             uint256 quoteInputRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);

140:             quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);

523:             uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

525:             quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);

138:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;

528:                 uint256 baseIncreaseRatio = DecimalMath.divFloor(baseInAmount, baseReserve);

529:                 uint256 quoteIncreaseRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);

523:             uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

138:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;

156:                 baseAdjustedInAmount = DecimalMath.mulCeil(baseReserve, quoteInputRatio);

157:                 shares = DecimalMath.mulFloor(totalSupply, quoteInputRatio);

152:                 quoteAdjustedInAmount = DecimalMath.mulCeil(quoteReserve, baseInputRatio);

153:                 shares = DecimalMath.mulFloor(totalSupply, baseInputRatio);

535:                     baseAdjustedInAmount = DecimalMath.mulFloor(baseReserve, quoteIncreaseRatio);

532:                     quoteAdjustedInAmount = DecimalMath.mulFloor(quoteReserve, baseIncreaseRatio);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L103-L103) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L101-L101), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L101-L101), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L148-L148), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L149-L149), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L140-L140), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L523-L523), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L525-L525), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L138-L138), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L528-L528), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L529-L529), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L523-L523), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L138-L138), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L156-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L157-L157), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L152-L152), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L153-L153), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L535-L535), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L532-L532)


```solidity

File: /src/staking/LockingMultiRewards.sol

270:         return MathLib.min(block.timestamp, _rewardData[rewardToken].periodFinish);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L270-L270) 


</details>


### [NC&#x2011;91] Avoid using underscore at the end of a variable name 
The use of the underscore at the end of the variable name is unusual, consider refactoring it.


*There are 98 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

//@audit variable : `weth_`
24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

//@audit variable : `registry_`
24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

//@audit variable : `feeTo_`
24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

//@audit variable : `token_`
56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

//@audit variable : `feeTo_`
72:     function setFeeTo(address feeTo_) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L24-L24) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L72)


```solidity

File: /src/blast/BlastGovernor.sol

//@audit variable : `feeTo_`
15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L15-L15) 


```solidity

File: /src/blast/BlastMagicLP.sol

//@audit variable : `registry_`
23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

//@audit variable : `feeTo_`
23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

//@audit variable : `owner_`
23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

//@audit variable : `feeTo_`
80:     function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {

//@audit variable : `feeTo_`
48:         address feeTo_ = BlastMagicLP(address(implementation)).feeTo();

//@audit variable : `feeTo_`
54:         address feeTo_ = BlastMagicLP(address(implementation)).feeTo();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L48-L48), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L54-L54)


```solidity

File: /src/blast/BlastOnboarding.sol

//@audit variable : `registry_`
84:     constructor(BlastTokenRegistry registry_, address feeTo_) {

//@audit variable : `feeTo_`
84:     constructor(BlastTokenRegistry registry_, address feeTo_) {

//@audit variable : `lock_`
101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

//@audit variable : `feeTo_`
147:     function setFeeTo(address feeTo_) external onlyOwner {

//@audit variable : `bootstrapper_`
190:     function setBootstrapper(address bootstrapper_) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L84-L84) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L101-L101), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L147-L147), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L190)


```solidity

File: /src/blast/BlastWrappers.sol

//@audit variable : `weth_`
20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

//@audit variable : `governor_`
20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

//@audit variable : `implementation_`
30:         address implementation_,

//@audit variable : `maintainerFeeRateModel_`
31:         IFeeRateModel maintainerFeeRateModel_,

//@audit variable : `owner_`
32:         address owner_,

//@audit variable : `governor_`
33:         address governor_

//@audit variable : `box_`
47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {

//@audit variable : `mim_`
47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {

//@audit variable : `governor_`
47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L20-L20) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L30-L30), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L47-L47)


```solidity

File: /src/blast/libraries/BlastYields.sol

//@audit variable : `governor_`
29:     function configureDefaultClaimables(address governor_) internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L29-L29) 


```solidity

File: /src/mimswap/MagicLP.sol

//@audit variable : `_INITIALIZED_`
68:     bool internal _INITIALIZED_;

//@audit variable : `_BASE_TOKEN_`
70:     address public _BASE_TOKEN_;

//@audit variable : `_QUOTE_TOKEN_`
71:     address public _QUOTE_TOKEN_;

//@audit variable : `_BASE_RESERVE_`
72:     uint112 public _BASE_RESERVE_;

//@audit variable : `_QUOTE_RESERVE_`
73:     uint112 public _QUOTE_RESERVE_;

//@audit variable : `_BLOCK_TIMESTAMP_LAST_`
74:     uint32 public _BLOCK_TIMESTAMP_LAST_;

//@audit variable : `_BASE_PRICE_CUMULATIVE_LAST_`
75:     uint256 public _BASE_PRICE_CUMULATIVE_LAST_;

//@audit variable : `_BASE_TARGET_`
76:     uint112 public _BASE_TARGET_;

//@audit variable : `_QUOTE_TARGET_`
77:     uint112 public _QUOTE_TARGET_;

//@audit variable : `_RState_`
78:     uint32 public _RState_;

//@audit variable : `_MT_FEE_RATE_MODEL_`
79:     IFeeRateModel public _MT_FEE_RATE_MODEL_;

//@audit variable : `_LP_FEE_RATE_`
80:     uint256 public _LP_FEE_RATE_;

//@audit variable : `_K_`
81:     uint256 public _K_;

//@audit variable : `_I_`
82:     uint256 public _I_;

//@audit variable : `owner_`
84:     constructor(address owner_) Owned(owner_) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L68-L68) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L78-L78), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L82-L82), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L84-L84)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

//@audit variable : `maintainer_`
22:     constructor(address maintainer_, address owner_) Owned(owner_) {

//@audit variable : `owner_`
22:     constructor(address maintainer_, address owner_) Owned(owner_) {

//@audit variable : `maintainer_`
46:     function setMaintainer(address maintainer_) external onlyOwner {

//@audit variable : `implementation_`
57:     function setImplementation(address implementation_) public onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L22-L22) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L46-L46), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L57)


```solidity

File: /src/mimswap/periphery/Factory.sol

//@audit variable : `clone_`
13:         address clone_,

//@audit variable : `baseToken_`
14:         address indexed baseToken_,

//@audit variable : `quoteToken_`
15:         address indexed quoteToken_,

//@audit variable : `creator_`
16:         address indexed creator_,

//@audit variable : `lpFeeRate_`
17:         uint256 lpFeeRate_,

//@audit variable : `i_`
19:         uint256 i_,

//@audit variable : `k_`
20:         uint256 k_

//@audit variable : `implementation_`
38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

//@audit variable : `maintainerFeeRateModel_`
38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

//@audit variable : `owner_`
38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

//@audit variable : `baseToken_`
67:         address baseToken_,

//@audit variable : `quoteToken_`
68:         address quoteToken_,

//@audit variable : `lpFeeRate_`
69:         uint256 lpFeeRate_,

//@audit variable : `i_`
70:         uint256 i_,

//@audit variable : `k_`
71:         uint256 k_

//@audit variable : `baseToken_`
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

//@audit variable : `quoteToken_`
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

//@audit variable : `lpFeeRate_`
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

//@audit variable : `i_`
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

//@audit variable : `k_`
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

//@audit variable : `implementation_`
96:     function setLpImplementation(address implementation_) external onlyOwner {

//@audit variable : `maintainerFeeRateModel_`
105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

//@audit variable : `sender_`
156:         address sender_,

//@audit variable : `baseToken_`
157:         address baseToken_,

//@audit variable : `quoteToken_`
158:         address quoteToken_,

//@audit variable : `lpFeeRate_`
159:         uint256 lpFeeRate_,

//@audit variable : `i_`
160:         uint256 i_,

//@audit variable : `k_`
161:         uint256 k_


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L13-L13) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L14-L14), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L16-L16), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L17-L17), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L67-L67), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L69-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L105), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L156-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L157-L157), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L158-L158), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L159-L159), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L160-L160), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L161-L161)


```solidity

File: /src/mimswap/periphery/Router.sol

//@audit variable : `weth_`
38:     constructor(IWETH weth_, IFactory factory_) {

//@audit variable : `factory_`
38:     constructor(IWETH weth_, IFactory factory_) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L38-L38) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L38-L38)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

//@audit variable : `pair_`
21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {

//@audit variable : `baseOracle_`
21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {

//@audit variable : `quoteOracle_`
21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L21-L21) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L21-L21)


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit variable : `lock_`
150:     function stake(uint256 amount, bool lock_) public whenNotPaused {

//@audit variable : `lastTimeRewardApplicable_`
277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

//@audit variable : `totalSupply_`
277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

//@audit variable : `balance_`
292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

//@audit variable : `rewardPerToken_`
292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

//@audit variable : `lock_`
349:     function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {

//@audit variable : `lock_`
458:     function _stakeFor(address account, uint256 amount, bool lock_) internal {

//@audit variable : `token_`
528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

//@audit variable : `totalSupply_`
528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

//@audit variable : `rewardPerToken_`
528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

//@audit variable : `user_`
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

//@audit variable : `balance_`
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

//@audit variable : `token_`
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

//@audit variable : `rewardPerToken_`
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

//@audit variable : `lastTimeRewardApplicable_`
529:         uint256 lastTimeRewardApplicable_ = lastTimeRewardApplicable(token_);

//@audit variable : `totalSupply_`
545:         uint256 totalSupply_ = totalSupply();

//@audit variable : `totalSupply_`
559:         uint256 totalSupply_ = totalSupply();

//@audit variable : `totalSupply_`
573:         uint256 totalSupply_ = totalSupply();

//@audit variable : `rewardPerToken_`
577:             uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L150-L150) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L292-L292), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L292-L292), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L349-L349), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L458-L458), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L528-L528), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L528-L528), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L528-L528), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L529-L529), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L545-L545), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L559-L559), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L573-L573), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L577-L577)


</details>


### [NC&#x2011;92] [NatSpec] Natspec `@param` is missing from `error` 



*There are 224 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

14:     event LogTokenDepositEnabled(address indexed token, bool enabled);

15:     event LogFeeToChanged(address indexed feeTo);

24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {

36:     function _onBeforeDeposit(

56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

65:     /// ADMIN

72:     function setFeeTo(address feeTo_) external onlyOwner {

81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {

103:     function isOwner(address _account) internal view override returns (bool) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L14-L14) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L65-L65), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L103-L103)


```solidity

File: /src/blast/BlastGovernor.sol

8:     event LogFeeToChanged(address indexed feeTo);

15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {

25:     /// OPERATORS

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

37:     /// ADMIN

49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L8-L8) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L49-L49), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L53-L53)


```solidity

File: /src/blast/BlastMagicLP.sol

11:     event LogFeeToChanged(address indexed feeTo);

12:     event LogOperatorChanged(address indexed, bool);

13:     event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);

23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {

69:     /// ADMIN / CLONES ONLY

77:     /// ADMIN / IMPLEMENTATION ONLY

89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L11-L11) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L13-L13), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L69-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L77-L77), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L89-L89)


```solidity

File: /src/blast/BlastOnboarding.sol

43:     modifier onlyState(State _state) {

50:     modifier onlySupportedTokens(address token) {

67:     event LogBootstrapperChanged(address indexed bootstrapper);

68:     event LogTokenSupported(address indexed token, bool supported);

69:     event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);

70:     event LogLock(address indexed user, address indexed token, uint256 amount);

71:     event LogFeeToChanged(address indexed feeTo);

72:     event LogWithdraw(address indexed user, address indexed token, uint256 amount);

73:     event LogTokenCapChanged(address indexed token, uint256 cap);

74:     event LogStateChange(State state);

75:     event LogTokenRescue(address indexed token, address indexed to, uint256 amount);

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {

98:     /// PUBLIC

123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {

144:     /// ADMIN

156:     function callBlastPrecompile(bytes calldata data) external onlyOwner {

164:     function claimTokenYields(address[] memory tokens) external onlyOwner {

175:     function setTokenSupported(address token, bool supported) external onlyOwner {

185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {

205:     function rescue(address token, address to, uint256 amount) external onlyOwner {

24:     struct Balances {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L43-L43) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L67-L67), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L69-L69), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L72-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L74-L74), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L98-L98), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L123-L123), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L132-L132), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L144-L144), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L156-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L164-L164), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L205-L205), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L24-L24)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

37:     event LogReadyChanged(bool ready);

38:     event LogClaimed(address indexed user, uint256 shares, bool lock);

39:     event LogInitialized(Router indexed router);

40:     event LogLiquidityBootstrapped(address indexed pool, address indexed staking, uint256 amountOut);

41:     event LogStakingChanged(address indexed staking);

52:     /// PUBLIC

75:     /// VIEWS

93:     /// ADMIN

129:     function initialize(Router _router) external onlyOwner {

137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {

146:     function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {

152:     /// INTERNALS


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L37-L37) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L40-L40), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L41-L41), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L52-L52), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L93-L93), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L129-L129), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L137), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L146-L146), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L152-L152)


```solidity

File: /src/blast/BlastTokenRegistry.sol

7:     event LogNativeYieldTokenEnabled(address indexed token, bool enabled);

12:     constructor(address _owner) Owned(_owner) {}

14:     function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L7-L7) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L14-L14)


```solidity

File: /src/blast/BlastWrappers.sol

20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

29:     constructor(

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {

59:     function init(bytes calldata data) public payable override {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L20-L20) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L59-L59)


```solidity

File: /src/blast/libraries/BlastYields.sol

8:     event LogBlastGasClaimed(address indexed recipient, uint256 amount);

9:     event LogBlastETHClaimed(address indexed recipient, uint256 amount);

10:     event LogBlastTokenClaimed(address indexed recipient, address indexed token, uint256 amount);

11:     event LogBlastTokenClaimableEnabled(address indexed contractAddress, address indexed token);

12:     event LogBlastNativeClaimableEnabled(address indexed contractAddress);

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L8-L8) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L9-L9), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L10-L10), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L11-L11), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L12-L12), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L60-L60), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L75-L75), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L86-L86)


```solidity

File: /src/mimswap/MagicLP.sol

30:     event BuyShares(address to, uint256 increaseShares, uint256 totalShares);

31:     event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);

32:     event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);

33:     event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);

34:     event RChange(PMMPricing.RState newRState);

35:     event TokenRescue(address indexed token, address to, uint256 amount);

36:     event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);

84:     constructor(address owner_) Owned(owner_) {

91:     function init(

167:     function querySellBase(

180:     function querySellQuote(

224:     function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {

241:     /// TRADE FUNCTIONS

267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

356:     /// BUY & SELL SHARES

413:     function sellShares(

458:     /// ADMIN

470:     function setParameters(

560:     function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {

581:     function _transferBaseOut(address to, uint256 amount) internal {

587:     function _transferQuoteOut(address to, uint256 amount) internal {

593:     function _mint(address to, uint256 amount) internal override {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L30-L30) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L34-L34), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L84-L84), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L91-L91), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L167-L167), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L180-L180), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L224-L224), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L241-L241), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L267-L267), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L290-L290), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L356-L356), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L413-L413), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L458-L458), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L470), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L560-L560), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L581-L581), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L587-L587), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L593-L593)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

14:     event LogImplementationChanged(address indexed implementation);

15:     event LogMaintainerChanged(address indexed maintainer);

22:     constructor(address maintainer_, address owner_) Owned(owner_) {

31:     /// VIEWS

43:     /// ADMIN


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L14-L14) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L15-L15), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L43-L43)


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

9:     function getFeeRate(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L9) 


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L47-L47)


```solidity

File: /src/mimswap/libraries/Math.sol

19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

29:     function sqrt(uint256 x) internal pure returns (uint256 y) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L19-L19) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L131-L131)


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

27:     struct PMMState {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L39-L39) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L76-L76), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L104-L104), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L119-L119), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L134-L134), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L147-L147), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L162-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L203-L203), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L27-L27)


```solidity

File: /src/mimswap/periphery/Factory.sol

12:     event LogCreated(

23:     event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);

24:     event LogPoolRemoved(address pool);

25:     event LogSetImplementation(address indexed implementation);

26:     event LogSetMaintainer(address indexed newMaintainer);

27:     event LogSetMaintainerFeeRateModel(IFeeRateModel newMaintainerFeeRateModel);

38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {

50:     /// VIEWS

57:     function getUserPoolCount(address creator) external view returns (uint256) {

62:     /// PUBLIC

81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

93:     /// ADMIN

105:     function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

114:     /// @notice Register a pool to the list
115:     /// Note this doesn't check if the pool is valid or if it's already registered.

120:     function removePool(

145:     /// INTERNALS

155:     function _computeSalt(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L12-L12) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L62-L62), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L93-L93), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L105-L105), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L114-L115), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L120), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L145-L145), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L155-L155)


```solidity

File: /src/mimswap/periphery/Router.sol

22:     error ErrTooHighSlippage(uint256 amountOut);

38:     constructor(IWETH weth_, IFactory factory_) {

47:     modifier ensureDeadline(uint256 deadline) {

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

496:     /// INTERNALS

507:     /// Adapted from: https://github.com/DODOEX/contractV2/blob/main/contracts/SmartRoute/proxies/DODODspProxy.sol
508:     /// Copyright 2020 DODO ZOO. Licensed under Apache-2.0.

541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

586:     function _validatePath(address[] calldata path) internal pure {

598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L22-L22) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L47-L47), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L54-L54), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L73-L73), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L96-L96), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L112-L112), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L162-L162), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L178-L178), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L192-L192), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L229), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L251-L251), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L274-L274), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L314-L314), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L336-L336), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L365-L365), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L404), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L415-L415), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L432-L432), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L449-L449), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L461-L461), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L478-L478), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L496-L496), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L507-L508), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L541-L541), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L571-L571), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L578-L578), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L586-L586), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L598-L598)


```solidity

File: /src/staking/LockingMultiRewards.sol

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

154:     /// @notice Locks an existing unlocked balance.

186:     function withdrawWithRewards(uint256 amount) public virtual {

197:     /// VIEWS

203:     function rewardsForDuration(address rewardToken) external view returns (uint256) {

211:     function balances(address user) external view returns (Balances memory) {

215:     function userRewardLock(address user) external view returns (RewardLock memory) {

219:     function userLocks(address user) external view returns (LockedBalance[] memory) {

223:     function userLocksLength(address user) external view returns (uint256) {

227:     function locked(address user) external view returns (uint256) {

231:     function unlocked(address user) external view returns (uint256) {

239:     function balanceOf(address user) public view returns (uint256) {

269:     function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {

273:     function rewardPerToken(address rewardToken) public view returns (uint256) {

277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {

288:     function earned(address user, address rewardToken) public view returns (uint256) {

292:     function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {

298:     /// ADMIN

317:     function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

322:     /// @notice This function can recover any token except for the staking token beyond the balance necessary for rewards.
323:     /// WARNING: Use this function with caution to ensure it does not affect the reward mechanism.

346:     /// OPERATORS

395:     /// @notice Updates the balances of the given user and lock indexes

456:     /// INTERNALS

479:     function _createLock(address user, uint256 amount) internal {

516:     /// @dev Update the global accumulated rewards from the last update to this point,
517:     /// in relation with the `totalSupply`
518:     ///
519:     /// The idea is to allow everyone that are currently part of that supply to get their allocated
520:     /// reward share.
521:     ///
522:     /// Each user's reward share is taking in account when `rewards[user][token] = _earned(...)`
523:     /// is called. And only updated when a user is interacting with `stake`, `lock`, `withdraw`
524:     /// or `getRewards`.
525:     ///
526:     /// Otherwise, if it's yet-to-be-updated, it's going to get considered as part of the pending
527:     /// yet-to-receive rewards in the `earned` function.

536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

555:     /// @dev More gas efficient version of `_updateRewards` when we
556:     /// only need to update the rewards for a single user.

571:     /// @dev `_updateRewardsForUser` for multiple users.

595:     /// @notice Claim unlocked rewards or create a new reward lock that

50:     struct Reward {

58:     struct Balances {

63:     struct LockedBalance {

68:     struct RewardLockItem {

73:     struct RewardLock {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L17-L17) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L18-L18), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L19-L19), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L20-L20), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L21-L21), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L22-L22), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L154-L154), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L186-L186), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L197-L197), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L203-L203), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L211-L211), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L219-L219), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L223-L223), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L227-L227), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L231-L231), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L239-L239), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L269-L269), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L273-L273), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L288-L288), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L292-L292), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L298-L298), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L317-L317), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L322-L323), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L346-L346), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L395-L395), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L456-L456), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L479-L479), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L516-L527), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L555-L556), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L571-L571), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L595-L595), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L50-L50), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L58-L58), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L63-L63), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L68-L68), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L73-L73)


</details>


### [NC&#x2011;93] Not using the latest version of `prb-math` from dependencies 
`prb-math` is an important mathematical library The package.json configuration file says that the project is using an old version of `prb-math`.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: package.json

//@audit `prb-math` version is 
1: 


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//package.json#L1-L1) 


</details>


### [NC&#x2011;94] Enforcing Lowercase and Underscores Only in the `name` Field of package.json 
package.json name variable should only consist of lowercase letters and underscores


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: package.json

//@audit package.json name is abracadabra-money-contracts
1: {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main//package.json#L1-L1) 


</details>


### [NC&#x2011;95] Non constant/immutable state variables are missing a setter post deployment 
Non-constant or non-immutable state variables lacking a setter function can create inflexibility in contract operations. If there's no way to update these variables post-deployment, the contract might not adapt to changing conditions or requirements, which can be a significant drawback, especially in upgradable or long-lived contracts. To resolve this, implement setter functions guarded by appropriate access controls, like `onlyOwner` or similar modifiers, so that these variables can be updated as required while maintaining security. This enables smoother contract maintenance and feature upgrades.


*There are 15 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

30:     State public state;

31:     address public bootstrapper;

32:     address public feeTo;

33:     BlastTokenRegistry public registry;

36:     mapping(address token => bool) public supportedTokens;

37:     mapping(address token => Balances) public totals;

38:     mapping(address token => uint256 cap) public caps;

41:     mapping(address user => mapping(address token => Balances)) public balances;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L30-L30) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L36-L36), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L41-L41)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

24:     address public pool;

25:     Router public router;

26:     IFactory public factory;

27:     uint256 public totalPoolShares;

28:     bool public ready;

29:     LockingMultiRewards public staking;

30:     mapping(address user => bool claimed) public claimed;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L24-L24) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L26-L26), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L28-L28), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L29-L29), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L30-L30)


</details>


### [NC&#x2011;96] Consider making private state variables internal to increase flexibility 
In Solidity, `private` state variables are strictly confined to the contract they are defined in and can't be accessed or modified by its derived contracts. While this offers strong encapsulation, it can limit contract extensibility and modification in inheritance chains. On the other hand, `internal` variables can be accessed and potentially overridden by child contracts, granting more flexibility in contract development and upgrades. Therefore, it's recommended to use `private` only when you explicitly want to prevent child contract access. Otherwise, prefer `internal` to maintain a balance between encapsulation and the flexibility offered by inheritance patterns in Solidity.


*There are 9 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastWrappers.sol

45:     address private immutable _governor;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L45-L45) 


```solidity

File: /src/staking/LockingMultiRewards.sol

78:     uint256 private constant BIPS = 10_000;

79:     uint256 private constant MAX_NUM_REWARDS = 5;

80:     uint256 private constant MIN_LOCK_DURATION = 1 weeks;

81:     uint256 private constant MIN_REWARDS_DURATION = 1 days;

89:     mapping(address token => Reward info) private _rewardData;

90:     mapping(address user => Balances balances) private _balances;

91:     mapping(address user => LockedBalance[] locks) private _userLocks;

92:     mapping(address user => RewardLock rewardLock) private _userRewardLock;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L78-L78) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L80-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L89-L89), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L90-L90), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L91-L91), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L92-L92)


</details>


### [NC&#x2011;97] Using Low-Level Call for Transfers 
Utilizing low-level calls like `.call{value: value}` for Ether transfers in Ethereum can be risky, as it can inadvertently allow malicious contract executions through fallback functions. To mitigate these risks and ensure safer Ether transfers, it is recommended to adopt more secure and explicit methods provided by reputable libraries such as OpenZeppelin. Functions like `Address.sendValue()` from OpenZeppelin provide a clearer and safer alternative for sending Ether, as they encapsulate necessary checks and error handling, ensuring that Ether is transferred securely and any errors are appropriately dealt with. This not only enhances the security of your smart contract but also improves code readability and maintainability, aligning with modern Solidity development practices.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastGovernor.sol

54:         (success, result) = to.call{value: value}(data);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L54-L54) 


</details>


### [NC&#x2011;98] Off-by-one timestamp error 
In Solidity, using `>=` or `<=` to compare against `block.timestamp` (alias `now`) may introduce off-by-one errors due to the fact that `block.timestamp` is only updated once per block and its value remains constant throughout the block's execution. If an operation happens at the exact second when `block.timestamp` changes, it could result in unexpected behavior. To avoid this, it's safer to use strict inequality operators (`>` or `<`). For instance, if a condition should only be met after a certain time, use `block.timestamp > time` rather than `block.timestamp >= time`. This way, potential off-by-one errors due to the exact timing of block mining are mitigated, leading to safer, more predictable contract behavior.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/staking/LockingMultiRewards.sol

602:         bool expired = _rewardLock.unlockTime <= block.timestamp;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L602-L602) 


</details>


### [NC&#x2011;99] Lack of space near the operator 
Lack of space near operators in code can lead to reduced readability, making it more challenging to distinguish between different elements and understand the logic quickly. As a resolution, always include spaces around operators to ensure a clear visual separation, which promotes better maintainability and comprehension of the code.


*There are 27 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

//@audit operator : %
546:         uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);

//@audit operator : %
125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L546-L546) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L125-L125)


```solidity

File: /src/mimswap/libraries/Math.sol

//@audit operator : *
56:         uint256 fairAmount = i * (V1 - V2); // i*delta

//@audit operator : +
170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB

//@audit operator : *
171:         uint256 bAbs = (DecimalMath.ONE - k) * V1; // (1-k)Q1

//@audit operator : *
188:         uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)

//@audit operator : *
184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2

//@audit operator : *
184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2

//@audit operator : -
56:         uint256 fairAmount = i * (V1 - V2); // i*delta

//@audit operator : *
170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB

//@audit operator : *
170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB

//@audit operator : -
171:         uint256 bAbs = (DecimalMath.ONE - k) * V1; // (1-k)Q1

//@audit operator : +
185:         squareRoot = sqrt((bAbs * bAbs) + squareRoot); // sqrt(b*b+4(1-k)kQ0*Q0)

//@audit operator : -
188:         uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)

//@audit operator : -
184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2

//@audit operator : /
170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB

//@audit operator : *
185:         squareRoot = sqrt((bAbs * bAbs) + squareRoot); // sqrt(b*b+4(1-k)kQ0*Q0)

//@audit operator : *
170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L56-L56) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L170-L170), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L171-L171), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L188-L188), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L184-L184), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L184-L184), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L170-L170), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L170-L170), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L171-L171), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L188-L188), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L184-L184), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L170-L170), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L170-L170)


```solidity

File: /src/mimswap/periphery/Router.sol

//@audit operator : -
542:         uint256 iterations = path.length - 1; // Subtract by one as last swap is done separately


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L542-L542) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

//@audit operator : *
38:         uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));

//@audit operator : *
39:         uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));

//@audit operator : *
43:         baseReserve = baseReserve * (10 ** (WAD - baseDecimals));

//@audit operator : *
44:         quoteReserve = quoteReserve * (10 ** (WAD - quoteDecimals));

//@audit operator : -
38:         uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));

//@audit operator : -
39:         uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));

//@audit operator : -
43:         baseReserve = baseReserve * (10 ** (WAD - baseDecimals));

//@audit operator : -
44:         quoteReserve = quoteReserve * (10 ** (WAD - quoteDecimals));


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L38-L38) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L44-L44), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L44-L44)


</details>


### [NC&#x2011;100] Incorrect withdraw declaration 
In Solidity, it's essential for clarity and interoperability to correctly specify return types in function declarations. If the `withdraw` function is expected to return a `bool` to indicate success or failure, its omission could lead to ambiguity or unexpected behavior when interacting with or calling this function from other contracts or off-chain systems. Missing return values can mislead developers and potentially lead to contract integrations built on incorrect assumptions. To resolve this, the function declaration for `withdraw` should be modified to explicitly include the `bool` return type, ensuring clarity and correctness in contract interactions.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
133:         balances[msg.sender][token].unlocked -= amount;
134:         balances[msg.sender][token].total -= amount;
135:         totals[token].unlocked -= amount;
136:         totals[token].total -= amount;
137: 
138:         token.safeTransfer(msg.sender, amount);
139: 
140:         emit LogWithdraw(msg.sender, token, amount);
141:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L132-L141) 


```solidity

File: /src/staking/LockingMultiRewards.sol

170:     function withdraw(uint256 amount) public virtual {
171:         if (amount == 0) {
172:             revert ErrZeroAmount();
173:         }
174: 
175:         _updateRewardsForUser(msg.sender);
176: 
177:         _balances[msg.sender].unlocked -= amount;
178:         unlockedSupply -= amount;
179: 
180:         stakingToken.safeTransfer(msg.sender, amount);
181:         stakingTokenBalance -= amount;
182: 
183:         emit LogWithdrawn(msg.sender, amount);
184:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L170-L184) 


</details>


### [NC&#x2011;101] Avoid mutating function parameters 
Function parameters in Solidity are passed by value, meaning they are essentially local copies. Mutating them can lead to confusion and errors because the changes don't persist outside the function. By keeping function parameters immutable, you ensure clarity in code behavior, preventing unintended side-effects. If you need to modify a value based on a parameter, use a local variable inside the function, leaving the original parameter unaltered. By adhering to this practice, you maintain a clear distinction between input data and the internal processing logic, improving code readability and reducing the potential for bugs.


*There are 6 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/libraries/BlastYields.sol

//@audit the following parameters are mutated amount,
60:     function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {
61:         amount = BLAST_YIELD_PRECOMPILE.claimYield(contractAddress, recipient, amount);
62:         emit LogBlastETHClaimed(recipient, amount);
63:         return amount;
64:     }

//@audit the following parameters are mutated amount,
75:     function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {
76:         amount = IERC20Rebasing(token).claim(recipient, amount);
77:         emit LogBlastTokenClaimed(recipient, address(token), amount);
78:         return amount;
79:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L60-L64) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L75-L79)


```solidity

File: /src/mimswap/periphery/Router.sol

//@audit the following parameters are mutated baseInAmount,quoteInAmount,
112:     function previewAddLiquidity(
113:         address lp,
114:         uint256 baseInAmount,
115:         uint256 quoteInAmount
116:     ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
117:         (uint256 baseReserve, uint256 quoteReserve) = IMagicLP(lp).getReserves();
118: 
119:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;
120:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;
121: 
122:         baseInAmount = baseBalance - baseReserve;
123:         quoteInAmount = quoteBalance - quoteReserve;
124: 
125:         if (baseInAmount == 0) {
126:             return (0, 0, 0);
127:         }
128: 
129:         uint256 totalSupply = IERC20(lp).totalSupply();
130: 
131:         if (totalSupply == 0) {
132:             if (quoteBalance == 0) {
133:                 return (0, 0, 0);
134:             }
135: 
136:             uint256 i = IMagicLP(lp)._I_();
137: 
138:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;
139:             baseAdjustedInAmount = shares;
140:             quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);
141: 
142:             if (shares <= 2001) {
143:                 return (0, 0, 0);
144:             }
145: 
146:             shares -= 1001;
147:         } else if (baseReserve > 0 && quoteReserve > 0) {
148:             uint256 baseInputRatio = DecimalMath.divFloor(baseInAmount, baseReserve);
149:             uint256 quoteInputRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);
150:             if (baseInputRatio <= quoteInputRatio) {
151:                 baseAdjustedInAmount = baseInAmount;
152:                 quoteAdjustedInAmount = DecimalMath.mulCeil(quoteReserve, baseInputRatio);
153:                 shares = DecimalMath.mulFloor(totalSupply, baseInputRatio);
154:             } else {
155:                 quoteAdjustedInAmount = quoteInAmount;
156:                 baseAdjustedInAmount = DecimalMath.mulCeil(baseReserve, quoteInputRatio);
157:                 shares = DecimalMath.mulFloor(totalSupply, quoteInputRatio);
158:             }
159:         }
160:     }

//@audit the following parameters are mutated baseInAmount,quoteInAmount,
509:     function _adjustAddLiquidity(
510:         address lp,
511:         uint256 baseInAmount,
512:         uint256 quoteInAmount
513:     ) internal view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount) {
514:         (uint256 baseReserve, uint256 quoteReserve) = IMagicLP(lp).getReserves();
515:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;
516:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;
517: 
518:         baseInAmount = baseBalance - baseReserve;
519:         quoteInAmount = quoteBalance - quoteReserve;
520: 
521:         if (IERC20(lp).totalSupply() == 0) {
522:             uint256 i = IMagicLP(lp)._I_();
523:             uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
524:             baseAdjustedInAmount = shares;
525:             quoteAdjustedInAmount = DecimalMath.mulFloor(shares, i);
526:         } else {
527:             if (quoteReserve > 0 && baseReserve > 0) {
528:                 uint256 baseIncreaseRatio = DecimalMath.divFloor(baseInAmount, baseReserve);
529:                 uint256 quoteIncreaseRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);
530:                 if (baseIncreaseRatio <= quoteIncreaseRatio) {
531:                     baseAdjustedInAmount = baseInAmount;
532:                     quoteAdjustedInAmount = DecimalMath.mulFloor(quoteReserve, baseIncreaseRatio);
533:                 } else {
534:                     quoteAdjustedInAmount = quoteInAmount;
535:                     baseAdjustedInAmount = DecimalMath.mulFloor(baseReserve, quoteIncreaseRatio);
536:                 }
537:             }
538:         }
539:     }

//@audit the following parameters are mutated directions,
541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {
542:         uint256 iterations = path.length - 1; // Subtract by one as last swap is done separately
543: 
544:         for (uint256 i = 0; i < iterations; ) {
545:             if (directions & 1 == 0) {
546:                 // Sell base
547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));
548:             } else {
549:                 // Sell quote
550:                 IMagicLP(path[i]).sellQuote(address(path[i + 1]));
551:             }
552: 
553:             directions >>= 1;
554: 
555:             unchecked {
556:                 ++i;
557:             }
558:         }
559: 
560:         if ((directions & 1 == 0)) {
561:             amountOut = IMagicLP(path[iterations]).sellBase(to);
562:         } else {
563:             amountOut = IMagicLP(path[iterations]).sellQuote(to);
564:         }
565: 
566:         if (amountOut < minimumOut) {
567:             revert ErrTooHighSlippage(amountOut);
568:         }
569:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L112-L160) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L509-L539), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L541-L569)


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit the following parameters are mutated amount,
361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
362:         if (!_rewardData[rewardToken].exists) {
363:             revert ErrInvalidTokenAddress();
364:         }
365: 
366:         _updateRewards();
367:         rewardToken.safeTransferFrom(msg.sender, address(this), amount);
368: 
369:         Reward storage reward = _rewardData[rewardToken];
370: 
371:         uint256 _nextEpoch = nextEpoch();
372:         uint256 _remainingRewardTime = _nextEpoch - block.timestamp;
373: 
374:         if (_remainingRewardTime < minRemainingTime) {
375:             revert ErrInsufficientRemainingTime();
376:         }
377: 
378:         // Take the remainder of the current rewards and add it to the amount for the next period
379:         if (block.timestamp < reward.periodFinish) {
380:             amount += _remainingRewardTime * reward.rewardRate;
381:         }
382: 
383:         // avoid `rewardRate` being 0
384:         if (amount < _remainingRewardTime) {
385:             revert ErrNotEnoughReward();
386:         }
387: 
388:         reward.rewardRate = amount / _remainingRewardTime;
389:         reward.lastUpdateTime = uint248(block.timestamp);
390:         reward.periodFinish = _nextEpoch;
391: 
392:         emit LogRewardAdded(amount);
393:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L361-L393) 


</details>


### [NC&#x2011;102] A event should be emitted if a non immutable state variable is set in a constructor 



*There are 25 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

32:         registry = registry_;

33:         feeTo = feeTo_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L32-L32) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L33-L33)


```solidity

File: /src/blast/BlastGovernor.sol

20:         feeTo = feeTo_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L20-L20) 


```solidity

File: /src/blast/BlastMagicLP.sol

31:         registry = registry_;

32:         feeTo = feeTo_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L31-L31) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L32-L32)


```solidity

File: /src/blast/BlastOnboarding.sol

93:         registry = registry_;

94:         feeTo = feeTo_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L93-L93) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L94-L94)


```solidity

File: /src/blast/BlastWrappers.sol

55:         _governor = governor_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L55-L55) 


```solidity

File: /src/mimswap/MagicLP.sol

85:         implementation = this;

88:         _INITIALIZED_ = true;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L85-L85) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L88-L88)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

27:         maintainer = maintainer_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L27-L27) 


```solidity

File: /src/mimswap/periphery/Factory.sol

45:         implementation = implementation_;

46:         maintainerFeeRateModel = maintainerFeeRateModel_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L45-L45) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L46-L46)


```solidity

File: /src/mimswap/periphery/Router.sol

43:         weth = weth_;

44:         factory = factory_;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L43-L43) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L44-L44)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

22:         pair = pair_;

23:         baseOracle = baseOracle_;

24:         quoteOracle = quoteOracle_;

25:         baseDecimals = IERC20Metadata(pair_._BASE_TOKEN_()).decimals();

26:         quoteDecimals = IERC20Metadata(pair_._QUOTE_TOKEN_()).decimals();


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L22-L22) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L23-L23), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L24-L24), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L25-L25), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L26-L26)


```solidity

File: /src/staking/LockingMultiRewards.sol

135:         stakingToken = _stakingToken;

136:         lockingBoostMultiplerInBips = _lockingBoostMultiplerInBips;

137:         rewardsDuration = _rewardsDuration;

138:         lockDuration = _lockDuration;

144:         maxLocks = _lockDuration / _rewardsDuration;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L135-L135) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L136-L136), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L137-L137), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L138-L138), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L144-L144)


</details>


### [NC&#x2011;103] Returning a struct instead of returning many variables is better 
Returning a struct from a Solidity function instead of multiple variables offers several benefits, enhancing code clarity and efficiency. Structs allow for the grouping of related data into a single entity, making the function's return values more organized and easier to manage. This approach significantly improves readability, as it encapsulates the data logically, helping developers quickly understand the returned information's structure. Additionally, it simplifies function interfaces, reducing the potential for errors when handling multiple return values. By using structs, you can also easily extend or modify the returned data without altering the function signature, facilitating smoother updates and maintenance of your smart contract code.


*There are 2 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

204:     function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
205:         PMMPricing.PMMState memory state = getPMMState();
206:         i = state.i;
207:         K = state.K;
208:         B = state.B;
209:         Q = state.Q;
210:         B0 = state.B0;
211:         Q0 = state.Q0;
212:         R = uint256(state.R);
213:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L204-L213) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
49:         return (0, latestAnswer(), 0, 0, 0);
50:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L48-L50) 


</details>


### [NC&#x2011;104] [Solidity]: Order of Argument Evaluation Disrupted in Non-Expression-Split Code by Optimizer Sequences with FullInliner 
Function call arguments in Yul are evaluated right to left. This order matters when the argument expressions have side-effects, and changing it may change contract behavior. FullInliner is an optimizer step that can replace a function call with the body of that function. The transformation involves assigning argument expressions to temporary variables, which imposes an explicit evaluation order. FullInliner was written with the assumption that this order does not necessarily have to match usual argument evaluation order because the argument expressions have no side-effects. In most circumstances this assumption is true because the default optimization step sequence contains the ExpressionSplitter step. ExpressionSplitter ensures that the code is in *expression-split form*, which means that function calls cannot appear nested inside expressions, and all function call arguments have to be variables. The assumption is, however, not guaranteed to be true in general. Version 0.6.7 introduced a setting allowing users to specify an arbitrary optimization step sequence, making it possible for the FullInliner to actually encounter argument expressions with side-effects, which can result in behavior differences between optimized and unoptimized bytecode. Contracts compiled without optimization or with the default optimization sequence are not affected. To trigger the bug the user has to explicitly choose compiler settings that contain a sequence with FullInliner step not preceded by ExpressionSplitter. [Ref](https://blog.soliditylang.org/2023/07/19/full-inliner-non-expression-split-argument-evaluation-order-bug/)


*There are 20 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastDapp.sol#L2-L2) 


```solidity

File: /src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L3-L3) 


```solidity

File: /src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L2-L2) 


```solidity

File: /src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L3-L3) 


```solidity

File: /src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L2-L2) 


```solidity

File: /src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L2-L2) 


```solidity

File: /src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastTokenRegistry.sol#L2-L2) 


```solidity

File: /src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastWrappers.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastPoints.sol#L2-L2) 


```solidity

File: /src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L2-L2) 


```solidity

File: /src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L8-L8) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L2) 


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L7-L7) 


```solidity

File: /src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L8-L8) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L8-L8) 


```solidity

File: /src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L2-L2) 


```solidity

File: /src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L2-L2) 


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L2-L2) 


```solidity

File: /src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L2-L2) 


</details>


### [NC&#x2011;105] Not using the named return variables anywhere in the function is confusing 
Consider changing the variable to be an unnamed one, since the variable is never assigned, nor is it returned by name. If the optimizer is not turned on, leaving the code as it is will also waste gas for the stack variable.


*There are 19 instances of this issue:*



<details>
<summary>see instances</summary>


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L78-L78) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L86-L86), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L155-L155)


```solidity

File: /src/blast/libraries/BlastYields.sol

// @audit amount
51:     function claimAllNativeYields(address recipient) internal returns (uint256 amount) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L51-L51) 


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L215-L215) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L224-L224), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L228-L228), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L232-L232)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

// @audit adjustedLpFeeRate
// @audit mtFeeRate
34:     function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L34-L34) 


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

// @audit adjustedLpFeeRate
9:     function getFeeRate(


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L9) 


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L178-L178) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L229), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L314-L314), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L336-L336), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L404), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L415-L415), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L449-L449), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L461-L461)


</details>


### [NC&#x2011;106] Use named return values 
Using named returns makes the code more self-documenting, makes it easier to fill out NatSpec, and in some cases can save gas. The cases below are where there currently is at most one return statement, which is ideal for named returns.


*There are 62 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

52:     function claimGasYields() external onlyOperators returns (uint256) {

103:     function isOwner(address _account) internal view override returns (bool) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L52-L52) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L103-L103)


```solidity

File: /src/blast/BlastGovernor.sol

28:     function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {

32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L28-L28) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L32-L32)


```solidity

File: /src/blast/BlastMagicLP.sol

39:     function version() external pure override returns (string memory) {

47:     function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L39-L39) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L47-L47)


```solidity

File: /src/blast/BlastOnboarding.sol

160:     function claimGasYields() external onlyOwner returns (uint256) {

226:     function _implementation() internal view override returns (address) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L160-L160) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L226-L226)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L96-L96) 


```solidity

File: /src/blast/libraries/BlastYields.sol

38:     function claimMaxGasYields(address recipient) internal returns (uint256) {

60:     function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {

75:     function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L38-L38) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L60-L60), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L75-L75)


```solidity

File: /src/mimswap/MagicLP.sol

155:     function name() public view override returns (string memory) {

159:     function symbol() public pure override returns (string memory) {

163:     function decimals() public view override returns (uint8) {

236:     function version() external pure virtual returns (string memory) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L155-L155) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L159-L159), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L163-L163), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L236-L236)


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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L23-L23) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L27-L27), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L31-L31), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L35-L35), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L39-L39), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L43-L43), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L47-L47)


```solidity

File: /src/mimswap/libraries/Math.sol

19:     function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {

51:     function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {

79:     function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {

131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L19-L19) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L79-L79), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/Math.sol#L131-L131)


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

104:     function _ROneSellBaseToken(
105:         PMMState memory state,
106:         uint256 payBaseAmount
107:     )
108:         internal
109:         pure
110:         returns (
111:             uint256 // receiveQuoteToken

119:     function _ROneSellQuoteToken(
120:         PMMState memory state,
121:         uint256 payQuoteAmount
122:     )
123:         internal
124:         pure
125:         returns (
126:             uint256 // receiveBaseToken

134:     function _RBelowSellQuoteToken(
135:         PMMState memory state,
136:         uint256 payQuoteAmount
137:     )
138:         internal
139:         pure
140:         returns (
141:             uint256 // receiveBaseToken

147:     function _RBelowSellBaseToken(
148:         PMMState memory state,
149:         uint256 payBaseAmount
150:     )
151:         internal
152:         pure
153:         returns (
154:             uint256 // receiveQuoteToken

162:     function _RAboveSellBaseToken(
163:         PMMState memory state,
164:         uint256 payBaseAmount
165:     )
166:         internal
167:         pure
168:         returns (
169:             uint256 // receiveQuoteToken

175:     function _RAboveSellQuoteToken(
176:         PMMState memory state,
177:         uint256 payQuoteAmount
178:     )
179:         internal
180:         pure
181:         returns (
182:             uint256 // receiveBaseToken

203:     function getMidPrice(PMMState memory state) internal pure returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L104-L111) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L119-L126), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L134-L141), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L147-L154), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L162-L169), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L175-L182), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L203-L203)


```solidity

File: /src/mimswap/periphery/Factory.sol

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L53-L53) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L65-L72), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L155-L162)


```solidity

File: /src/oracles/aggregators/MagicLpAggregator.sol

29:     function decimals() external pure override returns (uint8) {

33:     function _getReserves() internal view virtual returns (uint256, uint256) {

37:     function latestAnswer() public view override returns (int256) {

48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L29-L29) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L33-L33), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L37-L37), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/oracles/aggregators/MagicLpAggregator.sol#L48-L48)


```solidity

File: /src/staking/LockingMultiRewards.sol

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

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L199-L199) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L203-L203), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L207-L207), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L211-L211), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L219-L219), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L223-L223), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L227-L227), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L231-L231), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L235-L235), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L239-L239), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L253-L253), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L257-L257), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L261-L261), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L265-L265), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L269-L269), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L273-L273), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L277-L277), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L288-L288), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L292-L292)


</details>


### [NC&#x2011;107] Consider moving duplicated strings to constants 



*There are 4 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

160:         return "MagicLP";

237:         return "MagicLP 1.0.0";

156:         return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));

156:         return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L160-L160) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L237-L237), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L156-L156), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L156-L156)


</details>


### [NC&#x2011;108] Missing checks for uint state variable assignments 
Consider whether reasonable bounds checks for variables would be useful


*There are 11 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/mimswap/MagicLP.sol

122:         _K_ = k;

123:         _LP_FEE_RATE_ = lpFeeRate;

141:             _BASE_TARGET_ = _BASE_RESERVE_;

142:             _QUOTE_TARGET_ = _QUOTE_RESERVE_;

146:             _BASE_TARGET_ = _BASE_RESERVE_;

147:             _QUOTE_TARGET_ = _QUOTE_RESERVE_;

557:         _BLOCK_TIMESTAMP_LAST_ = blockTimestamp;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L122-L122) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L123-L123), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L141-L141), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L142-L142), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L146-L146), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L147-L147), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L557-L557)


```solidity

File: /src/staking/LockingMultiRewards.sol

136:         lockingBoostMultiplerInBips = _lockingBoostMultiplerInBips;

137:         rewardsDuration = _rewardsDuration;

138:         lockDuration = _lockDuration;

319:         minLockAmount = _minLockAmount;


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L136-L136) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L137-L137), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L138-L138), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L319-L319)


</details>


### [NC&#x2011;109] Consider adding validation of user inputs 



*There are 87 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastBox.sol

//@audit these parameters `token`,``,``, are not checked
36:     function _onBeforeDeposit(
37:         IERC20 token,
38:         address /*from*/,
39:         address /*to*/,
40:         uint256 /*amount*/,
41:         uint256 /*share*/

//@audit these parameters `token_`, are not checked
56:     function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {

//@audit these parameters `token`, are not checked
81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L36-L41) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L56-L56), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastBox.sol#L81-L81)


```solidity

File: /src/blast/BlastGovernor.sol

//@audit these parameters `contractAddress`, are not checked
28:     function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {

//@audit these parameters `contractAddress`, are not checked
32:     function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {

//@audit these parameters `to`, are not checked
53:     function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L28-L28) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L32-L32), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastGovernor.sol#L53-L53)


```solidity

File: /src/blast/BlastMagicLP.sol

//@audit these parameters `operator`, are not checked
89:     function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastMagicLP.sol#L89-L89) 


```solidity

File: /src/blast/BlastOnboarding.sol

//@audit these parameters `token`, are not checked
123:     function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {

//@audit these parameters `token`, are not checked
132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {

//@audit these parameters `token`, are not checked
175:     function setTokenSupported(address token, bool supported) external onlyOwner {

//@audit these parameters `token`, are not checked
185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

//@audit these parameters `bootstrapper_`, are not checked
190:     function setBootstrapper(address bootstrapper_) external onlyOwner {

//@audit these parameters `token`,`to`, are not checked
205:     function rescue(address token, address to, uint256 amount) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L123-L123) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L132-L132), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L185-L185), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L190-L190), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L205-L205)


```solidity

File: /src/blast/BlastOnboardingBoot.sol

//@audit these parameters `_router`, are not checked
129:     function initialize(Router _router) external onlyOwner {

//@audit these parameters `_staking`, are not checked
137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L129-L129) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboardingBoot.sol#L137-L137)


```solidity

File: /src/blast/libraries/BlastYields.sol

//@audit these parameters `governor_`, are not checked
29:     function configureDefaultClaimables(address governor_) internal {

//@audit these parameters `recipient`, are not checked
38:     function claimMaxGasYields(address recipient) internal returns (uint256) {

//@audit these parameters `contractAddress`,`recipient`, are not checked
42:     function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {

//@audit these parameters `recipient`, are not checked
51:     function claimAllNativeYields(address recipient) internal returns (uint256 amount) {

//@audit these parameters `contractAddress`,`recipient`, are not checked
55:     function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {

//@audit these parameters `contractAddress`,`recipient`, are not checked
60:     function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {

//@audit these parameters `token`,`recipient`, are not checked
70:     function claimAllTokenYields(address token, address recipient) internal returns (uint256 amount) {

//@audit these parameters `token`,`recipient`, are not checked
75:     function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L29-L29) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L38-L38), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L42-L42), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L51-L51), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L55-L55), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L60-L60), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L70-L70), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L75-L75)


```solidity

File: /src/mimswap/MagicLP.sol

//@audit these parameters `trader`, are not checked
167:     function querySellBase(
168:         address trader,
169:         uint256 payBaseAmount

//@audit these parameters `trader`, are not checked
180:     function querySellQuote(
181:         address trader,
182:         uint256 payQuoteAmount

//@audit these parameters `user`, are not checked
224:     function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {

//@audit these parameters `to`, are not checked
244:     function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {

//@audit these parameters `to`, are not checked
267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

//@audit these parameters `assetTo`, are not checked
290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

//@audit these parameters `to`, are not checked
360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {

//@audit these parameters `to`, are not checked
461:     function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {

//@audit these parameters `assetTo`, are not checked
470:     function setParameters(
471:         address assetTo,
472:         uint256 newLpFeeRate,
473:         uint256 newI,
474:         uint256 newK,
475:         uint256 baseOutAmount,
476:         uint256 quoteOutAmount,
477:         uint256 minBaseReserve,
478:         uint256 minQuoteReserve

//@audit these parameters `to`, are not checked
581:     function _transferBaseOut(address to, uint256 amount) internal {

//@audit these parameters `to`, are not checked
587:     function _transferQuoteOut(address to, uint256 amount) internal {

//@audit these parameters `to`, are not checked
593:     function _mint(address to, uint256 amount) internal override {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L167-L169) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L180-L182), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L224-L224), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L244-L244), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L267-L267), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L290-L290), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L360-L360), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L461-L461), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L470-L478), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L581-L581), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L587-L587), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L593-L593)


```solidity

File: /src/mimswap/auxiliary/FeeRateModel.sol

//@audit these parameters `trader`, are not checked
34:     function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {

//@audit these parameters `implementation_`, are not checked
57:     function setImplementation(address implementation_) public onlyOwner {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L34-L34) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModel.sol#L57-L57)


```solidity

File: /src/mimswap/auxiliary/FeeRateModelImpl.sol

//@audit these parameters ``,``, are not checked
09:     function getFeeRate(
10:         address /*pool*/,
11:         address /*trader*/,
12:         uint256 lpFeeRate


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L12) 


```solidity

File: /src/mimswap/periphery/Factory.sol

//@audit these parameters `token0`,`token1`, are not checked
53:     function getPoolCount(address token0, address token1) external view returns (uint256) {

//@audit these parameters `creator`, are not checked
57:     function getUserPoolCount(address creator) external view returns (uint256) {

//@audit these parameters `creator`,`baseToken_`,`quoteToken_`, are not checked
65:     function predictDeterministicAddress(
66:         address creator,
67:         address baseToken_,
68:         address quoteToken_,
69:         uint256 lpFeeRate_,
70:         uint256 i_,
71:         uint256 k_

//@audit these parameters `baseToken_`,`quoteToken_`, are not checked
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {

//@audit these parameters `creator`,`baseToken`,`quoteToken`,`pool`, are not checked
116:     function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {

//@audit these parameters `creator`,`baseToken`,`quoteToken`, are not checked
120:     function removePool(
121:         address creator,
122:         address baseToken,
123:         address quoteToken,
124:         uint256 poolIndex,
125:         uint256 userPoolIndex

//@audit these parameters `creator`,`baseToken`,`quoteToken`,`pool`, are not checked
148:     function _addPool(address creator, address baseToken, address quoteToken, address pool) internal {

//@audit these parameters `sender_`,`baseToken_`,`quoteToken_`, are not checked
155:     function _computeSalt(
156:         address sender_,
157:         address baseToken_,
158:         address quoteToken_,
159:         uint256 lpFeeRate_,
160:         uint256 i_,
161:         uint256 k_


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L53-L53) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L57-L57), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L65-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L116-L116), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L120-L125), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L148-L148), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L155-L161)


```solidity

File: /src/mimswap/periphery/Router.sol

//@audit these parameters `baseToken`,`quoteToken`,`to`, are not checked
54:     function createPool(
55:         address baseToken,
56:         address quoteToken,
57:         uint256 lpFeeRate,
58:         uint256 i,
59:         uint256 k,
60:         address to,
61:         uint256 baseInAmount,
62:         uint256 quoteInAmount

//@audit these parameters `token`,`to`, are not checked
73:     function createPoolETH(
74:         address token,
75:         bool useTokenAsQuote,
76:         uint256 lpFeeRate,
77:         uint256 i,
78:         uint256 k,
79:         address to,
80:         uint256 tokenInAmount

//@audit these parameters `lp`,`to`, are not checked
162:     function addLiquidity(
163:         address lp,
164:         address to,
165:         uint256 baseInAmount,
166:         uint256 quoteInAmount,
167:         uint256 minimumShares,
168:         uint256 deadline

//@audit these parameters `lp`,`to`, are not checked
178:     function addLiquidityUnsafe(
179:         address lp,
180:         address to,
181:         uint256 baseInAmount,
182:         uint256 quoteInAmount,
183:         uint256 minimumShares,
184:         uint256 deadline

//@audit these parameters `to`,`refundTo`, are not checked
192:     function addLiquidityETH(
193:         address lp,
194:         address to,
195:         address payable refundTo,
196:         uint256 tokenInAmount,
197:         uint256 minimumShares,
198:         uint256 deadline

//@audit these parameters `to`, are not checked
229:     function addLiquidityETHUnsafe(
230:         address lp,
231:         address to,
232:         uint256 tokenInAmount,
233:         uint256 minimumShares,
234:         uint256 deadline

//@audit these parameters `lp`, are not checked
251:     function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

//@audit these parameters `lp`,`to`, are not checked
261:     function removeLiquidity(
262:         address lp,
263:         address to,
264:         uint256 sharesIn,
265:         uint256 minimumBaseAmount,
266:         uint256 minimumQuoteAmount,
267:         uint256 deadline

//@audit these parameters `to`, are not checked
274:     function removeLiquidityETH(
275:         address lp,
276:         address to,
277:         uint256 sharesIn,
278:         uint256 minimumETHAmount,
279:         uint256 minimumTokenAmount,
280:         uint256 deadline

//@audit these parameters `to`,`path`, are not checked
314:     function swapTokensForTokens(
315:         address to,
316:         uint256 amountIn,
317:         address[] calldata path,
318:         uint256 directions,
319:         uint256 minimumOut,
320:         uint256 deadline

//@audit these parameters `to`,`path`, are not checked
336:     function swapETHForTokens(
337:         address to,
338:         address[] calldata path,
339:         uint256 directions,
340:         uint256 minimumOut,
341:         uint256 deadline

//@audit these parameters `to`, are not checked
365:     function swapTokensForETH(
366:         address to,
367:         uint256 amountIn,
368:         address[] calldata path,
369:         uint256 directions,
370:         uint256 minimumOut,
371:         uint256 deadline

//@audit these parameters `lp`,`to`, are not checked
404:     function sellBaseTokensForTokens(
405:         address lp,
406:         address to,
407:         uint256 amountIn,
408:         uint256 minimumOut,
409:         uint256 deadline

//@audit these parameters `lp`,`to`, are not checked
415:     function sellBaseETHForTokens(
416:         address lp,
417:         address to,
418:         uint256 minimumOut,
419:         uint256 deadline

//@audit these parameters `to`, are not checked
432:     function sellBaseTokensForETH(
433:         address lp,
434:         address to,
435:         uint256 amountIn,
436:         uint256 minimumOut,
437:         uint256 deadline

//@audit these parameters `lp`,`to`, are not checked
449:     function sellQuoteTokensForTokens(
450:         address lp,
451:         address to,
452:         uint256 amountIn,
453:         uint256 minimumOut,
454:         uint256 deadline

//@audit these parameters `lp`,`to`, are not checked
461:     function sellQuoteETHForTokens(
462:         address lp,
463:         address to,
464:         uint256 minimumOut,
465:         uint256 deadline

//@audit these parameters `to`, are not checked
478:     function sellQuoteTokensForETH(
479:         address lp,
480:         address to,
481:         uint256 amountIn,
482:         uint256 minimumOut,
483:         uint256 deadline

//@audit these parameters `lp`,`to`, are not checked
499:     function _addLiquidity(address lp, address to, uint256 minimumShares) internal returns (uint256 shares) {

//@audit these parameters `to`, are not checked
541:     function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {

//@audit these parameters `lp`,`to`, are not checked
571:     function _sellBase(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

//@audit these parameters `lp`,`to`, are not checked
578:     function _sellQuote(address lp, address to, uint256 minimumOut) internal returns (uint256 amountOut) {

//@audit these parameters `path`, are not checked
586:     function _validatePath(address[] calldata path) internal pure {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L54-L62) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L73-L80), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L162-L168), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L178-L184), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L192-L198), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L229-L234), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L251-L251), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L261-L267), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L274-L280), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L314-L320), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L336-L341), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L365-L371), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L404-L409), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L415-L419), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L432-L437), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L449-L454), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L461-L465), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L478-L483), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L499-L499), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L541-L541), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L571-L571), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L578-L578), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L586-L586)


```solidity

File: /src/staking/LockingMultiRewards.sol

//@audit these parameters `token`, are not checked
199:     function rewardData(address token) external view returns (Reward memory) {

//@audit these parameters `user`, are not checked
211:     function balances(address user) external view returns (Balances memory) {

//@audit these parameters `user`, are not checked
215:     function userRewardLock(address user) external view returns (RewardLock memory) {

//@audit these parameters `user`, are not checked
219:     function userLocks(address user) external view returns (LockedBalance[] memory) {

//@audit these parameters `user`, are not checked
223:     function userLocksLength(address user) external view returns (uint256) {

//@audit these parameters `user`, are not checked
227:     function locked(address user) external view returns (uint256) {

//@audit these parameters `user`, are not checked
231:     function unlocked(address user) external view returns (uint256) {

//@audit these parameters `user`, are not checked
239:     function balanceOf(address user) public view returns (uint256) {

//@audit these parameters `rewardToken`, are not checked
269:     function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {

//@audit these parameters `rewardToken`, are not checked
273:     function rewardPerToken(address rewardToken) public view returns (uint256) {

//@audit these parameters `user`,`rewardToken`, are not checked
288:     function earned(address user, address rewardToken) public view returns (uint256) {

//@audit these parameters `account`, are not checked
349:     function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {

//@audit these parameters `rewardToken`, are not checked
361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {

//@audit these parameters `account`, are not checked
458:     function _stakeFor(address account, uint256 amount, bool lock_) internal {

//@audit these parameters `token_`, are not checked
528:     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {

//@audit these parameters `user_`,`token_`, are not checked
536:     function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {

//@audit these parameters `user`, are not checked
557:     function _updateRewardsForUser(address user) internal {

//@audit these parameters `user`, are not checked
597:     function _getRewards(address user) internal {


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L199-L199) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L211-L211), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L215-L215), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L219-L219), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L223-L223), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L227-L227), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L231-L231), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L239-L239), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L269-L269), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L273-L273), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L288-L288), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L349-L349), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L361-L361), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L458-L458), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L528-L528), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L536-L536), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L557-L557), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L597-L597)


</details>


### [NC&#x2011;110] Consider allowing users access to their funds at all times 
Users should always have access to their funds. Consider whether withdrawal functionality really must be disabled when the contract is paused.


*There are 1 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/BlastOnboarding.sol

132:     function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
133:         balances[msg.sender][token].unlocked -= amount;
134:         balances[msg.sender][token].total -= amount;
135:         totals[token].unlocked -= amount;
136:         totals[token].total -= amount;
137: 
138:         token.safeTransfer(msg.sender, amount);
139: 
140:         emit LogWithdraw(msg.sender, token, amount);
141:     }


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/BlastOnboarding.sol#L132-L141) 


</details>


### [NC&#x2011;111] Consider using named function calls 
Named function calls in Solidity greatly improve code readability by explicitly mapping arguments to their respective parameter names. This clarity becomes critical when dealing with functions that have numerous or complex parameters, reducing potential errors due to misordered arguments. Therefore, adopting named function calls contributes to more maintainable and less error-prone code.


*There are 69 instances of this issue:*



<details>
<summary>see instances</summary>


```solidity
File: /src/blast/libraries/BlastYields.sol

39:         return claimMaxGasYields(address(this), recipient);

52:         return claimAllNativeYields(address(this), recipient);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L39-L39) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/blast/libraries/BlastYields.sol#L52-L52)


```solidity

File: /src/mimswap/MagicLP.sol

252:         _transferQuoteOut(to, receiveQuoteAmount);

253:         _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);

262:         _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));

275:         _transferBaseOut(to, receiveBaseAmount);

276:         _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);

285:         _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);

291:         _transferBaseOut(assetTo, baseAmount);

292:         _transferQuoteOut(assetTo, quoteAmount);

406:         _mint(to, shares);

407:         _setReserve(baseBalance, quoteBalance);

445:         _burn(msg.sender, shareAmount);

446:         _transferBaseOut(to, baseAmount);

447:         _transferQuoteOut(to, quoteAmount);

497:         _transferBaseOut(assetTo, baseOutAmount);

498:         _transferQuoteOut(assetTo, quoteOutAmount);

250:         (receiveQuoteAmount, mtFee, newRState, newBaseTarget) = querySellBase(tx.origin, baseInput);

273:         (receiveBaseAmount, mtFee, newRState, newQuoteTarget) = querySellQuote(tx.origin, quoteInput);

310:             (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) = querySellQuote(
311:                 tx.origin,
312:                 quoteInput
313:             );

319:             _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);

332:             (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) = querySellBase(
333:                 tx.origin,
334:                 baseInput
335:             );

341:             _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);

393:             _mint(address(0), 1001);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L252-L252) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L253-L253), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L262-L262), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L275-L275), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L276-L276), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L285-L285), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L291-L291), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L292-L292), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L406-L406), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L407-L407), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L445-L445), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L446-L446), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L447-L447), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L497-L497), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L498-L498), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L250-L250), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L273-L273), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L310-L313), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L319-L319), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L332-L335), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L341-L341), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/MagicLP.sol#L393-L393)


```solidity

File: /src/mimswap/libraries/DecimalMath.sol

53:             uint p = powFloor(target, e / 2);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/DecimalMath.sol#L53-L53) 


```solidity

File: /src/mimswap/libraries/PMMPricing.sol

43:             receiveQuoteAmount = _ROneSellBaseToken(state, payBaseAmount);

78:             receiveBaseAmount = _ROneSellQuoteToken(state, payQuoteAmount);

71:             receiveQuoteAmount = _RBelowSellBaseToken(state, payBaseAmount);

81:             receiveBaseAmount = _RAboveSellQuoteToken(state, payQuoteAmount);

52:                 receiveQuoteAmount = _RAboveSellBaseToken(state, payBaseAmount);

87:                 receiveBaseAmount = _RBelowSellQuoteToken(state, payQuoteAmount);

65:                 receiveQuoteAmount = backToOneReceiveQuote + _ROneSellBaseToken(state, payBaseAmount - backToOnePayBase);

96:                 receiveBaseAmount = backToOneReceiveBase + _ROneSellQuoteToken(state, payQuoteAmount - backToOnePayQuote);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L43-L43) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L78-L78), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L71-L71), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L81-L81), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L52-L52), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L87-L87), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L65-L65), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/libraries/PMMPricing.sol#L96-L96)


```solidity

File: /src/mimswap/periphery/Factory.sol

84:         bytes32 salt = _computeSalt(creator, baseToken_, quoteToken_, lpFeeRate_, i_, k_);

89:         _addPool(creator, baseToken_, quoteToken_, clone);

117:         _addPool(creator, baseToken, quoteToken, pool);

76:                 _computeSalt(creator, baseToken_, quoteToken_, lpFeeRate_, i_, k_),


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L84-L84) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L89-L89), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L117-L117), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Factory.sol#L76-L76)


```solidity

File: /src/mimswap/periphery/Router.sol

64:         _validateDecimals(IERC20Metadata(baseToken).decimals(), IERC20Metadata(quoteToken).decimals());

189:         return _addLiquidity(lp, to, minimumShares);

248:         return _addLiquidity(lp, to, minimumShares);

333:         return _swap(to, path, directions, minimumOut);

362:         return _swap(to, path, directions, minimumOut);

412:         return _sellBase(lp, to, minimumOut);

429:         return _sellBase(lp, to, minimumOut);

458:         return _sellQuote(lp, to, minimumOut);

475:         return _sellQuote(lp, to, minimumOut);

170:         (baseAdjustedInAmount, quoteAdjustedInAmount) = _adjustAddLiquidity(lp, baseInAmount, quoteInAmount);

175:         shares = _addLiquidity(lp, to, minimumShares);

226:         shares = _addLiquidity(lp, to, minimumShares);

398:         amountOut = _swap(address(this), path, directions, minimumOut);

444:         amountOut = _sellBase(lp, address(this), minimumOut);

490:         amountOut = _sellQuote(lp, address(this), minimumOut);

85:             _validateDecimals(IERC20Metadata(token).decimals(), 18);

83:             _validateDecimals(18, IERC20Metadata(token).decimals());

205:             (baseAdjustedInAmount, quoteAdjustedInAmount) = _adjustAddLiquidity(lp, msg.value, tokenInAmount);

209:             (baseAdjustedInAmount, quoteAdjustedInAmount) = _adjustAddLiquidity(lp, tokenInAmount, msg.value);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L64-L64) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L189-L189), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L248-L248), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L333-L333), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L362-L362), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L412-L412), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L429-L429), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L458-L458), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L475-L475), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L170-L170), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L175-L175), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L226-L226), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L398-L398), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L444-L444), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L490-L490), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L85-L85), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L83-L83), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L205-L205), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/mimswap/periphery/Router.sol#L209-L209)


```solidity

File: /src/staking/LockingMultiRewards.sol

151:         _stakeFor(msg.sender, amount, lock_);

165:         _createLock(msg.sender, amount);

274:         return _rewardPerToken(rewardToken, lastTimeRewardApplicable(rewardToken), totalSupply());

289:         return _earned(user, balanceOf(user), rewardToken, rewardPerToken(rewardToken));

350:         _stakeFor(account, amount, lock_);

530:         rewardPerToken_ = _rewardPerToken(token_, lastTimeRewardApplicable_, totalSupply_);

537:         rewards[user_][token_] = _earned(user_, balance_, token_, rewardPerToken_);

470:             _createLock(account, amount);

548:             _updateRewardsGlobal(rewardTokens[i], totalSupply_);

563:             _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_));

577:             uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);

563:             _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_));

582:                 _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);


```

[link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L151-L151) , [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L165-L165), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L274-L274), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L289-L289), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L350-L350), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L530-L530), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L537-L537), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L470-L470), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L548-L548), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L563-L563), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L577-L577), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L563-L563), [link](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main///src/staking/LockingMultiRewards.sol#L582-L582)


</details>
