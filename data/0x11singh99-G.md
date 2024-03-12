**Note: These all are unique finding are not present in analyzer report.Gas Mentioned in these findings title is total gas saved by all instances of that finding covered in this report.**

# Gas Optimizations

## Table of Contents

- [G-01] [State variables can be packed into fewer storage slot by reducing their size (**Saves ~4000 Gas**)](#g-01-state-variables-can-be-packed-into-fewer-storage-slot-by-reducing-their-size-saves-4000-gas)

- [G-02] [Reduce the size of struct variables and pack them together to save storage slots (**Saves ~2000 Gas**)](#g-02-reduce-the-size-of-struct-variables-and-pack-them-together-to-save-storage-slots-saves-2000-gas)

- [G-03] [Cache external function call to save gas instead of re-calling avoid 1 external call](#g-03-cache-external-function-call-to-save-gas-instead-of-re-calling-avoid-1-external-call)

- [G-04] [State variable only set in the constructor should be declare immutable (**Gas Saved ~2100 Gas**)](#g-04-state-variables-only-set-in-the-constructor-should-be-declared-immutablegas-saved-2100-gas)

- [G-05] [Check before updating bool state variable to avoid with same bool value(Saves ~800 Gas)](#g-05-check-before-updating-bool-state-variable-to-avoid-with-same-bool-value)

- [G-06] [Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct](#g-06-multiple-addressid-mappings-can-be-combined-into-a-single-mapping-of-an-addressid-to-a-struct)

- [G-07] [Multiple accesses of the same mapping/array key/index inside `loop` should be cached(**Gas Saved ~300 Gas**)](#g-07-multiple-accesses-of-the-same-mappingarray-keyindex-inside-loop-should-be-cachedgas-saved-300-gas-per-iteration)

- [G-08] [Use `calldata` instead of `memory` if parameter not get mutated(**Gas Saved ~100 Gas**)](#g-08-use-calldata-instead-of-memory-if-parameter-not-get-mutatedgas-saved-100-gas)
- [G-09] [State variables should be cached in stack variables rather than re-reading them from storage(**Gas Saved ~1800 Gas**)](#g-09-state-variables-should-be-cached-in-stack-variables-rather-than-re-reading-them-from-storagegas-saved-1800-gas)
- [G-10] [Within contract's function call should be cached instead of re-calling the same function](#g-10-within-contracts-function-call-should-be-cached-instead-of-re-calling-the-same-function)
- [G-11] [Nesting `if`-statements is cheaper than using `&&`(**Gas Saved ~24 Gas**)](#g-11-nesting-if-statements-is-cheaper-than-using-gas-saved-24-gas)

- [G-12] [`Switch` the order of `if` statement to fail early saves gas(**~2000 Gas** of Gcoldsload) half of the time](#g-12-switch-the-order-of-if-statement-to-fail-early-saves-gas2000-gas-of-gcoldsload-half-of-the-times)
- [G-13] [Refactor `_getRewards` function to save `1 SLOAD` by caching function call](#g-13-refactor-_getrewards-function-to-save-1-sload-by-caching-function-call)
- [G-14] [Cache calculations instead of recalculating saves checked subtraction and checked multiplication(**Gas Saved ~300 Gas**)](#g-14-cache-calculations-instead-of-recalculating-saves-checked-subtraction-and-checked-multiplicationgas-saved-300-gas)
- [G-15] [Do not cache external call in stack variable if stack variable used only once](#g-15-do-not-cache-external-call-in-stack-variable-if-stack-variable-used-only-once)
-

## Auditor's Disclaimer :

All these findings are good findings and 100% safe to implement at no security/logic risk. They all are found by thorough manual review.

## [G-01] State variables can be packed into fewer storage slot by reducing their size (**Saves ~4000 Gas**)

The EVM works with 32 byte words. Variables less than 32 bytes can be declared next to each other in storage and this will pack the values together into a single 32 byte storage slot (if values combined are <= 32 bytes). If the variables packed together are retrieved together in functions (more likely with structs), we will effectively save ~2000 gas with every subsequent SLOAD for that storage slot. This is due to us incurring a Gwarmaccess (100 gas) versus a Gcoldsload (2100 gas).

### `SAVE: ~4000 GAS, 2 SLOT`

### `_LP_FEE_RATE_`,` _K_` and `_I_` can be packed in single slot SAVES: ~4000 Gas, 2 storage Slot

Since `_LP_FEE_RATE_`,`_K_` and `_I_` can not be more than from their max values:
Here is the constant max values ::
When `_LP_FEE_RATE_`,`_K_` and `_I_` updated inside `init` function and `setParameters` function they are updated only inside those functions and before assigning values in these variables ,values are checked with these values respective MAX constants so that their value can never be more than those defined constants.
That means `_LP_FEE_RATE_` can be max. **1e16**, `_K_` can be max. **1e18** and `_I_` can be maximum **1e36**.
So their sizes can be reduced to `uint64`, `uint64` and `uint128`. So these three can be packed into one slot and saves _Total 2 Storage slots_.
`uint64` can hold up to **1.8e19** and `uint128` can hold up to **~3.4e38**. So they are sufficient enough to hold above values.

```solidity
File : mimswap/MagicLP.sol

63: uint256 public constant MAX_I = 10 ** 36;
64: uint256 public constant MAX_K = 10 ** 18;
...
66: uint256 public constant MAX_LP_FEE_RATE = 1e16; // 1%

```

[MagicLP.sol#L63-L66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63C1-L66C58)

So we can easily reduce there sizes and pack them into single slot.

```solidity
File : mimswap/MagicLP.sol

80: uint256 public _LP_FEE_RATE_;
81: uint256 public _K_;
82: uint256 public _I_;

```

[MagicLP.sol#L80-L82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L80C1-L82C24)

**Recommended Mitigation Steps:**

```diff
File : mimswap/MagicLP.sol

-80: uint256 public _LP_FEE_RATE_;
-81: uint256 public _K_;
-82: uint256 public _I_;

+80: uint64 public _LP_FEE_RATE_;
+81: uint64 public _K_;
+82: uint128 public _I_;

```

## [G-02] Reduce the size of struct variables and pack them together to save storage slots (**Saves ~2000 Gas**)

### `SAVE: ~2000 GAS, 1 SLOT` on every key-value pair in `_rewardData` mapping

### `periodFinish` and `lastUpdateTime` can be reduced to `uint64` and packed with `bool exists` in single slot

Since `periodFinish` and `lastUpdateTime` hold timestamp so these two can be easily reduced to `uint64`.
`uint64` is very big number to hold any realistic timestamp. So it is completely safe to reduce time holding variables to this size. And save slot.

```solidity
File : staking/LockingMultiRewards.sol

50: struct Reward {
51:     uint256 periodFinish;
52:     uint256 rewardRate;
53:     uint256 rewardPerTokenStored;
54:     bool exists;
55:     uint248 lastUpdateTime;
56:    }

```

[LockingMultiRewards.sol#L50-L56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L50C5-L56C6)

**Recommended Mitigation Steps:**

```diff
File : staking/LockingMultiRewards.sol

50: struct Reward {
- 51:     uint256 periodFinish;
52:     uint256 rewardRate;
53:     uint256 rewardPerTokenStored;
54:     bool exists;
+ 51:     uint64 periodFinish;
+ 55:     uint64 lastUpdateTime;
- 55:     uint248 lastUpdateTime;
56:    }

```

## [G-03] Cache external function call to save gas instead of re-calling avoid 1 external call

### Cache external function call `_MT_FEE_RATE_MODEL_.maintainer()`

`_MT_FEE_RATE_MODEL_.maintainer()` will return same value both times in `flashLoan` function. Since it's value haven't impacted by the flashLoan function flow from 319 to 342 line. So it is reduntant and gas consuming to call this external function again for same value. It is better to cache `_MT_FEE_RATE_MODEL_.maintainer()` return value first time and use that value both times when needed. **Avoids 1 external call**.

```solidity
File : mimswap/MagicLP.sol

290: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
...

319:     _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
...
341:            _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);

...
      }
```

[MagicLP.sol#L319-L341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L319C8-L341C72)

**Recommended Mitigation Steps:**

```diff
File : mimswap/MagicLP.sol

+        IFeeRateModel _MT_FEE_RATE_MODEL_maintainer = _MT_FEE_RATE_MODEL_.maintainer();

-319:     _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
+319:     _transferBaseOut(_MT_FEE_RATE_MODEL_maintainer, mtFee);
...
-341:            _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);
+341:            _transferQuoteOut(_MT_FEE_RATE_MODEL_maintainer, mtFee);
```

## [G-04] State variables only set in the constructor should be declared immutable(**Gas Saved ~2100 Gas**)

State variables only set in the constructor should be declared immutable as it avoids a Gsset (20000 gas) in the constructor, and replaces the first access in each transaction (Gcoldsload - 2100 gas) and each access thereafter (Gwarmacces - 100 gas) with a PUSH32 (3 gas).

### Making `registry` immutable will save 1 Storage slot ( ~2100 Gas)

`registry` can be marked immutable. Since it is only set in its child contract `BlastOnboarding` constructor. And apart from this it is never changed. Neither it is set in any `BlastOnboardingData` function where this variable defined nor it is set in child `BlastOnboarding` function apart from it's constructor. Also `BlastOnboarding` not inherited further. So it is completely safe to make this variable immutable so save 1 storage slot.

```solidity
File : blast/BlastOnboarding.sol

93: constructor(BlastTokenRegistry registry_, address feeTo_) {
...
84:    registry = registry_;
85:        feeTo = feeTo_;
86:    }

```

[BlastOnboarding.sol#L84-L96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L84C4-L96C1)

```solidity
File : blast/BlastOnboarding.sol

33:  BlastTokenRegistry public registry;

```

[BlastOnboarding.sol#L33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L33)

**Recommended Mitigation Steps:**

```diff
File : blast/BlastOnboarding.sol

-33:  BlastTokenRegistry public registry;
+33:  BlastTokenRegistry public immutable registry;

```

## [G-05] Check before updating bool state variable to avoid with same bool value.

Check state variable before updating to avoid updating with same bool value. It is highly possible that passed value to change can be same since bool can hold only 2 values. So it better to check that updating value is different from previous value. To avoid SSTORE opcode.

```solidity
File : blast/BlastOnboardingBoot.sol

146:    function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
147:        ready = _ready;
148:        emit LogReadyChanged(ready);
149:    }

```

[BlastOnboardingBoot.sol#L146-L149](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146C1-L149C6)

**Recommended Mitigation Steps:**

```diff
File : blast/BlastOnboardingBoot.sol

146:    function setReady(bool _ready) external onlyOwner onlyState(State.Closed) {
+        if(_ready == ready){
+       revert();
+       }
147:        ready = _ready;
148:        emit LogReadyChanged(ready);
149:    }

```

## [G-06] Multiple address/ID mappings can be combined into a single mapping of an address/ID to a struct

Saves a storage slot for the mapping. Depending on the circumstances and sizes of types, can avoid a Gsset (20000 gas) per mapping combined. Reads and subsequent writes can also be cheaper when a function requires both values and they both fit in the same storage slot. Finally, if both fields are accessed in the same function, can save ~42 gas per access due to not having to recalculate the key's keccak256 hash (Gkeccak256 - 30 gas) and that calculation's associated stack operations

```solidity
File : staking/LockingMultiRewards.sol

90:    mapping(address user => Balances balances) private _balances;
91:    mapping(address user => LockedBalance[] locks) private _userLocks;
92:    mapping(address user => RewardLock rewardLock) private _userRewardLock;
93:
94:    mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
95:    mapping(address user => mapping(address token => uint256 amount)) public rewards;
96:    mapping(address user => uint256 index) public lastLockIndex;

```

[LockingMultiRewards.sol#L90-L96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L90C1-L96C65)

**Recommended Mitigation Steps:**

```diff
File : staking/LockingMultiRewards.sol

// Define a struct to hold all necessary data
+ struct UserData {
+    Balances balances;
+    LockedBalance[] locks;
+    RewardLock rewardLock;
+    mapping(address => uint256) userRewardPerTokenPaid;
+    mapping(address => uint256) rewards;
+    uint256 lastLockIndex;
+ }

// Define a single mapping to store instances of the struct
+ mapping(address => UserData) private userData;

-90:    mapping(address user => Balances balances) private _balances;
-91:    mapping(address user => LockedBalance[] locks) private _userLocks;
-92:    mapping(address user => RewardLock rewardLock) private _userRewardLock;
-93:
-94:    mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
-95:    mapping(address user => mapping(address token => uint256 amount)) public rewards;
-96:    mapping(address user => uint256 index) public lastLockIndex;

```

## [G-07] Multiple accesses of the same mapping/array key/index inside `loop` should be cached(**Gas Saved: ~300 Gas per iteration**)

Caching repeated accesses to the same mapping or array key/index in smart contracts can lead to significant gas savings. In Solidity, each read operation from storage (like accessing a value in a mapping or array using a key or index) costs gas. By storing the accessed value in a local variable and reusing it within the function, you avoid multiple expensive storage read operations. This practice is particularly beneficial in loops or functions with multiple reads of the same data. Implementing this caching approach enhances efficiency and reduces transaction costs, which is crucial for optimizing smart contract performance and user experience on the blockchain.

### `locks.length` and `lastLockIndex[user]` can be cached `SAVES: 3 SLOADs per iteration`.

Since they are dependent on loop index so they cant be cached outside loop. But reading them in single iteration more than once can be more costly so it is better to cache them inside loop to avoid 3 SLOADs per iteration. And use cached value in other part of the loop instead re-reading from storage more than once inside loop.

**Note: This `locks.length` is not loop iteration length which is covered by analyzer it is compltely diffrent and loop are not running this length times**

```solidity
File : staking/LockingMultiRewards.sol

397:        function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
...
403:
404:            // Release all expired users' locks
405:            for (uint256 i; i < users.length; ) {
...
409:
410:                if (locks.length == 0) {//@audit locks.length read 1st
411:                    revert ErrNoLocks();
412:                }
...
415:
416:                // Prevents processing `lastLockIndex` out of order

417:                if (index == lastLockIndex[user] && locks.length > 1) {//@audit locks.length read 2nd time and lastLockIndex[user] read
418:                    revert ErrInvalidLockIndex();
419:                }
...
427:                uint256 lastIndex = locks.length - 1;//@audit locks.length read 3rd time
...
430:                if (lastLockIndex[user] == lastIndex) { //@audit lastLockIndex[user] read
431:                    lastLockIndex[user] = index;
432:                }

```

[LockingMultiRewards.sol#L397-L432](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397-L432)

**Recommended Mitigation Steps:**

```diff
File : staking/LockingMultiRewards.sol

397:        function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
...
403:
404:            // Release all expired users' locks
405:            for (uint256 i; i < users.length; ) {
...
+                uint256 locks_length = locks.length;
409:
-410:                if (locks.length == 0) {
+410:                if (locks_length == 0) {
411:                    revert ErrNoLocks();
412:                }
...
+                uint256 _lastLockIndex_user = lastLockIndex[user];
415:
416:                // Prevents processing `lastLockIndex` out of order
-417:                if (index == lastLockIndex[user] && locks.length > 1) {
+417:                if (index == _lastLockIndex_user && locks_length > 1) {
418:                    revert ErrInvalidLockIndex();
419:                }
...
-427:                uint256 lastIndex = locks.length - 1;
+427:                uint256 lastIndex = locks_length - 1;
...
-430:                if (lastLockIndex[user] == lastIndex) {
+430:                if (_lastLockIndex_user == lastIndex) {
431:                    lastLockIndex[user] = index;
432:                }

```

## [G-08] Use `calldata` instead of `memory` if parameter not get mutated(**Gas Saved: ~100 Gas**)

When a function with a `memory` array is called externally, the `abi.decode()` step has to use a for-loop to copy each index of the `calldata` to the `memory` index. Each iteration of this for-loop costs at least 60 gas (i.e. 60 \* `<mem_array>.length`). Using calldata directly, removes the need for such a loop in the contract code and runtime execution.

If the array is passed to an `internal` function which passes the array to another `internal` function where the array is modified and therefore `memory` is used in the `external` call, it's still more gas-efficient to use `calldata` when the external function uses modifiers, since the modifiers may prevent the `internal` functions from being called. `Structs` have the same overhead as an array of length one.

### 2 Instances

#### Instance 1

Change `address[] memory users` to calldata since it is not mutated.

```solidity
File : staking/LockingMultiRewards.sol

397:  function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {

```

[LockingMultiRewards.sol#L397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397)

**Recommended Mitigation Steps:**

```diff
File : staking/LockingMultiRewards.sol

-397:  function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
+397:  function processExpiredLocks(address[] calldata users, uint256[] calldata lockIndexes) external onlyOperators {

```

#### Instance 2

```solidity
File : blast/BlastOnboarding.sol

164:  function claimTokenYields(address[] memory tokens) external onlyOwner {

```

[BlastOnboarding.sol#L164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164)

**Recommended Mitigation Steps:**

```diff
File : blast/BlastOnboarding.sol

-164:  function claimTokenYields(address[] memory tokens) external onlyOwner {
+164:  function claimTokenYields(address[] calldata tokens) external onlyOwner {

```

## [G-09] State variables should be cached in stack variables rather than re-reading them from storage(**Gas Saved ~1800 Gas**)

The instances below point to the second+ access of a state variable within a function. Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.

### Cache `_BASE_RESERVE_` and `_QUOTE_RESERVE_` in `correctRState` function saves `4 SLOADs(~400 Gas)`

```solidity
File : mimswap/MagicLP.sol

139:    if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
140:        _RState_ = uint32(PMMPricing.RState.ONE);
141:        _BASE_TARGET_ = _BASE_RESERVE_;
142:        _QUOTE_TARGET_ = _QUOTE_RESERVE_;
143:    }
144:    if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
145:        _RState_ = uint32(PMMPricing.RState.ONE);
146:        _BASE_TARGET_ = _BASE_RESERVE_;
147:        _QUOTE_TARGET_ = _QUOTE_RESERVE_;
148:    }
```

[MagicLP.sol#L139-L148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139C1-L148C10)

**Recommended Mitigation Steps:**

```diff
File : mimswap/MagicLP.sol

+      uint112 _BASE_RESERVE = _BASE_RESERVE_;
+      uint112 _QUOTE_RESERVE = _QUOTE_RESERVE_;

-139:    if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
+139:    if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE < _BASE_TARGET_) {
140:        _RState_ = uint32(PMMPricing.RState.ONE);
-141:        _BASE_TARGET_ = _BASE_RESERVE_;
-142:        _QUOTE_TARGET_ = _QUOTE_RESERVE_;
+141:        _BASE_TARGET_ = _BASE_RESERVE;
+142:        _QUOTE_TARGET_ = _QUOTE_RESERVE;
143:    }
-144:    if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
+144:    if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE < _QUOTE_TARGET_) {
145:        _RState_ = uint32(PMMPricing.RState.ONE);
-146:        _BASE_TARGET_ = _BASE_RESERVE_;
-147:        _QUOTE_TARGET_ = _QUOTE_RESERVE_;
+146:        _BASE_TARGET_ = _BASE_RESERVE;
+147:        _QUOTE_TARGET_ = _QUOTE_RESERVE;
148:    }
```

### Cache `_QUOTE_TOKEN_` and `_BASE_TOKEN_` in `sellBase` function `saves 2 SLOADs(~200 Gas)`

```solidity
File : mimswap/MagicLP.sol

245:  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
...
262:     _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));
...
264:    emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);

```

[MagicLP.sol#L245-L264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L245C1-L264C113)

**Recommended Mitigation Steps:**

```diff
File : mimswap/MagicLP.sol

+      address _BASE_TOKEN = _BASE_TOKEN_;
+      address _QUOTE_TOKEN = _QUOTE_TOKEN_;

-245:  uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
+245:  uint256 baseBalance = _BASE_TOKEN.balanceOf(address(this));
...
-262:     _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));
+262:     _setReserve(baseBalance, _QUOTE_TOKEN.balanceOf(address(this)));
...
-264:    emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);
+264:    emit Swap(address(_BASE_TOKEN), address(_QUOTE_TOKEN), baseInput, receiveQuoteAmount, msg.sender, to);

```

### Cache `_QUOTE_TOKEN_` and `_BASE_TOKEN_` in `sellQuote` function `saves 2 SLOADs(~200 Gas)`

```solidity
File : mimswap/MagicLP.sol

268:     uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
...
285:    _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);
...
287:     emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);

```

[MagicLP.sol#L268-L287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L268C1-L287C113)

**Recommended Mitigation Steps:**

```diff
File : mimswap/MagicLP.sol

+      address _BASE_TOKEN = _BASE_TOKEN_;
+      address _QUOTE_TOKEN = _QUOTE_TOKEN_;

-268:     uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
+268:     uint256 quoteBalance = _QUOTE_TOKEN.balanceOf(address(this));
...
-285:    _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);
+285:    _setReserve(_BASE_TOKEN.balanceOf(address(this)), quoteBalance);
...
-287:     emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);
+287:     emit Swap(address(_QUOTE_TOKEN), address(_BASE_TOKEN), quoteInput, receiveBaseAmount, msg.sender, to);

```

### Cache `_BASE_TOKEN_`, `_QUOTE_TOKEN_`, `_BASE_RESERVE_` and `_QUOTE_RESERVE_` in `flashLoan` function `saves 10 SLOADs(~1000 Gas)`

```solidity
File : mimswap/MagicLP.sol

290: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
...
298:        uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
299:        uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
300:
301:        // no input -> pure loss
302:        if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
303:            revert ErrFlashLoanFailed();
304:        }
305:
306:        // sell quote case
307:        // quote input + base output
308:        if (baseBalance < _BASE_RESERVE_) {
309:            uint256 quoteInput = quoteBalance - uint256(_QUOTE_RESERVE_);
310:            (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) = querySellQuote(
311:                tx.origin,
312:                quoteInput
313:            );
314:
315:            if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {
316:                revert ErrFlashLoanFailed();
317:            }
...
325:            emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);
326:        }
...
330:        if (quoteBalance < _QUOTE_RESERVE_) {
331:            uint256 baseInput = baseBalance - uint256(_BASE_RESERVE_);
332:            (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) = querySellBase(
333:                tx.origin,
334:                baseInput
335:            );
336:
337:            if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {
338:                revert ErrFlashLoanFailed();
339:            }
...
347:            emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
348:        }

```

[MagicLP.sol#L290-L353](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290C5-L353C6)

**Recommended Mitigation Steps:**

```diff
File : mimswap/MagicLP.sol

290: function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
...
+      address _BASE_TOKEN = _BASE_TOKEN_;
+      address _QUOTE_TOKEN = _QUOTE_TOKEN_;

+      uint112 _BASE_RESERVE = _BASE_RESERVE_;
+      uint112 _QUOTE_RESERVE = _QUOTE_RESERVE_;

-298:        uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
+298:        uint256 baseBalance = _BASE_TOKEN.balanceOf(address(this));
-299:        uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
+299:        uint256 quoteBalance = _QUOTE_TOKEN.balanceOf(address(this));
300:
301:        // no input -> pure loss
-302:        if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
+302:        if (baseBalance < _BASE_RESERVE && quoteBalance < _QUOTE_RESERVE) {
303:            revert ErrFlashLoanFailed();
304:        }
305:
306:        // sell quote case
307:        // quote input + base output
-308:        if (baseBalance < _BASE_RESERVE_) {
+308:        if (baseBalance < _BASE_RESERVE) {
-309:            uint256 quoteInput = quoteBalance - uint256(_QUOTE_RESERVE_);
+309:            uint256 quoteInput = quoteBalance - uint256(_QUOTE_RESERVE);
310:            (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) = querySellQuote(
311:                tx.origin,
312:                quoteInput
313:            );
314:
-315:            if (uint256(_BASE_RESERVE_) - baseBalance > receiveBaseAmount) {
+315:            if (uint256(_BASE_RESERVE) - baseBalance > receiveBaseAmount) {
316:                revert ErrFlashLoanFailed();
317:            }
...
-325:            emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);
+325:            emit Swap(address(_QUOTE_TOKEN), address(_BASE_TOKEN), quoteInput, receiveBaseAmount, msg.sender, assetTo);
326:        }
...
-330:        if (quoteBalance < _QUOTE_RESERVE_) {
+330:        if (quoteBalance < _QUOTE_RESERVE) {
-331:            uint256 baseInput = baseBalance - uint256(_BASE_RESERVE_);
+331:            uint256 baseInput = baseBalance - uint256(_BASE_RESERVE);
332:            (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) = querySellBase(
333:                tx.origin,
334:                baseInput
335:            );
336:
-337:            if (uint256(_QUOTE_RESERVE_) - quoteBalance > receiveQuoteAmount) {
+337:            if (uint256(_QUOTE_RESERVE) - quoteBalance > receiveQuoteAmount) {
338:                revert ErrFlashLoanFailed();
339:            }
...
-347:            emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
+347:            emit Swap(address(_BASE_TOKEN), address(_QUOTE_TOKEN), baseInput, receiveQuoteAmount, msg.sender, assetTo);
348:        }

```

## [G-10] Within contract`s function call should be cached instead of re-calling the same function

Since `totalSupply()` will return same value both times when call from inside a same function 2nd time when it doesn't impact the totalSupply() returning value yet. So it is better to cache it to avoid 1 function call.

### `totalSupply()` function call can be cached

```solidity
File : mimswap/MagicLP.sol

375:  if (totalSupply() == 0) {
...
400:   shares = DecimalMath.mulFloor(totalSupply(), mintRatio);

```

[MagicLP.sol#L375](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L375), [MagicLP.sol#L400](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L400)

**Recommended Mitigation Steps:**

```diff
File : mimswap/MagicLP.sol

+     uint256 _totalSupply = totalSupply();

-375:  if (totalSupply() == 0) {
+375:  if (_totalSupply == 0) {
...

-400:   shares = DecimalMath.mulFloor(totalSupply(), mintRatio);
+400:   shares = DecimalMath.mulFloor(_totalSupply, mintRatio);
```

## [G-11] Nesting `if`-statements is cheaper than using `&&`(**Gas Saved ~24 Gas**)

Nesting if-statements avoids the stack operations of setting up and using an extra jumpdest and saves `6 gas`

### 3 Instances

#### Instance 1

```solidity
File : staking/LockingMultiRewards.sol

326:  if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {
327:         revert ErrSkimmingTooMuch();
328:     }

```

[LockingMultiRewards.sol#L326-L328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326C1-L328C10)

**Recommended Mitigation Steps:**

```diff
File : staking/LockingMultiRewards.sol

-326:  if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {
-327:         revert ErrSkimmingTooMuch();
-328:     }

+ if (tokenAddress == stakingToken) {
+    if (tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {
+        revert ErrSkimmingTooMuch();
+    }
+ }

```

#### Instance 2

```solidity
File : staking/LockingMultiRewards.sol

417:  if (index == lastLockIndex[user] && locks.length > 1) {
418:     revert ErrInvalidLockIndex();
419:     }

```

[LockingMultiRewards.sol#L417-L419](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L417C1-L419C14)

**Recommended Mitigation Steps:**

```diff
File : staking/LockingMultiRewards.sol

-417:  if (index == lastLockIndex[user] && locks.length > 1) {
-418:     revert ErrInvalidLockIndex();
-419:     }

+   if (index == lastLockIndex[user]){
+        if(locks.length > 1){
+            revert ErrInvalidLockIndex();
+          }
+     }

```

#### Instance 3

```solidity
File : mimswap/MagicLP.sol

139:    if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
140:        _RState_ = uint32(PMMPricing.RState.ONE);
141:        _BASE_TARGET_ = _BASE_RESERVE_;
142:        _QUOTE_TARGET_ = _QUOTE_RESERVE_;
143:    }
144:    if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
145:        _RState_ = uint32(PMMPricing.RState.ONE);
146:        _BASE_TARGET_ = _BASE_RESERVE_;
147:        _QUOTE_TARGET_ = _QUOTE_RESERVE_;
148:    }
```

[MagicLP.sol#L139-L148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139C1-L148C10)

**Recommended Mitigation Steps:**

```diff
File : mimswap/MagicLP.sol

-139:    if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
-140:        _RState_ = uint32(PMMPricing.RState.ONE);
-141:        _BASE_TARGET_ = _BASE_RESERVE_;
-142:        _QUOTE_TARGET_ = _QUOTE_RESERVE_;
-143:    }
+139:    if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE)) {
+           if(_BASE_RESERVE_ < _BASE_TARGET_){
+140:        _RState_ = uint32(PMMPricing.RState.ONE);
+141:        _BASE_TARGET_ = _BASE_RESERVE_;
+142:        _QUOTE_TARGET_ = _QUOTE_RESERVE_;
+143:          }
+       }
-144:    if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
-145:        _RState_ = uint32(PMMPricing.RState.ONE);
-146:        _BASE_TARGET_ = _BASE_RESERVE_;
-147:        _QUOTE_TARGET_ = _QUOTE_RESERVE_;
-148:    }
+144:    if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE)) {
+            if(_QUOTE_RESERVE_ < _QUOTE_TARGET_){
+145:        _RState_ = uint32(PMMPricing.RState.ONE);
+146:        _BASE_TARGET_ = _BASE_RESERVE_;
+147:        _QUOTE_TARGET_ = _QUOTE_RESERVE_;
+148:        }
+        }
```

## [G-12] `Switch` the order of `if` statement to fail early saves gas(**~2000 Gas** of Gcoldsload) half of the times

It is recommended to order checks from low to high gas consuming to revert early.

### 2 Instances

#### Instance 1

First if statement reads 2 state variables `lastLockIndex[user]` and `locks.length` and second reads only 1 state variable `locks[index].unlockTime` so we switch these two statements to save 1 state variable read.

```solidity
File : staking/LockingMultiRewards.sol

417:  if (index == lastLockIndex[user] && locks.length > 1) {
418:     revert ErrInvalidLockIndex();
419:     }
420:
421:  // prohibit releasing non-expired locks
422:  if (locks[index].unlockTime > block.timestamp) {
423:      revert ErrLockNotExpired();
424:  }

```

[LockingMultiRewards.sol#L417-L424](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L417-L424)

**Recommended Mitigation Steps:**

```diff
File : staking/LockingMultiRewards.sol

+     // prohibit releasing non-expired locks
+     if (locks[index].unlockTime > block.timestamp) {
+        revert ErrLockNotExpired();
+       }

417:  if (index == lastLockIndex[user] && locks.length > 1) {
418:     revert ErrInvalidLockIndex();
419:     }
420:
-421:  // prohibit releasing non-expired locks
-422:  if (locks[index].unlockTime > block.timestamp) {
-423:      revert ErrLockNotExpired();
-424:  }

```

#### Instance 2

We can place the first if statement in the last because it is reading `_INITIALIZED_` state variable and no one else also `_INITIALIZED_` used after all if statements

```solidity
File : mimswap/MagicLP.sol

99:         if (_INITIALIZED_) {
100:          revert ErrInitialized();
101:         }
102:        if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
103:           revert ErrZeroAddress();
104:        }
105:        if (baseTokenAddress == quoteTokenAddress) {
106:            revert ErrBaseQuoteSame();
107:        }
108:        if (i == 0 || i > MAX_I) {
109:            revert ErrInvalidI();
110:        }
111:        if (k > MAX_K) {
112:            revert ErrInvalidK();
113:        }
114:        if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {
115:            revert ErrInvalidLPFeeRate();
116:        }

```

[MagicLP.sol#L99-L116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L99C9-L116C10)

**Recommended Mitigation Steps:**

````diff
File : mimswap/MagicLP.sol

-99:         if (_INITIALIZED_) {
-100:          revert ErrInitialized();
-101:         }
102:        if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
103:           revert ErrZeroAddress();
104:        }
105:        if (baseTokenAddress == quoteTokenAddress) {
106:            revert ErrBaseQuoteSame();
107:        }
108:        if (i == 0 || i > MAX_I) {
109:            revert ErrInvalidI();
110:        }
111:        if (k > MAX_K) {
112:            revert ErrInvalidK();
113:        }
114:        if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {
115:            revert ErrInvalidLPFeeRate();
116:        }
+99:         if (_INITIALIZED_) {
+100:          revert ErrInitialized();
+101:         }

## [G-05] Avoid emitting event on every iteration

Emitting events within a loop can cause significant gas consumption due to repeated I/O operations. Instead, accumulate changes in memory and emit a single event post-loop with aggregated data. This approach improves contract efficiency, reduces gas costs, and simplifies event tracking for event listeners.

#### Instance 1

```solidity
File : staking/LockingMultiRewards.sol

405:      for (uint256 i; i < users.length; ) {
...
434:          if (index != lastIndex) {
435:              locks[index] = locks[lastIndex];
436:              emit LogLockIndexChanged(user, lastIndex, index);
437:          }
...
447:          emit LogUnlocked(user, amount, index);
...
449:          unchecked {
450:              ++i;
451:          }
452:      }

````

[LockingMultiRewards.sol#L405-L452](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405-L452)

#### Instance 2

```solidity
File : staking/LockingMultiRewards.sol

614:   for (uint256 i; i < rewardTokens.length; ) {

636:                if (amount > 0) {
637:                    rewardToken.safeTransfer(user, amount);
638:                    emit LogRewardPaid(user, rewardToken, amount);
639:                    }

651:        emit LogRewardLocked(user, rewardToken, rewardAmount);

653:        unchecked {
654:            ++i;
655:        }
656:    }

```

[LockingMultiRewards.sol#L614-L656](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614-656)

## [G-13] Refactor `_getRewards` function to save `1 SLOAD` by caching function call

Cache n`extEpoch()` function call and use it for emitting event instead of `_rewardLock.unlockTime` saves 1 SLOAD.

```solidity
File : staking/LockingMultiRewards.sol

609:   if (expired) {
610:       _rewardLock.unlockTime = nextEpoch();
611:       emit LogRewardLockCreated(user, _rewardLock.unlockTime);
612:   }

```

[LockingMultiRewards.sol#L609-L612](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L609-L612)

**Recommended Mitigation Steps:**

```diff
File : staking/LockingMultiRewards.sol

609:   if (expired) {
+        uint256 _nextEpoch = nextEpoch();
-610:       _rewardLock.unlockTime = nextEpoch();
-611:       emit LogRewardLockCreated(user, _rewardLock.unlockTime);
+610:       _rewardLock.unlockTime = _nextEpoch;
+611:       emit LogRewardLockCreated(user, _nextEpoch);
612:   }

```

## [G-14] Cache calculations instead of recalculating saves checked subtraction and checked multiplication(**Gas Saved ~300 Gas**)

#### Cache `idelta * V1` and `DecimalMath.ONE - k` saves checked multiplication and checked subtraction. It can save upto `~150 GAS`

```solidity
File : mimswap/libraries/Math.sol

155:    } else if ((idelta * V1) / idelta == V1) {
156:      temp = (idelta * V1) / (V0 * V0);
...
184:   uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
185:   squareRoot = sqrt((bAbs * bAbs) + squareRoot); // sqrt(b*b+4(1-k)kQ0*Q0)
186:
187:        // final res
188:    uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
```

[Math.sol#L155-L156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L155C1-L156C50), [Math.sol#L184-L188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184C1-L188C67)

**Recommended Mitigation Steps:**

```diff
File : mimswap/libraries/Math.sol

+       uint256 ideltaxV1 = idelta * V1;
+       uint256 DecimalMath_k = DecimalMath.ONE - k;

-155:    } else if ((idelta * V1) / idelta == V1) {
-156:      temp = (idelta * V1) / (V0 * V0);
+155:    } else if ((ideltaxV1) / idelta == V1) {
+156:      temp = (ideltaxV1) / (V0 * V0);
...
-184:   uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
+184:   uint256 squareRoot = DecimalMath.mulFloor((DecimalMath_k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
185:   squareRoot = sqrt((bAbs * bAbs) + squareRoot); // sqrt(b*b+4(1-k)kQ0*Q0)
186:
187:        // final res
-188:    uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
+188:    uint256 denominator = (DecimalMath_k) * 2; // 2(1-k)
```

## [G-15] Do not cache external call in stack variable if stack variable used only once

#### No need to cache `IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount` and `IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount` since they are used only once.

```solidity
File : mimswap/periphery/Router.sol

515:    uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;
516:    uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;
517:
518:    baseInAmount = baseBalance - baseReserve;
519:    quoteInAmount = quoteBalance - quoteReserve;

```

[Router.sol#L515-L519](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L515C1-L519C53)

**Recommended Mitigation Steps:**

```diff
File : mimswap/periphery/Router.sol

-515:    uint256 baseBalance = IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount;
-516:    uint256 quoteBalance = IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount;
517:
-518:    baseInAmount = baseBalance - baseReserve;
-519:    quoteInAmount = quoteBalance - quoteReserve;
+518:    baseInAmount = (IMagicLP(lp)._BASE_TOKEN_().balanceOf(address(lp)) + baseInAmount) - baseReserve;
+519:    quoteInAmount = (IMagicLP(lp)._QUOTE_TOKEN_().balanceOf(address(lp)) + quoteInAmount) - quoteReserve;

```
