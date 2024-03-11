## Gas Findings

|    | Issue | Instances | Total Gas Saved |
|----|-------|:---------:|:---------:|
| [G-01] | Contract storage can use fewer slots by changing the order of state variables | 1 | 20000 |
| [G-02] | Optimize Storage Layout in Structs by Truncating Time Related Fields | 1 | 20000 |
| [G-03] | A `memory` array's `length` should not be looked up in every iteration of a `for`/`while`-loop | 7 | 21 |
| [G-04] | `do`-`while` is cheaper than `for`-loops when the initial check can be skipped | 8 | 2040 |
| [G-05] | Use `assembly` for Efficient Event Emission | 59 | 22420 |
| [G-06] | Avoid Emitting Events Inside Loops | 2 | 800 |
| [G-07] | Enable IR-based code generation | 20 | - |
| [G-08] | Assembly: Check `msg.sender` using xor and the scratch space | 2 | 42 |
| [G-09] | Multiple `address`/ID mappings can be combined into a single `mapping` of an `address`/ID to a `struct` | 13 | - |
| [G-10] | Assembly: Use scratch space when building emitted events with two data arguments | 18 | 270 |
| [G-11] | Stack variable is only used once | 29 | 87 |
| [G-12] | Use `assembly` to write mutable storage values | 89 | 979 |
| [G-13] | Using `delete` on a `uint/int` variable is cheaper than assigning it to `0` | 2 | 16 |
| [G-14] | Optimize Ether Transfers with `receive()` Function | 7 | 315 |
| [G-15] | Use `revert()` to gain maximum gas savings | 109 | 5450 |
| [G-16] | Use local variables for emitting | 5 | 500 |
| [G-17] | `x.a = x.a + b` always cheaper than `x.a += b` for Structs | 22 | 110 |
| [G-18] | Initializers can be marked as payable | 2 | - |
| [G-19] | Using `constants` instead of `enum` can save gas | 2 | 0 |
| [G-20] | Create variable outside the loop | 16 | 320 |
| [G-21] | Nested for loops should be avoided due to high gas costs resulting from O^2 time complexity | 1 | 0 |
| [G-22] | Use bytes32 in place of string | 1 | 0 |
| [G-23] | Using `delete` on a `bool` variable is cheaper than assigning it to `false` | 1 | 24 |
| [G-24] | Use `Array.unsafeAccess()` to avoid repeated array length checks | 7 | 14700 |
| [G-25] | Counting down when iterating, saves gas | 1 | 9 |
| [G-26] | `>=` costs less gas than `>` | 14 | 84 |
| [G-27] | Consider pre-calculating the address of `address(this)` to save gas | 49 | 0 |
| [G-28] | Constructors can be marked `payable` | 13 | 312 |
| [G-29] | Split `revert` checks to save gas | 12 | - |
| [G-30] | Multiple accesses of a mapping/array should use a local variable cache | 35 | 4900 |
| [G-31] | Optimize Increment and Decrement in loops with `unchecked` keyword | 1 | 60 |
| [G-32] | Reduce gas usage by moving to Solidity 0.8.19 or later | 20 | - |
| [G-33] | Reduce deployment costs by tweaking contracts' metadata | 20 | 212000 |
| [G-34] | Use Pre-Increment/Decrement (++i/--i) to Save Gas | 1 | 5 |
| [G-35] | Nesting `if`-statements is cheaper than using `&&` | 11 | 66 |
| [G-36] | Use `storage` instead of `memory` for state structs/arrays | 3 | 6300 |
| [G-37] | Avoid transferring amounts of zero in order to save gas | 22 | 2200 |
| [G-38] | `>=` costs less gas than `>` | 70 | 210 |
| [G-39] | Cache Function Calls for Efficiency | 5 | - |
| [G-40] | Unutilized Named Return Variables Waste Gas Without Optimizer | 27 | - |
| [G-41] | Use `unchecked` for Math Operations if they already checked | 7 | 595 |
| [G-42] | Using `private` rather than `public`, saves gas | 71 | 1562000 |
| [G-43] | Use Assembly for Hash Calculations | 1 | 1005 |
| [G-44] | Refactor duplicated require()/revert() checks to save gas | 25 | - |
| [G-45] | Use Assembly for Efficient Memory Management in Multiple External Calls | 16 | 46000 |
| [G-46] | Cached Global Variables | 1 | 12 |
| [G-47] | Simple checks for zero `uint` can be done using `assembly` to save gas | 36 | 144 |
| [G-48] | Use Cached Contracts for Multiple External Calls | 4 | 672 |
| [G-49] | Consider using solady's `FixedPointMathLib` | 118 | - |
| [G-50] | Avoid Zero to Non-Zero Storage Writes Where Possible | 40 | 884000 |
| [G-51] | Consider Packing Small `uint` When it's Possible | 6 | 124800 |
| [G-52] | Consider Using `calldata` Instead of `memory` for Function Parameters | 1 | 300 |
| [G-53] | Use `unchecked` for division which do not divide by -X sonce they can't overflow | 40 | 800 |
| [G-54] | Minimize Gas Cost with Local Variables for State Writes in Loops | 2 | 800 |
| [G-55] | State Variables Should Be `immutable` Since They Are Only Set in the Constructor | 1 | 2100 |
| [G-56] | Use solady library where possible to save gas | 8 | 8000 |
| [G-57] | Use `uint256(1)`/`uint256(2)` instead of `true`/`false` to save gas for changes | 7 | 119000 |
| [G-58] | Use Bit Shifting for Multiplication by Powers of Two | 3 | 60 |
| [G-59] | Delete Unused State Variables | 2 | 40000 |
| [G-60] | Avoid contract existence checks by using low-level calls | 188 | 18800 |
| [G-61] | Consider Using Mappings Instead of Arrays to Save Gas | 1 | 2102 |
| [G-62] | Mark Functions That Revert For Normal Users As `payable` | 53 | 1113 |
| [G-63] | Prefer `private` over `public` for Constants to Save Gas | 8 | 24000 |
| [G-64] | `<x> += <y>` costs more gas than `<x> = <x> + <y>` for state variables | 9 | 1017 |
| [G-65] | Using `bool`s for storage incurs overhead | 7 | 700 |
| [G-66] | Optimize Gas by Using Only Named Returns | 56 | 2464 |
| [G-67] | Cache State Variable Reads Outside Loops | 1 | 265 |
| [G-68] | Usage of `uints`/`ints` smaller than 32 bytes (256 bits) incurs overhead | 45 | 270 |
| [G-69] | Unlimited gas consumption risk due to external call recipients | 1 | - |
| [G-70] | Use assembly to check for `address(0)` | 26 | 1508 |
| [G-71] | `internal`/`private` functions only called once can be inlined to save gas | 11 | 220 |
| [G-72] | Consider using OZ EnumerateSet in place of nested mappings | 4 | 4000 |
| [G-73] | Declare `immutable` as `private` to save gas | 15 | 45000 |
| [G-74] | State variables should be cached in stack rather than re-reading them from storage | 52 | 6887 |
| [G-75] | Division by powers of two should use bit shifting | 4 | 80 |
| [G-76] | Optimize names to save gas | 24 | 480 |
| [G-77] | Avoid updating storage when the value hasn't changed | 19 | 15200 |
| [G-78] | Optimize External Calls with Assembly for Memory Efficiency | 43 | 9460 |

## Gas Findings Details

### [G-01] Contract storage can use fewer slots by changing the order of state variables

The reduction of slots can reduce the gas consumption of each storage read/write operation.
If variables occupying the same slot are written within the same transaction, avoids a separate Gsset (20000 gas).
Reads of the variables can also be cheaper.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit - State variables use 7 storage slots, but can be packed to 6 storage slots.
//	mapping(address user => bool claimed) public claimed
//	LockingMultiRewards public staking
//	uint256 public totalPoolShares
//	IFactory public factory
//	Router public router
//	address public pool
//	bool public ready

34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1
```
[34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L34)
</details>

### [G-02] Optimize Storage Layout in Structs by Truncating Time Related Fields

The field ordering within the following structs isn't optimized for efficient storage in the Ethereum Virtual Machine (EVM). By appropriately rearranging the fields within these structs, you can achieve improved gas efficiency during interactions with these structs. 

In the context of EVM, a well-structured and optimized struct can save a substantial amount of gas. For instance, packing the struct into fewer storage slots could avoid an extra SSTORE operation (costing 20000 gas) during the first setting of the struct. Subsequent read and write operations also experience reduced gas consumption due to optimized struct layout.

Please consider rearranging the fields in the identified structs to capitalize on these potential gas savings and improve overall contract performance.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit - Packed struct used 4 storage slots, but can be packed to 3 storage slots.
//	struct Reward {
//	    uint256 rewardPerTokenStored;
//	    uint256 rewardRate;
//	    uint32 lastUpdateTime;
//	    uint32 periodFinish;
//	    bool exists;
//	}
50: struct Reward {
        uint256 periodFinish;
        uint256 rewardRate;
        uint256 rewardPerTokenStored;
        bool exists;
        uint248 lastUpdateTime;
    }
```
[50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L50)
</details>

### [G-03] A `memory` array's `length` should not be looked up in every iteration of a `for`/`while`-loop

It is more efficient to cache the array length instead of looking it up in every iteration of a for-loop.

Example:

```solidity
- for(uint i = 0; i < array.length; i++)
+ uint length = array.length;
+ for(uint i = 0; i < length; i++);
```

<details>
<summary><i>7 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

165: for (uint256 i = 0; i < tokens.length; i++) {
```
[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)

```solidity
File: src/staking/LockingMultiRewards.sol

405: for (uint256 i; i < users.length; ) {
547: for (uint256 i; i < rewardTokens.length; ) {
561: for (uint256 i; i < rewardTokens.length; ) {
575: for (uint256 i; i < rewardTokens.length; ) {
580: for (uint256 j; j < users.length; ) {
614: for (uint256 i; i < rewardTokens.length; ) {
```
[405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405) | [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547) | [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561) | [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575) | [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580) | [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614)
</details>

### [G-04] `do`-`while` is cheaper than `for`-loops when the initial check can be skipped

Using `do-while` loops instead of `for` loops can be more gas-efficient. 
Even if you add an `if` condition to account for the case where the loop doesn't execute at all, a `do-while` loop can still be cheaper in terms of gas.

Example:
```solidity
/// 774 gas cost
function forLoop() public pure {
    for (uint256 i; i < 10;) {
        unchecked {
            ++i;
        }
    }
}
/// 519 gas cost
function doWhileLoop() public pure {
    uint256 i;
    do {
        unchecked {
            ++i;
        }
    } while (i < 10);
}
```

<details>
<summary><i>8 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

165: for (uint256 i = 0; i < tokens.length; i++)
```
[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)

```solidity
File: src/mimswap/periphery/Router.sol

544: for (uint256 i = 0; i < iterations; )
```
[544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544)

```solidity
File: src/staking/LockingMultiRewards.sol

405: for (uint256 i; i < users.length; )
547: for (uint256 i; i < rewardTokens.length; )
561: for (uint256 i; i < rewardTokens.length; )
575: for (uint256 i; i < rewardTokens.length; )
580: for (uint256 j; j < users.length; )
614: for (uint256 i; i < rewardTokens.length; )
```
[405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405) | [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547) | [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561) | [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575) | [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580) | [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614)
</details>

### [G-05] Use `assembly` for Efficient Event Emission

To efficiently emit events, consider utilizing assembly by making use of scratch space and the free memory pointer.
This approach can potentially avoid the costs associated with memory expansion.

However, it's crucial to cache and restore the free memory pointer for safe optimization.
Good examples of such practices can be found in well-optimized [Solady's codebases](https://github.com/Vectorized/solady/blob/main/src/tokens/ERC1155.sol#L167).
Please review your code and consider the potential gas savings of this approach.

<details>
<summary><i>59 issue instances in 11 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

78: emit LogFeeToChanged(feeTo_)
90: emit LogTokenDepositEnabled(token, enabled)
```
[78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L78) | [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L90)

```solidity
File: src/blast/BlastGovernor.sol

46: emit LogFeeToChanged(_feeTo)
```
[46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L46)

```solidity
File: src/blast/BlastMagicLP.sol

86: emit LogFeeToChanged(feeTo_)
91: emit LogOperatorChanged(operator, status)
```
[86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L86) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L91)

```solidity
File: src/blast/BlastOnboarding.sol

120: emit LogDeposit(msg.sender, token, amount, lock_)
129: emit LogLock(msg.sender, token, amount)
140: emit LogWithdraw(msg.sender, token, amount)
153: emit LogFeeToChanged(feeTo_)
182: emit LogTokenSupported(token, supported)
187: emit LogTokenCapChanged(token, cap)
192: emit LogBootstrapperChanged(bootstrapper_)
197: emit LogStateChange(State.Opened)
202: emit LogStateChange(State.Closed)
211: emit LogTokenRescue(token, to, amount)
```
[120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L120) | [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L129) | [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L140) | [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L153) | [182](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L182) | [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L187) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L192) | [197](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L197) | [202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L202) | [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L211)

```solidity
File: src/blast/BlastOnboardingBoot.sol

71: emit LogClaimed(msg.sender, shares, lock)
124: emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares)
132: emit LogInitialized(_router)
143: emit LogStakingChanged(address(_staking))
148: emit LogReadyChanged(ready)
```
[71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L71) | [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L132) | [143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L143) | [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148)

```solidity
File: src/blast/BlastTokenRegistry.sol

20: emit LogNativeYieldTokenEnabled(token, enabled)
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L20)

```solidity
File: src/blast/libraries/BlastYields.sol

26: emit LogBlastTokenClaimableEnabled(address(this), token)
31: emit LogBlastNativeClaimableEnabled(address(this))
44: emit LogBlastGasClaimed(recipient, amount)
57: emit LogBlastETHClaimed(recipient, amount)
62: emit LogBlastETHClaimed(recipient, amount)
72: emit LogBlastTokenClaimed(recipient, address(token), amount)
77: emit LogBlastTokenClaimed(recipient, address(token), amount)
```
[26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L26) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L31) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L44) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L57) | [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L62) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L72) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L77)

```solidity
File: src/mimswap/MagicLP.sol

259: emit RChange(newRState)
264: emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to)
282: emit RChange(newRState)
287: emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to)
323: emit RChange(newRState)
325: emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo)
345: emit RChange(newRState)
347: emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo)
352: emit FlashLoan(msg.sender, assetTo, baseAmount, quoteAmount)
409: emit BuyShares(to, shares, balanceOf(to))
454: emit SellShares(msg.sender, to, shareAmount, balanceOf(msg.sender))
467: emit TokenRescue(token, to, amount)
501: emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance)
```
[259](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L259) | [264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L264) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L282) | [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L287) | [323](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L323) | [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L325) | [345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L345) | [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L347) | [352](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L352) | [409](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L409) | [454](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L454) | [467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L467) | [501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L501)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

52: emit LogMaintainerChanged(maintainer_)
59: emit LogImplementationChanged(implementation_)
```
[52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L52) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L59)

```solidity
File: src/mimswap/periphery/Factory.sol

88: emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_)
102: emit LogSetImplementation(implementation_)
111: emit LogSetMaintainerFeeRateModel(maintainerFeeRateModel_)
141: emit LogPoolRemoved(pool)
152: emit LogPoolAdded(baseToken, quoteToken, creator, pool)
```
[88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88) | [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L102) | [111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L111) | [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L141) | [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L152)

```solidity
File: src/staking/LockingMultiRewards.sol

183: emit LogWithdrawn(msg.sender, amount)
318: emit LogSetMinLockAmount(minLockAmount, _minLockAmount)
331: emit LogRecovered(tokenAddress, tokenAmount)
392: emit LogRewardAdded(amount)
436: emit LogLockIndexChanged(user, lastIndex, index)
447: emit LogUnlocked(user, amount, index)
475: emit LogStaked(account, amount)
513: emit LogLocked(user, amount, _nextUnlockTime, lockCount)
611: emit LogRewardLockCreated(user, _rewardLock.unlockTime)
638: emit LogRewardPaid(user, rewardToken, amount)
651: emit LogRewardLocked(user, rewardToken, rewardAmount)
```
[183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L183) | [318](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L318) | [331](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L331) | [392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L392) | [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L436) | [447](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L447) | [475](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L475) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L513) | [611](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L611) | [638](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L638) | [651](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L651)
</details>

### [G-06] Avoid Emitting Events Inside Loops

Emitting an event inside a loop performs a LOG operation N times, where N is the loop length.
Consider refactoring the code to emit the event only once at the end of the loop.
Gas savings should be multiplied by the average loop length.
This approach can improve the gas efficiency of your contract and make transaction costs more predictable for users.

<details>
<summary><i>2 issue instances in 1 files:</i></summary>

```solidity
File: src/staking/LockingMultiRewards.sol

436: emit LogLockIndexChanged(user, lastIndex, index)
638: emit LogRewardPaid(user, rewardToken, amount)
```
[436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L436) | [638](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L638)
</details>

### [G-07] Enable IR-based code generation

The `--via-ir` command line option activates the IR-based code generator in Solidity, which is designed to enable powerful optimization passes that can span across functions. The end result may be a contract that requires less gas to execute its functions.

We recommend you enable this feature, run tests, and benchmark the gas usage of your contract to evaluate if it leads to any tangible gas savings. Experimenting with this feature could lead to a more gas-efficient contract.

[Solidity Documentation](https://docs.soliditylang.org/en/v0.8.20/ir-breaking-changes.html#solidity-ir-based-codegen-changes).

<details>
<summary><i>20 issue instances in 1 files:</i></summary>

```solidity

File: src/blast/BlastDapp.sol
File: src/blast/BlastBox.sol
File: src/blast/BlastGovernor.sol
File: src/blast/BlastMagicLP.sol
File: src/blast/BlastOnboarding.sol
File: src/blast/BlastOnboardingBoot.sol
File: src/blast/BlastTokenRegistry.sol
File: src/blast/BlastWrappers.sol
File: src/blast/libraries/BlastPoints.sol
File: src/blast/libraries/BlastYields.sol
File: src/mimswap/MagicLP.sol
File: src/mimswap/auxiliary/FeeRateModel.sol
File: src/mimswap/auxiliary/FeeRateModelImpl.sol
File: src/mimswap/libraries/DecimalMath.sol
File: src/mimswap/libraries/Math.sol
File: src/mimswap/libraries/PMMPricing.sol
File: src/mimswap/periphery/Factory.sol
File: src/mimswap/periphery/Router.sol
File: src/oracles/aggregators/MagicLpAggregator.sol
File: src/staking/LockingMultiRewards.sol
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L1) | [1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L1)
</details>

### [G-08] Assembly: Check `msg.sender` using xor and the scratch space

See [this](https://code4rena.com/reports/2023-05-juicebox#g-06-use-assembly-to-validate-msgsender) prior finding for details on the conversion

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastMagicLP.sol

119: if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
```
[119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119)

```solidity
File: src/mimswap/MagicLP.sol

608: if (msg.sender != implementation.owner()) {
```
[608](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L608)
</details>

### [G-09] Multiple `address`/ID mappings can be combined into a single `mapping` of an `address`/ID to a `struct`

Combining multiple address/ID mappings into a single mapping to a struct can lead to gas savings.
By refactoring multiple mappings into a singular mapping with a struct, you can save on storage slots, which in turn can reduce the gas cost in certain operations.
Prioritize this refactor if optimizing gas is a primary concern for your contract's operations.

<details>
<summary><i>13 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

36: mapping(address token => bool) public supportedTokens
37: mapping(address token => Balances) public totals
38: mapping(address token => uint256 cap) public caps
41: mapping(address user => mapping(address token => Balances)) public balances
```
[36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L37) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L38) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L41)

```solidity
File: src/mimswap/periphery/Factory.sol

35: mapping(address base => mapping(address quote => address[] pools)) public pools
36: mapping(address creator => address[] pools) public userPools
```
[35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L35) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L36)

```solidity
File: src/staking/LockingMultiRewards.sol

89: mapping(address token => Reward info) private _rewardData
90: mapping(address user => Balances balances) private _balances
91: mapping(address user => LockedBalance[] locks) private _userLocks
92: mapping(address user => RewardLock rewardLock) private _userRewardLock
94: mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid
95: mapping(address user => mapping(address token => uint256 amount)) public rewards
96: mapping(address user => uint256 index) public lastLockIndex
```
[89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L89) | [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L90) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L91) | [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L92) | [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L94) | [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L95) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L96)
</details>

### [G-10] Assembly: Use scratch space when building emitted events with two data arguments

Using the scratch space for more than one, but at most two words worth of data (non-indexed arguments) will save gas over needing Solidity's abi memory expansion used for emitting normally.

<details>
<summary><i>18 issue instances in 5 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

120: emit LogDeposit(msg.sender, token, amount, lock_)
```
[120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L120)

```solidity
File: src/blast/BlastOnboardingBoot.sol

71: emit LogClaimed(msg.sender, shares, lock)
```
[71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L71)

```solidity
File: src/mimswap/MagicLP.sol

264: emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to)
287: emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to)
325: emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo)
347: emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo)
352: emit FlashLoan(msg.sender, assetTo, baseAmount, quoteAmount)
409: emit BuyShares(to, shares, balanceOf(to))
454: emit SellShares(msg.sender, to, shareAmount, balanceOf(msg.sender))
467: emit TokenRescue(token, to, amount)
501: emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance)
```
[264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L264) | [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L287) | [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L325) | [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L347) | [352](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L352) | [409](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L409) | [454](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L454) | [467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L467) | [501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L501)

```solidity
File: src/mimswap/periphery/Factory.sol

88: emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_)
152: emit LogPoolAdded(baseToken, quoteToken, creator, pool)
```
[88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88) | [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L152)

```solidity
File: src/staking/LockingMultiRewards.sol

318: emit LogSetMinLockAmount(minLockAmount, _minLockAmount)
331: emit LogRecovered(tokenAddress, tokenAmount)
436: emit LogLockIndexChanged(user, lastIndex, index)
447: emit LogUnlocked(user, amount, index)
513: emit LogLocked(user, amount, _nextUnlockTime, lockCount)
```
[318](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L318) | [331](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L331) | [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L436) | [447](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L447) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L513)
</details>

### [G-11] Stack variable is only used once

If the variable is only accessed once, it's cheaper to use the assigned value directly that one time, and save the 3 gas the extra stack assignment would spend

<details>
<summary><i>29 issue instances in 8 files:</i></summary>

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit - `feeTo_` variable
48: address feeTo_ = BlastMagicLP(address(implementation)).feeTo()
```
[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L48)

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit - `baseAmount` variable
87: uint256 baseAmount = totals[MIM].locked
/// @audit - `quoteAmount` variable
88: uint256 quoteAmount = totals[USDB].locked
/// @audit - `baseAmount` variable
101: uint256 baseAmount = totals[MIM].locked
/// @audit - `quoteAmount` variable
102: uint256 quoteAmount = totals[USDB].locked
/// @audit - `userLocked` variable
162: uint256 userLocked = balances[user][MIM].locked + balances[user][USDB].locked
```
[87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L87) | [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L88) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L101) | [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L102) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L162)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit - `baseBalance` variable
431: uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this))
/// @audit - `quoteBalance` variable
432: uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this))
```
[431](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L431) | [432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L432)

