### Low Risk Issues


# SUMMARY
|      |  issue  |  instance  |
|------|---------|------------|
|[L-01]|`_setupRole` is Deprecated:|6|
|[L-02]|Missing checks for `address(0x0)` when assigning values to address state variables:|2|
|[L-03]|Unsafe downcast:|7|
|[L-04]|Array does not have a `pop` function:|5|
|[L-05]|Approve `type(uint256).max` may not work with some tokens:|2|
|[L-06]|Setters should have initial value check:|19|
|[L-07]|Empty `receive()`/`payable fallback()` function does not authorize requests:|2|
|[L-08]|Contracts are designed to receive ETH but do not implement function for withdrawal:|2|
|[L-09]|latestAnswer() is deprecated:|1|
|[L-10]|Int casting `block.timestamp` can reduce the lifespan of a contract:|1|
|[L-11]|Contract inherits Pausable but does not expose pausing/unpausing functionality:|1|
|[L-12]| No limits when setting state variable amounts:|21|
|[L-13]| Pausing withdrawals is unfair to the users:|1|
|[L-14]|Allowed fees/rates should be capped by smart contracts:|6|
|[L-15]|Owner can renounce ownership while system is paused:|2|
|[L-16]|Constructor contains no validation:|2|
|[L-17]|For loops in `public` or `external` functions should be avoided due to high gas costs and possible DOS:|2|
|[L-18]|Function calls within for loops:|4|
|[L-19]|External calls in an unbounded for-loop may result in a DoS:|3|
|[L-20]|Multiplication on the result of a division:|4|
|[L-21]|Governance functions should be controlled by time locks:|35|
|[L-22]|Code does not follow the best practice of check-effects-interaction:|4|
|[L-23]|The additions/multiplications may silently overflow because they're in unchecked blocks with no preceding value checks, which may lead to unexpected results.:|1|
|[L-24]|Unbounded state array which is iterated upon:|14|
|[L-25]|Prefer continue over revert model in iteration:|2|
|[L-26]|Contracts use infinite approvals with no means to revoke:|1|
|[L-27]|External calls in modifiers should be avoided:|1|

## [L-01] - `_setupRole` is Deprecated:
`_setupRole` is deprecated in favor of `grantRole` and `renounceRole`.

There are 6 instances of this issue:

```solidity
File: src/blast/BlastOnboardingBoot.sol
MIM.safeApprove(address(router), type(uint256).max);

USDB.safeApprove(address(router), type(uint256).max);

pool.safeApprove(address(staking), totalPoolShares);

MIM.safeApprove(address(router), type(uint256).max);

USDB.safeApprove(address(router), type(uint256).max);

pool.safeApprove(address(staking), totalPoolShares);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L122:122



## [L-02] - Missing checks for `address(0x0)` when assigning values to address state variables:
This issue arises when an address state variable is assigned a value without a preceding check to ensure it isn't address(0x0). This can lead to unexpected behavior as address(0x0) often represents an uninitialized address.


There are 2 instances of this issue:

```solidity
File: src/blast/BlastOnboarding.sol
191             bootstrapper = bootstrapper_;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L191:191


```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol
58              implementation = implementation_;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L58:58


## [L-03] - Unsafe downcast:

When a type is downcast to a smaller type, the higher order bits are truncated, effectively applying a modulo to the original value. Without any other checks, this wrapping will lead to unexpected behavior and bugs.


There are 7 instances of this issue


```solidity
File: src/mimswap/MagicLP.sol
438             _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));

125             _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

495             _I_ = uint128(newI);

494             _K_ = uint64(newK);

439             _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));

493             _LP_FEE_RATE_ = uint64(newLpFeeRate);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L493:493

```solidity
File: src/staking/LockingMultiRewards.sol
389             reward.lastUpdateTime = uint248(block.timestamp);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L389:389


## [L-04] - Array does not have a `pop` function:

Arrays without the pop operation in Solidity can lead to inefficient memory management and increase the likelihood of out-of-gas errors.


There are 5 instances of this issue

```solidity
File: src/mimswap/periphery/Factory.sol
149             pools[baseToken][quoteToken].push(pool);

