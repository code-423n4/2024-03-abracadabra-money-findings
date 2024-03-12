## INTRODUCTION

Highlighted below are optimizations exclusively targeting state-mutating functions and view/pure functions invoked by state-mutating functions. In the discussion that follows, only runtime gas is emphasized, given its inevitable dominance over deployment gas costs throughout the protocol's lifetime.

Please be aware that some code snippets may be shortened to conserve space, and certain code snippets may include @audit tags in comments to facilitate issue explanations.

## Gas report
 - [State variables can be packed into fewer storage slot (saves 5 SLOTS: 10.2k Gas)](#g-01-state-variables-can-be-packed-into-fewer-storage-slot-saves-5-slots-102k-gas)
- [Cache calculations in loop to avoid re-calculating on each iteration](#g-02-cache-calculations-in-loop-to-avoid-re-calculating-on-each-iteration)
- [Move lesser gas costing require checks to the top](#g-03-move-lesser-gas-costing-require-checks-to-the-top)
- [Check amount for zero before mint/burn](#g-04-check-amount-for-zero-before-mintburn)
- [Storing similar computations to reduce the number of operations](#g-05-storing-similar-computations-to-reduce-the-number-of-operations)
- [State variables should be cached in stack variables rather than re-reading them from storage](#g-06-state-variables-should-be-cached-in-stack-variables-rather-than-re-reading-them-from-storage)
- [Do not cache global variable](#g-07-do-not-cache-global-variable)
- [Cache array length in for loop](#g-08-cache-array-length-in-for-loop)
- [Storage variables should be used in place of state variables rather than re-reading them from storage](#g-09-storage-variables-should-be-used-in-place-of-state-variables-rather-than-re-reading-them-from-storage)
- [Multiple accesses of a mapping/array should use a local variable cache](#g-10-multiple-accesses-of-a-mappingarray-should-use-a-local-variable-cache)
## [G-01] State variables can be packed into fewer storage slot (saves 5 SLOTS: 10.2k Gas)

### Pack the following by reducing their size (saves 2.1k Gas)

### Details

### Proof of Code
- [BlastOnboardingBoot.sol#L28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L28)
```solidity
File: src/blast/BlastOnboardingBoot.sol
23: contract BlastOnboardingBootDataV1 is BlastOnboardingData {
    address public pool;
    Router public router;
    IFactory public factory;
    uint256 public totalPoolShares;
    bool public ready; //@audit pack
    LockingMultiRewards public staking;
    mapping(address user => bool claimed) public claimed;
}
```
### Optimized code:

```diff
diff --git a/src/blast/BlastOnboardingBoot.sol b/src/blast/BlastOnboardingBoot.sol
index f9dda06..02ba1f2 100644
--- a/src/blast/BlastOnboardingBoot.sol
+++ b/src/blast/BlastOnboardingBoot.sol
@@ -22,10 +22,10 @@ uint256 constant MIM_TO_MIN = I;
 // adding new storage variables.
 contract BlastOnboardingBootDataV1 is BlastOnboardingData {
     address public pool;
+    bool public ready;
     Router public router;
     IFactory public factory;
     uint256 public totalPoolShares;
-    bool public ready;
     LockingMultiRewards public staking;
     mapping(address user => bool claimed) public claimed;
 }
```
## [G-02] Cache calculations in loop to avoid re-calculating on each iteration

In `BlastOnboarding.sol:claimTokenYields)` : `token[i]` we can cache once and use multiple times. Instead of repeatedly calling _newFees[i] in the loop, you can calculate it once and use the result.

### Details

### Proof of Code
- [BlastOnboarding.sol#L164C3-L173C6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164C3-L173C6)
```solidity
File: src/blast/BlastOnboarding.sol
164: function claimTokenYields(address[] memory tokens) external onlyOwner {
        for (uint256 i = 0; i < tokens.length; i++) { //@audit cache token[i]
            if (!supportedTokens[tokens[i]]) {
                revert ErrUnsupportedToken();
            }
            if (registry.nativeYieldTokens(tokens[i])) {
                BlastYields.claimAllTokenYields(tokens[i], feeTo);
            }
        }
    }
```
### Optimized code:

```diff
diff --git a/src/blast/BlastOnboarding.sol b/src/blast/BlastOnboarding.sol
index cd2bb96..817e46d 100644
--- a/src/blast/BlastOnboarding.sol
+++ b/src/blast/BlastOnboarding.sol
@@ -162,12 +162,13 @@ contract BlastOnboarding is BlastOnboardingData, Proxy {
     }
 
     function claimTokenYields(address[] memory tokens) external onlyOwner {
-        for (uint256 i = 0; i < tokens.length; i++) {
-            if (!supportedTokens[tokens[i]]) {
+        for (uint256 i = 0; i < tokens.length; i++) {
+            address _tokens = tokens[i];
+            if (!supportedTokens[_tokens]) {
                 revert ErrUnsupportedToken();
             }
-            if (registry.nativeYieldTokens(tokens[i])) {
-                BlastYields.claimAllTokenYields(tokens[i], feeTo);
+            if (registry.nativeYieldTokens(_tokens)) {
+                BlastYields.claimAllTokenYields(_tokens, feeTo);
             }
         }
     }
```
### Details

### Proof of Code
- [LockingMultiRewards.sol#L544C5-L553C6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L544C5-L553C6)
```solidity
File: src/staking/LockingMultiRewards.sol
544:   function _updateRewards() internal {
        uint256 totalSupply_ = totalSupply();

        for (uint256 i; i < rewardTokens.length; ) {
            _updateRewardsGlobal(rewardTokens[i], totalSupply_); //@audit cache   address token = rewardTokens[i];
            unchecked {
                ++i;
            }
        }
    }
```
### Optimized code:

```diff
diff --git a/src/staking/LockingMultiRewards.sol b/src/staking/LockingMultiRewards.sol
index 55d6403..a8a6394 100644
--- a/src/staking/LockingMultiRewards.sol
+++ b/src/staking/LockingMultiRewards.sol
@@ -545,7 +545,8 @@ contract LockingMultiRewards is OperatableV2, Pausable {
         uint256 totalSupply_ = totalSupply();
 
         for (uint256 i; i < rewardTokens.length; ) {
-            _updateRewardsGlobal(rewardTokens[i], totalSupply_);
+            address _rewardPerToken = rewardTokens[i];
+            _updateRewardsGlobal(_rewardToken, totalSupply_);
             unchecked {
                 ++i;
             }
```
## [G-03] Move lesser gas costing require checks to the top
Require() or revert() statements that check input arguments or cost lesser gas should be at the top of the function. Checks that involve constants should come before checks that involve state variables, function calls, and calculations. By doing these checks first, the function is able to revert before wasting alot of gas in a function that may ultimately revert in the unhappy case.

### Details
In `MainHelper.sol._checkLiquidatorNft`: This function check liquidator which check against input argument which is cheaper to check. we revert this condition early.In a result we can save gas through avoiding critical check which involve external call and state read.

### Proof of Code
- [MagicLP.sol#L90C1-L117C1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L90C1-L117C1)
```solidity
File: src/mimswap/MagicLP.sol
91: function init(
        address baseTokenAddress,
        address quoteTokenAddress,
        uint256 lpFeeRate,
        address mtFeeRateModel,
        uint256 i,
        uint256 k
    ) external {
        if (_INITIALIZED_) {//@audit check at last
            revert ErrInitialized();
        }
        if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
            revert ErrZeroAddress();
        }
        if (baseTokenAddress == quoteTokenAddress) {
            revert ErrBaseQuoteSame();
        }
        if (i == 0 || i > MAX_I) {
            revert ErrInvalidI();
        }
        if (k > MAX_K) {
            revert ErrInvalidK();
        }
        if (lpFeeRate < MIN_LP_FEE_RATE || lpFeeRate > MAX_LP_FEE_RATE) {
            revert ErrInvalidLPFeeRate();
        }

        _INITIALIZED_ = true;
        _BASE_TOKEN_ = baseTokenAddress;
        _QUOTE_TOKEN_ = quoteTokenAddress;
        _I_ = i;
        _K_ = k;
        _LP_FEE_RATE_ = lpFeeRate;
        _MT_FEE_RATE_MODEL_ = IFeeRateModel(mtFeeRateModel);
        _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);

        _afterInitialized();
    }
```
### Optimized code:

```diff
diff --git a/src/mimswap/MagicLP.sol b/src/mimswap/MagicLP.sol
index 3d19de4..f8c60f1 100644
--- a/src/mimswap/MagicLP.sol
+++ b/src/mimswap/MagicLP.sol
@@ -96,15 +96,15 @@ contract MagicLP is ERC20, ReentrancyGuard, Owned {
         uint256 i,
         uint256 k
     ) external {
-        if (_INITIALIZED_) {
-            revert ErrInitialized();
-        }
         if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {
             revert ErrZeroAddress();
         }
         if (baseTokenAddress == quoteTokenAddress) {
             revert ErrBaseQuoteSame();
         }
+        if (_INITIALIZED_) {
+            revert ErrInitialized();
+        }
         if (i == 0 || i > MAX_I) {
             revert ErrInvalidI();
         }
```
### Details
In `MainHelper.sol._checkLiquidatorNft`: This function check liquidator which check against input argument which is cheaper to check. we revert this condition early.In a result we can save gas through avoiding critical check which involve external call and state read.
### Proof of Code
- [MagicLP.sol#L434C1-L444C1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L434C1-L444C1)
```solidity
File: src/mimswap/MagicLP.sol
435:  baseAmount = (baseBalance * shareAmount) / totalShares;
        quoteAmount = (quoteBalance * shareAmount) / totalShares;

        _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
        _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));

        if (baseAmount < baseMinAmount || quoteAmount < quoteMinAmount) { //@audit revet first
            revert ErrWithdrawNotEnough();
        }

```
### Optimized code:

```diff
diff --git a/src/mimswap/MagicLP.sol b/src/mimswap/MagicLP.sol
index 3d19de4..628db58 100644
--- a/src/mimswap/MagicLP.sol
+++ b/src/mimswap/MagicLP.sol
@@ -435,13 +435,15 @@ contract MagicLP is ERC20, ReentrancyGuard, Owned {
         baseAmount = (baseBalance * shareAmount) / totalShares;
         quoteAmount = (quoteBalance * shareAmount) / totalShares;
 
-        _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
-        _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
-
         if (baseAmount < baseMinAmount || quoteAmount < quoteMinAmount) {
             revert ErrWithdrawNotEnough();
         }
 
+
+        _BASE_TARGET_ = uint112(uint256(_BASE_TARGET_) - (uint256(_BASE_TARGET_) * shareAmount).divCeil(totalShares));
+        _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
+
+        
         _burn(msg.sender, shareAmount);
         _transferBaseOut(to, baseAmount);
         _transferQuoteOut(to, quoteAmount);
```
### [G-04] Check amount for zero before mint/burn

### Details
0 amount burning and minting doesn't have any effect but just wastes gas when 0 value passed by mistake in mint/burn. Openzeppelin(used here) mint/burn will not revert when 0 amount passed. So it is better to revert early when amount is 0 in mint/burn rather than wasting more gas in 0 value minting/burning.
### Proof of Code
- [MagicLP.sol#L593C3-L599C6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L593C3-L599C6)
```solidity
File: src/mimswap/MagicLP.sol
593:  function _mint(address to, uint256 amount) internal override {
        if (amount <= 1000) {
            revert ErrMintAmountNotEnough();
        }

@>        super._mint(to, amount); //@audit check zero address
    }

```
### Optimized code:

```diff
593:  function _mint(address to, uint256 amount) internal override {
        if (amount <= 1000) {
            revert ErrMintAmountNotEnough();
        }
+       if(amonut>0){
        super._mint(to, amount);
+       }
    }
```
## [G-05] Storing similar computations to reduce the number of operations.

### Details
Combine similar computations to reduce the number of operations.The calculation involving decimals() is repeated. Consider storing this value in a variable. 

### Proof of Code
- [Router.sol#L53C1-L71C6](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L53C1-L71C6)
```solidity
File: src/mimswap/periphery/Router.sol
54:   function createPool(
        address baseToken,
        address quoteToken,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 baseInAmount,
        uint256 quoteInAmount
    ) external returns (address clone, uint256 shares) {
@>        _validateDecimals(IERC20Metadata(baseToken).decimals(), IERC20Metadata(quoteToken).decimals()); //@audit cache decimals

        clone = IFactory(factory).create(baseToken, quoteToken, lpFeeRate, i, k);

        baseToken.safeTransferFrom(msg.sender, clone, baseInAmount);
        quoteToken.safeTransferFrom(msg.sender, clone, quoteInAmount);
        (shares, , ) = IMagicLP(clone).buyShares(to);
    }
```
### Optimized code:

```diff
diff --git a/src/mimswap/periphery/Router.sol b/src/mimswap/periphery/Router.sol
index a767f56..f4a1ccd 100644
--- a/src/mimswap/periphery/Router.sol
+++ b/src/mimswap/periphery/Router.sol
@@ -61,7 +61,8 @@ contract Router {
         uint256 baseInAmount,
         uint256 quoteInAmount
     ) external returns (address clone, uint256 shares) {
-        _validateDecimals(IERC20Metadata(baseToken).decimals(), IERC20Metadata(quoteToken).decimals());
+        uint256 _decimals = decimals(); 
+        _validateDecimals(IERC20Metadata(baseToken)._decimals, IERC20Metadata(quoteToken)._decimals);
 
         clone = IFactory(factory).create(baseToken, quoteToken, lpFeeRate, i, k);
```
### Details

### Proof of Code
- [Factory.sol#L80C1-L91C1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L80C1-L91C1)
```solidity
File: src/mimswap/periphery/Factory.sol
73: function createPoolETH(
        address token,
        bool useTokenAsQuote,
        uint256 lpFeeRate,
        uint256 i,
        uint256 k,
        address to,
        uint256 tokenInAmount
    ) external payable returns (address clone, uint256 shares) {
        if (useTokenAsQuote) {
@>            _validateDecimals(18, IERC20Metadata(token).decimals()); //@audit cache decimals
        } else {
            _validateDecimals(IERC20Metadata(token).decimals(), 18);
        }
```
### Optimized code:

```diff
diff --git a/src/mimswap/periphery/Factory.sol b/src/mimswap/periphery/Factory.sol
index 978bdf6..d31927a 100644
--- a/src/mimswap/periphery/Factory.sol
+++ b/src/mimswap/periphery/Factory.sol
@@ -79,10 +80,11 @@ contract Router {
         address to,
         uint256 tokenInAmount
     ) external payable returns (address clone, uint256 shares) {
+        uint256 _decimals = decimals(); 
         if (useTokenAsQuote) {
-            _validateDecimals(18, IERC20Metadata(token).decimals());
+            _validateDecimals(18, IERC20Metadata(token)._decimals);
         } else {
-            _validateDecimals(IERC20Metadata(token).decimals(), 18);
+            _validateDecimals(IERC20Metadata(token)._decimals, 18);
         }
```
## [G-06] State variables should be cached in stack variables rather than re-reading them from storage

### Details
The instances below point to the second+ access of a state variable within a function. Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.
- [Factory.sol#L80C1-L91C1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L80C1-L91C1)
### Optimized code:

```diff
diff --git a/src/mimswap/periphery/Factory.sol b/src/mimswap/periphery/Factory.sol
index 978bdf6..511f14b 100644
--- a/src/mimswap/periphery/Factory.sol
+++ b/src/mimswap/periphery/Factory.sol
@@ -79,13 +79,14 @@ contract Factory is Owned {
     }
 
     function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
        address creator = tx.origin;
 
         bytes32 salt = _computeSalt(creator, baseToken_, quoteToken_, lpFeeRate_, i_, k_);
         clone = LibClone.cloneDeterministic(address(implementation), salt);
-        IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
+        _maintainerFeeRateModel = maintainerFeeRateModel;
+        IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(_maintainerFeeRateModel), i_, k_); //@audit cache maintainerFeeRateModel = maintainerFeeRateModel_;
 
-        emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
+        emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, _maintainerFeeRateModel, i_, k_);
         _addPool(creator, baseToken_, quoteToken_, clone);
     }
```

## [G-07] Do not cache global variable

### Details
Use global value instead of caching in local variable.Caching global variable is more likely consume more gas.
### Proof of Code
- [Factory.sol#L80C1-L91C1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L80C1-L91C1)
```diff
File:
81: function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
-        address creator = tx.origin; //@audit do not cache global variable

-        bytes32 salt = _computeSalt(creator, baseToken_, quoteToken_, lpFeeRate_, i_, k_);
+        bytes32 salt = _computeSalt(tx.origin, baseToken_, quoteToken_, lpFeeRate_, i_, k_);
        clone = LibClone.cloneDeterministic(address(implementation), salt);
        _maintainerFeeRateModel = maintainerFeeRateModel;
        IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(_maintainerFeeRateModel), i_, k_); 

-        emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, _maintainerFeeRateModel, i_, k_);
-        _addPool(creator, baseToken_, quoteToken_, clone);
+        emit LogCreated(clone, baseToken_, quoteToken_, tx.origin, lpFeeRate_, _maintainerFeeRateModel, i_, k_);
+        _addPool(tx.origin, baseToken_, quoteToken_, clone);
    }
```
## [G-08] Cache array length in for loop

### Details
If not cached, the solidity compiler will always read the length of the array during each iteration. That is, if it is a storage array, this is an extra sload operation (100 additional extra gas for each iteration except for the first) and if it is a memory array, this is an extra mload operation (3 additional gas for each iteration except for the first).

### Proof of Code
- [LockingMultiRewards.sol#L398C2-L420C1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L398C2-L420C1)
```solidity
File: src/staking/LockingMultiRewards.sol
405:  for (uint256 i; i < users.length; ) {
            address user = users[i];
            Balances storage bal = _balances[user];
            LockedBalance[] storage locks = _userLocks[user];

@>            if (locks.length == 0) {
                revert ErrNoLocks();
            }

            uint256 index = lockIndexes[i];

            // Prevents processing `lastLockIndex` out of order
@>            if (index == lastLockIndex[user] && locks.length > 1) { //@audit cache lastLockIndex[user]
                revert ErrInvalidLockIndex();
            }

            // prohibit releasing non-expired locks
            if (locks[index].unlockTime > block.timestamp) {
                revert ErrLockNotExpired();
            }

            uint256 amount = locks[index].amount;
@>            uint256 lastIndex = locks.length - 1;

            /// Last lock index changed place with the one we just swapped.
            if (lastLockIndex[user] == lastIndex) {
                lastLockIndex[user] = index;
            }
```
### Optimized code:

```diff
diff --git a/src/staking/LockingMultiRewards.sol b/src/staking/LockingMultiRewards.sol
index 55d6403..02ea517 100644
--- a/src/staking/LockingMultiRewards.sol
+++ b/src/staking/LockingMultiRewards.sol
@@ -406,25 +406,25 @@ contract LockingMultiRewards is OperatableV2, Pausable {
             address user = users[i];
             // Prevents processing `lastLockIndex` out of order
-            if (index == lastLockIndex[user] && locks.length > 1) {
+            if (index == lastLockIndex[user] && locksLength > 1) { //@audit cache lastLockIndex[user]
                 revert ErrInvalidLockIndex();
             }
 
             // prohibit releasing non-expired locks
-            if (locks[index].unlockTime > block.timestamp) {
+            if (locks[index].unlockTime > block.timestamp) {
                 revert ErrLockNotExpired();
             }
 
             uint256 amount = locks[index].amount;
-            uint256 lastIndex = locks.length - 1;
+            uint256 lastIndex = locksLength - 1;
 
             /// Last lock index changed place with the one we just swapped.
             if (lastLockIndex[user] == lastIndex) {
```
## [G-09] Storage variables should be used in place of state variables rather than re-reading them from storage

### Details
The instances below point to the second+ access of a state variable within a function. Caching of a state variable replaces each Gwarmaccess (100 gas) with a much cheaper stack read. Other less obvious fixes/optimizations include having local memory caches of state variable structs, or having local caches of state variable contracts/addresses.
### Proof of Code
- [LockingMultiRewards.sol#L361C3-L379C39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361C3-L379C39)
```solidity
File: src/staking/LockingMultiRewards.sol
361:  function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
@>        if (!_rewardData[rewardToken].exists) { //@audit use cache value
            revert ErrInvalidTokenAddress();
        }

        _updateRewards();
        rewardToken.safeTransferFrom(msg.sender, address(this), amount);

        Reward storage reward = _rewardData[rewardToken];
```
### Optimized code:

```diff
diff --git a/src/staking/LockingMultiRewards.sol b/src/staking/LockingMultiRewards.sol
index 55d6403..30ccf1f 100644
--- a/src/staking/LockingMultiRewards.sol
+++ b/src/staking/LockingMultiRewards.sol
@@ -359,14 +359,15 @@ contract LockingMultiRewards is OperatableV2, Pausable {
     /// 2 days will revert the transaction.
     /// To ignore this check, set `minRemainingTime` to 0.
     function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
-        if (!_rewardData[rewardToken].exists) {
+         Reward storage reward = _rewardData[rewardToken];
+        if (!reward.exists) {
             revert ErrInvalidTokenAddress();
         }
 
         _updateRewards();
         rewardToken.safeTransferFrom(msg.sender, address(this), amount);
 
-        Reward storage reward = _rewardData[rewardToken];
+       
```
## [G-10] Multiple accesses of a mapping/array should use a local variable cache

### Details
Caching a mapping's value in a local storage or calldata variable when the value is accessed multiple times saves ~42 gas per access due to not having to perform the same offset calculation every time. Help the Optimizer by saving a storage variable's reference instead of repeatedly fetching it

To help the optimizer,declare a storage type variable and use it instead of repeatedly fetching the reference in a map or an array. As an example, instead of repeatedly calling someMap[someIndex], save its reference like this: SomeStruct storage someStruct = someMap[someIndex] and use it.

### Proof of Code
- [LockingMultiRewards.sol#L277C3-L287C1](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277C3-L287C1)
```solidity
File: src/staking/LockingMultiRewards.sol
277: function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
        if (totalSupply_ == 0) {
@>            return _rewardData[rewardToken].rewardPerTokenStored;
        }

        uint256 timeElapsed = lastTimeRewardApplicable_ - _rewardData[rewardToken].lastUpdateTime;
        uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_; //@audit cache  Reward storage reward = _rewardData[rewardToken];

        return _rewardData[rewardToken].rewardPerTokenStored + pendingRewardsPerToken;
    }
``` 
### Optimized code:

```diff
diff --git a/src/staking/LockingMultiRewards.sol b/src/staking/LockingMultiRewards.sol
index 55d6403..00067b2 100644
--- a/src/staking/LockingMultiRewards.sol
+++ b/src/staking/LockingMultiRewards.sol
@@ -275,14 +275,15 @@ contract LockingMultiRewards is OperatableV2, Pausable {
     }
 
     function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
+         Reward storage reward = _rewardData[rewardToken];
         if (totalSupply_ == 0) {
-            return _rewardData[rewardToken].rewardPerTokenStored;
+            return reward.rewardPerTokenStored;
         }
 
-        uint256 timeElapsed = lastTimeRewardApplicable_ - _rewardData[rewardToken].lastUpdateTime;
-        uint256 pendingRewardsPerToken = (timeElapsed * _rewardData[rewardToken].rewardRate * 1e18) / totalSupply_;
+        uint256 timeElapsed = lastTimeRewardApplicable_ - reward.lastUpdateTime;
+        uint256 pendingRewardsPerToken = (timeElapsed * reward.rewardRate * 1e18) / totalSupply_;
 
-        return _rewardData[rewardToken].rewardPerTokenStored + pendingRewardsPerToken;
+        return reward.rewardPerTokenStored + pendingRewardsPerToken;
     }
```
### Details

### Proof of Code
- [LockingMultiRewards.sol#L528C4](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L528C4-L534C6)
```solidity
File: src/staking/LockingMultiRewards.sol
528:  function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {
        uint256 lastTimeRewardApplicable_ = lastTimeRewardApplicable(token_);
        rewardPerToken_ = _rewardPerToken(token_, lastTimeRewardApplicable_, totalSupply_);

@>        _rewardData[token_].rewardPerTokenStored = rewardPerToken_;
        _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow
    }
```
### Optimized code:

```diff
diff --git a/src/staking/LockingMultiRewards.sol b/src/staking/LockingMultiRewards.sol
index 55d6403..c6e9661 100644
--- a/src/staking/LockingMultiRewards.sol
+++ b/src/staking/LockingMultiRewards.sol
@@ -528,9 +528,9 @@ contract LockingMultiRewards is OperatableV2, Pausable {
     function _updateRewardsGlobal(address token_, uint256 totalSupply_) internal returns (uint256 rewardPerToken_) {
         uint256 lastTimeRewardApplicable_ = lastTimeRewardApplicable(token_);
         rewardPerToken_ = _rewardPerToken(token_, lastTimeRewardApplicable_, totalSupply_);
-
-        _rewardData[token_].rewardPerTokenStored = rewardPerToken_;
-        _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow
+        Reward storage reward = _rewardData[rewardToken];
+        reward.rewardPerTokenStored = rewardPerToken_; 
+        reward.lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow
     }
```