```solidity
File: src/mimswap/libraries/Math.sol

/// @audit - `remainder` variable
21: uint256 remainder = a - quotient * b
/// @audit - `V0V0V1V2` variable
62: uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2)
/// @audit - `penalty` variable
63: uint256 penalty = DecimalMath.mulFloor(k, V0V0V1V2)
/// @audit - `premium` variable
101: uint256 premium = DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2) + DecimalMath.ONE
/// @audit - `denominator` variable
188: uint256 denominator = (DecimalMath.ONE - k) * 2
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L21) | [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L63) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L101) | [188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L188)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit - `salt` variable
84: bytes32 salt = _computeSalt(creator, baseToken_, quoteToken_, lpFeeRate_, i_, k_)
```
[84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L84)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit - `baseBalance` variable
252: uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp))
/// @audit - `quoteBalance` variable
253: uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp))
/// @audit - `baseBalance` variable
515: uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount
/// @audit - `quoteBalance` variable
516: uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount
```
[252](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L252) | [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L253) | [515](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L515) | [516](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L516)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

/// @audit - `minAnswer` variable
40: uint256 minAnswer = baseAnswerNomalized < quoteAnswerNormalized ? baseAnswerNomalized : quoteAnswerNormalized
```
[40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L40)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit - `timeElapsed` variable
282: uint256 timeElapsed = lastTimeRewardApplicable_ - _rewardData[rewardToken].lastUpdateTime
/// @audit - `pendingRewardsPerToken` variable
283: uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_
/// @audit - `pendingUserRewardsPerToken` variable
293: uint256 pendingUserRewardsPerToken = rewardPerToken_ - userRewardPerTokenPaid[user][rewardToken]
/// @audit - `bal` variable
480: Balances storage bal = _balances[user]
/// @audit - `totalSupply_` variable
545: uint256 totalSupply_ = totalSupply()
/// @audit - `balance` variable
558: uint256 balance = balanceOf(user)
/// @audit - `totalSupply_` variable
559: uint256 totalSupply_ = totalSupply()
/// @audit - `totalSupply_` variable
573: uint256 totalSupply_ = totalSupply()
/// @audit - `rewardPerToken_` variable
577: uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_)
/// @audit - `rewardItemLength` variable
605: uint256 rewardItemLength = _rewardLock.items.length
```
[282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L282) | [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283) | [293](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L293) | [480](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L480) | [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L545) | [558](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L558) | [559](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L559) | [573](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L573) | [577](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L577) | [605](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L605)
</details>

### [G-12] Use `assembly` to write mutable storage values

Writing to storage using `assembly` is more gas efficient.
```solidity
    function writeStorage() external {
        // storageNumber = 10; // 2358 gas
        // assembly {
        //     sstore(storageNumber.slot, 10) // 2350 gas
        // }
        // storageAddr = 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc3; // 2411 gas
        // assembly {
        //     sstore(storageAddr.slot, 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc3) // 2350 gas
        // }
    }
```

<details>
<summary><i>89 issue instances in 12 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

33: feeTo = feeTo_
77: feeTo = feeTo_
82: enabledTokens[token] = enabled
```
[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L33) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L77) | [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L82)

```solidity
File: src/blast/BlastGovernor.sol

20: feeTo = feeTo_
45: feeTo = _feeTo
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L20) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L45)

```solidity
File: src/blast/BlastMagicLP.sol

32: feeTo = feeTo_
85: feeTo = feeTo_
90: operators[operator] = status
```
[32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L32) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L85) | [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L90)

```solidity
File: src/blast/BlastOnboarding.sol

93: registry = registry_
94: feeTo = feeTo_
152: feeTo = feeTo_
176: supportedTokens[token] = supported
186: caps[token] = cap
191: bootstrapper = bootstrapper_
196: state = State.Opened
201: state = State.Closed
```
[93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L93) | [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L94) | [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L152) | [176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L176) | [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L186) | [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L191) | [196](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L196) | [201](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L201)

```solidity
File: src/blast/BlastOnboardingBoot.sol

68: claimed[msg.sender] = true
106: (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount)
117: staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this))
130: router = Router(payable(_router))
131: factory = IFactory(router.factory())
142: staking = _staking
147: ready = _ready
```
[68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L68) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106) | [117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117) | [130](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L130) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L131) | [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L142) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L147)

```solidity
File: src/blast/BlastTokenRegistry.sol

19: nativeYieldTokens[token] = enabled
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L19)

```solidity
File: src/blast/BlastWrappers.sol

71: blacklistedCallees[address(BlastYields.BLAST_YIELD_PRECOMPILE)] = true
```
[71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L71)

```solidity
File: src/mimswap/MagicLP.sol

88: _INITIALIZED_ = true
118: _INITIALIZED_ = true
119: _BASE_TOKEN_ = baseTokenAddress
120: _QUOTE_TOKEN_ = quoteTokenAddress
121: _I_ = i
122: _K_ = k
123: _LP_FEE_RATE_ = lpFeeRate
124: _MT_FEE_RATE_MODEL_ = IFeeRateModel(mtFeeRateModel)
125: _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32)
140: _RState_ = uint32(PMMPricing.RState.ONE)
141: _BASE_TARGET_ = _BASE_RESERVE_
142: _QUOTE_TARGET_ = _QUOTE_RESERVE_
145: _RState_ = uint32(PMMPricing.RState.ONE)
146: _BASE_TARGET_ = _BASE_RESERVE_
147: _QUOTE_TARGET_ = _QUOTE_RESERVE_
257: _BASE_TARGET_ = newBaseTarget.toUint112()
258: _RState_ = uint32(newRState)
280: _QUOTE_TARGET_ = newQuoteTarget.toUint112()
281: _RState_ = uint32(newRState)
321: _QUOTE_TARGET_ = newQuoteTarget.toUint112()
322: _RState_ = uint32(newRState)
343: _BASE_TARGET_ = newBaseTarget.toUint112()
344: _RState_ = uint32(newRState)
382: _BASE_TARGET_ = shares.toUint112()
383: _QUOTE_TARGET_ = DecimalMath.mulFloor(shares, _I_).toUint112()
402: _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112()
403: _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112()
438: _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares))
439: _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares))
493: _LP_FEE_RATE_ = uint64(newLpFeeRate)
494: _K_ = uint64(newK)
495: _I_ = uint128(newI)
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_))
514: _BASE_RESERVE_ = uint112(baseBalance)
517: _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_))
518: _QUOTE_RESERVE_ = uint112(quoteBalance)
536: _BASE_RESERVE_ = uint112(baseBalance)
537: _QUOTE_RESERVE_ = uint112(quoteBalance)
538: _BASE_TARGET_ = uint112(baseBalance)
539: _QUOTE_TARGET_ = uint112(quoteBalance)
540: _RState_ = uint32(PMMPricing.RState.ONE)
557: _BLOCK_TIMESTAMP_LAST_ = blockTimestamp
561: _BASE_RESERVE_ = baseReserve.toUint112()
562: _QUOTE_RESERVE_ = quoteReserve.toUint112()
572: _BASE_RESERVE_ = baseBalance.toUint112()
575: _QUOTE_RESERVE_ = quoteBalance.toUint112()
```
[88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L88) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L118) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L119) | [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L120) | [121](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L121) | [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L122) | [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L123) | [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L124) | [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L125) | [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L140) | [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L141) | [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L142) | [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L145) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L146) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L147) | [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L257) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L258) | [280](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L280) | [281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L281) | [321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L321) | [322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L322) | [343](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L343) | [344](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L344) | [382](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L382) | [383](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L383) | [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402) | [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403) | [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439) | [493](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L493) | [494](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L494) | [495](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L495) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [514](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L514) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517) | [518](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L518) | [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L536) | [537](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L537) | [538](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L538) | [539](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L539) | [540](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L540) | [557](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L557) | [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L561) | [562](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L562) | [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L572) | [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L575)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

27: maintainer = maintainer_
51: maintainer = maintainer_
58: implementation = implementation_
```
[27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L27) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L51) | [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L58)

```solidity
File: src/mimswap/periphery/Factory.sol

45: implementation = implementation_
46: maintainerFeeRateModel = maintainerFeeRateModel_
101: implementation = implementation_
110: maintainerFeeRateModel = maintainerFeeRateModel_
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L45) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L46) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L101) | [110](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L110)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

43: baseReserve = baseReserve * (10 ** (WAD - baseDecimals))
44: quoteReserve = quoteReserve * (10 ** (WAD - quoteDecimals))
```
[43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L43) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L44)

```solidity
File: src/staking/LockingMultiRewards.sol

314: _rewardData[rewardToken].exists = true
319: minLockAmount = _minLockAmount
431: lastLockIndex[user] = index
502: lastLockIndex[user] = lockCount
532: _rewardData[token_].rewardPerTokenStored = rewardPerToken_
533: _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_)
537: rewards[user_][token_] = _earned(user_, balance_, token_, rewardPerToken_)
538: userRewardPerTokenPaid[user_][token_] = rewardPerToken_
619: rewards[user][rewardToken] = 0
```
[314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L314) | [319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L319) | [431](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L431) | [502](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L502) | [532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L532) | [533](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L533) | [537](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L537) | [538](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L538) | [619](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L619)
</details>

### [G-13] Using `delete` on a `uint/int` variable is cheaper than assigning it to `0`

```solidity
function test() external {
    delete foo; // 5148 gas
    foo = 0; // 5156 gas
}
```

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/libraries/Math.sol

154: temp = 0
```
[154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L154)

```solidity
File: src/staking/LockingMultiRewards.sol

619: rewards[user][rewardToken] = 0
```
[619](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L619)
</details>

### [G-14] Optimize Ether Transfers with `receive()` Function

Consider using `receive()` function instead of a specific `deposit()` (or similar) function.
If there are several functions in the contract that can receive Ether, it is recommended to use `receive()` for the most frequently used function.
```solidity
function deposit() external payable { // 5401 gas
    // your logic
}

receive() external payable {  // 5356 gas
    // your logic
}
```

The `receive()` or `fallback()` function can handle incoming Ether transfers directly, providing more gas-efficient way to manage deposits.

<details>
<summary><i>7 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastWrappers.sol

59: function init(bytes calldata data) public payable override
```
[59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59)

```solidity
File: src/mimswap/periphery/Router.sol

73: function createPoolETH(
        address token,
        bool useTokenAsQuote,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 tokenInAmount
    ) external payable returns (address clone, uint256 shares)
192: function addLiquidityETH(
        address lp,
        address to,
        address payable refundTo,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares)
229: function addLiquidityETHUnsafe(
        address lp,
        address to,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 shares)
336: function swapETHForTokens(
        address to,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut)
415: function sellBaseETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut)
461: function sellQuoteETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut)
```
[73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L73) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192) | [229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229) | [336](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336) | [415](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L415) | [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L461)
</details>

### [G-15] Use `revert()` to gain maximum gas savings

If you dont need Error messages, or you want gain maximum gas savings - `revert()` is a cheapest way to revert transaction in terms of gas.
```solidity
    revert(); // 117 gas 
    require(false); // 132 gas
    revert CustomError(); // 157 gas
    assert(false); // 164 gas
    revert("Custom Error"); // 406 gas
    require(false, "Custom Error"); // 421 gas
```


<details>
<summary><i>109 issue instances in 13 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

26: revert ErrZeroAddress()
29: revert ErrZeroAddress()
44: revert ErrUnsupportedToken()
58: revert ErrUnsupportedToken()
74: revert ErrZeroAddress()
```
[26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L26) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L29) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L44) | [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L58) | [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L74)

```solidity
File: src/blast/BlastGovernor.sol

17: revert ErrZeroAddress()
42: revert ErrZeroAddress()
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L17) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L42)

```solidity
File: src/blast/BlastMagicLP.sol

25: revert ErrZeroAddress()
28: revert ErrZeroAddress()
82: revert ErrZeroAddress()
120: revert ErrNotAllowedImplementationOperator()
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L25) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L28) | [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L82) | [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L120)

```solidity
File: src/blast/BlastOnboarding.sol

45: revert ErrWrongState()
52: revert ErrUnsupportedToken()
81: revert ErrUnsupported()
86: revert ErrZeroAddress()
90: revert ErrZeroAddress()
115: revert ErrCapReached()
149: revert ErrZeroAddress()
167: revert ErrUnsupportedToken()
207: revert ErrNotAllowed()
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L45) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L52) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L81) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L86) | [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L90) | [115](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L115) | [149](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L149) | [167](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L167) | [207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L207)

```solidity
File: src/blast/BlastOnboardingBoot.sol

57: revert ErrNotReady()
60: revert ErrAlreadyClaimed()
65: revert ErrNothingToClaim()
98: revert ErrAlreadyBootstrapped()
109: revert ErrInsufficientAmountOut()
139: revert ErrCannotChangeOnceReady()
```
[57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L57) | [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L60) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L65) | [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L98) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L109) | [139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L139)

```solidity
File: src/blast/BlastTokenRegistry.sol

16: revert ErrZeroAddress()
```
[16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L16)

```solidity
File: src/blast/BlastWrappers.sol

22: revert ErrZeroAddress()
36: revert ErrZeroAddress()
49: revert ErrZeroAddress()
52: revert ErrInvalidGovernorAddress()
61: revert ErrInvalidGovernorAddress()
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L22) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L36) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L49) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L52) | [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L61)

```solidity
File: src/mimswap/MagicLP.sol

100: revert ErrInitialized()
103: revert ErrZeroAddress()
106: revert ErrBaseQuoteSame()
109: revert ErrInvalidI()
112: revert ErrInvalidK()
115: revert ErrInvalidLPFeeRate()
303: revert ErrFlashLoanFailed()
316: revert ErrFlashLoanFailed()
338: revert ErrFlashLoanFailed()
370: revert ErrNoBaseInput()
378: revert ErrZeroQuoteAmount()
386: revert ErrZeroQuoteTarget()
390: revert ErrMintAmountNotEnough()
422: revert ErrExpired()
425: revert ErrNotEnough()
428: revert ErrSellBackNotAllowed()
442: revert ErrWithdrawNotEnough()
463: revert ErrNotAllowed()
481: revert ErrReserveAmountNotEnough()
484: revert ErrInvalidI()
487: revert ErrInvalidK()
490: revert ErrInvalidLPFeeRate()
509: revert ErrOverflow()
533: revert ErrOverflow()
595: revert ErrMintAmountNotEnough()
609: revert ErrNotImplementationOwner()
616: revert ErrNotClone()
623: revert ErrNotImplementation()
```
[100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L100) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L103) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L106) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L109) | [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L112) | [115](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L115) | [303](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L303) | [316](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L316) | [338](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L338) | [370](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L370) | [378](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L378) | [386](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L386) | [390](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L390) | [422](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L422) | [425](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L425) | [428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L428) | [442](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L442) | [463](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L463) | [481](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L481) | [484](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L484) | [487](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L487) | [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L490) | [509](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L509) | [533](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L533) | [595](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L595) | [609](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L609) | [616](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L616) | [623](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L623)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

24: revert ErrZeroAddress()
48: revert ErrZeroAddress()
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L24) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L48)

```solidity
File: src/mimswap/libraries/Math.sol

53: revert ErrIsZero()
133: revert ErrIsZero()
193: revert ErrIsZero()
```
[53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L53) | [133](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L133) | [193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L193)

```solidity
File: src/mimswap/periphery/Factory.sol

40: revert ErrZeroAddress()
43: revert ErrZeroAddress()
98: revert ErrZeroAddress()
107: revert ErrZeroAddress()
135: revert ErrInvalidUserPoolIndex()
```
[40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L40) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L43) | [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L98) | [107](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L107) | [135](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L135)

```solidity
File: src/mimswap/periphery/Router.sol

40: revert ErrZeroAddress()
49: revert ErrExpired()
213: revert ErrNotETHLP()
240: revert ErrNotETHLP()
305: revert ErrNotETHLP()
356: revert ErrInTokenNotETH()
386: revert ErrOutTokenNotETH()
424: revert ErrInvalidBaseToken()
440: revert ErrInvalidQuoteToken()
470: revert ErrInvalidQuoteToken()
486: revert ErrInvalidBaseToken()
503: revert ErrTooHighSlippage(shares)
567: revert ErrTooHighSlippage(amountOut)
574: revert ErrTooHighSlippage(amountOut)
582: revert ErrTooHighSlippage(amountOut)
591: revert ErrPathTooLong()
594: revert ErrEmptyPath()
600: revert ErrZeroDecimals()
603: revert ErrDecimalsDifferenceTooLarge()
```
[40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L40) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L49) | [213](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L213) | [240](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L240) | [305](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L305) | [356](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L356) | [386](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L386) | [424](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L424) | [440](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L440) | [470](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L470) | [486](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L486) | [503](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L503) | [567](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L567) | [574](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L574) | [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L582) | [591](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L591) | [594](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L594) | [600](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L600) | [603](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L603)

```solidity
File: src/staking/LockingMultiRewards.sol

120: revert ErrInvalidBoostMultiplier()
124: revert ErrInvalidLockDuration()
128: revert ErrInvalidRewardDuration()
132: revert ErrInvalidDurationRatio()
157: revert ErrZeroAmount()
172: revert ErrZeroAmount()
302: revert ErrInvalidTokenAddress()
306: revert ErrRewardAlreadyExists()
310: revert ErrMaxRewardsExceeded()
327: revert ErrSkimmingTooMuch()
363: revert ErrInvalidTokenAddress()
375: revert ErrInsufficientRemainingTime()
385: revert ErrNotEnoughReward()
399: revert ErrLengthMismatch()
411: revert ErrNoLocks()
418: revert ErrInvalidLockIndex()
423: revert ErrLockNotExpired()
460: revert ErrZeroAmount()
494: revert ErrMaxUserLocksExceeded()
498: revert ErrLockAmountTooSmall()
```
[120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L120) | [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L124) | [128](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L128) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L132) | [157](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L157) | [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L172) | [302](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L302) | [306](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L306) | [310](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L310) | [327](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L327) | [363](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L363) | [375](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L375) | [385](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L385) | [399](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L399) | [411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L411) | [418](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L418) | [423](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L423) | [460](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L460) | [494](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L494) | [498](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L498)
</details>

### [G-16] Use local variables for emitting

Use the function/modifier's local copy of the state variable, rather than incurring an extra Gwarmaccess (100 gas).
In the unlikely event that the state variable hasn't already been used by the function/modifier, consider whether it is really necessary to include it in the event, given the fact that it incurs a Gcoldsload (2100 gas), or whether it can be passed in to or back out of the functions that do use it.

<details>
<summary><i>5 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

124: emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares)
148: emit LogReadyChanged(ready)
```
[124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124) | [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148)

```solidity
File: src/mimswap/MagicLP.sol

501: emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance)
```
[501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L501)

```solidity
File: src/mimswap/periphery/Factory.sol

88: emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_)
```
[88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88)

```solidity
File: src/staking/LockingMultiRewards.sol

318: emit LogSetMinLockAmount(minLockAmount, _minLockAmount)
```
[318](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L318)
</details>

### [G-17] `x.a = x.a + b` always cheaper than `x.a += b` for Structs

Using direct assignment operations (e.g., `x.a = x.a + b`) is more gas-efficient compared to compound assignment operations (e.g., `x.a += b`).
Examples:
```solidity
    // direct write to storage   -> 5337 gas
    // struct storage pointer    -> 5341 gas
    // memory struct             -> 4628 gas
    // memory function param     -> 1109 gas
    x.a += b;

    // direct write to storage   -> 5330 gas
    // struct storage pointer    -> 5334 gas
    // memory struct             -> 4625 gas
    // memory function param     -> 1106 gas
    x.a = struct.a + b;
```


<details>
<summary><i>22 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

105: totals[token].locked += amount
106: balances[msg.sender][token].locked += amount
108: totals[token].unlocked += amount
109: balances[msg.sender][token].unlocked += amount
112: totals[token].total += amount
118: balances[msg.sender][token].total += amount
124: balances[msg.sender][token].unlocked -= amount
125: balances[msg.sender][token].locked += amount
126: totals[token].unlocked -= amount
127: totals[token].locked += amount
133: balances[msg.sender][token].unlocked -= amount
134: balances[msg.sender][token].total -= amount
135: totals[token].unlocked -= amount
136: totals[token].total -= amount
```
[105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L105) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L106) | [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L108) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L109) | [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L112) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L118) | [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L124) | [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L125) | [126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L126) | [127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L127) | [133](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L133) | [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L134) | [135](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L135) | [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L136)

```solidity
File: src/staking/LockingMultiRewards.sol

162: _balances[msg.sender].unlocked -= amount
177: _balances[msg.sender].unlocked -= amount
444: bal.unlocked += amount
445: bal.locked -= amount
472: _balances[account].unlocked += amount
485: bal.locked += amount
510: _userLocks[user][_lastLockIndex].amount += amount
642: item.amount += rewardAmount
```
[162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L162) | [177](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L177) | [444](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L444) | [445](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L445) | [472](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L472) | [485](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L485) | [510](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L510) | [642](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L642)
</details>

### [G-18] Initializers can be marked as payable

Payable functions cost less gas to execute, because the compiler does not have to add extra checks to ensure that no payment is provided.
Initializers can be safely marked as payable, because only the deployer or the factory contract would call the function without carrying any funds.

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

129: function initialize(Router _router) external onlyOwner
```
[129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129)

```solidity
File: src/mimswap/MagicLP.sol

91: function init(
        address baseTokenAddress,
        address quoteTokenAddress,
        uint256 lpFeeRate,
        address mtFeeRateModel,
        uint256 i,
        uint256 k
    ) external
