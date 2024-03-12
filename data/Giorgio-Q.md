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