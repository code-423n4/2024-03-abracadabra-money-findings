1. [BlastOnboardingBoot:](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol)
   - The contract has an `owner` role, which has significant control over the onboarding process. The owner can set the `feeTo` address, change the `bootstrapper`, and control the `ready` state of the contract.
   - While these privileges are necessary for managing the onboarding process, a malicious or compromised owner could potentially misuse these powers to manipulate the distribution of tokens or shares.
   - The contract does not have a formal governance mechanism, so any changes to critical parameters depend on the integrity of the owner.

2. [BlastOnboarding:](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol)
   - Similar to BlastOnboardingBoot, this contract has an `owner` role with significant privileges, such as setting supported tokens, enabling/disabling deposits, and changing the `feeTo` address.
   - A malicious or compromised owner could potentially use these privileges to add malicious tokens, prevent users from withdrawing their funds, or siphon off collected fees.
   - The contract does not have a formal governance mechanism, so the integrity of the owner is crucial.

3. [MagicLP:](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol)
   - The contract has an `owner` role, which can call the `setParameters` function to change critical parameters such as the swap fee rate and the PMM parameters.
   - While changing these parameters can be necessary for optimizing the pool's performance, a malicious or compromised owner could set these parameters to extreme values, potentially making the pool unusable or facilitating a rug pull.
   - The contract does not have a formal governance mechanism, so any parameter changes are at the discretion of the owner.

4. [BlastMagicLP:](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol)
   - In addition to the risks inherited from MagicLP, BlastMagicLP introduces an `operator` role that can call the `claimGasYields` and `claimTokenYields` functions to claim yields on behalf of the contract.
   - While these functions are intended to be used for the benefit of the contract and its users, a malicious operator could potentially abuse these privileges for their own gain.
   - The contract owner can add or remove operators, so the integrity of the owner is crucial.

5. [BlastBox:](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol)
   - The contract has an `owner` role that can set the `feeTo` address, enable/disable token deposits, and call arbitrary functions on the Blast precompile contract.
   - A malicious or compromised owner could use these privileges to siphon off fees, prevent users from depositing certain tokens, or interact with the Blast precompile in unintended ways.
   - The contract does not have a formal governance mechanism, so the owner has significant control over the contract's operation.

6. [BlastGovernor:](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol)
   - This contract is designed to be a central point of control for the Blast ecosystem, with the ability to claim yields on behalf of other contracts and execute arbitrary transactions.
   - While this centralized control can be useful for efficiently managing the ecosystem, it also introduces a significant risk if the BlastGovernor contract or its owner is compromised.
   - A malicious BlastGovernor could potentially drain funds from the contracts it governs or interfere with their normal operation.
   - The contract does not have a formal governance mechanism, so the integrity of the owner is crucial.

Code:

```solidity
// BlastOnboardingBoot
function setFeeTo(address feeTo_) external onlyOwner {
    feeTo = feeTo_;
    emit LogFeeToChanged(feeTo_);
}

// BlastOnboarding
function setTokenSupported(address token, bool supported) external onlyOwner {
    supportedTokens[token] = supported;
    emit LogTokenSupported(token, supported);
}

// MagicLP
function setParameters(address assetTo, uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 baseOutAmount, uint256 quoteOutAmount, uint256 minBaseReserve, uint256 minQuoteReserve) public nonReentrant onlyImplementationOwner {
    // ... Set new parameters ...
}

// BlastMagicLP
function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
    operators[operator] = status;
    emit LogOperatorChanged(operator, status);
}

// BlastBox
function setTokenEnabled(address token, bool enabled) external onlyOwner {
    enabledTokens[token] = enabled;
    emit LogTokenDepositEnabled(token, enabled);
}

// BlastGovernor
function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
    (success, result) = to.call{value: value}(data);
}
```

## Recommended Mitigation Steps
1. Implement a secure, decentralized governance mechanism for critical parameter changes and upgrades. This could involve a multi-signature scheme, a time-lock, or a voting system that allows stakeholders to participate in decision-making.

2. Limit the privileges of the owner and operator roles to the minimum necessary for the contract's operation. Avoid giving these roles the ability to arbitrarily change parameters or withdraw funds.

3. Implement emergency stop mechanisms that can be triggered by a diverse set of stakeholders (not just the owner) in case of a security incident or a malicious owner.

****************************************************

The `bootstrap` function, which creates the initial MIM-USDB liquidity pool, could potentially be front-run. If a malicious actor sees the `bootstrap` transaction in the mempool, they could try to create the pool first with their own parameters, potentially impacting the initial liquidity and token ratios.

However, the impact of this is limited because the `bootstrap` function can only be called once by the contract owner.

**BlastOnboarding:**
   - The `deposit`, `lock`, and `withdraw` functions could potentially be front-run. For example, if a large deposit is about to be made, a front-runner could try to deposit first to manipulate their share of the pool.
   - Similarly, if a large withdrawal is about to happen, a front-runner could try to withdraw first, potentially leaving less liquidity for the original withdrawer.

However, the impact of this is limited because the contract has a defined onboarding period, and the funds are not immediately available for trading.

**MagicLP:**
   - The `sellBase` and `sellQuote` functions, which execute swaps, are vulnerable to front-running. If a large swap transaction is detected in the mempool, a front-runner could try to execute their own swap first, affecting the price for the original swap.
   - This is a common problem in AMMs (Automated Market Makers) and can lead to MEV exploitation, where miners or other networked actors can profit from front-running or sandwich attacking trades.
   - The `buyShares` and `sellShares` functions, which add and remove liquidity, could also be front-run in a similar manner to impact the price or share of the pool.

**BlastMagicLP:**
   - Inherits the same vulnerabilities as MagicLP.

**BlastBox:**
   - The `deposit` and `withdraw` functions could potentially be front-run, similar to BlastOnboarding. A front-runner could try to deposit or withdraw before a large transaction to manipulate their share of the pool.

Other Contracts (BlastGovernor, BlastDapp, BlastPoints, BlastYields):
   - No significant front-running risks identified based on the provided code.

## Code
The vulnerability in MagicLP's [`sellBase`](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L244-L265) and [`sellQuote`](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L267-L288) functions is representative of the front-running risk:

```solidity
function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {
    uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
    uint256 baseInput = baseBalance - uint256(_BASE_RESERVE_);
    // ... Swap logic ...
}

function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {
    uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
    uint256 quoteInput = quoteBalance - uint256(_QUOTE_RESERVE_);
    // ... Swap logic ...
}
```

If a large `sellBase` or `sellQuote` transaction is detected in the mempool, a front-runner can attempt to execute their own trade first, affecting the price for the original trade.

## Recommended Mitigation Steps
None of the contracts implement commit-reveal schemes or batch auctions, which are common methods to prevent front-running.

- Implementing a commit-reveal scheme where users commit to a trade and reveal it later, making it harder for front-runners to know the details of the trade in advance.
- Using batch auctions, where trades are executed in batches at set intervals, reducing the granularity of MEV opportunities.
- Exploring MEV-resistant AMM designs, such as those that use cryptographic techniques to hide trade details until execution.
- Implementing front-running protection for critical functions, such as rate limiting, or requiring a minimum time delay between certain actions.

Several of the provided contracts, particularly MagicLP, are vulnerable to front-running and MEV exploitation due to the nature of their AMM design. While the impact is somewhat limited in the onboarding contracts due to their defined periods, the trading contracts are at higher risk. Implementing commit-reveal schemes, batch auctions, or exploring MEV-resistant AMM designs could help mitigate these risks.