150             userPools[creator].push(pool);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L150:150

```solidity
File: src/staking/LockingMultiRewards.sol
313             rewardTokens.push(rewardToken);

501                 _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));

648                     _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L648:648


## [L-05] - Approve `type(uint256).max` may not work with some tokens:

Source: https://github.com/d-xo/weird-erc20#revert-on-large-approvals--transfers

There are 2 instances of this issue

```solidity
File: src/blast/BlastOnboardingBoot.sol
103             MIM.safeApprove(address(router), type(uint256).max);

104             USDB.safeApprove(address(router), type(uint256).max);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L104:104


## [L-06] - Setters should have initial value check:

Setters should have initial value check to prevent assigning wrong value to the variable. Assginment of wrong value can lead to unexpected behavior of the contract.

There are 19 instances of this issue

```solidity
File: src/blast/BlastBox.sol
72          function setFeeTo(address feeTo_) external onlyOwner {
73              if (feeTo_ == address(0)) {
74                  revert ErrZeroAddress();
75              }
76      
77              feeTo = feeTo_;
78              emit LogFeeToChanged(feeTo_);
79          }


81          function setTokenEnabled(address token, bool enabled) external onlyOwner {
82              enabledTokens[token] = enabled;
83      
84              // enable native yields if token is recognized
85              // no matter if it's enabled or not
86              if (registry.nativeYieldTokens(token)) {
87                  BlastYields.enableTokenClaimable(token);
88              }
89      
90              emit LogTokenDepositEnabled(token, enabled);
91          }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81:91

```solidity
File: src/blast/BlastGovernor.sol
40          function setFeeTo(address _feeTo) external onlyOwner {
41              if(_feeTo == address(0)) {
42                  revert ErrZeroAddress();
43              }
44              
45              feeTo = _feeTo;
46              emit LogFeeToChanged(_feeTo);
47          }
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40:47

```solidity
File: src/blast/BlastMagicLP.sol
80          function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
81              if (feeTo_ == address(0)) {
82                  revert ErrZeroAddress();
83              }
84      
85              feeTo = feeTo_;
86              emit LogFeeToChanged(feeTo_);
87          }


89          function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
90              operators[operator] = status;
91              emit LogOperatorChanged(operator, status);
92          }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89:92

```solidity
File: src/blast/BlastOnboarding.sol
147         function setFeeTo(address feeTo_) external onlyOwner {
148             if (feeTo_ == address(0)) {
149                 revert ErrZeroAddress();
150             }
151     
152             feeTo = feeTo_;
153             emit LogFeeToChanged(feeTo_);
154         }


175         function setTokenSupported(address token, bool supported) external onlyOwner {
176             supportedTokens[token] = supported;
177     
178             if (registry.nativeYieldTokens(token)) {
179                 BlastYields.enableTokenClaimable(token);
180             }
181     
182             emit LogTokenSupported(token, supported);
183         }


185         function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
186             caps[token] = cap;
187             emit LogTokenCapChanged(token, cap);
188         }


190         function setBootstrapper(address bootstrapper_) external onlyOwner {
191             bootstrapper = bootstrapper_;
192             emit LogBootstrapperChanged(bootstrapper_);
193         }


```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190:193

```solidity
File: src/blast/BlastOnboardingBoot.sol

137         function setStaking(LockingMultiRewards _staking) external onlyOwner {
138             if (ready) {
139                 revert ErrCannotChangeOnceReady();
140             }
141     
142             staking = _staking;
143             emit LogStakingChanged(address(_staking));
144         }


146         function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
147             ready = _ready;
148             emit LogReadyChanged(ready);
149         }


```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146:149

```solidity
File: src/blast/BlastTokenRegistry.sol

14          function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
15              if (token == address(0)) {
16                  revert ErrZeroAddress();
17              }
18      
19              nativeYieldTokens[token] = enabled;
20              emit LogNativeYieldTokenEnabled(token, enabled);
21          }


```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14:21


```solidity
File: src/mimswap/MagicLP.sol


