## \[G-01\] Declaring constructor as payable

You can cut out 10 opcodes in the creation-time EVM bytecode if you declare a constructor payable. The following opcodes are cut out:

- `CALLVALUE`
- `DUP1`
- `ISZERO`
- `PUSH2`
- `JUMPI`
- `PUSH1`
- `DUP1`
- `REVERT`
- `JUMPDEST`
- `POP`

```
constructor(
        address _stakingToken,
        uint256 _lockingBoostMultiplerInBips,
        uint256 _rewardsDuration,
        uint256 _lockDuration,
        address _owner
```

> All contracts

&nbsp;

# \[G-02\] Use assembly to validate msg.sender

We can use assembly to efficiently validate msg.sender for the didPay and uniswapV3SwapCallback functions with the least amount of opcodes necessary. Additionally, we can use xor() instead of iszero(eq()), saving 3 gas. We can also potentially save gas on the unhappy path by using scratch space to store the error selector, potentially avoiding memory expansion costs.

```
if (address(this) == address(implementation)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L615

&nbsp;

## \[G-03\] Make 3 event parameters indexed when possible

events are used to emit information about state changes in a contract. When defining an event, it's important to consider the gas cost of emitting the event, as well as the efficiency of searching for events in the Ethereum blockchain.

Making event parameters indexed can help reduce the gas cost of emitting events and improve the efficiency of searching for events. When an event parameter is marked as indexed, its value is stored in a separate data structure called the event topic, which allows for more efficient searching of events.

```
event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);
    event LogPoolRemoved(address pool);
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L23C1-L24C40

```
event BuyShares(address to, uint256 increaseShares, uint256 totalShares);
    event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);
    event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);
    event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);
    event RChange(PMMPricing.RState newRState);
    event TokenRescue(address indexed token, address to, uint256 amount);
    event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L30C1-L36C7

## \[G-04\]Amounts should be checked for 0 before calling a transfer

Checking non-zero transfer values can avoid an expensive external call and save gas. While this is done at some places, it's not consistently done in the solution.

```
token.safeTransfer(to, amount);
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L466

## <ins>\[G-05\] Events are not indexed</ins>

The emitted events are not indexed, making off-chain scripts such as front-ends of dApps difficult to filter the events efficiently.

Recommend adding the `indexed` keyword in each event,

&nbsp;

```
event LogPoolAdded(address baseToken, address quoteToken, address creator, address pool);
    event LogPoolRemoved(address pool);
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L23C1-L24C40

```
event BuyShares(address to, uint256 increaseShares, uint256 totalShares);
    event SellShares(address payer, address to, uint256 decreaseShares, uint256 totalShares);
    event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);
    event FlashLoan(address borrower, address assetTo, uint256 baseAmount, uint256 quoteAmount);
    event RChange(PMMPricing.RState newRState);
    event TokenRescue(address indexed token, address to, uint256 amount);
    event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L30C1-L36C7

&nbsp;

## \[G‑06\] Functions guaranteed to revert when called by normal users can be marked payable

```
function withdraw(uint256 amount) public virtual {
```

# \[G-07\] Use constants instead of type(uintx).max

it's generally more gas-efficient to use constants instead of type(uintX).max when you need to set the maximum value of an unsigned integer type.

The reason for this is that the type(uintX).max expression involves a computation at runtime, whereas a constant is evaluated at compile-time. This means that using type(uintX).max can result in additional gas costs for each transaction that involves the expression.

By using a constant instead of type(uintX).max, you can avoid these additional gas costs and make your code more efficient.

Here's an example of how you can use a constant instead of type(uintX).max:

```
contract MyContract {
    uint120 constant MAX_VALUE = 2**120 - 1;
    
    function doSomething(uint120 value) public {
        require(value <= MAX_VALUE, "Value exceeds maximum");
        
        // Do something
    }
}
```

In the above example, we have a contract with a constant MAX\_VALUE that represents the maximum value of a uint120. When the doSomething function is called with a value parameter, it checks whether the value is less than or equal to MAX\_VALUE using the <= operator.

By using a constant instead of type(uint120).max, we can make our code more efficient and reduce the gas cost of our contract.

It's important to note that using constants can make your code more readable and maintainable, since the value is defined in one place and can be easily updated if necessary. However, constants should be used with caution and only when their value is known at compile-time.

```
508:       if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L508

```
532: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L532

