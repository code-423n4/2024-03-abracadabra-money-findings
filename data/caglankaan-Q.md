### Consider implementing two-step procedure for updating protocol addresses

```solidity
Path: ./src/blast/BlastOnboarding.sol

152:        feeTo = feeTo_;	// @audit-issue

191:        bootstrapper = bootstrapper_;	// @audit-issue
```
[152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastOnboarding.sol#L152-L152), [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastOnboarding.sol#L191-L191), 


```solidity
Path: ./src/blast/BlastOnboardingBoot.sol

142:        staking = _staking;	// @audit-issue
```
[142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastOnboardingBoot.sol#L142-L142), 


```solidity
Path: ./src/blast/BlastMagicLP.sol

85:        feeTo = feeTo_;	// @audit-issue
```
[85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastMagicLP.sol#L85-L85), 


```solidity
Path: ./src/blast/BlastGovernor.sol

45:        feeTo = _feeTo;	// @audit-issue
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastGovernor.sol#L45-L45), 


```solidity
Path: ./src/blast/BlastBox.sol

77:        feeTo = feeTo_;	// @audit-issue
```
[77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastBox.sol#L77-L77), 


```solidity
Path: ./src/mimswap/MagicLP.sol

119:        _BASE_TOKEN_ = baseTokenAddress;	// @audit-issue

120:        _QUOTE_TOKEN_ = quoteTokenAddress;	// @audit-issue

124:        _MT_FEE_RATE_MODEL_ = IFeeRateModel(mtFeeRateModel);	// @audit-issue
```
[119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L119-L119), [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L120-L120), [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L124-L124), 


```solidity
Path: ./src/mimswap/periphery/Factory.sol

101:        implementation = implementation_;	// @audit-issue

110:        maintainerFeeRateModel = maintainerFeeRateModel_;	// @audit-issue
```
[101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/periphery/Factory.sol#L101-L101), [110](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/periphery/Factory.sol#L110-L110), 


```solidity
Path: ./src/mimswap/auxiliary/FeeRateModel.sol

51:        maintainer = maintainer_;	// @audit-issue

58:        implementation = implementation_;	// @audit-issue
```
[51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/auxiliary/FeeRateModel.sol#L51-L51), [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/auxiliary/FeeRateModel.sol#L58-L58), 


#### Recommendation
Introduce two state variables in your contract: one to hold the proposed new address (`address public proposedAddress`) and another to timestamp the proposal (`uint public addressChangeInitiated`). Implement two functions: one to propose a new address, recording the current timestamp, and another to finalize the address change after the delay period has elapsed.### 02"></a> Centralization risk for privileged functions
Contracts with privileged functions need owner/admin to be trusted not to perform malicious updates or drain funds. This may also cause a single point failure.

### Missing checks for `address(0)` in constructor/initializers
In Solidity, the Ethereum address `0x0000000000000000000000000000000000000000` is known as the "zero address". This address has significance because it's the default value for uninitialized address variables and is often used to represent an invalid or non-existent address. The "
Missing zero address control" issue arises when a Solidity smart contract does not properly check or prevent interactions with the zero address, leading to unintended behavior.
For instance, a contract might allow tokens to be sent to the zero address without any checks, which essentially burns those tokens as they become irretrievable. While sometimes this is intentional, without proper control or checks, accidental transfers could occur.    
        

```solidity
Path: ./src/staking/LockingMultiRewards.sol

135:        stakingToken = _stakingToken;	// @audit-issue
```
[135](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/staking/LockingMultiRewards.sol#L135-L135), 


```solidity
Path: ./src/oracles/aggregators/MagicLpAggregator.sol

22:        pair = pair_;	// @audit-issue

23:        baseOracle = baseOracle_;	// @audit-issue

24:        quoteOracle = quoteOracle_;	// @audit-issue

25:        baseDecimals = IERC20Metadata(pair_._BASE_TOKEN_()).decimals();	// @audit-issue

26:        quoteDecimals = IERC20Metadata(pair_._QUOTE_TOKEN_()).decimals();	// @audit-issue
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/oracles/aggregators/MagicLpAggregator.sol#L22-L22), [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/oracles/aggregators/MagicLpAggregator.sol#L23-L23), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/oracles/aggregators/MagicLpAggregator.sol#L24-L24), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/oracles/aggregators/MagicLpAggregator.sol#L25-L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/oracles/aggregators/MagicLpAggregator.sol#L26-L26), 


```solidity
Path: ./src/mimswap/periphery/Router.sol

44:        factory = factory_;	// @audit-issue
```
[44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/periphery/Router.sol#L44-L44), 

#### Recommendation
It is strongly recommended to implement checks to prevent the zero address from being set during the initialization of contracts. This can be achieved by adding require statements that ensure address parameters are not the zero address. 


### Division before multiplication
When dealing with arithmetic operations, it's crucial to prioritize multiplication before division. This practice helps to reduce the risk of rounding errors and increases the precision of the calculations. By rearranging your mathematical operations to perform multiplications first, you can enhance the accuracy and efficiency of your contract's computational processes.

```solidity
Path: ./src/staking/LockingMultiRewards.sol

258:        return (block.timestamp / rewardsDuration) * rewardsDuration;	// @audit-issue
```
[258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/staking/LockingMultiRewards.sol#L258-L258), 


```solidity
Path: ./src/mimswap/libraries/Math.sol

99:            _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);	// @audit-issue

158:                temp = (((delta * V1) / V0) * i) / V0;	// @audit-issue

170:        uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB	// @audit-issue
```
[99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/libraries/Math.sol#L99-L99), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/libraries/Math.sol#L158-L158), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/libraries/Math.sol#L170-L170), 

#### Recommendation
Review your smart contract code to identify instances where division precedes multiplication. Refactor these calculations by rearranging the order, ensuring multiplication is performed first. This adjustment can significantly improve the precision of your results, especially in environments where every decimal point matters, like financial or token-related contracts.


### Consider the case where `totalSupply()` is 0
Consider the case where `totalSupply()` is 0. When `totalSupply()` is 0, it should return 0 directly, because there will be an error of dividing by 0.

```solidity
Path: ./src/oracles/aggregators/MagicLpAggregator.sol

45:        return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());	// @audit-issue
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/oracles/aggregators/MagicLpAggregator.sol#L45-L45), 

#### Recommendation
Implement a check for `totalSupply()` being 0 before executing division operations that depend on its value. For calculations that involve dividing by `totalSupply()`, return a default value, typically 0, if `totalSupply()` equals 0. This approach avoids division by zero errors and ensures that your contract behaves predictably under all conditions. For example:
```solidity
function calculateAllocation(uint256 y) public view returns (uint256) {
    uint256 supply = totalSupply();
    if (supply == 0) {
        return 0;
    }
    return y / supply;
}
```



### Gas griefing/theft is possible on an unsafe external call
A low-level call will copy any amount of bytes to local memory. When bytes are copied from returndata to memory, the memory expansion cost is paid.

This means that when using a standard solidity call, the callee can 'returnbomb' the caller, imposing an arbitrary gas cost.

Because this gas is paid by the caller and in the caller's context, it can cause the caller to run out of gas and halt execution.

Consider replacing all unsafe `call` with `excessivelySafeCall` from this [repository](https://github.com/nomad-xyz/ExcessivelySafeCall).


```solidity
Path: ./src/blast/BlastGovernor.sol

54:        (success, result) = to.call{value: value}(data);	// @audit-issue
```
[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastGovernor.sol#L54-L54), 

#### Recommendation
Mitigate the risk of gas griefing by replacing direct low-level calls (`call`, `delegatecall`, etc.) with `excessivelySafeCall`, a utility that limits the amount of gas used for copying return data, thereby preventing return bombing. The `excessivelySafeCall` function, available in certain security-focused repositories such as [nomad-xyz/ExcessivelySafeCall](https://github.com/nomad-xyz/ExcessivelySafeCall), implements additional checks to ensure that the callee cannot impose arbitrary gas costs on the caller. To incorporate this into your contract:

1. Review your contract for external calls to untrusted contracts.
2. Import or implement an `excessivelySafeCall` utility in your contract.
3. Replace unsafe external calls with `excessivelySafeCall`, specifying limits on return data size as appropriate for your application.

Example usage:
```solidity
// Assuming excessivelySafeCall is available in your contract
(bool success, ) = target.excessivelySafeCall(gasLimit, callData, maxReturnSize);
require(success, "External call failed");

This approach not only protects against gas griefing attacks but also enhances the overall security posture of your contract by ensuring that external interactions do not lead to unexpected execution halts or excessive gas consumption. Always perform thorough testing after integrating `excessivelySafeCall` to ensure compatibility and intended functionality.

### `decimals()` is not a part of the `ERC-20` standard
The `decimals()` function is not a part of the [ERC-20](https://eips.ethereum.org/EIPS/eip-20) standard, and was added later as an [optional extension](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/extensions/IERC20Metadata.sol). As such, some valid `ERC20` tokens do not support this interface, so it is unsafe to blindly cast all tokens to this interface, and then call this function.


```solidity
Path: ./src/oracles/aggregators/MagicLpAggregator.sol

25:        baseDecimals = IERC20Metadata(pair_._BASE_TOKEN_()).decimals();	// @audit-issue

26:        quoteDecimals = IERC20Metadata(pair_._QUOTE_TOKEN_()).decimals();	// @audit-issue
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/oracles/aggregators/MagicLpAggregator.sol#L25-L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/oracles/aggregators/MagicLpAggregator.sol#L26-L26), 


```solidity
Path: ./src/mimswap/MagicLP.sol

164:        return IERC20Metadata(_BASE_TOKEN_).decimals();	// @audit-issue
```
[164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L164-L164), 


```solidity
Path: ./src/mimswap/periphery/Router.sol

64:        _validateDecimals(IERC20Metadata(baseToken).decimals(), IERC20Metadata(quoteToken).decimals());	// @audit-issue

83:            _validateDecimals(18, IERC20Metadata(token).decimals());	// @audit-issue

85:            _validateDecimals(IERC20Metadata(token).decimals(), 18);	// @audit-issue
```
[64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/periphery/Router.sol#L64-L64), [83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/periphery/Router.sol#L83-L83), [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/periphery/Router.sol#L85-L85), 

#### Recommendation
When working with ERC-20 tokens in your Solidity code, be aware that the `decimals()` function is not a part of the ERC-20 standard and is considered an optional extension. Not all valid ERC-20 tokens implement this interface, so avoid blindly casting all tokens to this interface and calling the `decimals()` function. Instead, check the token's documentation or contract to determine whether it supports this extension before using it.

### `symbol()` is not a part of the `ERC-20` standard
The `symbol()` function is not a part of the [ERC-20](https://eips.ethereum.org/EIPS/eip-20) standard, and was added later as an [optional extension](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/extensions/IERC20Metadata.sol). As such, some valid `ERC20` tokens do not support this interface, so it is unsafe to blindly cast all tokens to this interface, and then call this function.


```solidity
Path: ./src/mimswap/MagicLP.sol

156:        return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));	// @audit-issue
```
[156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L156-L156), 

#### Recommendation
When working with ERC-20 tokens in your Solidity code, be aware that the `symbol()` function is not a part of the ERC-20 standard and is considered an optional extension. Not all valid ERC-20 tokens implement this interface, so avoid blindly casting all tokens to this interface and calling the `symbol()` function. Instead, check the token's documentation or contract to determine whether it supports this extension before using it.

### Solidity version 0.8.20 might not work on all chains due to `PUSH0`
The Solidity version 0.8.20 employs the recently introduced PUSH0 opcode in the Shanghai EVM. This opcode might not be universally supported across all blockchain networks and Layer 2 solutions. Thus, as a result, it might be not possible to deploy solution with version 0.8.20 >= on some blockchains.

```solidity
Path: ./src/staking/LockingMultiRewards.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/staking/LockingMultiRewards.sol#L2-L2), 


```solidity
Path: ./src/blast/BlastOnboarding.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastOnboarding.sol#L2-L2), 


```solidity
Path: ./src/blast/BlastDapp.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastDapp.sol#L2-L2), 


```solidity
Path: ./src/blast/BlastOnboardingBoot.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastOnboardingBoot.sol#L2-L2), 


```solidity
Path: ./src/blast/BlastMagicLP.sol

3:pragma solidity >=0.8.0;	// @audit-issue
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastMagicLP.sol#L3-L3), 


```solidity
Path: ./src/blast/BlastGovernor.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastGovernor.sol#L2-L2), 


```solidity
Path: ./src/blast/BlastTokenRegistry.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastTokenRegistry.sol#L2-L2), 


```solidity
Path: ./src/blast/BlastBox.sol

3:pragma solidity >=0.8.0;	// @audit-issue
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastBox.sol#L3-L3), 


```solidity
Path: ./src/blast/BlastWrappers.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/BlastWrappers.sol#L2-L2), 


```solidity
Path: ./src/blast/libraries/BlastYields.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/libraries/BlastYields.sol#L2-L2), 


```solidity
Path: ./src/blast/libraries/BlastPoints.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/blast/libraries/BlastPoints.sol#L2-L2), 


```solidity
Path: ./src/oracles/aggregators/MagicLpAggregator.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/oracles/aggregators/MagicLpAggregator.sol#L2-L2), 


```solidity
Path: ./src/mimswap/MagicLP.sol

8:pragma solidity >=0.8.0;	// @audit-issue
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/MagicLP.sol#L8-L8), 


```solidity
Path: ./src/mimswap/periphery/Factory.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/periphery/Factory.sol#L2-L2), 


```solidity
Path: ./src/mimswap/periphery/Router.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/periphery/Router.sol#L2-L2), 


```solidity
Path: ./src/mimswap/auxiliary/FeeRateModelImpl.sol

2:pragma solidity >=0.8.0;	// @audit-issue
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/auxiliary/FeeRateModelImpl.sol#L2-L2), 


```solidity
Path: ./src/mimswap/auxiliary/FeeRateModel.sol

8:pragma solidity >=0.8.0;	// @audit-issue
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/auxiliary/FeeRateModel.sol#L8-L8), 


```solidity
Path: ./src/mimswap/libraries/DecimalMath.sol

7:pragma solidity >=0.8.0;	// @audit-issue
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/libraries/DecimalMath.sol#L7-L7), 


```solidity
Path: ./src/mimswap/libraries/PMMPricing.sol

8:pragma solidity >=0.8.0;	// @audit-issue
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/libraries/PMMPricing.sol#L8-L8), 


```solidity
Path: ./src/mimswap/libraries/Math.sol

8:pragma solidity >=0.8.0;	// @audit-issue
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/5da03be9e6bb3c6081ffea4ae4bfa441f1cc2fdd/./src/mimswap/libraries/Math.sol#L8-L8), 

#### Recommendation
The Solidity version 0.8.20 employs the recently introduced PUSH0 opcode in the Shanghai EVM. This opcode might not be universally supported across all blockchain networks and Layer 2 solutions. Thus, as a result, it might be not possible to deploy solution with version 0.8.20 >= on some blockchains.

It is recommended to verify whether solution can be deployed on particular blockchain with the Solidity version 0.8.20 >=. Whenever such deployment is not possible due to lack of PUSH0 opcode support and lowering the Solidity version is a must, it is strongly advised to review all feature changes and bugfixes in [Solidity releases](https://soliditylang.org/blog/category/releases/). Some changes may have impact on current implementation and may impose a necessity of maintaining another version of solution.

