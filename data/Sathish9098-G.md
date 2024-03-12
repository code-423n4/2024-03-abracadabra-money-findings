# GAS OPTIMIZATIONS

## [G-1] State variables should be cached with memory variables 

Caching state variables in memory (often by assigning them to local variables) can be beneficial, especially when those state variables are accessed multiple times within a function. This practice reduces the cost associated with repeated state reads, which are more expensive than reading from memory

##

## [G-2] Merging multiple mappings into a single struct Mapping Saves gas

It's common to use mappings for storing data associated with specific addresses or IDs. If multiple mappings are used to store related data, combining them into a single mapping that maps addresses or IDs to a struct can optimize gas usage and improve code readability.

```diff
FILE: 2024-03-abracadabra-money/src/blast/BlastOnboarding.sol

mapping(address token => bool) public supportedTokens;
    mapping(address token => Balances) public totals;
    mapping(address token => uint256 cap) public caps;

    // Per-user
    mapping(address user => mapping(address token => Balances)) public balances;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L36-L41

##

## [G-2] Replacing Logical ANDs with nested If Statements to save gas

Using nested if statements instead of combining conditions with logical AND operators (&&) can result in gas savings, particularly in scenarios where most conditions are false. This approach ensures that once a condition is found to be false, subsequent conditions are not evaluated, reducing the overall computational effort. Saves 13 Gas

```solidity
FILE: 2024-03-abracadabra-money/src/blast/BlastOnboarding.sol

114: if (caps[token] > 0 && totals[token].total > caps[token]) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L114

##

## [G-3] ``deposit()`` function can be more gas optimized

Function deposit can be optimized for gas efficiency by minimizing redundant storage operations and optimizing conditional logic.

### Original Code

```solidity
FILE: 2024-03-abracadabra-money/src/blast/BlastOnboarding.sol

function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
    token.safeTransferFrom(msg.sender, address(this), amount);

    if (lock_) {
        totals[token].locked += amount;
        balances[msg.sender][token].locked += amount;
    } else {
        totals[token].unlocked += amount;
        balances[msg.sender][token].unlocked += amount;
    }

    totals[token].total += amount;

    if (caps[token] > 0 && totals[token].total > caps[token]) {
        revert ErrCapReached();
    }

    balances[msg.sender][token].total += amount;

    emit LogDeposit(msg.sender, token, amount, lock_);
}

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L101-L121

### Optimized Code

```solidity

function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
    token.safeTransferFrom(msg.sender, address(this), amount);

    // Combine the locked and unlocked updates to reduce redundant code
    uint256 previousTotal = totals[token].total; // Cache the previous total for cap comparison
    Balance storage userBalance = balances[msg.sender][token]; // Use storage reference to reduce repeated lookups

    if (lock_) {
        totals[token].locked += amount;
        userBalance.locked += amount;
    } else {
        totals[token].unlocked += amount;
        userBalance.unlocked += amount;
    }

    uint256 updatedTotal = previousTotal + amount;
    totals[token].total = updatedTotal; // Update total once after calculation

    // Check the cap with updated total to save gas on unnecessary condition evaluation
    if (caps[token] > 0 && updatedTotal > caps[token]) {
        revert ErrCapReached();
    }

    userBalance.total += amount; // Update user's total once after calculation

    emit LogDeposit(msg.sender, token, amount, lock_);
}

```
### Explanation
In the optimized code:

- The token's total amount (totals[token].total) is updated only once after determining whether the amount is locked or unlocked, reducing the number of writes.
- A single reference (userBalance) is used to interact with balances[msg.sender][token], minimizing repeated state variable lookups and thus reducing gas costs.
- The caps check uses the already updated updatedTotal, eliminating the need to access totals[token].total again.
- By caching the previousTotal before any changes, we ensure that the cap comparison is accurate without needing to read from storage twice.







