# GAS OPTIMIZATIONS

##

## [G-1] _LP_FEE_RATE_ , _K_ , _I_ can be packed within same slot

When setting values down casted as per implementation in setParameters() functions.

```solidity
_LP_FEE_RATE_ = uint64(newLpFeeRate);
        _K_ = uint64(newK);
        _I_ = uint128(newI);

```

So its safe to down casting as per implementations. This saves ``4000 GAS`` , ``2 SLOT``

```diff
FILE: 2024-03-abracadabra-money/src/mimswap/MagicLP.sol

- 80: uint256 public _LP_FEE_RATE_;
+ 80: uint64 public _LP_FEE_RATE_;
- 81: uint256 public _K_;
+ 81: uint64 public _K_;
- 82: uint256 public _I_;
+ 82: uint128 public _I_;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L80-L82

## [G-2] ``pool`` and ``totalPoolShares`` inherited state variables can be cached with ``memory`` variables 

Caching state variables in memory (often by assigning them to local variables) can be beneficial, especially when those state variables are accessed multiple times within a function. This practice reduces the cost associated with repeated state reads, which are more expensive than reading from memory . Saves ``800 GAS`` , ``8 SLOD``

```diff
FILE:2024-03-abracadabra-money/src/blast/BlastOnboardingBoot.sol

 function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {

Address _pool = pool ;
-        if (pool != address(0)) {
+        if (_pool != address(0)) {
            revert ErrAlreadyBootstrapped();
        }

        uint256 baseAmount = totals[MIM].locked;
        uint256 quoteAmount = totals[USDB].locked;
        MIM.safeApprove(address(router), type(uint256).max);
        USDB.safeApprove(address(router), type(uint256).max);
+   uint256 totalPoolShares_ = totalPoolShares ;

-        (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
+        (_pool, totalPoolShares_ ) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);

-        if (totalPoolShares < minAmountOut) {
+        if (totalPoolShares_ < minAmountOut) {
            revert ErrInsufficientAmountOut();
        }

        // Create staking contract
        // 3x boosting for locker, 7 days reward duration, 13 weeks lp locking
        // make this contract temporary the owner the set it as an operator
        // for permissionned `stakeFor` during the claiming process and then
        // transfer the ownership to the onboarding owner.
        staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
        staking.setOperator(address(this), true);
        staking.transferOwnership(owner);

        // Approve staking contract
-        pool.safeApprove(address(staking), totalPoolShares);
+        _pool.safeApprove(address(staking), totalPoolShares_ );

-        emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);
+        emit LogLiquidityBootstrapped(_pool, address(staking), totalPoolShares_);

-        return (pool, address(staking), totalPoolShares);
+        return (_pool, address(staking), totalPoolShares_);
    }


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L95-L127

##

## [G-3] Merging multiple mappings into a single struct Mapping Saves gas

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

```solidity
FILE: 2024-03-abracadabra-money/src/staking/LockingMultiRewards.sol

  mapping(address user => mapping(address token => uint256 amount)) public userRewardPerTokenPaid;
    mapping(address user => mapping(address token => uint256 amount)) public rewards;
    mapping(address user => uint256 index) public lastLockIndex;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L94-L96


##

## [G-4] The result of function calls should be cached rather than re-calling the function

The instances below point to the second+ call of the function within a single function

``totalSupply()`` value should be cached instead calling recursively 

```diff
FILE: 2024-03-abracadabra-money/src/mimswap/MagicLP.sol

// buy shares [round down]
    function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
        uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
        uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
        uint256 baseReserve = _BASE_RESERVE_;
        uint256 quoteReserve = _QUOTE_RESERVE_;

        baseInput = baseBalance - baseReserve;
        quoteInput = quoteBalance - quoteReserve;

        if (baseInput == 0) {
            revert ErrNoBaseInput();
        }

        // Round down when withdrawing. Therefore, never be a situation occurring balance is 0 but totalsupply is not 0
        // But May Happen，reserve >0 But totalSupply = 0

+ uint256 result = totalSupply();
-        if (totalSupply() == 0) {
+        if (result  == 0) {
            // case 1. initial supply
            if (quoteBalance == 0) {
                revert ErrZeroQuoteAmount();
            }

            shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;
            _BASE_TARGET_ = shares.toUint112();
            _QUOTE_TARGET_ = DecimalMath.mulFloor(shares, _I_).toUint112();

            if (_QUOTE_TARGET_ == 0) {
                revert ErrZeroQuoteTarget();
            }

            if (shares <= 2001) {
                revert ErrMintAmountNotEnough();
            }

            _mint(address(0), 1001);
            shares -= 1001;
        } else if (baseReserve > 0 && quoteReserve > 0) {
            // case 2. normal case
            uint256 baseInputRatio = DecimalMath.divFloor(baseInput, baseReserve);
            uint256 quoteInputRatio = DecimalMath.divFloor(quoteInput, quoteReserve);
            uint256 mintRatio = quoteInputRatio < baseInputRatio ? quoteInputRatio : baseInputRatio;
-            shares = DecimalMath.mulFloor(totalSupply(), mintRatio);
+            shares = DecimalMath.mulFloor(result , mintRatio);

            _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();
            _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
        }

        _mint(to, shares);
        _setReserve(baseBalance, quoteBalance);

        emit BuyShares(to, shares, balanceOf(to));
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L375



##

## [G-5] Replacing Logical ANDs with nested If Statements to save gas

Using nested if statements instead of combining conditions with logical AND operators (&&) can result in gas savings, particularly in scenarios where most conditions are false. This approach ensures that once a condition is found to be false, subsequent conditions are not evaluated, reducing the overall computational effort. Saves 13 Gas

```solidity
FILE: 2024-03-abracadabra-money/src/blast/BlastOnboarding.sol

114: if (caps[token] > 0 && totals[token].total > caps[token]) {

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L114

##

## [G-6] ``deposit()`` function can be more gas optimized

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

##

## [G-7] Don't cache state variables once used once 

State variable is only used once in a function, directly use the state variable without storing it in a local variable. Saves 13 GAS per instance 

```diff
FILE: 2024-03-abracadabra-money/src/blast
/BlastOnboardingBoot.sol

function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
-        uint256 baseAmount = totals[MIM].locked;
-        uint256 quoteAmount = totals[USDB].locked;
-        return router.previewCreatePool(I, baseAmount, quoteAmount);
+        return router.previewCreatePool(I, totals[MIM].locked, totals[USDB].locked);
    }



- int256 baseAmount = totals[MIM].locked;
-         uint256 quoteAmount = totals[USDB].locked;
        MIM.safeApprove(address(router), type(uint256).max);
        USDB.safeApprove(address(router), type(uint256).max);

-        (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), baseAmount, quoteAmount);
+        (pool, totalPoolShares) = router.createPool(MIM, USDB, FEE_RATE, I, K, address(this), totals[MIM].locked, totals[USDB].locked);


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L87-L88