```
MIM.safeApprove(address(router), type(uint256).max);
        USDB.safeApprove(address(router), type(uint256).max);
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L103C1-L104C62

# \[G-08\] Duplicated require()/if() checks should be refactored to a modifier or function

&nbsp;

&nbsp;

```
327:	if (directions & 1 == 0) {

348:	 if (directions & 1 == 0) {

392:	if (directions & 1 == 0) {

545:	 if (directions & 1 == 0) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L327

&nbsp;

```
23: if (maintainer_ == address(0)) {

47: if (maintainer_ == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L47

## \[G‑09\] Multiple accesses of a mapping/array should use a local variable cache

Caching a mapping’s value in a local storage or calldata variable when the value is accessed multiple times saves ~42 gas per access due to not having to perform the same offset calculation every time. Help the Optimizer by saving a storage variable’s reference instead of repeatedly fetching it.

To help the optimizer,declare a storage type variable and use it instead of repeatedly fetching the reference in a map or an array.

```
File: LockingMultiRewards.sol

204:        return _rewardData[rewardToken].rewardRate * rewardsDuration;

270: 	     return MathLib.min(block.timestamp, _rewardData[rewardToken].periodFinish);

279: 	    return _rewardData[rewardToken].rewardPerTokenStored;

282:        uint256 timeElapsed = lastTimeRewardApplicable_ - _rewardData[rewardToken].lastUpdateTime;
283:        uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;

285:	    return _rewardData[rewardToken].rewardPerTokenStored + pendingRewardsPerToken;

305:        if (_rewardData[rewardToken].exists) {

314:        _rewardData[rewardToken].exists = true;

362:	   if (!_rewardData[rewardToken].exists) {
```

&nbsp;https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L204

&nbsp;

## \[G‑10\] Division by two should use bit shifting

<x>/ 2 is the same as <x>\>> 1. While the compiler uses the SHR opcode to accomplish both, the version that uses division incurs an overhead of 20 gas due to JUMPs to and from a compiler utility function that introduces checks which can be avoided by using unchecked {} around the division by two.</x></x>

`<x> * 2` is equivalent to `<x> << 1` and `<x> / 2` is the same as `<x> >> 1`. The `MUL` and `DIV` opcodes cost 5 gas, whereas `SHL` and `SHR` only cost 3 gas.

```
File: Math.sol

34:           z = (x / z + z) / 2;

101:         uint256 premium = DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2) + DecimalMath.ONE;

188:         uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
```

&nbsp;https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L34

```
File: DecimalMath.sol

 53:  uint p = powFloor(target, e / 2);
```

&nbsp;https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L53

## \[G‑11\] Counting down in `for` statements is more gas efficient

Counting down is more gas efficient than counting up because neither we are making zero variable to non-zero variable and also we will get gas refund in the last transaction when making non-zero to zero variable.

[Reference.](https://code4rena.com/reports/2023-08-pooltogether#wardens:~:text=%5BG%E2%80%9102%5D%20Counting%20down%20in%20for%20statements%20is%20more%20gas%20efficient)

## \[G-12\] Use Assembly To Check For address(0)

it's generally more gas-efficient to use assembly to check for a zero address (address(0)) than to use the == operator.

The reason for this is that the == operator generates additional instructions in the EVM bytecode, which can increase the gas cost of your contract. By using assembly, you can perform the zero address check more efficiently and reduce the overall gas cost of your contract.

Here's an example of how you can use assembly to check for a zero address:

```
contract MyContract {
    function isZeroAddress(address addr) public pure returns (bool) {
        uint256 addrInt = uint256(addr);
        
        assembly {
            // Load the zero address into memory
            let zero := mload(0x00)
            
            // Compare the address to the zero address
            let isZero := eq(addrInt, zero)
            
            // Return the result
            mstore(0x00, isZero)
            return(0, 0x20)
        }
    }
}
```

In the above example, we have a function isZeroAddress that takes an address as input and returns a boolean value indicating whether the address is equal to the zero address. Inside the function, we convert the address to an integer using uint256(addr), and then use assembly to compare the integer to the zero address.

By using assembly to perform the zero address check, we can make our code more gas-efficient and reduce the overall cost of our contract. It's important to note that assembly can be more difficult to read and maintain than Solidity code, so it should be used with caution and only when necessary.

### Mitigation

Using `assembly` to check for the zero address can result in significant gas savings compared to using a Solidity expression; especially if the check is performed frequently or in a loop. However, it’s important to note that using `assembly` can make the code less readable and harder to maintain, so it should be used judiciously and with caution.

```
if (rewardToken == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L301

&nbsp;

```
if (address(weth_) == address(0) || address(factory_) == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L39

```
39: if (implementation_ == address(0)) {

42: if (address(maintainerFeeRateModel_) == address(0)) {

97:  if (implementation_ == address(0)) {

106: if (address(maintainerFeeRateModel_) == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L39

```
if (maintainer_ == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L23

&nbsp;

```
35: if (implementation == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L35

&nbsp;

```
23: if (maintainer_ == address(0)) {

47: if (maintainer_ == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L47

```
if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L102

&nbsp;

```
21: 	    if (governor_ == address(0)) {

35:         if (governor_ == address(0)) {

48:         if (governor_ == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L21

```
85:         if (address(registry_) == address(0)) {

89:  	    if (feeTo_ == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L85

&nbsp;

## \[G-13\] Rearranging order of state variable declarations to pack them will save storage slots and gas[](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L35)

```diff
bool internal _INITIALIZED_;
    address public _BASE_TOKEN_;
    address public _QUOTE_TOKEN_;
    uint112 public _BASE_RESERVE_;
    uint112 public _QUOTE_RESERVE_;
    uint32 public _BLOCK_TIMESTAMP_LAST_;
    uint256 public _BASE_PRICE_CUMULATIVE_LAST_;
    uint112 public _BASE_TARGET_;
    uint112 public _QUOTE_TARGET_;
    uint32 public _RState_;
    IFeeRateModel public _MT_FEE_RATE_MODEL_;
    uint256 public _LP_FEE_RATE_;
    uint256 public _K_;
    uint256 public _I_;
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L68C1-L82C24

## \[G‑14\] Use nested `if` and avoid multiple check combinations

Using nested `if`, is cheaper than using `&&` multiple check combinations. There are more advantages, such as easier to read code and better coverage reports.

&nbsp;

```
326: if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

417: if (index == lastLockIndex[user] && locks.length > 1) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L326

```
if (address(weth_) == address(0) || address(factory_) == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L39

```
} else if (baseReserve > 0 && quoteReserve > 0) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L147

```
327:	if (directions & 1 == 0) {

348:	 if (directions & 1 == 0) {

379:	 if ((directions >> lastLpIndex) & 1 == 0) {

392:	if (directions & 1 == 0) {

545:	 if (directions & 1 == 0) {

599:	 if (baseDecimals == 0 || quoteDecimals == 0) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L327

&nbsp;

```
139:         if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {

144:        if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L139

```
if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L302

&nbsp;

```
102:  if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L102

```
if (governor_ == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L21

## \[G-15\]  `10 ** 18` can be changed to `1e18` and save some gas

`10 ** 18` can be changed to `1e18` to avoid unnecessary arithmetic operation and save gas.

```
File: DecimalMath.sol

20:    uint256 internal constant ONE = 10 ** 18;

49:    return 10 ** 18;
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L20C5-L20C46

```
uint256 public constant MAX_K = 10 ** 18;
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L64

## \[G‑16\] Save gas by preventing zero amount in mint() and burn()

```
_mint(to, shares);
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L406

&nbsp;

```
_burn(msg.sender, shareAmount);
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L445

&nbsp;

## \[G-17\] uint8 is not always cheaper than uint256

The EVM only operates on 32 bytes/ 256 bits at a time. This means that if you use uint8, EVM has to first convert it uint256 to work on it and the conversion costs extra gas! You may wonder, What were the devs thinking? Why did they create smaller variables then? The answer lies in packing. In solidity, you can pack multiple small variables into one slot, but if you are defining a lone variable and can’t pack it, it’s optimal to use a uint256 rather than uint8.

```
uint8 public immutable baseDecimals;
    uint8 public immutable quoteDecimals;
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L13C1-L14C42

## \[G-18\] Use hardcode address instead `address(this)`

Instead of using `address(this)`, it is more gas-efficient to pre-calculate and use the hardcoded `address`. Foundry’s script.sol and solmate’s `LibRlp.sol` contracts can help achieve this.

References: <ins>https://book.getfoundry.sh/reference/forge-std/compute-create-address</ins>

<ins>https://twitter.com/transmissions11/status/1518507047943245824</ins>

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L92

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L228C4-L234C6

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L245

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L262

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L268

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L427

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L431C1-L432C71

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L615

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L59

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastWrappers.sol#L60

## \[G-19\] Do not calculate constants

Due to how constant variables are implemented (replacements at compile-time), an expression assigned to a constant variable is recomputed each time that the variable is used, which wastes some gas.

&nbsp;

```
File: DecimalMath.sol

20:    uint256 internal constant ONE = 10 ** 18;

21:    uint256 internal constant ONE2 = 10 ** 36;

49:    return 10 ** 18;
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L20C5-L20C46

```
uint256 public constant MAX_I = 10 ** 36;
    uint256 public constant MAX_K = 10 ** 18;
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L63C1-L64C46