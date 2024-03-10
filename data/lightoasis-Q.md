## Using tx.origin goes against solidity best practices.

tx.orgin is used for the creator's address during the clone creation.
[Factory.sol#L82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/periphery/Factory.sol#L82)
```
    function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
 @>       address creator = tx.origin;

        bytes32 salt = _computeSalt(creator, baseToken_, quoteToken_, lpFeeRate_, i_, k_);
        clone = LibClone.cloneDeterministic(address(implementation), salt);
        IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);

        emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
        _addPool(creator, baseToken_, quoteToken_, clone);
    }
```
This goes against solidity best practices. tx.origin shouldn't be used for vvalidation or authorization.
see Solidity best practices: https://consensys.io/blog/solidity-best-practices-for-smart-contract-security and [swc](https://swcregistry.io/docs/SWC-115/)

## Recommendation
tx.origin should not be used for authorization. Use msg.sender instead.