## [G-01] We can multiple mapping can be combined into a single mapping to a struct save `Storage slot`

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol

```solidity

36    mapping(address token => bool) public supportedTokens;
37    mapping(address token => Balances) public totals;
38    mapping(address token => uint256 cap) public caps;

```

We can save a storage slot by combining these mappings into a single mapping that uses a struct to store all of the related values for each token address:

```solidity

struct SupportedTokens_Caps {
    bool supportedTokens
    uint256 cap
}


mapping(address token => SupportedTokens_Caps )
```

Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (20000 gas) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save ~42 gas per access due to not having to recalculate the key’s keccak256 hash (Gkeccak256 - 30gas) and that calculation’s associated stack operations.

## [G-02] `BlastOnboarding.sol::Balances` remove total to save one storage slot

In the `Balances` struct, the `total` field can be calculated on the fly instead of being stored. This is because the `total` is just the sum of `unlocked` and `locked` balances. Storing it separately requires additional storage, which costs gas.

Here's how you can modify the `Balances` struct and the functions that use it:

```solidity
struct Balances {
    uint256 unlocked;
    uint256 locked;
}

function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
    token.safeTransferFrom(msg.sender, address(this), amount);

    if (lock_) {
        totals[token].locked += amount;
        balances[msg.sender][token].locked += amount;
    } else {
        totals[token].unlocked += amount;
        balances[msg.sender][token].unlocked += amount;
    }

    if (caps[token] > 0 && getTotal(token) > caps[token]) {
        revert ErrCapReached();
    }

    balances[msg.sender][token].total += amount;

    emit LogDeposit(msg.sender, token, amount, lock_);
}

function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
    balances[msg.sender][token].unlocked -= amount;
    balances[msg.sender][token].locked += amount;
    totals[token].unlocked -= amount;
    totals[token].locked += amount;

    emit LogLock(msg.sender, token, amount);
}

function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
    balances[msg.sender][token].unlocked -= amount;
    balances[msg.sender][token].total -= amount;
    totals[token].unlocked -= amount;
    totals[token].total -= amount;

    token.safeTransfer(msg.sender, amount);

    emit LogWithdraw(msg.sender, token, amount);
}

function getTotal(address token) public view returns (uint256) {
    return totals[token].unlocked + totals[token].locked;
}
```

In this modified version, I've removed the `total` field from the `Balances` struct and added a `getTotal` function that calculates and returns the total balance for a given token. The `deposit`, `lock`, and `withdraw` functions have been updated to use this new function. This change should save gas by reducing the amount of storage used by the contract.

```diff
+ function getTotal(address token) public view returns (uint256) {
+     return totals[token].unlocked + totals[token].locked;
+ }
```

## [G-03] In this `BlastOnboardingBoot.sol` contract we can remove the `claimed` mapping and use a different approach to check if a user has already claimed their shares `To Save a Storage Slot`

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol

1. Add a new `claimTime` variable to the `BlastOnboardingBootDataV1` contract to store the timestamp when the user claimed their shares:

   ```solidity
   uint256 public claimTime;
   ```

2. Modify the `claim` function in the `BlastOnboardingBoot` contract to set the `claimTime` variable instead of the `claimed` mapping:

   ```solidity
   function claim(bool lock) external returns (uint256 shares) {
       if (!ready) {
           revert ErrNotReady();
       }
       if (claimTime[msg.sender] != 0) {
           revert ErrAlreadyClaimed();
       }

       shares = _claimable(msg.sender);
       if (shares == 0) {
           revert ErrNothingToClaim();
       }

       claimTime[msg.sender] = block.timestamp;
       staking.stakeFor(msg.sender, shares, lock);

       emit LogClaimed(msg.sender, shares, lock);
   }
   ```

3. Modify the `claimable` function to check the `claimTime` variable instead of the `claimed` mapping:

   ```solidity
   function claimable(address user) external view returns (uint256 shares) {
       if (!ready || claimTime[user] != 0) {
           return 0;
       }

       return _claimable(user);
   }
   ```

By doing this, we can save a storage slot since we no longer need to store a separate boolean value for each user. Instead, we're using the `claimTime` variable to check if a user has already claimed their shares. The `claimTime` variable can also be used for other purposes, such as tracking when users claimed their shares.

