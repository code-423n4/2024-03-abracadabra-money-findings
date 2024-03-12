## \[L-01\] Empty receive()/payable fallback() function does not authenticate requests

If the intention is for the Ether to be used, the function should call another function, otherwise it should revert (e.g. require(msg.sender == address(weth))). Having no access control on the function means that someone may send Ether to the contract, and have no way to get anything back out, which is a loss of funds. If the concern is having to spend a small amount of gas to check the sender against an immutable address, the code should at least have a function to rescue unused Ether.

```
receive() external payable {}
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L36

## \[L-02\] Unsafe cast

```
_BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
        _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L438C1-L439C122

```
if (baseBalance != _BASE_RESERVE_) {
            _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
            _BASE_RESERVE_ = uint112(baseBalance);
        }
        if (quoteBalance != _QUOTE_RESERVE_) {
            _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
            _QUOTE_RESERVE_ = uint112(quoteBalance);
        }
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L512C1-L519C10

## \[L-03\] Insufficient coverage

Description  
The test coverage rate of the project is ~60%. Testing all functions is best practice in terms of security criteria.

Due to its capacity, test coverage is expected to be 100%.

## \[L-04\] \`receive()\` should not be \`payable\`

```
File: BlastOnboarding.sol

80: receive() external payable override { 
        revert ErrUnsupported();
    }
```

the `receive()` function is marked as `payable` but immediately reverts with an error `ErrUnsupported()`.

Marking a function as `payable` means that it can receive Ether along with a transaction. However, since this function immediately reverts with an error, any attempt to send Ether to this contract's address will result in a failed transaction with the specified error.

it could be misleading or confusing to developers interacting with the contract. If the intention is not to accept Ether payments at all, the `receive()` function could be omitted or modified to handle Ether transfers differently (such as logging an event or reverting with a different error message).

## \[L05\] Some contracts is UNLICENSED it's better to choose a proper LICENSE.

`// SPDX-License-Identifier: UNLICENSED`

## \[L-06\] Use of magic numbers is confusing and risky

### Summary:

Magic numbers are hardcoded numbers used in the code which are ambiguous to their intended purpose. These should be replaced with constants to make code more readable and maintainable.

### Details:

Values are hardcoded and would be more readable and maintainable if declared as a constant

### Mitigation

Replace magic hardcoded numbers with declared constants.

### Github Permalinks

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L81C4-L110C6

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L594

## \[N-01\] Showing the actual values of numbers in NatSpec comments makes checking and reading code easier.

```diff
-    uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%
-    uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1% 

+    uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%  , 	100_000_000_000_000
+    uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1% 	,       10_000_000_000_000_000
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L65C1-L66C58

## \[N-02\] For immutable variables in Solidity, the convention is to use CAPS\_CASE or UPPER\_CASE\_WITH\_UNDERSCORES.

```
uint256 public immutable maxLocks;
    uint256 public immutable lockingBoostMultiplerInBips;
    uint256 public immutable rewardsDuration;
    uint256 public immutable lockDuration;
    address public immutable stakingToken;
```

&nbsp;https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L83

```
IMagicLP public immutable pair;
    IAggregator public immutable baseOracle;
    IAggregator public immutable quoteOracle;
    uint8 public immutable baseDecimals;
    uint8 public immutable quoteDecimals;
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L10

## \[N-03\] constants should be defined rather than using magic numbers

A magic number is a numeric literal that is used in the code without any explanation of its meaning. The use of magic numbers makes programs less readable and hence more difficult to maintain and update.

Even assembly can benefit from using readable constants instead of hex/numeric literals.

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Router.sol#L81C4-L110C6

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L594

## \[N-04\] Use a single file for all system-wide constants

There are many addresses and constants used in the system. It is recommended to put the most used ones in one file (for example constants.sol, use inheritance to access these values).

This will help with readability and easier maintenance for future changes. This also helps with any issues, as some of these hard-coded values are admin addresses.

constants.sol  
Use and import this file in contracts that require access to these values. This is just a suggestion, in some use cases this may result in higher gas usage in the distribution.

## \[N-05\] Take advantage of Custom Error’s return value property

An important feature of Custom Error is that values such as address, tokenID, msg.value can be written inside the `()` sign, this kind of approach provides a serious advantage in debugging and examining the revert details of dapps such as tenderly.

For Example;

## \[G-06\]  `10 ** 18` can be changed to `1e18` and save some gas

`10 ** 18` can be changed to `1e18` to avoid unnecessary arithmetic operation and save gas.

```
File: DecimalMath.sol

20:    uint256 internal constant ONE = 10 ** 18;

49:    return 10 ** 18;
```

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/DecimalMath.sol#L20C5-L20C46

&nbsp;

## \[N-7\] NatSpec is missing

NatSpec is missing for the   functions , constructor and modifiers:

## \[N-08\] Use a more recent version of Solidity

For security, it is best practice to use the latest Solidity version.

For the security fix list in the versions: https://github.com/ethereum/solidity/blob/develop/Changelog.md

Recommended Mitigation Steps  
Old version of Solidity is used, newer version can be used

## \[N‑10\] Contracts should have full test coverage

While 100% code coverage does not guarantee that there are no bugs, it often will catch easy-to-find bugs, and will ensure that there are fewer regressions when the code invariably has to be modified. Furthermore, in order to get full coverage, code authors will often have to re-organize their code so that it is more modular, so that each component can be tested separately, which reduces interdependencies between modules and layers, and makes for code that is easier to reason about and audit.