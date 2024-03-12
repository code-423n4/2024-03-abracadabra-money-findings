# QA Report for Abracadabra

## Table of Contents

| Issue ID                                                                   | Description                                                |
| -------------------------------------------------------------------------- | ---------------------------------------------------------- |
| [QA-01](#qa-01-protocol-hardcodes-acceptable-tokens-to-18-decimals)        | Protocol hardcodes acceptable tokens to 18 decimals        |
| [QA-02](#qa-02-unhandled-chainlink-revert-would-halt-core-functionalities) | Unhandled Chainlink revert would halt core functionalities |
| [QA-03](#qa-03-unused-local-variables-should-be-removed)                   | Unused local variables should be removed                   |
| [QA-04](#qa-04-always-implement-cei-patterns-where-possible)               | Always implement CEI patterns where possible               |
| [QA-05](#qa-05-unnamed-return-variable-can-remain-unassigned)              | Unnamed return variable can remain unassigned              |

## QA-01 Protocol hardcodes acceptable tokens to 18 decimals

## Proof of Concept

Take a look at https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L16

```solidity
    uint256 public constant WAD = 18;
```

See this https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L37-L48

```solidity
    //@audit chainlink issues
    function latestAnswer() public view override returns (int256) {
       //@audit
        uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
        uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
        uint256 minAnswer = baseAnswerNomalized < quoteAnswerNormalized ? baseAnswerNomalized : quoteAnswerNormalized;

        (uint256 baseReserve, uint256 quoteReserve) = _getReserves();
       //@audit
        baseReserve = baseReserve * (10 ** (WAD - baseDecimals));
        quoteReserve = quoteReserve * (10 ** (WAD - quoteDecimals));
        return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
    }

```

Evidently protocol assumes in four instances that the decimals would always be < 18, i.e in a case where the decimals are above 18 for either of tokens or oracles then this attempt to query the price always reverts

### Impact

Medium to low depending on if plans on supporting tokens whose decimals or their price feed decimals would be more than 18, cause currently protocol is incompatible with some popular tokens out there, limiting adoption.

### Recommended Mitigation Steps

Consider reimplementing the logic and accept tokens that have more than 18 decimals.

## QA-02 Unhandled Chainlink revert would halt core functionalities

### Proof of Concept

Take a look at https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L38-L51

```solidity
    function latestAnswer() public view override returns (int256) {
        uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
        uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
        uint256 minAnswer = baseAnswerNomalized < quoteAnswerNormalized ? baseAnswerNomalized : quoteAnswerNormalized;

        (uint256 baseReserve, uint256 quoteReserve) = _getReserves();
        baseReserve = baseReserve * (10 ** (WAD - baseDecimals));
        quoteReserve = quoteReserve * (10 ** (WAD - quoteDecimals));
        return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
    }

    function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
        return (0, latestAnswer(), 0, 0, 0);
    }
```

Evidently we can see that this is the logic for getting prices that's implemented in the protocol, note that a call to `latestRoundData()` actually [just queries latestAnswer() ](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L49-L51)

But also we can see that this call lacks error handling for the potential failure of `feedConfig.feed.latestRoundData()`, note that Chainlink pricefeeds could revert due to whatever reason, i.e say maintenance or maybe the Chainlink team decide to change the underlying address. Now this omission of not considering this call failing would lead to systemic issues, since calls to this would now revert halting any action that requires this call to succeed.

Here is a minimalistic POC proving the issue:

TokenA has a minPrice of $1. The price of TokenA drops to $0.10. The aggregator still returns $1 allowing the user to interact with TokenA as if it is $1 which is 10x it's actual value.

### Impact

A revert of the entire operation that requires querying the Chainlink pricing logic, This limitation poses a significant risk, since all three pricing modes that use the Chainlink mode either as a primary or secondary source would now revert.

### Recommended Mitigation Steps

Wrap the `feedConfig.feed.latestRoundData()` call in a try-catch block, and consider introducing a fallback oracle incase the call to chainlink reverts.

## QA-03 Unused local variables should be removed

### Proof of Concept

Take a look at some of the instances from code

```sol
  --> script/BlastOnboarding.s.sol:17:9:
   |
17 |         address blastGovernor = toolkit.getAddress(block.chainid, "blastGovernor");
   |         ^^^^^^^^^^^^^^^^^^^^^

  --> src/oracles/aggregators/MagicLpAggregator.sol:34:10:
   |
34 |         (uint256 baseReserve, uint256 quoteReserve) = pair.getReserves();
   |          ^^^^^^^^^^^^^^^^^^^

  --> src/oracles/aggregators/MagicLpAggregator.sol:34:31:
   |
34 |         (uint256 baseReserve, uint256 quoteReserve) = pair.getReserves();
   |                               ^^^^^^^^^^^^^^^^^^^^
```

### Impact

Low, bad code structuring, makes it harder for bith users and developers to understnad code

### Recommended Mitigation Steps

Either use the valriables or remove them from code

## QA-04 Always implement CEI patterns where possible

### Proof of Concept

Take a look athttps://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L458-L478

```solidity
    function _stakeFor(address account, uint256 amount, bool lock_) internal {
        if (amount == 0) {
            revert ErrZeroAmount();
        }

        // This staking contract isn't using balanceOf, so it's safe to transfer immediately
        stakingToken.safeTransferFrom(msg.sender, address(this), amount);
        stakingTokenBalance += amount;

        _updateRewardsForUser(account);

        if (lock_) {
            _createLock(account, amount);
        } else {
            _balances[account].unlocked += amount;
            unlockedSupply += amount;

            emit LogStaked(account, amount);
        }
    }

```

We can see that the CEI pattern is not followed

### Impact

Low, code is not following the best practise.

### Recommended Mitigation Steps

It's always great practise to follow the check effects interaction pattern

## QA-05 Unnamed return variable can remain unassigned

Take a look at some of the instances from code

```sol
  --> src/oracles/aggregators/MagicLpAggregator.sol:33:60:
   |
33 |     function _getReserves() internal view virtual returns (uint256, uint256) {
   |                                                            ^^^^^^^
  --> src/oracles/aggregators/MagicLpAggregator.sol:33:69:
   |
33 |     function _getReserves() internal view virtual returns (uint256, uint256) {
```

### Impact

It'ss known that unnamed return variables can remain unassigned leading to bad code structure.

### Recommended Mitigation Steps

Add an explicit return with value to all non-reverting code paths or name the variable.