## [G-04] Removing the `factory` state variable it's not being used elsewhere in `BlastOnboardingBoot` contract

The `factory` variable is set in the `initialize` function but it's not used in any other function in contract. If the contract doesn't need to access the `factory` later, you can remove it to save a storage slot.

1. Remove the `IFactory public factory;`
2. In the `initialize` function, remove the `factory = IFactory(router.factory());`

We can save one storage slot by removing an unused state variable.

## [G-05] In the `MagicLP` contract, one storage slot can be saved by combining the `_BASE_TOKEN_` and `_QUOTE_TOKEN_` state variables into a single state variable of type `address[2]`.

Currently, the contract has the following state variables:

```solidity
address public _BASE_TOKEN_;
address public _QUOTE_TOKEN_;
```

To save a storage slot, you can replace these two state variables with a single state variable:

```solidity
address[2] public tokens;
```

Then, in the `init` function, you can set the values of the `tokens` array as follows:

```solidity
tokens[0] = baseTokenAddress;
tokens[1] = quoteTokenAddress;
```

Finally, you will need to update all occurrences of `_BASE_TOKEN_` and `_QUOTE_TOKEN_` in the contract to use `tokens[0]` and `tokens[1]`, respectively. For example:

```solidity
_BASE_TOKEN_.safeTransfer(to, amount);
```

would become:

```solidity
tokens[0].safeTransfer(to, amount);
```

By combining the two state variables into a single array, you can save one storage slot. However, keep in mind that this change may require updates to any external contracts or off-chain code that interacts with the `MagicLP` contract.

## [G-06] We can use a single mapping that combines the `Factory::pools` and `Factory::userPools` mappings to save one storage slots

Instead of having separate mappings for `pools` and `userPools`, we can store both the token pair and the creator address as the keys in a single mapping.

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol

Here are the changes required to optimize the storage by using a single mapping:

Remove the following lines:

```solidity
mapping(address base => mapping(address quote => address[] pools)) public pools;
mapping(address creator => address[] pools) public userPools;
```

Add the following line:

```solidity
mapping(bytes32 => address[]) public pools;
```

Modify the error:

```solidity
error ErrInvalidPoolIndex();
```

Modify the `getPoolCount` function:

```solidity
function getPoolCount(address token0, address token1) external view returns (uint256) {
    return pools[_computeKey(token0, token1, address(0))].length;
}
```

Modify the `getUserPoolCount` function:

```solidity
function getUserPoolCount(address creator) external view returns (uint256 count) {
    bytes32 key = _computeKey(address(0), address(0), creator);
    count = pools[key].length;
}
```

Modify the `_addPool` function:

```solidity
function _addPool(address baseToken, address quoteToken, address creator, address pool) internal {
    bytes32 key = _computeKey(baseToken, quoteToken, creator);
    pools[key].push(pool);

    emit LogPoolAdded(baseToken, quoteToken, creator, pool);
}
```

Add the `_computeKey` function:

```solidity
function _computeKey(address baseToken, address quoteToken, address creator) internal pure returns (bytes32) {
    return keccak256(abi.encodePacked(baseToken, quoteToken, creator));
}
```

Modify the `removePool` function:

```solidity
function removePool(
    address baseToken,
    address quoteToken,
    address creator,
    uint256 poolIndex
) external onlyOwner {
    bytes32 key = _computeKey(baseToken, quoteToken, creator);
    address[] storage _pools = pools[key];

    if (poolIndex >= _pools.length) {
        revert ErrInvalidPoolIndex();
    }

    _pools[poolIndex] = _pools[_pools.length - 1];
    _pools.pop();

    emit LogPoolRemoved(_pools[poolIndex]);
}
```

These changes combine the `pools` and `userPools` mappings into a single mapping `pools`, where the key is computed using the `_computeKey` function, which takes the `baseToken`, `quoteToken`, and `creator` addresses as input.

We use a single mapping `pools` that combines the token pair and the creator address as the key. The key is computed using the `_computeKey` function, which takes the `baseToken`, `quoteToken`, and `creator` addresses as input.

- To get the pool count for a token pair, we call `getPoolCount` with `creator` set to `address(0)`.
- To get the pool count for a creator, we call `getUserPoolCount` with `baseToken` and `quoteToken` set to `address(0)`.

The `addPool` and `removePool` functions have been updated to use the new key computation and storage structure.

