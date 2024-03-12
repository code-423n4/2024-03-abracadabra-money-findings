# GAS OPTIMIZATION

# SUMMARY
|      |  issue  |  instance  |
|------|---------|------------|
|[G‑01]|Avoid updating storage when the value hasn't changed|18|
|[G‑02]|Can Make The Variable Outside The Loop To Save Gas|9|
|[G‑03]|Use assembly to write address storage values|14|
|[G‑04]|Amounts should be checked for 0 before calling a transfer|5|
|[G‑05]|Do not calculate constants|4|
|[G‑06]| With assembly, .call (bool success) transfer can be done gas-optimized|1|
|[G‑07]|Avoid contract existence checks by using low level calls|51|
|[G‑08]| Use Assembly To Check For address(0)|26|
|[G‑09]|Use hardcode address instead address(this)|41|
|[G‑10]|Constructors can be marked payable|16|
|[G‑11]|Use the inputs/results of assignments rather than re-reading state variables|44|
|[G‑12]|State variables that are used multiple times in a function should be cached in stack variables|8|
|[G‑13]|Use nested if statements instead of &&|8|
|[G‑14]| Use assembly to emit events|57|
|[G‑15]|Instead of counting down in for statements, count up|8|
|[G‑16]|Move storage pointer to top of function to avoid offset calculation|1|
|[G‑17]|Consider using OZ EnumerateSet in place of nested mappings |5|
|[G‑18]|Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct, where appropriate|3|
|[G‑19]| Use calldata instead of memory for function arguments that do not get mutated|2|
|[G‑20]|Unlimited gas consumption risk due to external call recipients|1|
|[G‑21]|Same cast is done multiple times|5|
|[G‑22]|Using constants instead of enum can save gas|2|
|[G‑23]|Use assembly to calculate hashes to save gas:|1|
|[G‑24]|Unused named return variables without optimizer waste gas|18|
|[G‑25]|Emit Used In Loop:|4|
|[G‑26]|Structs can be modified to fit in fewer storage slots|2|
|[G‑27]| Use assembly to validate msg.sender|1|
|[G‑28]| State variable read in a loop|2|
|[G‑29]|Initializers can be marked payable|2|
|[G‑30]|Usage of `uints`/`ints` smaller than 32 bytes (256 bits) incurs overhead|2|
|[G‑31]|Stack variable used as a cheaper cache for a state variable is only used once|2|
|[G‑32]|Use local variables for emitting|4|
|[G‑33]|State variables can be packed into fewer storage slots|2|
|[G‑34]|Storage re-read via storage pointer|4|
|[G‑35]|Sort Solidity operations using short-circuit mode|1|
|[G‑36]|Internal functions only called once can be inlined to save gas|3|
|[G‑37]|Use constants instead of type(uintx).max|6|



## [G-01] Avoid updating storage when the value hasn't changed

If the old value is equal to the new value, not re-storing the value will avoid a Gsreset (**2900 gas**), potentially at the expense of a Gcoldsload (**2100 gas**) or a Gwarmaccess (**100 gas**).