470         function setParameters(
471             address assetTo,
472             uint256 newLpFeeRate,
473             uint256 newI,
474             uint256 newK,
475             uint256 baseOutAmount,
476             uint256 quoteOutAmount,
477             uint256 minBaseReserve,
478             uint256 minQuoteReserve
479         ) public nonReentrant onlyImplementationOwner {
480             if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
481                 revert ErrReserveAmountNotEnough();
482             }
483             if (newI == 0 || newI > MAX_I) {
484                 revert ErrInvalidI();
485             }
486             if (newK > MAX_K) {
487                 revert ErrInvalidK();
488             }
489             if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {
490                 revert ErrInvalidLPFeeRate();
491             }
492     
493             _LP_FEE_RATE_ = uint64(newLpFeeRate);
494             _K_ = uint64(newK);
495             _I_ = uint128(newI);
496     
497             _transferBaseOut(assetTo, baseOutAmount);
498             _transferQuoteOut(assetTo, quoteOutAmount);
499             (uint256 newBaseBalance, uint256 newQuoteBalance) = _resetTargetAndReserve();
500     
501             emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);
502         }


560         function _setReserve(uint256 baseReserve, uint256 quoteReserve) internal {
561             _BASE_RESERVE_ = baseReserve.toUint112();
562             _QUOTE_RESERVE_ = quoteReserve.toUint112();
563     
564             _twapUpdate();
565         }


```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L560:565

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol


46          function setMaintainer(address maintainer_) external onlyOwner {
47              if (maintainer_ == address(0)) {
48                  revert ErrZeroAddress();
49              }
50      
51              maintainer = maintainer_;
52              emit LogMaintainerChanged(maintainer_);
53          }


57          function setImplementation(address implementation_) public onlyOwner {
58              implementation = implementation_;
59              emit LogImplementationChanged(implementation_);
60          }


```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57:60

```solidity
File: src/mimswap/periphery/Factory.sol


96          function setLpImplementation(address implementation_) external onlyOwner {
97              if (implementation_ == address(0)) {
98                  revert ErrZeroAddress();
99              }
100     
101             implementation = implementation_;
102             emit LogSetImplementation(implementation_);
103         }


105         function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
106             if (address(maintainerFeeRateModel_) == address(0)) {
107                 revert ErrZeroAddress();
108             }
109     
110             maintainerFeeRateModel = maintainerFeeRateModel_;
111             emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);
112         }


```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105:112


```solidity
File: src/staking/LockingMultiRewards.sol


317         function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
318             emit LogSetMinLockAmount(minLockAmount, _minLockAmount);
319             minLockAmount = _minLockAmount;
320         }


```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317:320




## [L-07] - Empty `receive()`/`payable fallback()` function does not authorize requests:

If the intention is for the Ether to be used, the function should call another function, otherwise it should revert (e.g. `require(msg.sender == address(weth))`). Having no access control on the function means that someone may send Ether to the contract, and have no way to get anything back out, which is a loss of funds. If the concern is having to spend a small amount of gas to check the sender against an immutable address, the code should at least have a function to rescue unused Ether.

There are 2 instances of this issue


```solidity
File: src/blast/BlastGovernor.sol
13          receive() external payable {}
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L13:13

```solidity
File: src/mimswap/periphery/Router.sol
36          receive() external payable {}
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L36:36

## [L-08] - Contracts are designed to receive ETH but do not implement function for withdrawal:
The following contracts can receive ETH but can not withdraw, ETH is occasionally sent by users will be stuck in those contracts. This functionality also applies to baseTokens resulting in locked tokens and loss of funds.
There are 2 instances of this issue
```solidity
File: src/blast/BlastGovernor.sol
13          receive() external payable {}
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L13:13

```solidity
File: src/mimswap/periphery/Router.sol
36          receive() external payable {}
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L36:36



## [L-09] - latestAnswer() is deprecated:

Use latestRoundData() instead so that you can tell whether the answer is stale or not. The latestAnswer() function returns zero if it is unable to fetch data, which may be the case if ChainLink stops supporting this API. The API and its deprecation message no longer even appear on the ChainLink website, so it is dangerous to continue using it.


