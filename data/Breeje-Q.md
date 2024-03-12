### [L-01] Division before multiplication can result to rounding errors

There are multiple areas where Multiplication is performed on the result of a division in Math.sol contract. 

One such example is in `_SolveQuadraticFunctionForTrade` function:

```solidity

    uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB

```

As denoted by the accompanying comment, the intention is to multiply `k` by the square of `V0`. However, the current implementation deviates from this intention by initially multiplying `k` with `V0`, then dividing the result by `V1`, followed by another multiplication by `V0`.

In scenarios where the value of `k = 1` and `V0 < V1`, the initial expression `(k * V0) / V1)` could be rounded down to zero due to integer division truncation. Consequently, the entire initial expression `kQ0^2/Q1` might be rounded down to zero, resulting in a loss of value due to precision.

This discrepancy is noteworthy since `k = 1` is a legitimate value that creators might opt to employ.

### [L-02] `MagicLpAggregator` won't support >18 decimal tokens

There are token with more than 18 decimals precision and `MagicLpAggregator` can't handle it as `WAD - decimals` expression will always revert.

```solidity

    function latestAnswer() public view override returns (int256) {
      // SNIP

      (uint256 baseReserve, uint256 quoteReserve) = _getReserves();
@->   baseReserve = baseReserve * (10 ** (WAD - baseDecimals));
@->   quoteReserve = quoteReserve * (10 ** (WAD - quoteDecimals));

      // SNIP
    }

```