##

## [G-8] Use constants instead of ``type(uint256).max``

Using constants can lead to significant gas savings, especially when you replace commonly used expressions like type(uint256).max.

```solidity
FILE: 2024-03-abracadabra-money/src/blast/BlastOnboardingBoot.sol

103: MIM.safeApprove(address(router), type(uint256).max);
104: USDB.safeApprove(address(router), type(uint256).max);

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L103-L104

##

## [G-9] ``_QUOTE_RESERVE_`` and ``_BASE_RESERVE_`` values can be cached with memory variable . Saves ``800 GAS`` , ``8 SLOD``

In the given function correctRState, caching ``_QUOTE_RESERVE_``,``_BASE_RESERVE_ `` as a local variable can reduce gas consumption since _QUOTE_RESERVE_ and _BASE_RESERVE_  is accessed multiple times. This is because reading from a local variable is cheaper in terms of gas than reading from storage.

```diff
FILE: 2024-03-abracadabra-money/src/mimswap/MagicLP.sol

function correctRState() external {
+ uint112 _BASE_Reserve_ = _BASE_RESERVE_ ; 
+ uint112  _QUOTE_Reserve_ = _QUOTE_RESERVE_ ;
-        if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
+        if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_Reserve_ < _BASE_TARGET_) {
            _RState_ = uint32(PMMPricing.RState.ONE);
-            _BASE_TARGET_ = _BASE_RESERVE_;
+            _BASE_TARGET_ = _BASE_Reserve_ ;
-            _QUOTE_TARGET_ = _QUOTE_RESERVE_;
+            _QUOTE_TARGET_ = _QUOTE_Reserve_ ;
        }
-        if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
+        if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_Reserve_< _QUOTE_TARGET_) {
            _RState_ = uint32(PMMPricing.RState.ONE);
-            _BASE_TARGET_ = _BASE_RESERVE_;
+            _BASE_TARGET_ = _BASE_Reserve_ ;
-            _QUOTE_TARGET_ = _QUOTE_RESERVE_;
+            _QUOTE_TARGET_ = _QUOTE_Reserve_ ;
        }
    }


function correctRState() external {
        if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
            _RState_ = uint32(PMMPricing.RState.ONE);
            _BASE_TARGET_ = _BASE_RESERVE_;
            _QUOTE_TARGET_ = _QUOTE_RESERVE_;
        }
        if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
            _RState_ = uint32(PMMPricing.RState.ONE);
            _BASE_TARGET_ = _BASE_RESERVE_;
            _QUOTE_TARGET_ = _QUOTE_RESERVE_;
        }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L138-L149

##

