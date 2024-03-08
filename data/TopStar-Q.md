### [L-1] Using `ERC721::_mint()` can be dangerous

Using `ERC721::_mint()` can mint ERC721 tokens to addresses which don't support ERC721 tokens. Use `_safeMint()` instead of `_mint()` for ERC721.


### [L-2] Weak Pseudo Random Number Generator in `MagicLP._twapUpdate()` 

The random number generator `blockTimestamp = uint32(block.timestamp % 2 ** 32)` in the contract `MagicLP.sol#546` is not truly random because it relies on factors like the sender's address, the current block's timestamp, and the block's difficulty. 