```
[91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L91)
</details>

### [G-19] Using `constants` instead of `enum` can save gas

`Enum` is expensive and it is [more efficient to use constants](https://www.codehawks.com/finding/clm84992q02j9w9ruebun36d9) instead.
An illustrative example of this approach can be found in the [ReentrancyGuard.sol](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/181d518609a9f006fcb97af63e6952e603cf100e/contracts/utils/ReentrancyGuard.sol#L34-L35)

<details>
<summary><i>2 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

18: enum State {
        Idle,
        Opened,
        Closed
    }
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L18)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

21: enum RState {
        ONE,
        ABOVE_ONE,
        BELOW_ONE
    }
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L21)
</details>

### [G-20] Create variable outside the loop

Creating variables inside the loop consum more gas compared to declaring them outside and just reaffecting values to them inside the loop.
```solidity
    // uint256 outsideVar = anyValue;
    for (uint256 i = 0; i < 10; i++) {
        // outsideVar = value;     // 1984 gas
        uint256 insideVar = value; // 2012 gas 
    }
```

<details>
<summary><i>16 issue instances in 1 files:</i></summary>

```solidity
File: src/staking/LockingMultiRewards.sol

406: address user = users[i]
407: Balances storage bal = _balances[user]
408: LockedBalance[] storage locks = _userLocks[user]
414: uint256 index = lockIndexes[i]
426: uint256 amount = locks[index].amount
427: uint256 lastIndex = locks.length - 1
562: address token = rewardTokens[i]
576: address token = rewardTokens[i]
577: uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_)
580: uint256 j
581: address user = users[j]
581: address user = users[j]
615: address rewardToken = rewardTokens[i]
616: uint256 rewardAmount = rewards[user][rewardToken]
624: RewardLockItem storage item = _rewardLock.items[i]
628: uint256 amount = item.amount
```
[406](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L406) | [407](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L407) | [408](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L408) | [414](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L414) | [426](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L426) | [427](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L427) | [562](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L562) | [576](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L576) | [577](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L577) | [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580) | [581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L581) | [581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L581) | [615](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L615) | [616](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L616) | [624](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L624) | [628](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L628)
</details>

### [G-21] Nested for loops should be avoided due to high gas costs resulting from O^2 time complexity

In Solidity, avoiding nested for loops is a recommended practice primarily due to the high gas costs associated with them.
These loops can lead to quadratic (O^2) time complexity, especially when they iterate over large data sets or perform complex computations.
Since every operation in a smart contract consumes gas, and users pay for this gas, optimizing for lower gas usage is crucial.
Nested loops, which inherently have higher computational complexity, can significantly increase the gas costs of a contract.
To optimize for efficiency, it's advisable to minimize the use of loops, limit their range, and reduce computations within each loop iteration.
Alternative patterns like map/filter/reduce might often be cheaper than traditional for loops in terms of gas usage

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/staking/LockingMultiRewards.sol

580: for (uint256 j; j < users.length; )
```
[580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580)
</details>

### [G-22] Use bytes32 in place of string

For strings of 32 char strings and below you can use bytes32 instead as it's more gas efficient

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

156: string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()))
```
[156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L156)
</details>

### [G-23] Using `delete` on a `bool` variable is cheaper than assigning it to `false`

```solidity
function test() external {
    delete bar; // 5184 gas
    bar = false; // 5208 gas
}
```

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/libraries/Math.sol

176: bSig = false
```
[176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L176)
</details>

### [G-24] Use `Array.unsafeAccess()` to avoid repeated array length checks

When using storage arrays, solidity adds an internal lookup of the array's length (a Gcoldsload 2100 gas) to ensure you don't read past the array's end.
You can avoid this lookup by using `Array.unsafeAccess()` in cases where the length has already been checked, as is the case with the instances below.

<details>
<summary><i>7 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

165: for (uint256 i = 0; i < tokens.length; i++) {
```
[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)

```solidity
File: src/staking/LockingMultiRewards.sol

405: for (uint256 i; i < users.length; ) {
547: for (uint256 i; i < rewardTokens.length; ) {
561: for (uint256 i; i < rewardTokens.length; ) {
575: for (uint256 i; i < rewardTokens.length; ) {
580: for (uint256 j; j < users.length; ) {
614: for (uint256 i; i < rewardTokens.length; ) {
```
[405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405) | [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547) | [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561) | [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575) | [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580) | [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614)
</details>

### [G-25] Counting down when iterating, saves gas

Counting down saves 6 gas per loop, since checks for zero are more efficient than checks against any other value.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

165: for (uint256 i = 0; i < tokens.length; i++) {
```
[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)
</details>

### [G-26] `>=` costs less gas than `>`

The compiler uses opcodes GT and ISZERO for solidity code that uses >, but only requires LT for >=, which saves 3 gas. If < is being used, the condition can be inverted.
In cases where a for-loop is being used, one can count down rather than up, in order to use the optimal operator.

<details>
<summary><i>14 issue instances in 5 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

114: if (caps[token] > 0 && totals[token].total > caps[token]) {
```
[114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114)

```solidity
File: src/mimswap/MagicLP.sol

294: if (data.length > 0) {
395: } else if (baseReserve > 0 && quoteReserve > 0) {
395: } else if (baseReserve > 0 && quoteReserve > 0) {
450: if (data.length > 0) {
549: if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
582: if (amount > 0) {
588: if (amount > 0) {
```
[294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L294) | [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395) | [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395) | [450](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L450) | [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549) | [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L582) | [588](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L588)

```solidity
File: src/mimswap/libraries/Math.sol

22: if (remainder > 0) {
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L22)

```solidity
File: src/mimswap/periphery/Router.sol

147: } else if (baseReserve > 0 && quoteReserve > 0) {
147: } else if (baseReserve > 0 && quoteReserve > 0) {
527: if (quoteReserve > 0 && baseReserve > 0) {
527: if (quoteReserve > 0 && baseReserve > 0) {
```
[147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147) | [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527) | [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527)

```solidity
File: src/staking/LockingMultiRewards.sol

636: if (amount > 0) {
```
[636](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L636)
</details>

### [G-27] Consider pre-calculating the address of `address(this)` to save gas

Use foundry's script.sol or solady's LibRlp.sol to save the value in a constant, which will avoid having to spend gas to push the value on the stack every time it's used.

<details>
<summary><i>49 issue instances in 11 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

99: BlastYields.configureDefaultClaimables(address(this));
```
[99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L99)

```solidity
File: src/blast/BlastGovernor.sol

21: BlastYields.configureDefaultClaimables(address(this));
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L21)

```solidity
File: src/blast/BlastMagicLP.sol

99: BlastYields.configureDefaultClaimables(address(this));
```
[99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L99)

```solidity
File: src/blast/BlastOnboarding.sol

59: BlastYields.configureDefaultClaimables(address(this));
102: token.safeTransferFrom(msg.sender, address(this), amount);
```
[59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L59) | [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L102)

```solidity
File: src/blast/BlastOnboardingBoot.sol

106: (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
117: staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
118: staking.setOperator(address(this), true);
```
[106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106) | [117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L118)

```solidity
File: src/blast/BlastWrappers.sol

51: if (governor_ == address(this)) {
60: if (_governor == address(this)) {
```
[51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L51) | [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L60)

```solidity
File: src/blast/libraries/BlastYields.sol

21: if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {
26: emit LogBlastTokenClaimableEnabled(address(this), token);
31: emit LogBlastNativeClaimableEnabled(address(this));
39: return claimMaxGasYields(address(this), recipient);
52: return claimAllNativeYields(address(this), recipient);
71: amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L21) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L26) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L31) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L39) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L52) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L71)

```solidity
File: src/mimswap/MagicLP.sol

229: return _BASE_TOKEN_.balanceOf(address(this)) - uint256(_BASE_RESERVE_);
233: return _QUOTE_TOKEN_.balanceOf(address(this)) - uint256(_QUOTE_RESERVE_);
245: uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
262: _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));
268: uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
285: _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);
298: uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
299: uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
361: uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
362: uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
427: if (to == address(this)) {
431: uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
432: uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
505: uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
506: uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
529: baseBalance = _BASE_TOKEN_.balanceOf(address(this));
530: quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
568: uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
569: uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
615: if (address(this) == address(implementation)) {
622: if (address(this) != address(implementation)) {
```
[229](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L229) | [233](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L233) | [245](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L245) | [262](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L262) | [268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L268) | [285](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L285) | [298](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L298) | [299](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L299) | [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L361) | [362](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L362) | [427](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L427) | [431](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L431) | [432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L432) | [505](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L505) | [506](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L506) | [529](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L529) | [530](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L530) | [568](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L568) | [569](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L569) | [615](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L615) | [622](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L622)

```solidity
File: src/mimswap/periphery/Factory.sol

77: address(this)
```
[77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L77)

```solidity
File: src/mimswap/periphery/Router.sol

92: address(weth).safeTransferFrom(address(this), clone, msg.value);
269: lp.safeTransferFrom(msg.sender, address(this), sharesIn);
282: lp.safeTransferFrom(msg.sender, address(this), sharesIn);
289: address(this),
298: address(this),
398: amountOut = _swap(address(this), path, directions, minimumOut);
444: amountOut = _sellBase(lp, address(this), minimumOut);
490: amountOut = _sellQuote(lp, address(this), minimumOut);
```
[92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L269) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282) | [289](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L289) | [298](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L298) | [398](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L398) | [444](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L444) | [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L490)

```solidity
File: src/staking/LockingMultiRewards.sol

326: if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {
367: rewardToken.safeTransferFrom(msg.sender, address(this), amount);
464: stakingToken.safeTransferFrom(msg.sender, address(this), amount);
```
[326](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326) | [367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367) | [464](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L464)
</details>

### [G-28] Constructors can be marked `payable`

Payable functions cost less gas to execute, since the compiler does not have to add extra checks to ensure that a payment wasn't provided.

A constructor can safely be marked as `payable`, since only the deployer would be able to pass funds, and the project itself would not pass any funds. 
T
his could save an average of about 21 gas per call, in addition to the extra deployment cost.

<details>
<summary><i>13 issue instances in 13 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

7: constructor() {
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L7)

```solidity
File: src/blast/BlastBox.sol

23: constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L23)

```solidity
File: src/blast/BlastGovernor.sol

14: constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L14)

```solidity
File: src/blast/BlastMagicLP.sol

22: constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L22)

```solidity
File: src/blast/BlastOnboarding.sol

57: constructor() Owned(msg.sender) {
```
[57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L57)

```solidity
File: src/blast/BlastTokenRegistry.sol

11: constructor(address _owner) Owned(_owner) {}
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L11)

```solidity
File: src/blast/BlastWrappers.sol

20: constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20)

```solidity
File: src/mimswap/MagicLP.sol

83: constructor(address owner_) Owned(owner_) {
```
[83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L83)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

21: constructor(address maintainer_, address owner_) Owned(owner_) {
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L21)

```solidity
File: src/mimswap/periphery/Factory.sol

37: constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
```
[37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L37)

```solidity
File: src/mimswap/periphery/Router.sol

37: constructor(IWETH weth_, IFactory factory_) {
```
[37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L37)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

21: constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21)

```solidity
File: src/staking/LockingMultiRewards.sol

112: constructor(
        address _stakingToken,
        uint256 _lockingBoostMultiplerInBips,
        uint256 _rewardsDuration,
        uint256 _lockDuration,
        address _owner
    ) OperatableV2(_owner) {
```
[112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L112)
</details>

### [G-29] Split `revert` checks to save gas

Using boolean operators in a single `if() revert` statement can consume more gas than necessary.
Consider splitting these statements to save gas.

<details>
<summary><i>12 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

102: if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
            revert ErrZeroAddress();
108: if (i == 0 || i > MAX_I) {
            revert ErrInvalidI();
114: if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {
            revert ErrInvalidLPFeeRate();
440: if (baseAmount < baseMinAmount || quoteAmount < quoteMinAmount) {
            revert ErrWithdrawNotEnough();
462: if (token == _BASE_TOKEN_ || token == _QUOTE_TOKEN_) {
            revert ErrNotAllowed();
480: if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
            revert ErrReserveAmountNotEnough();
483: if (newI == 0 || newI > MAX_I) {
            revert ErrInvalidI();
489: if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {
            revert ErrInvalidLPFeeRate();
507: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
            revert ErrOverflow();
531: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
            revert ErrOverflow();
```
[102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102) | [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L108) | [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L114) | [440](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L440) | [462](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L462) | [480](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L480) | [483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L483) | [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L489) | [507](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L507) | [531](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L531)

```solidity
File: src/mimswap/periphery/Router.sol

39: if (address(weth_) == address(0) || address(factory_) == address(0)) {
            revert ErrZeroAddress();
599: if (baseDecimals == 0 || quoteDecimals == 0) {
            revert ErrZeroDecimals();
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L39) | [599](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L599)
</details>

### [G-30] Multiple accesses of a mapping/array should use a local variable cache

Leveraging a local variable to cache these values when accessed more than once can yield a gas saving of approximately 42 units per access.
This reduction is attributed to eliminating the need for recalculating the key's keccak256 hash (which costs Gkeccak256 - 30 gas) and the associated stack operations.
For arrays, this also prevents the overhead of re-computing offsets in memory or calldata.

<details>
<summary><i>35 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit `totals[token]` is used 4 times
105: totals[token].locked += amount;
108: totals[token].unlocked += amount;
112: totals[token].total += amount;
114: if (caps[token] > 0 && totals[token].total > caps[token]) {
/// @audit `caps[token]` is used 2 times
114: if (caps[token] > 0 && totals[token].total > caps[token]) {
114: if (caps[token] > 0 && totals[token].total > caps[token]) {
/// @audit `balances[msg.sender]` is used 3 times
106: balances[msg.sender][token].locked += amount;
109: balances[msg.sender][token].unlocked += amount;
118: balances[msg.sender][token].total += amount;
/// @audit `totals[token]` is used 2 times
126: totals[token].unlocked -= amount;
127: totals[token].locked += amount;
/// @audit `balances[msg.sender]` is used 2 times
124: balances[msg.sender][token].unlocked -= amount;
125: balances[msg.sender][token].locked += amount;
/// @audit `totals[token]` is used 2 times
135: totals[token].unlocked -= amount;
136: totals[token].total -= amount;
/// @audit `balances[msg.sender]` is used 2 times
133: balances[msg.sender][token].unlocked -= amount;
134: balances[msg.sender][token].total -= amount;
```
[105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L105) | [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L108) | [112](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L112) | [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114) | [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114) | [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L106) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L109) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L118) | [126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L126) | [127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L127) | [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L124) | [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L125) | [135](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L135) | [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L136) | [133](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L133) | [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L134)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit `_rewardData[rewardToken]` is used 4 times
279: return _rewardData[rewardToken].rewardPerTokenStored;
282: uint256 timeElapsed = lastTimeRewardApplicable_ - _rewardData[rewardToken].lastUpdateTime;
283: uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
285: return _rewardData[rewardToken].rewardPerTokenStored + pendingRewardsPerToken;
/// @audit `_rewardData[rewardToken]` is used 2 times
305: if (_rewardData[rewardToken].exists) {
314: _rewardData[rewardToken].exists = true;
/// @audit `_rewardData[rewardToken]` is used 2 times
362: if (!_rewardData[rewardToken].exists) {
369: Reward storage reward = _rewardData[rewardToken];
/// @audit `_userLocks[user]` is used 4 times
483: uint256 lockCount = _userLocks[user].length;
490: if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {
501: _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));
510: _userLocks[user][_lastLockIndex].amount += amount;
/// @audit `_rewardData[token_]` is used 2 times
532: _rewardData[token_].rewardPerTokenStored = rewardPerToken_;
533: _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow
/// @audit `_userRewardLock[user]` is used 2 times
598: RewardLock storage _rewardLock = _userRewardLock[user];
648: _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
/// @audit `rewards[user]` is used 2 times
616: uint256 rewardAmount = rewards[user][rewardToken];
619: rewards[user][rewardToken] = 0;
```
[279](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L279) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L282) | [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283) | [285](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L285) | [305](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L305) | [314](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L314) | [362](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L362) | [369](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L369) | [483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L483) | [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L490) | [501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L501) | [510](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L510) | [532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L532) | [533](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L533) | [598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L598) | [648](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L648) | [616](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L616) | [619](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L619)
</details>

### [G-31] Optimize Increment and Decrement in loops with `unchecked` keyword

Use `unchecked{i++}` or `unchecked{++i}` instead of `i++` or `++i` when it is not possible for them to overflow.
This is applicable for Solidity version `0.8.0` or higher to `0.8.23` and saves 30-40 gas per loop.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

165: for (uint256 i = 0; i < tokens.length; i++) {
```
[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)
</details>

### [G-32] Reduce gas usage by moving to Solidity 0.8.19 or later

See [this](https://soliditylang.org/blog/2023/02/22/solidity-0.8.19-release-announcement/#preventing-dead-code-in-runtime-bytecode) link for the full details. Additionally, every new release has new optimizations, which will save gas.

<details>
<summary><i>20 issue instances in 20 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2)

```solidity
File: src/blast/BlastBox.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L3)

```solidity
File: src/blast/BlastGovernor.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L2)

```solidity
File: src/blast/BlastMagicLP.sol

3: pragma solidity >=0.8.0;
```
[3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L3)

```solidity
File: src/blast/BlastOnboarding.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L2)

```solidity
File: src/blast/BlastOnboardingBoot.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L2)

```solidity
File: src/blast/BlastTokenRegistry.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L2)

```solidity
File: src/blast/BlastWrappers.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L2)

```solidity
File: src/blast/libraries/BlastPoints.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L2)

```solidity
File: src/blast/libraries/BlastYields.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L2)

```solidity
File: src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L8)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

7: pragma solidity >=0.8.0;
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L7)

```solidity
File: src/mimswap/libraries/Math.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L8)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

8: pragma solidity >=0.8.0;
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L8)

```solidity
File: src/mimswap/periphery/Factory.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L2)

```solidity
File: src/mimswap/periphery/Router.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L2)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L2)

```solidity
File: src/staking/LockingMultiRewards.sol

2: pragma solidity >=0.8.0;
```
[2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L2)
</details>

### [G-33] Reduce deployment costs by tweaking contracts' metadata

The Solidity compiler appends 53 bytes of metadata to the smart contract code which translates to an extra 10,600 gas (200 per bytecode) + the calldata cost (16 gas per non-zero bytes, 4 gas per zero-byte).
This translates to up to 848 additional gas in calldata cost.
One way to reduce this cost is by optimizing the IPFS hash that gets appended to the smart contract code.

Why is this important?
- The metadata adds an extra 53 bytes, resulting in an additional 10,600 gas cost for deployment.
- It also incurs up to 848 additional gas in calldata cost.

Options to Reduce Gas:
1. Use the `--no-cbor-metadata` compiler option to exclude metadata, but this might affect contract verification.
2. Mine for code comments that lead to an IPFS hash with more zeros, reducing calldata costs.

<details>
<summary><i>20 issue instances in 20 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L1)

```solidity
File: src/blast/BlastBox.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L1)

```solidity
File: src/blast/BlastGovernor.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L1)

```solidity
File: src/blast/BlastMagicLP.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L1)

```solidity
File: src/blast/BlastOnboarding.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L1)

```solidity
File: src/blast/BlastOnboardingBoot.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L1)

```solidity
File: src/blast/BlastTokenRegistry.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L1)

```solidity
File: src/blast/BlastWrappers.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L1)

```solidity
File: src/blast/libraries/BlastPoints.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L1)

```solidity
File: src/blast/libraries/BlastYields.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L1)

```solidity
File: src/mimswap/MagicLP.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L1)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L1)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L1)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L1)

```solidity
File: src/mimswap/libraries/Math.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L1)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L1)

```solidity
File: src/mimswap/periphery/Factory.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L1)

```solidity
File: src/mimswap/periphery/Router.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L1)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L1)

```solidity
File: src/staking/LockingMultiRewards.sol

1: Consider optimizing the IPFS hash during deployment.
```
[1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L1)
</details>

### [G-34] Use Pre-Increment/Decrement (++i/--i) to Save Gas

Using pre-increment (++i) or pre-decrement (--i) operators is more gas-efficient compared to their post counterparts (i++ or i--).
This is because pre-increment/decrement operators avoid the need for an additional temporary variable that stores the original value of the iterator.
This subtle difference results in saving of around 5 gas units per operation, which can accumulate to substantial savings in gas costs in contracts with frequent increment/decrement operations.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

165: for (uint256 i = 0; i < tokens.length; i++) {
```
[165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)
</details>

### [G-35] Nesting `if`-statements is cheaper than using `&&`

Optimization of condition checks in your smart contract is a crucial aspect in ensuring gas efficiency. Specifically, substituting multiple `&&` checks with nested `if` statements can lead to substantial gas savings.

When evaluating multiple conditions within a single `if` statement using the `&&` operator, each condition will consume gas even if a preceding condition fails. However, if these checks are broken down into nested `if` statements, execution halts as soon as a condition fails, saving the gas that would have been consumed by subsequent checks.

This practice is especially beneficial in scenarios where the `if` statement isn't followed by an `else` statement. The reason being, when an `else` statement is present, all conditions must be checked regardless to determine the correct branch of execution.

By reworking your code to utilize nested `if` statements, you can optimize gas usage, reduce execution cost, and enhance your contract's performance.

<details>
<summary><i>11 issue instances in 5 files:</i></summary>

```solidity
File: src/blast/BlastMagicLP.sol

119: if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
```
[119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119)

```solidity
File: src/blast/BlastOnboarding.sol

114: if (caps[token] > 0 && totals[token].total > caps[token]) {
```
[114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114)

```solidity
File: src/mimswap/MagicLP.sol

139: if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
144: if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
302: if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
395: } else if (baseReserve > 0 && quoteReserve > 0) {
549: if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
```
[139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139) | [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144) | [302](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302) | [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395) | [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549)

```solidity
File: src/mimswap/periphery/Router.sol

147: } else if (baseReserve > 0 && quoteReserve > 0) {
527: if (quoteReserve > 0 && baseReserve > 0) {
```
[147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147) | [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527)

```solidity
File: src/staking/LockingMultiRewards.sol

326: if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {
417: if (index == lastLockIndex[user] && locks.length > 1) {
```
[326](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326) | [417](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L417)
</details>

### [G-36] Use `storage` instead of `memory` for state structs/arrays

When fetching data from storage, assigning it to a memory variable causes all fields of the struct/array to be read from storage, incurring a Gcoldsload (2100 gas) for each field.
Reading fields from the new memory variable incurs an additional MLOAD rather than a cheap stack read.

Instead, declare variables with the storage keyword and cache any fields that need to be re-read in stack variables.
This approach is more cost-efficient, only incurring the Gcoldsload for fields actually read.

The only time it makes sense to read the whole struct/array into a memory variable is if the full struct/array is being returned by the function, passed to a function that requires memory, or read from another memory array/struct.

<details>
<summary><i>3 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

171: PMMPricing.PMMState memory state = getPMMState();
184: PMMPricing.PMMState memory state = getPMMState();
205: PMMPricing.PMMState memory state = getPMMState();
```
[171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L171) | [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L184) | [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L205)
</details>

### [G-37] Avoid transferring amounts of zero in order to save gas

Performing token or Ether transfers with a zero amount may result in unnecessary gas consumption. 
The absence of a zero-amount check before a transfer or send operation can lead to wasted gas, as the state of the contract remains the same even if the amount is zero. 
Adding a conditional check for zero amounts can prevent these costly, unnecessary operations, thereby optimizing the contract's gas usage.

<details>
<summary><i>22 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit `amount` has not been checked for zero value before transfer
102: token.safeTransferFrom(msg.sender, address(this), amount);
/// @audit `amount` has not been checked for zero value before transfer
138: token.safeTransfer(msg.sender, amount);
/// @audit `amount` has not been checked for zero value before transfer
210: token.safeTransfer(to, amount);
```
[102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L102) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L138) | [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L210)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit `amount` has not been checked for zero value before transfer
466: token.safeTransfer(to, amount);
```
[466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L466)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit `baseInAmount` has not been checked for zero value before transfer
68: baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);
/// @audit `quoteInAmount` has not been checked for zero value before transfer
69: quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);
/// @audit `tokenInAmount` has not been checked for zero value before transfer
91: token.safeTransferFrom(msg.sender, clone, tokenInAmount);
/// @audit `baseAdjustedInAmount` has not been checked for zero value before transfer
172: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);
/// @audit `quoteAdjustedInAmount` has not been checked for zero value before transfer
173: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);
/// @audit `quoteInAmount` has not been checked for zero value before transfer
187: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);
/// @audit `tokenAdjustedAmount` has not been checked for zero value before transfer
224: token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);
/// @audit `tokenInAmount` has not been checked for zero value before transfer
246: token.safeTransferFrom(msg.sender, lp, tokenInAmount);
/// @audit `sharesIn` has not been checked for zero value before transfer
269: lp.safeTransferFrom(msg.sender, address(this), sharesIn);
/// @audit `sharesIn` has not been checked for zero value before transfer
282: lp.safeTransferFrom(msg.sender, address(this), sharesIn);
/// @audit `amountIn` has not been checked for zero value before transfer
328: IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
/// @audit `amountIn` has not been checked for zero value before transfer
330: IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
/// @audit `amountIn` has not been checked for zero value before transfer
393: IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
/// @audit `amountIn` has not been checked for zero value before transfer
395: IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
/// @audit `amountIn` has not been checked for zero value before transfer
411: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
/// @audit `amountIn` has not been checked for zero value before transfer
443: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
/// @audit `amountIn` has not been checked for zero value before transfer
456: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
/// @audit `amountIn` has not been checked for zero value before transfer
489: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
```
[68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L68) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L69) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L91) | [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L172) | [173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L173) | [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L187) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L224) | [246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L246) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L269) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282) | [328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L328) | [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L330) | [393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L393) | [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L395) | [411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L411) | [443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L443) | [456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L456) | [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L489)
</details>

### [G-38] `>=` costs less gas than `>`

The Solidity compiler requires fewer opcodes when the `>=` operator is used in place of the `>` operator. 
Specifically, the compiler uses GT and ISZERO opcodes for `>` but only requires LT for `>=`, saving 3 gas. 
Thus, wherever applicable, it's recommended to use `>=` instead of `>` to enhance gas efficiency in your code. Same applies for `<=` and `<`.

<details>
<summary><i>70 issue instances in 8 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

114: if (caps[token] > 0 && totals[token].total > caps[token]) {
165: for (uint256 i = 0; i < tokens.length; i++) {
```
[114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114) | [165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)

```solidity
File: src/blast/BlastOnboardingBoot.sol

108: if (totalPoolShares < minAmountOut) {
```
[108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L108)

```solidity
File: src/mimswap/MagicLP.sol

108: if (i == 0 || i > MAX_I) {
111: if (k > MAX_K) {
114: if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {
114: if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {
139: if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
144: if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
302: if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
302: if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
308: if (baseBalance < _BASE_RESERVE_) {
315: if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {
330: if (quoteBalance < _QUOTE_RESERVE_) {
337: if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {
381: shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;
399: uint256 mintRatio = quoteInputRatio < baseInputRatio ? quoteInputRatio : baseInputRatio;
421: if (deadline < block.timestamp) {
424: if (shareAmount > balanceOf(msg.sender)) {
441: if (baseAmount < baseMinAmount || quoteAmount < quoteMinAmount) {
441: if (baseAmount < baseMinAmount || quoteAmount < quoteMinAmount) {
480: if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
480: if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
483: if (newI == 0 || newI > MAX_I) {
486: if (newK > MAX_K) {
489: if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {
489: if (newLpFeeRate < MIN_LP_FEE_RATE || newLpFeeRate > MAX_LP_FEE_RATE) {
508: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
508: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
532: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
532: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
```
[108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L108) | [111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L111) | [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L114) | [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L114) | [139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139) | [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144) | [302](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302) | [302](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302) | [308](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L308) | [315](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L315) | [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L330) | [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L337) | [381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L381) | [399](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L399) | [421](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L421) | [424](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L424) | [441](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L441) | [441](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L441) | [480](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L480) | [480](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L480) | [483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L483) | [486](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L486) | [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L489) | [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L489) | [508](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508) | [508](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508) | [532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L532) | [532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L532)

```solidity
File: src/mimswap/libraries/Math.sol

32: while (z < y) {
40: require V0>=V1>=V2>0
        res = (1-k)i(V1-V2)+ikV0*V0(1/V2-1/V1)
118: if deltaBSig=true, then Q2>Q1, user sell Q and receive B
119: if deltaBSig=false, then Q2<Q1, user sell B and receive Q
200: if (V2 > V1) {
```
[32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L32) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L40) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L118) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L119) | [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L200)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