There are 1 instances of this issue


```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

function latestAnswer() public view override returns (int256) {

uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));

uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));

return (0, latestAnswer(), 0, 0, 0);

```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L49



## [L-10] - Int casting `block.timestamp` can reduce the lifespan of a contract:

Consider removing casting to ensure future functionality.

```solidity
File: src/staking/LockingMultiRewards.sol
389             reward.lastUpdateTime = uint248(block.timestamp);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L389:389



## [L-11] - Contract inherits Pausable but does not expose pausing/unpausing functionality:

When a contract inherits from the Pausable contract in Solidity, it gains the ability to pause and resume certain actions, which can be crucial in mitigating potential risks or issues. However, the _pause and _unpause functions are internal and can only be called from within the contract or derived contracts. If the functionality to pause and unpause isn't exposed through public or external functions, it can't be called by the contract owner or designated pauser account. To take advantage of the Pausable contract, create public or external functions that call _pause and _unpause.


```solidity
File: src/blast/BlastOnboarding.sol
12      contract BlastOnboardingData is Owned, Pausable {
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L12:12

## [L-12] - No limits when setting state variable amounts:

It is important to ensure state variables numbers are set to a reasonable value.


```solidity
File: src/mimswap/MagicLP.sol
125             _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

140                 _RState_ = uint32(PMMPricing.RState.ONE);

142                 _QUOTE_TARGET_ = _QUOTE_RESERVE_;

145                 _RState_ = uint32(PMMPricing.RState.ONE);

194             state.i = _I_;

195             state.K = _K_;

196             state.B = _BASE_RESERVE_;

197             state.Q = _QUOTE_RESERVE_;

198             state.B0 = _BASE_TARGET_; // will be calculated in adjustedTarget

199             state.Q0 = _QUOTE_TARGET_;

212             R = uint256(state.R);

220             baseReserve = _BASE_RESERVE_;

221             quoteReserve = _QUOTE_RESERVE_;

258                 _RState_ = uint32(newRState);

281                 _RState_ = uint32(newRState);

322                     _RState_ = uint32(newRState);

344                     _RState_ = uint32(newRState);

493             _LP_FEE_RATE_ = uint64(newLpFeeRate);

494             _K_ = uint64(newK);

495             _I_ = uint128(newI);

540             _RState_ = uint32(PMMPricing.RState.ONE);

557             _BLOCK_TIMESTAMP_LAST_ = blockTimestamp;
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L557:557

```solidity
File: src/mimswap/libraries/Math.sol
31              y = x;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L31:31

```solidity
File: src/mimswap/periphery/Router.sol
155                     quoteAdjustedInAmount = quoteInAmount;

524                 baseAdjustedInAmount = shares;

531                         baseAdjustedInAmount = baseInAmount;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L531:531


## [L-13] - Pausing withdrawals is unfair to the users:
Users should always have the possibility of accessing their own funds, but when these functions are paused, their funds will be locked until the contracts are unpaused.


```solidity
File: src/blast/BlastOnboarding.sol
132         function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132:132

## [L-14] - Allowed fees/rates should be capped by smart contracts:

Fees/rates should be required to be below 100%, preferably at a much lower limit, to ensure users don't have to monitor the blockchain for changes prior to using the protocol.

```solidity
File: src/blast/BlastBox.sol
72          function setFeeTo(address feeTo_) external onlyOwner {
73              if (feeTo_ == address(0)) {
74                  revert ErrZeroAddress();
75              }
76      
77              feeTo = feeTo_;
78              emit LogFeeToChanged(feeTo_);
79          }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72:79

```solidity
File: src/blast/BlastGovernor.sol
40          function setFeeTo(address _feeTo) external onlyOwner {
41              if(_feeTo == address(0)) {
42                  revert ErrZeroAddress();
43              }
44              
45              feeTo = _feeTo;
46              emit LogFeeToChanged(_feeTo);
47          }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40:47

```solidity
File: src/blast/BlastMagicLP.sol
80          function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
81              if (feeTo_ == address(0)) {
82                  revert ErrZeroAddress();
83              }
84      
85              feeTo = feeTo_;
86              emit LogFeeToChanged(feeTo_);
87          }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80:87

```solidity
File: src/blast/BlastOnboarding.sol
147         function setFeeTo(address feeTo_) external onlyOwner {
148             if (feeTo_ == address(0)) {
149                 revert ErrZeroAddress();
150             }
151     
152             feeTo = feeTo_;
153             emit LogFeeToChanged(feeTo_);
154         }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147:154


```solidity
File: src/mimswap/periphery/Factory.sol
105         function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
106             if (address(maintainerFeeRateModel_) == address(0)) {
107                 revert ErrZeroAddress();
108             }
109     
110             maintainerFeeRateModel = maintainerFeeRateModel_;
111             emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);
112         }
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105:112



## [L-15] - Owner can renounce ownership while system is paused:

The contract owner is not prevented from renouncing the ownership while the contract is paused, which would cause any user assets stored in the protocol to be locked indefinitely.

```solidity
File: src/blast/BlastOnboarding.sol
214         function pause() external onlyOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L214:214

```solidity
File: src/staking/LockingMultiRewards.sol
337         function pause() external onlyOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337:337



## [L-16] - Constructor contains no validation:

In Solidity, when values are being assigned in constructors to unsigned or integer variables, it's crucial to ensure the provided values adhere to the protocol's specific operational boundaries as laid out in the project specifications and documentation. If the constructors lack appropriate validation checks, there's a risk of setting state variables with values that could cause unexpected and potentially detrimental behavior within the contract's operations, violating the intended logic of the protocol. This can compromise the contract's security and impact the maintainability and reliability of the system. In order to avoid such issues, it is recommended to incorporate rigorous validation checks in constructors. These checks should align with the project's defined rules and constraints, making use of Solidity's built-in require function to enforce these conditions. If the validation checks fail, the require function will cause the transaction to revert, ensuring the integrity and adherence to the protocol's expected behavior.


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


## [L-17] - For loops in `public` or `external` functions should be avoided due to high gas costs and possible DOS:

In Solidity, for loops can potentially cause Denial of Service (DoS) attacks if not handled carefully. DoS attacks can occur when an attacker intentionally exploits the gas cost of a function, causing it to run out of gas or making it too expensive for other users to call. Below are some scenarios where for loops can lead to DoS attacks: Nested for loops can become exceptionally gas expensive and should be used sparingly.

```solidity
File: src/blast/BlastOnboarding.sol

164         function claimTokenYields(address[] memory tokens) external onlyOwner {
165             for (uint256 i = 0; i < tokens.length; i++) {
166                 if (!supportedTokens[tokens[i]]) {
167                     revert ErrUnsupportedToken();
168                 }
169                 if (registry.nativeYieldTokens(tokens[i])) {
170                     BlastYields.claimAllTokenYields(tokens[i], feeTo);
171                 }
172             }
173         }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164:173


```solidity
File: src/staking/LockingMultiRewards.sol
397         function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
398             if (users.length != lockIndexes.length) {
399                 revert ErrLengthMismatch();
400             }
401     
402             _updateRewardsForUsers(users);
403     
404             // Release all expired users' locks
405             for (uint256 i; i < users.length; ) {
406                 address user = users[i];
407                 Balances storage bal = _balances[user];
408                 LockedBalance[] storage locks = _userLocks[user];
409     
410                 if (locks.length == 0) {
411                     revert ErrNoLocks();
412                 }
413     
414                 uint256 index = lockIndexes[i];
415     
416                 // Prevents processing `lastLockIndex` out of order
417                 if (index == lastLockIndex[user] && locks.length > 1) {
418                     revert ErrInvalidLockIndex();
419                 }
420     
421                 // prohibit releasing non-expired locks
422                 if (locks[index].unlockTime > block.timestamp) {
423                     revert ErrLockNotExpired();
424                 }
425     
426                 uint256 amount = locks[index].amount;
427                 uint256 lastIndex = locks.length - 1;
428     
429                 /// Last lock index changed place with the one we just swapped.
430                 if (lastLockIndex[user] == lastIndex) {
431                     lastLockIndex[user] = index;
432                 }
433     
434                 if (index != lastIndex) {
435                     locks[index] = locks[lastIndex];
436                     emit LogLockIndexChanged(user, lastIndex, index);
437                 }
438     
439                 locks.pop();
440     
441                 unlockedSupply += amount;
442                 lockedSupply -= amount;
443     
444                 bal.unlocked += amount;
445                 bal.locked -= amount;
446     
447                 emit LogUnlocked(user, amount, index);
448     
449                 unchecked {
450                     ++i;
451                 }
452             }
453         }


```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397:453


## [L-18] - Function calls within for loops:

Making function calls within loops in Solidity can lead to inefficient gas usage, potential bottlenecks, and increased vulnerability to attacks. Each function call or external call consumes gas, and when executed within a loop, the gas cost multiplies, potentially causing the transaction to run out of gas or exceed block gas limits. This can result in transaction failure or unpredictable behavior.

```solidity
File: src/staking/LockingMultiRewards.sol
580                 for (uint256 j; j < users.length; ) {
581                     address user = users[j];
582                     _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);
583     
584                     unchecked {
585                         ++j;
586                     }
587                 }


561             for (uint256 i; i < rewardTokens.length; ) {
562                 address token = rewardTokens[i];
563                 _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_));
564     
565                 unchecked {
566                     ++i;
567                 }
568             }


547             for (uint256 i; i < rewardTokens.length; ) {
548                 _updateRewardsGlobal(rewardTokens[i], totalSupply_);
549                 unchecked {
550                     ++i;
551                 }
552             }


575             for (uint256 i; i < rewardTokens.length; ) {
576                 address token = rewardTokens[i];
577                 uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);
578     
579                 // Record each user's rewards
580                 for (uint256 j; j < users.length; ) {
581                     address user = users[j];
582                     _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);
583     
584                     unchecked {
585                         ++j;
586                     }
587                 }
588     
589                 unchecked {
590                     ++i;
591                 }
592             }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575:592


## [L-19] - External calls in an unbounded for-loop may result in a DoS:

Consider limiting the number of iterations in for-loops that make external calls.


```solidity
File: src/blast/BlastOnboarding.sol
165             for (uint256 i = 0; i < tokens.length; i++) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165:165

```solidity
File: src/staking/LockingMultiRewards.sol
405             for (uint256 i; i < users.length; ) {

614             for (uint256 i; i < rewardTokens.length; ) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614:614


## [L-20] - Multiplication on the result of a division:

Dividing an integer by another integer will often result in loss of precision. When the result is multiplied by another number, the loss of precision is magnified, often to material magnitudes. (X / Z) * Y should be re-written as (X * Y) / Z.

```solidity
File: src/mimswap/libraries/Math.sol
99                  _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);

