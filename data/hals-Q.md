# Abracadabra MimSwap QA Report

| ID            | Title                                                                                                                         | Severity |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------- | -------- |
| [L-01](#l-01) | `MagicLp.buyShares` mints wrong number of shares for the first buyer                                                          | Low      |
| [L-02](#l-02) | `MagicLp.buyShares` function can be DoSed when any of the reserves are empty                                                  | Low      |
| [L-03](#l-03) | `setParameters()` should check the reserves after the update                                                                  | Low      |
| [L-04](#l-04) | Incorrect TWAP calculation if any of the base or quote tokens reserves become zero                                            | Low      |
| [L-05](#l-05) | Users can be griefed when `minLockAmount` is zero                                                                             | Low      |
| [L-06](#l-06) | `LockingMultiRewards.notifyRewardAmount()` function can be invoked with zero amount of rewards                                | Low      |
| [L-07](#l-07) | `BlastPoints` library uses hardcoded addresses                                                                                | Low      |
| [L-08](#l-08) | `BlastOnboarding.withdraw()` function should allow withdrawing tokens that became unsupported                                 | Low      |
| [L-09](#l-09) | `BlastOnboarding` contract doesn't support fee-on-transfer tokens                                                             | Low      |
| [L-10](#l-10) | Unifying `LockingMultiRewards.minLockAmount` variable doesn't fit all rewards tokens                                          | Low      |
| [L-11](#l-11) | `MagicLP.setParameters()` function resets the reserves and the the targets even if the contract balances haven't been updated | Low      |
| [L-12](#l-12) | `BlastBox` contract: token yield will be lost if the registry disabled it after being enabled                                 | Low      |
| [L-13](#l-13) | Consider using OpenZeppelin's SafeCast library to prevent unexpected overflows when casting from higher to lower uint types   | Low      |
| [L-14](#l-14) | `BlastOnboardingBoot.setStaking()` function doesn't grant pool approvals on `totalPoolShares`                                 | Low      |

## [L-01] `MagicLp.buyShares` mints wrong number of shares for the first buyer <a id="l-01" ></a>

## Details

`MagicLp.buyShares` function is meant to mint the buyer LP share tokens after he transfers base and quote tokens, and to protect against the well known inflation attack that can be caused by the first depositor; when the first purchase of shares is made, an amount of 1001 is minted to the address(0) to prevent manipulating the shares minting by the first buyer:

```javascript
    function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
        //some code...
            // But May Happen，reserve >0 But totalSupply = 0
            if (totalSupply() == 0) {
                // case 1. initial supply
            //some code...
                _mint(address(0), 1001);
                shares -= 1001;
            } else if (baseReserve > 0 && quoteReserve > 0) {
                // case 2. normal case
                //some code...
            }

            _mint(to, shares);
            //some code...
        }
```

as can be noticed from the code above, when `totalSupply` of shares is zero, the amount of shares is calculated based on the amounts of base and quote tokens the user would like to buy with, and then an amount of `1001` will be deducted from his shares and transferred to `address(0)`, and the rest of the shares will be transferred to an address determined by the buyer.

But this will result in the first shares buyer having less shares than intended by 1001, while this amount should be a ghost amount that's minted to `address(0)` without affecting the shares bought by the first buyer.

## Proof of Concept

[MagicLP.buyShares function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L393-L394)

```javascript
  function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
        //some code...
            // But May Happen，reserve >0 But totalSupply = 0
            if (totalSupply() == 0) {
                // case 1. initial supply
            //some code...
                _mint(address(0), 1001);
                shares -= 1001;
            } else if (baseReserve > 0 && quoteReserve > 0) {
                // case 2. normal case
                //some code...
            }

            _mint(to, shares);
            //some code...
        }
```

## Recommendation

Update `buyShares` to mint the dust/ghost amount to the `address(0)` without affecting the shares of the first buyer:

```diff
  function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
        //some code...
            // But May Happen，reserve >0 But totalSupply = 0
            if (totalSupply() == 0) {
                // case 1. initial supply
            //some code...
                _mint(address(0), 1001);
-               shares -= 1001;
            } else if (baseReserve > 0 && quoteReserve > 0) {
                // case 2. normal case
                //some code...
            }

            _mint(to, shares);
            //some code...
        }
```

## [L-02] `MagicLp.buyShares` function can be DoSed when any of the reserves are empty <a id="l-02" ></a>

## Details

- `MagicLp` contract has `sellBase` function that enables users to sell their base tokens for a quote token in return, and it has `sellQuote` function that enables users to sell their quote tokens and get base tokens in return (from the contract reserves), where users trade their tokens with the contract tokens reserves.

- But these functions (`sellBase` & `sellQuote`) allow sellers to purchase the contract reserves without a limit, where any user can empty the base or quote reserves as there's no limit on the amount of tokens being purchased from the contract.

- So if any of the base or quote tokens reserves are empty; the `buyShares` function would revert as the amount of shares to be minted for the buyer would be zero as it will be not calculated, which will result in reverting the txn as the `_mint` function requires a minimum amount of `1001` shares to be minted, otherwise; it will revert:

  ```javascript
  function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
  //some code..
          uint256 baseReserve = _BASE_RESERVE_;
          uint256 quoteReserve = _QUOTE_RESERVE_;

      //some code..
          if (totalSupply() == 0) {
          //some code..
          } else if (baseReserve > 0 && quoteReserve > 0) {<// @audit : will not be executed if any of the reserves are empty
              // case 2. normal case
          //some code...
          }

          _mint(to, shares);
          _setReserve(baseBalance, quoteBalance);

          emit BuyShares(to, shares, balanceOf(to));
      }
  ```

  ```javascript
    function _mint(address to, uint256 amount) internal override {
        if (amount <= 1000) {
            revert ErrMintAmountNotEnough();
        }

        super._mint(to, amount);
    }
  ```

## Proof of Concept

[MagicLP.sellBase function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L244-L265)

```javascript
  function sellBase(address to) external nonReentrant returns (uint256 receiveQuoteAmount) {
        uint256 baseBalance = _BASE_TOKEN_.balanceOf(address(this));
        uint256 baseInput = baseBalance - uint256(_BASE_RESERVE_);
        uint256 mtFee;
        uint256 newBaseTarget;
        PMMPricing.RState newRState;
        (receiveQuoteAmount, mtFee, newRState, newBaseTarget) = querySellBase(tx.origin, baseInput);

        _transferQuoteOut(to, receiveQuoteAmount);
        _transferQuoteOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);

        // update TARGET
        if (_RState_ != uint32(newRState)) {
            _BASE_TARGET_ = newBaseTarget.toUint112();
            _RState_ = uint32(newRState);
            emit RChange(newRState);
        }

        _setReserve(baseBalance, _QUOTE_TOKEN_.balanceOf(address(this)));

        emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);
    }
```

[MagicLP.sellQuote function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L267-L288)

```javascript
 function sellQuote(address to) external nonReentrant returns (uint256 receiveBaseAmount) {
        uint256 quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));
        uint256 quoteInput = quoteBalance - uint256(_QUOTE_RESERVE_);
        uint256 mtFee;
        uint256 newQuoteTarget;
        PMMPricing.RState newRState;
        (receiveBaseAmount, mtFee, newRState, newQuoteTarget) = querySellQuote(tx.origin, quoteInput);

        _transferBaseOut(to, receiveBaseAmount);
        _transferBaseOut(_MT_FEE_RATE_MODEL_.maintainer(), mtFee);

        // update TARGET
        if (_RState_ != uint32(newRState)) {
            _QUOTE_TARGET_ = newQuoteTarget.toUint112();
            _RState_ = uint32(newRState);
            emit RChange(newRState);
        }

        _setReserve(_BASE_TOKEN_.balanceOf(address(this)), quoteBalance);

        emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);
    }
```

[MagicLP.buyShares function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L395-L407)

```javascript
function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
   //some code..
        uint256 baseReserve = _BASE_RESERVE_;
        uint256 quoteReserve = _QUOTE_RESERVE_;

    //some code..
        if (totalSupply() == 0) {
          //some code..
        } else if (baseReserve > 0 && quoteReserve > 0) {<// @audit : will not be executed if any of the reserves are empty
            // case 2. normal case
            uint256 baseInputRatio = DecimalMath.divFloor(baseInput, baseReserve);
            uint256 quoteInputRatio = DecimalMath.divFloor(quoteInput, quoteReserve);
            uint256 mintRatio = quoteInputRatio < baseInputRatio ? quoteInputRatio : baseInputRatio;
            shares = DecimalMath.mulFloor(totalSupply(), mintRatio);

            _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();
            _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
        }

        _mint(to, shares);
        _setReserve(baseBalance, quoteBalance);

        emit BuyShares(to, shares, balanceOf(to));
    }
```

[MagicLP.\_mint function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L593C1-L599C6)

```javascript
    function _mint(address to, uint256 amount) internal override {
        if (amount <= 1000) {
            revert ErrMintAmountNotEnough();
        }

        super._mint(to, amount);
    }
```

## Recommendation

Update `sellQuote` & `sellBase` functions to limit the purchased amounts so that the reserves wouldn't be emptied.

## [L-03] `setParameters()` should check the reserves after the update <a id="l-03" ></a>

## Details

- `Magic.setParameters` function enables the contract owner from updating vital contract parameters such as `_K_`,`_I_`, `_LP_FEE_RATE_` and the balances and reserves of base and quote tokens by resetting these reserves via `_resetTargetAndReserve()`.

- `Magic.setParameters` function takes two parameters to check the reserves against: `minBaseReserve` & `minQuoteReserve` to ensure that the result of the owner updates wouldn't result in lowering the reserves below these minimum amounts, but it was noticed that the function checks these reserves first before the update, while this check should be done after the reserves update to ensure they are not falling below the minimum inputs:

  ```javascript
  function setParameters(
          address assetTo,
          uint256 newLpFeeRate,
          uint256 newI,
          uint256 newK,
          uint256 baseOutAmount,
          uint256 quoteOutAmount,
          uint256 minBaseReserve,
          uint256 minQuoteReserve
      ) public nonReentrant onlyImplementationOwner {

          // @audit : should check the reserves after calling `_resetTargetAndReserve()`
          if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
              revert ErrReserveAmountNotEnough();
          }

          // some code...

          _transferBaseOut(assetTo, baseOutAmount);
          _transferQuoteOut(assetTo, quoteOutAmount);
          (uint256 newBaseBalance, uint256 newQuoteBalance) = _resetTargetAndReserve(); //<< @audit :this function resets the reserves and targets to be equal to the base and quote balances of the contract
          emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);
      }
  ```

## Proof of Concept

[MagicLP.setParameters function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L480C8-L482C10)

```javascript
function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner {

        if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
            revert ErrReserveAmountNotEnough();
        }

        // some code...

        _transferBaseOut(assetTo, baseOutAmount);
        _transferQuoteOut(assetTo, quoteOutAmount);
        (uint256 newBaseBalance, uint256 newQuoteBalance) = _resetTargetAndReserve();
        emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);
    }
```

[MagicLP.\_resetTargetAndReserve function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L528-L543)

```javascript
function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {
        baseBalance = _BASE_TOKEN_.balanceOf(address(this));
        quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

        if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
            revert ErrOverflow();
        }

        _BASE_RESERVE_ = uint112(baseBalance);
        _QUOTE_RESERVE_ = uint112(quoteBalance);
        _BASE_TARGET_ = uint112(baseBalance);
        _QUOTE_TARGET_ = uint112(quoteBalance);
        _RState_ = uint32(PMMPricing.RState.ONE);

        _twapUpdate();
    }
```

## Recommendation

Update `setParameters()` function to check for the minimum reserves after the update is done:

```diff
function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner {

-       if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
-           revert ErrReserveAmountNotEnough();
-       }

        // some code...

        _transferBaseOut(assetTo, baseOutAmount);
        _transferQuoteOut(assetTo, quoteOutAmount);
        (uint256 newBaseBalance, uint256 newQuoteBalance) = _resetTargetAndReserve();

+       if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
+           revert ErrReserveAmountNotEnough();
+       }

        emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);
    }
```

## [L-04] Incorrect TWAP calculation if any of the base or quote tokens reserves become zero <a id="l-04" ></a>

## Details

- `MagicLp._twapUpdate()` function calcultaes TWAP price by getting the mid price\* time elapsed from the last price update, and this function is invoked wherever the contract tokens balances or reserves are updated (in `ratioSync()`, when selling base or quote tokens, when buying shares,...):

```javascript
function _twapUpdate() internal {
        uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
        uint32 timeElapsed = blockTimestamp - _BLOCK_TIMESTAMP_LAST_;

        if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
            /// @dev It is desired and expected for this value to
            /// overflow once it has hit the max of `type.uint256`.
            unchecked {
                _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
            }
        }

        _BLOCK_TIMESTAMP_LAST_ = blockTimestamp;
    }

```

and the reason for checking that the reserves are not zeros before updating the cumulative price is to prevent division by zero when calculating the price via `getMidPrice()`.

- But there's a possiblity to empty any of the base or quote tokens reserves via `sellQuote()` or `sellBase()` functions that enable users from buying the whole contract tokens reserves (no limit on the purchased amount/reported in a separate issue), and if this is the case; then whenever `_twapUpdate()` function is called, it will not update the `_BASE_PRICE_CUMULATIVE_LAST_` **but** the `_BLOCK_TIMESTAMP_LAST_` will be updated eventhough the price is not updated, and this will result in a wrong price calculation next time the function is called sincethe time difference will be lower.

## Proof of Concept

[MagicLP.\_twapUpdate function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L545C5-L559C1)

```javascript
function _twapUpdate() internal {
        uint32 blockTimestamp = uint32(block.timestamp % 2 ** 32);
        uint32 timeElapsed = blockTimestamp - _BLOCK_TIMESTAMP_LAST_;

        if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
            /// @dev It is desired and expected for this value to
            /// overflow once it has hit the max of `type.uint256`.
            unchecked {
                _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
            }
        }

        _BLOCK_TIMESTAMP_LAST_ = blockTimestamp;
    }
```

## Recommendation

Since `_BASE_PRICE_CUMULATIVE_LAST_` is set as a public variable and can be called by any DEX at any time, I would suggest the following updates to prevent using this price in case any of the reserves are zeros:

1. Set the visibilty of `_BASE_PRICE_CUMULATIVE_LAST_` to private:

```diff
-uint256 public _BASE_PRICE_CUMULATIVE_LAST_;
+uint256 private _BASE_PRICE_CUMULATIVE_LAST_;
```

2. And add a public function to get its value **only** if the reserves are > 0 , to ensure that the price is correctly updated before using it:

```diff
+function getTWAP() public returns(uint256) {
+        require( _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0,"invlid TWAP price");
+        return  _BASE_PRICE_CUMULATIVE_LAST_;
+    }
```

## [L-05] Users can be griefed when `minLockAmount` is zero <a id="l-05" ></a>

## Details

- `LockingMultiRewards` contract has a `minLockAmount` variable that ensures that the amount locked for a user not to be less than that:

  ```javascript
      function _createLock(address user, uint256 amount) internal {
          //some code...

          // Add to current lock if it's the same unlock time or the first one
          // userLocks is sorted by unlockTime, so the last lock is the most recent one
          if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {
              // Limit the number of locks per user to avoid too much gas costs per user
              // when looping through the locks
              if (lockCount == maxLocks) {
                  revert ErrMaxUserLocksExceeded();
              }

              if (amount < minLockAmount) {
                  revert ErrLockAmountTooSmall();
              }

              _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));
              lastLockIndex[user] = lockCount;

              unchecked {
                  ++lockCount;
              }
          }
          //some code...
      }
  ```

- Knowing that the `minLockAmount` variable is not set upon deployment, but set via a separate funtion `setMinLockAmount()`, then a griefer can create a number of **locked** staking positions equals to the `maxLocks` for a victim address, with 1 wei (dust amount) for each lock via calling `stakeFor()` on behalf of the victime address (calling this function with `maxLocks` number of times in the same block so that the `_userLocks[user]` array length can't be incremented anymore until the locks expired and the contract operator calls `processExpiredLocks()` on the victim address).

**How could this harm the grifed user?**

- By knowing that the total rewards that can be claimed by the user depends heavily on his locked balance:

```javascript
    function _updateRewardsForUser(address user) internal {
        uint256 balance = balanceOf(user); //! unlocked + locked*3
        uint256 totalSupply_ = totalSupply(); //! unlocked + locked*3

        for (uint256 i; i < rewardTokens.length; ) {
            address token = rewardTokens[i];

            _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_));

            unchecked {
                ++i;
            }
        }
    }
```

where `balanceOf(user)` will be equal to the unlocked balance + `lockingBoostMultiplerInBips`\* locked balance, where the `lockingBoostMultiplerInBips` minimum value is 10_001 (from the deployment script `LockingMultiRewardsScript.s.sol` this value is set to 30_000); the locked balance considered will be amplified:

```javascript
    function balanceOf(address user) public view returns (uint256) {
        Balances storage bal = _balances[user];
        return bal.unlocked + ((bal.locked * lockingBoostMultiplerInBips) / BIPS);
    }
```

then griefing the user (when the `minLockAmount` is zero) by creating a locked staking positions with a dust value for each stake will result in reducing the rewards that could be claimed by the user within a specific unlock time.

## Proof of Concept

[LockingMultiRewards.\_createLock function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L490-L499)

```javascript
    function _createLock(address user, uint256 amount) internal {
         //some code...

        // Add to current lock if it's the same unlock time or the first one
        // userLocks is sorted by unlockTime, so the last lock is the most recent one
        if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {
            // Limit the number of locks per user to avoid too much gas costs per user
            // when looping through the locks
            if (lockCount == maxLocks) {
                revert ErrMaxUserLocksExceeded();
            }

            if (amount < minLockAmount) {
                revert ErrLockAmountTooSmall();
            }

            _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));
            lastLockIndex[user] = lockCount;

            unchecked {
                ++lockCount;
            }
        }
        //some code...
    }
```

## Recommendation

Prevent users from creating locked staking onbehalf of other users when `minLockAmount` is zero.

## [L-06] `LockingMultiRewards.notifyRewardAmount()` function can be invoked with zero amount of rewards <a id="l-06" ></a>

## Details

- `LockingMultiRewards.notifyRewardAmount` function is meant to be called by any of the operators to add an amount of whitelisted rewards tokens to be distributed to the stakers, where it will update the global reward parameters such as:

```javascript
reward.rewardRate = amount / _remainingRewardTime;
reward.lastUpdateTime = uint248(block.timestamp);
reward.periodFinish = _nextEpoch;
```

where these parameters are being used later to claculate the earned rewards for stakers.

- But this function can update these global parameters even when the amount added by the operator is zero as there's no check that the input `amount` is > 0, which will result in incorrect rewards calculation for users (as the global parameters are updated without adding an extra rewards amount).

## Proof of Concept

[LockingMultiRewards.notifyRewardAmount function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L361C5-L393C6)

```javascript
function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
        if (!_rewardData[rewardToken].exists) {
            revert ErrInvalidTokenAddress();
        }

        _updateRewards();
        rewardToken.safeTransferFrom(msg.sender, address(this), amount);

        Reward storage reward = _rewardData[rewardToken];

        uint256 _nextEpoch = nextEpoch();
        uint256 _remainingRewardTime = _nextEpoch - block.timestamp;

        if (_remainingRewardTime < minRemainingTime) {
            revert ErrInsufficientRemainingTime();
        }

        // Take the remainder of the current rewards and add it to the amount for the next period
        if (block.timestamp < reward.periodFinish) {
            amount += _remainingRewardTime * reward.rewardRate;
        }

        // avoid `rewardRate` being 0
        if (amount < _remainingRewardTime) {
            revert ErrNotEnoughReward();
        }

        reward.rewardRate = amount / _remainingRewardTime;
        reward.lastUpdateTime = uint248(block.timestamp);
        reward.periodFinish = _nextEpoch;

        emit LogRewardAdded(amount);
    }
```

## Recommendation

Update `notifyRewardAmount()` function to revert on zero `amount` of rewards:

```diff
function notifyRewardAmount(address rewardToken, uint256 amount, uint minRemainingTime) public onlyOperators {
+      require (amount > 0, "invalid amount");

    //the rest of the function
    }
```

## [L-07] `BlastPoints` library uses hardcoded addresses <a id="l-07" ></a>

## Details

`BlastPoints` library is used in multiple Blast contracts to configure the points operator, where it calls a hardcoded `BLAST_POINTS` contract to configure a hardcoded `BLAST_POINTS_OPERATOR`, but this might intoduce a risk to the contracts using this library to configure operator if any of the addresses got compromised/hacked or became inactive.

## Proof of Concept

[BlastPoints.configure function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/libraries/BlastPoints.sol#L6C1-L13C2)

```javascript
library BlastPoints {
    address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;
    IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);

    function configure() internal {
        BLAST_POINTS.configurePointsOperator(BLAST_POINTS_OPERATOR);
    }
}
```

## Recommendation

Update `BlastPoints.configure()` function to take these addreses as arguments.

## [L-08] `BlastOnboarding.withdraw()` function should allow withdrawing tokens that became unsupported <a id="l-08" ></a>

## Details

`BlastOnboarding` contract enables users to deposit and withdraw supported tokens via `deposit` & `withdraw` functions, where these supported tokens are whitelisted by the contract owner via `setTokenSupported()`, but if any of these tokens removed from the whitelist (became unsupported); users can't withdraw their deposits of this token unless rescued by the owner via `rescue()` functin, where an overhead will be incurred for this process by the owner.

## Proof of Concept

[BlastOnboarding.withdraw function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L132C1-L141C6)

```javascript
    function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
        balances[msg.sender][token].unlocked -= amount;
        balances[msg.sender][token].total -= amount;
        totals[token].unlocked -= amount;
        totals[token].total -= amount;

        token.safeTransfer(msg.sender, amount);

        emit LogWithdraw(msg.sender, token, amount);
    }
```

## Recommendation

Update `withdraw()` function to allow users from withdrawing their unsupported tokens:

```diff
-   function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
+   function withdraw(address token, uint256 amount) external whenNotPaused{
        balances[msg.sender][token].unlocked -= amount;
        balances[msg.sender][token].total -= amount;
        totals[token].unlocked -= amount;
        totals[token].total -= amount;

        token.safeTransfer(msg.sender, amount);

        emit LogWithdraw(msg.sender, token, amount);
    }
```

## [L-09] `BlastOnboarding` contract doesn't support fee-on-transfer tokens <a id="l-09" ></a>

## Details

- `BlastOnboarding` contract enables users to deposit and withdraw supported tokens via `deposit` & `withdraw` functions, where these supported tokens are whitelisted by the contract owner via `setTokenSupported()`.

- But if any of these tokens are of fee-on-transfer type (where the transferred amount is reduced by a fee amount), the last users withdrawing their deposits of that token will not be able to withdraw their full deposits as the contract balance will be insufficient since the actual balance is less than the tracked total deposited amount (due to the deducted fee for each transfer).

## Proof of Concept

[BlastOnboarding.deposit function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboarding.sol#L101C1-L121C6)

```javascript
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

## Recommendation

Either prevent using such tokens, or update deposit mechanism to account for the actual deposited amount after token-transfer-fee deduction.

## [L-10] Unifying `LockingMultiRewards.minLockAmount` variable doesn't fit all rewards tokens <a id="l-10" ></a>

## Details

- `LockingMultiRewards` contract has a `minLockAmount` variable that ensures that the amount **locked** for each stake for a user not to be less than that amount:

  ```javascript
      function _createLock(address user, uint256 amount) internal {
          //some code...

          // Add to current lock if it's the same unlock time or the first one
          // userLocks is sorted by unlockTime, so the last lock is the most recent one
          if (lockCount == 0 || _userLocks[user][_lastLockIndex].unlockTime < _nextUnlockTime) {
              // Limit the number of locks per user to avoid too much gas costs per user
              // when looping through the locks
              if (lockCount == maxLocks) {
                  revert ErrMaxUserLocksExceeded();
              }

              if (amount < minLockAmount) {
                  revert ErrLockAmountTooSmall();
              }

              _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));
              lastLockIndex[user] = lockCount;

              unchecked {
                  ++lockCount;
              }
          }
          //some code...
      }
  ```

- But since there are different rewards tokens (up to 5); then unifying the `minLockAmount` for all these tokens might not be reasonable and can be bypassed to grief users if that amount is considered a dust amount for some rewards tokens, or can be considered a very large amount for other rewards tokens, which will prevent users from creating locked staking for that token.

- For example:
  - if `minLockAmount` is set to 1e18, and among the rewards tokens are USDC (of 6 decimals) & WETH (of 18 decimals), so this minimum amount will be 1_000_000_000_000$ for USDC and 3900$ for WETH! which is unreasonable/very huge minimum amount for USDC.
  - if `minLockAmount` is set to 1e18 and among the rewards tokens are SPELL (of 18 decimals) & WETH (of 18 decimals), so this minimum amount will be ~ 0.0014$ for SPELL token and 3900$ for WETH! which is considered as a very low/dust value for SPELL token, and this can be exploited by a griefer to fill the locked staking arrays for users and preventing them from creating locked stakes to claim more rewards for that period/epoch (as they will wait until these locks are expired and processed/removed by operators so that they can create locks again).

## Proof of Concept

[LockingMultiRewards.minLockAmount variable](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/staking/LockingMultiRewards.sol#L102C5-L102C68)

```javascript
uint256 public minLockAmount; // minimum amount allowed to lock
```

## Recommendation

Update `Reward` struct to have this value specified for each reward token:

```diff
    struct Reward {
        uint256 periodFinish;
        uint256 rewardRate;
        uint256 rewardPerTokenStored;
        bool exists;
        uint248 lastUpdateTime;
+       uint256 minLockAmount;
    }
```

## [L-11] `MagicLP.setParameters()` function resets the reserves and the the targets even if the contract balances haven't been updated <a id="l-11" ></a>

## Details

`MagicLP.setParameters` function enables the contract owner from updating vital contract parameters such as `_K_`,`_I_`, `_LP_FEE_RATE_` and the balances and reserves of base and quote tokens by resetting these reserves via `_resetTargetAndReserve()`, but if the owner updates any of the parameters without actually updating the contract balances (no assets were sent out of the contract) like updating the `_LP_FEE_RATE_` only; the base and quote tokens reserves and targets will be reset to equal the current contract balance, and this will affect the price calculation of these assets upon selling/trading them.

## Proof of Concept

[MagicLP.setParameters function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L480C8-L482C10)

```javascript
function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner {

        if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
            revert ErrReserveAmountNotEnough();
        }

        // some code...

        _transferBaseOut(assetTo, baseOutAmount);
        _transferQuoteOut(assetTo, quoteOutAmount);
        (uint256 newBaseBalance, uint256 newQuoteBalance) = _resetTargetAndReserve();
        emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);
    }
```

[MagicLP.\_resetTargetAndReserve function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L528-L543)

```javascript
function _resetTargetAndReserve() internal returns (uint256 baseBalance, uint256 quoteBalance) {
        baseBalance = _BASE_TOKEN_.balanceOf(address(this));
        quoteBalance = _QUOTE_TOKEN_.balanceOf(address(this));

        if (baseBalance > type(uint112).max || quoteBalance > type(uint112).max) {
            revert ErrOverflow();
        }

        _BASE_RESERVE_ = uint112(baseBalance);
        _QUOTE_RESERVE_ = uint112(quoteBalance);
        _BASE_TARGET_ = uint112(baseBalance);
        _QUOTE_TARGET_ = uint112(quoteBalance);
        _RState_ = uint32(PMMPricing.RState.ONE);

        _twapUpdate();
    }
```

## Recommendation

Update `setParameters()` function to only call `_resetTargetAndReserve()` if the contract balances have been changed:

```diff
function setParameters(
        address assetTo,
        uint256 newLpFeeRate,
        uint256 newI,
        uint256 newK,
        uint256 baseOutAmount,
        uint256 quoteOutAmount,
        uint256 minBaseReserve,
        uint256 minQuoteReserve
    ) public nonReentrant onlyImplementationOwner {

        if (_BASE_RESERVE_ < minBaseReserve || _QUOTE_RESERVE_ < minQuoteReserve) {
            revert ErrReserveAmountNotEnough();
        }

        // some code...

        _transferBaseOut(assetTo, baseOutAmount);
        _transferQuoteOut(assetTo, quoteOutAmount);
+       if(baseOutAmount > 0 || quoteOutAmount > 0){
+       (uint256 newBaseBalance, uint256 newQuoteBalance) = _resetTargetAndReserve();
+       }
-       (uint256 newBaseBalance, uint256 newQuoteBalance) = _resetTargetAndReserve();
        emit ParametersChanged(newLpFeeRate, newI, newK, newBaseBalance, newQuoteBalance);
    }
```

## [L-12] `BlastBox` contract: token yield will be lost if the registry disabled it after being enabled <a id="l-12" ></a>

## Details

- `BlastBox.setTokenEnabled()` function is meant to set if the token is supported (enabled) or not; if enabled; then users can deposit this token and yield will accrue for this token **only if** the registry contract has this token supported:

  ```javascript
      function setTokenEnabled(address token, bool enabled) external onlyOwner {
          enabledTokens[token] = enabled;

          // enable native yields if token is recognized
          // no matter if it's enabled or not
          if (registry.nativeYieldTokens(token)) {
              BlastYields.enableTokenClaimable(token);
          }

          emit LogTokenDepositEnabled(token, enabled);
      }
  ```

- Then the `BlastBox` contract operators can claim the accrued token yield via `claimTokenYields()`, where it first checks the registry if the token is enabled or not; and if it's not enabled the transaction will revert:

  ```javascript
      function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
          if (!registry.nativeYieldTokens(token_)) {
              revert ErrUnsupportedToken();
          }

          amount = BlastYields.claimAllTokenYields(token_, feeTo);
      }
  ```

and by knowing that the `BlastTokenRegistry` contract owner can enable and disable tokens at anytime; then disabling a native yield token after enabling it will result in losing yield accrued for that token.

## Proof of Concept

[BlastBox.claimTokenYields function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastBox.sol#L56C1-L62C6)

```javascript
    function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
        if (!registry.nativeYieldTokens(token_)) {
            revert ErrUnsupportedToken();
        }

        amount = BlastYields.claimAllTokenYields(token_, feeTo);
    }
```

## Recommendation

Update `BlastBox.claimTokenYields()` function to enable claiming the registry-disabled-token yield so that it will not be lost:

```diff
    function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
-       if (!registry.nativeYieldTokens(token_)) {
-           revert ErrUnsupportedToken();
-       }

        amount = BlastYields.claimAllTokenYields(token_, feeTo);
    }
```

## [L-13] Consider using OpenZeppelin's SafeCast library to prevent unexpected overflows when casting from higher to lower uint types <a id="l-13" ></a>

## Details

In `MagicLp` contract, casting from higher uint types (`uint256`) to lower uint types (`uint32`, `uint112`) is done in multiple locations without checking if the casted value could result in unexpected silent overflowing/underflowing.

## Proof of Concept

[1.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L140C13-L140C54)

```javascript
_RState_ = uint32(PMMPricing.RState.ONE);
```

[2.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L145C13-L145C54)

```javascript
_RState_ = uint32(PMMPricing.RState.ONE);
```

[3.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L258C13-L258C42)

```javascript
_RState_ = uint32(newRState);
```

[4.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L281C13-L281C42)

```javascript
_RState_ = uint32(newRState);
```

[5.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L540C9-L540C50)

```javascript
_RState_ = uint32(PMMPricing.RState.ONE);
```

[6.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L257C13-L257C55)

```javascript
_BASE_TARGET_ = newBaseTarget.toUint112();
```

[7.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L280C13-L280C57)

```javascript
_QUOTE_TARGET_ = newQuoteTarget.toUint112();
```

[8.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L382C13-L382C48)

```javascript
_BASE_TARGET_ = shares.toUint112();
```

[9.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L383C12-L383C76)

```javascript
_QUOTE_TARGET_ = DecimalMath.mulFloor(shares, _I_).toUint112();
```

[10.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L402C4-L403C127)

```javascript
_BASE_TARGET_ = (
  uint256(_BASE_TARGET_) +
  DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)
).toUint112();
_QUOTE_TARGET_ = (
  uint256(_QUOTE_TARGET_) +
  DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)
).toUint112();
```

[11.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L561C6-L562C52)

```javascript
_BASE_RESERVE_ = baseReserve.toUint112();
_QUOTE_RESERVE_ = quoteReserve.toUint112();
```

[12.](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/mimswap/MagicLP.sol#L571C9-L576C10)

```javascript
if (baseBalance != _BASE_RESERVE_) {
  _BASE_RESERVE_ = baseBalance.toUint112();
}
if (quoteBalance != _QUOTE_RESERVE_) {
  _QUOTE_RESERVE_ = quoteBalance.toUint112();
}
```

## Recommendation

Consider using OpenZeppelin's SafeCast library to prevent unexpected overflows when casting from higher to lower uint types.

## [L-14] `BlastOnboardingBoot.setStaking()` function doesn't grant pool approvals on `totalPoolShares` <a id="l-14" ></a>

## Details

`BlastOnboardingBoot.setStaking()` function enables the contract owner from updating the `LockingMultiRewards` staking contract after the automatic bootstrapping process, but it was noticed that the contract doesn't approve the new staking contract on the `totalPoolShares`, which will result in reverting any transaction that would move the shares by the new staking contract.

## Proof of Concept

[BlastOnboardingBoot.setStaking function](https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/src/blast/BlastOnboardingBoot.sol#L137C4-L144C6)

```javascript
 function setStaking(LockingMultiRewards _staking) external onlyOwner {
        if (ready) {
            revert ErrCannotChangeOnceReady();
        }

        staking = _staking;
        emit LogStakingChanged(address(_staking));
    }
```

## Recommendation

```diff
 function setStaking(LockingMultiRewards _staking) external onlyOwner {
        if (ready) {
            revert ErrCannotChangeOnceReady();
        }

+       // Approve staking contract
+       pool.safeApprove(address(_staking), totalPoolShares);
        staking = _staking;
        emit LogStakingChanged(address(_staking));
    }
```