50: if (payBaseAmount < backToOnePayBase) {
54: if (receiveQuoteAmount > backToOneReceiveQuote) {
86: if (payQuoteAmount < backToOnePayQuote) {
89: if (receiveBaseAmount > backToOneReceiveBase) {
```
[50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L50) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L54) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L86) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L89)

```solidity
File: src/mimswap/periphery/Router.sol

48: if (block.timestamp > deadline) {
101: shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
138: shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;
220: if (msg.value > wethAdjustedAmount) {
502: if (shares < minimumShares) {
523: uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
544: for (uint256 i = 0; i < iterations; ) {
566: if (amountOut < minimumOut) {
573: if (amountOut < minimumOut) {
581: if (amountOut < minimumOut) {
590: if (pathLength > 256) {
602: if (quoteDecimals - baseDecimals > MAX_BASE_QUOTE_DECIMALS_DIFFERENCE) {
```
[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L48) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L101) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L138) | [220](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L220) | [502](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L502) | [523](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L523) | [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544) | [566](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L566) | [573](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L573) | [581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L581) | [590](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L590) | [602](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L602)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

40: uint256 minAnswer = baseAnswerNomalized < quoteAnswerNormalized ? baseAnswerNomalized : quoteAnswerNormalized;
```
[40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L40)

```solidity
File: src/staking/LockingMultiRewards.sol

123: if (_lockDuration < MIN_LOCK_DURATION) {
127: if (_rewardsDuration < MIN_REWARDS_DURATION) {
326: if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {
374: if (_remainingRewardTime < minRemainingTime) {
379: if (block.timestamp < reward.periodFinish) {
384: if (amount < _remainingRewardTime) {
405: for (uint256 i; i < users.length; ) {
417: if (index == lastLockIndex[user] && locks.length > 1) {
422: if (locks[index].unlockTime > block.timestamp) {
490: if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {
497: if (amount < minLockAmount) {
547: for (uint256 i; i < rewardTokens.length; ) {
561: for (uint256 i; i < rewardTokens.length; ) {
575: for (uint256 i; i < rewardTokens.length; ) {
580: for (uint256 j; j < users.length; ) {
614: for (uint256 i; i < rewardTokens.length; ) {
623: if (i < rewardItemLength) {
```
[123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L123) | [127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L127) | [326](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326) | [374](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L374) | [379](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L379) | [384](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L384) | [405](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405) | [417](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L417) | [422](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L422) | [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L490) | [497](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L497) | [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547) | [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561) | [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575) | [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580) | [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614) | [623](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L623)
</details>

### [G-39] Cache Function Calls for Efficiency

Function calls, especially external function calls, can be quite expensive in terms of gas. 
If you need to retrieve the same data more than once in a function, it is more efficient to call 
the function once, store the result in a local variable, and then use that variable later in the 
code instead of making the function call again.

<details>
<summary><i>5 issue instances in 3 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

319: _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
341: _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
```
[319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L319) | [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L341)

```solidity
File: src/mimswap/libraries/Math.sol

141: return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);
```
[141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L141)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

206: R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);
210: R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);
```
[206](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L206) | [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L210)
</details>

### [G-40] Unutilized Named Return Variables Waste Gas Without Optimizer

Utilizing named return variables without assignment or explicit return in functions can lead to unnecessary gas costs without an active optimizer.
To enhance gas efficiency, you might consider opting for unnamed return variables, especially when they aren't explicitly used or returned.
Keeping the current configuration without an active optimizer can result in extra gas costs associated with superfluous stack variables.

<details>
<summary><i>27 issue instances in 7 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit - Redundant `return 0;` statement in functions with named return variables
/// @audit - Redundant `return _claimable(user);` statement in functions with named return variables
77: function claimable(address user) external view returns (uint256 shares) {
/// @audit - Redundant `return router.previewCreatePool(I, baseAmount, quoteAmount);` statement in functions with named return variables
85: function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit - Redundant `return 0;` statement in functions with named return variables
/// @audit - Redundant `return (userLocked * totalPoolShares) / totalLocked;` statement in functions with named return variables
154: function _claimable(address user) internal view returns (uint256 shares) {
```
[77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L77) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L85) | [154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L154)

```solidity
File: src/blast/libraries/BlastYields.sol

/// @audit - Redundant `return claimAllNativeYields(address(this), recipient);` statement in functions with named return variables
50: function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
```
[50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L50)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit - Redundant `return PMMPricing.getMidPrice(getPMMState());` statement in functions with named return variables
214: function getMidPrice() public view returns (uint256 midPrice) {
/// @audit - Redundant `return _MT_FEE_RATE_MODEL_.getFeeRate(user, _LP_FEE_RATE_);` statement in functions with named return variables
223: function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
/// @audit - Redundant `return _BASE_TOKEN_.balanceOf(address(this)) - uint256(_BASE_RESERVE_);` statement in functions with named return variables
227: function getBaseInput() public view returns (uint256 input) {
/// @audit - Redundant `return _QUOTE_TOKEN_.balanceOf(address(this)) - uint256(_QUOTE_RESERVE_);` statement in functions with named return variables
231: function getQuoteInput() public view returns (uint256 input) {
```
[214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L214) | [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L223) | [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L227) | [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L231)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit - Redundant `return (lpFeeRate, 0);` statement in functions with named return variables
/// @audit - Redundant `return IFeeRateImpl(implementation).getFeeRate(msg.sender, trader, lpFeeRate);` statement in functions with named return variables
33: function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L33)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

/// @audit - Redundant `return (lpFeeRate - mtFeeRate, mtFeeRate);` statement in functions with named return variables
9: function getFeeRate(
        address /*pool*/,
        address /*trader*/,
        uint256 lpFeeRate
    ) external pure returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

/// @audit - Redundant `return Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q0, payBaseAmount, state.i, state.K);` statement in functions with named return variables
103: function _ROneSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {
/// @audit - Redundant `return Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);` statement in functions with named return variables
118: function _ROneSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {
/// @audit - Redundant `return Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K);` statement in functions with named return variables
133: function _RBelowSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {
/// @audit - Redundant `return Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q, payBaseAmount, state.i, state.K);` statement in functions with named return variables
146: function _RBelowSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {
/// @audit - Redundant `return Math._GeneralIntegrate(state.B0, state.B + payBaseAmount, state.B, state.i, state.K);` statement in functions with named return variables
161: function _RAboveSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {
/// @audit - Redundant `return Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);` statement in functions with named return variables
174: function _RAboveSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {
```
[103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L103) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L118) | [133](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L133) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L146) | [161](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L161) | [174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L174)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit - Redundant `return (0, 0, 0);` statement in functions with named return variables
95: function previewCreatePool(
        uint256 i,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external pure returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit - Redundant `return (0, 0, 0);` statement in functions with named return variables
/// @audit - Redundant `return (0, 0, 0);` statement in functions with named return variables
/// @audit - Redundant `return (0, 0, 0);` statement in functions with named return variables
111: function previewAddLiquidity(
        address lp,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
/// @audit - Redundant `return _addLiquidity(lp, to, minimumShares);` statement in functions with named return variables
177: function addLiquidityUnsafe(
        address lp,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 shares) {
/// @audit - Redundant `return _addLiquidity(lp, to, minimumShares);` statement in functions with named return variables
228: function addLiquidityETHUnsafe(
        address lp,
        address to,
        uint256 tokenInAmount,
        uint256 minimumShares,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 shares) {
/// @audit - Redundant `return IMagicLP(lp).sellShares(sharesIn, to, minimumBaseAmount, minimumQuoteAmount, "", deadline);` statement in functions with named return variables
260: function removeLiquidity(
        address lp,
        address to,
        uint256 sharesIn,
        uint256 minimumBaseAmount,
        uint256 minimumQuoteAmount,
        uint256 deadline
    ) external returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
/// @audit - Redundant `return _swap(to, path, directions, minimumOut);` statement in functions with named return variables
313: function swapTokensForTokens(
        address to,
        uint256 amountIn,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit - Redundant `return _swap(to, path, directions, minimumOut);` statement in functions with named return variables
335: function swapETHForTokens(
        address to,
        address[] calldata path,
        uint256 directions,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit - Redundant `return _sellBase(lp, to, minimumOut);` statement in functions with named return variables
403: function sellBaseTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit - Redundant `return _sellBase(lp, to, minimumOut);` statement in functions with named return variables
414: function sellBaseETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit - Redundant `return _sellQuote(lp, to, minimumOut);` statement in functions with named return variables
448: function sellQuoteTokensForTokens(
        address lp,
        address to,
        uint256 amountIn,
        uint256 minimumOut,
        uint256 deadline
    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
/// @audit - Redundant `return _sellQuote(lp, to, minimumOut);` statement in functions with named return variables
460: function sellQuoteETHForTokens(
        address lp,
        address to,
        uint256 minimumOut,
        uint256 deadline
    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
```
[95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L95) | [111](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L111) | [177](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L177) | [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L228) | [260](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L260) | [313](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L313) | [335](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L335) | [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L403) | [414](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L414) | [448](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L448) | [460](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L460)
</details>

### [G-41] Use `unchecked` for Math Operations if they already checked

Some subtraction operations in the contract have implicit checks that prevent underflow. 
To optimize gas, consider wrapping such operations in an `unchecked` block. 
Always review the logic thoroughly before making changes to ensure the safety of operations.

<details>
<summary><i>7 issue instances in 4 files:</i></summary>

```solidity
File: src/mimswap/libraries/Math.sol

/// @audit - mathematical operation `bAbs - part2` checked above in line:
/// 174: if (bAbs >= part2) {
175: bAbs = bAbs - part2;
/// @audit - mathematical operation `part2 - bAbs` checked above in line:
/// 174: if (bAbs >= part2) {
178: bAbs = part2 - bAbs;
/// @audit - mathematical operation `V1 - V2` checked above in line:
/// 200: if (V2 > V1) {
203: return V1 - V2;
```
[175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L175) | [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L178) | [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L203)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

/// @audit - mathematical operation `payBaseAmount - backToOnePayBase` checked above in line:
/// 50: if (payBaseAmount < backToOnePayBase) {
65: receiveQuoteAmount = backToOneReceiveQuote + _ROneSellBaseToken(state, payBaseAmount - backToOnePayBase);
/// @audit - mathematical operation `payQuoteAmount - backToOnePayQuote` checked above in line:
/// 86: if (payQuoteAmount < backToOnePayQuote) {
96: receiveBaseAmount = backToOneReceiveBase + _ROneSellQuoteToken(state, payQuoteAmount - backToOnePayQuote);
```
[65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L65) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L96)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit - mathematical operation `msg.value - wethAdjustedAmount` checked above in line:
/// 220: if (msg.value > wethAdjustedAmount) {
221: refundTo.safeTransferETH(msg.value - wethAdjustedAmount);
```
[221](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L221)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit - mathematical operation `locks.length - 1` checked above in line:
/// 417: if (index == lastLockIndex[user] && locks.length > 1) {
427: uint256 lastIndex = locks.length - 1;
```
[427](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L427)
</details>

### [G-42] Using `private` rather than `public`, saves gas

Public storage variables increase the contract's size due to the implicit generation of public getter functions. 
This makes the contract larger and could increase deployment and interaction costs.

If you do not require other contracts to read these variables, consider making them `private`. 

Example:
```solidity
/// 145426 gas to deploy
contract PublicState {
    address public first;
    address public second;
}
/// 77126 gas to deploy
contract PrivateState {
    address private first;
    address private second;
}
```

<details>
<summary><i>71 issue instances in 13 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

20: BlastTokenRegistry public immutable registry;
21: mapping(address => bool) public enabledTokens;
22: address public feeTo;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21) | [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L22)

```solidity
File: src/blast/BlastGovernor.sol

11: address public feeTo;
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L11)

```solidity
File: src/blast/BlastMagicLP.sol

17: BlastTokenRegistry public immutable registry;
20: address public feeTo;
21: mapping(address => bool) public operators;
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L17) | [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L21)

```solidity
File: src/blast/BlastOnboarding.sol

30: State public state;
31: address public bootstrapper;
32: address public feeTo;
33: BlastTokenRegistry public registry;
36: mapping(address token => bool) public supportedTokens;
37: mapping(address token => Balances) public totals;
38: mapping(address token => uint256 cap) public caps;
41: mapping(address user => mapping(address token => Balances)) public balances;
```
[30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L30) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L31) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L32) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L33) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36) | [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L37) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L38) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L41)

```solidity
File: src/blast/BlastOnboardingBoot.sol

24: address public pool;
25: Router public router;
26: IFactory public factory;
27: uint256 public totalPoolShares;
28: bool public ready;
29: LockingMultiRewards public staking;
30: mapping(address user => bool claimed) public claimed;
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L24) | [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L25) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L26) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L27) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L28) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L29) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L30)

```solidity
File: src/blast/BlastTokenRegistry.sol

10: mapping(address => bool) public nativeYieldTokens;
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10)

```solidity
File: src/blast/libraries/BlastPoints.sol

7: address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;
8: IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L7) | [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L8)

```solidity
File: src/mimswap/MagicLP.sol

61: MagicLP public immutable implementation;
63: uint256 public constant MAX_I = 10 ** 36;
64: uint256 public constant MAX_K = 10 ** 18;
65: uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%
66: uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%
70: address public _BASE_TOKEN_;
71: address public _QUOTE_TOKEN_;
72: uint112 public _BASE_RESERVE_;
73: uint112 public _QUOTE_RESERVE_;
74: uint32 public _BLOCK_TIMESTAMP_LAST_;
75: uint256 public _BASE_PRICE_CUMULATIVE_LAST_;
76: uint112 public _BASE_TARGET_;
77: uint112 public _QUOTE_TARGET_;
78: uint32 public _RState_;
79: IFeeRateModel public _MT_FEE_RATE_MODEL_;
80: uint256 public _LP_FEE_RATE_;
81: uint256 public _K_;
82: uint256 public _I_;
```
[61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L61) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L65) | [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L66) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L70) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L71) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73) | [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74) | [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L75) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77) | [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L78) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L79) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L80) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L81) | [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L82)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

19: address public maintainer;
20: address public implementation;
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L19) | [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L20)

```solidity
File: src/mimswap/periphery/Factory.sol

32: address public implementation;
33: IFeeRateModel public maintainerFeeRateModel;
35: mapping(address base => mapping(address quote => address[] pools)) public pools;
36: mapping(address creator => address[] pools) public userPools;
```
[32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L32) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L33) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L35) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L36)

```solidity
File: src/mimswap/periphery/Router.sol

31: uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;
33: IWETH public immutable weth;
34: IFactory public immutable factory;
```
[31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L31) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L33) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L34)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

10: IMagicLP public immutable pair;
11: IAggregator public immutable baseOracle;
12: IAggregator public immutable quoteOracle;
13: uint8 public immutable baseDecimals;
14: uint8 public immutable quoteDecimals;
16: uint256 public constant WAD = 18;
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L10) | [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L11) | [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L12) | [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L14) | [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L16)

```solidity
File: src/staking/LockingMultiRewards.sol

83: uint256 public immutable maxLocks;
84: uint256 public immutable lockingBoostMultiplerInBips;
85: uint256 public immutable rewardsDuration;
86: uint256 public immutable lockDuration;
87: address public immutable stakingToken;
94: mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
95: mapping(address user => mapping(address token => uint256 amount)) public rewards;
96: mapping(address user => uint256 index) public lastLockIndex;
98: address[] public rewardTokens;
100: uint256 public lockedSupply; // all locked boosted deposits
101: uint256 public unlockedSupply; // all unlocked unboosted deposits
102: uint256 public minLockAmount; // minimum amount allowed to lock
103: uint256 public stakingTokenBalance; // total staking token balance
```
[83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L83) | [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L84) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L85) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L86) | [87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L87) | [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L94) | [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L95) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L96) | [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L98) | [100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L100) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L101) | [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L102) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L103)
</details>

### [G-43] Use Assembly for Hash Calculations

In certain cases, using inline assembly to calculate hashes can lead to significant gas savings. Solidity's built-in keccak256 function is convenient but costs more gas than the equivalent assembly code. However, it's important to note that using assembly should be done with care as it's less readable and could increase the risk of introducing errors.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/periphery/Factory.sol

163: return keccak256(abi.encodePacked(sender_, implementation, baseToken_, quoteToken_, lpFeeRate_, i_, k_));
```
[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L163)
</details>

### [G-44] Refactor duplicated require()/revert() checks to save gas

Duplicate require()/revert() checks can be refactored into a modifier or function, saving deployment costs.

<details>
<summary><i>25 issue instances in 10 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

25: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
73: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L25) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L73)

```solidity
File: src/blast/BlastMagicLP.sol