158                     temp = (((delta * V1) / V0) * i) / V0;

170             uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170:170

```solidity
File: src/staking/LockingMultiRewards.sol
258             return (block.timestamp / rewardsDuration) * rewardsDuration;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L258:258


## [L-21] - Governance functions should be controlled by time locks:

Governance functions (such as upgrading contracts, setting critical parameters) should be controlled using time locks to introduce a delay between a proposal and its execution. This gives users time to exit before a potentially dangerous or malicious operation is applied.


```solidity
File: src/blast/BlastBox.sol

81          function setTokenEnabled(address token, bool enabled) external onlyOwner {

68          function callBlastPrecompile(bytes calldata data) external onlyOwner {

72          function setFeeTo(address feeTo_) external onlyOwner {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72:79

```solidity
File: src/blast/BlastGovernor.sol
40          function setFeeTo(address _feeTo) external onlyOwner {

53          function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {

49          function callBlastPrecompile(bytes calldata data) external onlyOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L49:51

```solidity
File: src/blast/BlastOnboarding.sol
175         function setTokenSupported(address token, bool supported) external onlyOwner {

156         function callBlastPrecompile(bytes calldata data) external onlyOwner {

218         function unpause() external onlyOwner {

160         function claimGasYields() external onlyOwner returns (uint256) {

205         function rescue(address token, address to, uint256 amount) external onlyOwner {

147         function setFeeTo(address feeTo_) external onlyOwner {

214         function pause() external onlyOwner {

195         function open() external onlyOwner onlyState(State.Idle) {

200         function close() external onlyOwner onlyState(State.Opened) {

185         function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {

190         function setBootstrapper(address bootstrapper_) external onlyOwner {

164         function claimTokenYields(address[] memory tokens) external onlyOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164:173

```solidity
File: src/blast/BlastOnboardingBoot.sol
129         function initialize(Router _router) external onlyOwner {

96          function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {

137         function setStaking(LockingMultiRewards _staking) external onlyOwner {

146         function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146:149

```solidity
File: src/blast/BlastTokenRegistry.sol
14          function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14:21

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol
46          function setMaintainer(address maintainer_) external onlyOwner {

57          function setImplementation(address implementation_) public onlyOwner {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57:60

```solidity
File: src/mimswap/periphery/Factory.sol
105         function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {

120         function removePool(
121             address creator,
122             address baseToken,
123             address quoteToken,
124             uint256 poolIndex,
125             uint256 userPoolIndex
126         ) external onlyOwner {

96          function setLpImplementation(address implementation_) external onlyOwner {

116         function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L116:118

```solidity
File: src/staking/LockingMultiRewards.sol
337         function pause() external onlyOwner {

300         function addReward(address rewardToken) public onlyOwner {

317         function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {

324         function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {

341         function unpause() external onlyOwner {

```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L341:343


## [L-22] - Code does not follow the best practice of check-effects-interaction:

Code should follow the best-practice of [check-effects-interaction](https://blockchain-academy.hs-mittweida.de/courses/solidity-coding-beginners-to-intermediate/lessons/solidity-11-coding-patterns/topic/checks-effects-interactions/), where state variables are updated before any external calls are made. Doing so prevents a large class of reentrancy bugs.

```solidity
File: src/blast/BlastOnboarding.sol
/// @audit token.safeTransferFrom() called prior to this assignment
118             balances[msg.sender][token].total += amount;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L118:118

```solidity
File: src/mimswap/MagicLP.sol
/// @audit _BASE_TOKEN_.balanceOf() called prior to this assignment
557             _BLOCK_TIMESTAMP_LAST_ = blockTimestamp;

/// @audit _BASE_TOKEN_.balanceOf() called prior to this assignment
/// @audit State change when _sync() calls _twapUpdate() 
/// @audit at line 553                     _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
578             _twapUpdate();
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L578:578

```solidity
File: src/staking/LockingMultiRewards.sol
/// @audit _getRewards() called prior to this assignment
/// @audit contains nested function call rewardToken.safeTransfer() 
/// @audit located in file 2024-03-abracadabra-money/src/staking/LockingMultiRewards.sol  
619                 rewards[user][rewardToken] = 0;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L619:619


## [L-23] - The additions/multiplications may silently overflow because they're in unchecked blocks with no preceding value checks, which may lead to unexpected results.:
The additions/multiplications may silently overflow because they're in unchecked blocks with no preceding value checks, which may lead to unexpected results.

```solidity
File: src/mimswap/MagicLP.sol
553                     _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L553:553


## [L-24] - Unbounded state array which is iterated upon:
Iterating over an unbounded state array in Solidity can result in excessive gas consumption, especially if the array size exceeds the block gas limit. This issue commonly arises in tasks like token distribution. To address this, it is recommended to limit array sizes for iteration, consider alternative data structures like linked lists, adopt paginated processing for smaller batches over multiple transactions, or use a 'state array' with a separate index-tracking array to manage large datasets and avoid gas-related problems.

```solidity
File: src/staking/LockingMultiRewards.sol
407                 Balances storage bal = _balances[user];

408                 LockedBalance[] storage locks = _userLocks[user];

417                 if (index == lastLockIndex[user] && locks.length > 1) {

430                 if (lastLockIndex[user] == lastIndex) {

431                     lastLockIndex[user] = index;

548                 _updateRewardsGlobal(rewardTokens[i], totalSupply_);

562                 address token = rewardTokens[i];

576                 address token = rewardTokens[i];

615                 address rewardToken = rewardTokens[i];

616                 uint256 rewardAmount = rewards[user][rewardToken];

616                 uint256 rewardAmount = rewards[user][rewardToken];

619                 rewards[user][rewardToken] = 0;

619                 rewards[user][rewardToken] = 0;

648                     _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L648:648

## [L-25] - Prefer continue over revert model in iteration:

Preferably, it's better to skip operations on array indices when a condition is not met instead of reverting the entire transaction. Reverting could be exploited by malicious actors who might intentionally introduce array objects failing conditional checks, disrupting group operations. It's advisable to skip array indices rather than revert, unless there are valid security or logic reasons for doing otherwise

```solidity
File: src/blast/BlastOnboarding.sol
165             for (uint256 i = 0; i < tokens.length; i++) {
166                 if (!supportedTokens[tokens[i]]) {
167                     revert ErrUnsupportedToken();
168                 }
169                 if (registry.nativeYieldTokens(tokens[i])) {
170                     BlastYields.claimAllTokenYields(tokens[i], feeTo);
171                 }
172             }
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165:172

```solidity
File: src/staking/LockingMultiRewards.sol
405             for (uint256 i; i < users.length; ) {
406                 address user = users[i];
407                 Balances storage bal = _balances[user];
408                 LockedBalance[] storage locks = _userLocks[user];
409     
410                 if (locks.length == 0) {
411                     revert ErrNoLocks();
412                 }
413     
414                 uint256 index = lockIndexes[i];
415     
416                 // Prevents processing `lastLockIndex` out of order
417                 if (index == lastLockIndex[user] && locks.length > 1) {
418                     revert ErrInvalidLockIndex();
419                 }
420     
421                 // prohibit releasing non-expired locks
422                 if (locks[index].unlockTime > block.timestamp) {
423                     revert ErrLockNotExpired();
424                 }
425     
426                 uint256 amount = locks[index].amount;
427                 uint256 lastIndex = locks.length - 1;
428     
429                 /// Last lock index changed place with the one we just swapped.
430                 if (lastLockIndex[user] == lastIndex) {
431                     lastLockIndex[user] = index;
432                 }
433     
434                 if (index != lastIndex) {
435                     locks[index] = locks[lastIndex];
436                     emit LogLockIndexChanged(user, lastIndex, index);
437                 }
438     
439                 locks.pop();
440     
441                 unlockedSupply += amount;
442                 lockedSupply -= amount;
443     
444                 bal.unlocked += amount;
445                 bal.locked -= amount;
446     
447                 emit LogUnlocked(user, amount, index);
448     
449                 unchecked {
450                     ++i;
451                 }
452             }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405:452

## [L-26] - Contracts use infinite approvals with no means to revoke:
Infinite approvals on external contracts can be dangerous if the target becomes compromised. See [here](https://revoke.cash/exploits) for a list of approval exploits.  The following contracts are vulnerable to such attacks since they have no functionality to revoke the approval (call  with amount ). Consider enabling the contract to revoke approval in emergency situations.

```solidity
File: src/cauldrons/CauldronV4.sol
143             magicInternetMoney.approve(address(bentoBox), type(uint256).max);
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/cauldrons/CauldronV4.sol#L143:143

## [L-27] - External calls in modifiers should be avoided:
Using external calls within modifiers can introduce reentrancy risks and make a contract's logic less transparent. Modifiers are meant for pre-execution checks, and external calls can lead to unpredictable flow and potential reentrancy issues. Avoiding external calls in modifiers and placing them directly in the function body enhances code clarity, aids in auditing, and minimizes unexpected behaviors. This practice ensures a more explicit execution order and clearer understanding of the code's effects.

```solidity
File: src/blast/BlastMagicLP.sol
119       if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119:119