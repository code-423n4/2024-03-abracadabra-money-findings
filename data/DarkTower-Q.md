# [L-01]: Removing supported tokens prevents users from withdrawing tokens from `BlastOnboarding`.

Due to the `onlySupportedTokens(token)` modifier, if the owner removes support for tokens, users can no longer withdraw their tokens and their funds will get stuck in the `BlastOnboarding`

Consider removing `onlySupportedTokens(token)` modifier for withdrawals.

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