24: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
81: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L24) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L81)

```solidity
File: src/blast/BlastOnboarding.sol

89: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
148: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
```
[89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L89) | [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L148)

```solidity
File: src/blast/BlastWrappers.sol

21: if (governor_ == address(0)) {
            revert ErrZeroAddress();
35: if (governor_ == address(0)) {
            revert ErrZeroAddress();
48: if (governor_ == address(0)) {
            revert ErrZeroAddress();
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L21) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L35) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L48)

```solidity
File: src/mimswap/MagicLP.sol

508: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
            revert ErrOverflow();
532: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
            revert ErrOverflow();
```
[508](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508) | [532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L532)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

23: if (maintainer_ == address(0)) {
            revert ErrZeroAddress();
47: if (maintainer_ == address(0)) {
            revert ErrZeroAddress();
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L23) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L47)

```solidity
File: src/mimswap/libraries/Math.sol

52: if (V0 == 0) {
            revert ErrIsZero();
132: if (V0 == 0) {
            revert ErrIsZero();
```
[52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L52) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L132)

```solidity
File: src/mimswap/periphery/Factory.sol

39: if (implementation_ == address(0)) {
            revert ErrZeroAddress();
97: if (implementation_ == address(0)) {
            revert ErrZeroAddress();
42: if (address(maintainerFeeRateModel_) == address(0)) {
            revert ErrZeroAddress();
106: if (address(maintainerFeeRateModel_) == address(0)) {
            revert ErrZeroAddress();
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L39) | [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L97) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L42) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L106)

```solidity
File: src/mimswap/periphery/Router.sol

566: if (amountOut < minimumOut) {
            revert ErrTooHighSlippage(amountOut);
573: if (amountOut < minimumOut) {
            revert ErrTooHighSlippage(amountOut);
581: if (amountOut < minimumOut) {
            revert ErrTooHighSlippage(amountOut);
```
[566](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L566) | [573](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L573) | [581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L581)

```solidity
File: src/staking/LockingMultiRewards.sol

156: if (amount == 0) {
            revert ErrZeroAmount();
171: if (amount == 0) {
            revert ErrZeroAmount();
459: if (amount == 0) {
            revert ErrZeroAmount();
```
[156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L156) | [171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L171) | [459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L459)
</details>

### [G-45] Use Assembly for Efficient Memory Management in Multiple External Calls

When making multiple external calls in a Solidity contract, it may be more efficient to use inline assembly to reuse the memory space allocated for function arguments and return data.
This can prevent unnecessary memory expansion and reduce gas costs.

Example:
```solidity
contract Solidity {
    // cost: 7262
    function call(address calledAddress) external pure returns(uint256) {
        Called called = Called(calledAddress);
        uint256 res1 = called.add(1, 2);
        uint256 res2 = called.add(3, 4);

        uint256 res = res1 + res2;
        return res;
    }
}

contract Assembly {
    // cost: 5281
    function call(address calledAddress) external view returns(uint256) {
        assembly {
            // check that calledAddress has code deployed to it
            if iszero(extcodesize(calledAddress)) {
                revert(0x00, 0x00)
            }

            // first call
            mstore(0x00, hex"771602f7")
            mstore(0x04, 0x01)
            mstore(0x24, 0x02)
            let success := staticcall(gas(), calledAddress, 0x00, 0x44, 0x60, 0x20)
            if iszero(success) {
                revert(0x00, 0x00)
            }
            let res1 := mload(0x60)

            // second call
            mstore(0x04, 0x03)
            mstore(0x24, 0x4)
            success := staticcall(gas(), calledAddress, 0x00, 0x44, 0x60, 0x20)
            if iszero(success) {
                revert(0x00, 0x00)
            }
            let res2 := mload(0x60)

            // add results
            let res := add(res1, res2)

            // return data
            mstore(0x60, res)
            return(0x60, 0x20)
        }
    }
}
```

<details>
<summary><i>16 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit function `claimTokenYields()` has multiple external calls
56: if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
            token0Amount = BlastYields.claimAllTokenYields(_BASE_TOKEN_, feeTo_);
59: if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
            token1Amount = BlastYields.claimAllTokenYields(_QUOTE_TOKEN_, feeTo_);
/// @audit function `_updateTokenClaimables()` has multiple external calls
105: if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
            BlastYields.enableTokenClaimable(_BASE_TOKEN_);
109: if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
            BlastYields.enableTokenClaimable(_QUOTE_TOKEN_);
```
[56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L56) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L59) | [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L105) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L109)

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit function `bootstrap()` has multiple external calls
106: (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
118: staking.setOperator(address(this), true);
119: staking.transferOwnership(owner);
```
[106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L118) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L119)

```solidity
File: src/blast/libraries/BlastYields.sol

/// @audit function `enableTokenClaimable()` has multiple external calls
21: if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {
            return;
25: IERC20Rebasing(token).configure(YieldMode.CLAIMABLE);
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L21) | [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L25)

```solidity
File: src/mimswap/periphery/Router.sol

/// @audit function `createPool()` has multiple external calls
66: clone = IFactory(factory).create(baseToken, quoteToken, lpFeeRate, i, k);
70: (shares, , ) = IMagicLP(clone).buyShares(to);
/// @audit function `createPoolETH()` has multiple external calls
88: clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);
93: (shares, , ) = IMagicLP(clone).buyShares(to);
/// @audit function `removeLiquidityETH()` has multiple external calls
287: (ethAmountOut, tokenAmountOut) = IMagicLP(lp).sellShares(
                sharesIn,
                address(this),
                minimumETHAmount,
                minimumTokenAmount,
                "",
                deadline
            );
296: (tokenAmountOut, ethAmountOut) = IMagicLP(lp).sellShares(
                sharesIn,
                address(this),
                minimumTokenAmount,
                minimumETHAmount,
                "",
                deadline
            );
308: weth.withdraw(ethAmountOut);
```
[66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L66) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L70) | [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L88) | [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L93) | [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L287) | [296](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L296) | [308](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L308)
</details>

### [G-46] Cached Global Variables

Storing global variables in local storage might appear as a useful caching mechanism. 
However, in Solidity, accessing global variables directly is often more gas-efficient than caching them. 
Consider removing these redundant assignments and use the global variables directly.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/periphery/Factory.sol

82: address creator = tx.origin;
```
[82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L82)
</details>

### [G-47] Simple checks for zero `uint` can be done using `assembly` to save gas

The usage of inline `assembly` to check if variable is the `zero` can save gas compared to traditional `require` or `if` statement checks.
```solidity
    // gas 396 gas | 399 gas
    assembly {
        if iszero(value) { // use iszero(iszero(value)) for != add 3 gas
            revert(0, 0)
        }
    }
    require(value != 0); // 401 gas
    require(value == 0); // 401 gas

<details>
<summary><i>36 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

64: if (shares == 0) {
            revert ErrNothingToClaim();
158: if (totalLocked == 0) {
```
[64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L64) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L158)

```solidity
File: src/mimswap/MagicLP.sol

108: if (i == 0 || i > MAX_I) {
            revert ErrInvalidI();
369: if (baseInput == 0) {
            revert ErrNoBaseInput();
375: if (totalSupply() == 0) {
            // case 1. initial supply
            if (quoteBalance == 0) {
                revert ErrZeroQuoteAmount();
385: if (_QUOTE_TARGET_ == 0) {
                revert ErrZeroQuoteTarget();
483: if (newI == 0 || newI > MAX_I) {
            revert ErrInvalidI();
549: if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
            /// @dev It is desired and expected for this value to
            /// overflow once it has hit the max of `type.uint256`.
            unchecked {
                _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
```
[108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L108) | [369](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L369) | [375](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L375) | [385](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L385) | [483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L483) | [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

48: if (e == 0) {
```
[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L48)

```solidity
File: src/mimswap/libraries/Math.sol

52: if (V0 == 0) {
            revert ErrIsZero();
58: if (k == 0) {
80: if (k == 0) {
            return V1 + DecimalMath.mulFloor(i, delta);
89: if (V1 == 0) {
94: if (ki == 0) {
132: if (V0 == 0) {
            revert ErrIsZero();
136: if (delta == 0) {
140: if (k == 0) {
            return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);
153: if (idelta == 0) {
192: if (numerator == 0) {
                revert ErrIsZero();
```
[52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L52) | [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L58) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L80) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L89) | [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L94) | [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L132) | [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L136) | [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L140) | [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L153) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L192)

```solidity
File: src/mimswap/periphery/Router.sol

125: if (baseInAmount == 0) {
            return (0, 0, 0);
131: if (totalSupply == 0) {
            if (quoteBalance == 0) {
                return (0, 0, 0);
327: if (directions & 1 == 0) {
            IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
348: if (directions & 1 == 0) {
            inToken = IMagicLP(firstLp)._BASE_TOKEN_();
379: if ((directions >> lastLpIndex) & 1 == 0) {
            outToken = IMagicLP(lastLp)._QUOTE_TOKEN_();
392: if (directions & 1 == 0) {
            IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
521: if (IERC20(lp).totalSupply() == 0) {
            uint256 i = IMagicLP(lp)._I_();
545: if (directions & 1 == 0) {
                // Sell base
                IMagicLP(path[i]).sellBase(address(path[i + 1]));
560: if ((directions & 1 == 0)) {
            amountOut = IMagicLP(path[iterations]).sellBase(to);
599: if (baseDecimals == 0 || quoteDecimals == 0) {
            revert ErrZeroDecimals();
```
[125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L125) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L131) | [327](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L327) | [348](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L348) | [379](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L379) | [392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L392) | [521](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L521) | [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L545) | [560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L560) | [599](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L599)

```solidity
File: src/staking/LockingMultiRewards.sol

131: if (_lockDuration % _rewardsDuration != 0) {
            revert ErrInvalidDurationRatio();
156: if (amount == 0) {
            revert ErrZeroAmount();
171: if (amount == 0) {
            revert ErrZeroAmount();
278: if (totalSupply_ == 0) {
410: if (locks.length == 0) {
                revert ErrNoLocks();
459: if (amount == 0) {
            revert ErrZeroAmount();
490: if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {
            // Limit the number of locks per user to avoid too much gas costs per user
            // when looping through the locks
            if (lockCount == maxLocks) {
                revert ErrMaxUserLocksExceeded();
```
[131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L131) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L156) | [171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L171) | [278](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L278) | [410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L410) | [459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L459) | [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L490)
</details>

### [G-48] Use Cached Contracts for Multiple External Calls

When function makes multiple calls to the same external contract, it is more gas-efficient to use a local copy of the contract.
This is because the EVM will cache the contract in memory, and subsequent calls will be cheaper.
It's especially true for contracts that are large and/or have many functions.
```solidity
    // local cache -> 6561 gas
    IToken localCache = storageContract;
    localCache.externalCall();
    localCache.externalCall();

    // direct call 6683 gas
    storageContract.externalCall();
    storageContract.externalCall();
```

<details>
<summary><i>4 issue instances in 2 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit function bootstrap() make external call of `staking` - 2 times
118: staking.setOperator(address(this), true);
119: staking.transferOwnership(owner);
```
[118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L118) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L119)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit function flashLoan() make external call of `_MT_FEE_RATE_MODEL_` - 2 times
276: _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
253: _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
```
[276](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L276) | [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L253)
</details>

### [G-49] Consider using solady's `FixedPointMathLib`

Utilizing gas-optimized math functions from libraries like [Solady](https://github.com/Vectorized/solady/blob/main/src/utils/FixedPointMathLib.sol) can lead to more efficient smart contracts.
This is particularly beneficial in contracts where these operations are frequently used.

<details>
<summary><i>118 issue instances in 8 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

163: return (userLocked * totalPoolShares) / totalLocked;
163: return (userLocked * totalPoolShares) / totalLocked;
```
[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L163) | [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L163)

```solidity
File: src/mimswap/MagicLP.sol

435: baseAmount = (baseBalance * shareAmount) / totalShares;
436: quoteAmount = (quoteBalance * shareAmount) / totalShares;
438: _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
439: _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
517: _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
553: _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
435: baseAmount = (baseBalance * shareAmount) / totalShares;
436: quoteAmount = (quoteBalance * shareAmount) / totalShares;
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
517: _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
63: uint256 public constant MAX_I = 10 ** 36;
64: uint256 public constant MAX_K = 10 ** 18;
125: _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);
546: uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
```
[435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L435) | [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L436) | [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517) | [553](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L553) | [435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L435) | [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L436) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64) | [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L125) | [546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L546)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

24: return (target * d) / ONE;
28: return (target * d).divCeil(ONE);
32: return (target * ONE) / d;
36: return (target * ONE).divCeil(d);
54: p = (p * p) / ONE;
56: p = (p * target) / ONE;
24: return (target * d) / ONE;
32: return (target * ONE) / d;
40: return ONE2 / target;
53: uint p = powFloor(target, e / 2);
54: p = (p * p) / ONE;
56: p = (p * target) / ONE;
20: uint256 internal constant ONE = 10 ** 18;
21: uint256 internal constant ONE2 = 10 ** 36;
49: return 10 ** 18;
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L24) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L28) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L32) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L36) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L54) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L56) | [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L24) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L32) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L40) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L53) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L54) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L56) | [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20) | [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L21) | [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L49)

```solidity
File: src/mimswap/libraries/Math.sol

21: uint256 remainder = a - quotient * b;
41: res = (1-k)i(V1-V2)+ikV0*V0(1/V2-1/V1)
43: res = i*delta*(1-k+k(V0^2/V1/V2))
56: uint256 fairAmount = i * (V1 - V2); // i*delta
62: uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);
64: return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;
68: Follow the integration function above
        i*deltaB = (Q2-Q1)*(1-k+kQ0^2/Q1/Q2)
69: i*deltaB = (Q2-Q1)*(1-k+kQ0^2/Q1/Q2)
93: uint256 ki = (4 * k) * i;
93: uint256 ki = (4 * k) * i;
96: } else if ((ki * delta) / ki == delta) {
97: _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);
99: _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);
101: uint256 premium = DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2) + DecimalMath.ONE;
108: i*deltaB = (Q2-Q1)*(1-k+kQ0^2/Q1/Q2)
152: uint256 idelta = i * delta;
155: } else if ((idelta * V1) / idelta == V1) {
156: temp = (idelta * V1) / (V0 * V0);
156: temp = (idelta * V1) / (V0 * V0);
158: temp = (((delta * V1) / V0) * i) / V0;
158: temp = (((delta * V1) / V0) * i) / V0;
160: return (V1 * temp) / (temp + DecimalMath.ONE);
170: uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
170: uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
170: uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
171: uint256 bAbs = (DecimalMath.ONE - k) * V1; // (1-k)Q1
184: uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
184: uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
185: squareRoot = sqrt((bAbs * bAbs) + squareRoot); // sqrt(b*b+4(1-k)kQ0*Q0)
185: squareRoot = sqrt((bAbs * bAbs) + squareRoot); // sqrt(b*b+4(1-k)kQ0*Q0)
188: uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
20: uint256 quotient = a / b;
30: uint256 z = x / 2 + 1;
34: z = (x / z + z) / 2;
34: z = (x / z + z) / 2;
43: res = i*delta*(1-k+k(V0^2/V1/V2))
59: return fairAmount / DecimalMath.ONE;
62: uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);
63: uint256 penalty = DecimalMath.mulFloor(k, V0V0V1V2); // k(V0^2/V1/V2)
64: return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;
69: i*deltaB = (Q2-Q1)*(1-k+kQ0^2/Q1/Q2)
96: } else if ((ki * delta) / ki == delta) {
97: _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);
99: _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);
108: i*deltaB = (Q2-Q1)*(1-k+kQ0^2/Q1/Q2)
115: and Q2=(-b+sqrt(b^2+4(1-k)kQ0^2))/2(1-k)
155: } else if ((idelta * V1) / idelta == V1) {
156: temp = (idelta * V1) / (V0 * V0);
158: temp = (((delta * V1) / V0) * i) / V0;
158: temp = (((delta * V1) / V0) * i) / V0;
160: return (V1 * temp) / (temp + DecimalMath.ONE);
170: uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
181: bAbs = bAbs / DecimalMath.ONE;
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L21) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L41) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L43) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L56) | [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64) | [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L68) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L69) | [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L93) | [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L93) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L96) | [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L97) | [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L99) | [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L101) | [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L108) | [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L152) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L155) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L156) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L156) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158) | [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L160) | [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170) | [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170) | [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170) | [171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L171) | [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184) | [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L185) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L185) | [188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L188) | [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L20) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L30) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L43) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L59) | [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L63) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L69) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L96) | [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L97) | [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L99) | [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L108) | [115](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L115) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L155) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L156) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158) | [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L160) | [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170) | [181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L181)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

205: uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);
209: uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
205: uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);
209: uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
```
[205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205) | [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209) | [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205) | [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209)

```solidity
File: src/mimswap/periphery/Router.sol

257: baseAmountOut = (baseBalance * sharesIn) / totalShares;
258: quoteAmountOut = (quoteBalance * sharesIn) / totalShares;
257: baseAmountOut = (baseBalance * sharesIn) / totalShares;
258: quoteAmountOut = (quoteBalance * sharesIn) / totalShares;
```
[257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L257) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L258) | [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L257) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L258)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

38: uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
39: uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
43: baseReserve = baseReserve * (10 ** (WAD - baseDecimals));
44: quoteReserve = quoteReserve * (10 ** (WAD - quoteDecimals));
45: return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
45: return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
38: uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
39: uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
43: baseReserve = baseReserve * (10 ** (WAD - baseDecimals));
44: quoteReserve = quoteReserve * (10 ** (WAD - quoteDecimals));
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L38) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L39) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L43) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L44) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L38) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L39) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L43) | [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L44)

```solidity
File: src/staking/LockingMultiRewards.sol

204: return _rewardData[rewardToken].rewardRate * rewardsDuration;
236: return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);
241: return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);
258: return (block.timestamp / rewardsDuration) * rewardsDuration;
283: uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
283: uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
294: return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];
380: amount += _remainingRewardTime * reward.rewardRate;
144: maxLocks = _lockDuration / _rewardsDuration;
236: return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);
241: return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);
258: return (block.timestamp / rewardsDuration) * rewardsDuration;
283: uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
294: return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];
388: reward.rewardRate = amount / _remainingRewardTime;
```
[204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L204) | [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L236) | [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L241) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L258) | [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283) | [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283) | [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294) | [380](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L380) | [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L144) | [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L236) | [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L241) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L258) | [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283) | [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294) | [388](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L388)
</details>

### [G-50] Avoid Zero to Non-Zero Storage Writes Where Possible

Changing a storage variable from zero to non-zero costs 22,100 gas in total. (20,000 gas for a zero to non-zero write and 2,100 for a cold storage access)
Consider using non-zero architecture to avoid high gas costs for zero to non-zero storage writes.

Example:

```solidity
- uint256 public counter = 0;  // rewrite this costs more
+ uint256 public counter = 1;  // rewrite this costs less
```

<details>
<summary><i>40 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

186: caps[token] = cap;
```
[186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L186)

```solidity
File: src/mimswap/MagicLP.sol

118: _INITIALIZED_ = true;
121: _I_ = i;
122: _K_ = k;
123: _LP_FEE_RATE_ = lpFeeRate;
125: _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);
140: _RState_ = uint32(PMMPricing.RState.ONE);
141: _BASE_TARGET_ = _BASE_RESERVE_;
142: _QUOTE_TARGET_ = _QUOTE_RESERVE_;
145: _RState_ = uint32(PMMPricing.RState.ONE);
146: _BASE_TARGET_ = _BASE_RESERVE_;
147: _QUOTE_TARGET_ = _QUOTE_RESERVE_;
257: _BASE_TARGET_ = newBaseTarget.toUint112();
258: _RState_ = uint32(newRState);
280: _QUOTE_TARGET_ = newQuoteTarget.toUint112();
321: _QUOTE_TARGET_ = newQuoteTarget.toUint112();
343: _BASE_TARGET_ = newBaseTarget.toUint112();
382: _BASE_TARGET_ = shares.toUint112();
383: _QUOTE_TARGET_ = DecimalMath.mulFloor(shares, _I_).toUint112();
402: _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();
403: _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
438: _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
493: _LP_FEE_RATE_ = uint64(newLpFeeRate);
494: _K_ = uint64(newK);
495: _I_ = uint128(newI);
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
517: _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
538: _BASE_TARGET_ = uint112(baseBalance);
539: _QUOTE_TARGET_ = uint112(quoteBalance);
540: _RState_ = uint32(PMMPricing.RState.ONE);
557: _BLOCK_TIMESTAMP_LAST_ = blockTimestamp;
572: _BASE_RESERVE_ = baseBalance.toUint112();
575: _QUOTE_RESERVE_ = quoteBalance.toUint112();
```
[118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L118) | [121](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L121) | [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L122) | [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L123) | [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L125) | [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L140) | [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L141) | [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L142) | [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L145) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L146) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L147) | [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L257) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L258) | [280](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L280) | [321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L321) | [343](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L343) | [382](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L382) | [383](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L383) | [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402) | [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403) | [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [493](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L493) | [494](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L494) | [495](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L495) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517) | [538](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L538) | [539](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L539) | [540](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L540) | [557](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L557) | [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L572) | [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L575)

```solidity
File: src/staking/LockingMultiRewards.sol

163: unlockedSupply -= amount;
178: unlockedSupply -= amount;
181: stakingTokenBalance -= amount;
319: minLockAmount = _minLockAmount;
431: lastLockIndex[user] = index;
442: lockedSupply -= amount;
502: lastLockIndex[user] = lockCount;
```
[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L163) | [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L178) | [181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L181) | [319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L319) | [431](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L431) | [442](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L442) | [502](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L502)
</details>

### [G-51] Consider Packing Small `uint` When it's Possible

Packing `uint` variables into the same storage slot can help in reducing gas costs.
This is particularly useful when storing or reading multiple smaller uints (e.g., uint80) in a single transaction.
Consider using bit manipulation to pack these variables.

If you pack two `uint` variables into a single `uint` storage slot, you'd perform only one SLOAD operation (800 gas) instead of two (1,600 gas) when you read them.
This saves 800 gas for each read operation involving the two variables.

Similarly, when you need to update both variables, a single SSTORE operation would cost you 20,000 gas instead of 40,000 gas, saving you another 20,000 gas. 

Example:
```Solidity
uint160 packedVariables;

function packVariables(uint80 x, uint80 y) external {
    packedVariables = uint160(x) << 80 | uint160(y);
}
```

<details>
<summary><i>6 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

74: uint32 public _BLOCK_TIMESTAMP_LAST_;
78: uint32 public _RState_;
72: uint112 public _BASE_RESERVE_;
73: uint112 public _QUOTE_RESERVE_;
76: uint112 public _BASE_TARGET_;
77: uint112 public _QUOTE_TARGET_;
```
[74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74) | [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L78) | [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77)
</details>

### [G-52] Consider Using `calldata` Instead of `memory` for Function Parameters

When function parameters are not being modified within the function, it can be more gas efficient 
to use `calldata` instead of `memory`. The Ethereum Virtual Machine (EVM) does not need to copy 
parameters marked with `calldata` from `calldata` to `memory`, saving gas. This is particularly effective 
for larger arrays and structs.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit `tokens` not modified within function
163: function claimTokenYields(address[] memory tokens) external onlyOwner {
```
[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L163)
</details>

### [G-53] Use `unchecked` for division which do not divide by -X sonce they can't overflow

Solidity introduced the `unchecked` block in version 0.8.0 as a measure to provide control over arithmetic operations. 
Any operation inside this block will not trigger the built-in overflow and underflow checks, thus saving gas costs. 
Since a division operation between two `uint`s (unsigned integers) can never result in an overflow or underflow, it's an ideal candidate for the use of `unchecked {}` block.
This practice enables optimal gas usage without risking any arithmetic anomalies.

<details>
<summary><i>40 issue instances in 8 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

163: return (userLocked * totalPoolShares) / totalLocked;
```
[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L163)

```solidity
File: src/mimswap/MagicLP.sol

435: baseAmount = (baseBalance * shareAmount) / totalShares;
436: quoteAmount = (quoteBalance * shareAmount) / totalShares;
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
517: _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
```
[435](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L435) | [436](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L436) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

24: return (target * d) / ONE;
32: return (target * ONE) / d;
40: return ONE2 / target;
53: uint p = powFloor(target, e / 2);
54: p = (p * p) / ONE;
56: p = (p * target) / ONE;
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L24) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L32) | [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L40) | [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L53) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L54) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L56)

```solidity
File: src/mimswap/libraries/Math.sol

20: uint256 quotient = a / b;
30: uint256 z = x / 2 + 1;
34: z = (x / z + z) / 2;
34: z = (x / z + z) / 2;
59: return fairAmount / DecimalMath.ONE;
62: uint256 V0V0V1V2 = DecimalMath.divFloor((V0 * V0) / V1, V2);
64: return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;
96: } else if ((ki * delta) / ki == delta) {
97: _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);
99: _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);
155: } else if ((idelta * V1) / idelta == V1) {
156: temp = (idelta * V1) / (V0 * V0);
158: temp = (((delta * V1) / V0) * i) / V0;
158: temp = (((delta * V1) / V0) * i) / V0;
160: return (V1 * temp) / (temp + DecimalMath.ONE);
170: uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
181: bAbs = bAbs / DecimalMath.ONE;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L20) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L30) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L59) | [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64) | [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L96) | [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L97) | [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L99) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L155) | [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L156) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158) | [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L160) | [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170) | [181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L181)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

205: uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);
209: uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
```
[205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205) | [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209)

```solidity
File: src/mimswap/periphery/Router.sol

257: baseAmountOut = (baseBalance * sharesIn) / totalShares;
258: quoteAmountOut = (quoteBalance * sharesIn) / totalShares;
```
[257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L257) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L258)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

45: return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45)

