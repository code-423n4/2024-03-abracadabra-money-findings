# L-01 - `BlastOnboarding.sol::deposit()` is succeptible to re entrancy attack

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101-L121

In deposit, `token.safeTransferFrom` is triggered first and then all the state changes being done which can lead to exploits if the token is a token that gives control to the sender, like ERC777 tokens.

The safeTransferFrom should be the last call in deposit.