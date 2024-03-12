## [L-01]: Removing supported tokens prevents users from withdrawing tokens from `BlastOnboarding`.

Due to the `onlySupportedTokens(token)` modifier, if the owner removes support for tokens, users can no longer withdraw their tokens and their funds will get stuck in the `BlastOnboarding`.

[BlastOnboarding.sol#L132-L141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132-L141)
```solidity
    function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
        balances[msg.sender][token].unlocked -= amount;
        balances[msg.sender][token].total -= amount;
        totals[token].unlocked -= amount;
        totals[token].total -= amount;

        token.safeTransfer(msg.sender, amount);

        emit LogWithdraw(msg.sender, token, amount);
    }
```
Rescues will also not be able function for unsupported tokens.

[BlastOnboarding.sol#L205-L212](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L205-L212)
```solidity
    function rescue(address token, address to, uint256 amount) external onlyOwner {
        if (supportedTokens[token]) {
            revert ErrNotAllowed();
        }

        token.safeTransfer(to, amount);
        emit LogTokenRescue(token, to, amount);
    }
```

Therefore, these tokens will get stuck in the contract until it supports these tokens again which may not be ideal.

Consider removing `onlySupportedTokens(token)` modifier for withdrawals and rescues

## [L-02]: `FeeRateModel.sol`, `FeeRateModelImpl.sol`, `BlastTokenRegistry.sol` do not configure gas yield.

The constructors for the following contracts do not configure gas yield on Blast:

1. https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol

2. https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol

3. https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol

Gas yield for these files won't be substantial so this is marked as low.

## [L-03]: `BlastMagicLP` implementation do not configure gas yield.

The implementation `BlastMagicLP` does not configure the gas yield mode in the constructor.

[BlastMagicLP.sol#L23-L33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23-L33)
```solidity
    constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
        if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
        }
        if (address(registry_) == address(0)) {
            revert ErrZeroAddress();
        }

        registry = registry_;
        feeTo = feeTo_;
    }
```

Since there will still be operations carried out on the implementation contract for admin configuration purposes, it might be best to configure the yield mode by calling `BlastYields.configureDefaultClaimables(address(this))` in the constructor so that any gas spent on implementation contract can be reclaimed.

## [L-04] The maintainer fee model can be changed in the Factory

The maintainer fee model can be changed in the Factory for new MagicLPs deployed.

[Factory.sol#L105-L112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105-L112)
```solidity
    function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
        if (address(maintainerFeeRateModel_) == address(0)) {
            revert ErrZeroAddress();
        }

        maintainerFeeRateModel = maintainerFeeRateModel_;
        emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_);
    }
```

However, this affects new pools deployed and old pools will still use the old maintainer fee model leading to different pools potentially having different fee models which breaks consistency. The maintainer fee rate model contract already has a function to change the rate model implementation and therefore such a function in the factory isn't required.

[FeeRateModel.sol#L57-L60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57-L60)
```solidity
    /// @notice Set the fee rate implementation and default fee rate
    /// @param implementation_ The address of the fee rate implementation, use address(0) to disable
    function setImplementation(address implementation_) public onlyOwner {
        implementation = implementation_;
        emit LogImplementationChanged(implementation_);
    }
```

## [L-05] MagicLP is neither pausable not upgradeable.

[MagicLP](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol) is neither pausable nor upgradeable (it uses non-upgradeable clones). We don't believe this to be a good idea because if a pool-draining exploit was found it would be nearly impossible to protect all the funds still present in the MagicLP.

## [L-06] Router does not verify whether LP provided is a MagicLP

For all swap functions in the [Router](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol), it doesn't validate that the `lp` address provided is an actual MagicLP. While we couldn't find a way to exploit this. Historically, this has been the cause of famous router hacks such as the famous Sushiswap hack - [https://maxwelldulin.com/BlogPost/sushiswap-exploit-explained-2023](https://maxwelldulin.com/BlogPost/sushiswap-exploit-explained-2023)

## [L-07] `MagicLpAggregator` can't work if any oracle returns more than 18 decimals

It will revert due to underflow in `WAD - baseOracle.decimals()` or `WAD - quoteOracle.decimals()`.

[MagicLpAggregator.sol#L38-L39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L38-L39)
```solidity
        uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
        uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
```


## [R-01] Consider a clearer naming for the maximum boost multiplier that can be set in basis points

The `BIPS` variable caps the maximum boost multiplier at 100%. It could do well to be renamed to `MAX_BIPS` for better code readability.

- (LockingMultiRewards.sol#L78)[https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L78]

```diff
- uint256 private constant BIPS = 10_000;
+ uint256 private constant MAX_BIPS = 10_000;
```

## [N-01] Typo in the `_udpateUserRewards` function naming
As can be seen from the title of this log and in the codebase, the function to update user rewards has a typo and should be corrected.

- (LockingMultiRewards.sol#L536-L539)[https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L536-L539]

```js
function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
    rewards[user_][token_] = _earned(user_, balance_, token_, rewardPerToken_);
    userRewardPerTokenPaid[user_][token_] = rewardPerToken_;
}
```

```diff
- function _udpateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
+ function _updateUserRewards(address user_, uint256 balance_, address token_, uint256 rewardPerToken_) internal {
    rewards[user_][token_] = _earned(user_, balance_, token_, rewardPerToken_);
    userRewardPerTokenPaid[user_][token_] = rewardPerToken_;
}
```