```solidity
File: src/staking/LockingMultiRewards.sol

144: maxLocks = _lockDuration / _rewardsDuration;
236: return unlockedSupply + ((lockedSupply * lockingBoostMultiplerInBips) / BIPS);
241: return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);
258: return (block.timestamp / rewardsDuration) * rewardsDuration;
283: uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
294: return ((balance_ * pendingUserRewardsPerToken) / 1e18) + rewards[user][rewardToken];
388: reward.rewardRate = amount / _remainingRewardTime;
```
[144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L144) | [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L236) | [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L241) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L258) | [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283) | [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294) | [388](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L388)
</details>

### [G-54] Minimize Gas Cost with Local Variables for State Writes in Loops

Writing to state variables within loops can significantly increase gas consumption, as state writes are more expensive operations.
An effective optimization strategy is to use local variables within the loop for intermediate calculations or storage and only update the state variables once after the loop completes.
This approach minimizes the number of state writes, thereby reducing the overall gas cost.
```solidity
    // 10802 gas
    for (uint256 i = 0; i < 10; i++) {
       foo += 10;
    }

    // update storage once 6047 gas
    uint256 localFoo;
    for (uint256 i = 0; i < 10; i++) {
        localFoo += 10;
    }
    foo = localFoo;
```

<details>
<summary><i>2 issue instances in 1 files:</i></summary>

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit access state variable `lockedSupply` access inside loop
442: lockedSupply -= amount;
/// @audit access state variable `unlockedSupply` access inside loop
441: unlockedSupply += amount;
```
[442](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L442) | [441](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L441)
</details>

### [G-55] State Variables Should Be `immutable` Since They Are Only Set in the Constructor

State variables that are only set in the constructor and are not modified elsewhere in the code should be declared as `immutable`.
This can optimize gas usage as `immutable` variables are read from code, not from storage.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

93: registry = registry_;
```
[93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L93)
</details>

### [G-56] Use solady library where possible to save gas

The following OpenZeppelin imports have a Solady equivalent, as such they can be used to save GAS as Solady modules have been specifically designed to be as GAS efficient as possible.

<details>
<summary><i>8 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

7: import {Proxy} from "openzeppelin-contracts/proxy/Proxy.sol";
10: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L7) | [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L10)

```solidity
File: src/blast/libraries/BlastYields.sol

5: import {Address} from "openzeppelin-contracts/utils/Address.sol";
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L5)

```solidity
File: src/mimswap/MagicLP.sol

11: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L11)

```solidity
File: src/mimswap/periphery/Router.sol

5: import {IERC20} from "openzeppelin-contracts/interfaces/IERC20.sol";
10: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L5) | [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L10)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

5: import {IERC20Metadata} from "openzeppelin-contracts/interfaces/IERC20Metadata.sol";
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L5)

```solidity
File: src/staking/LockingMultiRewards.sol

5: import {Pausable} from "openzeppelin-contracts/security/Pausable.sol";
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L5)
</details>

### [G-57] Use `uint256(1)`/`uint256(2)` instead of `true`/`false` to save gas for changes

Boolean variables in Solidity are more expensive than `uint256` or any type that takes up a full word, due to additional gas costs associated with write operations.
When using boolean variables, each write operation emits an extra SLOAD to read the slot's contents, replace the bits taken up by the boolean, and then write back.
This process cannot be disabled and leads to extra gas consumption.

By using `uint256(1)` and `uint256(2)` for representing true and false states, you can avoid a `Gwarmaccess` (100 gas) cost and also avoid a `Gsset` (20000 gas) cost when changing from `false` to `true`, after having been `true` in the past.
This approach helps in optimizing gas usage, making your contract more cost-effective.

[Usage in OpenZeppelin ReentrancyGuard.sol](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/58f635312aa21f947cae5f8578638a85aa2519f5/contracts/security/ReentrancyGuard.sol#L23-L27)

<details>
<summary><i>7 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

21: mapping(address => bool) public enabledTokens;
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21)

```solidity
File: src/blast/BlastMagicLP.sol

21: mapping(address => bool) public operators;
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L21)

```solidity
File: src/blast/BlastOnboarding.sol

36: mapping(address token => bool) public supportedTokens;
```
[36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36)

```solidity
File: src/blast/BlastOnboardingBoot.sol

28: bool public ready;
30: mapping(address user => bool claimed) public claimed;
```
[28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L28) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L30)

```solidity
File: src/blast/BlastTokenRegistry.sol

10: mapping(address => bool) public nativeYieldTokens;
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10)

```solidity
File: src/mimswap/MagicLP.sol

68: bool internal _INITIALIZED_;
```
[68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L68)
</details>

### [G-58] Use Bit Shifting for Multiplication by Powers of Two

When multiplying by powers of two (e.g., 2, 4, 8), it is more efficient to use bit shifting.

`<x> * 2` can be replaced with `<x> << 1`, as both operations are equivalent.
However, the multiplication approach may incur additional gas overhead due to potential jumps to and from a compiler utility function that introduces checks.

This overhead can be minimized by using bit shifting when multiplying by powers of two.

<details>
<summary><i>3 issue instances in 1 files:</i></summary>

```solidity
File: src/mimswap/libraries/Math.sol

101: uint256 premium = DecimalMath.divFloor(_sqrt - DecimalMath.ONE, k * 2) + DecimalMath.ONE;
184: uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
188: uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
```
[101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L101) | [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184) | [188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L188)
</details>

### [G-59] Delete Unused State Variables

State variables that aren't used in the contract not only clutter the codebase but also consume unnecessary gas during deployment.
Specifically, setting non-zero initial values for state variables costs significant gas.
By removing these unused state variables, you can save on both deployment gas and potential future storage gas costs.
This optimization not only reduces gas expenditures but also enhances code clarity and maintainability.
Always ensure a thorough review to confirm that these variables are indeed redundant before removal.

<details>
<summary><i>2 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit Unused state variable: USDB_TO_MIN
18: uint256 constant USDB_TO_MIN = 1.002 ether; // 1 USDB = 1.002 MIM
/// @audit Unused state variable: MIM_TO_MIN
19: uint256 constant MIM_TO_MIN = I;
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L18) | [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L19)
</details>

### [G-60] Avoid contract existence checks by using low-level calls

Before version 0.8.10, the Solidity compiler would insert extra code, such as EXTCODESIZE (costing 100 gas), to check the existence of a contract for external function calls.
Newer versions, starting from 0.8.10, no longer insert these checks if the external call has a return value.
You can achieve similar behavior in earlier Solidity versions by using low-level calls like `call`.
This low-level call don't check for contract existence, saving gas costs.

<details>
<summary><i>188 issue instances in 16 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

8: BlastPoints.configure();
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L8)

```solidity
File: src/blast/BlastBox.sol

53: return BlastYields.claimMaxGasYields(feeTo);
57: if (!registry.nativeYieldTokens(token_)) {
61: amount = BlastYields.claimAllTokenYields(token_, feeTo);
69: BlastYields.callPrecompile(data);
86: if (registry.nativeYieldTokens(token)) {
87: BlastYields.enableTokenClaimable(token);
99: BlastYields.configureDefaultClaimables(address(this));
100: BlastPoints.configure();
```
[53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L53) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L57) | [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L61) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L69) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L86) | [87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L87) | [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L99) | [100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L100)

```solidity
File: src/blast/BlastGovernor.sol

21: BlastYields.configureDefaultClaimables(address(this));
29: return BlastYields.claimAllNativeYields(contractAddress, feeTo);
33: return BlastYields.claimMaxGasYields(contractAddress, feeTo);
50: BlastYields.callPrecompile(data);
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L21) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L29) | [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L33) | [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L50)

```solidity
File: src/blast/BlastMagicLP.sol

48: address feeTo_ = BlastMagicLP(address(implementation)).feeTo();
50: return BlastYields.claimMaxGasYields(feeTo_);
54: address feeTo_ = BlastMagicLP(address(implementation)).feeTo();
56: if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
57: token0Amount = BlastYields.claimAllTokenYields(_BASE_TOKEN_, feeTo_);
59: if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
60: token1Amount = BlastYields.claimAllTokenYields(_QUOTE_TOKEN_, feeTo_);
73: BlastYields.callPrecompile(data);
99: BlastYields.configureDefaultClaimables(address(this));
100: BlastPoints.configure();
105: if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
106: BlastYields.enableTokenClaimable(_BASE_TOKEN_);
109: if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
110: BlastYields.enableTokenClaimable(_QUOTE_TOKEN_);
119: if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
```
[48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L48) | [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L50) | [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L54) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L56) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L57) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L59) | [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L60) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L73) | [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L99) | [100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L100) | [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L105) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L106) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L109) | [110](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L110) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119)

```solidity
File: src/blast/BlastOnboarding.sol

59: BlastYields.configureDefaultClaimables(address(this));
60: BlastPoints.configure();
102: token.safeTransferFrom(msg.sender, address(this), amount);
138: token.safeTransfer(msg.sender, amount);
157: BlastYields.callPrecompile(data);
161: return BlastYields.claimMaxGasYields(feeTo);
169: if (registry.nativeYieldTokens(tokens[i])) {
170: BlastYields.claimAllTokenYields(tokens[i], feeTo);
178: if (registry.nativeYieldTokens(token)) {
179: BlastYields.enableTokenClaimable(token);
210: token.safeTransfer(to, amount);
```
[59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L59) | [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L60) | [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L102) | [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L138) | [157](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L157) | [161](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L161) | [169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L169) | [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L170) | [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L178) | [179](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L179) | [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L210)

```solidity
File: src/blast/BlastOnboardingBoot.sol

69: staking.stakeFor(msg.sender, shares, lock);
89: return router.previewCreatePool(I, baseAmount, quoteAmount);
103: MIM.safeApprove(address(router), type(uint256).max);
104: USDB.safeApprove(address(router), type(uint256).max);
106: (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
118: staking.setOperator(address(this), true);
119: staking.transferOwnership(owner);
122: pool.safeApprove(address(staking), totalPoolShares);
131: factory = IFactory(router.factory());
```
[69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L69) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L89) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L103) | [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L104) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L118) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L119) | [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L122) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L131)

```solidity
File: src/blast/BlastWrappers.sol

24: BlastYields.configureDefaultClaimables(governor_);
38: BlastYields.configureDefaultClaimables(governor_);
67: BlastYields.configureDefaultClaimables(_governor);
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L24) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L38) | [67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L67)

```solidity
File: src/blast/libraries/BlastPoints.sol

11: BLAST_POINTS.configurePointsOperator(BLAST_POINTS_OPERATOR);
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L11)

```solidity
File: src/blast/libraries/BlastYields.sol

21: if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {
25: IERC20Rebasing(token).configure(YieldMode.CLAIMABLE);
30: BLAST_YIELD_PRECOMPILE.configure(YieldMode.CLAIMABLE, GasMode.CLAIMABLE, governor_);
43: amount = BLAST_YIELD_PRECOMPILE.claimMaxGas(contractAddress, recipient);
56: amount = BLAST_YIELD_PRECOMPILE.claimAllYield(contractAddress, recipient);
61: amount = BLAST_YIELD_PRECOMPILE.claimYield(contractAddress, recipient, amount);
71: amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));
76: amount = IERC20Rebasing(token).claim(recipient, amount);
87: Address.functionCall(address(BLAST_YIELD_PRECOMPILE), data);
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L21) | [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L25) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L30) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L43) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L56) | [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L61) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L71) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L76) | [87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L87)

```solidity
File: src/mimswap/MagicLP.sol

156: return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));
164: return IERC20Metadata(_BASE_TOKEN_).decimals();
172: (receiveQuoteAmount, newRState) = PMMPricing.sellBaseToken(state, payBaseAmount);
174: (uint256 lpFeeRate, uint256 mtFeeRate) = _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_);
185: (receiveBaseAmount, newRState) = PMMPricing.sellQuoteToken(state, payQuoteAmount);
187: (uint256 lpFeeRate, uint256 mtFeeRate) = _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_);
200: state.R = PMMPricing.RState(_RState_);
201: PMMPricing.adjustedTarget(state);
216: return PMMPricing.getMidPrice(getPMMState());
225: return _MT_FEE_RATE_MODEL_.getFeeRate(user, _LP_FEE_RATE_);
253: _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
276: _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
295: ICallee(assetTo).FlashLoanCall(msg.sender, baseAmount, quoteAmount, data);
319: _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
341: _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
451: ICallee(to).SellShareCall(msg.sender, shareAmount, baseAmount, quoteAmount, data);
466: token.safeTransfer(to, amount);
583: _BASE_TOKEN_.safeTransfer(to, amount);
589: _QUOTE_TOKEN_.safeTransfer(to, amount);
608: if (msg.sender != implementation.owner()) {
```
[156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L156) | [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L164) | [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L172) | [174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L174) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L185) | [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L187) | [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L200) | [201](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L201) | [216](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L216) | [225](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L225) | [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L253) | [276](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L276) | [295](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L295) | [319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L319) | [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L341) | [451](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L451) | [466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L466) | [583](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L583) | [589](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L589) | [608](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L608)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

39: return IFeeRateImpl(implementation).getFeeRate(msg.sender, trader, lpFeeRate);
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L39)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