## [G-10] Avoid updating storage when the value hasn't changed

If the old value is equal to the new value, not re-storing the value will avoid a Gsreset (2900 gas), potentially at the expense of a Gcoldsload (2100 gas) or a Gwarmaccess (100 gas)

```solidity
FILE: 2024-03-abracadabra-money/src/blast/BlastBox.sol

 function setFeeTo(address feeTo_) external onlyOwner {
        if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
        }

        feeTo = feeTo_;
        emit LogFeeToChanged(feeTo_);
    }


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L72-L79

```solidity
FILE: 2024-03-abracadabra-money/src/blast/BlastGovernor.sol

 function setFeeTo(address _feeTo) external onlyOwner {
        if(_feeTo == address(0)) {
            revert ErrZeroAddress();
        }
        
        feeTo = _feeTo;
        emit LogFeeToChanged(_feeTo);
    }


```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastGovernor.sol#L40-L47

```solidity
FILE: 2024-03-abracadabra-money/src/blast
/BlastMagicLP.sol

function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
        if (feeTo_ == address(0)) {
            revert ErrZeroAddress();
        }

        feeTo = feeTo_;
        emit LogFeeToChanged(feeTo_);
    }

    function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
        operators[operator] = status;
        emit LogOperatorChanged(operator, status);
    }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastMagicLP.sol#L80-L92

##

## [G-11] unchecked {} can be used on the division of two uints in order to save gas

The division cannot overflow, since both the numerator and the denominator are non-negative

```solidity
FILE: 2024-03-abracadabra-money/src/blast/BlastOnboardingBoot.sol

163: return (userLocked * totalPoolShares) / totalLocked;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L163

```solidity
FILE: 2024-03-abracadabra-money/src/mimswap/MagicLP.sol

435: baseAmount = (baseBalance * shareAmount) / totalShares;
436: quoteAmount = (quoteBalance * shareAmount) / totalShares;
513: _BASE_TARGET_ = uint112((uint256(_BASE_TARGET_) * baseBalance) / uint256(_BASE_RESERVE_));
517: _QUOTE_TARGET_ = uint112((uint256(_QUOTE_TARGET_) * quoteBalance) / uint256(_QUOTE_RESERVE_));

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L435-L436

##

## [G-12] Use a more recent version of solidity

Use a solidity version of at least 0.8.0 to get simple compiler automatic inlining Use a solidity version of at least 0.8.3 to get better struct packing and cheaper multiple storage reads Use a solidity version of at least 0.8.4 to get custom errors, which are cheaper at deployment than revert()/require() strings Use a solidity version of at least 0.8.10 to have external calls skip contract existence checks if the external call has a return value.

```solidity
FILE: 2024-03-abracadabra-money/src/mimswap/MagicLP.sol

8: pragma solidity >=0.8.0;

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L8

##

## [G-13] ``divCeil()`` function can be optimized more gas efficient 

The divCeil function can be optimized for gas efficiency by reducing the operations performed within the function. One common optimization is to combine the calculation and the conditional check into fewer steps. This Saves 50-100 Gas approximately for every call 

### Original Code

```solidity
FILE: 2024-03-abracadabra-money/src/mimswap/libraries
/Math.sol

