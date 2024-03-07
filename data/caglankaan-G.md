### Cache State Variable Array Length In For Loop
Failing to cache the array length when iterating through arrays in Solidity can have significant performance and gas cost implications. In Solidity, array lengths can change during execution due to external calls or storage modifications. When the array length is not cached before entering a loop, it is recomputed with each iteration, leading to unnecessary gas consumption and potentially making the contract vulnerable to reentrancy attacks.        


```solidity
Path: ./src/staking/LockingMultiRewards.sol

547:        for (uint256 i; i < rewardTokens.length; ) {	// @audit-issue

561:        for (uint256 i; i < rewardTokens.length; ) {	// @audit-issue

575:        for (uint256 i; i < rewardTokens.length; ) {	// @audit-issue

614:        for (uint256 i; i < rewardTokens.length; ) {	// @audit-issue
```
[547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/staking/LockingMultiRewards.sol#L547-L547), [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/staking/LockingMultiRewards.sol#L561-L561), [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/staking/LockingMultiRewards.sol#L575-L575), [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/staking/LockingMultiRewards.sol#L614-L614), 

#### Recommendation
To enhance performance and reduce gas costs, cache the array length before entering a for loop in Solidity. This approach prevents repeated computation of the array length and mitigates the risk of reentrancy attacks due to array length changes during loop execution.


### `event` Declared But Not Emitted
An event within the contract is declared but not utilized in any of the contract's functions or operations. Having unused event declarations can consume unnecessary space and may lead to misunderstandings for developers or users expecting this event as part of the contract's functionality.


```solidity
Path: ./src/staking/LockingMultiRewards.sol

26:    event LogRewardsDurationUpdated(address token, uint256 newDuration);	// @audit-issue
```
[26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/staking/LockingMultiRewards.sol#L26-L26), 


```solidity
Path: ./src/blast/BlastMagicLP.sol

13:    event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);	// @audit-issue
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastMagicLP.sol#L13-L13), 


```solidity
Path: ./src/mimswap/periphery/Factory.sol

26:    event LogSetMaintainer(address indexed newMaintainer);	// @audit-issue
```
[26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/periphery/Factory.sol#L26-L26), 

#### Recommendation

Consider removing the unused event declaration to optimize the contract and enhance clarity. If there is an intent for this event to be part of certain operations, ensure it is emitted appropriately. Otherwise, for the sake of clean and efficient code, it is advisable to remove any unused declarations.



### WETH address definition can be use directly
WETH is a wrap Ether contract with a specific address in the Ethereum network, giving the option to define it may cause false recognition, it is healthier to define it directly.
Advantages of defining a specific contract directly:

It saves gas,
Prevents incorrect argument definition,
Prevents execution on a different chain and re-signature issues,
WETH Address : 0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2

```solidity
Path: ./src/mimswap/periphery/Router.sol

33:    IWETH public immutable weth;	// @audit-issue
```
[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/periphery/Router.sol#L33-L33), 


#### Recommendation
Use specific WETH contract directly.


### Avoid Using State Variables Directly in `emit` for Gas Efficiency
In Solidity, emitting events is a common way to log contract activity and changes, especially for off-chain monitoring and interfacing. However, using state variables directly in `emit` statements can lead to increased gas costs. Each access to a state variable incurs gas due to storage reading operations. When these variables are used directly in `emit` statements, especially within functions that perform multiple operations, the cumulative gas cost can become significant. Instead, caching state variables in memory and using these local copies in `emit` statements can optimize gas usage.


```solidity
Path: ./src/staking/LockingMultiRewards.sol

318:        emit LogSetMinLockAmount(minLockAmount, _minLockAmount);	// @audit-issue: `minLockAmount` is a state variable and used on line(s): ['319']
```
[318](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/staking/LockingMultiRewards.sol#L318-L318), 


```solidity
Path: ./src/blast/BlastOnboardingBoot.sol

124:        emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);	// @audit-issue: `pool` is a state variable and used on line(s): ['97', '122', '126', '117', '106']

124:        emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);	// @audit-issue: `staking` is a state variable and used on line(s): ['122', '117', '118', '126', '119']

124:        emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);	// @audit-issue: `totalPoolShares` is a state variable and used on line(s): ['122', '108', '126', '106']

148:        emit LogReadyChanged(ready);	// @audit-issue: `ready` is a state variable and used on line(s): ['147']
```
[124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastOnboardingBoot.sol#L124-L124), [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastOnboardingBoot.sol#L124-L124), [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastOnboardingBoot.sol#L124-L124), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastOnboardingBoot.sol#L148-L148), 


```solidity
Path: ./src/mimswap/MagicLP.sol

264:        emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);	// @audit-issue: `_BASE_TOKEN_` is a state variable and used on line(s): ['245']

264:        emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);	// @audit-issue: `_QUOTE_TOKEN_` is a state variable and used on line(s): ['262']

287:        emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);	// @audit-issue: `_QUOTE_TOKEN_` is a state variable and used on line(s): ['268']

287:        emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);	// @audit-issue: `_BASE_TOKEN_` is a state variable and used on line(s): ['285']

325:            emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);	// @audit-issue: `_QUOTE_TOKEN_` is a state variable and used on line(s): ['299', '347']

325:            emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);	// @audit-issue: `_BASE_TOKEN_` is a state variable and used on line(s): ['298', '347']

347:            emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);	// @audit-issue: `_BASE_TOKEN_` is a state variable and used on line(s): ['298', '325']

347:            emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);	// @audit-issue: `_QUOTE_TOKEN_` is a state variable and used on line(s): ['325', '299']
```
[264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L264-L264), [264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L264-L264), [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L287-L287), [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L287-L287), [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L325-L325), [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L325-L325), [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L347-L347), [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L347-L347), 


```solidity
Path: ./src/mimswap/periphery/Factory.sol

88:        emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);	// @audit-issue: `maintainerFeeRateModel` is a state variable and used on line(s): ['86']
```
[88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/periphery/Factory.sol#L88-L88), 


#### Recommendation
To optimize gas efficiency, cache state variables in memory when they are used multiple times within a function, including in `emit` statements.