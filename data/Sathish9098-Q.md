# QA Report

##

## [L-1] The Peril of Mistakenly Sending Tokens to a Smart Contract with a Payable Fallback Function

Contract can accept Ether through a receive() or payable fallback function, it doesn't mean it can manage ERC-20 tokens. Accidentally sent ERC-20 tokens may be permanently locked the contract lacks a method to return them, since moving these tokens requires specific interactions not covered by simple Ether transfers. 

```solidity
FILE: 2024-03-abracadabra-money/src/blast/BlastGovernor.sol

13: receive() external payable {}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L13

## Recommended Mitigation
Add the recoverable functions through admin if any tokens sent accidently

```solidity

function recoverERC20(address tokenAddress, uint256 tokenAmount) external onlyOperators {
        IERC20(tokenAddress).transfer(owner(), tokenAmount);
    }

```

##

## [

