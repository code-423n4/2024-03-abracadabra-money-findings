## `latestAnswer()` should revert if price returned is 0.

## Links

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L38-L39


## Bug description

Although unlikely, it is possible that the price feed returns 0 if an error occurs on their side. 

## Impact

If the feed returns 0, this will break all the logic and some tokens may be swapped for almost 0 cost.

## POC

We can see that [latesAnswer](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L37-L39)

```solidity
function latestAnswer() public view override returns (int256) {
        uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
        uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
```
will operate on the raw returned data.

## Mitigation route

Do implement more checks in order to be prevent tricky situation described above


```diff

    function latestAnswer() public view override returns (int256) {
++        uint256 basePrice = baseOracle.latestAnswer();
++        uint256 quotePrice = quoteOracle.latestAnswer();
++        if(basePrice == 0 || quotePrice == 0) revert priceIs0();
++        uint256 baseAnswerNomalized = basePrice * (10 ** (WAD - baseOracle.decimals()));
++        uint256 quoteAnswerNormalized = quotePrice * (10 ** (WAD - quoteOracle.decimals()));
--       uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
--        uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
```

## Owner of the protocl can rug the MagicLp pool with the `setParameters` 
   function

## Links

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L476-L504 

## Vulnerability Description

The `owner()` of the initial implementation can rug the protocol, this kind of power is quite deceptive because the function name doesn't transmit that this is what the `owner()` of the implementation has the power to do. 
This can be quite unfair if some liquidity providers bought shares, and become worthless afterwards.
Given that the function name is `setParameters()` and not withdraw assets, it is too deceptive not to be flagged. 

## Impact 

The assets can be withdrawn by the implementation owner of the implementation by a function that has a misleading name.

## POC

Here the [setParameters](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L476-L482) allows the implementation owner to simply withdraw assets out of the pool. 

 

```
        _transferBaseOut(assetTo, baseOutAmount); 
        _transferQuoteOut(assetTo, quoteOutAmount);
```

The event that this function has doesn't even indicate how many assets have been withdrawn `emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);`

## Mitigation Route

To increase transparency towards users change the name to something more accurate such as `withdrawLPFunds()`. 
Also add the assets withdrawn to the event.
`emit withdrawLPFunds(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance, quoteOutAmount, baseOutAmount);`