116: return Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q0, payBaseAmount, state.i, state.K);
129: return Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);
144: return Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K);
157: return Math._SolveQuadraticFunctionForTrade(state.Q0, state.Q, payBaseAmount, state.i, state.K);
172: return Math._GeneralIntegrate(state.B0, state.B + payBaseAmount, state.B, state.i, state.K);
185: return Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);
192: state.Q0 = Math._SolveQuadraticFunctionForTarget(state.Q, state.B - state.B0, state.i, state.K);
194: state.B0 = Math._SolveQuadraticFunctionForTarget(
197: DecimalMath.reciprocalFloor(state.i),
```
[116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L116) | [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L129) | [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L144) | [157](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L157) | [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L172) | [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L185) | [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L192) | [194](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L194) | [197](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L197)

```solidity
File: src/mimswap/periphery/Factory.sol

74: LibClone.predictDeterministicAddress(
85: clone = LibClone.cloneDeterministic(address(implementation), salt);
86: IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
```
[74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L74) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L85) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L86)

```solidity
File: src/mimswap/periphery/Router.sol

64: _validateDecimals(IERC20Metadata(baseToken).decimals(), IERC20Metadata(quoteToken).decimals());
66: clone = IFactory(factory).create(baseToken, quoteToken, lpFeeRate, i, k);
68: baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);
69: quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);
70: (shares, , ) = IMagicLP(clone).buyShares(to);
83: _validateDecimals(18, IERC20Metadata(token).decimals());
85: _validateDecimals(IERC20Metadata(token).decimals(), 18);
88: clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);
91: token.safeTransferFrom(msg.sender, clone, tokenInAmount);
92: address(weth).safeTransferFrom(address(this), clone, msg.value);
93: (shares, , ) = IMagicLP(clone).buyShares(to);
117: (uint256 baseReserve, uint256 quoteReserve) = IMagicLP(lp).getReserves();
119: uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;
120: uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;
129: uint256 totalSupply = IERC20(lp).totalSupply();
136: uint256 i = IMagicLP(lp)._I_();
172: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);
173: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);
186: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);
187: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);
202: address token = IMagicLP(lp)._BASE_TOKEN_();
204: token = IMagicLP(lp)._QUOTE_TOKEN_();
208: } else if (IMagicLP(lp)._QUOTE_TOKEN_() == address(weth)) {
217: address(weth).safeTransfer(lp, wethAdjustedAmount);
221: refundTo.safeTransferETH(msg.value - wethAdjustedAmount);
224: token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);
236: address token = IMagicLP(lp)._BASE_TOKEN_();
238: token = IMagicLP(lp)._QUOTE_TOKEN_();
239: } else if (IMagicLP(lp)._QUOTE_TOKEN_() != address(weth)) {
244: address(weth).safeTransfer(lp, msg.value);
246: token.safeTransferFrom(msg.sender, lp, tokenInAmount);
252: uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp));
253: uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp));
255: uint256 totalShares = IERC20(lp).totalSupply();
269: lp.safeTransferFrom(msg.sender, address(this), sharesIn);
271: return IMagicLP(lp).sellShares(sharesIn, to, minimumBaseAmount, minimumQuoteAmount, "", deadline);
282: lp.safeTransferFrom(msg.sender, address(this), sharesIn);
284: address token = IMagicLP(lp)._BASE_TOKEN_();
286: token = IMagicLP(lp)._QUOTE_TOKEN_();
287: (ethAmountOut, tokenAmountOut) = IMagicLP(lp).sellShares(
295: } else if (IMagicLP(lp)._QUOTE_TOKEN_() == address(weth)) {
296: (tokenAmountOut, ethAmountOut) = IMagicLP(lp).sellShares(
308: weth.withdraw(ethAmountOut);
309: to.safeTransferETH(ethAmountOut);
311: token.safeTransfer(to, tokenAmountOut);
328: IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
330: IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
349: inToken = IMagicLP(firstLp)._BASE_TOKEN_();
351: inToken = IMagicLP(firstLp)._QUOTE_TOKEN_();
360: inToken.safeTransfer(address(firstLp), msg.value);
380: outToken = IMagicLP(lastLp)._QUOTE_TOKEN_();
382: outToken = IMagicLP(lastLp)._BASE_TOKEN_();
393: IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
395: IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
399: weth.withdraw(amountOut);
401: to.safeTransferETH(amountOut);
411: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
421: address baseToken = IMagicLP(lp)._BASE_TOKEN_();
428: baseToken.safeTransfer(lp, msg.value);
439: if (IMagicLP(lp)._QUOTE_TOKEN_() != address(weth)) {
443: IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
445: weth.withdraw(amountOut);
446: to.safeTransferETH(amountOut);
456: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
467: address quoteToken = IMagicLP(lp)._QUOTE_TOKEN_();
474: quoteToken.safeTransfer(lp, msg.value);
485: if (IMagicLP(lp)._BASE_TOKEN_() != address(weth)) {
489: IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
491: weth.withdraw(amountOut);
492: to.safeTransferETH(amountOut);
500: (shares, , ) = IMagicLP(lp).buyShares(to);
514: (uint256 baseReserve, uint256 quoteReserve) = IMagicLP(lp).getReserves();
515: uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;
516: uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;
521: if (IERC20(lp).totalSupply() == 0) {
522: uint256 i = IMagicLP(lp)._I_();
547: IMagicLP(path[i]).sellBase(address(path[i + 1]));
550: IMagicLP(path[i]).sellQuote(address(path[i + 1]));
561: amountOut = IMagicLP(path[iterations]).sellBase(to);
563: amountOut = IMagicLP(path[iterations]).sellQuote(to);
572: amountOut = IMagicLP(lp).sellBase(to);
579: amountOut = IMagicLP(lp).sellQuote(to);
```
[64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L64) | [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L66) | [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L68) | [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L69) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L70) | [83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L83) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L85) | [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L88) | [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L91) | [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92) | [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L93) | [117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L117) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L119) | [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L120) | [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L129) | [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L136) | [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L172) | [173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L173) | [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L186) | [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L187) | [202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L202) | [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L204) | [208](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L208) | [217](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L217) | [221](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L221) | [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L224) | [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L236) | [238](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L238) | [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L239) | [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L244) | [246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L246) | [252](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L252) | [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L253) | [255](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L255) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L269) | [271](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L271) | [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282) | [284](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L284) | [286](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L286) | [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L287) | [295](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L295) | [296](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L296) | [308](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L308) | [309](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L309) | [311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L311) | [328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L328) | [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L330) | [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L349) | [351](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L351) | [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L360) | [380](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L380) | [382](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L382) | [393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L393) | [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L395) | [399](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L399) | [401](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L401) | [411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L411) | [421](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L421) | [428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L428) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L439) | [443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L443) | [445](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L445) | [446](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L446) | [456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L456) | [467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L467) | [474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L474) | [485](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L485) | [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L489) | [491](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L491) | [492](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L492) | [500](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L500) | [514](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L514) | [515](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L515) | [516](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L516) | [521](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L521) | [522](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L522) | [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L547) | [550](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L550) | [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L561) | [563](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L563) | [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L572) | [579](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L579)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

25: baseDecimals = IERC20Metadata(pair_._BASE_TOKEN_()).decimals();
26: quoteDecimals = IERC20Metadata(pair_._QUOTE_TOKEN_()).decimals();
34: (uint256 baseReserve, uint256 quoteReserve) = pair.getReserves();
38: uint256 baseAnswerNomalized = uint256(baseOracle.latestAnswer()) * (10 ** (WAD - baseOracle.decimals()));
39: uint256 quoteAnswerNormalized = uint256(quoteOracle.latestAnswer()) * (10 ** (WAD - quoteOracle.decimals()));
45: return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L25) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L26) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L34) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L38) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L39) | [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45)

```solidity
File: src/staking/LockingMultiRewards.sol

180: stakingToken.safeTransfer(msg.sender, amount);
270: return MathLib.min(block.timestamp, _rewardData[rewardToken].periodFinish);
330: tokenAddress.safeTransfer(owner, tokenAmount);
367: rewardToken.safeTransferFrom(msg.sender, address(this), amount);
464: stakingToken.safeTransferFrom(msg.sender, address(this), amount);
637: rewardToken.safeTransfer(user, amount);
```
[180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L180) | [270](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L270) | [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L330) | [367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367) | [464](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L464) | [637](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L637)
</details>

### [G-61] Consider Using Mappings Instead of Arrays to Save Gas

When you use arrays in Solidity, extra bytecode is generated to check whether the index being accessed is valid.
This ensures you don't read unallocated or dangerous memory locations, but it costs additional gas.

Mappings, being simple key-value pairs, do not have this check, which can save around 2102 gas per read operation.
Below array reads that can be replaced with mappings and saves 2102 on each read.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/staking/LockingMultiRewards.sol

548: _updateRewardsGlobal(rewardTokens[i], totalSupply_);
```
[548](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L548)
</details>

### [G-62] Mark Functions That Revert For Normal Users As `payable`

Functions guaranteed to revert when called by normal users can be marked `payable`.
If a function modifier such as onlyOwner is used, the function will revert if a normal user tries to pay the function.
Marking the function as payable will lower the gas cost for legitimate callers because the compiler will not include checks for whether a payment was provided.

The extra opcodes avoided are CALLVALUE(2),DUP1(3),ISZERO(3),PUSH2(3),JUMPI(10),PUSH1(3),DUP1(3),REVERT(0),JUMPDEST(1),POP(2), which costs an average of about 21 gas per call to the function, in addition to the extra deployment cost.

<details>
<summary><i>53 issue instances in 10 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

51: function claimGasYields() external onlyOperators returns (uint256) {
55: function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
67: function callBlastPrecompile(bytes calldata data) external onlyOwner {
71: function setFeeTo(address feeTo_) external onlyOwner {
80: function setTokenEnabled(address token, bool enabled) external onlyOwner {
```
[51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L51) | [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L55) | [67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L67) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L71) | [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L80)

```solidity
File: src/blast/BlastGovernor.sol

27: function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
31: function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
39: function setFeeTo(address _feeTo) external onlyOwner {
48: function callBlastPrecompile(bytes calldata data) external onlyOwner {
52: function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```
[27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L27) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L31) | [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L39) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L48) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L52)

```solidity
File: src/blast/BlastMagicLP.sol

46: function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {
52: function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {
63: function updateTokenClaimables() external onlyClones onlyImplementationOperators {
71: function callBlastPrecompile(bytes calldata data) external onlyClones onlyImplementationOwner {
79: function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
88: function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```
[46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L46) | [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L52) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L63) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L71) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L79) | [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L88)

```solidity
File: src/blast/BlastOnboarding.sol

100: function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
122: function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
131: function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
146: function setFeeTo(address feeTo_) external onlyOwner {
155: function callBlastPrecompile(bytes calldata data) external onlyOwner {
159: function claimGasYields() external onlyOwner returns (uint256) {
163: function claimTokenYields(address[] memory tokens) external onlyOwner {
174: function setTokenSupported(address token, bool supported) external onlyOwner {
184: function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
189: function setBootstrapper(address bootstrapper_) external onlyOwner {
194: function open() external onlyOwner onlyState(State.Idle) {
199: function close() external onlyOwner onlyState(State.Opened) {
204: function rescue(address token, address to, uint256 amount) external onlyOwner {
213: function pause() external onlyOwner {
217: function unpause() external onlyOwner {
```
[100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L100) | [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L122) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L131) | [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L146) | [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L155) | [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L159) | [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L163) | [174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L174) | [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L184) | [189](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L189) | [194](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L194) | [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L199) | [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L204) | [213](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L213) | [217](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L217)

```solidity
File: src/blast/BlastOnboardingBoot.sol

95: function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
128: function initialize(Router _router) external onlyOwner {
137: function setStaking(LockingMultiRewards _staking) external onlyOwner {
145: function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
```
[95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L95) | [128](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L128) | [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137) | [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L145)

```solidity
File: src/blast/BlastTokenRegistry.sol

13: function setNativeYieldTokenEnabled(address token, bool enabled) external onlyOwner {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L13)

```solidity
File: src/mimswap/MagicLP.sol

460: function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {
469: function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner {
503: function ratioSync() external nonReentrant onlyImplementationOwner {
```
[460](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L460) | [469](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L469) | [503](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L503)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

45: function setMaintainer(address maintainer_) external onlyOwner {
57: function setImplementation(address implementation_) public onlyOwner {
```
[45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L45) | [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)

```solidity
File: src/mimswap/periphery/Factory.sol

95: function setLpImplementation(address implementation_) external onlyOwner {
104: function setMaintainerFeeRateModel(IFeeRateModel maintainerFeeRateModel_) external onlyOwner {
116: function addPool(address creator, address baseToken, address quoteToken, address pool) external onlyOwner {
119: function removePool(
        address creator,
        address baseToken,
        address quoteToken,
        uint256 poolIndex,
        uint256 userPoolIndex
    ) external onlyOwner {
```
[95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L95) | [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L104) | [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L116) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L119)

```solidity
File: src/staking/LockingMultiRewards.sol

300: function addReward(address rewardToken) public onlyOwner {
316: function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
324: function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {
337: function pause() external onlyOwner {
340: function unpause() external onlyOwner {
348: function stakeFor(address account, uint256 amount, bool lock_) external onlyOperators {
361: function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
397: function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
```
[300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300) | [316](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L316) | [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L324) | [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337) | [340](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L340) | [348](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L348) | [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361) | [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397)
</details>

### [G-63] Prefer `private` over `public` for Constants to Save Gas

Using `private` instead of `public` for constants can save gas.

The compiler doesn't need to create non-payable getter functions for deployment calldata, store the bytes of the value outside of where it's used, or add another entry to the method ID table, saving 3406-3606 gas in deployment.

If needed, the values can be read from the verified contract source code, or a single getter function that returns a tuple of the values of all currently public constants can be implemented.

<details>
<summary><i>8 issue instances in 4 files:</i></summary>

```solidity
File: src/blast/libraries/BlastPoints.sol

7: address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;
8: IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);
```
[7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L7) | [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L8)

```solidity
File: src/mimswap/MagicLP.sol

63: uint256 public constant MAX_I = 10 ** 36;
64: uint256 public constant MAX_K = 10 ** 18;
65: uint256 public constant MIN_LP_FEE_RATE = 1e14; // 0.01%
66: uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%
```
[63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64) | [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L65) | [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L66)

```solidity
File: src/mimswap/periphery/Router.sol

31: uint256 public constant MAX_BASE_QUOTE_DECIMALS_DIFFERENCE = 12;
```
[31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L31)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

16: uint256 public constant WAD = 18;
```
[16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L16)
</details>

### [G-64] `<x> += <y>` costs more gas than `<x> = <x> + <y>` for state variables

Using the addition operator instead of plus-equals saves gas.
Replace `<x> += <y>` or `<x> -= <y>` with `<x> = <x> + <y>` or `<x> = <x> - <y>`.

<details>
<summary><i>9 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

553: _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
```
[553](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L553)

```solidity
File: src/staking/LockingMultiRewards.sol

163: unlockedSupply -= amount;
178: unlockedSupply -= amount;
181: stakingTokenBalance -= amount;
441: unlockedSupply += amount;
442: lockedSupply -= amount;
465: stakingTokenBalance += amount;
473: unlockedSupply += amount;
486: lockedSupply += amount;
```
[163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L163) | [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L178) | [181](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L181) | [441](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L441) | [442](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L442) | [465](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L465) | [473](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L473) | [486](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L486)
</details>

### [G-65] Using `bool`s for storage incurs overhead

Utilizing booleans for storage is less gas-efficient compared to using types that consume a full word like uint256.
Every write operation on a boolean necessitates an extra SLOAD operation to read the slot's current value, modify the boolean bits, and then write back.
This additional step is the compiler's measure against contract upgrades and pointer aliasing.

To enhance gas efficiency, consider using `uint256(0)` for false and `uint256(1)` for true, bypassing the extra Gwarmaccess (100 gas) incurred by the SLOAD.

<details>
<summary><i>7 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

21: mapping(address => bool) public enabledTokens;
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21)

```solidity
File: src/blast/BlastMagicLP.sol

21: mapping(address => bool) public operators;
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L21)

```solidity
File: src/blast/BlastOnboarding.sol

36: mapping(address token => bool) public supportedTokens;
```
[36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36)

```solidity
File: src/blast/BlastOnboardingBoot.sol

28: bool public ready;
30: mapping(address user => bool claimed) public claimed;
```
[28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L28) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L30)

```solidity
File: src/blast/BlastTokenRegistry.sol

10: mapping(address => bool) public nativeYieldTokens;
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10)

```solidity
File: src/mimswap/MagicLP.sol

68: bool internal _INITIALIZED_;
```
[68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L68)
</details>

### [G-66] Optimize Gas by Using Only Named Returns

The Solidity compiler can generate more efficient bytecode when using named returns.
It's recommended to replace anonymous returns with named returns for potential gas savings.

Example:
```solidity
/// 985 gas cost
function add(uint256 x, uint256 y) public pure returns (uint256) {
    return x + y;
}
/// 941 gas cost
function addNamed(uint256 x, uint256 y) public pure returns (uint256 res) {
    res = x + y;
}
```

<details>
<summary><i>56 issue instances in 13 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

51: function claimGasYields() external onlyOperators returns (uint256) {
102: function isOwner(address _account) internal view override returns (bool) {
```
[51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L51) | [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L102)

```solidity
File: src/blast/BlastGovernor.sol

27: function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
31: function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
```
[27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L27) | [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L31)

```solidity
File: src/blast/BlastMagicLP.sol

38: function version() external pure override returns (string memory) {
46: function claimGasYields() external onlyClones onlyImplementationOperators returns (uint256) {
```
[38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L38) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L46)

```solidity
File: src/blast/BlastOnboarding.sol

159: function claimGasYields() external onlyOwner returns (uint256) {
225: function _implementation() internal view override returns (address) {
```
[159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L159) | [225](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L225)

```solidity
File: src/blast/BlastOnboardingBoot.sol

95: function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
```
[95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L95)

```solidity
File: src/blast/libraries/BlastYields.sol

37: function claimMaxGasYields(address recipient) internal returns (uint256) {
59: function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {
74: function claimTokenYields(address token, uint256 amount, address recipient) internal returns (uint256) {
```
[37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L37) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L59) | [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L74)

```solidity
File: src/mimswap/MagicLP.sol

154: function name() public view override returns (string memory) {
158: function symbol() public pure override returns (string memory) {
162: function decimals() public view override returns (uint8) {
235: function version() external pure virtual returns (string memory) {
```
[154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L154) | [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L158) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L162) | [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L235)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

22: function mulFloor(uint256 target, uint256 d) internal pure returns (uint256) {
26: function mulCeil(uint256 target, uint256 d) internal pure returns (uint256) {
30: function divFloor(uint256 target, uint256 d) internal pure returns (uint256) {
34: function divCeil(uint256 target, uint256 d) internal pure returns (uint256) {
38: function reciprocalFloor(uint256 target) internal pure returns (uint256) {
42: function reciprocalCeil(uint256 target) internal pure returns (uint256) {
46: function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```
[22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L22) | [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L26) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L30) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L34) | [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L38) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L42) | [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L46)

```solidity
File: src/mimswap/libraries/Math.sol

18: function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {
51: function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {
79: function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
131: function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L18) | [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51) | [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L79) | [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

202: function getMidPrice(PMMState memory state) internal pure returns (uint256) {
```
[202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L202)

```solidity
File: src/mimswap/periphery/Factory.sol

52: function getPoolCount(address token0, address token1) external view returns (uint256) {
56: function getUserPoolCount(address creator) external view returns (uint256) {
64: function predictDeterministicAddress(
        address creator,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) public view returns (address) {
154: function _computeSalt(
        address sender_,
        address baseToken_,
        address quoteToken_,
        uint256 lpFeeRate_,
        uint256 i_,
        uint256 k_
    ) internal view returns (bytes32) {
```
[52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L52) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L56) | [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L64) | [154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L154)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

28: function decimals() external pure override returns (uint8) {
32: function _getReserves() internal view virtual returns (uint256, uint256) {
36: function latestAnswer() public view override returns (int256) {
47: function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```
[28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L28) | [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L32) | [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L36) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L47)

```solidity
File: src/staking/LockingMultiRewards.sol

199: function rewardData(address token) external view returns (Reward memory) {
202: function rewardsForDuration(address rewardToken) external view returns (uint256) {
206: function rewardTokensLength() external view returns (uint256) {
210: function balances(address user) external view returns (Balances memory) {
214: function userRewardLock(address user) external view returns (RewardLock memory) {
218: function userLocks(address user) external view returns (LockedBalance[] memory) {
222: function userLocksLength(address user) external view returns (uint256) {
226: function locked(address user) external view returns (uint256) {
230: function unlocked(address user) external view returns (uint256) {
234: function totalSupply() public view returns (uint256) {
238: function balanceOf(address user) public view returns (uint256) {
253: function nextUnlockTime() public view returns (uint256) {
256: function epoch() public view returns (uint256) {
260: function nextEpoch() public view returns (uint256) {
264: function remainingEpochTime() public view returns (uint256) {
268: function lastTimeRewardApplicable(address rewardToken) public view returns (uint256) {
272: function rewardPerToken(address rewardToken) public view returns (uint256) {
276: function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
287: function earned(address user, address rewardToken) public view returns (uint256) {
291: function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {
```
[199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199) | [202](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L202) | [206](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L206) | [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L210) | [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L214) | [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L218) | [222](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L222) | [226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L226) | [230](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L230) | [234](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L234) | [238](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L238) | [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L253) | [256](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L256) | [260](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L260) | [264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L264) | [268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L268) | [272](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L272) | [276](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L276) | [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L287) | [291](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L291)
</details>

### [G-67] Cache State Variable Reads Outside Loops

Accessing state variables directly within loops can lead to increased gas costs due to the higher expense of state reads.
To optimize for gas efficiency, consider caching state variable values in local variables before the loop.
This practice reduces the number of costly state reads, particularly beneficial when loops execute multiple iterations
Refactor your contract to move state variable reads outside of loops wherever possible, enhancing performance and cost-effectiveness.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit access state variable `feeTo` access inside loop
170: BlastYields.claimAllTokenYields(tokens[i], feeTo);
```
[170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L170)
</details>

### [G-68] Usage of `uints`/`ints` smaller than 32 bytes (256 bits) incurs overhead

Usage of uints/ints smaller than 32 bytes (256 bits) incurs overhead. The Ethereum Virtual Machine (EVM) operates on 32 bytes at a time. Therefore, if an element is smaller than 32 bytes, the EVM must use more operations to reduce the size of the element from 32 bytes to the desired size. 

Operations involving smaller size uints/ints cost extra gas due to the compiler having to clear the higher bits of the memory word before operating on the small size integer. This also includes the associated stack operations of doing so. 

It's recommended to use larger sizes and downcast where needed to optimize for gas efficiency.

<details>
<summary><i>45 issue instances in 4 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

72: uint112 public _BASE_RESERVE_;
73: uint112 public _QUOTE_RESERVE_;
74: uint32 public _BLOCK_TIMESTAMP_LAST_;
76: uint112 public _BASE_TARGET_;
77: uint112 public _QUOTE_TARGET_;
78: uint32 public _RState_;
125: _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);
139: if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
140: _RState_ = uint32(PMMPricing.RState.ONE);
144: if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
145: _RState_ = uint32(PMMPricing.RState.ONE);
163: function decimals() public view override returns (uint8) {
256: if (_RState_ != uint32(newRState)) {
258: _RState_ = uint32(newRState);
279: if (_RState_ != uint32(newRState)) {
281: _RState_ = uint32(newRState);
320: if (_RState_ != uint32(newRState)) {
322: _RState_ = uint32(newRState);
342: if (_RState_ != uint32(newRState)) {
344: _RState_ = uint32(newRState);
438: _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
439: _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
493: _LP_FEE_RATE_ = uint64(newLpFeeRate);
494: _K_ = uint64(newK);
495: _I_ = uint128(newI);
508: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
514: _BASE_RESERVE_ = uint112(baseBalance);
517: _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
518: _QUOTE_RESERVE_ = uint112(quoteBalance);
532: if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
536: _BASE_RESERVE_ = uint112(baseBalance);
537: _QUOTE_RESERVE_ = uint112(quoteBalance);
538: _BASE_TARGET_ = uint112(baseBalance);
539: _QUOTE_TARGET_ = uint112(quoteBalance);
540: _RState_ = uint32(PMMPricing.RState.ONE);
546: uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
547: uint32 timeElapsed = blockTimestamp - _BLOCK_TIMESTAMP_LAST_;
```
[72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73) | [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76) | [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77) | [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L78) | [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L125) | [139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139) | [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L140) | [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144) | [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L145) | [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163) | [256](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L256) | [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L258) | [279](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L279) | [281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L281) | [320](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L320) | [322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L322) | [342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L342) | [344](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L344) | [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439) | [493](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L493) | [494](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L494) | [495](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L495) | [508](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [514](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L514) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517) | [518](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L518) | [532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L532) | [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L536) | [537](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L537) | [538](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L538) | [539](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L539) | [540](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L540) | [546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L546) | [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L547)

```solidity
File: src/mimswap/periphery/Router.sol

598: function _validateDecimals(uint8 baseDecimals, uint8 quoteDecimals) internal pure {
```
[598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L598)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

13: uint8 public immutable baseDecimals;
14: uint8 public immutable quoteDecimals;
29: function decimals() external pure override returns (uint8) {
48: function latestRoundData() external view returns (uint80, int256, uint256, uint256, uint80) {
```
[13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L14) | [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L29) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L48)

```solidity
File: src/staking/LockingMultiRewards.sol

389: reward.lastUpdateTime = uint248(block.timestamp);
533: _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow
```
[389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L389) | [533](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L533)
</details>

### [G-69] Unlimited gas consumption risk due to external call recipients

When calling an external function without specifying a gas limit , the called contract may consume all the remaining gas, causing the tx to be reverted.
To mitigate this, it is recommended to explicitly set a gas limit when making low level external calls.

<details>
<summary><i>1 issue instances in 1 files:</i></summary>

```solidity
File: src/blast/BlastGovernor.sol

54: (success, result) = to.call{value: value}(data);
```
[54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L54)
</details>

### [G-70] Use assembly to check for `address(0)`

The usage of inline assembly to check if variable is the zero can save gas compared to traditional `require` or `if` statement checks. 

The assembly check uses the `extcodesize` operation which is generally cheaper in terms of gas.

[More information can be found here.](https://medium.com/@kalexotsu/solidity-assembly-checking-if-an-address-is-0-efficiently-d2bfe071331)

<details>
<summary><i>26 issue instances in 12 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

25: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
28: if (address(registry_) == address(0)) {
            revert ErrZeroAddress();
73: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L25) | [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L28) | [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L73)

```solidity
File: src/blast/BlastGovernor.sol

16: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
41: if(_feeTo == address(0)) {
            revert ErrZeroAddress();
```
[16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L16) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L41)

```solidity
File: src/blast/BlastMagicLP.sol

24: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
27: if (address(registry_) == address(0)) {
            revert ErrZeroAddress();
81: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
```
[24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L24) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L27) | [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L81)

```solidity
File: src/blast/BlastOnboarding.sol

85: if (address(registry_) == address(0)) {
            revert ErrZeroAddress();
89: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
148: if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
```
[85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L85) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L89) | [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L148)

```solidity
File: src/blast/BlastOnboardingBoot.sol

97: if (pool != address(0)) {
            revert ErrAlreadyBootstrapped();
```
[97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L97)

```solidity
File: src/blast/BlastTokenRegistry.sol

15: if (token == address(0)) {
            revert ErrZeroAddress();
```
[15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L15)

```solidity
File: src/blast/BlastWrappers.sol

21: if (governor_ == address(0)) {
            revert ErrZeroAddress();
35: if (governor_ == address(0)) {
            revert ErrZeroAddress();
48: if (governor_ == address(0)) {
            revert ErrZeroAddress();
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L21) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L35) | [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L48)

```solidity
File: src/mimswap/MagicLP.sol

102: if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
            revert ErrZeroAddress();
```
[102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

23: if (maintainer_ == address(0)) {
            revert ErrZeroAddress();
35: if (implementation == address(0)) {
            return (lpFeeRate, 0);
47: if (maintainer_ == address(0)) {
            revert ErrZeroAddress();
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L23) | [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L35) | [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L47)

```solidity
File: src/mimswap/periphery/Factory.sol

39: if (implementation_ == address(0)) {
            revert ErrZeroAddress();
42: if (address(maintainerFeeRateModel_) == address(0)) {
            revert ErrZeroAddress();
97: if (implementation_ == address(0)) {
            revert ErrZeroAddress();
106: if (address(maintainerFeeRateModel_) == address(0)) {
            revert ErrZeroAddress();
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L39) | [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L42) | [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L97) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L106)

```solidity
File: src/mimswap/periphery/Router.sol

39: if (address(weth_) == address(0) || address(factory_) == address(0)) {
            revert ErrZeroAddress();
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L39)

```solidity
File: src/staking/LockingMultiRewards.sol

301: if (rewardToken == address(0)) {
            revert ErrInvalidTokenAddress();
```
[301](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L301)
</details>

### [G-71] `internal`/`private` functions only called once can be inlined to save gas

`internal` functions that are only called once should be inlined to save gas. 
Not inlining such functions costs an extra 20 to 40 gas due to the additional `JUMP` instructions and stack operations required for function calls.

<details>
<summary><i>11 issue instances in 6 files:</i></summary>

```solidity
File: src/mimswap/MagicLP.sol

/// @audit function `_resetTargetAndReserve()` called only once
528: function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {
/// @audit function `_afterInitialized()` called only once
601: function _afterInitialized() internal virtual {}
```
[528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L528) | [601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L601)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

/// @audit function `powFloor()` called only once
47: function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
```
[47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L47)

```solidity
File: src/mimswap/libraries/Math.sol

/// @audit function `divCeil()` called only once
19: function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L19)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

/// @audit function `_RBelowSellQuoteToken()` called only once
134: function _RBelowSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {
/// @audit function `_RBelowSellBaseToken()` called only once
147: function _RBelowSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {
/// @audit function `_RAboveSellBaseToken()` called only once
162: function _RAboveSellBaseToken(
        PMMState memory state,
        uint256 payBaseAmount
    )
        internal
        pure
        returns (
            uint256 // receiveQuoteToken
        )
    {
/// @audit function `_RAboveSellQuoteToken()` called only once
175: function _RAboveSellQuoteToken(
        PMMState memory state,
        uint256 payQuoteAmount
    )
        internal
        pure
        returns (
            uint256 // receiveBaseToken
        )
    {
```
[134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L134) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L147) | [162](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L162) | [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L175)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

/// @audit function `_getReserves()` called only once
33: function _getReserves() internal view virtual returns (uint256, uint256) {
```
[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L33)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit function `_updateRewards()` called only once
544: function _updateRewards() internal {
/// @audit function `_updateRewardsForUsers()` called only once
572: function _updateRewardsForUsers(address[] memory users) internal {
```
[544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L544) | [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L572)
</details>

### [G-72] Consider using OZ EnumerateSet in place of nested mappings

Nested mappings and multi-dimensional arrays in Solidity operate through a process of double hashing, wherein the original storage slot and the first key are concatenated and hashed, and then this hash is again concatenated with the second key and hashed. This process can be quite gas expensive due to the double-hashing operation and subsequent storage operation (sstore).

A possible optimization involves manually concatenating the keys followed by a single hash operation and an sstore. However, this technique introduces the risk of storage collision, especially when there are other nested hash maps in the contract that use the same key types. Because Solidity is unaware of the number and structure of nested hash maps in a contract, it follows a conservative approach in computing the storage slot to avoid possible collisions.

OpenZeppelin's EnumerableSet provides a potential solution to this problem. It creates a data structure that combines the benefits of set operations with the ability to enumerate stored elements, which is not natively available in Solidity. EnumerableSet handles the element uniqueness internally and can therefore provide a more gas-efficient and collision-resistant alternative to nested mappings or multi-dimensional arrays in certain scenarios.

<details>
<summary><i>4 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboarding.sol

41: mapping(address user => mapping(address token => Balances)) public balances;
```
[41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L41)

```solidity
File: src/mimswap/periphery/Factory.sol

34: mapping(address base => mapping(address quote => address[] pools)) public pools;
```
[34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L34)

```solidity
File: src/staking/LockingMultiRewards.sol

93: mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
95: mapping(address user => mapping(address token => uint256 amount)) public rewards;
```
[93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L93) | [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L95)
</details>

### [G-73] Declare `immutable` as `private` to save gas

Using `private` instead of `public` for immutables saves gas.

The compiler doesn't need to create non-payable getter functions for deployment calldata, store the bytes of the value outside of where it's used, or add another entry to the method ID table, saving 3406-3606 gas in deployment.

<details>
<summary><i>15 issue instances in 6 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

20: BlastTokenRegistry public immutable registry;
```
[20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L20)

```solidity
File: src/blast/BlastMagicLP.sol

17: BlastTokenRegistry public immutable registry;
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L17)

```solidity
File: src/mimswap/MagicLP.sol

61: MagicLP public immutable implementation;
```
[61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L61)

```solidity
File: src/mimswap/periphery/Router.sol

33: IWETH public immutable weth;
34: IFactory public immutable factory;
```
[33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L33) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L34)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

10: IMagicLP public immutable pair;
11: IAggregator public immutable baseOracle;
12: IAggregator public immutable quoteOracle;
13: uint8 public immutable baseDecimals;
14: uint8 public immutable quoteDecimals;
```
[10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L10) | [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L11) | [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L12) | [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L13) | [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L14)

```solidity
File: src/staking/LockingMultiRewards.sol

83: uint256 public immutable maxLocks;
84: uint256 public immutable lockingBoostMultiplerInBips;
85: uint256 public immutable rewardsDuration;
86: uint256 public immutable lockDuration;
87: address public immutable stakingToken;
```
[83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L83) | [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L84) | [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L85) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L86) | [87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L87)
</details>

### [G-74] State variables should be cached in stack rather than re-reading them from storage

Caching state variables in local variables can optimize gas usage, as accessing the stack is cheaper than accessing storage.

The instances below point to the second+ access of a state variable within a function.

<details>
<summary><i>52 issue instances in 3 files:</i></summary>

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit function bootstrap() uses state variable `pool` 5 times
97: if (pool != address(0)) {
106: (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
117: staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
124: emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);
126: return (pool, address(staking), totalPoolShares);
/// @audit function bootstrap() uses state variable `router` 2 times
103: MIM.safeApprove(address(router), type(uint256).max);
104: USDB.safeApprove(address(router), type(uint256).max);
/// @audit function bootstrap() uses state variable `totalPoolShares` 5 times
106: (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
108: if (totalPoolShares < minAmountOut) {
122: pool.safeApprove(address(staking), totalPoolShares);
124: emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);
126: return (pool, address(staking), totalPoolShares);
/// @audit function bootstrap() uses state variable `staking` 3 times
122: pool.safeApprove(address(staking), totalPoolShares);
124: emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);
126: return (pool, address(staking), totalPoolShares);
```
[97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L97) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106) | [117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117) | [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124) | [126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L126) | [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L103) | [104](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L104) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106) | [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L108) | [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L122) | [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124) | [126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L126) | [122](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L122) | [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124) | [126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L126)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit function correctRState() uses state variable `_BASE_RESERVE_` 3 times
139: if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
141: _BASE_TARGET_ = _BASE_RESERVE_;
141: _BASE_TARGET_ = _BASE_RESERVE_;
/// @audit function correctRState() uses state variable `_QUOTE_RESERVE_` 3 times
142: _QUOTE_TARGET_ = _QUOTE_RESERVE_;
144: if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
142: _QUOTE_TARGET_ = _QUOTE_RESERVE_;
/// @audit function flashLoan() uses state variable `_BASE_TOKEN_` 2 times
325: emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);
347: emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
/// @audit function flashLoan() uses state variable `_QUOTE_TOKEN_` 2 times
325: emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);
347: emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
/// @audit function flashLoan() uses state variable `_BASE_RESERVE_` 4 times
302: if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
308: if (baseBalance < _BASE_RESERVE_) {
315: if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {
246: uint256 baseInput = baseBalance - uint256(_BASE_RESERVE_);
/// @audit function flashLoan() uses state variable `_QUOTE_RESERVE_` 4 times
302: if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
269: uint256 quoteInput = quoteBalance - uint256(_QUOTE_RESERVE_);
330: if (quoteBalance < _QUOTE_RESERVE_) {
337: if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {
/// @audit function flashLoan() uses state variable `_RState_` 2 times
256: if (_RState_ != uint32(newRState)) {
256: if (_RState_ != uint32(newRState)) {
/// @audit function buyShares() uses state variable `_BASE_TARGET_` 2 times
402: _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();
402: _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();
/// @audit function buyShares() uses state variable `_QUOTE_TARGET_` 2 times
403: _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
403: _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
/// @audit function buyShares() uses state variable `_I_` 3 times
381: shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;
381: shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;
383: _QUOTE_TARGET_ = DecimalMath.mulFloor(shares, _I_).toUint112();
/// @audit function sellShares() uses state variable `_BASE_TARGET_` 2 times
438: _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
438: _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
/// @audit function sellShares() uses state variable `_QUOTE_TARGET_` 2 times
439: _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
439: _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
/// @audit function ratioSync() uses state variable `_BASE_RESERVE_` 2 times
512: if (baseBalance != _BASE_RESERVE_) {
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
/// @audit function ratioSync() uses state variable `_QUOTE_RESERVE_` 2 times
516: if (quoteBalance != _QUOTE_RESERVE_) {
517: _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));
```
[139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139) | [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L141) | [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L141) | [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L142) | [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144) | [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L142) | [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L325) | [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L347) | [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L325) | [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L347) | [302](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302) | [308](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L308) | [315](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L315) | [246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L246) | [302](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302) | [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L269) | [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L330) | [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L337) | [256](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L256) | [256](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L256) | [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402) | [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402) | [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403) | [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403) | [381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L381) | [381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L381) | [383](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L383) | [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439) | [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439) | [512](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L512) | [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513) | [516](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L516) | [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit function create() uses state variable `maintainerFeeRateModel` 2 times
86: IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
88: emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
```
[86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L86) | [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88)
</details>

### [G-75] Division by powers of two should use bit shifting

When dividing by powers of two (e.g., 2, 4, 8), it is more efficient to use bit shifting.

`<x> / 2` can be replaced with `<x> >> 1`, as both operations use the SHR opcode in the compiler.
However, the division approach incurs an additional 20 gas overhead due to jumps to and from a compiler utility function that introduces checks.

This overhead can be avoided by using `unchecked` around the division by powers of two.

<details>
<summary><i>4 issue instances in 2 files:</i></summary>

```solidity
File: src/mimswap/libraries/DecimalMath.sol

53: uint p = powFloor(target, e / 2);
```
[53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L53)

```solidity
File: src/mimswap/libraries/Math.sol

30: uint256 z = x / 2 + 1;
34: z = (x / z + z) / 2;
115: and Q2=(-b+sqrt(b^2+4(1-k)kQ0^2))/2(1-k)
```
[30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L30) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34) | [115](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L115)
</details>

### [G-76] Optimize names to save gas

Function names for public and external methods, as well as public state variable names, can be optimized to achieve gas savings.
By renaming functions to generate method IDs with two leading zero bytes, you can save 128 gas during contract deployment.
Further, renaming functions for lower method IDs can conserve 22 gas per call for each sorted position shifted.

Optimizing function names for gas efficiency can result in significant savings, especially for frequently called functions or heavily deployed contracts. 
Reference: [Solidity Gas Optimizations - Function Name](https://blog.emn178.cc/en/post/solidity-gas-optimization-function-name/)

<details>
<summary><i>24 issue instances in 20 files:</i></summary>

```solidity
File: src/blast/BlastDapp.sol

5: contract BlastDapp {
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L5)

```solidity
File: src/blast/BlastBox.sol

12: contract BlastBox is DegenBox, OperatableV3 {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L12)

```solidity
File: src/blast/BlastGovernor.sol

6: contract BlastGovernor is OperatableV2 {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L6)

```solidity
File: src/blast/BlastMagicLP.sol

9: contract BlastMagicLP is MagicLP {
```
[9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L9)

```solidity
File: src/blast/BlastOnboarding.sol

11: contract BlastOnboardingData is Owned, Pausable {
63: contract BlastOnboarding is BlastOnboardingData, Proxy {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L11) | [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L63)

```solidity
File: src/blast/BlastOnboardingBoot.sol

23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
34: contract BlastOnboardingBoot is BlastOnboardingBootDataV1 {
```
[23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23) | [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L34)

```solidity
File: src/blast/BlastTokenRegistry.sol

5: contract BlastTokenRegistry is Owned {
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L5)

```solidity
File: src/blast/BlastWrappers.sol

18: contract BlastMIMSwapRouter is Router {
27: contract BlastMIMSwapFactory is Factory {
41: contract BlastCauldronV4 is CauldronV4 {
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L18) | [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L27) | [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L41)

```solidity
File: src/blast/libraries/BlastPoints.sol

5: library BlastPoints {
```
[5](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L5)

```solidity
File: src/blast/libraries/BlastYields.sol

6: library BlastYields {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L6)

```solidity
File: src/mimswap/MagicLP.sol

25: contract MagicLP is ERC20, ReentrancyGuard, Owned {
```
[25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L25)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

12: contract FeeRateModel is Owned {
```
[12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L12)

```solidity
File: src/mimswap/auxiliary/FeeRateModelImpl.sol

6: contract FeeRateModelImpl {
```
[6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L6)

```solidity
File: src/mimswap/libraries/DecimalMath.sol

17: library DecimalMath {
```
[17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L17)

```solidity
File: src/mimswap/libraries/Math.sol

16: library Math {
```
[16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L16)

```solidity
File: src/mimswap/libraries/PMMPricing.sol

19: library PMMPricing {
```
[19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L19)

```solidity
File: src/mimswap/periphery/Factory.sol

11: contract Factory is Owned {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L11)

```solidity
File: src/mimswap/periphery/Router.sol

11: contract Router {
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L11)

```solidity
File: src/oracles/aggregators/MagicLpAggregator.sol

8: contract MagicLpAggregator is IAggregator {
```
[8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L8)

```solidity
File: src/staking/LockingMultiRewards.sol

14: contract LockingMultiRewards is OperatableV2, Pausable {
```
[14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L14)
</details>

### [G-77] Avoid updating storage when the value hasn't changed

A check regarding whether the current value and the new value are the same should be added.
This helps prevent unnecessary state changes and events in case the new value is the same as the current value.

<details>
<summary><i>19 issue instances in 10 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

/// @audit Missing `feeTo_` check before state change
76: feeTo = feeTo_;
/// @audit Missing `enabled` check before state change
82: enabledTokens[token] = enabled;
```
[76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L76) | [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L82)

```solidity
File: src/blast/BlastGovernor.sol

/// @audit Missing `_feeTo` check before state change
44: feeTo = _feeTo;
```
[44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L44)

```solidity
File: src/blast/BlastMagicLP.sol

/// @audit Missing `feeTo_` check before state change
84: feeTo = feeTo_;
/// @audit Missing `status` check before state change
90: operators[operator] = status;
```
[84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L84) | [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L90)

```solidity
File: src/blast/BlastOnboarding.sol

/// @audit Missing `feeTo_` check before state change
151: feeTo = feeTo_;
/// @audit Missing `supported` check before state change
176: supportedTokens[token] = supported;
/// @audit Missing `cap` check before state change
186: caps[token] = cap;
/// @audit Missing `bootstrapper_` check before state change
191: bootstrapper = bootstrapper_;
```
[151](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L151) | [176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L176) | [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L186) | [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L191)

```solidity
File: src/blast/BlastOnboardingBoot.sol

/// @audit Missing `_staking` check before state change
141: staking = _staking;
/// @audit Missing `_ready` check before state change
147: ready = _ready;
```
[141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L141) | [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L147)

```solidity
File: src/blast/BlastTokenRegistry.sol

/// @audit Missing `enabled` check before state change
18: nativeYieldTokens[token] = enabled;
```
[18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L18)

```solidity
File: src/mimswap/MagicLP.sol

/// @audit Missing `baseReserve` check before state change
561: _BASE_RESERVE_ = baseReserve.toUint112();
/// @audit Missing `quoteReserve` check before state change
562: _QUOTE_RESERVE_ = quoteReserve.toUint112();
```
[561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L561) | [562](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L562)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

/// @audit Missing `maintainer_` check before state change
50: maintainer = maintainer_;
/// @audit Missing `implementation_` check before state change
58: implementation = implementation_;
```
[50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L50) | [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L58)

```solidity
File: src/mimswap/periphery/Factory.sol

/// @audit Missing `implementation_` check before state change
100: implementation = implementation_;
/// @audit Missing `maintainerFeeRateModel_` check before state change
109: maintainerFeeRateModel = maintainerFeeRateModel_;
```
[100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L100) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L109)

```solidity
File: src/staking/LockingMultiRewards.sol

/// @audit Missing `_minLockAmount` check before state change
319: minLockAmount = _minLockAmount;
```
[319](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L319)
</details>

### [G-78] Optimize External Calls with Assembly for Memory Efficiency

Using interfaces to make external contract calls in Solidity is convenient but can be inefficient in terms of memory utilization.
Each such call involves creating a new memory location to store the data being passed, thus incurring memory expansion costs. 

Inline assembly allows for optimized memory usage by re-using already allocated memory spaces or using the scratch space for smaller datasets.
This can result in notable gas savings, especially for contracts that make frequent external calls.

Additionally, using inline assembly enables important safety checks like verifying if the target address has code deployed to it using `extcodesize(addr)` before making the call, mitigating risks associated with contract interactions.

<details>
<summary><i>43 issue instances in 10 files:</i></summary>

```solidity
File: src/blast/BlastBox.sol

57: if (!registry.nativeYieldTokens(token_)) {
            revert ErrUnsupportedToken();
86: if (registry.nativeYieldTokens(token)) {
            BlastYields.enableTokenClaimable(token);
```
[57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L57) | [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L86)

```solidity
File: src/blast/BlastMagicLP.sol

56: if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
            token0Amount = BlastYields.claimAllTokenYields(_BASE_TOKEN_, feeTo_);
59: if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
            token1Amount = BlastYields.claimAllTokenYields(_QUOTE_TOKEN_, feeTo_);
105: if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
            BlastYields.enableTokenClaimable(_BASE_TOKEN_);
109: if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
            BlastYields.enableTokenClaimable(_QUOTE_TOKEN_);
```
[56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L56) | [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L59) | [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L105) | [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L109)

```solidity
File: src/blast/BlastOnboarding.sol

169: if (registry.nativeYieldTokens(tokens[i])) {
                BlastYields.claimAllTokenYields(tokens[i], feeTo);
178: if (registry.nativeYieldTokens(token)) {
            BlastYields.enableTokenClaimable(token);
```
[169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L169) | [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L178)

```solidity
File: src/blast/BlastOnboardingBoot.sol

69: staking.stakeFor(msg.sender, shares, lock);
89: return router.previewCreatePool(I, baseAmount, quoteAmount);
106: (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
118: staking.setOperator(address(this), true);
119: staking.transferOwnership(owner);
```
[69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L69) | [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L89) | [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L106) | [118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L118) | [119](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L119)

```solidity
File: src/blast/libraries/BlastPoints.sol

11: BLAST_POINTS.configurePointsOperator(BLAST_POINTS_OPERATOR);
```
[11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L11)

```solidity
File: src/blast/libraries/BlastYields.sol

21: if (IERC20Rebasing(token).getConfiguration(address(this)) == YieldMode.CLAIMABLE) {
            return;
25: IERC20Rebasing(token).configure(YieldMode.CLAIMABLE);
30: BLAST_YIELD_PRECOMPILE.configure(YieldMode.CLAIMABLE, GasMode.CLAIMABLE, governor_);
43: amount = BLAST_YIELD_PRECOMPILE.claimMaxGas(contractAddress, recipient);
56: amount = BLAST_YIELD_PRECOMPILE.claimAllYield(contractAddress, recipient);
61: amount = BLAST_YIELD_PRECOMPILE.claimYield(contractAddress, recipient, amount);
71: amount = IERC20Rebasing(token).claim(recipient, IERC20Rebasing(token).getClaimableAmount(address(this)));
76: amount = IERC20Rebasing(token).claim(recipient, amount);
```
[21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L21) | [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L25) | [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L30) | [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L43) | [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L56) | [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L61) | [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L71) | [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L76)

```solidity
File: src/mimswap/MagicLP.sol

174: (uint256 lpFeeRate, uint256 mtFeeRate) = _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_);
187: (uint256 lpFeeRate, uint256 mtFeeRate) = _MT_FEE_RATE_MODEL_.getFeeRate(trader, _LP_FEE_RATE_);
225: return _MT_FEE_RATE_MODEL_.getFeeRate(user, _LP_FEE_RATE_);
295: ICallee(assetTo).FlashLoanCall(msg.sender, baseAmount, quoteAmount, data);
451: ICallee(to).SellShareCall(msg.sender, shareAmount, baseAmount, quoteAmount, data);
```
[174](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L174) | [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L187) | [225](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L225) | [295](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L295) | [451](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L451)

```solidity
File: src/mimswap/auxiliary/FeeRateModel.sol

39: return IFeeRateImpl(implementation).getFeeRate(msg.sender, trader, lpFeeRate);
```
[39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L39)

```solidity
File: src/mimswap/periphery/Factory.sol

86: IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
```
[86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L86)

```solidity
File: src/mimswap/periphery/Router.sol

66: clone = IFactory(factory).create(baseToken, quoteToken, lpFeeRate, i, k);
70: (shares, , ) = IMagicLP(clone).buyShares(to);
88: clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);
93: (shares, , ) = IMagicLP(clone).buyShares(to);
271: return IMagicLP(lp).sellShares(sharesIn, to, minimumBaseAmount, minimumQuoteAmount, "", deadline);
287: (ethAmountOut, tokenAmountOut) = IMagicLP(lp).sellShares(
                sharesIn,
                address(this),
                minimumETHAmount,
                minimumTokenAmount,
                "",
                deadline
            );
296: (tokenAmountOut, ethAmountOut) = IMagicLP(lp).sellShares(
                sharesIn,
                address(this),
                minimumTokenAmount,
                minimumETHAmount,
                "",
                deadline
            );
308: weth.withdraw(ethAmountOut);
399: weth.withdraw(amountOut);
445: weth.withdraw(amountOut);
491: weth.withdraw(amountOut);
500: (shares, , ) = IMagicLP(lp).buyShares(to);
572: amountOut = IMagicLP(lp).sellBase(to);
579: amountOut = IMagicLP(lp).sellQuote(to);
```
[66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L66) | [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L70) | [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L88) | [93](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L93) | [271](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L271) | [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L287) | [296](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L296) | [308](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L308) | [399](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L399) | [445](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L445) | [491](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L491) | [500](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L500) | [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L572) | [579](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L579)
</details>

