# Gas Report

## Summary

Total **897 instances** over **53 issues**with **1164552** gas saved:

|ID|Issue|Instances|Gas|
|:--:|:---|:--:|:--:|
| [[G-01]](#g-01-constructors-can-be-marked-as-payable-to-save-deployment-gas) | Constructors can be marked as payable to save deployment gas | 16 | 336 |
| [[G-02]](#g-02-state-variables-only-set-in-their-definitions-should-be-declared-constant) | State variables only set in their definitions should be declared `constant` | 10 | 20970 |
| [[G-03]](#g-03-counting-down-in-for-statements-is-more-gas-efficient) | Counting down in for statements is more gas efficient | 1 | - |
| [[G-04]](#g-04-dont-caching-global-special-variables) | Don't caching global special variables | 1 | 10 |
| [[G-05]](#g-05-stack-variable-is-only-used-once) | Stack variable is only used once | 15 | 45 |
| [[G-06]](#g-06-do-not-cache-state-variables-that-are-used-only-once) | Do not cache state variables that are used only once | 5 | 15 |
| [[G-07]](#g-07-do-not-calculate-constants) | Do not calculate constants | 4 | - |
| [[G-08]](#g-08-use-of-emit-inside-a-loop) | Use of `emit` inside a loop | 4 | 1500 |
| [[G-09]](#g-09-use-local-variables-for-emitting) | Use local variables for emitting | 14 | 1400 |
| [[G-10]](#g-10-internal-functions-only-called-once-can-be-inlined-to-save-gas) | `internal` functions only called once can be inlined to save gas | 1 | 30 |
| [[G-11]](#g-11-update-openzeppelin-dependency-to-save-gas) | Update OpenZeppelin dependency to save gas | 8 | - |
| [[G-12]](#g-12-update-solady-dependency-to-save-gas) | Update solady dependency to save gas | 10 | - |
| [[G-13]](#g-13-mappings-are-cheaper-to-use-than-storage-arrays) | Mappings are cheaper to use than storage arrays | 4 | 8400 |
| [[G-14]](#g-14-operator--costs-less-gas-than-operator-) | Operator `>=`/`<=` costs less gas than operator `>`/`<` | 31 | 93 |
| [[G-15]](#g-15-consider-pre-calculating-the-address-of-addressthis-to-save-gas) | Consider pre-calculating the address of `address(this)` to save gas | 49 | - |
| [[G-16]](#g-16-remove-empty-functions-to-save-gas) | Remove empty functions to save gas | 1 | - |
| [[G-17]](#g-17-usage-of-intsuints-smaller-than-32-bytes-incurs-overhead) | Usage of `int`s/`uint`s smaller than 32 bytes incurs overhead | 22 | 1210 |
| [[G-18]](#g-18-using-a-double-if-statement-instead-of-a-logical-and) | Using a double `if` statement instead of a logical AND(`&&`) | 11 | 330 |
| [[G-19]](#g-19-reduce-deployment-costs-by-tweaking-contracts-metadata) | Reduce deployment costs by tweaking contracts' metadata | 19 | - |
| [[G-20]](#g-20-divisions-can-be-unchecked-to-save-gas) | Divisions can be unchecked to save gas | 40 | 800 |
| [[G-21]](#g-21-remove-unused-local-variables) | Remove unused local variables | 2 | - |
| [[G-22]](#g-22-use-assembly-to-validate-msgsender) | Use assembly to validate `msg.sender` | 2 | 24 |
| [[G-23]](#g-23-using-assembly-to-check-for-zero-can-save-gas) | Using assembly to check for zero can save gas | 56 | 336 |
| [[G-24]](#g-24-consider-using-oz-enumerateset-in-place-of-nested-mappings) | Consider using OZ EnumerateSet in place of nested mappings | 4 | 4000 |
| [[G-25]](#g-25-consider-using-soladys-fixedpointmathlib) | Consider using solady's `FixedPointMathLib` | 33 | - |
| [[G-26]](#g-26-avoid-zero-transfer-to-save-gas) | Avoid zero transfer to save gas | 30 | 3000 |
| [[G-27]](#g-27-cache-addressthis-when-used-more-than-once) | Cache address(this) when used more than once | 25 | - |
| [[G-28]](#g-28-state-variable-read-in-a-loop) | State variable read in a loop | 2 | 194 |
| [[G-29]](#g-29-state-variable-written-in-a-loop) | State variable written in a loop | 1 | 5794 |
| [[G-30]](#g-30-unlimited-gas-consumption-risk-due-to-external-call-recipients) | Unlimited gas consumption risk due to external call recipients | 1 | - |
| [[G-31]](#g-31-optimize-names-to-save-gas) | Optimize names to save gas | 14 | 308 |
| [[G-32]](#g-32-reduce-gas-usage-by-moving-to-solidity-0819-or-later) | Reduce gas usage by moving to Solidity 0.8.19 or later | 20 | - |
| [[G-33]](#g-33-newer-versions-of-solidity-are-more-gas-efficient) | Newer versions of solidity are more gas efficient | 20 | - |
| [[G-34]](#g-34-avoid-updating-storage-when-the-value-hasnt-changed) | Avoid updating storage when the value hasn't changed | 54 | 43200 |
| [[G-35]](#g-35-same-cast-is-done-multiple-times) | Same cast is done multiple times | 14 | - |
| [[G-36]](#g-36-state-variables-that-are-used-multiple-times-in-a-function-should-be-cached-in-stack-variables) | State variables that are used multiple times in a function should be cached in stack variables | 34 | 10185 |
| [[G-37]](#g-37-use-solady-library-where-possible-to-save-gas) | Use solady library where possible to save gas | 8 | 8000 |
| [[G-38]](#g-38-use-the-inputsresults-of-assignments-rather-than-re-reading-state-variables) | Use the inputs/results of assignments rather than re-reading state variables | 27 | 2619 |
| [[G-39]](#g-39-contracts-can-use-fewer-storage-slots-by-truncating-state-variables) | Contracts can use fewer storage slots by truncating state variables | 1 | 20000 |
| [[G-40]](#g-40-structs-can-be-packed-into-fewer-storage-slots-by-truncating-fields) | Structs can be packed into fewer storage slots by truncating fields | 1 | 40000 |
| [[G-41]](#g-41-using-constants-instead-of-enum-can-save-gas) | Using `constant`s instead of `enum` can save gas | 2 | - |
| [[G-42]](#g-42-use-arrayunsafeaccess-to-avoid-repeated-array-length-checks) | Use `Array.unsafeAccess()` to avoid repeated array length checks | 7 | 14700 |
| [[G-43]](#g-43-assembly-use-scratch-space-for-building-calldata) | Assembly: Use scratch space for building calldata | 110 | 24200 |
| [[G-44]](#g-44-use-assembly-to-emit-events) | Use assembly to emit events | 48 | 1824 |
| [[G-45]](#g-45-use-calldata-instead-of-memory-for-immutable-arguments) | Use `calldata` instead of `memory` for immutable arguments | 2 | 600 |
| [[G-46]](#g-46-consider-using-soladys-gas-optimized-lib-for-math) | Consider Using Solady's Gas Optimized Lib for Math | 16 | - |
| [[G-47]](#g-47-do-while-is-cheaper-than-for-loops-when-the-initial-check-can-be-skipped) | `do`-`while` is cheaper than `for`-loops when the initial check can be skipped | 8 | - |
| [[G-48]](#g-48-consider-activating-via-ir-for-deploying) | Consider activating via-ir for deploying | 1 | - |
| [[G-49]](#g-49-avoid-unnecessary-public-variables) | Avoid Unnecessary Public Variables | 34 | 748000 |
| [[G-50]](#g-50-optimize-deployment-size-by-fine-tuning-ipfs-hash) | Optimize Deployment Size by Fine-tuning IPFS Hash | 19 | 201400 |
| [[G-51]](#g-51-the-result-of-a-function-call-should-be-cached-rather-than-re-calling-the-function) | The result of a function call should be cached rather than re-calling the function | 4 | 400 |
| [[G-52]](#g-52-multiple-accesses-of-a-memorycalldata-array-should-use-a-local-variable-cache) | Multiple accesses of a `memory`/`calldata` array should use a local variable cache | 16 | - |
| [[G-53]](#g-53-multiple-accesses-of-the-same-mapping-key-should-be-cached) | Multiple accesses of the same mapping key should be cached | 15 | 630 |

## Gas Optimizations

### [G-01] Constructors can be marked as payable to save deployment gas

Payable functions cost less gas to execute, because the compiler does not have to add extra checks to ensure that no payment is provided. A constructor can be safely marked as payable, because only the deployer would be able to pass funds, and the project itself would not pass any funds.

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

### [G-02] State variables only set in their definitions should be declared `constant`

This can avoid a Gsset (**20000 gas**) on deployment (in constructor), and replaces the first access in each transaction (Gcoldsload - **2100 gas**) and each access thereafter (Gwarmacces - **100 gas**) with a `PUSH32` (**3 gas**).

There are 10 instances:

- *BlastOnboarding.sol* ( [30-30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L30-L30), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L31-L31), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L32-L32), [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L33-L33) ):

```solidity
30:     State public state;

31:     address public bootstrapper;

32:     address public feeTo;

33:     BlastTokenRegistry public registry;
```

- *BlastOnboardingBoot.sol* ( [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L24-L24), [25-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L25-L25), [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L26-L26), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L27-L27), [28-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L28-L28), [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L29-L29) ):

```solidity
24:     address public pool;

25:     Router public router;

26:     IFactory public factory;

27:     uint256 public totalPoolShares;

28:     bool public ready;

29:     LockingMultiRewards public staking;
```

### [G-03] Counting down in for statements is more gas efficient

Looping downwards is more gas efficient because of how the EVM compares variables. When using a 'for' loop that counts down, comparing the end condition with zero is cheaper than comparing with another number. Therefore, it is recommended to restructure loops to count downwards whenever possible.

There is 1 instance:

- *BlastOnboarding.sol* ( [165-165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L165-L165) ):

```solidity
165:         for (uint256 i = 0; i < tokens.length; i++) {
```

### [G-04] Don't caching global special variables

It's better not to cache the global special variables, because it's cheaper to use them directly.

There is 1 instance:

- *Factory.sol* ( [82-82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L82-L82) ):

```solidity
82:         address creator = tx.origin;
```

### [G-05] Stack variable is only used once

If the variable is only accessed once, it's cheaper to use the assigned value directly that one time, and save the 3 gas the extra stack assignment would spend.

<details>
<summary>There are 15 instances (click to show):</summary>

- *BlastOnboardingBoot.sol* ( [87-87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L87-L87), [88-88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L88-L88), [101-101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L101-L101), [102-102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L102-L102) ):

```solidity
/// @audit baseAmount
87:         uint256 baseAmount = totals[MIM].locked;

/// @audit quoteAmount
88:         uint256 quoteAmount = totals[USDB].locked;

/// @audit baseAmount
101:         uint256 baseAmount = totals[MIM].locked;

/// @audit quoteAmount
102:         uint256 quoteAmount = totals[USDB].locked;
```

- *MagicLP.sol* ( [431-431](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L431-L431) ):

```solidity
/// @audit baseBalance
431:         uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
```

- *Math.sol* ( [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L21-L21), [62-62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L62-L62), [63-63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L63-L63), [188-188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L188-L188) ):

```solidity
/// @audit remainder
21:         uint256 remainder = a - quotient * b;

/// @audit V0V0V1V2
62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

/// @audit penalty
63:         uint256 penalty = DecimalMath.mulFloor(k, V0V0V1V2); // k(V0^2/V1/V2)

/// @audit denominator
188:         uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
```

- *LockingMultiRewards.sol* ( [480-480](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L480-L480), [545-545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L545-L545), [558-558](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L558-L558), [559-559](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L559-L559), [573-573](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L573-L573), [605-605](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L605-L605) ):

```solidity
/// @audit bal
480:         Balances storage bal = _balances[user];

/// @audit totalSupply_
545:         uint256 totalSupply_ = totalSupply();

/// @audit balance
558:         uint256 balance = balanceOf(user);

/// @audit totalSupply_
559:         uint256 totalSupply_ = totalSupply();

/// @audit totalSupply_
573:         uint256 totalSupply_ = totalSupply();

/// @audit rewardItemLength
605:         uint256 rewardItemLength = _rewardLock.items.length;
```

</details>

### [G-06] Do not cache state variables that are used only once

It's cheaper to access the state variable directly if it is accessed only once. This can save some gas cost of the extra stack allocation.

There are 5 instances:

- *BlastOnboardingBoot.sol* ( [87-87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L87-L87), [88-88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L88-L88), [101-101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L101-L101), [102-102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L102-L102) ):

```solidity
87:         uint256 baseAmount = totals[MIM].locked;

88:         uint256 quoteAmount = totals[USDB].locked;

101:         uint256 baseAmount = totals[MIM].locked;

102:         uint256 quoteAmount = totals[USDB].locked;
```

- *LockingMultiRewards.sol* ( [480-480](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L480-L480) ):

```solidity
480:         Balances storage bal = _balances[user];
```

### [G-07] Do not calculate constants

Due to how constant variables are implemented (replacements at compile-time), an expression assigned to a constant variable is recomputed each time that the variable is used, which wastes some gas.

There are 4 instances:

- *MagicLP.sol* ( [63-63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L63-L63), [64-64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L64-L64) ):

```solidity
63:     uint256 public constant MAX_I = 10 ** 36;

64:     uint256 public constant MAX_K = 10 ** 18;
```

- *DecimalMath.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L20-L20), [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L21-L21) ):

```solidity
20:     uint256 internal constant ONE = 10 ** 18;

21:     uint256 internal constant ONE2 = 10 ** 36;
```

### [G-08] Use of `emit` inside a loop

Emitting an event inside a loop performs a `LOG` op N times, where N is the loop length. Consider refactoring the code to emit the event only once at the end of loop. Gas savings should be multiplied by the average loop length.

There are 4 instances:

- *LockingMultiRewards.sol* ( [436-436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L436-L436), [447-447](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L447-L447), [638-638](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L638-L638), [651-651](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L651-L651) ):

```solidity
436:                 emit LogLockIndexChanged(user, lastIndex, index);

447:             emit LogUnlocked(user, amount, index);

638:                         emit LogRewardPaid(user, rewardToken, amount);

651:             emit LogRewardLocked(user, rewardToken, rewardAmount);
```

### [G-09] Use local variables for emitting

Use the function/modifier's local copy of the state variable, rather than incurring an extra Gwarmaccess (**100 gas**). In the unlikely event that the state variable hasn't already been used by the function/modifier, consider whether it is really necessary to include it in the event, given the fact that it incurs a Gcoldsload (**2100 gas**), or whether it can be passed in to or back out of the functions that _do_ use it.

<details>
<summary>There are 14 instances (click to show):</summary>

- *BlastOnboardingBoot.sol* ( [124-124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L124-L124), [148-148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L148-L148) ):

```solidity
/// @audit pool
/// @audit totalPoolShares
/// @audit staking
124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

/// @audit ready
148:         emit LogReadyChanged(ready);
```

- *MagicLP.sol* ( [264-264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L264-L264), [287-287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L287-L287), [325-325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L325-L325), [347-347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L347-L347) ):

```solidity
/// @audit _BASE_TOKEN_
/// @audit _QUOTE_TOKEN_
264:         emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

/// @audit _QUOTE_TOKEN_
/// @audit _BASE_TOKEN_
287:         emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

/// @audit _QUOTE_TOKEN_
/// @audit _BASE_TOKEN_
325:             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

/// @audit _BASE_TOKEN_
/// @audit _QUOTE_TOKEN_
347:             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
```

- *Factory.sol* ( [88-88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L88-L88) ):

```solidity
/// @audit maintainerFeeRateModel
88:         emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
```

- *LockingMultiRewards.sol* ( [318-318](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L318-L318) ):

```solidity
/// @audit minLockAmount
318:         emit LogSetMinLockAmount(minLockAmount, _minLockAmount);
```

</details>

### [G-10] `internal` functions only called once can be inlined to save gas

If an `internal` function is only used once, there is no need to modularize it, unless the function calling it would otherwise be too long and complex. Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.

There is 1 instance:

- *LockingMultiRewards.sol* ( [544-544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L544-L544) ):

```solidity
544:     function _updateRewards() internal {
```

### [G-11] Update OpenZeppelin dependency to save gas

Every release contains new gas optimizations. Use the latest version to take advantage of this.

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

### [G-12] Update solady dependency to save gas

Every release contains new gas optimizations. Use the latest version to take advantage of this.

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

### [G-13] Mappings are cheaper to use than storage arrays

When using storage arrays, solidity adds an internal lookup of the array's length (a Gcoldsload **2100 gas**) to ensure you don't read past the array's end. You can avoid this lookup by using a `mapping` and storing the number of entries in a separate storage variable. In cases where you have sentinel values (e.g. 'zero' means invalid), you can avoid length checks.

There are 4 instances:

- *Factory.sol* ( [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L35-L35), [36-36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L36-L36) ):

```solidity
35:     mapping(address base => mapping(address quote => address[] pools)) public pools;

36:     mapping(address creator => address[] pools) public userPools;
```

- *LockingMultiRewards.sol* ( [91-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L91-L91), [98-98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L98-L98) ):

```solidity
91:     mapping(address user => LockedBalance[] locks) private _userLocks;

98:     address[] public rewardTokens;
```

### [G-14] Operator `>=`/`<=` costs less gas than operator `>`/`<`

The compiler uses opcodes `GT` and `ISZERO` for code that uses `>`, but only requires `LT` for `>=`. A similar behavior applies for `>`, which uses opcodes `LT` and `ISZERO`, but only requires `GT` for `<=`. It can [save **3 gas**](https://gist.github.com/IllIllI000/3dc79d25acccfa16dee4e83ffdc6ffde) for each.
It should be converted to the `<=`/`>=` equivalent when comparing against integer literals. In cases where a for-loop is being used, one can count down rather than up, in order to use the optimal operator.

<details>
<summary>There are 31 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [114-114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L114-L114) ):

```solidity
114:         if (caps[token] > 0 && totals[token].total > caps[token]) {
```

- *MagicLP.sol* ( [108-108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L108-L108), [111-111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L111-L111), [114-114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L114-L114), [114-114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L114-L114), [294-294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L294-L294), [395-395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L395-L395), [395-395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L395-L395), [450-450](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L450-L450), [483-483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L483-L483), [486-486](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L486-L486), [489-489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L489-L489), [489-489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L489-L489), [508-508](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L508-L508), [508-508](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L508-L508), [532-532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L532-L532), [532-532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L532-L532), [549-549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L549-L549), [582-582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L582-L582), [588-588](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L588-L588) ):

```solidity
108:         if (i == 0 || i > MAX_I) {

111:         if (k > MAX_K) {

114:         if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {

114:         if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {

294:         if (data.length > 0) {

395:         } else if (baseReserve > 0 && quoteReserve > 0) {

395:         } else if (baseReserve > 0 && quoteReserve > 0) {

450:         if (data.length > 0) {

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

- *Math.sol* ( [22-22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L22-L22) ):

```solidity
22:         if (remainder > 0) {
```

- *Router.sol* ( [147-147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L147-L147), [147-147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L147-L147), [527-527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L527-L527), [527-527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L527-L527), [590-590](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L590-L590), [602-602](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L602-L602) ):

```solidity
147:         } else if (baseReserve > 0 && quoteReserve > 0) {

147:         } else if (baseReserve > 0 && quoteReserve > 0) {

527:             if (quoteReserve > 0 && baseReserve > 0) {

527:             if (quoteReserve > 0 && baseReserve > 0) {

590:         if (pathLength > 256) {

602:         if (quoteDecimals - baseDecimals > MAX_BASE_QUOTE_DECIMALS_DIFFERENCE) {
```

- *LockingMultiRewards.sol* ( [123-123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L123-L123), [127-127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L127-L127), [417-417](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L417-L417), [636-636](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L636-L636) ):

```solidity
123:         if (_lockDuration < MIN_LOCK_DURATION) {

127:         if (_rewardsDuration < MIN_REWARDS_DURATION) {

417:             if (index == lastLockIndex[user] && locks.length > 1) {

636:                     if (amount > 0) {
```

</details>

### [G-15] Consider pre-calculating the address of `address(this)` to save gas

Use `foundry`'s [`script.sol`](https://book.getfoundry.sh/reference/forge-std/compute-create-address) or `solady`'s [`LibRlp.sol`](https://github.com/Vectorized/solady/blob/main/src/utils/LibRLP.sol) to save the value in a constant, which will avoid having to spend gas to push the value on the stack every time it's used.

<details>
<summary>There are 49 instances (click to show):</summary>

- *BlastBox.sol* ( [99-99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L99-L99) ):

```solidity
99:         BlastYields.configureDefaultClaimables(address(this));
```

- *BlastGovernor.sol* ( [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L21-L21) ):

```solidity
21:         BlastYields.configureDefaultClaimables(address(this));
```

- *BlastMagicLP.sol* ( [99-99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L99-L99) ):

```solidity
99:         BlastYields.configureDefaultClaimables(address(this));
```

- *BlastOnboarding.sol* ( [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L59-L59), [102-102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L102-L102) ):

```solidity
59:         BlastYields.configureDefaultClaimables(address(this));

102:         token.safeTransferFrom(msg.sender, address(this), amount);
```

- *BlastOnboardingBoot.sol* ( [106-106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L106-L106), [117-117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L117-L117), [118-118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L118-L118) ):

```solidity
106:         (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

117:         staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));

118:         staking.setOperator(address(this), true);
```

- *BlastWrappers.sol* ( [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L51-L51), [60-60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L60-L60) ):

```solidity
51:         if (governor_ == address(this)) {

60:         if (_governor == address(this)) {
```

- *BlastYields.sol* ( [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L21-L21), [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L26-L26), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L31-L31), [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L39-L39), [52-52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L52-L52), [71-71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L71-L71) ):

```solidity
21:         if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {

26:         emit LogBlastTokenClaimableEnabled(address(this), token);

31:         emit LogBlastNativeClaimableEnabled(address(this));

39:         return claimMaxGasYields(address(this), recipient);

52:         return claimAllNativeYields(address(this), recipient);

71:         amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));
```

- *MagicLP.sol* ( [229-229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L229-L229), [233-233](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L233-L233), [245-245](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L245-L245), [262-262](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L262-L262), [268-268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L268-L268), [285-285](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L285-L285), [298-298](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L298-L298), [299-299](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L299-L299), [361-361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L361-L361), [362-362](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L362-L362), [427-427](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L427-L427), [431-431](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L431-L431), [432-432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L432-L432), [505-505](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L505-L505), [506-506](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L506-L506), [529-529](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L529-L529), [530-530](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L530-L530), [568-568](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L568-L568), [569-569](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L569-L569), [615-615](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L615-L615), [622-622](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L622-L622) ):

```solidity
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

- *Factory.sol* ( [77-77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L77-L77) ):

```solidity
77:                 address(this)
```

- *Router.sol* ( [92-92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L92-L92), [269-269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L269-L269), [282-282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L282-L282), [289-289](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L289-L289), [298-298](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L298-L298), [398-398](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L398-L398), [444-444](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L444-L444), [490-490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L490-L490) ):

```solidity
92:         address(weth).safeTransferFrom(address(this), clone, msg.value);

269:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

282:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

289:                 address(this),

298:                 address(this),

398:         amountOut = _swap(address(this), path, directions, minimumOut);

444:         amountOut = _sellBase(lp, address(this), minimumOut);

490:         amountOut = _sellQuote(lp, address(this), minimumOut);
```

- *LockingMultiRewards.sol* ( [326-326](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L326-L326), [367-367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L367-L367), [464-464](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L464-L464) ):

```solidity
326:         if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

367:         rewardToken.safeTransferFrom(msg.sender, address(this), amount);

464:         stakingToken.safeTransferFrom(msg.sender, address(this), amount);
```

</details>

### [G-16] Remove empty functions to save gas

Empty function body in solidity is not recommended, remove it can save gas.

There is 1 instance:

- *MagicLP.sol* ( [601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L601) ):

```solidity
601:     function _afterInitialized() internal virtual {}
```

### [G-17] Usage of `int`s/`uint`s smaller than 32 bytes incurs overhead

Using `ints`/`uints` smaller than 32 bytes may cost more gas. This is because the EVM operates on 32 bytes at a time, so if an element is smaller than 32 bytes, the EVM must perform more operations to reduce the size of the element from 32 bytes to the desired size.

<details>
<summary>There are 22 instances (click to show):</summary>

- *MagicLP.sol* ( [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L72-L72), [73-73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L73-L73), [74-74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L74-L74), [76-76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L76-L76), [77-77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L77-L77), [78-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L78-L78), [80-80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L80-L80), [163-163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L163-L163), [546-546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L546-L546), [547-547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L547-L547) ):

```solidity
/// @audit uint112
72:     uint112 public _BASE_RESERVE_;

/// @audit uint112
73:     uint112 public _QUOTE_RESERVE_;

/// @audit uint32
74:     uint32 public _BLOCK_TIMESTAMP_LAST_;

/// @audit uint112
76:     uint112 public _BASE_TARGET_;

/// @audit uint112
77:     uint112 public _QUOTE_TARGET_;

/// @audit uint32
78:     uint32 public _RState_;

/// @audit uint256
80:     uint256 public _LP_FEE_RATE_;

/// @audit uint8
163:     function decimals() public view override returns (uint8) {

/// @audit uint32
546:         uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);

/// @audit uint32
547:         uint32 timeElapsed = blockTimestamp - _BLOCK_TIMESTAMP_LAST_;
```

- *Router.sol* ( [598-598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L598-L598), [598-598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L598-L598) ):

```solidity
/// @audit uint8
598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {

/// @audit uint8
598:     function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {
```

- *MagicLpAggregator.sol* ( [13-13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L13-L13), [14-14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L14-L14), [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L29-L29), [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L48-L48), [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L48-L48) ):

```solidity
/// @audit uint8
13:     uint8 public immutable baseDecimals;

/// @audit uint8
14:     uint8 public immutable quoteDecimals;

/// @audit uint8
29:     function decimals() external pure override returns (uint8) {

/// @audit uint80
48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {

/// @audit uint80
48:     function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```

- *LockingMultiRewards.sol* ( [51-51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L51-L51), [52-52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L52-L52), [55-55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L55-L55), [65-65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L65-L65), [75-75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L75-L75) ):

```solidity
/// @audit uint256
51:         uint256 periodFinish;

/// @audit uint256
52:         uint256 rewardRate;

/// @audit uint248
55:         uint248 lastUpdateTime;

/// @audit uint256
65:         uint256 unlockTime;

/// @audit uint256
75:         uint256 unlockTime;
```

</details>

### [G-18] Using a double `if` statement instead of a logical AND(`&&`)

Using a double `if` statement instead of a logical AND (`&&`) can provide similar short-circuiting behavior whereas double if is slightly [more gas efficient](https://gist.github.com/DadeKuma/931ce6794a050201ec6544dbcc31316c).

<details>
<summary>There are 11 instances (click to show):</summary>

- *BlastMagicLP.sol* ( [119-119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L119-L119) ):

```solidity
119:         if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
```

- *BlastOnboarding.sol* ( [114-114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L114-L114) ):

```solidity
114:         if (caps[token] > 0 && totals[token].total > caps[token]) {
```

- *MagicLP.sol* ( [139-139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L139-L139), [144-144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L144-L144), [302-302](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L302-L302), [395-395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L395-L395), [549-549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L549-L549) ):

```solidity
139:         if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {

144:         if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

302:         if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {

395:         } else if (baseReserve > 0 && quoteReserve > 0) {

549:         if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
```

- *Router.sol* ( [147-147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L147-L147), [527-527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L527-L527) ):

```solidity
147:         } else if (baseReserve > 0 && quoteReserve > 0) {

527:             if (quoteReserve > 0 && baseReserve > 0) {
```

- *LockingMultiRewards.sol* ( [326-326](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L326-L326), [417-417](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L417-L417) ):

```solidity
326:         if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

417:             if (index == lastLockIndex[user] && locks.length > 1) {
```

</details>

### [G-19] Reduce deployment costs by tweaking contracts' metadata

See [this](https://www.rareskills.io/post/solidity-metadata) link, at its bottom, for full details.

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

- *MagicLpAggregator.sol* ( [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L9) ):

```solidity
9: contract MagicLpAggregator is IAggregator {
```

- *LockingMultiRewards.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L14) ):

```solidity
14: contract LockingMultiRewards is OperatableV2, Pausable {
```

</details>

### [G-20] Divisions can be unchecked to save gas

The expression `type(int).min/(-1)` is the only case where division causes an overflow. Therefore, uncheck can be used to [save gas](https://gist.github.com/DadeKuma/3bc597338ae774b8b3bd43280d55271f) in scenarios where it is certain that such an overflow will not occur.

<details>
<summary>There are 40 instances (click to show):</summary>

- *BlastOnboardingBoot.sol* ( [163-163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L163-L163) ):

```solidity
163:         return (userLocked * totalPoolShares) / totalLocked;
```

- *MagicLP.sol* ( [435-435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L435-L435), [436-436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L436-L436), [513-513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L513-L513), [517-517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L517-L517) ):

```solidity
435:         baseAmount = (baseBalance * shareAmount) / totalShares;

436:         quoteAmount = (quoteBalance * shareAmount) / totalShares;

513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
```

- *DecimalMath.sol* ( [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L24-L24), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L32-L32), [40-40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L40-L40), [53-53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L53-L53), [54-54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L54-L54), [56-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L56-L56) ):

```solidity
24:         return (target * d) / ONE;

32:         return (target * ONE) / d;

40:         return ONE2 / target;

53:             uint p = powFloor(target, e / 2);

54:             p = (p * p) / ONE;

56:                 p = (p * target) / ONE;
```

- *Math.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L20-L20), [30-30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L30-L30), [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L34-L34), [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L34-L34), [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L59-L59), [62-62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L62-L62), [64-64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L64-L64), [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L96-L96), [97-97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L97-L97), [99-99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L99-L99), [155-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L155-L155), [156-156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L156-L156), [158-158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L158-L158), [158-158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L158-L158), [160-160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L160-L160), [170-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L170-L170), [181-181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L181-L181) ):

```solidity
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

- *PMMPricing.sol* ( [205-205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L205-L205), [209-209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L209-L209) ):

```solidity
205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);

209:             uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
```

- *Router.sol* ( [257-257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L257-L257), [258-258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L258-L258) ):

```solidity
257:         baseAmountOut = (baseBalance * sharesIn) / totalShares;

258:         quoteAmountOut = (quoteBalance * sharesIn) / totalShares;
```

- *MagicLpAggregator.sol* ( [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L45-L45) ):

```solidity
45:         return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
```

- *LockingMultiRewards.sol* ( [144-144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L144-L144), [236-236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L236-L236), [241-241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L241-L241), [258-258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L258-L258), [283-283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L283-L283), [294-294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L294-L294), [388-388](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L388-L388) ):

```solidity
144:         maxLocks = _lockDuration / _rewardsDuration;

236:         return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);

241:         return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);

258:         return (block.timestamp / rewardsDuration) * rewardsDuration;

283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

294:         return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];

388:         reward.rewardRate = amount / _remainingRewardTime;
```

</details>

### [G-21] Remove unused local variables

Unused local variables to save gas.

There are 2 instances:

- *MagicLpAggregator.sol* ( [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L34-L34), [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L34-L34) ):

```solidity
34:         (uint256 baseReserve, uint256 quoteReserve) = pair.getReserves();

34:         (uint256 baseReserve, uint256 quoteReserve) = pair.getReserves();
```

### [G-22] Use assembly to validate `msg.sender`

We can use assembly to efficiently validate msg.sender with the least amount of opcodes necessary. For more details check the following report [Here](https://code4rena.com/reports/2023-05-juicebox#g-06-use-assembly-to-validate-msgsender)

There are 2 instances:

- *BlastMagicLP.sol* ( [119-119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L119-L119) ):

```solidity
119:         if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
```

- *MagicLP.sol* ( [608-608](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L608-L608) ):

```solidity
608:         if (msg.sender != implementation.owner()) {
```

### [G-23] Using assembly to check for zero can save gas

Using assembly to check for zero can save gas by allowing more direct access to the evm and reducing some of the overhead associated with high-level operations in solidity.

<details>
<summary>There are 56 instances (click to show):</summary>

- *BlastBox.sol* ( [25-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L25-L25), [28-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L28-L28), [73-73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L73-L73) ):

```solidity
25:         if (feeTo_ == address(0)) {

28:         if (address(registry_) == address(0)) {

73:         if (feeTo_ == address(0)) {
```

- *BlastGovernor.sol* ( [16-16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L16-L16), [41-41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L41-L41) ):

```solidity
16:         if (feeTo_ == address(0)) {

41:         if(_feeTo == address(0)) {
```

- *BlastMagicLP.sol* ( [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L24-L24), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L27-L27), [81-81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L81-L81) ):

```solidity
24:         if (feeTo_ == address(0)) {

27:         if (address(registry_) == address(0)) {

81:         if (feeTo_ == address(0)) {
```

- *BlastOnboarding.sol* ( [85-85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L85-L85), [89-89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L89-L89), [148-148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L148-L148) ):

```solidity
85:         if (address(registry_) == address(0)) {

89:         if (feeTo_ == address(0)) {

148:         if (feeTo_ == address(0)) {
```

- *BlastOnboardingBoot.sol* ( [64-64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L64-L64), [97-97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L97-L97), [158-158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L158-L158) ):

```solidity
64:         if (shares == 0) {

97:         if (pool != address(0)) {

158:         if (totalLocked == 0) {
```

- *BlastTokenRegistry.sol* ( [15-15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L15-L15) ):

```solidity
15:         if (token == address(0)) {
```

- *BlastWrappers.sol* ( [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L21-L21), [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L35-L35), [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L48-L48) ):

```solidity
21:         if (governor_ == address(0)) {

35:         if (governor_ == address(0)) {

48:         if (governor_ == address(0)) {
```

- *MagicLP.sol* ( [369-369](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L369-L369), [375-375](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L375-L375), [377-377](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L377-L377), [385-385](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L385-L385) ):

```solidity
369:         if (baseInput == 0) {

375:         if (totalSupply() == 0) {

377:             if (quoteBalance == 0) {

385:             if (_QUOTE_TARGET_ == 0) {
```

- *FeeRateModel.sol* ( [23-23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L23-L23), [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L35-L35), [47-47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L47-L47) ):

```solidity
23:         if (maintainer_ == address(0)) {

35:         if (implementation == address(0)) {

47:         if (maintainer_ == address(0)) {
```

- *DecimalMath.sol* ( [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L48-L48) ):

```solidity
48:         if (e == 0) {
```

- *Math.sol* ( [52-52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L52-L52), [58-58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L58-L58), [80-80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L80-L80), [89-89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L89-L89), [94-94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L94-L94), [132-132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L132-L132), [136-136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L136-L136), [140-140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L140-L140), [153-153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L153-L153), [192-192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L192-L192) ):

```solidity
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

- *Factory.sol* ( [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L39-L39), [42-42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L42-L42), [97-97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L97-L97), [106-106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L106-L106) ):

```solidity
39:         if (implementation_ == address(0)) {

42:         if (address(maintainerFeeRateModel_) == address(0)) {

97:         if (implementation_ == address(0)) {

106:         if (address(maintainerFeeRateModel_) == address(0)) {
```

- *Router.sol* ( [125-125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L125-L125), [131-131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L131-L131), [132-132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L132-L132), [327-327](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L327-L327), [348-348](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L348-L348), [379-379](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L379-L379), [392-392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L392-L392), [521-521](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L521-L521), [545-545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L545-L545) ):

```solidity
125:         if (baseInAmount == 0) {

131:         if (totalSupply == 0) {

132:             if (quoteBalance == 0) {

327:         if (directions & 1 == 0) {

348:         if (directions & 1 == 0) {

379:         if ((directions >> lastLpIndex) & 1 == 0) {

392:         if (directions & 1 == 0) {

521:         if (IERC20(lp).totalSupply() == 0) {

545:             if (directions & 1 == 0) {
```

- *LockingMultiRewards.sol* ( [131-131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L131-L131), [156-156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L156-L156), [171-171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L171-L171), [278-278](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L278-L278), [301-301](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L301-L301), [410-410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L410-L410), [459-459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L459-L459) ):

```solidity
131:         if (_lockDuration % _rewardsDuration != 0) {

156:         if (amount == 0) {

171:         if (amount == 0) {

278:         if (totalSupply_ == 0) {

301:         if (rewardToken == address(0)) {

410:             if (locks.length == 0) {

459:         if (amount == 0) {
```

</details>

### [G-24] Consider using OZ EnumerateSet in place of nested mappings

Nested mappings and multi-dimensional arrays involve a double hashing process, which can be costly in terms of gas due to the repeated hashing and storage operations. An optimization approach is to manually concatenate keys and perform a single hash and storage operation, but this increases the risk of storage collisions, especially when there are other nested hash maps using the same key types. OpenZeppelin's EnumerableSet offers a solution by combining set operations with element enumeration, providing a gas-efficient and collision-resistant alternative for certain scenarios where nested mappings or multi-dimensional arrays are used in Solidity.

There are 4 instances:

- *BlastOnboarding.sol* ( [41-41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L41-L41) ):

```solidity
41:     mapping(address user => mapping(address token => Balances)) public balances;
```

- *Factory.sol* ( [35-35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L35-L35) ):

```solidity
35:     mapping(address base => mapping(address quote => address[] pools)) public pools;
```

- *LockingMultiRewards.sol* ( [94-94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L94-L94), [95-95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L95-L95) ):

```solidity
94:     mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;

95:     mapping(address user => mapping(address token => uint256 amount)) public rewards;
```

### [G-25] Consider using solady's `FixedPointMathLib`

Saves gas, and works to avoid unnecessary [overflows](https://github.com/Vectorized/solady/blob/9deb9ed36a27261a8745db5b7cd7f4cdc3b1cd4e/src/utils/FixedPointMathLib.sol#L436).

<details>
<summary>There are 33 instances (click to show):</summary>

- *BlastOnboardingBoot.sol* ( [163-163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L163-L163) ):

```solidity
163:         return (userLocked * totalPoolShares) / totalLocked;
```

- *MagicLP.sol* ( [435-435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L435-L435), [436-436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L436-L436), [513-513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L513-L513), [517-517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L517-L517) ):

```solidity
435:         baseAmount = (baseBalance * shareAmount) / totalShares;

436:         quoteAmount = (quoteBalance * shareAmount) / totalShares;

513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
```

- *DecimalMath.sol* ( [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L24-L24), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L32-L32), [54-54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L54-L54), [56-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L56-L56) ):

```solidity
24:         return (target * d) / ONE;

32:         return (target * ONE) / d;

54:             p = (p * p) / ONE;

56:                 p = (p * target) / ONE;
```

- *Math.sol* ( [62-62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L62-L62), [64-64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L64-L64), [96-96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L96-L96), [97-97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L97-L97), [99-99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L99-L99), [155-155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L155-L155), [156-156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L156-L156), [158-158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L158-L158), [160-160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L160-L160), [170-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L170-L170) ):

```solidity
62:         uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);

64:         return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;

96:         } else if ((ki * delta) / ki == delta) {

97:             _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);

99:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);

155:             } else if ((idelta * V1) / idelta == V1) {

156:                 temp = (idelta * V1) / (V0 * V0);

158:                 temp = (((delta * V1) / V0) * i) / V0;

160:             return (V1 * temp) / (temp + DecimalMath.ONE);

170:         uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
```

- *PMMPricing.sol* ( [205-205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L205-L205), [209-209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L209-L209) ):

```solidity
205:             uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);

209:             uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
```

- *Router.sol* ( [257-257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L257-L257), [258-258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L258-L258) ):

```solidity
257:         baseAmountOut = (baseBalance * sharesIn) / totalShares;

258:         quoteAmountOut = (quoteBalance * sharesIn) / totalShares;
```

- *MagicLpAggregator.sol* ( [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L45-L45) ):

```solidity
45:         return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
```

- *LockingMultiRewards.sol* ( [236-236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L236-L236), [241-241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L241-L241), [258-258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L258-L258), [283-283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L283-L283), [294-294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L294-L294) ):

```solidity
236:         return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);

241:         return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);

258:         return (block.timestamp / rewardsDuration) * rewardsDuration;

283:         uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

294:         return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];
```

</details>

### [G-26] Avoid zero transfer to save gas

In Solidity, unnecessary operations can waste gas. For example, a transfer function without a zero amount check uses gas even if called with a zero amount, since the contract state remains unchanged. Implementing a zero amount check avoids these unnecessary function calls, saving gas and improving efficiency.

<details>
<summary>There are 30 instances (click to show):</summary>

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

- *Router.sol* ( [68-68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L68-L68), [69-69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L69-L69), [91-91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L91-L91), [92-92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L92-L92), [172-172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L172-L172), [173-173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L173-L173), [186-186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L186-L186), [187-187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L187-L187), [217-217](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L217-L217), [224-224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L224-L224), [244-244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L244-L244), [246-246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L246-L246), [311-311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L311-L311), [328-328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L328-L328), [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L330-L330), [360-360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L360-L360), [393-393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L393-L393), [395-395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L395-L395), [411-411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L411-L411), [428-428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L428-L428), [443-443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L443-L443), [456-456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L456-L456), [474-474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L474-L474), [489-489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L489-L489) ):

```solidity
68:         baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);

69:         quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);

91:         token.safeTransferFrom(msg.sender, clone, tokenInAmount);

92:         address(weth).safeTransferFrom(address(this), clone, msg.value);

172:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);

173:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);

186:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);

187:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);

217:         address(weth).safeTransfer(lp, wethAdjustedAmount);

224:         token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);

244:         address(weth).safeTransfer(lp, msg.value);

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

### [G-27] Cache address(this) when used more than once

Caching address(this) when used more than once can save gas.

<details>
<summary>There are 25 instances (click to show):</summary>

- *BlastOnboardingBoot.sol* ( [106-106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L106-L106), [117-117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L117-L117), [118-118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L118-L118) ):

```solidity
106:         (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

117:         staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));

118:         staking.setOperator(address(this), true);
```

- *BlastYields.sol* ( [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L21-L21), [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L26-L26) ):

```solidity
21:         if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {

26:         emit LogBlastTokenClaimableEnabled(address(this), token);
```

- *MagicLP.sol* ( [245-245](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L245-L245), [262-262](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L262-L262), [268-268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L268-L268), [285-285](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L285-L285), [298-298](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L298-L298), [299-299](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L299-L299), [361-361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L361-L361), [362-362](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L362-L362), [427-427](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L427-L427), [431-431](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L431-L431), [432-432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L432-L432), [505-505](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L505-L505), [506-506](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L506-L506), [529-529](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L529-L529), [530-530](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L530-L530), [568-568](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L568-L568), [569-569](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L569-L569) ):

```solidity
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
```

- *Router.sol* ( [282-282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L282-L282), [289-289](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L289-L289), [298-298](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L298-L298) ):

```solidity
282:         lp.safeTransferFrom(msg.sender, address(this), sharesIn);

289:                 address(this),

298:                 address(this),
```

</details>

### [G-28] State variable read in a loop

The state variable should be cached in and read from a local variable, or accumulated in a local variable then written to storage once outside of the loop, rather than reading/updating it on every iteration of the loop, which will replace each Gwarmaccess (**100 gas**) with a much cheaper stack read.

There are 2 instances:

- *BlastOnboarding.sol* ( [165-172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L165-L172) ):

```solidity
/// @audit registry
/// @audit feeTo
165:         for (uint256 i = 0; i < tokens.length; i++) {
166:             if (!supportedTokens[tokens[i]]) {
167:                 revert ErrUnsupportedToken();
168:             }
169:             if (registry.nativeYieldTokens(tokens[i])) {
170:                 BlastYields.claimAllTokenYields(tokens[i], feeTo);
171:             }
172:         }
```

### [G-29] State variable written in a loop

The code should be refactored such that updates made to the state variable are instead accumulated/tracked in a local variable, then be written a single time outside the loop, converting a Gsreset (**2900 gas**) to a stack write for each iteration.

<details>
<summary>There is 1 instance (click to show):</summary>

- *LockingMultiRewards.sol* ( [405-452](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L405-L452) ):

```solidity
/// @audit unlockedSupply
/// @audit lockedSupply
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
```

</details>

### [G-30] Unlimited gas consumption risk due to external call recipients

When calling an external function without specifying a gas limit , the called contract may consume all the remaining gas, causing the tx to be reverted. To mitigate this, it is recommended to explicitly set a gas limit when making low level external calls.

There is 1 instance:

- *BlastGovernor.sol* ( [54-54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L54-L54) ):

```solidity
54:         (success, result) = to.call{value: value}(data);
```

### [G-31] Optimize names to save gas

`public`/`external` function names and `public` member variable names can be optimized to save gas. Below are the interfaces/abstract contracts that can be optimized so that the most frequently-called functions use the least amount of gas possible during method lookup. Method IDs that have two leading zero bytes can save 128 gas each during deployment, and renaming functions to have lower method IDs will save 22 gas per call, [per sorted position shifted](https://medium.com/joyso/solidity-how-does-function-name-affect-gas-consumption-in-smart-contract-47d270d8ac92).

<details>
<summary>There are 14 instances (click to show):</summary>

- *BlastBox.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L13) ):

```solidity
/// @audit claimGasYields(), claimTokenYields(), callBlastPrecompile(), setFeeTo(), setTokenEnabled(), registry, enabledTokens, feeTo
13: contract BlastBox is DegenBox, OperatableV3 {
```

- *BlastGovernor.sol* ( [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L7) ):

```solidity
/// @audit claimNativeYields(), claimMaxGasYields(), setFeeTo(), callBlastPrecompile(), execute(), feeTo
7: contract BlastGovernor is OperatableV2 {
```

- *BlastMagicLP.sol* ( [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L10) ):

```solidity
/// @audit version(), claimGasYields(), claimTokenYields(), updateTokenClaimables(), callBlastPrecompile(), setFeeTo(), setOperator(), registry, feeTo, operators
10: contract BlastMagicLP is MagicLP {
```

- *BlastOnboarding.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L12), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L64) ):

```solidity
/// @audit state, bootstrapper, feeTo, registry, supportedTokens, totals, caps, balances
12: contract BlastOnboardingData is Owned, Pausable {

/// @audit deposit(), lock(), withdraw(), setFeeTo(), callBlastPrecompile(), claimGasYields(), claimTokenYields(), setTokenSupported(), setCap(), setBootstrapper(), open(), close(), rescue(), pause(), unpause()
64: contract BlastOnboarding is BlastOnboardingData, Proxy {
```

- *BlastOnboardingBoot.sol* ( [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L23), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L34) ):

```solidity
/// @audit pool, router, factory, totalPoolShares, ready, staking, claimed
23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {

/// @audit claim(), claimable(), previewTotalPoolShares(), bootstrap(), initialize(), setStaking(), setReady()
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```

- *BlastTokenRegistry.sol* ( [6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L6) ):

```solidity
/// @audit setNativeYieldTokenEnabled(), nativeYieldTokens
6: contract BlastTokenRegistry is Owned {
```

- *MagicLP.sol* ( [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L25) ):

```solidity
/// @audit init(), sync(), correctRState(), querySellBase(), querySellQuote(), getPMMState(), getPMMStateForCall(), getMidPrice(), getReserves(), getUserFeeRate(), getBaseInput(), getQuoteInput(), version(), sellBase(), sellQuote(), flashLoan(), buyShares(), sellShares(), rescue(), setParameters(), ratioSync(), implementation, MAX_I, MAX_K, MIN_LP_FEE_RATE, MAX_LP_FEE_RATE, _BASE_TOKEN_, _QUOTE_TOKEN_, _BASE_RESERVE_, _QUOTE_RESERVE_, _BLOCK_TIMESTAMP_LAST_, _BASE_PRICE_CUMULATIVE_LAST_, _BASE_TARGET_, _QUOTE_TARGET_, _RState_, _MT_FEE_RATE_MODEL_, _LP_FEE_RATE_, _K_, _I_
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```

- *FeeRateModel.sol* ( [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L13) ):

```solidity
/// @audit getFeeRate(), setMaintainer(), setImplementation(), maintainer, implementation
13: contract FeeRateModel is Owned {
```

- *Factory.sol* ( [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L11) ):

```solidity
/// @audit getPoolCount(), getUserPoolCount(), predictDeterministicAddress(), create(), setLpImplementation(), setMaintainerFeeRateModel(), addPool(), removePool(), implementation, maintainerFeeRateModel, pools, userPools
11: contract Factory is Owned {
```

- *Router.sol* ( [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L12) ):

```solidity
/// @audit createPool(), createPoolETH(), previewCreatePool(), previewAddLiquidity(), addLiquidity(), addLiquidityUnsafe(), addLiquidityETH(), addLiquidityETHUnsafe(), previewRemoveLiquidity(), removeLiquidity(), removeLiquidityETH(), swapTokensForTokens(), swapETHForTokens(), swapTokensForETH(), sellBaseTokensForTokens(), sellBaseETHForTokens(), sellBaseTokensForETH(), sellQuoteTokensForTokens(), sellQuoteETHForTokens(), sellQuoteTokensForETH(), MAX_BASE_QUOTE_DECIMALS_DIFFERENCE, weth, factory
12: contract Router {
```

- *MagicLpAggregator.sol* ( [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L9) ):

```solidity
/// @audit latestAnswer(), latestRoundData(), pair, baseOracle, quoteOracle, baseDecimals, quoteDecimals, WAD
9: contract MagicLpAggregator is IAggregator {
```

- *LockingMultiRewards.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L14) ):

```solidity
/// @audit stake(), lock(), withdraw(), withdrawWithRewards(), getRewards(), rewardData(), rewardsForDuration(), rewardTokensLength(), balances(), userRewardLock(), userLocks(), userLocksLength(), locked(), unlocked(), nextUnlockTime(), epoch(), nextEpoch(), remainingEpochTime(), lastTimeRewardApplicable(), rewardPerToken(), _rewardPerToken(), earned(), addReward(), setMinLockAmount(), recover(), pause(), unpause(), stakeFor(), notifyRewardAmount(), processExpiredLocks(), maxLocks, lockingBoostMultiplerInBips, rewardsDuration, lockDuration, stakingToken, userRewardPerTokenPaid, rewards, lastLockIndex, rewardTokens, lockedSupply, unlockedSupply, minLockAmount, stakingTokenBalance
14: contract LockingMultiRewards is OperatableV2, Pausable {
```

</details>

### [G-32] Reduce gas usage by moving to Solidity 0.8.19 or later

Solidity version 0.8.19 introduced a number of gas optimizations, refer to the [Solidity 0.8.19 Release Announcement](https://soliditylang.org/blog/2023/02/22/solidity-0.8.19-release-announcement) for details.

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

### [G-33] Newer versions of solidity are more gas efficient

The solidity language continues to pursue more efficient gas optimization schemes. Adopting a [newer version of solidity](https://github.com/ethereum/solc-js/tags) can be more gas efficient.

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

### [G-34] Avoid updating storage when the value hasn't changed

Manipulating storage in solidity is gas-intensive. It can be optimized by avoiding unnecessary storage updates when the new value equals the existing value.
If the old value is equal to the new value, not re-storing the value will avoid a Gsreset (**2900 gas**), potentially at the expense of a Gcoldsload (**2100 gas**) or a Gwarmaccess (**100 gas**).

<details>
<summary>There are 54 instances (click to show):</summary>

- *BlastBox.sol* ( [77-77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L77-L77), [82-82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L82-L82) ):

```solidity
77:         feeTo = feeTo_;

82:         enabledTokens[token] = enabled;
```

- *BlastGovernor.sol* ( [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L45-L45) ):

```solidity
45:         feeTo = _feeTo;
```

- *BlastMagicLP.sol* ( [85-85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L85-L85), [90-90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L90-L90) ):

```solidity
85:         feeTo = feeTo_;

90:         operators[operator] = status;
```

- *BlastOnboarding.sol* ( [152-152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L152-L152), [176-176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L176-L176), [186-186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L186-L186), [191-191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L191-L191), [196-196](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L196-L196), [201-201](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L201-L201) ):

```solidity
152:         feeTo = feeTo_;

176:         supportedTokens[token] = supported;

186:         caps[token] = cap;

191:         bootstrapper = bootstrapper_;

196:         state = State.Opened;

201:         state = State.Closed;
```

- *BlastOnboardingBoot.sol* ( [142-142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L142-L142), [147-147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L147-L147) ):

```solidity
142:         staking = _staking;

147:         ready = _ready;
```

- *BlastTokenRegistry.sol* ( [19-19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L19-L19) ):

```solidity
19:         nativeYieldTokens[token] = enabled;
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

- *LockingMultiRewards.sol* ( [319-319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L319-L319), [537-537](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L537-L537), [538-538](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L538-L538) ):

```solidity
319:         minLockAmount = _minLockAmount;

537:         rewards[user_][token_] = _earned(user_, balance_, token_, rewardPerToken_);

538:         userRewardPerTokenPaid[user_][token_] = rewardPerToken_;
```

</details>

### [G-35] Same cast is done multiple times

It's cheaper to do it once, and store the result to a variable. The examples below are the second+ instance of a given cast of the variable.

<details>
<summary>There are 14 instances (click to show):</summary>

- *MagicLP.sol* ( [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L145), [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L258), [281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L281), [315](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L315), [322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L322), [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L337), [342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L342), [344](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L344), [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L402), [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L403), [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L438), [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L439), [538](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L538), [539](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L539) ):

```solidity
145:             _RState_ = uint32(PMMPricing.RState.ONE);

258:             _RState_ = uint32(newRState);

281:             _RState_ = uint32(newRState);

315:             if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {

322:                 _RState_ = uint32(newRState);

337:             if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {

342:             if (_RState_ != uint32(newRState)) {

344:                 _RState_ = uint32(newRState);

402:             _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

403:             _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();

438:         _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));

439:         _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));

538:         _BASE_TARGET_ = uint112(baseBalance);

539:         _QUOTE_TARGET_ = uint112(quoteBalance);
```

</details>

### [G-36] State variables that are used multiple times in a function should be cached in stack variables

When performing multiple operations on a state variable in a function, it is recommended to cache it first. Either multiple reads or multiple writes to a state variable can save gas by caching it on the stack.
Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.
*Saves 100 gas per instance*.

<details>
<summary>There are 34 instances (click to show):</summary>

- *BlastMagicLP.sol* ( [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L53), [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L104) ):

```solidity
/// @audit _BASE_TOKEN_: 2 reads
/// @audit _QUOTE_TOKEN_: 2 reads
53:     function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {

/// @audit _BASE_TOKEN_: 2 reads
/// @audit _QUOTE_TOKEN_: 2 reads
104:     function _updateTokenClaimables() internal {
```

- *BlastOnboarding.sol* ( [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L101) ):

```solidity
/// @audit totals[token].total: 2 reads 1 writes
101:     function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
```

- *BlastOnboardingBoot.sol* ( [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L96) ):

```solidity
/// @audit pool: 6 reads
/// @audit totalPoolShares: 5 reads
/// @audit staking: 5 reads 1 writes
/// @audit router: 3 reads
96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
```

- *MagicLP.sol* ( [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L138), [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L244), [267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L267), [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L290), [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L360), [413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L413), [504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L504) ):

```solidity
/// @audit _RState_: 2 reads 2 writes
/// @audit _BASE_RESERVE_: 3 reads
/// @audit _BASE_TARGET_: 1 reads 2 writes
/// @audit _QUOTE_RESERVE_: 3 reads
/// @audit _QUOTE_TARGET_: 1 reads 2 writes
138:     function correctRState() external {

/// @audit _BASE_TOKEN_: 2 reads
/// @audit _QUOTE_TOKEN_: 2 reads
244:     function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {

/// @audit _QUOTE_TOKEN_: 2 reads
/// @audit _BASE_TOKEN_: 2 reads
267:     function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {

/// @audit _BASE_RESERVE_: 4 reads
/// @audit _QUOTE_RESERVE_: 4 reads
/// @audit _BASE_TOKEN_: 3 reads
/// @audit _QUOTE_TOKEN_: 3 reads
/// @audit _RState_: 2 reads 2 writes
/// @audit _MT_FEE_RATE_MODEL_: 2 reads
290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

/// @audit _BASE_TARGET_: 2 reads 2 writes
/// @audit _QUOTE_TARGET_: 3 reads 2 writes
/// @audit _I_: 3 reads
360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {

/// @audit _BASE_TARGET_: 2 reads 1 writes
/// @audit _QUOTE_TARGET_: 2 reads 1 writes
413:     function sellShares(

/// @audit _BASE_RESERVE_: 2 reads 1 writes
/// @audit _QUOTE_RESERVE_: 2 reads 1 writes
504:     function ratioSync() external nonReentrant onlyImplementationOwner {
```

- *FeeRateModel.sol* ( [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L34) ):

```solidity
/// @audit implementation: 2 reads
34:     function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```

- *Factory.sol* ( [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L81) ):

```solidity
/// @audit maintainerFeeRateModel: 2 reads
81:     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
```

- *LockingMultiRewards.sol* ( [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L277) ):

```solidity
/// @audit _rewardData[rewardToken].rewardPerTokenStored: 2 reads
277:     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
```

</details>

### [G-37] Use solady library where possible to save gas

The following OpenZeppelin imports have a Solady equivalent, as such they can be used to save GAS as Solady modules have been specifically designed to be as GAS efficient as possible.

<details>
<summary>There are 8 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [7-7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L7-L7), [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L10-L10) ):

```solidity
7: import {Proxy} from "openzeppelin-contracts/proxy/Proxy.sol";

10: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";
```

- *BlastYields.sol* ( [5-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L5-L5) ):

```solidity
5: import {Address} from "openzeppelin-contracts/utils/Address.sol";
```

- *MagicLP.sol* ( [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L11-L11) ):

```solidity
11: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```

- *Router.sol* ( [5-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L5-L5), [10-10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L10-L10) ):

```solidity
5: import {IERC20} from "openzeppelin-contracts/interfaces/IERC20.sol";

10: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```

- *MagicLpAggregator.sol* ( [5-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L5-L5) ):

```solidity
5: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```

- *LockingMultiRewards.sol* ( [5-5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L5-L5) ):

```solidity
5: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";
```

</details>

### [G-38] Use the inputs/results of assignments rather than re-reading state variables

When a state variable is assigned, it saves gas to use the value being assigned, later in the function, rather than re-reading the state variable itself. If needed, it can also be stored to a local variable, and be used in that way. Both options avoid a Gwarmaccess (**100 gas**). Note that if the operation is, say `+=`, the assignment also results in a value which can be used. The instances below point to the first reference after the assignment, since later references are already covered by issues describing the caching of state variable values.

<details>
<summary>There are 27 instances (click to show):</summary>

- *BlastOnboardingBoot.sol* ( [118-118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L118-L118), [119-119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L119-L119), [122-122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L122-L122), [124-124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L124-L124), [126-126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L126-L126), [131-131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L131-L131), [148-148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L148-L148) ):

```solidity
/// @audit use result of assignment of staking
118:         staking.setOperator(address(this), true);

/// @audit use result of assignment of staking
119:         staking.transferOwnership(owner);

/// @audit use result of assignment of staking
122:         pool.safeApprove(address(staking), totalPoolShares);

/// @audit use result of assignment of staking
124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

/// @audit use result of assignment of staking
126:         return (pool, address(staking), totalPoolShares);

/// @audit use result of assignment of router
131:         factory = IFactory(router.factory());

/// @audit use result of assignment of ready
148:         emit LogReadyChanged(ready);
```

- *MagicLP.sol* ( [144-144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L144-L144), [144-144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L144-L144), [145-145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L145-L145), [146-146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L146-L146), [147-147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L147-L147), [342-342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L342-L342), [344-344](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L344-L344), [385-385](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L385-L385), [402-402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L402-L402), [402-402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L402-L402), [402-402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L402-L402), [403-403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L403-L403), [403-403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L403-L403), [403-403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L403-L403), [438-438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L438-L438), [438-438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L438-L438), [439-439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L439-L439), [439-439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L439-L439), [513-513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L513-L513), [517-517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L517-L517) ):

```solidity
/// @audit use result of assignment of _RState_
144:         if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

/// @audit use result of assignment of _QUOTE_TARGET_
144:         if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

/// @audit use result of assignment of _RState_
145:             _RState_ = uint32(PMMPricing.RState.ONE);

/// @audit use result of assignment of _BASE_TARGET_
146:             _BASE_TARGET_ = _BASE_RESERVE_;

/// @audit use result of assignment of _QUOTE_TARGET_
147:             _QUOTE_TARGET_ = _QUOTE_RESERVE_;

/// @audit use result of assignment of _RState_
342:             if (_RState_ != uint32(newRState)) {

/// @audit use result of assignment of _RState_
344:                 _RState_ = uint32(newRState);

/// @audit use result of assignment of _QUOTE_TARGET_
385:             if (_QUOTE_TARGET_ == 0) {

/// @audit use result of assignment of _BASE_TARGET_
402:             _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

/// @audit use result of assignment of _BASE_TARGET_
402:             _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

/// @audit use result of assignment of _BASE_TARGET_
402:             _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

/// @audit use result of assignment of _QUOTE_TARGET_
403:             _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();

/// @audit use result of assignment of _QUOTE_TARGET_
403:             _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();

/// @audit use result of assignment of _QUOTE_TARGET_
403:             _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();

/// @audit use result of assignment of _BASE_TARGET_
438:         _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));

/// @audit use result of assignment of _BASE_TARGET_
438:         _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));

/// @audit use result of assignment of _QUOTE_TARGET_
439:         _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));

/// @audit use result of assignment of _QUOTE_TARGET_
439:         _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));

/// @audit use result of assignment of _BASE_TARGET_
513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

/// @audit use result of assignment of _QUOTE_TARGET_
517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
```

</details>

### [G-39] Contracts can use fewer storage slots by truncating state variables

Some state variables can be safely modified so that the contract uses fewer storage slots. Each saved slot can avoid an extra Gsset (**20000 gas**) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.

There is 1 instance:

- *MagicLP.sol* ( [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L25) ):

```solidity
/// @audit Truncate `_BLOCK_TIMESTAMP_LAST_` to `uint32`
/// @audit Truncate `_LP_FEE_RATE_` to `uint32`
/// @audit Fewer storage usage (9 slots -> 8 slots):
///        32 B: uint256 _BASE_PRICE_CUMULATIVE_LAST_
///        32 B: uint256 _K_
///        32 B: uint256 _I_
///        20 B: address _BASE_TOKEN_
///        4 B: uint32 _BLOCK_TIMESTAMP_LAST_
///        4 B: uint32 _RState_
///        4 B: uint32 _LP_FEE_RATE_
///        20 B: address _QUOTE_TOKEN_
///        1 B: bool _INITIALIZED_
///        20 B: IFeeRateModel _MT_FEE_RATE_MODEL_
///        14 B: uint112 _BASE_RESERVE_
///        14 B: uint112 _QUOTE_RESERVE_
///        14 B: uint112 _BASE_TARGET_
///        14 B: uint112 _QUOTE_TARGET_
25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```

### [G-40] Structs can be packed into fewer storage slots by truncating fields

Some struct fields  can be safely modified so that the struct variable uses fewer storage slots. Each saved slot can avoid an extra Gsset (20000 gas) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.

There is 1 instance:

- *LockingMultiRewards.sol* ( [50-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L50-L56) ):

```solidity
/// @audit Truncate `periodFinish` to `uint32`
/// @audit Truncate `rewardRate` to `uint32`
/// @audit Truncate `lastUpdateTime` to `uint32`
/// @audit Fewer storage usage (4 slots -> 2 slots):
///        32 B: uint256 rewardPerTokenStored
///        4 B: uint32 periodFinish
///        4 B: uint32 rewardRate
///        4 B: uint32 lastUpdateTime
///        1 B: bool exists
50:     struct Reward {
51:         uint256 periodFinish;
52:         uint256 rewardRate;
53:         uint256 rewardPerTokenStored;
54:         bool exists;
55:         uint248 lastUpdateTime;
56:     }
```

### [G-41] Using `constant`s instead of `enum` can save gas

`Enum` is expensive and it is [more efficient to use constants](https://www.codehawks.com/finding/clm84992q02j9w9ruebun36d9) instead. An illustrative example of this approach can be found in the [ReentrancyGuard.sol](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/181d518609a9f006fcb97af63e6952e603cf100e/contracts/utils/ReentrancyGuard.sol#L34-L35).

There are 2 instances:

- *BlastOnboarding.sol* ( [18-22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L18-L22) ):

```solidity
18:     enum State {
19:         Idle,
20:         Opened,
21:         Closed
22:     }
```

- *PMMPricing.sol* ( [21-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/PMMPricing.sol#L21-L25) ):

```solidity
21:     enum RState {
22:         ONE,
23:         ABOVE_ONE,
24:         BELOW_ONE
25:     }
```

### [G-42] Use `Array.unsafeAccess()` to avoid repeated array length checks

When using storage arrays, solidity adds an internal lookup of the array's length (a Gcoldsload **2100 gas**) to ensure you don't read past the array's end. You can avoid this lookup by using [`Array.unsafeAccess()`](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/94697be8a3f0dfcd95dfb13ffbd39b5973f5c65d/contracts/utils/Arrays.sol#L57) in cases where the length has already been checked, as is the case with the instances below.

There are 7 instances:

- *LockingMultiRewards.sol* ( [490-490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L490-L490), [501-501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L501-L501), [510-510](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L510-L510), [548-548](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L548-L548), [562-562](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L562-L562), [576-576](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L576-L576), [615-615](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L615-L615) ):

```solidity
490:         if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {

501:             _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));

510:             _userLocks[user][_lastLockIndex].amount += amount;

548:             _updateRewardsGlobal(rewardTokens[i], totalSupply_);

562:             address token = rewardTokens[i];

576:             address token = rewardTokens[i];

615:             address rewardToken = rewardTokens[i];
```

### [G-43] Assembly: Use scratch space for building calldata

If an external call's calldata can fit into two or fewer words, use the scratch space to build the calldata, rather than allowing Solidity to do a memory expansion.

<details>
<summary>There are 110 instances (click to show):</summary>

- *BlastBox.sol* ( [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L57-L57), [86-86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L86-L86) ):

```solidity
57:         if (!registry.nativeYieldTokens(token_)) {

86:         if (registry.nativeYieldTokens(token)) {
```

- *BlastGovernor.sol* ( [54-54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L54-L54) ):

```solidity
54:         (success, result) = to.call{value: value}(data);
```

- *BlastMagicLP.sol* ( [48-48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L48-L48), [54-54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L54-L54), [56-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L56-L56), [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L59-L59), [105-105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L105-L105), [109-109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L109-L109), [119-119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L119-L119), [119-119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L119-L119) ):

```solidity
48:         address feeTo_ = BlastMagicLP(address(implementation)).feeTo();

54:         address feeTo_ = BlastMagicLP(address(implementation)).feeTo();

56:         if (registry.nativeYieldTokens(_BASE_TOKEN_)) {

59:         if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {

105:         if (registry.nativeYieldTokens(_BASE_TOKEN_)) {

109:         if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {

119:         if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {

119:         if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
```

- *BlastOnboarding.sol* ( [169-169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L169-L169), [178-178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L178-L178) ):

```solidity
169:             if (registry.nativeYieldTokens(tokens[i])) {

178:         if (registry.nativeYieldTokens(token)) {
```

- *BlastOnboardingBoot.sol* ( [118-118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L118-L118), [119-119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L119-L119), [131-131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L131-L131) ):

```solidity
118:         staking.setOperator(address(this), true);

119:         staking.transferOwnership(owner);

131:         factory = IFactory(router.factory());
```

- *BlastPoints.sol* ( [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L11-L11) ):

```solidity
11:         BLAST_POINTS.configurePointsOperator(BLAST_POINTS_OPERATOR);
```

- *BlastYields.sol* ( [21-21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L21-L21), [25-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L25-L25), [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L43-L43), [56-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L56-L56), [71-71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L71-L71), [71-71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L71-L71), [76-76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L76-L76) ):

```solidity
21:         if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {

25:         IERC20Rebasing(token).configure(YieldMode.CLAIMABLE);

43:         amount = BLAST_YIELD_PRECOMPILE.claimMaxGas(contractAddress, recipient);

56:         amount = BLAST_YIELD_PRECOMPILE.claimAllYield(contractAddress, recipient);

71:         amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));

71:         amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));

76:         amount = IERC20Rebasing(token).claim(recipient, amount);
```

- *MagicLP.sol* ( [156-156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L156-L156), [156-156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L156-L156), [164-164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L164-L164), [174-174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L174-L174), [187-187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L187-L187), [225-225](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L225-L225), [253-253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L253-L253), [276-276](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L276-L276), [319-319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L319-L319), [341-341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L341-L341), [608-608](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L608-L608) ):

```solidity
156:         return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));

156:         return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));

164:         return IERC20Metadata(_BASE_TOKEN_).decimals();

174:         (uint256 lpFeeRate, uint256 mtFeeRate) = _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_);

187:         (uint256 lpFeeRate, uint256 mtFeeRate) = _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_);

225:         return _MT_FEE_RATE_MODEL_.getFeeRate(user, _LP_FEE_RATE_);

253:         _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);

276:         _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);

319:             _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);

341:             _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);

608:         if (msg.sender != implementation.owner()) {
```

- *Router.sol* ( [64-64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L64-L64), [64-64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L64-L64), [70-70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L70-L70), [83-83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L83-L83), [85-85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L85-L85), [90-90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L90-L90), [93-93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L93-L93), [117-117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L117-L117), [119-119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L119-L119), [120-120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L120-L120), [129-129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L129-L129), [136-136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L136-L136), [172-172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L172-L172), [173-173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L173-L173), [186-186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L186-L186), [187-187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L187-L187), [202-202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L202-L202), [204-204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L204-L204), [208-208](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L208-L208), [216-216](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L216-L216), [236-236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L236-L236), [238-238](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L238-L238), [239-239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L239-L239), [243-243](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L243-L243), [252-252](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L252-L252), [253-253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L253-L253), [255-255](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L255-L255), [284-284](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L284-L284), [286-286](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L286-L286), [295-295](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L295-L295), [308-308](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L308-L308), [328-328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L328-L328), [330-330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L330-L330), [349-349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L349-L349), [351-351](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L351-L351), [359-359](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L359-L359), [380-380](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L380-L380), [382-382](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L382-L382), [393-393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L393-L393), [395-395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L395-L395), [399-399](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L399-L399), [411-411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L411-L411), [421-421](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L421-L421), [427-427](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L427-L427), [439-439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L439-L439), [443-443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L443-L443), [445-445](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L445-L445), [456-456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L456-L456), [467-467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L467-L467), [473-473](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L473-L473), [485-485](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L485-L485), [489-489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L489-L489), [491-491](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L491-L491), [500-500](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L500-L500), [514-514](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L514-L514), [515-515](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L515-L515), [516-516](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L516-L516), [521-521](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L521-L521), [522-522](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L522-L522), [547-547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L547-L547), [550-550](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L550-L550), [561-561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L561-L561), [563-563](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L563-L563), [572-572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L572-L572), [579-579](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L579-L579) ):

```solidity
64:         _validateDecimals(IERC20Metadata(baseToken).decimals(), IERC20Metadata(quoteToken).decimals());

64:         _validateDecimals(IERC20Metadata(baseToken).decimals(), IERC20Metadata(quoteToken).decimals());

70:         (shares, , ) = IMagicLP(clone).buyShares(to);

83:             _validateDecimals(18, IERC20Metadata(token).decimals());

85:             _validateDecimals(IERC20Metadata(token).decimals(), 18);

90:         weth.deposit{value: msg.value}();

93:         (shares, , ) = IMagicLP(clone).buyShares(to);

117:         (uint256 baseReserve, uint256 quoteReserve) = IMagicLP(lp).getReserves();

119:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;

120:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;

129:         uint256 totalSupply = IERC20(lp).totalSupply();

136:             uint256 i = IMagicLP(lp)._I_();

172:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);

173:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);

186:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);

187:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);

202:         address token = IMagicLP(lp)._BASE_TOKEN_();

204:             token = IMagicLP(lp)._QUOTE_TOKEN_();

208:         } else if (IMagicLP(lp)._QUOTE_TOKEN_() == address(weth)) {

216:         weth.deposit{value: wethAdjustedAmount}();

236:         address token = IMagicLP(lp)._BASE_TOKEN_();

238:             token = IMagicLP(lp)._QUOTE_TOKEN_();

239:         } else if (IMagicLP(lp)._QUOTE_TOKEN_() != address(weth)) {

243:         weth.deposit{value: msg.value}();

252:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp));

253:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp));

255:         uint256 totalShares = IERC20(lp).totalSupply();

284:         address token = IMagicLP(lp)._BASE_TOKEN_();

286:             token = IMagicLP(lp)._QUOTE_TOKEN_();

295:         } else if (IMagicLP(lp)._QUOTE_TOKEN_() == address(weth)) {

308:         weth.withdraw(ethAmountOut);

328:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

330:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

349:             inToken = IMagicLP(firstLp)._BASE_TOKEN_();

351:             inToken = IMagicLP(firstLp)._QUOTE_TOKEN_();

359:         weth.deposit{value: msg.value}();

380:             outToken = IMagicLP(lastLp)._QUOTE_TOKEN_();

382:             outToken = IMagicLP(lastLp)._BASE_TOKEN_();

393:             IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

395:             IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

399:         weth.withdraw(amountOut);

411:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

421:         address baseToken = IMagicLP(lp)._BASE_TOKEN_();

427:         weth.deposit{value: msg.value}();

439:         if (IMagicLP(lp)._QUOTE_TOKEN_() != address(weth)) {

443:         IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

445:         weth.withdraw(amountOut);

456:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

467:         address quoteToken = IMagicLP(lp)._QUOTE_TOKEN_();

473:         weth.deposit{value: msg.value}();

485:         if (IMagicLP(lp)._BASE_TOKEN_() != address(weth)) {

489:         IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

491:         weth.withdraw(amountOut);

500:         (shares, , ) = IMagicLP(lp).buyShares(to);

514:         (uint256 baseReserve, uint256 quoteReserve) = IMagicLP(lp).getReserves();

515:         uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;

516:         uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;

521:         if (IERC20(lp).totalSupply() == 0) {

522:             uint256 i = IMagicLP(lp)._I_();

547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));

550:                 IMagicLP(path[i]).sellQuote(address(path[i + 1]));

561:             amountOut = IMagicLP(path[iterations]).sellBase(to);

563:             amountOut = IMagicLP(path[iterations]).sellQuote(to);

572:         amountOut = IMagicLP(lp).sellBase(to);

579:         amountOut = IMagicLP(lp).sellQuote(to);
```

- *MagicLpAggregator.sol* ( [25-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L25-L25), [25-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L25-L25), [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L26-L26), [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L26-L26), [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L34-L34), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L38-L38), [38-38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L38-L38), [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L39-L39), [39-39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L39-L39), [45-45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L45-L45) ):

```solidity
25:         baseDecimals = IERC20Metadata(pair_._BASE_TOKEN_()).decimals();

25:         baseDecimals = IERC20Metadata(pair_._BASE_TOKEN_()).decimals();

26:         quoteDecimals = IERC20Metadata(pair_._QUOTE_TOKEN_()).decimals();

26:         quoteDecimals = IERC20Metadata(pair_._QUOTE_TOKEN_()).decimals();

34:         (uint256 baseReserve, uint256 quoteReserve) = pair.getReserves();

38:         uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));

38:         uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));

39:         uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));

39:         uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));

45:         return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
```

</details>

### [G-44] Use assembly to emit events

To efficiently emit events, it's possible to utilize assembly by making use of scratch space and the free memory pointer. This approach has the advantage of potentially avoiding the costs associated with memory expansion.

However, it's important to note that in order to safely optimize this process, it is preferable to cache and restore the free memory pointer.

A good example of such practice can be seen in [Solady's](https://github.com/Vectorized/solady/blob/main/src/tokens/ERC1155.sol#L167) codebase.

<details>
<summary>There are 48 instances (click to show):</summary>

- *BlastBox.sol* ( [78-78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L78-L78), [90-90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L90-L90) ):

```solidity
78:         emit LogFeeToChanged(feeTo_);

90:         emit LogTokenDepositEnabled(token, enabled);
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

- *BlastOnboarding.sol* ( [120-120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L120-L120), [129-129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L129-L129), [140-140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L140-L140), [153-153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L153-L153), [182-182](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L182-L182), [187-187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L187-L187), [192-192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L192-L192), [197-197](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L197-L197), [202-202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L202-L202), [211-211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L211-L211) ):

```solidity
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

- *BlastOnboardingBoot.sol* ( [71-71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L71-L71), [124-124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L124-L124), [132-132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L132-L132), [143-143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L143-L143), [148-148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L148-L148) ):

```solidity
71:         emit LogClaimed(msg.sender, shares, lock);

124:         emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

132:         emit LogInitialized(_router);

143:         emit LogStakingChanged(address(_staking));

148:         emit LogReadyChanged(ready);
```

- *BlastTokenRegistry.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastTokenRegistry.sol#L20-L20) ):

```solidity
20:         emit LogNativeYieldTokenEnabled(token, enabled);
```

- *BlastYields.sol* ( [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L26-L26), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L31-L31), [44-44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L44-L44), [57-57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L57-L57), [62-62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L62-L62), [72-72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L72-L72), [77-77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastYields.sol#L77-L77) ):

```solidity
26:         emit LogBlastTokenClaimableEnabled(address(this), token);

31:         emit LogBlastNativeClaimableEnabled(address(this));

44:         emit LogBlastGasClaimed(recipient, amount);

57:         emit LogBlastETHClaimed(recipient, amount);

62:         emit LogBlastETHClaimed(recipient, amount);

72:         emit LogBlastTokenClaimed(recipient, address(token), amount);

77:         emit LogBlastTokenClaimed(recipient, address(token), amount);
```

- *MagicLP.sol* ( [259-259](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L259-L259), [282-282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L282-L282), [323-323](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L323-L323), [345-345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L345-L345), [467-467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L467-L467) ):

```solidity
259:             emit RChange(newRState);

282:             emit RChange(newRState);

323:                 emit RChange(newRState);

345:                 emit RChange(newRState);

467:         emit TokenRescue(token, to, amount);
```

- *FeeRateModel.sol* ( [52-52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L52-L52), [59-59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L59-L59) ):

```solidity
52:         emit LogMaintainerChanged(maintainer_);

59:         emit LogImplementationChanged(implementation_);
```

- *Factory.sol* ( [102-102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L102-L102), [111-111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L111-L111), [141-141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L141-L141) ):

```solidity
102:         emit LogSetImplementation(implementation_);

111:         emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);

141:         emit LogPoolRemoved(pool);
```

- *LockingMultiRewards.sol* ( [183-183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L183-L183), [318-318](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L318-L318), [331-331](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L331-L331), [392-392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L392-L392), [436-436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L436-L436), [447-447](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L447-L447), [475-475](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L475-L475), [611-611](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L611-L611), [638-638](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L638-L638), [651-651](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L651-L651) ):

```solidity
183:         emit LogWithdrawn(msg.sender, amount);

318:         emit LogSetMinLockAmount(minLockAmount, _minLockAmount);

331:         emit LogRecovered(tokenAddress, tokenAmount);

392:         emit LogRewardAdded(amount);

436:                 emit LogLockIndexChanged(user, lastIndex, index);

447:             emit LogUnlocked(user, amount, index);

475:             emit LogStaked(account, amount);

611:             emit LogRewardLockCreated(user, _rewardLock.unlockTime);

638:                         emit LogRewardPaid(user, rewardToken, amount);

651:             emit LogRewardLocked(user, rewardToken, rewardAmount);
```

</details>

### [G-45] Use `calldata` instead of `memory` for immutable arguments

Mark data types as `calldata` instead of `memory` where possible. This makes it so that the data is not automatically loaded into memory. If the data passed into the function does not need to be changed (like updating values in an array), it can be passed in as `calldata`. The one exception to this is if the argument must later be passed into another function that takes an argument that specifies `memory` storage.

There are 2 instances:

- *BlastOnboarding.sol* ( [164-164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L164-L164) ):

```solidity
/// @audit tokens
164:     function claimTokenYields(address[] memory tokens) external onlyOwner {
```

- *LockingMultiRewards.sol* ( [397-397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L397-L397) ):

```solidity
/// @audit users
397:     function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
```

### [G-46] Consider Using Solady's Gas Optimized Lib for Math

In instances where many similar mathematical operations are performed, consider using Solady's math lib to benefit from the gas saving it can introduce.

<details>
<summary>There are 16 instances (click to show):</summary>

- *MagicLP.sol* ( [125-125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L125-L125), [435-435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L435-L435), [436-436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L436-L436), [513-513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L513-L513), [517-517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L517-L517) ):

```solidity
125:         _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

435:         baseAmount = (baseBalance * shareAmount) / totalShares;

436:         quoteAmount = (quoteBalance * shareAmount) / totalShares;

513:             _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

517:             _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
```

- *DecimalMath.sol* ( [54-54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L54-L54), [56-56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L56-L56) ):

```solidity
54:             p = (p * p) / ONE;

56:                 p = (p * target) / ONE;
```

- *Math.sol* ( [34-34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L34-L34), [97-97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L97-L97), [99-99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L99-L99), [156-156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L156-L156), [158-158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L158-L158) ):

```solidity
34:             z = (x / z + z) / 2;

97:             _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);

99:             _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);

156:                 temp = (idelta * V1) / (V0 * V0);

158:                 temp = (((delta * V1) / V0) * i) / V0;
```

- *Router.sol* ( [257-257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L257-L257), [258-258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L258-L258) ):

```solidity
257:         baseAmountOut = (baseBalance * sharesIn) / totalShares;

258:         quoteAmountOut = (quoteBalance * sharesIn) / totalShares;
```

- *MagicLpAggregator.sol* ( [43-43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L43-L43), [44-44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L44-L44) ):

```solidity
43:         baseReserve = baseReserve * (10 ** (WAD - baseDecimals));

44:         quoteReserve = quoteReserve * (10 ** (WAD - quoteDecimals));
```

</details>

### [G-47] `do`-`while` is cheaper than `for`-loops when the initial check can be skipped

`for (uint256 i; i < len; ++i){ ... }` -> `do { ...; ++i } while (i < len);`

There are 8 instances:

- *BlastOnboarding.sol* ( [165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L165) ):

```solidity
165:         for (uint256 i = 0; i < tokens.length; i++) {
```

- *Router.sol* ( [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L544) ):

```solidity
544:         for (uint256 i = 0; i < iterations; ) {
```

- *LockingMultiRewards.sol* ( [405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L405), [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L547), [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L561), [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L575), [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L580), [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L614) ):

```solidity
405:         for (uint256 i; i < users.length; ) {

547:         for (uint256 i; i < rewardTokens.length; ) {

561:         for (uint256 i; i < rewardTokens.length; ) {

575:         for (uint256 i; i < rewardTokens.length; ) {

580:             for (uint256 j; j < users.length; ) {

614:         for (uint256 i; i < rewardTokens.length; ) {
```

### [G-48] Consider activating via-ir for deploying

By using `--via-ir` or `{"viaIR": true}`, the compiler is able to use more advanced [multi-function optimizations](https://docs.soliditylang.org/en/v0.8.17/ir-breaking-changes.html#solidity-ir-based-codegen-changes), for extra gas savings.

There is 1 instance:

- Global finding

### [G-49] Avoid Unnecessary Public Variables

Public state variables automatically generate getter functions, increasing contract size and potentially leading to higher deployment and interaction costs. To optimize gas usage and contract efficiency, minimize the use of public variables unless external access is necessary. Instead, use internal or private visibility combined with explicit getter functions when required. This practice not only reduces contract size but also provides better control over data access and manipulation, enhancing security and readability. Prioritize lean, efficient contracts to ensure cost-effectiveness and better performance on the blockchain.

<details>
<summary>There are 34 instances (click to show):</summary>

- *BlastBox.sol* ( [22-22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L22-L22) ):

```solidity
22:     address public feeTo;
```

- *BlastGovernor.sol* ( [11-11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L11-L11) ):

```solidity
11:     address public feeTo;
```

- *BlastMagicLP.sol* ( [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L20-L20) ):

```solidity
20:     address public feeTo;
```

- *BlastOnboarding.sol* ( [30-30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L30-L30), [31-31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L31-L31), [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L32-L32), [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L33-L33) ):

```solidity
30:     State public state;

31:     address public bootstrapper;

32:     address public feeTo;

33:     BlastTokenRegistry public registry;
```

- *BlastOnboardingBoot.sol* ( [24-24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L24-L24), [25-25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L25-L25), [26-26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L26-L26), [27-27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L27-L27), [28-28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L28-L28), [29-29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L29-L29) ):

```solidity
24:     address public pool;

25:     Router public router;

26:     IFactory public factory;

27:     uint256 public totalPoolShares;

28:     bool public ready;

29:     LockingMultiRewards public staking;
```

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

- *FeeRateModel.sol* ( [19-19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L19-L19), [20-20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L20-L20) ):

```solidity
19:     address public maintainer;

20:     address public implementation;
```

- *Factory.sol* ( [32-32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L32-L32), [33-33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L33-L33) ):

```solidity
32:     address public implementation;

33:     IFeeRateModel public maintainerFeeRateModel;
```

- *LockingMultiRewards.sol* ( [100-100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L100-L100), [101-101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L101-L101), [102-102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L102-L102), [103-103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L103-L103) ):

```solidity
100:     uint256 public lockedSupply; // all locked boosted deposits

101:     uint256 public unlockedSupply; // all unlocked unboosted deposits

102:     uint256 public minLockAmount; // minimum amount allowed to lock

103:     uint256 public stakingTokenBalance; // total staking token balance
```

</details>

### [G-50] Optimize Deployment Size by Fine-tuning IPFS Hash

Optimizing the deployment size of a smart contract is vital to minimize gas costs, and one way to achieve this is by fine-tuning the IPFS hash appended by the Solidity compiler as metadata. This metadata, consisting of 53 bytes, increases the gas required for contract deployment by approximately 10,600 gas due to bytecode costs, and additionally, up to 848 gas due to calldata costs, depending on the proportion of zero and non-zero bytes. Utilize the --no-cbor-metadata compiler flag to prevent the compiler from appending metadata. However, this approach has a drawback as it can complicate the contract verification process on block explorers like Etherscan, potentially reducing transparency.

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

- *MagicLpAggregator.sol* ( [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L9) ):

```solidity
9: contract MagicLpAggregator is IAggregator {
```

- *LockingMultiRewards.sol* ( [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L14) ):

```solidity
14: contract LockingMultiRewards is OperatableV2, Pausable {
```

</details>

### [G-51] The result of a function call should be cached rather than re-calling the function

The function calls in solidity are expensive. If the same result of the same function calls are to be used several times, the result should be cached to reduce the gas consumption of repeated calls.

There are 4 instances:

- *MagicLP.sol* ( [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L290), [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L360), [413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L413) ):

```solidity
/// @audit `_MT_FEE_RATE_MODEL_.maintainer()` called on lines: 319, 341
290:     function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {

/// @audit `totalSupply()` called on lines: 375, 400
360:     function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {

/// @audit `balanceOf(msg.sender)` called on lines: 424, 454
413:     function sellShares(
```

- *Math.sol* ( [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L131) ):

```solidity
/// @audit `DecimalMath.mulFloor(i,delta)` called on lines: 141, 141
131:     function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```

### [G-52] Multiple accesses of a `memory`/`calldata` array should use a local variable cache

The instances below point to the second+ access of a value inside a storage array, within a function. Caching an array index value in a local `storage` or `calldata` variable when the value is accessed [multiple times](https://gist.github.com/IllIllI000/ec23a57daa30a8f8ca8b9681c8ccefb0), saves **~42 gas per access** due to not having to recalculate the array's keccak256 hash (`Gkeccak256` - **30 gas**) and that calculation's associated stack operations.

<details>
<summary>There are 16 instances (click to show):</summary>

- *BlastOnboarding.sol* ( [166-166](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L166-L166), [169-169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L169-L169), [170-170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L170-L170) ):

```solidity
/// @audit tokens...[]
166:             if (!supportedTokens[tokens[i]]) {

/// @audit tokens...[]
169:             if (registry.nativeYieldTokens(tokens[i])) {

/// @audit tokens...[]
170:                 BlastYields.claimAllTokenYields(tokens[i], feeTo);
```

- *Factory.sol* ( [128-128](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L128-L128), [131-131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L131-L131), [134-134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L134-L134), [138-138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L138-L138) ):

```solidity
/// @audit _pools...[]
128:         address pool = _pools[poolIndex];

/// @audit _pools...[]
131:         _pools[poolIndex] = _pools[_pools.length - 1];

/// @audit _userPools...[]
134:         if (_userPools[userPoolIndex] != pool) {

/// @audit _userPools...[]
138:         _userPools[userPoolIndex] = _userPools[_userPools.length - 1];
```

- *Router.sol* ( [547-547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L547-L547), [547-547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L547-L547), [550-550](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L550-L550), [550-550](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L550-L550), [561-561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L561-L561), [563-563](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L563-L563) ):

```solidity
/// @audit path...[]
547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));

/// @audit path...[]
547:                 IMagicLP(path[i]).sellBase(address(path[i + 1]));

/// @audit path...[]
550:                 IMagicLP(path[i]).sellQuote(address(path[i + 1]));

/// @audit path...[]
550:                 IMagicLP(path[i]).sellQuote(address(path[i + 1]));

/// @audit path...[]
561:             amountOut = IMagicLP(path[iterations]).sellBase(to);

/// @audit path...[]
563:             amountOut = IMagicLP(path[iterations]).sellQuote(to);
```

- *LockingMultiRewards.sol* ( [422-422](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L422-L422), [426-426](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L426-L426), [435-435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L435-L435) ):

```solidity
/// @audit locks...[]
422:             if (locks[index].unlockTime > block.timestamp) {

/// @audit locks...[]
426:             uint256 amount = locks[index].amount;

/// @audit locks...[]
435:                 locks[index] = locks[lastIndex];
```

</details>

### [G-53] Multiple accesses of the same mapping key should be cached

Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Even if the values can't be packed, if both fields are accessed in the same function (as is the case for these instances), combining them can save **~42 gas per access** due to [not having to recalculate the key's keccak256 hash](https://gist.github.com/IllIllI000/639032d73e35d7e968ff58d8784bc445) (Gkeccak256 - 30 gas) and that calculation's associated stack operations.

There are 15 instances:

- *BlastOnboarding.sol* ( [112-112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L112-L112), [118-118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L118-L118), [118-118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L118-L118) ):

```solidity
/// @audit `totals[token]` is accessed on line 112, 114, 108, 105
112:         totals[token].total += amount;

/// @audit `balances[msg.sender][token]` is accessed on line 118, 109, 106
118:         balances[msg.sender][token].total += amount;

/// @audit `balances[msg.sender]` is accessed on line 118, 109, 106
118:         balances[msg.sender][token].total += amount;
```

- *LockingMultiRewards.sol* ( [282-282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L282-L282), [430-430](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L430-L430), [483-483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L483-L483) ):

```solidity
/// @audit `_rewardData[rewardToken]` is accessed on line 282, 285, 279, 283
282:         uint256 timeElapsed = lastTimeRewardApplicable_ - _rewardData[rewardToken].lastUpdateTime;

/// @audit `lastLockIndex[user]` is accessed on line 430, 417, 431
430:             if (lastLockIndex[user] == lastIndex) {

/// @audit `_userLocks[user]` is accessed on line 483, 490, 501, 510
483:         uint256 lockCount = _userLocks[user].length;
```
