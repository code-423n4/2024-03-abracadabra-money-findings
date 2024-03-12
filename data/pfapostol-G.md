The content section shows only 10 examples, subsequent cases are listed as links.

## Summary

|                 | Issue                                                                                                                                                      | Instances | Gas Savings |
| --------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------: | :---------: |
| [[G-01](#g-01)] | `<array>.length` Should Not Be Looked Up In Every Loop Of A For-loop                                                                                       |     7     |     679     |
| [[G-02](#g-02)] | Setting the `constructor` to `payable`                                                                                                                     |    16     |     208     |
| [[G-03](#g-03)] | `++i`/`i++` should be `unchecked{++i}`/`unchecked{i++}` when it is not possible for them to overflow, as is the case when used in `for`- and `while`-loops |     1     |     60      |
| [[G-04](#g-04)] | Pre-increments and pre-decrements are cheaper than post-increments and post-decrements                                                                     |     1     |     90      |
| [[G-05](#g-05)] | Use assembly to check for `address(0)`                                                                                                                     |    29     |     174     |
| [[G-06](#g-06)] | `Internal` functions only called once can be inlined to save gas                                                                                           |    12     |     360     |
| [[G-07](#g-07)] | Usage of `uint`/`int` smaller than 32 bytes (256 bits) incurs overhead                                                                                     |    15     |     330     |
| [[G-08](#g-08)] | Functions guaranteed to revert when called by normal users can be marked `payable`                                                                         |    40     |     840     |
| [[G-09](#g-09)] | `>=` costs less gas than `>`                                                                                                                               |    16     |     48      |
| [[G-10](#g-10)] | Multiple mappings can be replaced with a single struct mapping                                                                                             |    13     |   260000    |
| [[G-11](#g-11)] | State variables should be cached in stack variables rather than re-reading them from storage                                                               |    186    |    18042    |
| [[G-12](#g-12)] | Stack variable used as a cheaper cache for a state variable is only used once                                                                              |    24     |     72      |
| [[G-13](#g-13)] | State Variables can be packed into fewer storage slots                                                                                                     |     1     |    20000    |
| [[G-14](#g-14)] | State variables access within a loop                                                                                                                       |     6     |    3180     |
| [[G-15](#g-15)] | Using `private` for constants saves gas                                                                                                                    |    18     |   151308    |
| [[G-16](#g-16)] | Using `bool` for storage incurs overhead                                                                                                                   |     7     |   119700    |
| [[G-17](#g-17)] | State variables only set in the constructor should be declared `immutable`                                                                                 |     1     |    20000    |
| [[G-18](#g-18)] | Consider activating `via-ir` for deploying                                                                                                                 |     1     |      0      |
| [[G-19](#g-19)] | Function calls should be cached instead of re-calling the function                                                                                         |    14     |     672     |
| [[G-20](#g-20)] | Add `unchecked` blocks for divisions where the operands cannot overflow                                                                                    |    40     |    6360     |
| [[G-21](#g-21)] | Multiplication/division by two should use bit shifting                                                                                                     |     7     |     140     |
| [[G-22](#g-22)] | Consider using `bytes32` rather than a `string`                                                                                                            |     4     |     512     |
| [[G-23](#g-23)] | Optimize Zero Checks Using Assembly                                                                                                                        |    84     |    4872     |
| [[G-24](#g-24)] | Consider using `assembly` to write address storage values if the address variable is mutable                                                               |    26     |      0      |
| [[G-25](#g-25)] | Consider Caching Multiple Accesses to Mappings/Arrays                                                                                                      |    22     |    2200     |
| [[G-26](#g-26)] | Optimize Gas by Using Do-While Loops                                                                                                                       |     9     |    2295     |
| [[G-27](#g-27)] | Use Assembly for Efficient Event Emission                                                                                                                  |    59     |   106200    |
| [[G-28](#g-28)] | Optimize External Calls with Assembly for Memory Efficiency                                                                                                |    129    |    28380    |
| [[G-29](#g-29)] | Use Assembly for Hash Calculations                                                                                                                         |     1     |    1005     |
| [[G-30](#g-30)] | Consider Using Solady's Gas Optimized Lib for Math                                                                                                         |    96     |      0      |
| [[G-31](#g-31)] | Trade-offs Between Modifiers and Internal Functions                                                                                                        |    99     |   1039500   |
| [[G-32](#g-32)] | Optimize Boolean States with `uint256(1/2)`                                                                                                                |     7     |   119000    |
| [[G-33](#g-33)] | Consider Packing Small `uint` When it's Possible                                                                                                           |     8     |   166400    |
| [[G-34](#g-34)] | Avoid Unnecessary Public Variables                                                                                                                         |    71     |   1562000   |
| [[G-35](#g-35)] | Optimize by Using Assembly for Low-Level Calls' Return Data                                                                                                |     1     |     159     |
| [[G-36](#g-36)] | Optimize Unsigned Integer Comparison With Zero                                                                                                             |    14     |     56      |
| [[G-37](#g-37)] | Delete Unused State Variables                                                                                                                              |    27     |   540000    |
| [[G-38](#g-38)] | Optimize Gas by Using Only Named Returns                                                                                                                   |    62     |    2728     |
| [[G-39](#g-39)] | Optimize Address Storage Value Management with `assembly`                                                                                                  |    18     |      0      |
| [[G-40](#g-40)] | Use calldata instead of memory for function arguments that do not get mutated                                                                              |    13     |      0      |
| [[G-41](#g-41)] | Gas savings can be achieved by changing the model for assigning value to the structure                                                                     |     2     |     520     |


### [G-01]<a name="g-01"></a> `<array>.length` Should Not Be Looked Up In Every Loop Of A For-loop

The overheads outlined below are PER LOOP, excluding the first loop

storage arrays incur a Gwarmaccess (100 gas)
memory arrays use MLOAD (3 gas)
calldata arrays use CALLDATALOAD (3 gas)

Caching the length changes each of these to a DUP<N> (3 gas), and gets rid of the extra DUP<N> needed to store the stack offset

*There are 7 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
165	        for (uint256 i = 0; i < tokens.length; i++) {
```

*GitHub* : [165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
405	        for (uint256 i; i < users.length; ) {
...
547	        for (uint256 i; i < rewardTokens.length; ) {
...
561	        for (uint256 i; i < rewardTokens.length; ) {
...
575	        for (uint256 i; i < rewardTokens.length; ) {
...
580	            for (uint256 j; j < users.length; ) {
...
614	        for (uint256 i; i < rewardTokens.length; ) {
```

*GitHub* : [405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405), [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547), [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561), [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575), [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580), [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614)

### [G-02]<a name="g-02"></a> Setting the `constructor` to `payable`

Saves ~13 gas per instance

*There are 16 instance(s) of this issue:*


---

	 - src/blast/BlastDapp.sol

```solidity
7	    constructor() {
```

*GitHub* : [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L7)


---

	 - src/blast/BlastBox.sol

```solidity
24	    constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
```

*GitHub* : [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24)


---

	 - src/blast/BlastGovernor.sol

```solidity
15	    constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```

*GitHub* : [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15)


---

	 - src/blast/BlastMagicLP.sol

```solidity
23	    constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
```

*GitHub* : [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23)


---

	 - src/blast/BlastOnboarding.sol

```solidity
58	    constructor() Owned(msg.sender) {
...
84	    constructor(BlastTokenRegistry registry_, address feeTo_) {
```

*GitHub* : [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L58), [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L84)


---

	 - src/blast/BlastTokenRegistry.sol

```solidity
12	    constructor(address _owner) Owned(_owner) {}
```

*GitHub* : [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12)


---

	 - src/blast/BlastWrappers.sol

```solidity
20	    constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
...
29	    constructor(
30	        address implementation_,
31	        IFeeRateModel maintainerFeeRateModel_,
32	        address owner_,
33	        address governor_
34	    ) Factory(implementation_, maintainerFeeRateModel_, owner_) {
...
47	    constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
```

*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20), [29..34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L29-L34), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L47)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [112..118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L112-L118)

### [G-03]<a name="g-03"></a> `++i`/`i++` should be `unchecked{++i}`/`unchecked{i++}` when it is not possible for them to overflow, as is the case when used in `for`- and `while`-loops

The `unchecked` keyword is new in solidity version 0.8.0, so this only applies to that version or higher, which these instances are. This saves 30-40 gas [per loop](https://gist.github.com/hrkrshnn/ee8fabd532058307229d65dcd5836ddc#the-increment-in-for-loop-post-condition-can-be-made-unchecked)

*There are 1 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
165	        for (uint256 i = 0; i < tokens.length; i++) {
166	            if (!supportedTokens[tokens[i]]) {
167	                revert ErrUnsupportedToken();
168	            }
169	            if (registry.nativeYieldTokens(tokens[i])) {
170	                BlastYields.claimAllTokenYields(tokens[i], feeTo);
171	            }
172	        }
```

*GitHub* : [165..172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165-L172)

### [G-04]<a name="g-04"></a> Pre-increments and pre-decrements are cheaper than post-increments and post-decrements

*Saves 5 gas per iteration*

*There are 1 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
165	        for (uint256 i = 0; i < tokens.length; i++) {
```

*GitHub* : [165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)

### [G-05]<a name="g-05"></a> Use assembly to check for `address(0)`



*There are 29 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
25	        if (feeTo_ == address(0)) {
...
28	        if (address(registry_) == address(0)) {
...
73	        if (feeTo_ == address(0)) {
```

*GitHub* : [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L25), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L28), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L73)


---

	 - src/blast/BlastGovernor.sol

```solidity
16	        if (feeTo_ == address(0)) {
...
41	        if(_feeTo == address(0)) {
```

*GitHub* : [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L16), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L41)


---

	 - src/blast/BlastMagicLP.sol

```solidity
24	        if (feeTo_ == address(0)) {
...
27	        if (address(registry_) == address(0)) {
...
81	        if (feeTo_ == address(0)) {
```

*GitHub* : [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L24), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L27), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L81)


---

	 - src/blast/BlastOnboarding.sol

```solidity
85	        if (address(registry_) == address(0)) {
...
89	        if (feeTo_ == address(0)) {
```

*GitHub* : [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L85), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L89), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L148)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L97)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L15)


---

	 - src/blast/BlastWrappers.sol


*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L21), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L35), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L48)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L23), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L35), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L47)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L39), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L42), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L97), [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L106)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L39), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L39)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [301](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L301)

### [G-06]<a name="g-06"></a> `Internal` functions only called once can be inlined to save gas



*There are 12 instance(s) of this issue:*


---

	 - src/blast/libraries/BlastYields.sol

```solidity
42	    function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {
...
55	    function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {
```

*GitHub* : [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L42), [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L55)


---

	 - src/mimswap/MagicLP.sol

```solidity
528	    function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {
...
601	    function _afterInitialized() internal virtual {}
```

*GitHub* : [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L528), [601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L601)


---

	 - src/mimswap/libraries/DecimalMath.sol

```solidity
47	    function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```

*GitHub* : [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L47)


---

	 - src/mimswap/libraries/PMMPricing.sol

```solidity
134	    function _RBelowSellQuoteToken(
135	        PMMState memory state,
136	        uint256 payQuoteAmount
137	    )
138	        internal
139	        pure
140	        returns (
141	            uint256 // receiveBaseToken
142	        )
143	    {
...
147	    function _RBelowSellBaseToken(
148	        PMMState memory state,
149	        uint256 payBaseAmount
150	    )
151	        internal
152	        pure
153	        returns (
154	            uint256 // receiveQuoteToken
155	        )
156	    {
...
162	    function _RAboveSellBaseToken(
163	        PMMState memory state,
164	        uint256 payBaseAmount
165	    )
166	        internal
167	        pure
168	        returns (
169	            uint256 // receiveQuoteToken
170	        )
171	    {
...
175	    function _RAboveSellQuoteToken(
176	        PMMState memory state,
177	        uint256 payQuoteAmount
178	    )
179	        internal
180	        pure
181	        returns (
182	            uint256 // receiveBaseToken
183	        )
184	    {
```

*GitHub* : [134..143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L134-L143), [147..156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L147-L156), [162..171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L162-L171), [175..184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L175-L184)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol

```solidity
33	    function _getReserves() internal view virtual returns (uint256, uint256) {
```

*GitHub* : [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L33)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L544), [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L572)

### [G-07]<a name="g-07"></a> Usage of `uint`/`int` smaller than 32 bytes (256 bits) incurs overhead

When using elements that are smaller than 32 bytes, your contract’s gas usage may be higher. This is because the EVM operates on 32 bytes at a time. Therefore, if the element is smaller than that, the EVM must use more operations in order to reduce the size of the element from 32 bytes to the desired size.

Each operation involving a uint8 costs an extra 22-28 gas (depending on whether the other operand is also a variable of type uint8) as compared to ones involving uint256, due to the compiler having to clear the higher bits of the memory word before operating on the uint8, as well as the associated stack operations of doing so. Use a larger size then downcast where needed.

https://docs.soliditylang.org/en/v0.8.11/internals/layout_in_storage.html

Use a larger size then downcast where needed.

*There are 15 instance(s) of this issue:*


---

	 - src/mimswap/MagicLP.sol

```solidity
72	    uint112 public _BASE_RESERVE_;
...
73	    uint112 public _QUOTE_RESERVE_;
...
74	    uint32 public _BLOCK_TIMESTAMP_LAST_;
...
76	    uint112 public _BASE_TARGET_;
...
77	    uint112 public _QUOTE_TARGET_;
...
78	    uint32 public _RState_;
...
163	    function decimals() public view override returns (uint8) {
...
546	        uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
...
547	        uint32 timeElapsed = blockTimestamp - _BLOCK_TIMESTAMP_LAST_;
```

*GitHub* : [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L78), [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163), [546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L546), [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L547)


---

	 - src/mimswap/periphery/Router.sol

```solidity
598	    function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {
```

*GitHub* : [598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L598), [598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L598)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L29), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L48), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L48)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L55)

### [G-08]<a name="g-08"></a> Functions guaranteed to revert when called by normal users can be marked `payable`

If a function modifier such as `onlyOwner` is used, the function will revert if a normal user tries to pay the function. Marking the function as `payable` will lower the gas cost for legitimate callers because the compiler will not include checks for whether a payment was provided. The extra opcodes avoided are `CALLVALUE`(2),`DUP1`(3),`ISZERO`(3),`PUSH2`(3),`JUMPI`(10),`PUSH1`(3),`DUP1`(3),`REVERT`(0),`JUMPDEST`(1),`POP`(2), which costs an average of about 21 gas per call to the function, in addition to the extra deployment cost


*There are 40 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
68	    function callBlastPrecompile(bytes calldata data) external onlyOwner {
...
72	    function setFeeTo(address feeTo_) external onlyOwner {
...
81	    function setTokenEnabled(address token, bool enabled) external onlyOwner {
```

*GitHub* : [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L68), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81)


---

	 - src/blast/BlastGovernor.sol

```solidity
40	    function setFeeTo(address _feeTo) external onlyOwner {
...
49	    function callBlastPrecompile(bytes calldata data) external onlyOwner {
...
53	    function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

*GitHub* : [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40), [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L49), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)


---

	 - src/blast/BlastMagicLP.sol

```solidity
72	    function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {
...
80	    function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
...
89	    function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```

*GitHub* : [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L72), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89)


---

	 - src/blast/BlastOnboarding.sol

```solidity
147	    function setFeeTo(address feeTo_) external onlyOwner {
```

*GitHub* : [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L156), [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L160), [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190), [195](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L195), [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L200), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L205), [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L214), [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L218)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96), [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129), [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L461), [470..479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470-L479), [504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L504)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105), [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L116), [120..126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L120-L126)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300), [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317), [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L324), [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337), [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L341)

### [G-09]<a name="g-09"></a> `>=` costs less gas than `>`

The compiler uses opcodes `GT` and `ISZERO` for solidity code that uses `>`, but only requires LT for `>=`, which saves 3 gas. Similarly for `<=`.

*There are 16 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
114	        if (caps[token] > 0 && totals[token].total > caps[token]) {
```

*GitHub* : [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114)


---

	 - src/mimswap/MagicLP.sol

```solidity
294	        if (data.length > 0) {
...
395	        } else if (baseReserve > 0 && quoteReserve > 0) {
...
395	        } else if (baseReserve > 0 && quoteReserve > 0) {
...
450	        if (data.length > 0) {
...
549	        if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
...
582	        if (amount > 0) {
...
588	        if (amount > 0) {
```

*GitHub* : [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L294), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395), [450](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L450), [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549), [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L582), [588](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L588)


---

	 - src/mimswap/libraries/Math.sol

```solidity
22	        if (remainder > 0) {
```

*GitHub* : [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L22)


---

	 - src/mimswap/periphery/Router.sol

```solidity
147	        } else if (baseReserve > 0 && quoteReserve > 0) {
```

*GitHub* : [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147), [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527), [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527), [590](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L590)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [417](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L417), [636](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L636)

### [G-10]<a name="g-10"></a> Multiple mappings can be replaced with a single struct mapping

Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (20000 gas) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot.

*There are 13 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
36	    mapping(address token => bool) public supportedTokens;
...
37	    mapping(address token => Balances) public totals;
...
38	    mapping(address token => uint256 cap) public caps;
...
41	    mapping(address user => mapping(address token => Balances)) public balances;
```

*GitHub* : [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L37), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L38), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L41)


---

	 - src/mimswap/periphery/Factory.sol

```solidity
35	    mapping(address base => mapping(address quote => address[] pools)) public pools;
...
36	    mapping(address creator => address[] pools) public userPools;
```

*GitHub* : [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L35), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L36)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
89	    mapping(address token => Reward info) private _rewardData;
...
90	    mapping(address user => Balances balances) private _balances;
...
91	    mapping(address user => LockedBalance[] locks) private _userLocks;
...
92	    mapping(address user => RewardLock rewardLock) private _userRewardLock;
```

*GitHub* : [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L89), [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L90), [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L91), [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L92), [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L94), [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L95), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L96)

### [G-11]<a name="g-11"></a> State variables should be cached in stack variables rather than re-reading them from storage

The instances below point to the second+ access of a state variable within a function. Caching of a state variable replaces each Gwarmaccess (**100 gas**) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.

*There are 186 instance(s) of this issue:*


---

	 - src/blast/BlastMagicLP.sol

```solidity
// @audit State variable `_BASE_TOKEN_` called 2 times in one function
56	        if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
...
// @audit State variable `_BASE_TOKEN_` called 2 times in one function
57	            token0Amount = BlastYields.claimAllTokenYields(_BASE_TOKEN_, feeTo_);
...
// @audit State variable `_QUOTE_TOKEN_` called 2 times in one function
59	        if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
...
// @audit State variable `_QUOTE_TOKEN_` called 2 times in one function
60	            token1Amount = BlastYields.claimAllTokenYields(_QUOTE_TOKEN_, feeTo_);
...
// @audit State variable `nativeYieldTokens` called 2 times in one function
56	        if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
...
// @audit State variable `nativeYieldTokens` called 2 times in one function
59	        if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
```

*GitHub* : [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L56), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L57), [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L59), [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L60), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L56), [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L59)


---

	 - src/blast/BlastMagicLP.sol

```solidity
// @audit State variable `_BASE_TOKEN_` called 2 times in one function
105	        if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
...
// @audit State variable `_BASE_TOKEN_` called 2 times in one function
106	            BlastYields.enableTokenClaimable(_BASE_TOKEN_);
...
// @audit State variable `_QUOTE_TOKEN_` called 2 times in one function
109	        if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
...
// @audit State variable `_QUOTE_TOKEN_` called 2 times in one function
110	            BlastYields.enableTokenClaimable(_QUOTE_TOKEN_);
```

*GitHub* : [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L105), [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L106), [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L109), [110](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L110), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L105), [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L109)


---

	 - src/blast/BlastOnboarding.sol


*GitHub* : [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L106), [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L109), [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L118), [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114), [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L105), [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L108), [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L112), [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114)


---

	 - src/blast/BlastOnboarding.sol


*GitHub* : [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L124), [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L125), [126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L126), [127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L127)


---

	 - src/blast/BlastOnboarding.sol


*GitHub* : [133](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L133), [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L134), [135](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L135), [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L136)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L59), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L68)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L87), [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L88)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L97), [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106), [117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117), [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L122), [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124), [126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L126), [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L103), [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L104), [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106), [117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117), [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L118), [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L119), [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L122), [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124), [126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L126), [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106), [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L108), [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L122), [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124), [126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L126), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L101), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L102)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [130](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L130), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L131)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L147), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L162), [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L162), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L156), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L156)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L99), [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L118)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139), [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L141), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L146), [139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139), [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L141), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L146), [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L142), [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L147), [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L142), [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L147), [139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139), [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L140), [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144), [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L145)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [245](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L245), [264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L264), [262](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L262), [264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L264), [256](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L256), [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L258)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [285](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L285), [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L287), [268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L268), [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L287), [279](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L279), [281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L281)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [302](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302), [308](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L308), [315](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L315), [331](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L331), [298](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L298), [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L325), [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L347), [319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L319), [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L341), [302](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302), [309](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L309), [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L330), [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L337), [299](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L299), [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L325), [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L347), [320](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L320), [322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L322), [342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L342), [344](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L344)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [382](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L382), [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402), [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402), [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402), [381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L381), [381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L381), [383](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L383), [383](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L383), [385](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L385), [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403), [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403), [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438), [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438), [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438), [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439), [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439), [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [512](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L512), [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513), [514](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L514), [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513), [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513), [516](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L516), [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517), [518](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L518), [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517), [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L547), [557](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L557)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [571](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L571), [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L572), [574](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L574), [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L575)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L35), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L39)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L86), [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [279](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L279), [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L282), [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283), [285](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L285)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [305](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L305), [314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L314), [309](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L309), [313](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L313)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [318](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L318), [319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L319)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [362](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L362), [369](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L369)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [417](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L417), [430](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L430), [431](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L431)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L483), [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L490), [501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L501), [510](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L510), [482](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L482), [502](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L502)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L532), [533](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L533)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547), [548](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L548)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561), [562](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L562)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575), [576](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L576)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L598), [648](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L648), [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614), [615](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L615), [616](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L616), [619](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L619)

### [G-12]<a name="g-12"></a> Stack variable used as a cheaper cache for a state variable is only used once

If the variable is only accessed once, it's cheaper to use the state variable directly that one time, and save the 3 gas the extra stack assignment would spend

*There are 24 instance(s) of this issue:*


---

	 - src/blast/BlastMagicLP.sol

```solidity
47	    function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {
```

*GitHub* : [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L47)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
86	    function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
96	    function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
...
155	    function _claimable(address user) internal view returns (uint256 shares) {
```

*GitHub* : [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L155)


---

	 - src/mimswap/MagicLP.sol

```solidity
167	    function querySellBase(
168	        address trader,
169	        uint256 payBaseAmount
170	    ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {
...
180	    function querySellQuote(
181	        address trader,
182	        uint256 payQuoteAmount
183	    ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {
...
290	    function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
...
413	    function sellShares(
414	        uint256 shareAmount,
415	        address to,
416	        uint256 baseMinAmount,
417	        uint256 quoteMinAmount,
418	        bytes calldata data,
419	        uint256 deadline
420	    ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {
...
470	    function setParameters(
471	        address assetTo,
472	        uint256 newLpFeeRate,
473	        uint256 newI,
474	        uint256 newK,
475	        uint256 baseOutAmount,
476	        uint256 quoteOutAmount,
477	        uint256 minBaseReserve,
478	        uint256 minQuoteReserve
479	    ) public nonReentrant onlyImplementationOwner {
```

*GitHub* : [167..170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L167-L170), [180..183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L180-L183), [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290), [413..420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L413-L420), [470..479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470-L479)


---

	 - src/mimswap/libraries/Math.sol

```solidity
19	    function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {
```

*GitHub* : [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L19), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L79), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L251), [509..513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L509-L513)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L37)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277), [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L292), [479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L479), [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L544), [557](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L557), [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L572), [597](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L597)

### [G-13]<a name="g-13"></a> State Variables can be packed into fewer storage slots

Each slot saved can avoid an extra Gsset (21000 gas). Subsequent reads as well as writes have smaller gas savings

*There are 1 instance(s) of this issue:*


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
23	contract BlastOnboardingBootDataV1 is BlastOnboardingData {
24	    address public pool;
```

*GitHub* : [23..24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23-L24)

### [G-14]<a name="g-14"></a> State variables access within a loop

State variable reads and writes are more expensive than local variable reads and writes. Therefore, it is recommended to replace state variable reads and writes within loops with a local variable. Gas savings should be multiplied by the average loop length.

*There are 6 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
165	        for (uint256 i = 0; i < tokens.length; i++) {
166	            if (!supportedTokens[tokens[i]]) {
167	                revert ErrUnsupportedToken();
168	            }
169	            if (registry.nativeYieldTokens(tokens[i])) {
170	                BlastYields.claimAllTokenYields(tokens[i], feeTo);
171	            }
172	        }
```

*GitHub* : [165..172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165-L172)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
405	        for (uint256 i; i < users.length; ) {
406	            address user = users[i];
407	            Balances storage bal = _balances[user];
408	            LockedBalance[] storage locks = _userLocks[user];
409	
410	            if (locks.length == 0) {
411	                revert ErrNoLocks();
412	            }
413	
414	            uint256 index = lockIndexes[i];
415	
416	            // Prevents processing `lastLockIndex` out of order
417	            if (index == lastLockIndex[user] && locks.length > 1) {
418	                revert ErrInvalidLockIndex();
419	            }
420	
421	            // prohibit releasing non-expired locks
422	            if (locks[index].unlockTime > block.timestamp) {
423	                revert ErrLockNotExpired();
424	            }
425	
426	            uint256 amount = locks[index].amount;
427	            uint256 lastIndex = locks.length - 1;
428	
429	            /// Last lock index changed place with the one we just swapped.
430	            if (lastLockIndex[user] == lastIndex) {
431	                lastLockIndex[user] = index;
432	            }
433	
434	            if (index != lastIndex) {
435	                locks[index] = locks[lastIndex];
436	                emit LogLockIndexChanged(user, lastIndex, index);
437	            }
438	
439	            locks.pop();
440	
441	            unlockedSupply += amount;
442	            lockedSupply -= amount;
443	
444	            bal.unlocked += amount;
445	            bal.locked -= amount;
446	
447	            emit LogUnlocked(user, amount, index);
448	
449	            unchecked {
450	                ++i;
451	            }
452	        }
...
547	        for (uint256 i; i < rewardTokens.length; ) {
548	            _updateRewardsGlobal(rewardTokens[i], totalSupply_);
549	            unchecked {
550	                ++i;
551	            }
552	        }
...
561	        for (uint256 i; i < rewardTokens.length; ) {
562	            address token = rewardTokens[i];
563	            _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_));
564	
565	            unchecked {
566	                ++i;
567	            }
568	        }
...
575	        for (uint256 i; i < rewardTokens.length; ) {
576	            address token = rewardTokens[i];
577	            uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);
578	
579	            // Record each user's rewards
580	            for (uint256 j; j < users.length; ) {
581	                address user = users[j];
582	                _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);
583	
584	                unchecked {
585	                    ++j;
586	                }
587	            }
588	
589	            unchecked {
590	                ++i;
591	            }
592	        }
...
614	        for (uint256 i; i < rewardTokens.length; ) {
615	            address rewardToken = rewardTokens[i];
616	            uint256 rewardAmount = rewards[user][rewardToken];
617	
618	            // in all scenario, reset the reward amount immediately
619	            rewards[user][rewardToken] = 0;
620	
621	            // don't assume the rewardTokens array is always the same length as the items array
622	            // as new reward tokens can be added by the owner
623	            if (i < rewardItemLength) {
624	                RewardLockItem storage item = _rewardLock.items[i];
625	
626	                // expired lock, claim existing unlocked rewards if any
627	                if (expired) {
628	                    uint256 amount = item.amount;
629	
630	                    // since this current lock is expired and that item index
631	                    // matches the reward index, override the current amount
632	                    // with the new locked amount.
633	                    item.amount = rewardAmount;
634	
635	                    // use cached amount
636	                    if (amount > 0) {
637	                        rewardToken.safeTransfer(user, amount);
638	                        emit LogRewardPaid(user, rewardToken, amount);
639	                    }
640	                } else {
641	                    // not expired, just add to the existing lock
642	                    item.amount += rewardAmount;
643	                }
644	            }
645	            // new reward token, create a new lock item
646	            // could mean it's adding to an existing lock or creating a new one
647	            else {
648	                _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
649	            }
650	
651	            emit LogRewardLocked(user, rewardToken, rewardAmount);
652	
653	            unchecked {
654	                ++i;
655	            }
656	        }
```

*GitHub* : [405..452](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405-L452), [547..552](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547-L552), [561..568](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561-L568), [575..592](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575-L592), [614..656](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614-L656)

### [G-15]<a name="g-15"></a> Using `private` for constants saves gas

Saves deployment gas due to the compiler not having to create non-payable getter functions for deployment calldata, not having to store the bytes of the value outside of where it's used, and not adding another entry to the method ID table.

*There are 18 instance(s) of this issue:*


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
13	address constant USDB = 0x4300000000000000000000000000000000000003;
...
14	address constant MIM = 0x76DA31D7C9CbEAE102aff34D3398bC450c8374c1;
...
15	uint256 constant FEE_RATE = 0.0005 ether; // 0.05%
...
16	uint256 constant K = 0.00025 ether; // 0.00025, 1.25% price fluctuation, similar to A2000 in curve
...
17	uint256 constant I = 0.998 ether; // 1 MIM = 0.998 USDB
...
18	uint256 constant USDB_TO_MIN = 1.002 ether; // 1 USDB = 1.002 MIM
...
19	uint256 constant MIM_TO_MIN = I;
```

*GitHub* : [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L13), [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L14), [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L15), [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L16), [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L17), [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L18), [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L19)


---

	 - src/blast/libraries/BlastPoints.sol

```solidity
7	    address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;
...
8	    IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);
```

*GitHub* : [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L7), [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L8)


---

	 - src/blast/libraries/BlastYields.sol

```solidity
14	    IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);
```

*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L14)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64), [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L65), [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L66)


---

	 - src/mimswap/libraries/DecimalMath.sol


*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L21)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L31)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L16)

### [G-16]<a name="g-16"></a> Using `bool` for storage incurs overhead

Use `uint256(1)` and `uint256(2)` for `true`/`false` to avoid a Gwarmaccess (100 gas), and to avoid Gsset (20000 gas) when changing from `false` to `true`, after having been `true` in the past. See [source](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27).

*There are 7 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
21	    mapping(address => bool) public enabledTokens;
```

*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21)


---

	 - src/blast/BlastMagicLP.sol

```solidity
21	    mapping(address => bool) public operators;
```

*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L21)


---

	 - src/blast/BlastOnboarding.sol

```solidity
36	    mapping(address token => bool) public supportedTokens;
```

*GitHub* : [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
28	    bool public ready;
...
30	    mapping(address user => bool claimed) public claimed;
```

*GitHub* : [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L28), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L30)


---

	 - src/blast/BlastTokenRegistry.sol

```solidity
10	    mapping(address => bool) public nativeYieldTokens;
```

*GitHub* : [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10)


---

	 - src/mimswap/MagicLP.sol

```solidity
68	    bool internal _INITIALIZED_;
```

*GitHub* : [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L68)

### [G-17]<a name="g-17"></a> State variables only set in the constructor should be declared `immutable`

Accessing state variables within a function involves an SLOAD operation, but `immutable` variables can be accessed directly without the need of it, thus reducing gas costs. As these state variables are assigned only in the constructor, consider declaring them `immutable`.

*There are 1 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
33	    BlastTokenRegistry public registry;
```

*GitHub* : [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L33)

### [G-18]<a name="g-18"></a> Consider activating `via-ir` for deploying

The IR-based code generator was developed to make code generation more performant by enabling optimization passes that can be applied across functions.

It is possible to activate the IR-based code generator through the command line by using the flag `--via-ir` or by including the option `{"viaIR": true}`.

Keep in mind that compiling with this option may take longer. However, you can simply test it before deploying your code. If you find that it provides better performance, you can add the `--via-ir` flag to your deploy command.

*There are 1 instance(s) of this issue:*

*GitHub* : [project\2024-03-abracadabra-money](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/#L0)

### [G-19]<a name="g-19"></a> Function calls should be cached instead of re-calling the function

Consider caching the result instead of re-calling the function when possible. Note: this also includes casts, which cost between 42-46 gas, depending on the type.

*There are 14 instance(s) of this issue:*


---

	 - src/mimswap/MagicLP.sol

```solidity
290	    function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
...
360	    function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
...
413	    function sellShares(
414	        uint256 shareAmount,
415	        address to,
416	        uint256 baseMinAmount,
417	        uint256 quoteMinAmount,
418	        bytes calldata data,
419	        uint256 deadline
420	    ) external nonReentrant returns (uint256 baseAmount, uint256 quoteAmount) {
```

*GitHub* : [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290), [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360), [413..420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L413-L420)


---

	 - src/mimswap/libraries/Math.sol

```solidity
131	    function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```

*GitHub* : [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)


---

	 - src/mimswap/libraries/PMMPricing.sol

```solidity
203	    function getMidPrice(PMMState memory state) internal pure returns (uint256) {
```

*GitHub* : [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L203)


---

	 - src/mimswap/periphery/Router.sol

```solidity
73	    function createPoolETH(
74	        address token,
75	        bool useTokenAsQuote,
76	        uint256 lpFeeRate,
77	        uint256 i,
78	        uint256 k,
79	        address to,
80	        uint256 tokenInAmount
81	    ) external payable returns (address clone, uint256 shares) {
...
112	    function previewAddLiquidity(
113	        address lp,
114	        uint256 baseInAmount,
115	        uint256 quoteInAmount
116	    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
192	    function addLiquidityETH(
193	        address lp,
194	        address to,
195	        address payable refundTo,
196	        uint256 tokenInAmount,
197	        uint256 minimumShares,
198	        uint256 deadline
199	    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
229	    function addLiquidityETHUnsafe(
230	        address lp,
231	        address to,
232	        uint256 tokenInAmount,
233	        uint256 minimumShares,
234	        uint256 deadline
235	    ) external payable ensureDeadline(deadline) returns (uint256 shares) {
...
251	    function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
```

*GitHub* : [73..81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L73-L81), [112..116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L112-L116), [192..199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192-L199), [229..235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229-L235), [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L251), [274..281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L274-L281), [314..321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L314-L321), [365..372](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L365-L372), [509..513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L509-L513)

### [G-20]<a name="g-20"></a> Add `unchecked` blocks for divisions where the operands cannot overflow

`uint` divisions can't overflow, while `int` divisions can overflow only in [one specific case](https://docs.soliditylang.org/en/latest/types.html#division).

Consider adding an `unchecked` block to have some [gas savings](https://gist.github.com/DadeKuma/3bc597338ae774b8b3bd43280d55271f).

*There are 40 instance(s) of this issue:*


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
163	        return (userLocked * totalPoolShares) / totalLocked;
```

*GitHub* : [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L163)


---

	 - src/mimswap/MagicLP.sol

```solidity
435	        baseAmount = (baseBalance * shareAmount) / totalShares;
...
436	        quoteAmount = (quoteBalance * shareAmount) / totalShares;
...
513	            _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
...
517	            _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
```

*GitHub* : [435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L435), [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L436), [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513), [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517)


---

	 - src/mimswap/libraries/DecimalMath.sol

```solidity
24	        return (target * d) / ONE;
...
32	        return (target * ONE) / d;
...
40	        return ONE2 / target;
...
53	            uint p = powFloor(target, e / 2);
...
54	            p = (p * p) / ONE;
```

*GitHub* : [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L24), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L32), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L40), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L53), [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L54), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L56)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L20), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L30), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34), [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L59), [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L96), [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L99), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L97), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L155), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L156), [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L160), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170), [181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L181)


---

	 - src/mimswap/libraries/PMMPricing.sol


*GitHub* : [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L257), [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L258)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L144), [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L236), [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L241), [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L258), [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283), [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294), [388](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L388)

### [G-21]<a name="g-21"></a> Multiplication/division by two should use bit shifting

`X * 2` is equivalent to `X << 1` and `X / 2` is the same as `X >> 1`.

The `MUL` and `DIV` opcodes cost 5 gas, whereas `SHL` and `SHR` only cost 3 gas.

*There are 7 instance(s) of this issue:*


---

	 - src/mimswap/libraries/DecimalMath.sol

```solidity
53	            uint p = powFloor(target, e / 2);
```

*GitHub* : [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L53)


---

	 - src/mimswap/libraries/Math.sol

```solidity
30	        uint256 z = x / 2 + 1;
...
34	            z = (x / z + z) / 2;
...
93	        uint256 ki = (4 * k) * i;
...
101	        uint256 premium = DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2) + DecimalMath.ONE;
...
184	        uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
...
188	        uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
```

*GitHub* : [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L30), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34), [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L93), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L101), [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184), [188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L188)

### [G-22]<a name="g-22"></a> Consider using `bytes32` rather than a `string`

Using the `bytes` types for fixed-length strings is more efficient than having the EVM have to incur the overhead of string processing. Consider whether the value _needs_ to be a `string`. A good reason to keep it as a `string` would be if the variable is defined in an interface that this project does not own.

*There are 4 instance(s) of this issue:*


---

	 - src/blast/BlastMagicLP.sol

```solidity
39	    function version() external pure override returns (string memory) {
```

*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L39)


---

	 - src/mimswap/MagicLP.sol

```solidity
155	    function name() public view override returns (string memory) {
...
159	    function symbol() public pure override returns (string memory) {
...
236	    function version() external pure virtual returns (string memory) {
```

*GitHub* : [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155), [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L159), [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L236)

### [G-23]<a name="g-23"></a> Optimize Zero Checks Using Assembly

The usage of inline assembly to check if variable is the zero can save gas compared to traditional `require` or `if` statement checks. 

The assembly check uses the `extcodesize` operation which is generally cheaper in terms of gas.

[More information can be found here.](https://medium.com/@kalexotsu/solidity-assembly-checking-if-an-address-is-0-efficiently-d2bfe071331)

*There are 84 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
25	        if (feeTo_ == address(0)) {
...
28	        if (address(registry_) == address(0)) {
...
73	        if (feeTo_ == address(0)) {
```

*GitHub* : [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L25), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L28), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L73)


---

	 - src/blast/BlastGovernor.sol

```solidity
16	        if (feeTo_ == address(0)) {
...
41	        if(_feeTo == address(0)) {
```

*GitHub* : [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L16), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L41)


---

	 - src/blast/BlastMagicLP.sol

```solidity
24	        if (feeTo_ == address(0)) {
...
27	        if (address(registry_) == address(0)) {
...
81	        if (feeTo_ == address(0)) {
```

*GitHub* : [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L24), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L27), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L81)


---

	 - src/blast/BlastOnboarding.sol

```solidity
85	        if (address(registry_) == address(0)) {
...
89	        if (feeTo_ == address(0)) {
```

*GitHub* : [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L85), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L89), [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L148)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L64), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L97), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L158)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L15)


---

	 - src/blast/BlastWrappers.sol


*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L21), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L35), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L48)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102), [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L108), [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L294), [369](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L369), [375](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L375), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395), [377](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L377), [385](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L385), [450](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L450), [483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L483), [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549), [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549), [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549), [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L582), [588](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L588)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L23), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L35), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L47)


---

	 - src/mimswap/libraries/DecimalMath.sol


*GitHub* : [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L48)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L22), [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L52), [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L58), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L80), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L89), [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L94), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L132), [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L136), [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L140), [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L153), [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L192)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L39), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L42), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L97), [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L106)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L39), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L39), [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L125), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L131), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L132), [327](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L327), [348](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L348), [379](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L379), [392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L392), [521](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L521), [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527), [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527), [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L545), [560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L560), [593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L593), [599](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L599), [599](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L599)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L131), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L156), [171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L171), [278](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L278), [301](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L301), [410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L410), [459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L459), [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L490), [636](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L636)

### [G-24]<a name="g-24"></a> Consider using `assembly` to write address storage values if the address variable is mutable

Writing address storage values using `assembly` can be more gas efficient when the address variable is mutable.
The following instances show mutable address storage variables that could be optimized using `assembly`.

*There are 26 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
33	        feeTo = feeTo_;
...
77	        feeTo = feeTo_;
```

*GitHub* : [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L33), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L77)


---

	 - src/blast/BlastGovernor.sol

```solidity
20	        feeTo = feeTo_;
...
45	        feeTo = _feeTo;
```

*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L20), [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L45)


---

	 - src/blast/BlastMagicLP.sol

```solidity
32	        feeTo = feeTo_;
...
85	        feeTo = feeTo_;
```

*GitHub* : [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L32), [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L85)


---

	 - src/blast/BlastOnboarding.sol

```solidity
94	        feeTo = feeTo_;
...
152	        feeTo = feeTo_;
...
191	        bootstrapper = bootstrapper_;
```

*GitHub* : [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L94), [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L152), [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L191)


---

	 - src/mimswap/MagicLP.sol

```solidity
119	        _BASE_TOKEN_ = baseTokenAddress;
```

*GitHub* : [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L119), [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L120)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L27), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L51), [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L58)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L45), [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L85), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L101)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L66), [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L88), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L204), [238](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L238), [286](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L286), [351](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L351), [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L349), [382](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L382), [380](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L380)

### [G-25]<a name="g-25"></a> Consider Caching Multiple Accesses to Mappings/Arrays

Leveraging a local variable to cache these values when accessed more than once can yield a gas saving of approximately 42 units per access. This reduction is attributed to eliminating the need for recalculating the key's keccak256 hash (which costs Gkeccak256 - 30 gas) and the associated stack operations. For arrays, this also prevents the overhead of re-computing offsets in memory or calldata.

*There are 22 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
101	    function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
...
123	    function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
...
132	    function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
```

*GitHub* : [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101), [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
55	    function claim(bool lock) external returns (uint256 shares) {
...
86	    function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
96	    function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
...
155	    function _claimable(address user) internal view returns (uint256 shares) {
```

*GitHub* : [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L55), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L155)


---

	 - src/mimswap/periphery/Factory.sol

```solidity
53	    function getPoolCount(address token0, address token1) external view returns (uint256) {
...
120	    function removePool(
121	        address creator,
122	        address baseToken,
123	        address quoteToken,
124	        uint256 poolIndex,
125	        uint256 userPoolIndex
126	    ) external onlyOwner {
...
148	    function _addPool(address creator, address baseToken, address quoteToken, address pool) internal {
```

*GitHub* : [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L53), [120..126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L120-L126), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L148)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277), [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L292), [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300), [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361), [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397), [479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L479), [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L528), [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L536), [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L544), [557](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L557), [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L572), [597](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L597)

### [G-26]<a name="g-26"></a> Optimize Gas by Using Do-While Loops

Using `do-while` loops instead of `for` loops can be more gas-efficient. 
Even if you add an `if` condition to account for the case where the loop doesn't execute at all, a `do-while` loop can still be cheaper in terms of gas.

*There are 9 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
165	        for (uint256 i = 0; i < tokens.length; i++) {
166	            if (!supportedTokens[tokens[i]]) {
167	                revert ErrUnsupportedToken();
168	            }
169	            if (registry.nativeYieldTokens(tokens[i])) {
170	                BlastYields.claimAllTokenYields(tokens[i], feeTo);
171	            }
172	        }
```

*GitHub* : [165..172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165-L172)


---

	 - src/mimswap/libraries/Math.sol

```solidity
32	        while (z < y) {
33	            y = z;
34	            z = (x / z + z) / 2;
35	        }
```

*GitHub* : [32..35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L32-L35)


---

	 - src/mimswap/periphery/Router.sol

```solidity
544	        for (uint256 i = 0; i < iterations; ) {
545	            if (directions & 1 == 0) {
546	                // Sell base
547	                IMagicLP(path[i]).sellBase(address(path[i + 1]));
548	            } else {
549	                // Sell quote
550	                IMagicLP(path[i]).sellQuote(address(path[i + 1]));
551	            }
552	
553	            directions >>= 1;
554	
555	            unchecked {
556	                ++i;
557	            }
558	        }
```

*GitHub* : [544..558](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544-L558)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
405	        for (uint256 i; i < users.length; ) {
406	            address user = users[i];
407	            Balances storage bal = _balances[user];
408	            LockedBalance[] storage locks = _userLocks[user];
409	
410	            if (locks.length == 0) {
411	                revert ErrNoLocks();
412	            }
413	
414	            uint256 index = lockIndexes[i];
415	
416	            // Prevents processing `lastLockIndex` out of order
417	            if (index == lastLockIndex[user] && locks.length > 1) {
418	                revert ErrInvalidLockIndex();
419	            }
420	
421	            // prohibit releasing non-expired locks
422	            if (locks[index].unlockTime > block.timestamp) {
423	                revert ErrLockNotExpired();
424	            }
425	
426	            uint256 amount = locks[index].amount;
427	            uint256 lastIndex = locks.length - 1;
428	
429	            /// Last lock index changed place with the one we just swapped.
430	            if (lastLockIndex[user] == lastIndex) {
431	                lastLockIndex[user] = index;
432	            }
433	
434	            if (index != lastIndex) {
435	                locks[index] = locks[lastIndex];
436	                emit LogLockIndexChanged(user, lastIndex, index);
437	            }
438	
439	            locks.pop();
440	
441	            unlockedSupply += amount;
442	            lockedSupply -= amount;
443	
444	            bal.unlocked += amount;
445	            bal.locked -= amount;
446	
447	            emit LogUnlocked(user, amount, index);
448	
449	            unchecked {
450	                ++i;
451	            }
452	        }
...
547	        for (uint256 i; i < rewardTokens.length; ) {
548	            _updateRewardsGlobal(rewardTokens[i], totalSupply_);
549	            unchecked {
550	                ++i;
551	            }
552	        }
...
561	        for (uint256 i; i < rewardTokens.length; ) {
562	            address token = rewardTokens[i];
563	            _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_));
564	
565	            unchecked {
566	                ++i;
567	            }
568	        }
...
575	        for (uint256 i; i < rewardTokens.length; ) {
576	            address token = rewardTokens[i];
577	            uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);
578	
579	            // Record each user's rewards
580	            for (uint256 j; j < users.length; ) {
581	                address user = users[j];
582	                _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);
583	
584	                unchecked {
585	                    ++j;
586	                }
587	            }
588	
589	            unchecked {
590	                ++i;
591	            }
592	        }
...
580	            for (uint256 j; j < users.length; ) {
581	                address user = users[j];
582	                _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);
583	
584	                unchecked {
585	                    ++j;
586	                }
587	            }
...
614	        for (uint256 i; i < rewardTokens.length; ) {
615	            address rewardToken = rewardTokens[i];
616	            uint256 rewardAmount = rewards[user][rewardToken];
617	
618	            // in all scenario, reset the reward amount immediately
619	            rewards[user][rewardToken] = 0;
620	
621	            // don't assume the rewardTokens array is always the same length as the items array
622	            // as new reward tokens can be added by the owner
623	            if (i < rewardItemLength) {
624	                RewardLockItem storage item = _rewardLock.items[i];
625	
626	                // expired lock, claim existing unlocked rewards if any
627	                if (expired) {
628	                    uint256 amount = item.amount;
629	
630	                    // since this current lock is expired and that item index
631	                    // matches the reward index, override the current amount
632	                    // with the new locked amount.
633	                    item.amount = rewardAmount;
634	
635	                    // use cached amount
636	                    if (amount > 0) {
637	                        rewardToken.safeTransfer(user, amount);
638	                        emit LogRewardPaid(user, rewardToken, amount);
639	                    }
640	                } else {
641	                    // not expired, just add to the existing lock
642	                    item.amount += rewardAmount;
643	                }
644	            }
645	            // new reward token, create a new lock item
646	            // could mean it's adding to an existing lock or creating a new one
647	            else {
648	                _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
649	            }
650	
651	            emit LogRewardLocked(user, rewardToken, rewardAmount);
652	
653	            unchecked {
654	                ++i;
655	            }
656	        }
```

*GitHub* : [405..452](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405-L452), [547..552](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547-L552), [561..568](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561-L568), [575..592](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575-L592), [580..587](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580-L587), [614..656](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614-L656)

### [G-27]<a name="g-27"></a> Use Assembly for Efficient Event Emission

To efficiently emit events, consider utilizing assembly by making use of scratch space and the free memory pointer.
This approach can potentially avoid the costs associated with memory expansion.

However, it's crucial to cache and restore the free memory pointer for safe optimization.
Good examples of such practices can be found in well-optimized [Solady's codebases](https://github.com/Vectorized/solady/blob/main/src/tokens/ERC1155.sol#L167).
Please review your code and consider the potential gas savings of this approach.

*There are 59 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
78	        emit LogFeeToChanged(feeTo_);
...
90	        emit LogTokenDepositEnabled(token, enabled);
```

*GitHub* : [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L78), [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L90)


---

	 - src/blast/BlastGovernor.sol

```solidity
46	        emit LogFeeToChanged(_feeTo);
```

*GitHub* : [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L46)


---

	 - src/blast/BlastMagicLP.sol

```solidity
86	        emit LogFeeToChanged(feeTo_);
...
91	        emit LogOperatorChanged(operator, status);
```

*GitHub* : [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L86), [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L91)


---

	 - src/blast/BlastOnboarding.sol

```solidity
120	        emit LogDeposit(msg.sender, token, amount, lock_);
...
129	        emit LogLock(msg.sender, token, amount);
...
140	        emit LogWithdraw(msg.sender, token, amount);
...
153	        emit LogFeeToChanged(feeTo_);
...
182	        emit LogTokenSupported(token, supported);
```

*GitHub* : [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L120), [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L129), [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L140), [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L153), [182](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L182), [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L187), [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L192), [197](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L197), [202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L202), [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L211)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L71), [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L132), [143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L143), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L20)


---

	 - src/blast/libraries/BlastYields.sol


*GitHub* : [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L26), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L31), [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L44), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L57), [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L62), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L72), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L77)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [259](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L259), [264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L264), [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L282), [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L287), [323](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L323), [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L325), [345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L345), [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L347), [352](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L352), [409](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L409), [454](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L454), [467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L467), [501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L501)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L52), [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L59)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L102), [111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L111), [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L141), [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L152)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L183), [318](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L318), [331](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L331), [392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L392), [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L436), [447](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L447), [475](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L475), [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L513), [611](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L611), [638](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L638), [651](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L651)

### [G-28]<a name="g-28"></a> Optimize External Calls with Assembly for Memory Efficiency

Using interfaces to make external contract calls in Solidity is convenient but can be inefficient in terms of memory utilization.
Each such call involves creating a new memory location to store the data being passed, thus incurring memory expansion costs. 

Inline assembly allows for optimized memory usage by re-using already allocated memory spaces or using the scratch space for smaller datasets.
This can result in notable gas savings, especially for contracts that make frequent external calls.

Additionally, using inline assembly enables important safety checks like verifying if the target address has code deployed to it using `extcodesize(addr)` before making the call, mitigating risks associated with contract interactions.

*There are 129 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
57	        if (!registry.nativeYieldTokens(token_)) {
...
86	        if (registry.nativeYieldTokens(token)) {
```

*GitHub* : [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L57), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L86)


---

	 - src/blast/BlastMagicLP.sol

```solidity
48	        address feeTo_ = BlastMagicLP(address(implementation)).feeTo();
...
54	        address feeTo_ = BlastMagicLP(address(implementation)).feeTo();
...
56	        if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
...
59	        if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
...
105	        if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
...
109	        if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
...
119	        if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
...
119	        if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
```

*GitHub* : [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L48), [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L54), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L56), [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L59), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L105), [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L109), [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119), [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119)


---

	 - src/blast/BlastOnboarding.sol


*GitHub* : [169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L169), [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L178)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L69), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L89), [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106), [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L118), [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L119), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L131)


---

	 - src/blast/libraries/BlastPoints.sol


*GitHub* : [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L11)


---

	 - src/blast/libraries/BlastYields.sol


*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L21), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L25), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L30), [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L43), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L56), [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L61), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L71), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L71), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L76)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L156), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L156), [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L164), [174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L174), [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L187), [225](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L225), [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L253), [276](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L276), [295](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L295), [319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L319), [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L341), [451](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L451), [608](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L608)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L39)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L86)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L64), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L64), [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L66), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L70), [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L85), [83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L83), [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L88), [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L90), [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L90), [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L93), [117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L117), [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L119), [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L120), [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L129), [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L136), [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L172), [173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L173), [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L186), [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L187), [202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L202), [208](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L208), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L204), [216](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L216), [216](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L216), [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L236), [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L239), [238](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L238), [243](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L243), [243](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L243), [252](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L252), [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L253), [255](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L255), [271](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L271), [284](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L284), [295](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L295), [296](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L296), [286](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L286), [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L287), [308](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L308), [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L330), [328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L328), [351](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L351), [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L349), [359](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L359), [359](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L359), [382](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L382), [380](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L380), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L395), [393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L393), [399](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L399), [411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L411), [421](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L421), [427](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L427), [427](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L427), [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L439), [443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L443), [445](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L445), [456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L456), [467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L467), [473](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L473), [473](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L473), [485](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L485), [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L489), [491](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L491), [500](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L500), [514](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L514), [515](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L515), [516](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L516), [521](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L521), [522](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L522), [550](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L550), [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L547), [563](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L563), [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L561), [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L572), [579](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L579)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L25), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L26), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L26), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L34), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L38), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L38), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L39), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L39), [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45)

### [G-29]<a name="g-29"></a> Use Assembly for Hash Calculations

In certain cases, using inline assembly to calculate hashes can lead to significant gas savings. Solidity's built-in keccak256 function is convenient but costs more gas than the equivalent assembly code. However, it's important to note that using assembly should be done with care as it's less readable and could increase the risk of introducing errors.

*There are 1 instance(s) of this issue:*


---

	 - src/mimswap/periphery/Factory.sol

```solidity
163	        return keccak256(abi.encodePacked(sender_, implementation, baseToken_, quoteToken_, lpFeeRate_, i_, k_));
```

*GitHub* : [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L163)

### [G-30]<a name="g-30"></a> Consider Using Solady's Gas Optimized Lib for Math

Utilizing gas-optimized math functions from libraries like [Solady](https://github.com/Vectorized/solady/blob/main/src/utils/FixedPointMathLib.sol) can lead to more efficient smart contracts.
This is particularly beneficial in contracts where these operations are frequently used.

*There are 96 instance(s) of this issue:*


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
163	        return (userLocked * totalPoolShares) / totalLocked;
...
163	        return (userLocked * totalPoolShares) / totalLocked;
```

*GitHub* : [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L163), [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L163)


---

	 - src/mimswap/MagicLP.sol

```solidity
435	        baseAmount = (baseBalance * shareAmount) / totalShares;
...
435	        baseAmount = (baseBalance * shareAmount) / totalShares;
...
436	        quoteAmount = (quoteBalance * shareAmount) / totalShares;
...
436	        quoteAmount = (quoteBalance * shareAmount) / totalShares;
...
438	        _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
...
439	        _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
...
513	            _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
...
513	            _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
```

*GitHub* : [435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L435), [435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L435), [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L436), [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L436), [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438), [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439), [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513), [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513), [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517), [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517), [553](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L553)


---

	 - src/mimswap/libraries/DecimalMath.sol


*GitHub* : [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L24), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L24), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L28), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L32), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L32), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L36), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L40), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L53), [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L54), [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L54), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L56), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L56)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L21), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L30), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L56), [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L59), [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62), [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64), [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L93), [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L93), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L96), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L96), [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L99), [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L99), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L97), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L97), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L101), [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L152), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L155), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L155), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L156), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L156), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L156), [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L160), [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L160), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170), [171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L171), [181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L181), [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184), [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L185), [188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L188)


---

	 - src/mimswap/libraries/PMMPricing.sol


*GitHub* : [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209), [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L257), [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L257), [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L258), [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L258)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L38), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L39), [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L43), [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L44), [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45), [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L144), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L204), [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L236), [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L236), [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L241), [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L241), [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L258), [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L258), [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283), [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283), [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283), [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294), [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294), [380](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L380), [388](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L388)

### [G-31]<a name="g-31"></a> Trade-offs Between Modifiers and Internal Functions

In Solidity, both internal functions and modifiers are used to refactor and manage code, but they come with their own trade-offs, especially in terms of gas cost and flexibility.

#### Modifiers:
- Less runtime gas cost (saves around 24 gas per function call).
- Increases deployment gas cost due to repetitive code.
- Can only be executed at the start or end of a function.

#### Internal Functions:
- Lower deployment cost.
- Can be executed at any point in a function.
- Slightly higher runtime gas cost (24 gas) due to the need to jump to the function's location in bytecode.

#### Recommendations:
- Use modifiers for high-frequency functions where runtime gas cost matters the most.
- Use internal functions where the priority is reducing deployment gas cost or when you need more flexibility in the function's logic.

Example analysis shows that using modifiers can increase deployment costs by over 35k gas but save 24 gas per function call during runtime. Choose wisely based on your specific use case.

*There are 99 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
52	    function claimGasYields() external onlyOperators returns (uint256) {
...
56	    function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
...
68	    function callBlastPrecompile(bytes calldata data) external onlyOwner {
...
72	    function setFeeTo(address feeTo_) external onlyOwner {
...
81	    function setTokenEnabled(address token, bool enabled) external onlyOwner {
```

*GitHub* : [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L52), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L56), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L68), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81)


---

	 - src/blast/BlastGovernor.sol

```solidity
28	    function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
...
32	    function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
...
40	    function setFeeTo(address _feeTo) external onlyOwner {
...
49	    function callBlastPrecompile(bytes calldata data) external onlyOwner {
...
53	    function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

*GitHub* : [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L28), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L32), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40), [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L49), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)


---

	 - src/blast/BlastMagicLP.sol


*GitHub* : [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L47), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L47), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L53), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L53), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L64), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L64), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L72), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L72), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89), [118..123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L118-L123)


---

	 - src/blast/BlastOnboarding.sol


*GitHub* : [43..48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L43-L48), [50..56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L50-L56), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101), [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123), [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123), [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L156), [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L160), [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190), [195](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L195), [195](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L195), [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L200), [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L200), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L205), [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L214), [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L218)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96), [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129), [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L134), [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L244), [267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L267), [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290), [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360), [420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L420), [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L461), [479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L479), [479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L479), [504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L504), [504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L504), [607..612](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L607-L612), [614..619](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L614-L619), [621..626](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L621-L626)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105), [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L116), [126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L126)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [47..52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L47-L52), [169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L169), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L185), [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L199), [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L235), [321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L321), [342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L342), [372](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L372), [410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L410), [420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L420), [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L438), [455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L455), [466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L466), [484](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L484)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L150), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L155), [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300), [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317), [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L324), [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337), [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L341), [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L349), [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361), [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397)

### [G-32]<a name="g-32"></a> Optimize Boolean States with `uint256(1/2)`

Boolean variables in Solidity are more expensive than `uint256` or any type that takes up a full word, due to additional gas costs associated with write operations.
When using boolean variables, each write operation emits an extra SLOAD to read the slot's contents, replace the bits taken up by the boolean, and then write back.
This process cannot be disabled and leads to extra gas consumption.

By using `uint256(1)` and `uint256(2)` for representing true and false states, you can avoid a `Gwarmaccess` (100 gas) cost and also avoid a `Gsset` (20000 gas) cost when changing from `false` to `true`, after having been `true` in the past.
This approach helps in optimizing gas usage, making your contract more cost-effective.

[Usage in OpenZeppelin ReentrancyGuard.sol](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27)

*There are 7 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
21	    mapping(address => bool) public enabledTokens;
```

*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21)


---

	 - src/blast/BlastMagicLP.sol

```solidity
21	    mapping(address => bool) public operators;
```

*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L21)


---

	 - src/blast/BlastOnboarding.sol

```solidity
36	    mapping(address token => bool) public supportedTokens;
```

*GitHub* : [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
28	    bool public ready;
...
30	    mapping(address user => bool claimed) public claimed;
```

*GitHub* : [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L28), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L30)


---

	 - src/blast/BlastTokenRegistry.sol

```solidity
10	    mapping(address => bool) public nativeYieldTokens;
```

*GitHub* : [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10)


---

	 - src/mimswap/MagicLP.sol

```solidity
68	    bool internal _INITIALIZED_;
```

*GitHub* : [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L68)

### [G-33]<a name="g-33"></a> Consider Packing Small `uint` When it's Possible

Packing `uint` variables into the same storage slot can help in reducing gas costs.
This is particularly useful when storing or reading multiple smaller uints (e.g., uint80) in a single transaction.
Consider using bit manipulation to pack these variables.

If you pack two `uint` variables into a single `uint` storage slot, you'd perform only one SLOAD operation (800 gas) instead of two (1,600 gas) when you read them.
This saves 800 gas for each read operation involving the two variables.

Similarly, when you need to update both variables, a single SSTORE operation would cost you 20,000 gas instead of 40,000 gas, saving you another 20,000 gas. 

Example:
```Solidity
uint160 packedVariables;

function packVariables(uint80 x, uint80 y) external {
  packedVariables = uint160(x) << 80 | uint160(y);
}
```

*There are 8 instance(s) of this issue:*


---

	 - src/mimswap/MagicLP.sol

```solidity
72	    uint112 public _BASE_RESERVE_;
...
73	    uint112 public _QUOTE_RESERVE_;
...
74	    uint32 public _BLOCK_TIMESTAMP_LAST_;
...
76	    uint112 public _BASE_TARGET_;
...
77	    uint112 public _QUOTE_TARGET_;
...
78	    uint32 public _RState_;
```

*GitHub* : [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L78)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol

```solidity
13	    uint8 public immutable baseDecimals;
...
14	    uint8 public immutable quoteDecimals;
```

*GitHub* : [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L13), [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L14)

### [G-34]<a name="g-34"></a> Avoid Unnecessary Public Variables

Public storage variables increase the contract's size due to the implicit generation of public getter functions. 
This makes the contract larger and could increase deployment and interaction costs.

If you do not require other contracts to read these variables, consider making them `private` or `internal`. 

Example:
```solidity
/// 145426 gas to deploy
contract PublicState {
  address public first;
  address public second;
}
/// 77126 gas to deploy
contract PrivateState {
  address private first;
  address private second;
}
```

*There are 71 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
20	    BlastTokenRegistry public immutable registry;
...
21	    mapping(address => bool) public enabledTokens;
...
22	    address public feeTo;
```

*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21), [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L22)


---

	 - src/blast/BlastGovernor.sol

```solidity
11	    address public feeTo;
```

*GitHub* : [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L11)


---

	 - src/blast/BlastMagicLP.sol

```solidity
17	    BlastTokenRegistry public immutable registry;
...
20	    address public feeTo;
...
21	    mapping(address => bool) public operators;
```

*GitHub* : [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L17), [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L21)


---

	 - src/blast/BlastOnboarding.sol

```solidity
30	    State public state;
...
31	    address public bootstrapper;
...
32	    address public feeTo;
```

*GitHub* : [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L30), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L31), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L33), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L37), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L38), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L41)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L24), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L26), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L27), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L28), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L29), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L30)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10)


---

	 - src/blast/libraries/BlastPoints.sol


*GitHub* : [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L7), [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L8)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L61), [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64), [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L65), [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L66), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L70), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L71), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L75), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L78), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L79), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L80), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L81), [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L82)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L19), [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L20)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L33), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L35), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L36)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L31), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L33), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L34)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L10), [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L11), [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L12), [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L13), [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L14), [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L16)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L83), [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L84), [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L85), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L86), [87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L87), [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L94), [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L95), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L96), [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L98), [100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L100), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L101), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L102), [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L103)

### [G-35]<a name="g-35"></a> Optimize by Using Assembly for Low-Level Calls' Return Data

Even second return value from a low-level call is not assigned, it is still copied to memory, leading to additional gas costs.
By employing assembly, you can bypass this memory copying, achieving a 159 gas saving.

*There are 1 instance(s) of this issue:*


---

	 - src/blast/BlastGovernor.sol

```solidity
54	        (success, result) = to.call{value: value}(data);
```

*GitHub* : [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L54)

### [G-36]<a name="g-36"></a> Optimize Unsigned Integer Comparison With Zero

For unsigned integers, checking whether the integer is not equal to zero (`!= 0`) is less gas-intensive than checking whether it is greater than zero (`> 0`). 

This is because the Ethereum Virtual Machine (EVM) can perform a simple bitwise operation to check if any bit is set (which directly translates to `!= 0`), while checking for `> 0` requires additional logic.

As such, when dealing with unsigned integers in Solidity, it is recommended to use the `!= 0` comparison for gas optimization.

*There are 14 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
114	        if (caps[token] > 0 && totals[token].total > caps[token]) {
```

*GitHub* : [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114)


---

	 - src/mimswap/MagicLP.sol

```solidity
294	        if (data.length > 0) {
...
395	        } else if (baseReserve > 0 && quoteReserve > 0) {
...
395	        } else if (baseReserve > 0 && quoteReserve > 0) {
...
450	        if (data.length > 0) {
...
549	        if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
...
582	        if (amount > 0) {
...
588	        if (amount > 0) {
```

*GitHub* : [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L294), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395), [450](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L450), [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549), [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L582), [588](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L588)


---

	 - src/mimswap/libraries/Math.sol

```solidity
22	        if (remainder > 0) {
```

*GitHub* : [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L22)


---

	 - src/mimswap/periphery/Router.sol

```solidity
147	        } else if (baseReserve > 0 && quoteReserve > 0) {
```

*GitHub* : [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147), [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527), [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [636](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L636)

### [G-37]<a name="g-37"></a> Delete Unused State Variables

State variables that aren't used in the contract not only clutter the codebase but also consume unnecessary gas during deployment.
Specifically, setting non-zero initial values for state variables costs significant gas.
By removing these unused state variables, you can save on both deployment gas and potential future storage gas costs.
This optimization not only reduces gas expenditures but also enhances code clarity and maintainability.
Always ensure a thorough review to confirm that these variables are indeed redundant before removal.

*There are 27 instance(s) of this issue:*


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
78	    function claimable(address user) external view returns (uint256 shares) {
...
86	    function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
86	    function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
86	    function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
155	    function _claimable(address user) internal view returns (uint256 shares) {
```

*GitHub* : [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L78), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L155)


---

	 - src/mimswap/MagicLP.sol

```solidity
215	    function getMidPrice() public view returns (uint256 midPrice) {
...
224	    function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
...
224	    function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
...
228	    function getBaseInput() public view returns (uint256 input) {
...
232	    function getQuoteInput() public view returns (uint256 input) {
```

*GitHub* : [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L215), [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L224), [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L224), [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L228), [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L232)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34)


---

	 - src/mimswap/auxiliary/FeeRateModelImpl.sol


*GitHub* : [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L13)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L22), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L185), [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L235), [268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L268), [268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L268), [321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L321), [342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L342), [410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L410), [420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L420), [455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L455), [466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L466)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L34), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L34)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L69)

### [G-38]<a name="g-38"></a> Optimize Gas by Using Only Named Returns

The Solidity compiler can generate more efficient bytecode when using named returns.
It's recommended to replace anonymous returns with named returns for potential gas savings.

Example:
```solidity
/// 985 gas cost
function add(uint256 x, uint256 y) public pure returns (uint256) {
  return x + y;
}
/// 941 gas cost
function addNamed(uint256 x, uint256 y) public pure returns (uint256 res) {
  res = x + y;
}
```

*There are 62 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
52	    function claimGasYields() external onlyOperators returns (uint256) {
...
103	    function isOwner(address _account) internal view override returns (bool) {
```

*GitHub* : [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L52), [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L103)


---

	 - src/blast/BlastGovernor.sol

```solidity
28	    function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
...
32	    function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
```

*GitHub* : [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L28), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L32)


---

	 - src/blast/BlastMagicLP.sol

```solidity
39	    function version() external pure override returns (string memory) {
...
47	    function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {
```

*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L39), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L47)


---

	 - src/blast/BlastOnboarding.sol

```solidity
160	    function claimGasYields() external onlyOwner returns (uint256) {
...
226	    function _implementation() internal view override returns (address) {
```

*GitHub* : [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L160), [226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L226)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
96	    function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
```

*GitHub* : [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96)


---

	 - src/blast/libraries/BlastYields.sol

```solidity
38	    function claimMaxGasYields(address recipient) internal returns (uint256) {
```

*GitHub* : [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L38), [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L60), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L75)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155), [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L159), [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163), [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L236)


---

	 - src/mimswap/libraries/DecimalMath.sol


*GitHub* : [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L23), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L27), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L31), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L35), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L39), [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L43), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L47)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L19), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L79), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)


---

	 - src/mimswap/libraries/PMMPricing.sol


*GitHub* : [104..113](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L104-L113), [119..128](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L119-L128), [134..143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L134-L143), [147..156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L147-L156), [162..171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L162-L171), [175..184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L175-L184), [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L203)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L53), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L57), [65..72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65-L72), [155..162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L155-L162)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L29), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L33), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L37), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L48)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199), [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L203), [207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L207), [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L211), [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L215), [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L219), [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L223), [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L227), [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L231), [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L235), [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L239), [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L253), [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L257), [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L261), [265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L265), [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L269), [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L273), [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277), [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L288), [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L292)

### [G-39]<a name="g-39"></a> Optimize Address Storage Value Management with `assembly`



*There are 18 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
33	        feeTo = feeTo_;
...
77	        feeTo = feeTo_;
```

*GitHub* : [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L33), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L77)


---

	 - src/blast/BlastGovernor.sol

```solidity
20	        feeTo = feeTo_;
...
45	        feeTo = _feeTo;
```

*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L20), [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L45)


---

	 - src/blast/BlastMagicLP.sol

```solidity
32	        feeTo = feeTo_;
...
85	        feeTo = feeTo_;
```

*GitHub* : [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L32), [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L85)


---

	 - src/blast/BlastOnboarding.sol

```solidity
94	        feeTo = feeTo_;
...
152	        feeTo = feeTo_;
...
191	        bootstrapper = bootstrapper_;
```

*GitHub* : [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L94), [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L152), [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L191)


---

	 - src/blast/BlastWrappers.sol

```solidity
55	        _governor = governor_;
```

*GitHub* : [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L55)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L119), [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L120)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L27), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L51), [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L58)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L45), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L101)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [135](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L135)

### [G-40]<a name="g-40"></a> Use calldata instead of memory for function arguments that do not get mutated

Mark data types as `calldata` instead of `memory` where possible. This makes it so that the data is not automatically loaded into memory. If the data passed into the function does not need to be changed (like updating values in an array), it can be passed in as `calldata`. The one exception to this is if the argument must later be passed into another function that takes an argument that specifies `memory` storage.

*There are 13 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
164	    function claimTokenYields(address[] memory tokens) external onlyOwner {
```

*GitHub* : [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164)


---

	 - src/mimswap/libraries/PMMPricing.sol

```solidity
39	    function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {
...
76	    function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {
...
105	        PMMState memory state,
...
120	        PMMState memory state,
...
135	        PMMState memory state,
...
148	        PMMState memory state,
...
163	        PMMState memory state,
...
176	        PMMState memory state,
...
190	    function adjustedTarget(PMMState memory state) internal pure {
```

*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L39), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L76), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L105), [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L120), [135](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L135), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L148), [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L163), [176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L176), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L190), [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L203)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397), [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L572)

### [G-41]<a name="g-41"></a> Gas savings can be achieved by changing the model for assigning value to the structure

Change this `structName a = structName({item1: val1,item2: val2}); ==> structName a; a.item1 = val1; a.item2 = val2;`

*There are 2 instance(s) of this issue:*


---

	 - src/staking/LockingMultiRewards.sol

```solidity
501	            _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));
...
648	                _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
```

*GitHub* : [501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L501), [648](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L648)


```toml/n2solc = "0.8.20"
```

proof: 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2


*There are 20 instance(s) of this issue:*


---

	 - src/blast/BlastDapp.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2)


---

	 - src/blast/BlastBox.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
3	pragma solidity >=0.8.0;
```

*GitHub* : [3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L3)


---

	 - src/blast/BlastGovernor.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L2)


---

	 - src/blast/BlastMagicLP.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
3	pragma solidity >=0.8.0;
```

*GitHub* : [3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L3)


---

	 - src/blast/BlastOnboarding.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L2)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L2)


---

	 - src/blast/BlastTokenRegistry.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L2)


---

	 - src/blast/BlastWrappers.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L2)


---

	 - src/blast/libraries/BlastPoints.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L2)


---

	 - src/blast/libraries/BlastYields.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L2)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L8)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L8)


---

	 - src/mimswap/auxiliary/FeeRateModelImpl.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2)


---

	 - src/mimswap/libraries/DecimalMath.sol


*GitHub* : [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L7)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L8)


---

	 - src/mimswap/libraries/PMMPricing.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L8)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L2)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L2)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L2)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L2)