```solidity
File: src/blast/BlastBox.sol
72          function setFeeTo(address feeTo_) external onlyOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72:72

```solidity
File: src/blast/BlastGovernor.sol
40          function setFeeTo(address _feeTo) external onlyOwner {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40:40

```solidity
File: src/blast/BlastMagicLP.sol
80          function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80:80

```solidity
File: src/blast/BlastOnboarding.sol
147         function setFeeTo(address feeTo_) external onlyOwner {

195         function open() external onlyOwner onlyState(State.Idle) {

190         function setBootstrapper(address bootstrapper_) external onlyOwner {

200         function close() external onlyOwner onlyState(State.Opened) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L200:200

```solidity
File: src/blast/BlastOnboardingBoot.sol
96          function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {

146         function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146:146


```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol
57          function setImplementation(address implementation_) public onlyOwner {

46          function setMaintainer(address maintainer_) external onlyOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46:46

```solidity
File: src/mimswap/periphery/Factory.sol
96          function setLpImplementation(address implementation_) external onlyOwner {

105         function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105:105


```solidity
File: src/staking/LockingMultiRewards.sol
317         function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317:317

```solidity
File: test/mocks/ERC20Mock.sol
19          function setDecimals(uint8 decimals_) external {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mocks/ERC20Mock.sol#L19:19

```solidity
File: utils/BaseScript.sol
33          function setNewDeploymentEnabled(bool _enabled) public {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/BaseScript.sol#L33:33

```solidity
File: utils/BaseTest.sol
28          function setUpNoMocks() public virtual {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/BaseTest.sol#L28:28

```solidity
File: utils/Toolkit.sol
273         function setTesting(bool _testing) public {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/Toolkit.sol#L273:273


## [G-02] Can Make The Variable Outside The Loop To Save Gas 

When you declare a variable inside a loop, Solidity creates a new instance of the variable for each iteration of the loop. This can lead to unnecessary gas costs, especially if the loop is executed frequently or iterates over a large number of elements.

By declaring the variable outside the loop, you can avoid the creation of multiple instances of the variable and reduce the gas cost of your contract. Here's an example:


```solidity
File:  src/staking/LockingMultiRewards.sol
406  address user = users[i];

414  uint256 index = lockIndexes[i];

426  uint256 amount = locks[index].amount;
427  uint256 lastIndex = locks.length - 1;

562  address token = rewardTokens[i];

576  address token = rewardTokens[i];

577  uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);

615  address rewardToken = rewardTokens[i];
616  uint256 rewardAmount = rewards[user][rewardToken];
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L406


## [G-03] Use assembly to write address storage values

By using assembly to write to address storage values, you can bypass some of these operations and lower the gas cost of writing to storage. Assembly code allows you to directly access the Ethereum Virtual Machine (EVM) and perform low-level operations that are not possible in Solidity.

example of using assembly to write to address storage values:
```solidity
contract MyContract {
    address private myAddress;
    
    function setAddressUsingAssembly(address newAddress) public {
        assembly {
            sstore(0, newAddress)
        }
    }
}
```

There are 14 instances of this issue:

```solidity
File:  src/blast/BlastBox.sol
33  feeTo = feeTo_;

77  feeTo = feeTo_;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L33

```solidity
File:  src/blast/BlastGovernor.sol
20  feeTo = feeTo_;

45  feeTo = _feeTo;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L45

```solidity
File:  src/blast/BlastMagicLP.sol
32   feeTo = feeTo_;

85   feeTo = feeTo_;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L32

```solidity
File:  src/blast/BlastOnboarding.sol
191   bootstrapper = bootstrapper_;

94    feeTo = feeTo_;

152   feeTo = feeTo_;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L191

```solidity
File:  src/mimswap/MagicLP.sol
119  _BASE_TOKEN_ = baseTokenAddress;

120  _QUOTE_TOKEN_ = quoteTokenAddress;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L119

```solidity
File:  src/mimswap/auxiliary/FeeRateModel.sol
27  maintainer = maintainer_;

51  maintainer = maintainer_;

58  implementation = implementation_;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L27


## [G-04] Amounts should be checked for 0 before calling a transfer

Checking non-zero transfer values can avoid an expensive external call and save gas.

There are 5 instances of this issue:

```solidity
File:  src/blast/BlastOnboarding.sol
138  token.safeTransfer(msg.sender, amount);

210  token.safeTransfer(to, amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L138


```solidity
File:  src/staking/LockingMultiRewards.sol
217  address(weth).safeTransfer(lp, wethAdjustedAmount);

311   token.safeTransfer(to, tokenAmountOut);

359     weth.deposit{value: msg.value}();
        inToken.safeTransfer(address(firstLp), msg.value);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L217





## [G-05] Do not calculate constants
Due to how constant variables are implemented (replacements at compile-time), an expression assigned to a constant variable is recomputed each time that the variable is used, which wastes some gas
[Reffrence](https://code4rena.com/reports/2022-07-golom#g-24-do-not-calculate-constants)


```solidity
File:  src/mimswap/MagicLP.sol
63    uint256 public constant MAX_I = 10 ** 36;
64    uint256 public constant MAX_K = 10 ** 18;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63-L64


```solidity
File:  src/mimswap/libraries/DecimalMath.sol
20    uint256 internal constant ONE = 10 ** 18;
21    uint256 internal constant ONE2 = 10 ** 36;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20-L21


## [G-06] With assembly, .call (bool success) transfer can be done gas-optimized

return data (bool success,) has to be stored due to EVM architecture, but in a usage like below, ‘out’ and ‘outsize’ values are given (0,0), this storage disappears and gas optimization is provided.

```solidity
File:  src/blast/BlastGovernor.sol
54  (success, result) = to.call{value: value}(data);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L54



## [G-07] Avoid contract existence checks by using low level calls

Prior to 0.8.10 the compiler inserted extra code, including `EXTCODESIZE` (100 gas), to check for contract existence for external function calls. In more recent solidity versions, the compiler will not insert these checks if the external call has a return value. Similar behavior can be achieved in earlier versions by using low-level calls, since low level calls never check for contract existence.

Note: missed from bots


```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol
39              return IFeeRateImpl(implementation).getFeeRate(msg.sender, trader, lpFeeRate);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L39:39

```solidity
File: src/mimswap/periphery/Factory.sol
86              IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L86:86

```solidity
File: src/mimswap/periphery/Router.sol
286                 token = IMagicLP(lp)._QUOTE_TOKEN_();

70              (shares, , ) = IMagicLP(clone).buyShares(to);

295             } else if (IMagicLP(lp)._QUOTE_TOKEN_() == address(weth)) {

328                 IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

208             } else if (IMagicLP(lp)._QUOTE_TOKEN_() == address(weth)) {

66              clone = IFactory(factory).create(baseToken, quoteToken, lpFeeRate, i, k);

411            IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

204                 token = IMagicLP(lp)._QUOTE_TOKEN_();

186             IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);

236             address token = IMagicLP(lp)._BASE_TOKEN_();

172             IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);

117             (uint256 baseReserve, uint256 quoteReserve) = IMagicLP(lp).getReserves();

287                 (ethAmountOut, tokenAmountOut) = IMagicLP(lp).sellShares(

296                 (tokenAmountOut, ethAmountOut) = IMagicLP(lp).sellShares(

351                 inToken = IMagicLP(firstLp)._QUOTE_TOKEN_();

489             IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

136                 uint256 i = IMagicLP(lp)._I_();

443             IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

572             amountOut = IMagicLP(lp).sellBase(to);

173             IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);

439             if (IMagicLP(lp)._QUOTE_TOKEN_() != address(weth)) {

393                 IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

467             address quoteToken = IMagicLP(lp)._QUOTE_TOKEN_();

522                 uint256 i = IMagicLP(lp)._I_();

563                 amountOut = IMagicLP(path[iterations]).sellQuote(to);

380                 outToken = IMagicLP(lastLp)._QUOTE_TOKEN_();

421             address baseToken = IMagicLP(lp)._BASE_TOKEN_();

187             IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);

485             if (IMagicLP(lp)._BASE_TOKEN_() != address(weth)) {

550            IMagicLP(path[i]).sellQuote(address(path[i + 1]));

252             uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp));

238             token = IMagicLP(lp)._QUOTE_TOKEN_();

500             (shares, , ) = IMagicLP(lp).buyShares(to);

202             address token = IMagicLP(lp)._BASE_TOKEN_();

284             address token = IMagicLP(lp)._BASE_TOKEN_();

330            IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);

349                 inToken = IMagicLP(firstLp)._BASE_TOKEN_();

239             } else if (IMagicLP(lp)._QUOTE_TOKEN_() != address(weth)) {

514             (uint256 baseReserve, uint256 quoteReserve) = IMagicLP(lp).getReserves();

271             return IMagicLP(lp).sellShares(sharesIn, to, minimumBaseAmount, minimumQuoteAmount, "", deadline);

395                 IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);

253             uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp));

547                     IMagicLP(path[i]).sellBase(address(path[i + 1]));

579             amountOut = IMagicLP(lp).sellQuote(to);

382                 outToken = IMagicLP(lastLp)._BASE_TOKEN_();

93              (shares, , ) = IMagicLP(clone).buyShares(to);

561                 amountOut = IMagicLP(path[iterations]).sellBase(to);

456             IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);

88              clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L88:88



## [G-08] Use Assembly To Check For address(0)
Saves 6 gas per instance if using assembly to check for address(0)

```solidity
File: src/blast/BlastBox.sol
25              if (feeTo_ == address(0)) {

28              if (address(registry_) == address(0)) {

73              if (feeTo_ == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L25

```solidity
File: src/blast/BlastGovernor.sol
16              if (feeTo_ == address(0)) {

41              if(_feeTo == address(0)) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L16

```solidity
File: src/blast/BlastMagicLP.sol
24              if (feeTo_ == address(0)) {

27              if (address(registry_) == address(0)) {

81              if (feeTo_ == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L24

```solidity
File: src/blast/BlastOnboarding.sol
85              if (address(registry_) == address(0)) {

89              if (feeTo_ == address(0)) {

148             if (feeTo_ == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L85

```solidity
File: src/blast/BlastOnboardingBoot.sol
97              if (pool != address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L97

```solidity
File: src/blast/BlastTokenRegistry.sol
15              if (token == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L15:15

```solidity
File: src/blast/BlastWrappers.sol
21              if (governor_ == address(0)) {

35              if (governor_ == address(0)) {

48              if (governor_ == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L48:48


```solidity
File: src/mimswap/MagicLP.sol
102             if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102:102

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol
23              if (maintainer_ == address(0)) {

35              if (implementation == address(0)) {

47              if (maintainer_ == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L23

```solidity
File: src/mimswap/periphery/Factory.sol
39              if (implementation_ == address(0)) {

42              if (address(maintainerFeeRateModel_) == address(0)) {

97              if (implementation_ == address(0)) {

106             if (address(maintainerFeeRateModel_) == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L106:106

```solidity
File: src/mimswap/periphery/Router.sol
39              if (address(weth_) == address(0) || address(factory_) == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L39:39


```solidity
File: src/staking/LockingMultiRewards.sol
301             if (rewardToken == address(0)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L301:301





## [G-09] Use hardcode address instead address(this)
it can be more gas-efficient to use a hardcoded address instead of the address(this) expression, especially if you need to use the same address multiple times in your contract.

```solidity
File:  src/blast/BlastOnboardingBoot.sol
106  (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

117        staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
        staking.setOperator(address(this), true);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106


```solidity
File:  src/blast/libraries/BlastYields.sol
21  if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {

26  emit LogBlastTokenClaimableEnabled(address(this), token);

31  emit LogBlastNativeClaimableEnabled(address(this));

39  return claimMaxGasYields(address(this), recipient);

52  return claimAllNativeYields(address(this), recipient);

71  amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L21


```solidity
File:  src/mimswap/MagicLP.sol
229  return _BASE_TOKEN_.balanceOf(address(this)) - uint256(_BASE_RESERVE_);

233  return _QUOTE_TOKEN_.balanceOf(address(this)) - uint256(_QUOTE_RESERVE_);

245  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));

262  _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));

268  uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

285  _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);

298      uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
        uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

361     uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
        uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this)); 

427   if (to == address(this)) {

431      uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
        uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));  

505     uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
        uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this)); 


530     baseBalance = _BASE_TOKEN_.balanceOf(address(this));
        quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));   

568     uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
        uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this)); 

615    if (address(this) == address(implementation)) {

622  if (address(this) != address(implementation)) {                                            
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L229



```solidity
File:  src/mimswap/periphery/Router.sol
92  address(weth).safeTransferFrom(address(this), clone, msg.value);

269  lp.safeTransferFrom(msg.sender, address(this), sharesIn);

283  lp.safeTransferFrom(msg.sender, address(this), sharesIn);

289   address(this),

298  address(this),

398  amountOut = _swap(address(this), path, directions, minimumOut);

444  amountOut = _sellBase(lp, address(this), minimumOut);

490   amountOut = _sellQuote(lp, address(this), minimumOut);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92


```solidity
File:  src/staking/LockingMultiRewards.sol
326  if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

367  rewardToken.safeTransferFrom(msg.sender, address(this), amount);

464   stakingToken.safeTransferFrom(msg.sender, address(this), amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326




## [G-10] Constructors can be marked payable
Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn't provided. A constructor can safely be marked as payable, since only the deployer would be able to pass funds, and the project itself would not pass any funds.


```solidity
File: src/blast/BlastBox.sol
24          constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
25              if (feeTo_ == address(0)) {
26                  revert ErrZeroAddress();
27              }
28              if (address(registry_) == address(0)) {
29                  revert ErrZeroAddress();
30              }
31      
32              registry = registry_;
33              feeTo = feeTo_;
34          }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24:34

```solidity
File: src/blast/BlastDapp.sol
7           constructor() {
8               BlastPoints.configure();
9           }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L7:9

```solidity
File: src/blast/BlastGovernor.sol
15          constructor(address feeTo_, address _owner) OperatableV2(_owner) {
16              if (feeTo_ == address(0)) {
17                  revert ErrZeroAddress();
18              }
19      
20              feeTo = feeTo_;
21              BlastYields.configureDefaultClaimables(address(this));
22          }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15:22

```solidity
File: src/blast/BlastMagicLP.sol
23          constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
24              if (feeTo_ == address(0)) {
25                  revert ErrZeroAddress();
26              }
27              if (address(registry_) == address(0)) {
28                  revert ErrZeroAddress();
29              }
30      
31              registry = registry_;
32              feeTo = feeTo_;
33          }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23:33

```solidity
File: src/blast/BlastOnboarding.sol
58          constructor() Owned(msg.sender) {
59              BlastYields.configureDefaultClaimables(address(this));
60              BlastPoints.configure();
61          }


84          constructor(BlastTokenRegistry registry_, address feeTo_) {
85              if (address(registry_) == address(0)) {
86                  revert ErrZeroAddress();
87              }
88      
89              if (feeTo_ == address(0)) {
90                  revert ErrZeroAddress();
91              }
92      
93              registry = registry_;
94              feeTo = feeTo_;
95          }
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L84:95

```solidity
File: src/blast/BlastTokenRegistry.sol
12          constructor(address _owner) Owned(_owner) {}
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12:12

```solidity
File: src/blast/BlastWrappers.sol
20          constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
21              if (governor_ == address(0)) {
22                  revert ErrZeroAddress();
23              }
24              BlastYields.configureDefaultClaimables(governor_);
25          }


29          constructor(
30              address implementation_,
31              IFeeRateModel maintainerFeeRateModel_,
32              address owner_,
33              address governor_
34          ) Factory(implementation_, maintainerFeeRateModel_, owner_) {
35              if (governor_ == address(0)) {
36                  revert ErrZeroAddress();
37              }
38              BlastYields.configureDefaultClaimables(governor_);
39          }


47          constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
48              if (governor_ == address(0)) {
49                  revert ErrZeroAddress();
50              }
51              if (governor_ == address(this)) {
52                  revert ErrInvalidGovernorAddress();
53              }
54      
55              _governor = governor_;
56              _setupBlacklist();
57          }


```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L47:57


```solidity
File: src/mimswap/MagicLP.sol
84          constructor(address owner_) Owned(owner_) {
85              implementation = this;
86      
87              // prevents the implementation contract initialization
88              _INITIALIZED_ = true;
89          }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84:89

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

22          constructor(address maintainer_, address owner_) Owned(owner_) {
23              if (maintainer_ == address(0)) {
24                  revert ErrZeroAddress();
25              }
26      
27              maintainer = maintainer_;
28          }
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22:28

```solidity
File: src/mimswap/periphery/Factory.sol
38          constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
39              if (implementation_ == address(0)) {
40                  revert ErrZeroAddress();
41              }
42              if (address(maintainerFeeRateModel_) == address(0)) {
43                  revert ErrZeroAddress();
44              }
45              implementation = implementation_;
46              maintainerFeeRateModel = maintainerFeeRateModel_;
47          }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38:47

```solidity
File: src/mimswap/periphery/Router.sol
38          constructor(IWETH weth_, IFactory factory_) {
39              if (address(weth_) == address(0) || address(factory_) == address(0)) {
40                  revert ErrZeroAddress();
41              }
42      
43              weth = weth_;
44              factory = factory_;
45          }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38:45


```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol
21          constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
22              pair = pair_;
23              baseOracle = baseOracle_;
24              quoteOracle = quoteOracle_;
25              baseDecimals = IERC20Metadata(pair_._BASE_TOKEN_()).decimals();
26              quoteDecimals = IERC20Metadata(pair_._QUOTE_TOKEN_()).decimals();
27          }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21:27

```solidity
File: src/staking/LockingMultiRewards.sol
112         constructor(
113             address _stakingToken,
114             uint256 _lockingBoostMultiplerInBips,
115             uint256 _rewardsDuration,
116             uint256 _lockDuration,
117             address _owner
118         ) OperatableV2(_owner) {
119             if (_lockingBoostMultiplerInBips <= BIPS) {
120                 revert ErrInvalidBoostMultiplier();
121             }
122     
123             if (_lockDuration < MIN_LOCK_DURATION) {
124                 revert ErrInvalidLockDuration();
125             }
126     
127             if (_rewardsDuration < MIN_REWARDS_DURATION) {
128                 revert ErrInvalidRewardDuration();
129             }
130     
131             if (_lockDuration % _rewardsDuration != 0) {
132                 revert ErrInvalidDurationRatio();
133             }
134     
135             stakingToken = _stakingToken;
136             lockingBoostMultiplerInBips = _lockingBoostMultiplerInBips;
137             rewardsDuration = _rewardsDuration;
138             lockDuration = _lockDuration;
139     
140             // kocks are combined into the same `rewardsDuration` epoch. So, if
141             // a user stake with locking every `rewardsDuration` this should reach the
142             // maximum number of possible simultaneous because the first lock gets expired,
143             // freeing up a slot.
144             maxLocks = _lockDuration / _rewardsDuration;
145         }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L112:145





## [G-11] Use the inputs/results of assignments rather than re-reading state variables
When a state variable is assigned, it saves gas to use the value being assigned, later in the function, rather than re-reading the state variable itself. If needed, it can also be stored to a local variable, and be used in that way. Both options avoid a Gwarmaccess (100 gas). Note that if the operation is, say +=, the assignment also results in a value which can be used. The instances below point to the first reference after the assignment, since later references are already covered by issues describing the caching of state variable values.

```solidity
File: src/blast/BlastOnboardingBoot.sol
103             MIM.safeApprove(address(router), type(uint256).max);

104             USDB.safeApprove(address(router), type(uint256).max);

117             staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));

122             pool.safeApprove(address(staking), totalPoolShares);

122             pool.safeApprove(address(staking), totalPoolShares);

122             pool.safeApprove(address(staking), totalPoolShares);

124             emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

126             return (pool, address(staking), totalPoolShares);

148             emit LogReadyChanged(ready);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148:148

```solidity
File: src/blast/BlastWrappers.sol
67              BlastYields.configureDefaultClaimables(_governor);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L67:67


```solidity
File: src/mimswap/MagicLP.sol
141                 _BASE_TARGET_ = _BASE_RESERVE_;

142                 _QUOTE_TARGET_ = _QUOTE_RESERVE_;

146                 _BASE_TARGET_ = _BASE_RESERVE_;

147                 _QUOTE_TARGET_ = _QUOTE_RESERVE_;

144             if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

144             if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

309                 uint256 quoteInput = quoteBalance - uint256(_QUOTE_RESERVE_);

315                 if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {

325                 emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

325                 emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

331                 uint256 baseInput = baseBalance - uint256(_BASE_RESERVE_);

337                 if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {

347                 emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

342                 if (_RState_ != uint32(newRState)) {

381                 shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;

381                 shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;

383                 _QUOTE_TARGET_ = DecimalMath.mulFloor(shares, _I_).toUint112();

402                 _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

402                 _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

402                 _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();

403                 _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();

403                 _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();

385                 if (_QUOTE_TARGET_ == 0) {

438             _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));

438             _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));

513                 _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));

517                 _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517:517

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol
39              return IFeeRateImpl(implementation).getFeeRate(msg.sender, trader, lpFeeRate);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L39:39

```solidity
File: src/mimswap/periphery/Factory.sol
86              IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L86:86

```solidity
File: src/mimswap/periphery/Router.sol
88              clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);

203             if (token == address(weth)) {

237             if (token == address(weth)) {

285             if (token == address(weth)) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L285:285




## [G‑12] State variables that are used multiple times in a function should be cached in stack variables

When performing multiple operations on a state variable in a function, it is recommended to cache it first. Either multiple reads or multiple writes to a state variable can save gas by caching it on the stack. Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses. Saves 100 gas per instance.



```solidity
File:  src/blast/BlastMagicLP.sol
// @audit `_BASE_TOKEN_` is State variable should be cached in stack variables
56      if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
            token0Amount = BlastYields.claimAllTokenYields(_BASE_TOKEN_, feeTo_);
        }

// @audit `_QUOTE_TOKEN_` is State variable should be cached in stack variables
59      if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
            token1Amount = BlastYields.claimAllTokenYields(_QUOTE_TOKEN_, feeTo_);
        }            
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L56


```solidity
File:  src/mimswap/MagicLP.sol
// @audit `_BASE_RESERVE_` and `_QUOTE_RESERVE_` are State variables should be cached in stack variables to save gas
138  function correctRState() external {
        if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
            _RState_ = uint32(PMMPricing.RState.ONE);
            _BASE_TARGET_ = _BASE_RESERVE_;
            _QUOTE_TARGET_ = _QUOTE_RESERVE_;
        }
        if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
            _RState_ = uint32(PMMPricing.RState.ONE);
            _BASE_TARGET_ = _BASE_RESERVE_;
            _QUOTE_TARGET_ = _QUOTE_RESERVE_;
        }
    }

// @audit `_BASE_TOKEN_` is State variable should be cached in stack variables
285     _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);

        emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L138-L148


```solidity
File: src/mimswap/MagicLP.sol
// @audit `_QUOTE_RESERVE_` and `_BASE_RESERVE_` are State variables should be cached in stack variables to save gas
290 function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
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
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290-L353


```solidity
File:  src/mimswap/periphery/Factory.sol
// @audit `maintainerFeeRateModel` is State variable should be cached in stack variables
86     IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);

        emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L86-L88


## [G-13] Use nested if statements instead of &&

If the if statement has a logical AND and is not followed by an else statement, it can be replaced with 2 if statements.





```solidity
File:  src/blast/BlastMagicLP.sol
119  if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119


```solidity
File:  src/blast/BlastOnboarding.sol
114  if (caps[token] > 0 && totals[token].total > caps[token]) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114


```solidity
File:  src/mimswap/MagicLP.sol
139  if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {

144  if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

302  if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {

549  if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {            
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139


```solidity
File:  src/mimswap/periphery/Router.sol
527  if (quoteReserve > 0 && baseReserve > 0) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527


```solidity
File:  src/staking/LockingMultiRewards.sol
326  if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

417  if (index == lastLockIndex[user] && locks.length > 1) {    
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326




## [G-14] Use assembly to emit events


There are 57 instances of this issue:

```solidity
File: src/blast/BlastBox.sol
78              emit LogFeeToChanged(feeTo_);

90              emit LogTokenDepositEnabled(token, enabled);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L90:90

```solidity
File: src/blast/BlastGovernor.sol
46              emit LogFeeToChanged(_feeTo);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L46:46

```solidity
File: src/blast/BlastMagicLP.sol
86              emit LogFeeToChanged(feeTo_);

91              emit LogOperatorChanged(operator, status);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L91:91

```solidity
File: src/blast/BlastOnboarding.sol
120             emit LogDeposit(msg.sender, token, amount, lock_);

129             emit LogLock(msg.sender, token, amount);

140             emit LogWithdraw(msg.sender, token, amount);

153             emit LogFeeToChanged(feeTo_);

182             emit LogTokenSupported(token, supported);

187             emit LogTokenCapChanged(token, cap);

192             emit LogBootstrapperChanged(bootstrapper_);

197             emit LogStateChange(State.Opened);

202             emit LogStateChange(State.Closed);

211             emit LogTokenRescue(token, to, amount);
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L211:211

```solidity
File: src/blast/BlastOnboardingBoot.sol
71              emit LogClaimed(msg.sender, shares, lock);

124             emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

132             emit LogInitialized(_router);

143             emit LogStakingChanged(address(_staking));

148             emit LogReadyChanged(ready);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148:148

```solidity
File: src/blast/BlastTokenRegistry.sol
20              emit LogNativeYieldTokenEnabled(token, enabled);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L20:20

```solidity
File: src/blast/libraries/BlastYields.sol
26              emit LogBlastTokenClaimableEnabled(address(this), token);

31              emit LogBlastNativeClaimableEnabled(address(this));

44              emit LogBlastGasClaimed(recipient, amount);

57              emit LogBlastETHClaimed(recipient, amount);

62              emit LogBlastETHClaimed(recipient, amount);

72              emit LogBlastTokenClaimed(recipient, address(token), amount);

77              emit LogBlastTokenClaimed(recipient, address(token), amount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L77:77


```solidity
File: src/mimswap/MagicLP.sol
259                 emit RChange(newRState);

264             emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

282                 emit RChange(newRState);

287             emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

323                     emit RChange(newRState);

325                 emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);

345                     emit RChange(newRState);

347                 emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);

352             emit FlashLoan(msg.sender, assetTo, baseAmount, quoteAmount);

409             emit BuyShares(to, shares, balanceOf(to));

454             emit SellShares(msg.sender, to, shareAmount, balanceOf(msg.sender));

467             emit TokenRescue(token, to, amount);

501             emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L501:501



```solidity
File: src/mimswap/periphery/Factory.sol
88              emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);

102             emit LogSetImplementation(implementation_);

111             emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);

141             emit LogPoolRemoved(pool);

152             emit LogPoolAdded(baseToken, quoteToken, creator, pool);
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L152:152

```solidity
File: src/staking/LockingMultiRewards.sol
183             emit LogWithdrawn(msg.sender, amount);

318             emit LogSetMinLockAmount(minLockAmount, _minLockAmount);

331             emit LogRecovered(tokenAddress, tokenAmount);

392             emit LogRewardAdded(amount);

436             emit LogLockIndexChanged(user, lastIndex, index);

447                 emit LogUnlocked(user, amount, index);

475                 emit LogStaked(account, amount);

513             emit LogLocked(user, amount, _nextUnlockTime, lockCount);

611                 emit LogRewardLockCreated(user, _rewardLock.unlockTime);

638                             emit LogRewardPaid(user, rewardToken, amount);

651                 emit LogRewardLocked(user, rewardToken, rewardAmount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L651:651



## [G-15] Instead of counting down in for statements, count up

Counting down is more gas efficient than counting up because neither we are making zero variable to non-zero variable and also we will get gas refund in the last transaction when making non-zero to zero variable.

```solidity
File:  src/blast/BlastOnboarding.sol
165  for (uint256 i = 0; i < tokens.length; i++) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165



```solidity
File:  src/mimswap/periphery/Router.sol
544  for (uint256 i = 0; i < iterations; ) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544


```solidity
File:  src/staking/LockingMultiRewards.sol
504 for (uint256 i; i < users.length; ) {

547 for (uint256 i; i < rewardTokens.length; ) {

561 for (uint256 i; i < rewardTokens.length; ) {

575 for (uint256 i; i < rewardTokens.length; ) {

580 for (uint256 j; j < users.length; ) {

614 for (uint256 i; i < rewardTokens.length; ) {                    
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L504



## [G-16] Move storage pointer to top of function to avoid offset calculation

We can avoid unnecessary offset calculations by moving the storage pointer to the top of the function.

```solidity
File:  src/staking/LockingMultiRewards.sol
369  Reward storage reward = _rewardData[rewardToken];
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L369


## [G-17] Consider using OZ EnumerateSet in place of nested mappings 

Nested mappings and multi-dimensional arrays in Solidity operate through a process of double hashing, wherein the original storage slot and the first key are concatenated and hashed, and then this hash is again concatenated with the second key and hashed. This process can be quite gas expensive due to the double-hashing operation and subsequent storage operation (sstore).
A possible optimization involves manually concatenating the keys followed by a single hash operation and an sstore. However, this technique introduces the risk of storage collision, especially when there are other nested hash maps in the contract that use the same key types. Because Solidity is unaware of the number and structure of nested hash maps in a contract, it follows a conservative approach in computing the storage slot to avoid possible collisions.


```solidity
File:  src/blast/BlastOnboarding.sol
41  mapping(address user => mapping(address token => Balances)) public balances;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L41


```solidity
File:  src/mimswap/periphery/Factory.sol
35   mapping(address base => mapping(address quote => address[] pools)) public pools;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L35


```solidity
File:  src/staking/LockingMultiRewards.sol
94    mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
95    mapping(address user => mapping(address token => uint256 amount)) public rewards;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L94-L95



## [G-18] Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct, where appropriate

Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (20000 gas) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save ~42 gas per access due to not having to recalculate the key's keccak256 hash (Gkeccak256 - 30 gas) and that calculation's associated stack operations.

There are 3 instances of this issue:
```solidity
File: src/blast/BlastOnboarding.sol
37          mapping(address token => Balances) public totals;
38          mapping(address token => uint256 cap) public caps;
39      
40          // Per-user
41          mapping(address user => mapping(address token => Balances)) public balances;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L37-L41


```solidity
File: src/mimswap/periphery/Factory.sol
35          mapping(address base => mapping(address quote => address[] pools)) public pools;
36          mapping(address creator => address[] pools) public userPools;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L35-L36

```solidity
File: src/staking/LockingMultiRewards.sol
89          mapping(address token => Reward info) private _rewardData;
90          mapping(address user => Balances balances) private _balances;
91          mapping(address user => LockedBalance[] locks) private _userLocks;
92          mapping(address user => RewardLock rewardLock) private _userRewardLock;
93      
94          mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
95          mapping(address user => mapping(address token => uint256 amount)) public rewards;
96          mapping(address user => uint256 index) public lastLockIndex;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L89-L96




## [G-19] Use calldata instead of memory for function arguments that do not get mutated

Mark data types as calldata instead of memory where possible. This makes it so that Mark data types as `calldata` instead of `memory` where possible. This makes it so that the data is not automatically loaded into memory. If the data passed into the function does not need to be changed (like updating values in an array), it can be passed in as `calldata`. The one exception to this is if the argument must later be passed into another function that takes an argument that specifies `memory` storage..

```solidity
File:  src/blast/BlastOnboarding.sol
164  function claimTokenYields(address[] memory tokens) external onlyOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164


```solidity
File:  src/staking/LockingMultiRewards.sol
397  function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397


## [G‑20] Unlimited gas consumption risk due to external call recipients

When calling an external function without specifying a gas limit , the called contract may consume all the remaining gas, causing the tx to be reverted. To mitigate this, it is recommended to explicitly set a gas limit when making low level external calls.

```solidity
File:  src/blast/BlastGovernor.sol
54  (success, result) = to.call{value: value}(data);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L54


## [G‑21] Same cast is done multiple times
It's cheaper to do it once, and store the result to a variable. The examples below are the second+ instance of a given cast of the variable.

```solidity
File:  src/blast/BlastOnboardingBoot.sol
103        MIM.safeApprove(address(router), type(uint256).max);
           USDB.safeApprove(address(router), type(uint256).max);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L103-L104

- `address(staking)`
```solidity
File:  src/blast/BlastOnboardingBoot.sol
        pool.safeApprove(address(staking), totalPoolShares);

        emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

        return (pool, address(staking), totalPoolShares);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L122-L126

## [G‑22] Using constants instead of enum can save gas


```solidity
File:  src/blast/BlastOnboarding.sol
18  enum State {
        Idle,
        Opened,
        Closed
    }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L18-L22


```solidity
File:  src/mimswap/libraries/PMMPricing.sol
21  enum RState {
        ONE,
        ABOVE_ONE,
        BELOW_ONE
    }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L21-L25




## [G-23] Use assembly to calculate hashes to save gas
Using assembly to calculate hashes can save 80 gas per instance

```solidity
File: src/mimswap/periphery/Factory.sol
163             return keccak256(abi.encodePacked(sender_, implementation, baseToken_, quoteToken_, lpFeeRate_, i_, k_));
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L163:163



## [G-24] Unused named return variables without optimizer waste gas

Consider changing the variable to be an unnamed one, since the variable is never assigned, nor is it returned by name. If the optimizer is not turned on, leaving the code as it is will also waste gas for the stack variable.

```solidity
File: src/blast/BlastOnboardingBoot.sol
78      function claimable(address user) external view returns (uint256 shares) {

86      function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {

155     function _claimable(address user) internal view returns (uint256 shares) {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L155:155

```solidity
File: src/blast/libraries/BlastYields.sol
51          function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L51:51

```solidity
File: src/mimswap/MagicLP.sol
215         function getMidPrice() public view returns (uint256 midPrice) {

224         function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {

228         function getBaseInput() public view returns (uint256 input) {

232         function getQuoteInput() public view returns (uint256 input) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L232:232

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol
34          function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34:34


```solidity
File: src/mimswap/periphery/Router.sol
185         ) external ensureDeadline(deadline) returns (uint256 shares) {

235         ) external payable ensureDeadline(deadline) returns (uint256 shares) {

268         ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {

321         ) external ensureDeadline(deadline) returns (uint256 amountOut) {

342         ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

410         ) external ensureDeadline(deadline) returns (uint256 amountOut) {

420         ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {

455         ) external ensureDeadline(deadline) returns (uint256 amountOut) {

466         ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L466:466



## [G-25] Emit Used In Loop:
Emitting an event inside a loop performs a LOG op N times, where N is the loop length. Consider refactoring the code to emit the event only once at the end of loop. Gas savings should be multiplied by the average loop length.

```solidity
File: src/staking/LockingMultiRewards.sol
436    emit LogLockIndexChanged(user, lastIndex, index);

447    emit LogUnlocked(user, amount, index);

638    emit LogRewardPaid(user, rewardToken, amount);

651    emit LogRewardLocked(user, rewardToken, rewardAmount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L651:651









## [G-26] Structs can be modified to fit in fewer storage slots

Some member types can be safely modified, and as result, these struct will fit in fewer storage slots. Each slot saved can avoid an extra Gsset (20000 gas) for the first setting of the struct. Subsequent reads as well as writes have smaller gas savings.

```solidity
File:  src/blast/BlastOnboarding.sol
24  struct Balances {
        uint256 unlocked;
        uint256 locked;
        uint256 total;
    }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L24-L28


```solidity
File:  src/mimswap/libraries/PMMPricing.sol
27  struct PMMState {
        uint256 i;
        uint256 K;
        uint256 B;
        uint256 Q;
        uint256 B0;
        uint256 Q0;
        RState R;
    }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L27-L35


## [G‑27] Use assembly to validate msg.sender

We can use assembly to efficiently validate msg.sender with the least amount of opcodes necessary. 

```solidity
File:  src/mimswap/MagicLP.sol
608   if (msg.sender != implementation.owner()) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L608



## [G-28] State variable read in a loop:

The state variable should be cached in and read from a local variable, or accumulated in a local variable then written to storage once outside of the loop, rather than reading/updating it on every iteration of the loop, which will replace each Gwarmaccess (100 gas) with a much cheaper stack read.

```solidity
File: src/staking/LockingMultiRewards.sol
547             for (uint256 i; i < rewardTokens.length; ) {

561             for (uint256 i; i < rewardTokens.length; ) {

575             for (uint256 i; i < rewardTokens.length; ) {

614             for (uint256 i; i < rewardTokens.length; ) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.


## [G-29] Initializers can be marked payable:

Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn't provided. An initializer can safely be marked as payable, since only the deployer would be able to pass funds, and the project itself would not pass any funds.

```solidity
File: src/blast/BlastOnboardingBoot.sol
129         function initialize(Router _router) external onlyOwner {
130             router = Router(payable(_router));
131             factory = IFactory(router.factory());
132             emit LogInitialized(_router);
133         }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129:133sol#L614:614





## [G-30] Usage of `uints`/`ints` smaller than 32 bytes (256 bits) incurs overhead

When using elements that are smaller than 32 bytes, your contract’s gas usage may be higher. This is because the EVM operates on 32 bytes at a time. Therefore, if the element is smaller than that, the EVM must use more operations in order to reduce the size of the element from 32 bytes to the desired size.https://docs.soliditylang.org/en/v0.8.11/internals/layout_in_storage.htmlEach operation involving a `uint8` costs an extra [**22-28 gas**](https://gist.github.com/IllIllI000/9388d20c70f9a4632eb3ca7836f54977) (depending on whether the other operand is also a variable of type `uint8`) as compared to ones involving `uint256`, due to the compiler having to clear the higher bits of the memory word before operating on the `uint8`, as well as the associated stack operations of doing so. Use a larger size then downcast where needed.

```solidity
File: src/mimswap/MagicLP.sol
546             uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);

547             uint32 timeElapsed = blockTimestamp - _BLOCK_TIMESTAMP_LAST_;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L547:547



## [G-31] Stack variable used as a cheaper cache for a state variable is only used once

If the variable is only accessed once, it's cheaper to use the state variable directly that one time, and save the 3 gas the extra stack assignment would spend.

```solidity
File: src/mimswap/MagicLP.sol
// @audit `baseBalance` and `quoteBalance` only used once
435             baseAmount = (baseBalance * shareAmount) / totalShares;

436             quoteAmount = (quoteBalance * shareAmount) / totalShares;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L436:436




## [G-32] Use local variables for emitting

Use the function/modifier's local copy of the state variable, rather than incurring an extra Gwarmaccess (100 gas). In the unlikely event that the state variable hasn't already been used by the function/modifier, consider whether it is really necessary to include it in the event, given the fact that it incurs a Gcoldsload (2100 gas), or whether it can be passed in to or back out of the functions that do use it

```solidity
File: src/blast/BlastOnboardingBoot.sol
124             emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);

148             emit LogReadyChanged(ready);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148:148


```solidity
File: src/mimswap/periphery/Factory.sol
88              emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88:88

```solidity
File: src/staking/LockingMultiRewards.sol
318             emit LogSetMinLockAmount(minLockAmount, _minLockAmount);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L318:318





## [G-33] State variables can be packed into fewer storage slots
If variables occupying the same slot are both written in the same function or by the constructor, avoids a separate Gsset (20000 gas). Reads of the variables can also be cheaper

```solidity
File: src/blast/BlastOnboardingBoot.sol
23      contract BlastOnboardingBootDataV1 is BlastOnboardingData {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23:23

```solidity
File: src/mimswap/MagicLP.sol
25      contract MagicLP is ERC20, ReentrancyGuard, Owned {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L25:25

## [G-34] Storage re-read via storage pointer

The instances below point to the second+ access of a state variable, via a storage pointer, within a function. Caching the value replaces each Gwarmaccess (100 gas) with a much cheaper stack read.


```solidity
File: src/staking/LockingMultiRewards.sol
241             return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);

380              amount += _remainingRewardTime * reward.rewardRate;

427              uint256 lastIndex = locks.length - 1;

605              uint256 rewardItemLength = _rewardLock.items.length;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L605:605




## [G-35] Sort Solidity operations using short-circuit mode

Short-circuiting is a solidity contract development model that uses OR/AND logic to sequence different cost operations. It puts low gas cost operations in the front and high gas cost operations in the back, so that if the front is low If the cost operation is feasible, you can skip (short-circuit) the subsequent high-cost Ethereum virtual machine operation.



- BlastMagicLP is external call
```solidity
File:  src/blast/BlastMagicLP.sol
119  if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119




## [G-37] Internal functions only called once can be inlined to save gas
Not inlining costs 20 to 40 gas because of two extra JUMP instructions and additional stack operations needed for function calls.

```solidity
File: src/mimswap/MagicLP.sol
528         function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L528:528


```solidity
File: src/staking/LockingMultiRewards.sol
544         function _updateRewards() internal {

572         function _updateRewardsForUsers(address[] memory users) internal {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L572:572



## [G-37] Use constants instead of type(uintx).max
Using constants instead of type(uintx).max can save gas in some cases because constants are precomputed at compile-time and can be reused throughout the code, whereas type(uintx).max requires computation at runtime


```solidity
File: src/blast/BlastOnboardingBoot.sol
103             MIM.safeApprove(address(router), type(uint256).max);

104             USDB.safeApprove(address(router), type(uint256).max);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L103


```solidity
File:  src/mimswap/MagicLP.sol
508  if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {

532  if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {    
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508