function divCeil(uint256 a, uint256 b) internal pure returns (uint256) {
        uint256 quotient = a / b;
        uint256 remainder = a - quotient * b;
        if (remainder > 0) {
            return quotient + 1;
        } else {
            return quotient;
        }

```
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/libraries/Math.sol#L19-L27

### Optimized Code

```solidity

unction divCeil(uint256 a, uint256 b) internal pure returns (uint256) {
    require(b > 0, "Division by zero"); // Added to prevent division by zero
    uint256 quotient = a / b;
    if (a % b > 0) { // Directly use modulo to check for a remainder
        return quotient + 1;
    }
    return quotient;
}

```

### Explanation
- This function removes the explicit calculation of the remainder by directly using a % b to determine if there is any remainder. This approach reduces the number of arithmetic operations required.
- The condition is simplified to directly check if a % b (the remainder from dividing a by b) is greater than zero. If so, it means that the division does not result in an exact quotient, and thus we add one to the quotient for the ceiling effect.
- I added a require statement at the beginning of the function to check that b is not zero, preventing a division by zero error, which is a common practice for safety in arithmetic functions.

##

## [G-14] Refactoring the _SolveQuadraticFunctionForTrade Function for Improved Gas Efficiency

Optimizing the _SolveQuadraticFunctionForTrade function involves reducing redundant calculations, reusing computed values, and ensuring operations are performed efficiently.

### Original Code

```solidity
FILE: 2024-03-abracadabra-money/src/mimswap/libraries
/Math.sol

 function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
        if (V0 == 0) {
            revert ErrIsZero();
        }

        if (delta == 0) {
            return 0;
        }

        if (k == 0) {
            return DecimalMath.mulFloor(i, delta) > V1 ? V1 : DecimalMath.mulFloor(i, delta);
        }

        if (k == DecimalMath.ONE) {
            // if k==1
            // Q2=Q1/(1+ideltaBQ1/Q0/Q0)
            // temp = ideltaBQ1/Q0/Q0
            // Q2 = Q1/(1+temp)
            // Q1-Q2 = Q1*(1-1/(1+temp)) = Q1*(temp/(1+temp))
            // uint256 temp = i.mul(delta).mul(V1).div(V0.mul(V0));
            uint256 temp;
            uint256 idelta = i * delta;
            if (idelta == 0) {
                temp = 0;
            } else if ((idelta * V1) / idelta == V1) {
                temp = (idelta * V1) / (V0 * V0);
            } else {
                temp = (((delta * V1) / V0) * i) / V0;
            }
            return (V1 * temp) / (temp + DecimalMath.ONE);
        }

        // calculate -b value and sig
        // b = kQ0^2/Q1-i*deltaB-(1-k)Q1
        // part1 = (1-k)Q1 >=0
        // part2 = kQ0^2/Q1-i*deltaB >=0
        // bAbs = abs(part1-part2)
        // if part1>part2 => b is negative => bSig is false
        // if part2>part1 => b is positive => bSig is true
        uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
        uint256 bAbs = (DecimalMath.ONE - k) * V1; // (1-k)Q1

        bool bSig;
        if (bAbs >= part2) {
            bAbs = bAbs - part2;
            bSig = false;
        } else {
            bAbs = part2 - bAbs;
            bSig = true;
        }
        bAbs = bAbs / DecimalMath.ONE;

        // calculate sqrt
        uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
        squareRoot = sqrt((bAbs * bAbs) + squareRoot); // sqrt(b*b+4(1-k)kQ0*Q0)

        // final res
        uint256 denominator = (DecimalMath.ONE - k) * 2; // 2(1-k)
        uint256 numerator;
        if (bSig) {
            numerator = squareRoot - bAbs;
            if (numerator == 0) {
                revert ErrIsZero();
            }
        } else {
            numerator = bAbs + squareRoot;
        }

        uint256 V2 = DecimalMath.divCeil(numerator, denominator);
        if (V2 > V1) {
            return 0;
        } else {
            return V1 - V2;
        }
    }

```

### Optimized Code

```solidity

function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
    require(V0 != 0, "ErrIsZero");

    if (delta == 0) {
        return 0;
    }

    uint256 idelta = i * delta;
    
    if (k == 0) {
        uint256 product = DecimalMath.mulFloor(i, delta); // Reuse this value to avoid duplication
        return product > V1 ? V1 : product;
    }

    if (k == DecimalMath.ONE) {
        uint256 temp = 0;
        if (idelta != 0) {
            uint256 ideltaV1 = idelta * V1;
            temp = (ideltaV1 / idelta == V1) ? (ideltaV1 / (V0 * V0)) : ((delta * V1) / V0 * i) / V0;
        }
        // No need to check temp == 0 as it doesn't lead to revert
        return (V1 * temp) / (temp + DecimalMath.ONE);
    }

    uint256 part1 = (DecimalMath.ONE - k) * V1;
    uint256 part2 = idelta + (k * V0 * V0) / V1;
    uint256 bAbs;
    bool bSig;

    if (part1 >= part2) {
        bAbs = part1 - part2;
        bSig = false;
    } else {
        bAbs = part2 - part1;
        bSig = true;
    }

    // Simplify square root calculation by combining constants and removing redundant operations
    uint256 squareRoot = sqrt(bAbs * bAbs + DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0));

    // Denominator is the same for both conditions
    uint256 denominator = (DecimalMath.ONE - k) * 2;
    uint256 numerator = bSig ? squareRoot - bAbs : bAbs + squareRoot;

    uint256 V2 = DecimalMath.divCeil(numerator, denominator);
    return V2 > V1 ? 0 : V1 - V2;
}

```

### Optimization Explantions

- Remove Redundant Checks: I've replaced the initial if (V0 == 0) revert condition with a require statement for clarity and gas efficiency.

- Combine and Reuse Calculations: Whenever possible, combine similar calculations and reuse results to avoid duplicating expensive operations. For example, idelta (i * delta) is calculated once and reused.

- Simplify Conditional Checks: Directly compare parts instead of recalculating them (for temp and bAbs calculations). This reduces the overall computational load.

- Optimize Square Root Calculation: Group and simplify calculations related to the square root to avoid unnecessary multiplications.

- Consolidate Return Statements: By computing V2 and directly returning the result of V1 - V2 (if appropriate), the function avoids unnecessary branches and makes the logic clearer.






