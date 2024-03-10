# 1. Eth can not be recovered from MagicLP
Links to affected code *

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L5

### Impact

MagicLP contracts are deployed with solady's LibClone, which makes them able to [receive](https://github.com/Vectorized/solady/blob/9deb9ed36a27261a8745db5b7cd7f4cdc3b1cd4e/src/utils/LibClone.sol#L421C1-L426C116) ETH.

But the pool's are only able to recover non ether tokens.
```
    function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {
        if (token == _BASE_TOKEN_ || token == _QUOTE_TOKEN_) {
            revert ErrNotAllowed();
        }

        token.safeTransfer(to, amount);
        emit TokenRescue(token, to, amount);
    }
```
As a consequence, any ether sent to the pools are lost and irretrievable, seeing as they can also be removed.

### Tools Used
Manual code review

### Recommended Mitigation Steps
Include a `rescueEth` function in the pools too.


***

# 2. User exit points should not be pausable

Lines of code* 

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L132

### Impact

The `withdraw` function in BlastOnboarding contract has a `whenNotPaused` modifier. This can put users' funds at risk if a compromised/malicious admin decides to admin pause the contract. He might even renounce ownership, leaving the funds stuck in the contract forever.

```
    function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
        balances[msg.sender][token].unlocked -= amount;
        balances[msg.sender][token].total -= amount;
        totals[token].unlocked -= amount;
        totals[token].total -= amount;

        token.safeTransfer(msg.sender, amount);

        emit LogWithdraw(msg.sender, token, amount);
    }
```

### Recommended Mitigation Steps
Remove the whenNotPaused modifier from the `withdraw` function

***

# 3. `_twapUpdate` can be dossed due to potential underflow error

Links to affected code *

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L546

### Impact

The a normalization of the block.timestamp value to uint32 in the `_twapUpdate` function will throw an underflow error due to the solidity version in use and the potential of block.timestamp to exceed type(uint32).max.

```
    function _twapUpdate() internal {
        uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
        uint32 timeElapsed = blockTimestamp - _BLOCK_TIMESTAMP_LAST_;

        if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
            /// @dev It is desired and expected for this value to
            /// overflow once it has hit the max of `type.uint256`.
            unchecked {
                _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
            }
        }

        _BLOCK_TIMESTAMP_LAST_ = blockTimestamp;
    }
```
### Recommended Mitigation Steps
Consider wrapping the `timeElapsed` in an unchecked block.
```
    unchecked {
        uint32 timeElapsed = blockTimestamp - _BLOCK_TIMESTAMP_LAST_;
    }
```
***

# 4. Return value of chainlink's `latestRoundData` should be well validated 

Lines of code* 

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol#L48

### Impact

Using the `latestRoundData` function requires price validation for 0 or negative values. 
```
    function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
        return (0, latestAnswer(), 0, 0, 0);
    }
```

### Recommended Mitigation Steps
Include a check for negative or zero values.
```
    require(latestAnswer() > 0 "Error");
```
Consider also checking for the roundid, startedAt and updatedAt time too.
***

# 5. Should check for active sequencer uptime 

Lines of code* 

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/oracles/aggregators/MagicLpAggregator.sol

### Impact
The MagicLpAggregator contract gets prices from chainlink without checking for active sequencer. In L2 oracles, Chainlink recommends consulting the Sequencer Uptime Feed to ensure that the sequencer is live before trusting the data returned by the Price Feed. If the Arbitrum Sequencer goes down, oracle data will not be kept up to date, and thus could become stale.

### Recommended Mitigation Steps
Include a function to call for active sequencer.`

***

# 6. Add explicit check for lowlevel call success/failure return value 

Lines of code* 

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L54

## Impact

Including an explicit check for return values of low level calls can help prevent silent failures.
```
    function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
        (success, result) = to.call{value: value}(data);
    }
```

***

# 7. Add checks for same parameter updates

Lines of code* 

https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L57
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/auxiliary/FeeRateModel.sol#L46
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L96
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L105
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L72
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L81
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L40
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L89
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L80
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L147
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L175
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L185
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L190
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L137
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L146
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L317

