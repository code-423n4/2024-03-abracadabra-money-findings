| Number                                                                                                                  | Issue                                                                                                   | Instances | Estimated Gas Saved |
| ----------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------ | :-------: | :-----------------: |
| [GAS&#x2011;1](#GAS1-++i-costs-less-gas-than-i++/i-+=-1-same-for---i-vs-i--/i--+-1)                                     | `++i` costs less gas than `i++`/`i += 1` (same for `--i` vs `i--`/`i -+ 1`)                             |     1     |          5          |
| [GAS&#x2011;2](#GAS2-++i/i++-should-be-unchecked-when-it-is-not-possible-for-them-to-overflow)                          | `++i`/`i++` should be `unchecked` when it is not possible for them to overflow                          |     1     |         60          |
| [GAS&#x2011;3](#GAS3->=/<=-costs-less-gas-than->/<)                                                                     | `>=`/`<=` costs less gas than `>`/`<`                                                                   |    82     |         246         |
| [GAS&#x2011;4](#GAS4-addressthis-should-be-cached-when-used-multiple-times)                                             | `address(this)` should be cached when used multiple times                                               |     3     |          -          |
| [GAS&#x2011;5](#GAS5-avoid-fetching-a-low-level-calls-return-data-by-using-assembly)                                    | Avoid fetching a low-level call's return data by using assembly                                         |     1     |         159         |
| [GAS&#x2011;6](#GAS6-avoid-unnecessary-public-variables)                                                                | Avoid unnecessary `public` variables                                                                    |    49     |      1,078,000      |
| [GAS&#x2011;7](#GAS7-avoid-updating-storage-when-the-value-hasnt-changed)                                               | Avoid updating storage when the value hasn't changed                                                    |    11     |       18,700        |
| [GAS&#x2011;8](#GAS8-avoid-zero-to-non-zero-storage-writes-where-possible)                                              | Avoid zero to non-zero storage writes where possible                                                    |    13     |       287,300       |
| [GAS&#x2011;9](#GAS9-consider-activating-via-ir-for-deploying)                                                          | Consider activating `via-ir` for deploying                                                              |     0     |         250         |
| [GAS&#x2011;10](#GAS10-consider-caching-repeated-computations)                                                          | Consider caching repeated computations                                                                  |     2     |         120         |
| [GAS&#x2011;11](#GAS11-consider-pre-calculating-the-address-of-addressthis)                                             | Consider pre-calculating the address of `address(this)`                                                 |    49     |          -          |
| [GAS&#x2011;12](#GAS12-consider-using-openzeppelins-enumerateset-instead-of-nested-mappings)                            | Consider using OpenZeppelin's `EnumerateSet` instead of nested mappings                                 |     4     |        4,000        |
| [GAS&#x2011;13](#GAS13-consider-using-soladys-gas-optimized-lib-for-math)                                               | Consider using Solady's gas optimized lib for Math                                                      |    39     |          -          |
| [GAS&#x2011;14](#GAS14-constructors-can-be-marked-payable)                                                              | Constructors can be marked `payable`                                                                    |    16     |         336         |
| [GAS&#x2011;15](#GAS15-counting-down-in-for-statements-is-more-gas-efficient)                                           | Counting down in `for` statements is more gas efficient                                                 |     8     |         128         |
| [GAS&#x2011;16](#GAS16-declare-variables-outside-of-loops)                                                              | Declare variables outside of loops                                                                      |    15     |         225         |
| [GAS&#x2011;17](#GAS17-do-not-calculate-constants)                                                                      | Do not calculate constants                                                                              |     4     |          -          |
| [GAS&#x2011;18](#GAS18-do-while-is-cheaper-than-for-loops-when-the-initial-check-can-be-skipped)                        | `do`-`while` is cheaper than `for`-loops when the initial check can be skipped                          |     8     |        2,040        |
| [GAS&#x2011;19](#GAS19-dont-transfer-with-zero-amount-to-save-gas)                                                      | Don't transfer with zero amount to save gas                                                             |    26     |         520         |
| [GAS&#x2011;20](#GAS20-emitting-storage-values-instead-of-the-memory-one)                                               | Emitting storage values instead of the memory one.                                                      |     8     |         800         |
| [GAS&#x2011;21](#GAS21-empty-blocks-should-be-removed-or-emit-something)                                                | Empty blocks should be removed or emit something                                                        |     3     |          -          |
| [GAS&#x2011;22](#GAS22-function-names-can-be-optimized)                                                                 | Function names can be optimized                                                                         |    11     |        1,408        |
| [GAS&#x2011;23](#GAS23-functions-not-used-internally-could-be-marked-external-to-save-gas)                              | Functions not used internally could be marked external to save gas                                      |    15     |          -          |
| [GAS&#x2011;24](#GAS24-initializers-can-be-marked-payable)                                                              | Initializers can be marked `payable`                                                                    |     3     |         63          |
| [GAS&#x2011;25](#GAS25-internal-functions-only-used-once-can-be-inlined-so-save-gas)                                    | `internal` functions only used once can be inlined so save gas                                          |     3     |         90          |
| [GAS&#x2011;26](#GAS26-low-level-call-can-be-optimized-with-assembly)                                                   | Low-level `call` can be optimized with assembly                                                         |     1     |         159         |
| [GAS&#x2011;27](#GAS27-mappings-are-cheaper-to-use-than-storage-arrays)                                                 | Mappings are cheaper to use than storage arrays                                                         |     5     |       10,500        |
| [GAS&#x2011;28](#GAS28-merge-events-to-save-gas)                                                                        | Merge events to save gas                                                                                |     9     |        3,375        |
| [GAS&#x2011;29](#GAS29-multiple-accesses-of-the-same-mapping/array-key/index-should-be-cached)                          | Multiple accesses of the same mapping/array key/index should be cached                                  |    23     |         966         |
| [GAS&#x2011;30](#GAS30-multiple-address/id-mappings-can-be-combined-into-a-single-mapping-of-an-address/id-to-a-struct) | Multiple `address`/ID mappings can be combined into a single `mapping` of an `address`/ID to a `struct` |     9     |       180,000       |
| [GAS&#x2011;31](#GAS31-nested-for-loops-should-be-avoided-due-to-high-gas-costs-resulting-from-o^2-time-complexity)     | Nested for loops should be avoided due to high gas costs resulting from O^2 time complexity             |     1     |          -          |
| [GAS&#x2011;32](#GAS32-nesting-if-statements-is-cheaper-than-using-&&)                                                  | Nesting `if`-statements is cheaper than using `&&`                                                      |    11     |         330         |
| [GAS&#x2011;33](#GAS33-newer-versions-of-solidity-are-more-gas-efficient)                                               | Newer versions of solidity are more gas efficient                                                       |    20     |          -          |
| [GAS&#x2011;34](#GAS34-only-emit-event-in-setter-function-if-the-state-variable-was-changed)                            | Only emit event in setter function if the state variable was changed                                    |    13     |          -          |
| [GAS&#x2011;35](#GAS35-optimize-deployment-size-by-fine-tuning-ipfs-hash)                                               | Optimize Deployment Size by Fine-tuning IPFS Hash                                                       |    20     |       212,000       |
| [GAS&#x2011;36](#GAS36-order-of-initial-checks-in-a-function-can-be-optimized)                                          | Order of initial checks in a function can be optimized                                                  |     2     |        4,200        |
| [GAS&#x2011;37](#GAS37-pre-increments/pre-decrements-are-cheaper-than-+1/-1)                                            | Pre-increments/pre-decrements are cheaper than `+1`/`-1`                                                |     1     |          6          |
| [GAS&#x2011;38](#GAS38-remove-or-replace-unused-state-variables)                                                        | Remove or replace unused state variables                                                                |     7     |       80,150        |
| [GAS&#x2011;39](#GAS39-simple-checks-for-zero-can-be-done-using-assembly-to-save-gas)                                   | Simple checks for zero can be done using assembly to save gas                                           |    74     |         444         |
| [GAS&#x2011;40](#GAS40-simplify-modulo-operations)                                                                      | Simplify modulo operations                                                                              |     1     |         101         |
| [GAS&#x2011;41](#GAS41-sort-solidity-operations-using-short-circuit-mode)                                               | Sort Solidity operations using short-circuit mode                                                       |    36     |          -          |
| [GAS&#x2011;42](#GAS42-stack-variable-is-only-used-once)                                                                | Stack variable is only used once                                                                        |    28     |         84          |
| [GAS&#x2011;43](#GAS43-state-variable-read-in-a-loop)                                                                   | State variable read in a loop                                                                           |     7     |         679         |
| [GAS&#x2011;44](#GAS44-state-variable-written-in-a-loop)                                                                | State variable written in a loop                                                                        |     2     |       11,588        |
| [GAS&#x2011;45](#GAS45-state-variables-can-be-packed-into-fewer-storage-slots-by-truncating-timestamp-bytes)            | State variables can be packed into fewer storage slots by truncating timestamp bytes                    |     1     |       140,000       |
| [GAS&#x2011;46](#GAS46-state-variables-can-be-reordered-to-fit-into-fewer-storage-slots)                                | State variables can be reordered to fit into fewer storage slots                                        |     1     |       20,000        |
| [GAS&#x2011;47](#GAS47-state-variables-should-be-cached-in-stack-variables-rather-than-re-reading-them-from-storage)    | State variables should be cached in stack variables rather than re-reading them from storage            |    53     |        5,300        |
| [GAS&#x2011;48](#GAS48-structs-can-be-packed-into-fewer-storage-slots-by-truncating-timestamp-bytes)                    | Structs can be packed into fewer storage slots by truncating timestamp bytes                            |     1     |       20,000        |
| [GAS&#x2011;49](#GAS49-superfluous-event-fields)                                                                        | Superfluous event fields                                                                                |     2     |         70          |
| [GAS&#x2011;50](#GAS50-unchecked-{}-can-be-used-on-the-division-of-two-uints-in-order-to-save-gas)                      | `unchecked {}` can be used on the division of two `uint`s in order to save gas                          |    36     |        2,160        |
| [GAS&#x2011;51](#GAS51-update-openzeppelin-dependency-to-the-latest-version)                                            | Update OpenZeppelin dependency to the latest version                                                    |     8     |          -          |
| [GAS&#x2011;52](#GAS52-usage-of-uints/ints-smaller-than-32-bytes-256-bits-incurs-overhead)                              | Usage of `uints`/`ints` smaller than 32 bytes (256 bits) incurs overhead                                |    12     |         72          |
| [GAS&#x2011;53](#GAS53-use-arrayunsafeaccess-to-avoid-repeated-array-length-checks)                                     | Use `Array.unsafeAccess()` to avoid repeated array length checks                                        |    10     |       21,000        |
| [GAS&#x2011;54](#GAS54-use-assembly-for-math-equations)                                                                 | Use assembly for math equations                                                                         |     6     |        1,560        |
| [GAS&#x2011;55](#GAS55-use-assembly-for-small-keccak256-hashes-in-order-to-save-gas)                                    | Use assembly for small `keccak256` hashes, in order to save gas                                         |     1     |         80          |
| [GAS&#x2011;56](#GAS56-use-assembly-scratch-space-to-build-calldata-for-external-calls)                                 | Use assembly scratch space to build calldata for external calls                                         |    40     |        8,800        |
| [GAS&#x2011;57](#GAS57-use-assembly-to-perform-efficient-back-to-back-calls)                                            | Use assembly to perform efficient back-to-back calls                                                    |     2     |         600         |
| [GAS&#x2011;58](#GAS58-use-assembly-to-validate-msgsender)                                                              | Use assembly to validate `msg.sender`                                                                   |     2     |         24          |
| [GAS&#x2011;59](#GAS59-use-assembly-to-write-address/contract-storage-values)                                           | Use `assembly` to write address/contract storage values                                                 |    38     |        1,900        |
| [GAS&#x2011;60](#GAS60-use-calldata-instead-of-memory-for-function-arguments-that-do-not-get-mutated)                   | Use `calldata` instead of `memory` for function arguments that do not get mutated                       |     2     |         600         |
| [GAS&#x2011;61](#GAS61-use-constants-instead-of-typeuint<n>max-/-min)                                                   | Use constants instead of `type(uint<n>).max` / `.min`                                                   |     6     |         24          |
| [GAS&#x2011;62](#GAS62-use-if-statements-instead-of-ternary-operators)                                                  | Use `if` statements instead of ternary operators                                                        |     6     |          -          |
| [GAS&#x2011;63](#GAS63-use-immutable-when-you-have-storage-variable-that-is-not-going-to-change)                        | Use immutable when you have storage variable that is not going to change                                |     2     |          -          |
| [GAS&#x2011;64](#GAS64-use-modifiers-rather-than-invoking-functions-to-perform-checks)                                  | Use modifiers rather than invoking functions to perform checks                                          |     7     |         280         |
| [GAS&#x2011;65](#GAS65-use-of-emit-inside-a-loop)                                                                       | Use of `emit` inside a loop                                                                             |     5     |        1,875        |
| [GAS&#x2011;66](#GAS66-use-scratch-space-when-building-emitted-events-with-two-data-arguments)                          | Use scratch space when building emitted events with two data arguments                                  |    36     |        1,368        |
| [GAS&#x2011;67](#GAS67-use-the-inputs/results-of-assignments-rather-than-re-reading-state-variables)                    | Use the inputs/results of assignments rather than re-reading state variables                            |    28     |        2,716        |
| [GAS&#x2011;68](#GAS68-use-unchecked-for-divisions-on-constant-or-immutable-values)                                     | Use `unchecked` for divisions on constant or immutable values                                           |     6     |         360         |
| [GAS&#x2011;69](#GAS69-using-bools-for-storage-incurs-overhead)                                                         | Using `bool`s for storage incurs overhead                                                               |     3     |       51,300        |
| [GAS&#x2011;70](#GAS70-using-constants-instead-of-enum-can-save-gas)                                                    | Using `constant`s instead of `enum` can save gas                                                        |     2     |          -          |
| [GAS&#x2011;71](#GAS71-using-globals-directly-is-cheaper-than-assigning-them-to-variables)                              | Using globals directly is cheaper than assigning them to variables                                      |     1     |          5          |
| [GAS&#x2011;72](#GAS72-using-storage-instead-of-memory-for-structs/arrays-saves-gas)                                    | Using `storage` instead of `memory` for structs/arrays saves gas                                        |     3     |        6,300        |
| [GAS&#x2011;73](#GAS73-x-+-y-is-more-efficient-than-using-+=-for-state-variables-likewise-for--=)                       | x + y is more efficient than using += for state variables (likewise for -=)                             |    35     |        8,680        |

**❗ Disclaimer:** Gas totals are estimates based on data from the Ethereum Yellowpaper. The estimates use the lower bounds of ranges and count two iterations of each `for`-loop. All values above are runtime, not deployment, values; deployment values are listed in the individual issue descriptions.

---

## THE FULL REPORT IS @ https://gist.github.com/notbozho/07d533d869f7cf2921a83e8d092a5b9a

---

### [GAS&#x2011;1] `++i` costs less gas than `i++`/`i += 1` (same for `--i` vs `i--`/`i -+ 1`)

Gas saved per Instance: ~5

<i>There is one instance of this issue:</i>

```solidity
📁 File: src/blast/BlastOnboarding.sol

165:         for (uint256 i = 0; i < tokens.length; i++) {
```

[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L165-L165)

---

### [GAS&#x2011;2] `++i`/`i++` should be `unchecked` when it is not possible for them to overflow

The `unchecked` keyword is new in solidity version 0.8.0, so this only applies to that version or higher, which these instances are. This saves **30-40 gas [per loop](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#the-increment-in-for-loop-post-condition-can-be-made-unchecked)**

Gas saved per Instance: ~60

<i>There is one instance of this issue:</i>

```solidity
📁 File: src/blast/BlastOnboarding.sol

165:         for (uint256 i = 0; i < tokens.length; i++) {
```

[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L165-L165)

---

### [GAS&#x2011;3] `>=`/`<=` costs less gas than `>`/`<`

The compiler uses opcodes `GT` and `ISZERO` for code that uses `>`, but only requires `LT` for `>=`. A similar behaviour applies for `>`, which uses opcodes `LT` and `ISZERO`, but only requires `GT` for `<=`.

Gas saved per Instance: ~3 _(Total: ~246)_

<details>
<summary><i>There are 82 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastOnboarding.sol

114:         if (caps[token] > 0 && totals[token].total > caps[token]) {

165:         for (uint256 i = 0; i < tokens.length; i++) {
```

[114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L114-L114), [165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L165-L165)

```solidity
📁 File: src/blast/BlastOnboardingBoot.sol

108:         if (totalPoolShares < minAmountOut) {
```

[108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L108-L108)

```solidity
📁 File: src/mimswap/MagicLP.sol

108:         if (i == 0 || i > MAX_I) {

111:         if (k > MAX_K) {

114:         if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {

139:         if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {

144:         if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

294:         if (data.length > 0) {

302:         if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {

308:         if (baseBalance < _BASE_RESERVE_) {

315:             if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {

330:         if (quoteBalance < _QUOTE_RESERVE_) {

337:             if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {

381:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;

395:         } else if (baseReserve > 0 && quoteReserve > 0) {

399:             uint256 mintRatio = quoteInputRatio < baseInputRatio ? quoteInputRatio : baseInputRatio;

421:         if (deadline < block.timestamp) {

424:         if (shareAmount > balanceOf(msg.sender)) {

441:         if (baseAmount < baseMinAmount || quoteAmount < quoteMinAmount) {

450:         if (data.length > 0) {

480:         if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {

483:         if (newI == 0 || newI > MAX_I) {

486:         if (newK > MAX_K) {

489:         if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {

508:         if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {

532:         if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {

549:         if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {

582:         if (amount > 0) {

588:         if (amount > 0) {
```

[108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L108-L108), [111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L111-L111), [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L114-L114), [139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L139-L139), [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L144-L144), [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L294-L294), [302](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L302-L302), [308](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L308-L308), [315](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L315-L315), [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L330-L330), [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L337-L337), [381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L381-L381), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L395-L395), [399](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L399-L399), [421](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L421-L421), [424](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L424-L424), [441](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L441-L441), [450](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L450-L450), [480](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L480-L480), [483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L483-L483), [486](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L486-L486), [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L489-L489), [508](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L508-L508), [532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L532-L532), [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L549-L549), [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L582-L582), [588](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L588-L588)

```solidity
📁 File: src/mimswap/libraries/Math.sol

22:         if (remainder > 0) {

32:         while (z < y) {

141:             return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);

200:         if (V2 > V1) {
```

[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L22-L22), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L32-L32), [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L141-L141), [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L200-L200)

```solidity
📁 File: src/mimswap/libraries/PMMPricing.sol

50:             if (payBaseAmount < backToOnePayBase) {

54:                 if (receiveQuoteAmount > backToOneReceiveQuote) {

86:             if (payQuoteAmount < backToOnePayQuote) {

89:                 if (receiveBaseAmount > backToOneReceiveBase) {
```

[50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol/#L50-L50), [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol/#L54-L54), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol/#L86-L86), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol/#L89-L89)

```solidity
📁 File: src/mimswap/periphery/Router.sol

48:         if (block.timestamp > deadline) {

101:         shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

138:             shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;

147:         } else if (baseReserve > 0 && quoteReserve > 0) {

220:         if (msg.value > wethAdjustedAmount) {

502:         if (shares < minimumShares) {

523:             uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;

527:             if (quoteReserve > 0 && baseReserve > 0) {

544:         for (uint256 i = 0; i < iterations; ) {

566:         if (amountOut < minimumOut) {

573:         if (amountOut < minimumOut) {

581:         if (amountOut < minimumOut) {

590:         if (pathLength > 256) {

602:         if (quoteDecimals - baseDecimals > MAX_BASE_QUOTE_DECIMALS_DIFFERENCE) {
```

[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L48-L48), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L101-L101), [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L138-L138), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L147-L147), [220](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L220-L220), [502](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L502-L502), [523](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L523-L523), [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L527-L527), [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L544-L544), [566](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L566-L566), [573](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L573-L573), [581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L581-L581), [590](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L590-L590), [602](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L602-L602)

```solidity
📁 File: src/oracles/aggregators/MagicLpAggregator.sol

40:         uint256 minAnswer = baseAnswerNomalized < quoteAnswerNormalized ? baseAnswerNomalized : quoteAnswerNormalized;
```

[40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol/#L40-L40)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

123:         if (_lockDuration < MIN_LOCK_DURATION) {

127:         if (_rewardsDuration < MIN_REWARDS_DURATION) {

326:         if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

374:         if (_remainingRewardTime < minRemainingTime) {

379:         if (block.timestamp < reward.periodFinish) {

384:         if (amount < _remainingRewardTime) {

405:         for (uint256 i; i < users.length; ) {

417:             if (index == lastLockIndex[user] && locks.length > 1) {

422:             if (locks[index].unlockTime > block.timestamp) {

490:         if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {

497:             if (amount < minLockAmount) {

547:         for (uint256 i; i < rewardTokens.length; ) {

561:         for (uint256 i; i < rewardTokens.length; ) {

575:         for (uint256 i; i < rewardTokens.length; ) {

580:             for (uint256 j; j < users.length; ) {

614:         for (uint256 i; i < rewardTokens.length; ) {

623:             if (i < rewardItemLength) {

636:                     if (amount > 0) {
```

[123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L123-L123), [127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L127-L127), [326](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L326-L326), [374](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L374-L374), [379](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L379-L379), [384](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L384-L384), [405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L405-L405), [417](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L417-L417), [422](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L422-L422), [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L490-L490), [497](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L497-L497), [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L547-L547), [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L561-L561), [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L575-L575), [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L580-L580), [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L614-L614), [623](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L623-L623), [636](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L636-L636)

</details>

---

### [GAS&#x2011;4] `address(this)` should be cached when used multiple times

<details>
<summary><i>There are 3 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastOnboardingBoot.sol

/// @audit 'address(this)' used 3 times
96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
```

[96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L96-L96)

```solidity
📁 File: src/mimswap/MagicLP.sol

/// @audit 'address(this)' used 3 times
413:     function sellShares(
414:         uint256 shareAmount,
415:         address to,
416:         uint256 baseMinAmount,
417:         uint256 quoteMinAmount,
418:         bytes calldata data,
419:         uint256 deadline
420:     ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {
```

[413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L413-L420)

```solidity
📁 File: src/mimswap/periphery/Router.sol

/// @audit 'address(this)' used 3 times
274:     function removeLiquidityETH(
275:         address lp,
276:         address to,
277:         uint256 sharesIn,
278:         uint256 minimumETHAmount,
279:         uint256 minimumTokenAmount,
280:         uint256 deadline
281:     ) external returns (uint256 ethAmountOut, uint256 tokenAmountOut) {
```

[274](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L274-L281)

</details>

---

### [GAS&#x2011;5] Avoid fetching a low-level call's return data by using assembly

Even if you don't assign the call's second return value, it still gets copied to memory. Use assembly instead to prevent this and save 159 [gas](https://gist.github.com/IllIllI000/0e18a40f3afb0b83f9a347b10ee89ad2):

Gas saved per Instance: ~159

<i>There is one instance of this issue:</i>

```solidity
📁 File: src/blast/BlastGovernor.sol

54:         (success, result) = to.call{value: value}(data);
```

[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol/#L54-L54)

---

### [GAS&#x2011;6] Avoid unnecessary `public` variables

Public state variables in Solidity automatically generate getter functions, increasing contract size and potentially leading to higher deployment and interaction costs. To optimize gas usage and contract efficiency, minimize the use of public variables unless external access is necessary. Instead, use internal or private visibility combined with explicit getter functions when required. This practice not only reduces contract size but also provides better control over data access and manipulation, enhancing security and readability. Prioritize lean, efficient contracts to ensure cost-effectiveness and better performance on the blockchain.

Gas saved per Instance: ~22,000 _(Total: ~1,078,000)_

<details>
<summary><i>There are 49 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastBox.sol

20:     BlastTokenRegistry public immutable registry;

22:     address public feeTo;
```

[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol/#L20-L20), [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol/#L22-L22)

```solidity
📁 File: src/blast/BlastGovernor.sol

11:     address public feeTo;
```

[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol/#L11-L11)

```solidity
📁 File: src/blast/BlastMagicLP.sol

17:     BlastTokenRegistry public immutable registry;
```

[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol/#L17-L17)

```solidity
📁 File: src/blast/BlastOnboarding.sol

30:     State public state;
31:     address public bootstrapper;
32:     address public feeTo;
33:     BlastTokenRegistry public registry;
```

[30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L30-L33)

```solidity
📁 File: src/blast/BlastOnboardingBoot.sol

24:     address public pool;
25:     Router public router;
26:     IFactory public factory;
27:     uint256 public totalPoolShares;
28:     bool public ready;
29:     LockingMultiRewards public staking;
```

[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L24-L29)

```solidity
📁 File: src/mimswap/MagicLP.sol

61:     MagicLP public immutable implementation;

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

[61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L61-L61), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L70-L82)

```solidity
📁 File: src/mimswap/auxiliary/FeeRateModel.sol

19:     address public maintainer;
20:     address public implementation;
```

[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol/#L19-L20)

```solidity
📁 File: src/mimswap/periphery/Factory.sol

32:     address public implementation;
33:     IFeeRateModel public maintainerFeeRateModel;
```

[32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L32-L33)

```solidity
📁 File: src/mimswap/periphery/Router.sol

33:     IWETH public immutable weth;
34:     IFactory public immutable factory;
```

[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L33-L34)

```solidity
📁 File: src/oracles/aggregators/MagicLpAggregator.sol

10:     IMagicLP public immutable pair;
11:     IAggregator public immutable baseOracle;
12:     IAggregator public immutable quoteOracle;
13:     uint8 public immutable baseDecimals;
14:     uint8 public immutable quoteDecimals;
```

[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol/#L10-L14)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

83:     uint256 public immutable maxLocks;
84:     uint256 public immutable lockingBoostMultiplerInBips;
85:     uint256 public immutable rewardsDuration;
86:     uint256 public immutable lockDuration;
87:     address public immutable stakingToken;

98:     address[] public rewardTokens;

100:     uint256 public lockedSupply; // all locked boosted deposits
101:     uint256 public unlockedSupply; // all unlocked unboosted deposits
102:     uint256 public minLockAmount; // minimum amount allowed to lock
103:     uint256 public stakingTokenBalance; // total staking token balance
```

[83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L83-L87), [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L98-L98), [100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L100-L103)

</details>

---

### [GAS&#x2011;7] Avoid updating storage when the value hasn't changed

If the old value is equal to the new value, not re-storing the value will avoid a Gsreset (2900 gas), potentially at the expense of a Gcoldsload (2100 gas) or a Gwarmaccess (100 gas)

Gas saved per Instance: ~1,700 _(Total: ~18,700)_

<details>
<summary><i>There are 11 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastBox.sol

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

147:     function setFeeTo(address feeTo_) external onlyOwner {
148:         if (feeTo_ == address(0)) {
149:             revert ErrZeroAddress();
150:         }
151:
152:         feeTo = feeTo_;
153:         emit LogFeeToChanged(feeTo_);
154:     }

190:     function setBootstrapper(address bootstrapper_) external onlyOwner {
191:         bootstrapper = bootstrapper_;
192:         emit LogBootstrapperChanged(bootstrapper_);
193:     }
```

[147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L147-L154), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L190-L193)

```solidity
📁 File: src/blast/BlastOnboardingBoot.sol

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

[137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L137-L144), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L146-L149)

```solidity
📁 File: src/mimswap/auxiliary/FeeRateModel.sol

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

[46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol/#L46-L53), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol/#L57-L60)

```solidity
📁 File: src/mimswap/periphery/Factory.sol

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

[96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L96-L103), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L105-L112)

</details>

---

### [GAS&#x2011;8] Avoid zero to non-zero storage writes where possible

Changing a storage variable from zero to non-zero costs **22,100 gas** in total. (20,000 gas for a zero to non-zero write and 2,100 for a cold storage access)

Consider using non-zero architecture to avoid high gas costs for zero to non-zero storage writes.

Gas saved per Instance: ~22,100 _(Total: ~287,300)_

<details>
<summary><i>There are 13 instances of this issue:</i></summary>

```solidity
📁 File: src/mimswap/MagicLP.sol

121:         _I_ = i;
122:         _K_ = k;
123:         _LP_FEE_RATE_ = lpFeeRate;
```

[121](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L121-L123)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

163:         unlockedSupply -= amount;

178:         unlockedSupply -= amount;

181:         stakingTokenBalance -= amount;

319:         minLockAmount = _minLockAmount;

380:             amount += _remainingRewardTime * reward.rewardRate;

441:             unlockedSupply += amount;
442:             lockedSupply -= amount;

465:         stakingTokenBalance += amount;

473:             unlockedSupply += amount;

486:         lockedSupply += amount;
```

[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L163-L163), [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L178-L178), [181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L181-L181), [319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L319-L319), [380](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L380-L380), [441](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L441-L442), [465](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L465-L465), [473](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L473-L473), [486](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L486-L486)

</details>

---

### [GAS&#x2011;9] Consider activating `via-ir` for deploying

The IR-based code generator was introduced with an aim to not only allow code generation to be more transparent and auditable but also to enable more powerful optimization passes that span across functions.You can enable it on the command line using `--via-ir` or with the option `{"viaIR": true}`.This will take longer to compile, but you can just simple test it before deploying and if you got a better benchmark then you can add --via-ir to your deploy commandMore on: https://docs.soliditylang.org/en/v0.8.17/ir-breaking-changes.html

---

### [GAS&#x2011;10] Consider caching repeated computations

The result of repeated computations can be cached to avoid calculating it multiple times and wasting gas.

Gas saved per Instance: ~60 _(Total: ~120)_

<details>
<summary><i>There are 2 instances of this issue:</i></summary>

```solidity
📁 File: src/mimswap/libraries/Math.sol

/// @audit DecimalMath.ONE-k is seen 3 times
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

[131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L131-L205)

```solidity
📁 File: src/mimswap/libraries/PMMPricing.sol

/// @audit (DecimalMath.ONE-state.K)+DecimalMath.mulFloor(state.K,R) is seen 2 times
203:     function getMidPrice(PMMState memory state) internal pure returns (uint256) {
204:         if (state.R == RState.BELOW_ONE) {
205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);
206:             R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);
207:             return DecimalMath.divFloor(state.i, R);
208:         } else {
209:             uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
210:             R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);
211:             return DecimalMath.mulFloor(state.i, R);
212:         }
213:     }
```

[203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol/#L203-L213)

</details>

---

### [GAS&#x2011;11] Consider pre-calculating the address of `address(this)`

It can be more gas-efficient to use a hardcoded address instead of the `address(this)` expression, especially if you need to use the same address multiple times in your contract.

The reason for this, is that using `address(this)` requires an additional `EXTCODESIZE` operation to retrieve the contract’s address from its bytecode, which can increase the gas cost of your contract. By pre-calculating and using a hardcoded address, you can avoid this additional operation and reduce the overall gas cost of your contract.

<details>
<summary><i>There are 49 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastBox.sol

99:         BlastYields.configureDefaultClaimables(address(this));
```

[99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol/#L99)

```solidity
📁 File: src/blast/BlastGovernor.sol

21:         BlastYields.configureDefaultClaimables(address(this));
```

[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol/#L21)

```solidity
📁 File: src/blast/BlastMagicLP.sol

99:         BlastYields.configureDefaultClaimables(address(this));
```

[99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol/#L99)

```solidity
📁 File: src/blast/BlastOnboarding.sol

59:         BlastYields.configureDefaultClaimables(address(this));

102:         token.safeTransferFrom(msg.sender, address(this), amount);
```

[59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L59), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L102)

```solidity
📁 File: src/blast/BlastOnboardingBoot.sol

106:         (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

117:         staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
118:         staking.setOperator(address(this), true);
```

[106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L106), [117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L117-L118)

```solidity
📁 File: src/blast/BlastWrappers.sol

51:         if (governor_ == address(this)) {

60:         if (_governor == address(this)) {
```

[51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol/#L51), [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol/#L60)

```solidity
📁 File: src/blast/libraries/BlastYields.sol

21:         if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {

26:         emit LogBlastTokenClaimableEnabled(address(this), token);

31:         emit LogBlastNativeClaimableEnabled(address(this));

39:         return claimMaxGasYields(address(this), recipient);

52:         return claimAllNativeYields(address(this), recipient);

71:         amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));
```

[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol/#L21), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol/#L26), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol/#L31), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol/#L39), [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol/#L52), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol/#L71)

```solidity
📁 File: src/mimswap/MagicLP.sol

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

[229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L229), [233](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L233), [245](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L245), [262](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L262), [268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L268), [285](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L285), [298](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L298-L299), [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L361-L362), [427](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L427), [431](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L431-L432), [505](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L505-L506), [529](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L529-L530), [568](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L568-L569), [615](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L615), [622](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L622)

```solidity
📁 File: src/mimswap/periphery/Factory.sol

77:                 address(this)
```

[77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L77)

```solidity
📁 File: src/mimswap/periphery/Router.sol

92:         address(weth).safeTransferFrom(address(this), clone, msg.value);

269:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

282:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

289:                 address(this),

298:                 address(this),

398:         amountOut = _swap(address(this), path, directions, minimumOut);

444:         amountOut = _sellBase(lp, address(this), minimumOut);

490:         amountOut = _sellQuote(lp, address(this), minimumOut);
```

[92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L92), [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L269), [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L282), [289](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L289), [298](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L298), [398](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L398), [444](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L444), [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L490)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

326:         if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

367:         rewardToken.safeTransferFrom(msg.sender, address(this), amount);

464:         stakingToken.safeTransferFrom(msg.sender, address(this), amount);
```

[326](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L326), [367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L367), [464](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L464)

</details>

---

### [GAS&#x2011;12] Consider using OpenZeppelin's `EnumerateSet` instead of nested mappings

Nested mappings and multi-dimensional arrays in Solidity operate through a process of double hashing, wherein the original storage slot and the first key are concatenated and hashed, and then this hash is again concatenated with the second key and hashed. This process can be quite gas expensive due to the double-hashing operation and subsequent storage operation (sstore).

A possible optimization involves manually concatenating the keys followed by a single hash operation and an sstore. However, this technique introduces the risk of storage collision, especially when there are other nested hash maps in the contract that use the same key types. Because Solidity is unaware of the number and structure of nested hash maps in a contract, it follows a conservative approach in computing the storage slot to avoid possible collisions.

OpenZeppelin's `EnumerableSet` provides a potential solution to this problem. It creates a data structure that combines the benefits of set operations with the ability to enumerate stored elements, which is not natively available in Solidity. EnumerableSet handles the element uniqueness internally and can therefore provide a more gas-efficient and collision-resistant alternative to nested mappings or multi-dimensional arrays in certain scenarios.

Gas saved per Instance: ~1,000 _(Total: ~4,000)_

<details>
<summary><i>There are 4 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastOnboarding.sol

41:     mapping(address user => mapping(address token => Balances)) public balances;
```

[41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L41-L41)

```solidity
📁 File: src/mimswap/periphery/Factory.sol

35:     mapping(address base => mapping(address quote => address[] pools)) public pools;
```

[35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L35-L35)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

94:     mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
95:     mapping(address user => mapping(address token => uint256 amount)) public rewards;
```

[94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L94-L95)

</details>

---

### [GAS&#x2011;13] Consider using Solady's gas optimized lib for Math

Utilizing gas-optimized math functions from libraries like [Solady](https://github.com/Vectorized/solady/blob/main/src/utils/FixedPointMathLib.sol) can lead to more efficient smart contracts.
This is particularly beneficial in contracts where these operations are frequently used.

<details>
<summary><i>There are 39 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastOnboardingBoot.sol

163:         return (userLocked * totalPoolShares) / totalLocked;
```

[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L163-L163)

```solidity
📁 File: src/mimswap/MagicLP.sol

125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

435:         baseAmount = (baseBalance * shareAmount) / totalShares;
436:         quoteAmount = (quoteBalance * shareAmount) / totalShares;

513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));

546:         uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
```

[125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L125-L125), [435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L435-L436), [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L513-L513), [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L517-L517), [546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L546-L546)

```solidity
📁 File: src/mimswap/libraries/DecimalMath.sol

24:         return (target * d) / ONE;

32:         return (target * ONE) / d;

54:             p = (p * p) / ONE;

56:                 p = (p * target) / ONE;
```

[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol/#L24-L24), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol/#L32-L32), [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol/#L54-L54), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol/#L56-L56)

```solidity
📁 File: src/mimswap/libraries/Math.sol

21:         uint256 remainder = a - quotient * b;

30:         uint256 z = x / 2 + 1;

34:             z = (x / z + z) / 2;

56:         uint256 fairAmount = i * (V1 - V2); // i*delta

62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

64:         return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;

93:         uint256 ki = (4 * k) * i;

96:         } else if ((ki * delta) / ki == delta) {
97:             _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);

99:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);

101:         uint256 premium = DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2) + DecimalMath.ONE;

155:             } else if ((idelta * V1) / idelta == V1) {
156:                 temp = (idelta * V1) / (V0 * V0);

158:                 temp = (((delta * V1) / V0) * i) / V0;

160:             return (V1 * temp) / (temp + DecimalMath.ONE);

170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
171:         uint256 bAbs = (DecimalMath.ONE - k) * V1; // (1-k)Q1

184:         uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
185:         squareRoot = sqrt((bAbs * bAbs) + squareRoot); // sqrt(b*b+4(1-k)kQ0*Q0)

188:         uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
```

[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L21-L21), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L30-L30), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L34-L34), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L56-L56), [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L62-L62), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L64-L64), [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L93-L93), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L96-L97), [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L99-L99), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L101-L101), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L155-L156), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L158-L158), [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L160-L160), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L170-L171), [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L184-L185), [188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol/#L188-L188)

```solidity
📁 File: src/mimswap/periphery/Router.sol

257:         baseAmountOut = (baseBalance * sharesIn) / totalShares;
258:         quoteAmountOut = (quoteBalance * sharesIn) / totalShares;

379:         if ((directions >> lastLpIndex) & 1 == 0) {
```

[257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L257-L258), [379](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L379-L379)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

236:         return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);

241:         return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);

258:         return (block.timestamp / rewardsDuration) * rewardsDuration;

283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

294:         return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];
```

[236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L236-L236), [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L241-L241), [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L258-L258), [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L283-L283), [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L294-L294)

</details>

---

### [GAS&#x2011;14] Constructors can be marked `payable`

Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn't provided. A constructor can safely be marked as payable, since only the deployer would be able to pass funds, and the project itself would not pass any funds.

Gas saved per Instance: ~21 _(Total: ~336)_

<details>
<summary><i>There are 16 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastBox.sol

24:     constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
```

[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol/#L24)

```solidity
📁 File: src/blast/BlastDapp.sol

7:     constructor() {
```

[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol/#L7)

```solidity
📁 File: src/blast/BlastGovernor.sol

15:     constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```

[15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol/#L15)

```solidity
📁 File: src/blast/BlastMagicLP.sol

23:     constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
```

[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol/#L23)

```solidity
📁 File: src/blast/BlastOnboarding.sol

58:     constructor() Owned(msg.sender) {

84:     constructor(BlastTokenRegistry registry_, address feeTo_) {
```

[58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L58), [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L84)

```solidity
📁 File: src/blast/BlastTokenRegistry.sol

12:     constructor(address _owner) Owned(_owner) {}
```

[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol/#L12)

```solidity
📁 File: src/blast/BlastWrappers.sol

20:     constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {

29:     constructor(

47:     constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
```

[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol/#L20), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol/#L29), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol/#L47)

```solidity
📁 File: src/mimswap/MagicLP.sol

84:     constructor(address owner_) Owned(owner_) {
```

[84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L84)

```solidity
📁 File: src/mimswap/auxiliary/FeeRateModel.sol

22:     constructor(address maintainer_, address owner_) Owned(owner_) {
```

[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol/#L22)

```solidity
📁 File: src/mimswap/periphery/Factory.sol

38:     constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
```

[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L38)

```solidity
📁 File: src/mimswap/periphery/Router.sol

38:     constructor(IWETH weth_, IFactory factory_) {
```

[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L38)

```solidity
📁 File: src/oracles/aggregators/MagicLpAggregator.sol

21:     constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```

[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol/#L21)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

112:     constructor(
```

[112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L112)

</details>

---

### [GAS&#x2011;15] Counting down in `for` statements is more gas efficient

Counting down is more gas efficient than counting up because neither we are making zero variable to non-zero variable and also we will get gas refund in the last transaction when making non-zero to zero variable. [More info](https://solodit.xyz/issues/g-02-counting-down-in-for-statements-is-more-gas-efficient-code4rena-pooltogether-pooltogether-git)

Gas saved per Instance: ~16 _(Total: ~128)_

<details>
<summary><i>There are 8 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastOnboarding.sol

165:         for (uint256 i = 0; i < tokens.length; i++) {
```

[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L165-L165)

```solidity
📁 File: src/mimswap/periphery/Router.sol

/// @audit line 556
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
```

[544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L544-L558)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

/// @audit line 450
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

/// @audit line 550
547:         for (uint256 i; i < rewardTokens.length; ) {
548:             _updateRewardsGlobal(rewardTokens[i], totalSupply_);
549:             unchecked {
550:                 ++i;
551:             }
552:         }

/// @audit line 566
561:         for (uint256 i; i < rewardTokens.length; ) {
562:             address token = rewardTokens[i];
563:             _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_));
564:
565:             unchecked {
566:                 ++i;
567:             }
568:         }

/// @audit line 590
575:         for (uint256 i; i < rewardTokens.length; ) {
576:             address token = rewardTokens[i];
577:             uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);
578:
579:             // Record each user's rewards
/// @audit line 585
580:             for (uint256 j; j < users.length; ) {
581:                 address user = users[j];
582:                 _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);
583:
584:                 unchecked {
585:                     ++j;
586:                 }
587:             }
588:
589:             unchecked {
590:                 ++i;
591:             }
592:         }

/// @audit line 654
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

[405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L405-L452), [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L547-L552), [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L561-L568), [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L575-L592), [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L614-L656)

</details>

---

### [GAS&#x2011;16] Declare variables outside of loops

Variables should be declared outside of loops, and get overriden with each iteration of loop, By doing so we save gas cost for memory variable declaration in each iteration.

Gas saved per Instance: ~15 _(Total: ~225)_

<i>There are 15 instaces of this issue:</i>

```solidity
📁 File: src/staking/LockingMultiRewards.sol

/// @audit loop from line 405 to line 452
406:             address user = users[i];
/// @audit loop from line 405 to line 452
407:             Balances storage bal = _balances[user];
/// @audit loop from line 405 to line 452
408:             LockedBalance[] storage locks = _userLocks[user];

/// @audit loop from line 405 to line 452
414:             uint256 index = lockIndexes[i];

/// @audit loop from line 405 to line 452
426:             uint256 amount = locks[index].amount;
/// @audit loop from line 405 to line 452
427:             uint256 lastIndex = locks.length - 1;

/// @audit loop from line 561 to line 568
562:             address token = rewardTokens[i];

/// @audit loop from line 575 to line 592
576:             address token = rewardTokens[i];
/// @audit loop from line 575 to line 592
577:             uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);

/// @audit loop from line 575 to line 592
/// @audit loop from line 580 to line 587
581:                 address user = users[j];

/// @audit loop from line 614 to line 656
615:             address rewardToken = rewardTokens[i];
/// @audit loop from line 614 to line 656
616:             uint256 rewardAmount = rewards[user][rewardToken];

/// @audit loop from line 614 to line 656
624:                 RewardLockItem storage item = _rewardLock.items[i];

/// @audit loop from line 614 to line 656
628:                     uint256 amount = item.amount;
```

[406](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L406-L408), [414](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L414-L414), [426](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L426-L427), [562](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L562-L562), [576](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L576-L577), [581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L581-L581), [615](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L615-L616), [624](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L624-L624), [628](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L628-L628)

---

### [GAS&#x2011;17] Do not calculate constants

Due to how constant variables are implemented (replacements at compile-time), an expression assigned to a constant variable is recomputed each time that the variable is used, which wastes some gas.

<details>
<summary><i>There are 4 instances of this issue:</i></summary>

```solidity
📁 File: src/mimswap/MagicLP.sol

63:     uint256 public constant MAX_I = 10 ** 36;
64:     uint256 public constant MAX_K = 10 ** 18;
```

[63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L63-L64)

```solidity
📁 File: src/mimswap/libraries/DecimalMath.sol

20:     uint256 internal constant ONE = 10 ** 18;
21:     uint256 internal constant ONE2 = 10 ** 36;
```

[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol/#L20-L21)

</details>

---

### [GAS&#x2011;18] `do`-`while` is cheaper than `for`-loops when the initial check can be skipped

Using `do-while` loops instead of `for` loops can be more gas-efficient.
Even if you add an `if` condition to account for the case where the loop doesn't execute at all, a `do-while` loop can still be cheaper in terms of gas.

Gas saved per Instance: ~255 _(Total: ~2,040)_

<details>
<summary><i>There are 8 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastOnboarding.sol

165:         for (uint256 i = 0; i < tokens.length; i++) {
```

[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L165-L165)

```solidity
📁 File: src/mimswap/periphery/Router.sol

544:         for (uint256 i = 0; i < iterations; ) {
```

[544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L544-L544)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

405:         for (uint256 i; i < users.length; ) {

547:         for (uint256 i; i < rewardTokens.length; ) {

561:         for (uint256 i; i < rewardTokens.length; ) {

575:         for (uint256 i; i < rewardTokens.length; ) {

580:             for (uint256 j; j < users.length; ) {

614:         for (uint256 i; i < rewardTokens.length; ) {
```

[405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L405-L405), [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L547-L547), [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L561-L561), [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L575-L575), [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L580-L580), [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L614-L614)

</details>

---

### [GAS&#x2011;19] Don't transfer with zero amount to save gas

In Solidity, unnecessary operations can waste gas. For example, a transfer function without a zero amount check uses gas even if called with a zero amount, since the contract state remains unchanged. Implementing a zero amount check avoids these unnecessary function calls, saving gas and improving efficiency.

Gas saved per Instance: ~20 _(Total: ~520)_

<details>
<summary><i>There are 26 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastOnboarding.sol

/// @audit check for zero amount on the 'amount' variable
102:         token.safeTransferFrom(msg.sender, address(this), amount);

/// @audit check for zero amount on the 'amount' variable
138:         token.safeTransfer(msg.sender, amount);

/// @audit check for zero amount on the 'amount' variable
210:         token.safeTransfer(to, amount);
```

[102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L102-L102), [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L138-L138), [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L210-L210)

```solidity
📁 File: src/mimswap/MagicLP.sol

/// @audit check for zero amount on the 'amount' variable
466:         token.safeTransfer(to, amount);
```

[466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L466-L466)

```solidity
📁 File: src/mimswap/periphery/Router.sol

/// @audit check for zero amount on the 'baseInAmount' variable
68:         baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);
/// @audit check for zero amount on the 'quoteInAmount' variable
69:         quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);

/// @audit check for zero amount on the 'tokenInAmount' variable
91:         token.safeTransferFrom(msg.sender, clone, tokenInAmount);

/// @audit check for zero amount on the 'baseAdjustedInAmount' variable
172:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);
/// @audit check for zero amount on the 'quoteAdjustedInAmount' variable
173:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);

/// @audit check for zero amount on the 'baseInAmount' variable
186:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);
/// @audit check for zero amount on the 'quoteInAmount' variable
187:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);

/// @audit check for zero amount on the 'wethAdjustedAmount' variable
217:         address(weth).safeTransfer(lp, wethAdjustedAmount);

/// @audit check for zero amount on the 'tokenAdjustedAmount' variable
224:         token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);

/// @audit check for zero amount on the 'tokenInAmount' variable
246:         token.safeTransferFrom(msg.sender, lp, tokenInAmount);

/// @audit check for zero amount on the 'sharesIn' variable
269:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

/// @audit check for zero amount on the 'sharesIn' variable
282:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

/// @audit check for zero amount on the 'tokenAmountOut' variable
311:         token.safeTransfer(to, tokenAmountOut);

/// @audit check for zero amount on the 'amountIn' variable
328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

/// @audit check for zero amount on the 'amountIn' variable
330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

/// @audit check for zero amount on the 'amountIn' variable
393:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

/// @audit check for zero amount on the 'amountIn' variable
395:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

/// @audit check for zero amount on the 'amountIn' variable
411:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

/// @audit check for zero amount on the 'amountIn' variable
443:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

/// @audit check for zero amount on the 'amountIn' variable
456:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

/// @audit check for zero amount on the 'amountIn' variable
489:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
```

[68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L68-L69), [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L91-L91), [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L172-L173), [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L186-L187), [217](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L217-L217), [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L224-L224), [246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L246-L246), [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L269-L269), [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L282-L282), [311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L311-L311), [328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L328-L328), [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L330-L330), [393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L393-L393), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L395-L395), [411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L411-L411), [443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L443-L443), [456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L456-L456), [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L489-L489)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

/// @audit check for zero amount on the 'amount' variable
367:         rewardToken.safeTransferFrom(msg.sender, address(this), amount);
```

[367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L367-L367)

</details>

---

### [GAS&#x2011;20] Emitting storage values instead of the memory one.

Emitted values should not be read from storage again. Instead, the existing values from memory should be used.

Gas saved per Instance: ~100 _(Total: ~800)_

<details>
<summary><i>There are 8 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastOnboardingBoot.sol

/// @audit pool, staking, totalPoolShares
124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

/// @audit ready
148:         emit LogReadyChanged(ready);
```

[124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L124-L124), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L148-L148)

```solidity
📁 File: src/mimswap/MagicLP.sol

/// @audit _BASE_TOKEN_, _QUOTE_TOKEN_
264:         emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

/// @audit _QUOTE_TOKEN_, _BASE_TOKEN_
287:         emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

/// @audit _QUOTE_TOKEN_, _BASE_TOKEN_
325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

/// @audit _BASE_TOKEN_, _QUOTE_TOKEN_
347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
```

[264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L264-L264), [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L287-L287), [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L325-L325), [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L347-L347)

```solidity
📁 File: src/mimswap/periphery/Factory.sol

/// @audit maintainerFeeRateModel
88:         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
```

[88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L88-L88)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

/// @audit minLockAmount
318:         emit LogSetMinLockAmount(minLockAmount, _minLockAmount);
```

[318](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L318-L318)

</details>

---

### [GAS&#x2011;21] Empty blocks should be removed or emit something

Some functions don't have a body: consider commenting why, or add some logic. Otherwise, refactor the code and remove these functions.

<details>
<summary><i>There are 3 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastGovernor.sol

13:     receive() external payable {}
```

[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol/#L13-L13)

```solidity
📁 File: src/mimswap/MagicLP.sol

601:     function _afterInitialized() internal virtual {}
```

[601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L601-L601)

```solidity
📁 File: src/mimswap/periphery/Router.sol

36:     receive() external payable {}
```

[36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L36-L36)

</details>

---

### [GAS&#x2011;22] Function names can be optimized

Function that are `public`/`external` and `public` state variable names can be optimized to save gas.

Method IDs that have two leading zero bytes can save **128 gas** each during deployment, and renaming functions to have lower method IDs will save **22 gas** per call, per sorted position shifted. [Reference](https://blog.emn178.cc/en/post/solidity-gas-optimization-function-name/)

Gas saved per Instance: ~128 _(Total: ~1,408)_

<details>
<summary><i>There are 11 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastBox.sol

/// @audit optimized order: _onBeforeDeposit(), setTokenEnabled(), setFeeTo(), callBlastPrecompile(), claimTokenYields(), claimGasYields(), _configure(), isOwner()
13: contract BlastBox is DegenBox, OperatableV3 {
```

[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol/#L13)

```solidity
📁 File: src/blast/BlastGovernor.sol

/// @audit optimized order: setFeeTo(), claimNativeYields(), callBlastPrecompile(), execute(), claimMaxGasYields()
7: contract BlastGovernor is OperatableV2 {
```

[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol/#L7)

```solidity
📁 File: src/blast/BlastMagicLP.sol

/// @audit optimized order: setFeeTo(), callBlastPrecompile(), updateTokenClaimables(), setOperator(), version(), claimTokenYields(), claimGasYields(), _afterInitialized(), _updateTokenClaimables()
10: contract BlastMagicLP is MagicLP {
```

[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol/#L10)

```solidity
📁 File: src/blast/BlastOnboarding.sol

/// @audit optimized order: claimTokenYields(), open(), setFeeTo(), withdraw(), callBlastPrecompile(), setTokenSupported(), pause(), setCap(), setBootstrapper(), close(), unpause(), deposit(), claimGasYields(), lock(), rescue(), _implementation()
64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```

[64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol/#L64)

```solidity
📁 File: src/blast/BlastOnboardingBoot.sol

/// @audit optimized order: previewTotalPoolShares(), setReady(), initialize(), setStaking(), claimable(), bootstrap(), claim(), _claimable()
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```

[34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L34)

```solidity
📁 File: src/mimswap/MagicLP.sol

/// @audit optimized order: sync(), getPMMStateForCall(), getMidPrice(), sellQuote(), flashLoan(), ratioSync(), sellBase(), sellShares(), init(), getPMMState(), symbol(), querySellBase(), correctRState(), getQuoteInput(), querySellQuote(), getBaseInput(), version(), buyShares(), getUserFeeRate(), decimals(), setParameters(), rescue(), getReserves(), name(), _resetTargetAndReserve(), _twapUpdate(), _setReserve(), _sync(), _transferBaseOut(), _transferQuoteOut(), _mint(), _afterInitialized()
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```

[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L25)

```solidity
📁 File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit optimized order: getFeeRate(), setImplementation(), setMaintainer()
13: contract FeeRateModel is Owned {
```

[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol/#L13)

```solidity
📁 File: src/mimswap/periphery/Factory.sol

/// @audit optimized order: getPoolCount(), create(), removePool(), getUserPoolCount(), setLpImplementation(), addPool(), predictDeterministicAddress(), setMaintainerFeeRateModel(), _addPool(), _computeSalt()
11: contract Factory is Owned {
```

[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L11)

```solidity
📁 File: src/mimswap/periphery/Router.sol

/// @audit optimized order: removeLiquidityETH(), swapTokensForTokens(), addLiquidityETH(), sellQuoteETHForTokens(), sellBaseTokensForTokens(), swapTokensForETH(), createPool(), addLiquidityUnsafe(), swapETHForTokens(), addLiquidityETHUnsafe(), createPoolETH(), previewRemoveLiquidity(), sellBaseTokensForETH(), previewAddLiquidity(), removeLiquidity(), previewCreatePool(), sellQuoteTokensForTokens(), sellBaseETHForTokens(), addLiquidity(), sellQuoteTokensForETH(), _addLiquidity(), _adjustAddLiquidity(), _swap(), _sellBase(), _sellQuote(), _validatePath(), _validateDecimals()
12: contract Router {
```

[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol/#L12)

```solidity
📁 File: src/oracles/aggregators/MagicLpAggregator.sol

/// @audit optimized order: decimals(), _getReserves(), latestRoundData(), latestAnswer()
9: contract MagicLpAggregator is IAggregator {
```

[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol/#L9)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

/// @audit optimized order: nextUnlockTime(), rewardPerToken(), lock(), remainingEpochTime(), stakeFor(), unlocked(), locked(), userLocksLength(), rewardTokensLength(), nextEpoch(), stake(), userRewardLock(), notifyRewardAmount(), withdrawWithRewards(), processExpiredLocks(), addReward(), epoch(), pause(), balanceOf(), lastTimeRewardApplicable(), recover(), _rewardPerToken(), rewardData(), unpause(), withdraw(), balances(), earned(), totalSupply(), setMinLockAmount(), rewardsForDuration(), getRewards(), userLocks(), _earned(), _stakeFor(), _createLock(), _updateRewardsGlobal(), _udpateUserRewards(), _updateRewards(), _updateRewardsForUser(), _updateRewardsForUsers(), _getRewards()
14: contract LockingMultiRewards is OperatableV2, Pausable {
```

[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L14)

</details>

---

### [GAS&#x2011;23] Functions not used internally could be marked external to save gas

Before Solidity version `0.6.9`, external functions are cheaper than public ones

<details>
<summary><i>There are 15 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastWrappers.sol

59:     function init(bytes calldata data) public payable override {
```

[59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol/#L59-L59)

```solidity
📁 File: src/mimswap/MagicLP.sol

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

[155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L155-L155), [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L159-L159), [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L163-L163), [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L228-L228), [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L232-L232), [470](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L470-L479)

```solidity
📁 File: src/mimswap/auxiliary/FeeRateModel.sol

57:     function setImplementation(address implementation_) public onlyOwner {
```

[57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol/#L57-L57)

```solidity
📁 File: src/mimswap/periphery/Factory.sol

65:     function predictDeterministicAddress(
66:         address creator,
67:         address baseToken_,
68:         address quoteToken_,
69:         uint256 lpFeeRate_,
70:         uint256 i_,
71:         uint256 k_
72:     ) public view returns (address) {
```

[65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L65-L72)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

150:     function stake(uint256 amount, bool lock_) public whenNotPaused {

155:     function lock(uint256 amount) public whenNotPaused {

265:     function remainingEpochTime() public view returns (uint256) {

288:     function earned(address user, address rewardToken) public view returns (uint256) {

300:     function addReward(address rewardToken) public onlyOwner {

361:     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
```

[150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L150-L150), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L155-L155), [265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L265-L265), [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L288-L288), [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L300-L300), [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L361-L361)

</details>

---

### [GAS&#x2011;24] Initializers can be marked `payable`

Gas saved per Instance: ~21 _(Total: ~63)_

<details>
<summary><i>There are 3 instances of this issue:</i></summary>

```solidity
📁 File: src/blast/BlastOnboardingBoot.sol

129:     function initialize(Router _router) external onlyOwner {
```

[129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol/#L129-L129)

```solidity
📁 File: src/mimswap/MagicLP.sol

91:     function init(
92:         address baseTokenAddress,
93:         address quoteTokenAddress,
94:         uint256 lpFeeRate,
95:         address mtFeeRateModel,
96:         uint256 i,
97:         uint256 k
98:     ) external {
```

[91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L91-L98)

</details>

---

### [GAS&#x2011;25] `internal` functions only used once can be inlined so save gas

If a internal function is only used once it doesn't make sense to modularise it unless the function which does call the function would be overly long and complex otherwise

Gas saved per Instance: ~30 _(Total: ~90)_

<details>
<summary><i>There are 3 instances of this issue:</i></summary>

```solidity
📁 File: src/mimswap/MagicLP.sol

528:     function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {
```

[528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L528-L528)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

544:     function _updateRewards() internal {

572:     function _updateRewardsForUsers(address[] memory users) internal {
```

[544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L544-L544), [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L572-L572)

</details>

---

### [GAS&#x2011;26] Low-level `call` can be optimized with assembly

`returnData` is copied to memory even if the variable is not utilized: the proper way to handle this is through a low level assembly call and save **159** [gas](https://gist.github.com/IllIllI000/0e18a40f3afb0b83f9a347b10ee89ad2).

```solidity
 // before (bool success,) = payable(receiver).call{gas: gas, value: value}("");
//after bool success; assembly { success := call(gas, receiver, value, 0, 0, 0, 0) }
```

Gas saved per Instance: ~159

<i>There is one instance of this issue:</i>

```solidity
📁 File: src/blast/BlastGovernor.sol

54:         (success, result) = to.call{value: value}(data);
```

[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol/#L54)

---

### [GAS&#x2011;27] Mappings are cheaper to use than storage arrays

When using storage arrays, solidity adds an internal lookup of the array's length (a Gcoldsload **2100 gas**) to ensure you don't read past the array's end. You can avoid this lookup by using a `mapping` and storing the number of entries in a separate storage variable. In cases where you have sentinel values (e.g. 'zero' means invalid), you can avoid length checks

Gas saved per Instance: ~2,100 _(Total: ~10,500)_

<details>
<summary><i>There are 5 instances of this issue:</i></summary>

```solidity
📁 File: src/mimswap/periphery/Factory.sol

35:     mapping(address base => mapping(address quote => address[] pools)) public pools;
36:     mapping(address creator => address[] pools) public userPools;
```

[35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol/#L35-L36)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

74:         RewardLockItem[] items;

91:     mapping(address user => LockedBalance[] locks) private _userLocks;

98:     address[] public rewardTokens;
```

[74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L74-L74), [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L91-L91), [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L98-L98)

</details>

---

### [GAS&#x2011;28] Merge events to save gas

Consolidating multiple event emissions into a single event in Solidity can result in significant gas savings. Each event emission in Ethereum involves a gas cost, specifically for the topics logged with the event. By merging sequential events into a singular event, you can save on the Glogtopic cost, which is incurred for each topic of each event. This approach can save around 375 gas per additional topic. This strategy is particularly beneficial in functions where multiple related events are emitted in sequence. However, it's crucial to balance gas optimization with the clarity and utility of the event data for off-chain consumers.

Gas saved per Instance: ~375 _(Total: ~3,375)_

<details>
<summary><i>There are 9 instances of this issue:</i></summary>

```solidity
📁 File: src/mimswap/MagicLP.sol

/// @audit 'Swap', 'RChange'
244:     function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {
245:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
246:         uint256 baseInput = baseBalance - uint256(_BASE_RESERVE_);
247:         uint256 mtFee;
248:         uint256 newBaseTarget;
249:         PMMPricing.RState newRState;
250:         (receiveQuoteAmount, mtFee, newRState, newBaseTarget) = querySellBase(tx.origin, baseInput);
251:
252:         _transferQuoteOut(to, receiveQuoteAmount);
253:         _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
254:
255:         // update TARGET
256:         if (_RState_ != uint32(newRState)) {
257:             _BASE_TARGET_ = newBaseTarget.toUint112();
258:             _RState_ = uint32(newRState);
259:             emit RChange(newRState);
260:         }
261:
262:         _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));
263:
264:         emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);
265:     }

/// @audit 'Swap', 'RChange'
267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {
268:         uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
269:         uint256 quoteInput = quoteBalance - uint256(_QUOTE_RESERVE_);
270:         uint256 mtFee;
271:         uint256 newQuoteTarget;
272:         PMMPricing.RState newRState;
273:         (receiveBaseAmount, mtFee, newRState, newQuoteTarget) = querySellQuote(tx.origin, quoteInput);
274:
275:         _transferBaseOut(to, receiveBaseAmount);
276:         _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
277:
278:         // update TARGET
279:         if (_RState_ != uint32(newRState)) {
280:             _QUOTE_TARGET_ = newQuoteTarget.toUint112();
281:             _RState_ = uint32(newRState);
282:             emit RChange(newRState);
283:         }
284:
285:         _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);
286:
287:         emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);
288:     }

/// @audit 'FlashLoan', 'Swap', 'Swap', 'RChange', 'RChange'
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
/// @audit 'Swap', 'RChange'
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
/// @audit 'Swap', 'RChange'
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
```

[244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L244-L265), [267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L267-L288), [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol/#L290-L353)

```solidity
📁 File: src/staking/LockingMultiRewards.sol

/// @audit 'LogUnlocked', 'LogLockIndexChanged'
397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
398:         if (users.length != lockIndexes.length) {
399:             revert ErrLengthMismatch();
400:         }
401:
402:         _updateRewardsForUsers(users);
403:
404:         // Release all expired users' locks
/// @audit 'LogUnlocked', 'LogLockIndexChanged'
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

/// @audit 'LogRewardLockCreated', 'LogRewardLocked', 'LogRewardPaid'
597:     function _getRewards(address user) internal {
598:         RewardLock storage _rewardLock = _userRewardLock[user];
599:
600:         // first ever lock is always expired because `unlockTime` is 0
601:         // unlock time is aligned to epoch
602:         bool expired = _rewardLock.unlockTime <= block.timestamp;
603:
604:         // cache the length here since the loop will be modifying the array
605:         uint256 rewardItemLength = _rewardLock.items.length;
606:
607:         // expired lock
608:         // existing lock items will be reused
609:         if (expired) {
610:             _rewardLock.unlockTime = nextEpoch();
611:             emit LogRewardLockCreated(user, _rewardLock.unlockTime);
612:         }
613:
/// @audit 'LogRewardLocked', 'LogRewardPaid'
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
657:     }
```

[397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L397-L453), [597](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol/#L597-L657)

</details>

