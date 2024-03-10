The content section shows only 10 examples, subsequent cases are listed as links.

## Summary

### Low Severity issues

|                 | Issue                                                                                   | Instances |
| --------------- | :-------------------------------------------------------------------------------------- | :-------: |
| [[L-01](#l-01)] | Permanent DoS due to non-shrinking array usage in an unbounded loop                     |     5     |
| [[L-02](#l-02)] | Missing checks for `address(0)` when assigning values to address state variables        |     6     |
| [[L-03](#l-03)] | Empty receive functions can cause gas issues                                            |     2     |
| [[L-04](#l-04)] | Contract inherits Pausable but does not expose pausing/unpausing functionality          |     1     |
| [[L-05](#l-05)] | Emitting storage values instead of the memory one.                                      |     8     |
| [[L-06](#l-06)] | Functions calling contracts/addresses with transfer hooks are missing reentrancy guards |    37     |
| [[L-07](#l-07)] | `onlyOwner` functions not accessible if owner renounces ownership                       |    34     |
| [[L-08](#l-08)] | Subtraction may underflow if multiplication is too large                                |     1     |
| [[L-09](#l-09)] | Consider bounding input array length                                                    |     3     |
| [[L-10](#l-10)] | Use of `abi.encodePacked` with dynamic types inside `keccak256`                         |     1     |
| [[L-11](#l-11)] | Using `>`/`>=` without specifying an upper bound in version pragma is unsafe            |    20     |

### None Critical issues

|                 | Issue                                                                                                      | Instances |
| --------------- | :--------------------------------------------------------------------------------------------------------- | :-------: |
| [[N-01](#n-01)] | Empty function blocks                                                                                      |     4     |
| [[N-02](#n-02)] | Functions which are either private or internal should have a preceding _ in their name                     |    25     |
| [[N-03](#n-03)] | Function names should differ to make the code more readable                                                |     4     |
| [[N-04](#n-04)] | Emits without `msg.sender` parameter                                                                       |     6     |
| [[N-05](#n-05)] | A function which defines named returns in it's declaration doesn't need to use `return`                    |    21     |
| [[N-06](#n-06)] | Use multiple `require()` and `if` statements instead of `&&`                                               |    11     |
| [[N-07](#n-07)] | Change `public` to `external` for functions that are not called internally                                 |    17     |
| [[N-08](#n-08)] | `Constants` in comparisons should appear on the left side                                                  |    123    |
| [[N-09](#n-09)] | Do not use underscore at the end of variable name                                                          |    98     |
| [[N-10](#n-10)] | Event is missing `indexed` field                                                                           |    39     |
| [[N-11](#n-11)] | Variable names that consist of all capital letters should be reserved for `constant`/`immutable` variables |    35     |
| [[N-12](#n-12)] | Consider using `delete` rather than assigning zero/false to clear values                                   |     3     |
| [[N-13](#n-13)] | Array is `push()`ed but not `pop()`ed                                                                      |     5     |
| [[N-14](#n-14)] | Unused contract variables                                                                                  |    27     |
| [[N-15](#n-15)] | `else`-block not required                                                                                  |     5     |
| [[N-16](#n-16)] | Remaining eth may not be refunded to users                                                                 |     7     |
| [[N-17](#n-17)] | Condition will not revert when `block.timestamp` is `==` to the compared variable                          |     3     |
| [[N-18](#n-18)] | External calls in an un-bounded `for`-loop may result in a DOS                                             |     8     |
| [[N-19](#n-19)] | `constructor` missing zero address check                                                                   |    11     |
| [[N-20](#n-20)] | Variable initialization with default value                                                                 |     2     |
| [[N-21](#n-21)] | Complex math should be split into multiple steps                                                           |    21     |
| [[N-22](#n-22)] | Duplicated `require/if` statements should be refactored                                                    |    69     |
| [[N-23](#n-23)] | Variable names don't follow the Solidity naming convention                                                 |    38     |
| [[N-24](#n-24)] | Contract functions should use an `interface`                                                               |    124    |
| [[N-25](#n-25)] | Custom `error` without details                                                                             |    78     |
| [[N-26](#n-26)] | State variables should include comments                                                                    |    83     |
| [[N-27](#n-27)] | Events that mark critical parameter changes should contain both the old and the new value                  |    20     |
| [[N-28](#n-28)] | Constant redefined elsewhere                                                                               |     2     |
| [[N-29](#n-29)] | Function ordering does not follow the Solidity style guide                                                 |    12     |
| [[N-30](#n-30)] | Array indicies should be referenced via `enum`s rather than via numeric literals                           |     3     |
| [[N-31](#n-31)] | Use of `override` is unnecessary                                                                           |    13     |
| [[N-32](#n-32)] | Unused function parameter                                                                                  |    13     |
| [[N-33](#n-33)] | Unused `event` definition                                                                                  |     3     |
| [[N-34](#n-34)] | Function names should use lowerCamelCase                                                                   |    22     |
| [[N-35](#n-35)] | Overflows in unchecked blocks                                                                              |     9     |
| [[N-36](#n-36)] | Missing event and or timelock for critical parameter change                                                |    21     |
| [[N-37](#n-37)] | Setters should prevent re-setting of the same value                                                        |    21     |
| [[N-38](#n-38)] | Events may be emitted out of order due to reentrancy                                                       |    16     |
| [[N-39](#n-39)] | Execution at deadlines should be allowed                                                                   |     4     |
| [[N-40](#n-40)] | Function can return unassigned variable                                                                    |     1     |
| [[N-41](#n-41)] | Missing zero address check in initializer                                                                  |     1     |
| [[N-42](#n-42)] | Events should be emitted before external calls                                                             |    38     |
| [[N-43](#n-43)] | Use `@inheritdoc` for overridden functions                                                                 |    13     |
| [[N-44](#n-44)] | Contract name does not follow the Solidity Style Guide                                                     |     7     |
| [[N-45](#n-45)] | Variable names for `immutable`s should use UPPER_CASE_WITH_UNDERSCORES                                     |    16     |
| [[N-46](#n-46)] | Use a single file for system wide constants                                                                |    22     |
| [[N-47](#n-47)] | Unsafe `uint` to `int` conversion                                                                          |     1     |
| [[N-48](#n-48)] | Use SafeCast to safely downcast variables                                                                  |    30     |
| [[N-49](#n-49)] | Consider adding a block/deny-list                                                                          |     5     |
| [[N-50](#n-50)] | Expressions for constant values should use `immutable` rather than `constant`                              |     7     |
| [[N-51](#n-51)] | Lines are too long                                                                                         |    54     |

### Low Risk Issues

### [L-01]<a name="l-01"></a> Permanent DoS due to non-shrinking array usage in an unbounded loop

There are some arrays that can grow indefinitely in size, as they never shrink. When these arrays are used in unbounded loops, they may lead to a permanent denial-of-service (DoS) of these functions.

*There are 5 instance(s) of this issue:*


---

	 - src/staking/LockingMultiRewards.sol

```solidity
// @audit Array pushed here, but never poped
313	        rewardTokens.push(rewardToken);
...
// @audit Array pushed here, but never poped
501	            _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));
...
// @audit Array pushed here, but never poped
648	                _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
...
// @audit function _updateRewards is vulnerable as length grows in size but never shrinks
547	        for (uint256 i; i < rewardTokens.length; ) {
...
// @audit function _updateRewardsForUser is vulnerable as length grows in size but never shrinks
561	        for (uint256 i; i < rewardTokens.length; ) {
...
// @audit function _updateRewardsForUsers is vulnerable as length grows in size but never shrinks
575	        for (uint256 i; i < rewardTokens.length; ) {
...
// @audit function _updateRewardsForUsers is vulnerable as length grows in size but never shrinks
580	            for (uint256 j; j < users.length; ) {
...
// @audit function _getRewards is vulnerable as length grows in size but never shrinks
614	        for (uint256 i; i < rewardTokens.length; ) {
```

*GitHub* : [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547), [561](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561), [575](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575), [580](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580), [614](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614)

### [L-02]<a name="l-02"></a> Missing checks for `address(0)` when assigning values to address state variables



*There are 6 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
190	    function setBootstrapper(address bootstrapper_) external onlyOwner {
...
// @audit Address `bootstrapper_` is not cheched for zero in current function
191	        bootstrapper = bootstrapper_;
```

*GitHub* : [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L191)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
96	    function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
...
// @audit Address `` is not cheched for zero in current function
117	        staking = new LockingMultiRewards(pool, 30_000, 7 days, 13 weeks, address(this));
...
129	    function initialize(Router _router) external onlyOwner {
...
// @audit Address `` is not cheched for zero in current function
130	        router = Router(payable(_router));
...
// @audit Address `` is not cheched for zero in current function
131	        factory = IFactory(router.factory());
...
137	    function setStaking(LockingMultiRewards _staking) external onlyOwner {
...
// @audit Address `_staking` is not cheched for zero in current function
142	        staking = _staking;
```

*GitHub* : [117](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L117), [130](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L130), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L131), [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L142)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol

```solidity
57	    function setImplementation(address implementation_) public onlyOwner {
```

*GitHub* : [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L58)

### [L-03]<a name="l-03"></a> Empty receive functions can cause gas issues

In Solidity, functions that receive Ether without corresponding functionality to utilize or withdraw these funds can inadvertently lead to a permanent loss of value. This is because if someone sends Ether to the contract, they may be unable to retrieve it. To avoid this, functions receiving Ether should be accompanied by additional methods that process or allow the withdrawal of these funds. If the intent is to use the received Ether, it should trigger a separate function; if not, it should revert the transaction (for instance, via `require(msg.sender == address(weth))`). Access control checks can also prevent unintended Ether transfers, despite the slight gas cost they entail. If concerns over gas costs persist, at minimum, include a rescue function to recover unused Ether. Missteps in handling Ether in smart contracts can lead to irreversible financial losses, hence these precautions are crucial.

*There are 2 instance(s) of this issue:*


---

	 - src/blast/BlastGovernor.sol

```solidity
13	    receive() external payable {}
```

*GitHub* : [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L13)


---

	 - src/mimswap/periphery/Router.sol

```solidity
36	    receive() external payable {}
```

*GitHub* : [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L36)

### [L-04]<a name="l-04"></a> Contract inherits Pausable but does not expose pausing/unpausing functionality

When a contract inherits from the Pausable contract in Solidity, it gains the ability to pause and resume certain actions, which can be crucial in mitigating potential risks or issues. However, the _pause and _unpause functions are internal and can only be called from within the contract or derived contracts. If the functionality to pause and unpause isn't exposed through public or external functions, it can't be called by the contract owner or designated pauser account.

Resolution: To take advantage of the Pausable contract, create public or external functions that call _pause and _unpause.

*There are 1 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
12	contract BlastOnboardingData is Owned, Pausable {
13	    error ErrZeroAddress();
14	    error ErrWrongState();
15	    error ErrUnsupportedToken();
16	    error ErrNotAllowed();
17	
18	    enum State {
19	        Idle,
20	        Opened,
21	        Closed
22	    }
23	
24	    struct Balances {
25	        uint256 unlocked;
26	        uint256 locked;
27	        uint256 total;
28	    }
29	
30	    State public state;
31	    address public bootstrapper;
32	    address public feeTo;
33	    BlastTokenRegistry public registry;
34	
35	    // Global
36	    mapping(address token => bool) public supportedTokens;
37	    mapping(address token => Balances) public totals;
38	    mapping(address token => uint256 cap) public caps;
39	
40	    // Per-user
41	    mapping(address user => mapping(address token => Balances)) public balances;
42	
43	    modifier onlyState(State _state) {
44	        if (state != _state) {
45	            revert ErrWrongState();
46	        }
47	        _;
48	    }
49	
50	    modifier onlySupportedTokens(address token) {
51	        if (!supportedTokens[token]) {
52	            revert ErrUnsupportedToken();
53	        }
54	
55	        _;
56	    }
57	
58	    constructor() Owned(msg.sender) {
59	        BlastYields.configureDefaultClaimables(address(this));
60	        BlastPoints.configure();
61	    }
62	}
```

*GitHub* : [12..62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L12-L62)

### [L-05]<a name="l-05"></a> Emitting storage values instead of the memory one.

Emitted values should not be read from storage again. Instead, the existing values from memory should be used.

*There are 8 instance(s) of this issue:*


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
124	        emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);
...
148	        emit LogReadyChanged(ready);
```

*GitHub* : [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L148)


---

	 - src/mimswap/MagicLP.sol

```solidity
264	        emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, to);
...
287	        emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, to);
...
325	            emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);
...
347	            emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
```

*GitHub* : [264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L264), [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L287), [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L325), [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L347)


---

	 - src/mimswap/periphery/Factory.sol

```solidity
88	        emit LogCreated(clone, baseToken_, quoteToken_, creator, lpFeeRate_, maintainerFeeRateModel, i_, k_);
```

*GitHub* : [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
318	        emit LogSetMinLockAmount(minLockAmount, _minLockAmount);
```

*GitHub* : [318](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L318)

### [L-06]<a name="l-06"></a> Functions calling contracts/addresses with transfer hooks are missing reentrancy guards

Even if the function follows the best practice of check-effects-interaction, not using a reentrancy guard when there may be transfer hooks will open the users of this protocol up to [read-only reentrancies](https://chainsecurity.com/curve-lp-oracle-manipulation-post-mortem/) with no way to protect against it, except by block-listing the whole protocol.`

*There are 37 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
101	    function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
...
// @audit Function `deposit` doesn't  have the `nonReentrant` modifier
102	        token.safeTransferFrom(msg.sender, address(this), amount);
...
132	    function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
...
// @audit Function `withdraw` doesn't  have the `nonReentrant` modifier
138	        token.safeTransfer(msg.sender, amount);
...
205	    function rescue(address token, address to, uint256 amount) external onlyOwner {
...
// @audit Function `rescue` doesn't  have the `nonReentrant` modifier
210	        token.safeTransfer(to, amount);
```

*GitHub* : [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L102), [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L138), [210](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L210)


---

	 - src/mimswap/MagicLP.sol

```solidity
461	    function rescue(address token, address to, uint256 amount) external onlyImplementationOwner {
...
// @audit Function `rescue` doesn't  have the `nonReentrant` modifier
466	        token.safeTransfer(to, amount);
...
581	    function _transferBaseOut(address to, uint256 amount) internal {
...
// @audit Function `_transferBaseOut` doesn't  have the `nonReentrant` modifier
583	            _BASE_TOKEN_.safeTransfer(to, amount);
```

*GitHub* : [466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L466), [583](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L583), [589](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L589)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L68), [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L69), [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L91), [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L92), [172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L172), [173](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L173), [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L186), [187](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L187), [217](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L217), [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L224), [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L244), [246](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L246), [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L269), [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L282), [311](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L311), [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L330), [328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L328), [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L360), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L395), [393](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L393), [411](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L411), [428](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L428), [443](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L443), [456](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L456), [474](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L474), [489](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L489)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [180](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L180), [330](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L330), [367](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L367), [464](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L464), [637](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L637)

### [L-07]<a name="l-07"></a> `onlyOwner` functions not accessible if owner renounces ownership

The `owner` is able to perform certain privileged activities, but it's possible to set the owner to `address(0)`. This can represent a certain risk if the ownership is renounced for any other reason than by design.
Renouncing ownership will leave the contract without an `owner`, therefore limiting any functionality that needs authority.

*There are 34 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
68	    function callBlastPrecompile(bytes calldata data) external onlyOwner {
...
72	    function setFeeTo(address feeTo_) external onlyOwner {
...
81	    function setTokenEnabled(address token, bool enabled) external onlyOwner {
```

*GitHub* : [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L68), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81)


---

	 - src/blast/BlastGovernor.sol

```solidity
40	    function setFeeTo(address _feeTo) external onlyOwner {
...
49	    function callBlastPrecompile(bytes calldata data) external onlyOwner {
...
53	    function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

*GitHub* : [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40), [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L49), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)


---

	 - src/blast/BlastOnboarding.sol

```solidity
147	    function setFeeTo(address feeTo_) external onlyOwner {
...
156	    function callBlastPrecompile(bytes calldata data) external onlyOwner {
...
160	    function claimGasYields() external onlyOwner returns (uint256) {
...
164	    function claimTokenYields(address[] memory tokens) external onlyOwner {
```

*GitHub* : [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L156), [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L160), [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190), [195](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L195), [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L200), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L205), [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L214), [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L218)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96), [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129), [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105), [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L116), [120..126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L120-L126)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300), [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317), [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L324), [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337), [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L341)

### [L-08]<a name="l-08"></a> Subtraction may underflow if multiplication is too large

The following expressions may underflow, as the subtrahend could be greater than the minuend in case the former is multiplied by a large number.

*There are 1 instance(s) of this issue:*


---

	 - src/mimswap/libraries/Math.sol

```solidity
21	        uint256 remainder = a - quotient * b;
```

*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L21)

### [L-09]<a name="l-09"></a> Consider bounding input array length

The functions below take in an unbounded array, and make function calls for entries in the array. While the function will revert if it eventually runs out of gas, it may be a nicer user experience to `require()` that the length of the array is below some reasonable maximum, so that the user doesn't have to use up a full transaction's gas only to see that the transaction reverts.

*There are 3 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
164	    function claimTokenYields(address[] memory tokens) external onlyOwner {
```

*GitHub* : [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
397	    function processExpiredLocks(address[] memory users, uint256[] calldata lockIndexes) external onlyOperators {
...
572	    function _updateRewardsForUsers(address[] memory users) internal {
```

*GitHub* : [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397), [572](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L572)

### [L-10]<a name="l-10"></a> Use of `abi.encodePacked` with dynamic types inside `keccak256`

`abi.encodePacked` should not be used with dynamic types when passing the result to a hash function such as `keccak256`. Use `abi.encode` instead, which will pad items to 32 bytes, to [prevent any hash collisions](https://docs.soliditylang.org/en/latest/abi-spec.html#non-standard-packed-mode).

*There are 1 instance(s) of this issue:*


---

	 - src/mimswap/periphery/Factory.sol

```solidity
163	        return keccak256(abi.encodePacked(sender_, implementation, baseToken_, quoteToken_, lpFeeRate_, i_, k_));
```

*GitHub* : [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L163)

### [L-11]<a name="l-11"></a> Using `>`/`>=` without specifying an upper bound in version pragma is unsafe

There **will** be breaking changes in future versions of solidity, and at that point your code will no longer be compatible. While you may have the specific version to use in a configuration file, others that include your source files may not.

*There are 20 instance(s) of this issue:*


---

	 - src/blast/BlastDapp.sol

```solidity
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2)


---

	 - src/blast/BlastBox.sol

```solidity
3	pragma solidity >=0.8.0;
```

*GitHub* : [3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L3)


---

	 - src/blast/BlastGovernor.sol

```solidity
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L2)


---

	 - src/blast/BlastMagicLP.sol

```solidity
3	pragma solidity >=0.8.0;
```

*GitHub* : [3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L3)


---

	 - src/blast/BlastOnboarding.sol

```solidity
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L2)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L2)


---

	 - src/blast/BlastTokenRegistry.sol

```solidity
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L2)


---

	 - src/blast/BlastWrappers.sol

```solidity
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L2)


---

	 - src/blast/libraries/BlastPoints.sol

```solidity
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L2)


---

	 - src/blast/libraries/BlastYields.sol

```solidity
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L2)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L8)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L8)


---

	 - src/mimswap/auxiliary/FeeRateModelImpl.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2)


---

	 - src/mimswap/libraries/DecimalMath.sol


*GitHub* : [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L7)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L8)


---

	 - src/mimswap/libraries/PMMPricing.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L8)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L2)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L2)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L2)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L2)

### NonCritical Risk Issues

### [N-01]<a name="n-01"></a> Empty function blocks

Empty code blocks (i.e., {}) in a Solidity contract can be harmful as they can lead to ambiguity, misinterpretation, and unintended behavior. When developers encounter empty code blocks, it may be unclear whether the absence of code is intentional or the result of an oversight. This uncertainty can cause confusion during development, testing, and debugging, increasing the likelihood of introducing errors or vulnerabilities. Moreover, empty code blocks may give a false impression of implemented functionality or security measures, creating a misleading sense of assurance. To ensure clarity and maintainability, it is essential to avoid empty code blocks and explicitly document the intended behavior or any intentional omissions.

*There are 4 instance(s) of this issue:*


---

	 - src/blast/BlastGovernor.sol

```solidity
13	    receive() external payable {}
```

*GitHub* : [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L13)


---

	 - src/blast/BlastTokenRegistry.sol

```solidity
12	    constructor(address _owner) Owned(_owner) {}
```

*GitHub* : [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L12)


---

	 - src/mimswap/MagicLP.sol

```solidity
601	    function _afterInitialized() internal virtual {}
```

*GitHub* : [601](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L601)


---

	 - src/mimswap/periphery/Router.sol

```solidity
36	    receive() external payable {}
```

*GitHub* : [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L36)

### [N-02]<a name="n-02"></a> Functions which are either private or internal should have a preceding _ in their name

Add a preceding underscore to the function name, take care to refactor where there functions are called

*There are 25 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
103	    function isOwner(address _account) internal view override returns (bool) {
```

*GitHub* : [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L103)


---

	 - src/blast/libraries/BlastPoints.sol

```solidity
10	    function configure() internal {
```

*GitHub* : [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L10)


---

	 - src/blast/libraries/BlastYields.sol

```solidity
20	    function enableTokenClaimable(address token) internal {
...
29	    function configureDefaultClaimables(address governor_) internal {
...
38	    function claimMaxGasYields(address recipient) internal returns (uint256) {
...
42	    function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {
...
51	    function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
...
55	    function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {
...
60	    function claimNativeYields(address contractAddress, uint256 amount, address recipient) internal returns (uint256) {
...
70	    function claimAllTokenYields(address token, address recipient) internal returns (uint256 amount) {
```

*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L20), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L29), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L38), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L42), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L51), [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L55), [60](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L60), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L70), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L75), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L86)


---

	 - src/mimswap/libraries/DecimalMath.sol


*GitHub* : [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L23), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L27), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L31), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L35), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L39), [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L43), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L47)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L19), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L29)


---

	 - src/mimswap/libraries/PMMPricing.sol


*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L39), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L76), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L190), [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L203)

### [N-03]<a name="n-03"></a> Function names should differ to make the code more readable

In Solidity, while function overriding allows for functions with the same name to coexist, it is advisable to avoid this practice to enhance code readability and maintainability. Having multiple functions with the same name, even with different parameters or in inherited contracts, can cause confusion and increase the likelihood of errors during development, testing, and debugging. Using distinct and descriptive function names not only clarifies the purpose and behavior of each function, but also helps prevent unintended function calls or incorrect overriding. By adopting a clear and consistent naming convention, developers can create more comprehensible and maintainable smart contracts.

*There are 4 instance(s) of this issue:*


---

	 - src/blast/libraries/BlastYields.sol

```solidity
51	    function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
...
55	    function claimAllNativeYields(address contractAddress, address recipient) internal returns (uint256 amount) {
...
38	    function claimMaxGasYields(address recipient) internal returns (uint256) {
...
42	    function claimMaxGasYields(address contractAddress, address recipient) internal returns (uint256 amount) {
```

*GitHub* : [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L51), [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L55), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L38), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L42)

### [N-04]<a name="n-04"></a> Emits without `msg.sender` parameter

If `msg.sender` play a part in the functionality of a function, any emits of this function should include msg.sender to ensure transparency with users

*There are 6 instance(s) of this issue:*


---

	 - src/mimswap/MagicLP.sol

```solidity
// @audit Current function use `msg.sender`, but do not emit it
259	            emit RChange(newRState);
...
// @audit Current function use `msg.sender`, but do not emit it
282	            emit RChange(newRState);
...
// @audit Current function use `msg.sender`, but do not emit it
323	                emit RChange(newRState);
...
// @audit Current function use `msg.sender`, but do not emit it
345	                emit RChange(newRState);
```

*GitHub* : [259](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L259), [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L282), [323](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L323), [345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L345)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
// @audit Current function use `msg.sender`, but do not emit it
392	        emit LogRewardAdded(amount);
...
// @audit Current function use `msg.sender`, but do not emit it
475	            emit LogStaked(account, amount);
```

*GitHub* : [392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L392), [475](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L475)

### [N-05]<a name="n-05"></a> A function which defines named returns in it's declaration doesn't need to use `return`

Once the return variable has been assigned (or has its default value), there is no need to explicitly return it at the end of the function, since it's returned automatically.
Remove the return statement once ensuring it is safe to do so

*There are 21 instance(s) of this issue:*


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
78	    function claimable(address user) external view returns (uint256 shares) {
...
86	    function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
155	    function _claimable(address user) internal view returns (uint256 shares) {
```

*GitHub* : [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L78), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L155)


---

	 - src/blast/libraries/BlastYields.sol

```solidity
51	    function claimAllNativeYields(address recipient) internal returns (uint256 amount) {
```

*GitHub* : [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L51)


---

	 - src/mimswap/MagicLP.sol

```solidity
215	    function getMidPrice() public view returns (uint256 midPrice) {
...
224	    function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
...
228	    function getBaseInput() public view returns (uint256 input) {
...
232	    function getQuoteInput() public view returns (uint256 input) {
```

*GitHub* : [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L215), [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L224), [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L228), [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L232)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol

```solidity
34	    function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```

*GitHub* : [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34)


---

	 - src/mimswap/auxiliary/FeeRateModelImpl.sol

```solidity
9	    function getFeeRate(
10	        address /*pool*/,
11	        address /*trader*/,
12	        uint256 lpFeeRate
13	    ) external pure returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```

*GitHub* : [9..13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L13)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [96..100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L96-L100), [112..116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L112-L116), [178..185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L178-L185), [229..235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229-L235), [261..268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L261-L268), [314..321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L314-L321), [336..342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336-L342), [404..410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L404-L410), [415..420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L415-L420), [449..455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L449-L455), [461..466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L461-L466)

### [N-06]<a name="n-06"></a> Use multiple `require()` and `if` statements instead of `&&`

Using multiple `require()` and `if` improves code readability and makes it easier to debug.

*There are 11 instance(s) of this issue:*


---

	 - src/blast/BlastMagicLP.sol

```solidity
119	        if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {
120	            revert ErrNotAllowedImplementationOperator();
121	        }
```

*GitHub* : [119..121](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L119-L121)


---

	 - src/blast/BlastOnboarding.sol

```solidity
114	        if (caps[token] > 0 && totals[token].total > caps[token]) {
115	            revert ErrCapReached();
116	        }
```

*GitHub* : [114..116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114-L116)


---

	 - src/mimswap/MagicLP.sol

```solidity
139	        if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
140	            _RState_ = uint32(PMMPricing.RState.ONE);
141	            _BASE_TARGET_ = _BASE_RESERVE_;
142	            _QUOTE_TARGET_ = _QUOTE_RESERVE_;
143	        }
...
144	        if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
145	            _RState_ = uint32(PMMPricing.RState.ONE);
146	            _BASE_TARGET_ = _BASE_RESERVE_;
147	            _QUOTE_TARGET_ = _QUOTE_RESERVE_;
148	        }
...
302	        if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {
303	            revert ErrFlashLoanFailed();
304	        }
...
395	        } else if (baseReserve > 0 && quoteReserve > 0) {
396	            // case 2. normal case
397	            uint256 baseInputRatio = DecimalMath.divFloor(baseInput, baseReserve);
398	            uint256 quoteInputRatio = DecimalMath.divFloor(quoteInput, quoteReserve);
399	            uint256 mintRatio = quoteInputRatio < baseInputRatio ? quoteInputRatio : baseInputRatio;
400	            shares = DecimalMath.mulFloor(totalSupply(), mintRatio);
401	
402	            _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();
403	            _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
404	        }
...
549	        if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {
550	            /// @dev It is desired and expected for this value to
551	            /// overflow once it has hit the max of `type.uint256`.
552	            unchecked {
553	                _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
554	            }
555	        }
```

*GitHub* : [139..143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139-L143), [144..148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144-L148), [302..304](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L302-L304), [395..404](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395-L404), [549..555](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549-L555)


---

	 - src/mimswap/periphery/Router.sol

```solidity
147	        } else if (baseReserve > 0 && quoteReserve > 0) {
148	            uint256 baseInputRatio = DecimalMath.divFloor(baseInAmount, baseReserve);
149	            uint256 quoteInputRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);
150	            if (baseInputRatio <= quoteInputRatio) {
151	                baseAdjustedInAmount = baseInAmount;
152	                quoteAdjustedInAmount = DecimalMath.mulCeil(quoteReserve, baseInputRatio);
153	                shares = DecimalMath.mulFloor(totalSupply, baseInputRatio);
154	            } else {
155	                quoteAdjustedInAmount = quoteInAmount;
156	                baseAdjustedInAmount = DecimalMath.mulCeil(baseReserve, quoteInputRatio);
157	                shares = DecimalMath.mulFloor(totalSupply, quoteInputRatio);
158	            }
159	        }
...
527	            if (quoteReserve > 0 && baseReserve > 0) {
528	                uint256 baseIncreaseRatio = DecimalMath.divFloor(baseInAmount, baseReserve);
529	                uint256 quoteIncreaseRatio = DecimalMath.divFloor(quoteInAmount, quoteReserve);
530	                if (baseIncreaseRatio <= quoteIncreaseRatio) {
531	                    baseAdjustedInAmount = baseInAmount;
532	                    quoteAdjustedInAmount = DecimalMath.mulFloor(quoteReserve, baseIncreaseRatio);
533	                } else {
534	                    quoteAdjustedInAmount = quoteInAmount;
535	                    baseAdjustedInAmount = DecimalMath.mulFloor(baseReserve, quoteIncreaseRatio);
536	                }
537	            }
```

*GitHub* : [147..159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147-L159), [527..537](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527-L537)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
326	        if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {
327	            revert ErrSkimmingTooMuch();
328	        }
```

*GitHub* : [326..328](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L326-L328), [417..419](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L417-L419)

### [N-07]<a name="n-07"></a> Change `public` to `external` for functions that are not called internally

Contracts [are allowed](https://docs.soliditylang.org/en/latest/contracts.html#function-overriding) to override their parents' functions and change the visibility from `external` to `public`.

*There are 17 instance(s) of this issue:*


---

	 - src/blast/BlastWrappers.sol

```solidity
59	    function init(bytes calldata data) public payable override {
```

*GitHub* : [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59)


---

	 - src/mimswap/MagicLP.sol

```solidity
155	    function name() public view override returns (string memory) {
...
159	    function symbol() public pure override returns (string memory) {
...
163	    function decimals() public view override returns (uint8) {
...
228	    function getBaseInput() public view returns (uint256 input) {
...
232	    function getQuoteInput() public view returns (uint256 input) {
...
470	    function setParameters(
471	        address assetTo,
472	        uint256 newLpFeeRate,
473	        uint256 newI,
474	        uint256 newK,
475	        uint256 baseOutAmount,
476	        uint256 quoteOutAmount,
477	        uint256 minBaseReserve,
478	        uint256 minQuoteReserve
479	    ) public nonReentrant onlyImplementationOwner {
```

*GitHub* : [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155), [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L159), [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163), [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L228), [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L232), [470..479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470-L479)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol

```solidity
57	    function setImplementation(address implementation_) public onlyOwner {
```

*GitHub* : [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)


---

	 - src/mimswap/periphery/Factory.sol

```solidity
65	    function predictDeterministicAddress(
66	        address creator,
67	        address baseToken_,
68	        address quoteToken_,
69	        uint256 lpFeeRate_,
70	        uint256 i_,
71	        uint256 k_
72	    ) public view returns (address) {
```

*GitHub* : [65..72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65-L72)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
150	    function stake(uint256 amount, bool lock_) public whenNotPaused {
```

*GitHub* : [150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L150), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L155), [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L186), [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L191), [265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L265), [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L288), [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300), [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361)

### [N-08]<a name="n-08"></a> `Constants` in comparisons should appear on the left side

Doing so will prevent [typo bugs](https://www.moserware.com/2008/01/constants-on-left-are-better-but-this.html)

*There are 123 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
25	        if (feeTo_ == address(0)) {
...
28	        if (address(registry_) == address(0)) {
...
73	        if (feeTo_ == address(0)) {
```

*GitHub* : [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L25), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L28), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L73)


---

	 - src/blast/BlastGovernor.sol

```solidity
16	        if (feeTo_ == address(0)) {
...
41	        if(_feeTo == address(0)) {
```

*GitHub* : [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L16), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L41)


---

	 - src/blast/BlastMagicLP.sol

```solidity
24	        if (feeTo_ == address(0)) {
...
27	        if (address(registry_) == address(0)) {
...
81	        if (feeTo_ == address(0)) {
```

*GitHub* : [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L24), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L27), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L81)


---

	 - src/blast/BlastOnboarding.sol

```solidity
85	        if (address(registry_) == address(0)) {
...
89	        if (feeTo_ == address(0)) {
```

*GitHub* : [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L85), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L89), [114](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L114), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L148)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L64), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L97), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L158)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L15)


---

	 - src/blast/BlastWrappers.sol


*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L21), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L35), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L48)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L102), [108](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L108), [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L125), [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L294), [369](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L369), [375](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L375), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395), [395](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L395), [377](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L377), [385](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L385), [389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L389), [450](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L450), [483](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L483), [546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L546), [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549), [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549), [549](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L549), [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L582), [588](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L588), [594](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L594)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L23), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L35), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L47)


---

	 - src/mimswap/libraries/DecimalMath.sol


*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L21), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L48), [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L50), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L53), [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L55), [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L55), [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L49)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L22), [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L23), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L30), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L30), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34), [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L52), [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L58), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L80), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L89), [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L94), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L101), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L132), [136](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L136), [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L140), [153](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L153), [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184), [188](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L188), [192](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L192)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L39), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L42), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L97), [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L106), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L131), [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L138)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L39), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L39), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L105), [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L125), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L131), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L147), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L132), [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L142), [327](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L327), [327](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L327), [348](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L348), [348](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L348), [375](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L375), [379](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L379), [379](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L379), [392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L392), [392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L392), [521](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L521), [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527), [527](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L527), [542](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L542), [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L545), [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L545), [550](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L550), [547](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L547), [560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L560), [560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L560), [590](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L590), [593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L593), [599](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L599), [599](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L599)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L131), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L156), [171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L171), [278](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L278), [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283), [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294), [301](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L301), [410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L410), [417](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L417), [427](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L427), [459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L459), [490](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L490), [636](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L636)

### [N-09]<a name="n-09"></a> Do not use underscore at the end of variable name

The use of underscore at the end of the variable name is uncommon and also suggests that the variable name was not completely changed.

Consider refactoring variableName_ to variableName.

*There are 98 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
24	    constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
...
24	    constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
...
24	    constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
...
56	    function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
...
72	    function setFeeTo(address feeTo_) external onlyOwner {
```

*GitHub* : [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L56), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72)


---

	 - src/blast/BlastGovernor.sol

```solidity
15	    constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```

*GitHub* : [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15)


---

	 - src/blast/BlastMagicLP.sol

```solidity
23	    constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
...
23	    constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
...
23	    constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
...
48	        address feeTo_ = BlastMagicLP(address(implementation)).feeTo();
```

*GitHub* : [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23), [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23), [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L48), [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L54), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80)


---

	 - src/blast/BlastOnboarding.sol


*GitHub* : [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L84), [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L84), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190)


---

	 - src/blast/BlastWrappers.sol


*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20), [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L30), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L31), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L33), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L47), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L47), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L47)


---

	 - src/blast/libraries/BlastYields.sol


*GitHub* : [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L29)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L68), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L70), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L71), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L75), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L78), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L79), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L80), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L81), [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L82), [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22), [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22), [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L13), [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L14), [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L15), [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L16), [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L17), [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L19), [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L20), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38), [67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L67), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L68), [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L69), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L70), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L71), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L156), [157](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L157), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L158), [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L159), [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L160), [161](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L161)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L38)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L150), [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277), [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277), [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L292), [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L292), [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L349), [458](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L458), [529](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L529), [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L528), [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L528), [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L528), [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L536), [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L536), [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L536), [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L536), [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L545), [559](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L559), [573](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L573), [577](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L577)

### [N-10]<a name="n-10"></a> Event is missing `indexed` field



*There are 39 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
14	    event LogTokenDepositEnabled(address indexed token, bool enabled);
```

*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L14)


---

	 - src/blast/BlastMagicLP.sol

```solidity
12	    event LogOperatorChanged(address indexed, bool);
...
13	    event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);
```

*GitHub* : [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L12), [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L13)


---

	 - src/blast/BlastOnboarding.sol

```solidity
68	    event LogTokenSupported(address indexed token, bool supported);
...
69	    event LogDeposit(address indexed user, address indexed token, uint256 amount, bool lock);
...
70	    event LogLock(address indexed user, address indexed token, uint256 amount);
...
72	    event LogWithdraw(address indexed user, address indexed token, uint256 amount);
...
73	    event LogTokenCapChanged(address indexed token, uint256 cap);
...
74	    event LogStateChange(State state);
...
75	    event LogTokenRescue(address indexed token, address indexed to, uint256 amount);
```

*GitHub* : [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L68), [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L69), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L70), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L74), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L75)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L37), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L38), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L40)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L7)


---

	 - src/blast/libraries/BlastYields.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L8), [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L9), [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L10)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L30), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L31), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L33), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L34), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L35), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L36)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L23), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L24), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L27)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L17), [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L18), [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L19), [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L21), [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L22), [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L23), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L24), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L26), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L27), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L28)

### [N-11]<a name="n-11"></a> Variable names that consist of all capital letters should be reserved for `constant`/`immutable` variables

If the variable needs to be different based on which class it comes from, a `view`/`pure` _function_ should be used instead (e.g. like [this](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/76eee35971c2541585e05cbf258510dda7b2fbc6/contracts/token/ERC20/extensions/draft-IERC20Permit.sol#L59)).

*There are 35 instance(s) of this issue:*


---

	 - src/mimswap/MagicLP.sol

```solidity
68	    bool internal _INITIALIZED_;
...
70	    address public _BASE_TOKEN_;
...
71	    address public _QUOTE_TOKEN_;
...
72	    uint112 public _BASE_RESERVE_;
...
73	    uint112 public _QUOTE_RESERVE_;
...
74	    uint32 public _BLOCK_TIMESTAMP_LAST_;
...
75	    uint256 public _BASE_PRICE_CUMULATIVE_LAST_;
...
76	    uint112 public _BASE_TARGET_;
...
77	    uint112 public _QUOTE_TARGET_;
...
79	    IFeeRateModel public _MT_FEE_RATE_MODEL_;
```

*GitHub* : [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L68), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L70), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L71), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L75), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L79), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L80), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L81), [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L82), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L79), [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L199), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)


---

	 - src/mimswap/libraries/PMMPricing.sol


*GitHub* : [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L29), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L30), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L31), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L33), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L34), [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205)

### [N-12]<a name="n-12"></a> Consider using `delete` rather than assigning zero/false to clear values

The `delete` keyword more closely matches the semantics of what is being done, and draws more attention to the changing of state, which may lead to a more thorough audit of its associated logic

*There are 3 instance(s) of this issue:*


---

	 - src/mimswap/libraries/Math.sol

```solidity
154	                temp = 0;
...
176	            bSig = false;
```

*GitHub* : [154](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L154), [176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L176)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
619	            rewards[user][rewardToken] = 0;
```

*GitHub* : [619](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L619)

### [N-13]<a name="n-13"></a> Array is `push()`ed but not `pop()`ed

Array entries are added but are never removed. Consider whether this should be the case, or whether there should be a maximum, or whether old entries should be removed. Cases where there are specific potential problems will be flagged separately under a different issue.

*There are 5 instance(s) of this issue:*


---

	 - src/mimswap/periphery/Factory.sol

```solidity
149	        pools[baseToken][quoteToken].push(pool);
...
150	        userPools[creator].push(pool);
```

*GitHub* : [149](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L149), [150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L150)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
313	        rewardTokens.push(rewardToken);
...
501	            _userLocks[user].push(LockedBalance({amount: amount, unlockTime: _nextUnlockTime}));
...
648	                _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
```

*GitHub* : [313](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L313), [501](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L501), [648](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L648)

### [N-14]<a name="n-14"></a> Unused contract variables

Note that there may be cases where a variable appears to be used, but this is only because there are multiple definitions of the varible in different files. In such cases, the variable definition should be moved into a separate file. The instances below are the unused variables.

*There are 27 instance(s) of this issue:*


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
78	    function claimable(address user) external view returns (uint256 shares) {
...
86	    function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
86	    function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
86	    function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
155	    function _claimable(address user) internal view returns (uint256 shares) {
```

*GitHub* : [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L78), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L155)


---

	 - src/mimswap/MagicLP.sol

```solidity
215	    function getMidPrice() public view returns (uint256 midPrice) {
...
224	    function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
...
224	    function getUserFeeRate(address user) external view returns (uint256 lpFeeRate, uint256 mtFeeRate) {
...
228	    function getBaseInput() public view returns (uint256 input) {
...
232	    function getQuoteInput() public view returns (uint256 input) {
```

*GitHub* : [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L215), [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L224), [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L224), [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L228), [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L232)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34)


---

	 - src/mimswap/auxiliary/FeeRateModelImpl.sol


*GitHub* : [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L13)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L22), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L185), [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L235), [268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L268), [268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L268), [321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L321), [342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L342), [410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L410), [420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L420), [455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L455), [466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L466)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L34), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L34)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [69](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L69)

### [N-15]<a name="n-15"></a> `else`-block not required

One level of nesting can be removed by not having an `else` block when the `if`-block returns, and `if (foo) { return 1; } else { return 2; }` becomes `if (foo) { return 1; } return 2;`

*There are 5 instance(s) of this issue:*


---

	 - src/mimswap/libraries/DecimalMath.sol

```solidity
48	        if (e == 0) {
49	            return 10 ** 18;
50	        } else if (e == 1) {
51	            return target;
52	        } else {
53	            uint p = powFloor(target, e / 2);
54	            p = (p * p) / ONE;
55	            if (e % 2 == 1) {
56	                p = (p * target) / ONE;
57	            }
58	            return p;
59	        }
...
50	        } else if (e == 1) {
51	            return target;
52	        } else {
53	            uint p = powFloor(target, e / 2);
54	            p = (p * p) / ONE;
55	            if (e % 2 == 1) {
56	                p = (p * target) / ONE;
57	            }
58	            return p;
59	        }
```

*GitHub* : [48..59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L48-L59), [50..59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L50-L59)


---

	 - src/mimswap/libraries/Math.sol

```solidity
22	        if (remainder > 0) {
23	            return quotient + 1;
24	        } else {
25	            return quotient;
26	        }
...
200	        if (V2 > V1) {
201	            return 0;
202	        } else {
203	            return V1 - V2;
204	        }
```

*GitHub* : [22..26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L22-L26), [200..204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L200-L204)


---

	 - src/mimswap/libraries/PMMPricing.sol

```solidity
204	        if (state.R == RState.BELOW_ONE) {
205	            uint256 R = DecimalMath.divFloor((state.Q0 * state.Q0) / state.Q, state.Q);
206	            R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);
207	            return DecimalMath.divFloor(state.i, R);
208	        } else {
209	            uint256 R = DecimalMath.divFloor((state.B0 * state.B0) / state.B, state.B);
210	            R = (DecimalMath.ONE - state.K) + DecimalMath.mulFloor(state.K, R);
211	            return DecimalMath.mulFloor(state.i, R);
212	        }
```

*GitHub* : [204..212](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L204-L212)

### [N-16]<a name="n-16"></a> Remaining eth may not be refunded to users

 When a contract function accepts Ethereum and executes a `.call()` or similar function that also forwards Ethereum value, it's important to check for and refund any remaining balance. This is because some of the supplied value may not be used during the call execution due to gas constraints, a revert in the called contract, or simply because not all the value was needed.

If you do not account for this remaining balance, it can become "locked" in the contract. It's crucial to either return the remaining balance to the sender or handle it in a way that ensures it is not permanently stuck. Neglecting to do so can lead to loss of funds and degradation of the contract's reliability. Furthermore, it's good practice to ensure fairness and trust with your users by returning unused funds. 

*There are 7 instance(s) of this issue:*


---

	 - src/blast/BlastWrappers.sol

```solidity
59	    function init(bytes calldata data) public payable override {
```

*GitHub* : [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59)


---

	 - src/mimswap/periphery/Router.sol

```solidity
73	    function createPoolETH(
74	        address token,
75	        bool useTokenAsQuote,
76	        uint256 lpFeeRate,
77	        uint256 i,
78	        uint256 k,
79	        address to,
80	        uint256 tokenInAmount
81	    ) external payable returns (address clone, uint256 shares) {
...
192	    function addLiquidityETH(
193	        address lp,
194	        address to,
195	        address payable refundTo,
196	        uint256 tokenInAmount,
197	        uint256 minimumShares,
198	        uint256 deadline
199	    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
229	    function addLiquidityETHUnsafe(
230	        address lp,
231	        address to,
232	        uint256 tokenInAmount,
233	        uint256 minimumShares,
234	        uint256 deadline
235	    ) external payable ensureDeadline(deadline) returns (uint256 shares) {
...
336	    function swapETHForTokens(
337	        address to,
338	        address[] calldata path,
339	        uint256 directions,
340	        uint256 minimumOut,
341	        uint256 deadline
342	    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
...
415	    function sellBaseETHForTokens(
416	        address lp,
417	        address to,
418	        uint256 minimumOut,
419	        uint256 deadline
420	    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
...
461	    function sellQuoteETHForTokens(
462	        address lp,
463	        address to,
464	        uint256 minimumOut,
465	        uint256 deadline
466	    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
```

*GitHub* : [73..81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L73-L81), [192..199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192-L199), [229..235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229-L235), [336..342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336-L342), [415..420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L415-L420), [461..466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L461-L466)

### [N-17]<a name="n-17"></a> Condition will not revert when `block.timestamp` is `==` to the compared variable

The condition remains unaltered even if `block.timestamp` is equal to the compared `>` or `<` variable. For example, if there is a condition `block.timestamp > proposerSignature.expirationTimestamp`, it is necessary to also account for cases where `block.timestamp` is `==` to `proposerSignature.expirationTimestamp`.

*There are 3 instance(s) of this issue:*


---

	 - src/mimswap/MagicLP.sol

```solidity
421	        if (deadline < block.timestamp) {
422	            revert ErrExpired();
423	        }
```

*GitHub* : [421..423](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L421-L423)


---

	 - src/mimswap/periphery/Router.sol

```solidity
48	        if (block.timestamp > deadline) {
49	            revert ErrExpired();
50	        }
```

*GitHub* : [48..50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L48-L50)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
422	            if (locks[index].unlockTime > block.timestamp) {
423	                revert ErrLockNotExpired();
424	            }
```

*GitHub* : [422..424](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L422-L424)

### [N-18]<a name="n-18"></a> External calls in an un-bounded `for`-loop may result in a DOS

Consider limiting the number of iterations in `for`-loops that make external calls

*There are 8 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
165	        for (uint256 i = 0; i < tokens.length; i++) {
166	            if (!supportedTokens[tokens[i]]) {
167	                revert ErrUnsupportedToken();
168	            }
169	            if (registry.nativeYieldTokens(tokens[i])) {
170	                BlastYields.claimAllTokenYields(tokens[i], feeTo);
171	            }
172	        }
```

*GitHub* : [165..172](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165-L172)


---

	 - src/mimswap/periphery/Router.sol

```solidity
544	        for (uint256 i = 0; i < iterations; ) {
545	            if (directions & 1 == 0) {
546	                // Sell base
547	                IMagicLP(path[i]).sellBase(address(path[i + 1]));
548	            } else {
549	                // Sell quote
550	                IMagicLP(path[i]).sellQuote(address(path[i + 1]));
551	            }
552	
553	            directions >>= 1;
554	
555	            unchecked {
556	                ++i;
557	            }
558	        }
```

*GitHub* : [544..558](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544-L558)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
405	        for (uint256 i; i < users.length; ) {
406	            address user = users[i];
407	            Balances storage bal = _balances[user];
408	            LockedBalance[] storage locks = _userLocks[user];
409	
410	            if (locks.length == 0) {
411	                revert ErrNoLocks();
412	            }
413	
414	            uint256 index = lockIndexes[i];
415	
416	            // Prevents processing `lastLockIndex` out of order
417	            if (index == lastLockIndex[user] && locks.length > 1) {
418	                revert ErrInvalidLockIndex();
419	            }
420	
421	            // prohibit releasing non-expired locks
422	            if (locks[index].unlockTime > block.timestamp) {
423	                revert ErrLockNotExpired();
424	            }
425	
426	            uint256 amount = locks[index].amount;
427	            uint256 lastIndex = locks.length - 1;
428	
429	            /// Last lock index changed place with the one we just swapped.
430	            if (lastLockIndex[user] == lastIndex) {
431	                lastLockIndex[user] = index;
432	            }
433	
434	            if (index != lastIndex) {
435	                locks[index] = locks[lastIndex];
436	                emit LogLockIndexChanged(user, lastIndex, index);
437	            }
438	
439	            locks.pop();
440	
441	            unlockedSupply += amount;
442	            lockedSupply -= amount;
443	
444	            bal.unlocked += amount;
445	            bal.locked -= amount;
446	
447	            emit LogUnlocked(user, amount, index);
448	
449	            unchecked {
450	                ++i;
451	            }
452	        }
...
547	        for (uint256 i; i < rewardTokens.length; ) {
548	            _updateRewardsGlobal(rewardTokens[i], totalSupply_);
549	            unchecked {
550	                ++i;
551	            }
552	        }
...
561	        for (uint256 i; i < rewardTokens.length; ) {
562	            address token = rewardTokens[i];
563	            _udpateUserRewards(user, balance, token, _updateRewardsGlobal(token, totalSupply_));
564	
565	            unchecked {
566	                ++i;
567	            }
568	        }
...
575	        for (uint256 i; i < rewardTokens.length; ) {
576	            address token = rewardTokens[i];
577	            uint256 rewardPerToken_ = _updateRewardsGlobal(token, totalSupply_);
578	
579	            // Record each user's rewards
580	            for (uint256 j; j < users.length; ) {
581	                address user = users[j];
582	                _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);
583	
584	                unchecked {
585	                    ++j;
586	                }
587	            }
588	
589	            unchecked {
590	                ++i;
591	            }
592	        }
...
580	            for (uint256 j; j < users.length; ) {
581	                address user = users[j];
582	                _udpateUserRewards(user, balanceOf(user), token, rewardPerToken_);
583	
584	                unchecked {
585	                    ++j;
586	                }
587	            }
...
614	        for (uint256 i; i < rewardTokens.length; ) {
615	            address rewardToken = rewardTokens[i];
616	            uint256 rewardAmount = rewards[user][rewardToken];
617	
618	            // in all scenario, reset the reward amount immediately
619	            rewards[user][rewardToken] = 0;
620	
621	            // don't assume the rewardTokens array is always the same length as the items array
622	            // as new reward tokens can be added by the owner
623	            if (i < rewardItemLength) {
624	                RewardLockItem storage item = _rewardLock.items[i];
625	
626	                // expired lock, claim existing unlocked rewards if any
627	                if (expired) {
628	                    uint256 amount = item.amount;
629	
630	                    // since this current lock is expired and that item index
631	                    // matches the reward index, override the current amount
632	                    // with the new locked amount.
633	                    item.amount = rewardAmount;
634	
635	                    // use cached amount
636	                    if (amount > 0) {
637	                        rewardToken.safeTransfer(user, amount);
638	                        emit LogRewardPaid(user, rewardToken, amount);
639	                    }
640	                } else {
641	                    // not expired, just add to the existing lock
642	                    item.amount += rewardAmount;
643	                }
644	            }
645	            // new reward token, create a new lock item
646	            // could mean it's adding to an existing lock or creating a new one
647	            else {
648	                _userRewardLock[user].items.push(RewardLockItem({token: rewardToken, amount: rewardAmount}));
649	            }
650	
651	            emit LogRewardLocked(user, rewardToken, rewardAmount);
652	
653	            unchecked {
654	                ++i;
655	            }
656	        }
```

*GitHub* : [405..452](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L405-L452), [547..552](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L547-L552), [561..568](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L561-L568), [575..592](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L575-L592), [580..587](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L580-L587), [614..656](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L614-L656)

### [N-19]<a name="n-19"></a> `constructor` missing zero address check

It is important to ensure that the constructor does not allow zero address to be set.
    This is a common mistake that can lead to loss of funds or redeployment of the contract.

*There are 11 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
24	    constructor(IERC20 weth_, BlastTokenRegistry registry_, address feeTo_) DegenBox(weth_) {
```

*GitHub* : [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L24)


---

	 - src/blast/BlastGovernor.sol

```solidity
15	    constructor(address feeTo_, address _owner) OperatableV2(_owner) {
```

*GitHub* : [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L15)


---

	 - src/blast/BlastMagicLP.sol

```solidity
23	    constructor(BlastTokenRegistry registry_, address feeTo_, address owner_) MagicLP(owner_) {
```

*GitHub* : [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L23)


---

	 - src/blast/BlastWrappers.sol

```solidity
20	    constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
...
29	    constructor(
30	        address implementation_,
31	        IFeeRateModel maintainerFeeRateModel_,
32	        address owner_,
33	        address governor_
34	    ) Factory(implementation_, maintainerFeeRateModel_, owner_) {
...
47	    constructor(address box_, address mim_, address governor_) CauldronV4(IBentoBoxV1(box_), IERC20(mim_)) {
```

*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L20), [29..34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L29-L34), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L47)


---

	 - src/mimswap/MagicLP.sol

```solidity
84	    constructor(address owner_) Owned(owner_) {
```

*GitHub* : [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L84)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol

```solidity
22	    constructor(address maintainer_, address owner_) Owned(owner_) {
```

*GitHub* : [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L22)


---

	 - src/mimswap/periphery/Factory.sol

```solidity
38	    constructor(address implementation_, IFeeRateModel maintainerFeeRateModel_, address owner_) Owned(owner_) {
```

*GitHub* : [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L38)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol

```solidity
21	    constructor(IMagicLP pair_, IAggregator baseOracle_, IAggregator quoteOracle_) {
```

*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L21)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [112..118](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L112-L118)

### [N-20]<a name="n-20"></a> Variable initialization with default value

It's not necessary to initialize a variable with its default value, and it's actually worse in gas terms as it adds an overhead.

*There are 2 instance(s) of this issue:*


---

	 - src/blast/BlastOnboarding.sol

```solidity
165	        for (uint256 i = 0; i < tokens.length; i++) {
```

*GitHub* : [165](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L165)


---

	 - src/mimswap/periphery/Router.sol

```solidity
544	        for (uint256 i = 0; i < iterations; ) {
```

*GitHub* : [544](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L544)

### [N-21]<a name="n-21"></a> Complex math should be split into multiple steps

Consider splitting long arithmetic calculations into multiple steps to improve the code readability.

*There are 21 instance(s) of this issue:*


---

	 - src/mimswap/libraries/Math.sol

```solidity
34	            z = (x / z + z) / 2;
...
64	        return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;
...
64	        return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;
...
64	        return (((DecimalMath.ONE - k) + penalty) * fairAmount) / DecimalMath.ONE2;
...
99	            _sqrt = sqrt(((ki / V1) * delta) + DecimalMath.ONE2);
...
97	            _sqrt = sqrt(((ki * delta) / V1) + DecimalMath.ONE2);
...
158	                temp = (((delta * V1) / V0) * i) / V0;
...
158	                temp = (((delta * V1) / V0) * i) / V0;
...
158	                temp = (((delta * V1) / V0) * i) / V0;
...
170	        uint256 part2 = (((k * V0) / V1) * V0) + (i * delta); // kQ0^2/Q1-i*deltaB
```

*GitHub* : [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L34), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L64), [99](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L99), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L97), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158), [158](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L158), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L170)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L38), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L39), [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L43), [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L44), [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L236), [241](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L241), [283](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L283), [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L294)

### [N-22]<a name="n-22"></a> Duplicated `require/if` statements should be refactored

These statements should be refactored to a separate function, as there are multiple parts of the codebase that use the same logic, to improve the code readability and reduce code duplication.



*There are 69 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
25	        if (feeTo_ == address(0)) {
...
73	        if (feeTo_ == address(0)) {
```

*GitHub* : [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L25), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L73)


---

	 - src/blast/BlastMagicLP.sol

```solidity
56	        if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
...
59	        if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
...
81	        if (feeTo_ == address(0)) {
...
105	        if (registry.nativeYieldTokens(_BASE_TOKEN_)) {
...
109	        if (registry.nativeYieldTokens(_QUOTE_TOKEN_)) {
...
24	        if (feeTo_ == address(0)) {
```

*GitHub* : [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L56), [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L59), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L81), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L105), [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L109), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L24)


---

	 - src/blast/BlastOnboarding.sol

```solidity
89	        if (feeTo_ == address(0)) {
...
148	        if (feeTo_ == address(0)) {
```

*GitHub* : [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L89), [148](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L148), [169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L169), [178](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L178)


---

	 - src/blast/BlastWrappers.sol


*GitHub* : [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L35), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L48), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L51), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L21)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [256](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L256), [279](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L279), [294](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L294), [320](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L320), [342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L342), [450](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L450), [508](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L508), [512](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L512), [516](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L516), [532](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L532), [571](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L571), [574](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L574), [582](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L582), [588](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L588)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L47), [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L23)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L52), [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L58), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L80), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L132), [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L140)


---

	 - src/mimswap/libraries/PMMPricing.sol


*GitHub* : [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L45), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L77), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L80), [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L191), [193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L193), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L204), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L40)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L39), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L42), [97](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L97), [106](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L106)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [285](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L285), [295](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L295), [327](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L327), [348](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L348), [392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L392), [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L439), [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L545), [566](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L566), [573](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L573), [581](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L581), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L105), [142](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L142), [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L203), [208](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L208), [237](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L237), [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L239)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L459), [609](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L609), [627](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L627), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L156), [171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L171)

### [N-23]<a name="n-23"></a> Variable names don't follow the Solidity naming convention

Use `mixedCase` for local and state variables that are not constants, and add a trailing underscore for internal variables. [Documentation](https://docs.soliditylang.org/en/latest/style-guide.html#local-and-state-variable-names)

*There are 38 instance(s) of this issue:*


---

	 - src/blast/BlastMagicLP.sol

```solidity
48	        address feeTo_ = BlastMagicLP(address(implementation)).feeTo();
...
54	        address feeTo_ = BlastMagicLP(address(implementation)).feeTo();
```

*GitHub* : [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L48), [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L54)


---

	 - src/blast/BlastWrappers.sol

```solidity
45	    address private immutable _governor;
```

*GitHub* : [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L45)


---

	 - src/mimswap/MagicLP.sol

```solidity
68	    bool internal _INITIALIZED_;
...
70	    address public _BASE_TOKEN_;
...
71	    address public _QUOTE_TOKEN_;
...
72	    uint112 public _BASE_RESERVE_;
...
73	    uint112 public _QUOTE_RESERVE_;
...
74	    uint32 public _BLOCK_TIMESTAMP_LAST_;
...
75	    uint256 public _BASE_PRICE_CUMULATIVE_LAST_;
```

*GitHub* : [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L68), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L70), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L71), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L75), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L78), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L79), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L80), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L81), [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L82)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L62), [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L92), [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L199)


---

	 - src/mimswap/libraries/PMMPricing.sol


*GitHub* : [209](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L209), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L205)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [127](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L127), [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L129)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L89), [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L90), [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L91), [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L92), [371](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L371), [372](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L372), [481](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L481), [482](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L482), [529](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L529), [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L545), [559](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L559), [573](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L573), [577](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L577), [598](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L598)

### [N-24]<a name="n-24"></a> Contract functions should use an `interface`

All `external`/`public` functions should extend an `interface`. This is useful to make sure that the whole API is extracted.

*There are 124 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
52	    function claimGasYields() external onlyOperators returns (uint256) {
...
56	    function claimTokenYields(address token_) external onlyOperators returns (uint256 amount) {
...
68	    function callBlastPrecompile(bytes calldata data) external onlyOwner {
...
72	    function setFeeTo(address feeTo_) external onlyOwner {
...
81	    function setTokenEnabled(address token, bool enabled) external onlyOwner {
```

*GitHub* : [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L52), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L56), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L68), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81)


---

	 - src/blast/BlastGovernor.sol

```solidity
28	    function claimNativeYields(address contractAddress) external onlyOperators returns (uint256) {
...
32	    function claimMaxGasYields(address contractAddress) external onlyOperators returns (uint256) {
...
40	    function setFeeTo(address _feeTo) external onlyOwner {
...
49	    function callBlastPrecompile(bytes calldata data) external onlyOwner {
...
53	    function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

*GitHub* : [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L28), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L32), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40), [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L49), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)


---

	 - src/blast/BlastMagicLP.sol


*GitHub* : [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L47), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L53), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L64), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L72), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89)


---

	 - src/blast/BlastOnboarding.sol


*GitHub* : [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101), [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132), [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L156), [160](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L160), [164](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L164), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190), [195](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L195), [200](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L200), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L205), [214](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L214), [218](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L218)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L55), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L78), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96), [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129), [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [91..98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L91-L98), [134](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L134), [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L138), [167..170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L167-L170), [180..183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L180-L183), [193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L193), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204), [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L215), [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L219), [224](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L224), [228](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L228), [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L232), [236](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L236), [244](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L244), [267](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L267), [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290), [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360), [413..420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L413-L420), [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L461), [470..479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470-L479), [504](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L504)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34), [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)


---

	 - src/mimswap/auxiliary/FeeRateModelImpl.sol


*GitHub* : [9..13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L9-L13)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L53), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L57), [65..72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65-L72), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105), [116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L116), [120..126](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L120-L126)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [54..63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L54-L63), [73..81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L73-L81), [96..100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L96-L100), [112..116](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L112-L116), [162..169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L162-L169), [178..185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L178-L185), [192..199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192-L199), [229..235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229-L235), [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L251), [261..268](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L261-L268), [274..281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L274-L281), [314..321](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L314-L321), [336..342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336-L342), [365..372](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L365-L372), [404..410](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L404-L410), [415..420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L415-L420), [432..438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L432-L438), [449..455](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L449-L455), [461..466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L461-L466), [478..484](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L478-L484)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [150](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L150), [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L155), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L170), [186](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L186), [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L191), [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L199), [203](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L203), [207](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L207), [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L211), [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L215), [219](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L219), [223](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L223), [227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L227), [231](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L231), [235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L235), [239](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L239), [253](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L253), [257](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L257), [261](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L261), [265](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L265), [269](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L269), [273](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L273), [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277), [288](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L288), [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300), [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317), [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L324), [337](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L337), [341](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L341), [349](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L349), [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361), [397](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L397)

### [N-25]<a name="n-25"></a> Custom `error` without details

Consider adding some parameters to the error to indicate which user or values caused the failure.

*There are 78 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
17	    error ErrZeroAddress();
...
18	    error ErrUnsupportedToken();
```

*GitHub* : [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L17), [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L18)


---

	 - src/blast/BlastGovernor.sol

```solidity
9	    error ErrZeroAddress();
```

*GitHub* : [9](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L9)


---

	 - src/blast/BlastMagicLP.sol

```solidity
15	    error ErrNotAllowedImplementationOperator();
```

*GitHub* : [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L15)


---

	 - src/blast/BlastOnboarding.sol

```solidity
13	    error ErrZeroAddress();
...
14	    error ErrWrongState();
...
15	    error ErrUnsupportedToken();
...
16	    error ErrNotAllowed();
...
77	    error ErrUnsupported();
...
78	    error ErrCapReached();
```

*GitHub* : [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L13), [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L14), [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L15), [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L16), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L77), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L78)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L43), [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L44), [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L45), [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L46), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L47), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L48), [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L49)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L8)


---

	 - src/blast/BlastWrappers.sol


*GitHub* : [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L17), [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L43)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L38), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L39), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L40), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L41), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L42), [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L43), [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L44), [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L45), [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L46), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L47), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L48), [49](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L49), [50](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L50), [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L51), [52](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L52), [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L53), [54](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L54), [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L55), [56](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L56), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L57), [58](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L58), [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L59)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L17)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L17)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L29), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L30)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L16), [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L17), [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L18), [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L19), [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L21), [23](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L23), [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L24), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L26), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L27), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L28), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L29)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L30), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L31), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L33), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L34), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L35), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L36), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L37), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L38), [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L39), [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L40), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L41), [42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L42), [43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L43), [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L44), [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L45), [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L46), [47](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L47), [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L48)

### [N-26]<a name="n-26"></a> State variables should include comments

Consider adding some comments on critical state variables to explain what they are supposed to do: this will help for future code reviews.

*There are 83 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
20	    BlastTokenRegistry public immutable registry;
...
21	    mapping(address => bool) public enabledTokens;
...
22	    address public feeTo;
```

*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L21), [22](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L22)


---

	 - src/blast/BlastGovernor.sol

```solidity
11	    address public feeTo;
```

*GitHub* : [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L11)


---

	 - src/blast/BlastMagicLP.sol

```solidity
17	    BlastTokenRegistry public immutable registry;
...
21	    mapping(address => bool) public operators;
```

*GitHub* : [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L17), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L21)


---

	 - src/blast/BlastOnboarding.sol

```solidity
30	    State public state;
...
31	    address public bootstrapper;
...
32	    address public feeTo;
...
33	    BlastTokenRegistry public registry;
```

*GitHub* : [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L30), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L31), [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L33), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L36), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L37), [38](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L38), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L41)


---

	 - src/blast/BlastOnboardingBoot.sol


*GitHub* : [24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L24), [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L26), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L27), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L28), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L29), [30](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L30)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L10)


---

	 - src/blast/BlastWrappers.sol


*GitHub* : [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L45)


---

	 - src/blast/libraries/BlastPoints.sol


*GitHub* : [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L7), [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L8)


---

	 - src/blast/libraries/BlastYields.sol


*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L14)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L61), [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64), [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L65), [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L66), [68](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L68), [70](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L70), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L71), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L72), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L74), [75](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L75), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L76), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L77), [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L78), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L79), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L80), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L81), [82](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L82)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L19), [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L20)


---

	 - src/mimswap/libraries/DecimalMath.sol


*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L21)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L32), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L33), [35](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L35), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L36)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L31), [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L33), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L34)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L10), [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L11), [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L12), [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L13), [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L14), [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L16)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L78), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L79), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L80), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L81), [83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L83), [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L84), [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L85), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L86), [87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L87), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L89), [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L90), [91](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L91), [92](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L92), [94](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L94), [95](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L95), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L96), [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L98), [100](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L100), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L101), [102](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L102), [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L103)

### [N-27]<a name="n-27"></a> Events that mark critical parameter changes should contain both the old and the new value

This should especially be done if the new value is not required to be different from the old value

*There are 20 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
15	    event LogFeeToChanged(address indexed feeTo);
```

*GitHub* : [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L15)


---

	 - src/blast/BlastGovernor.sol

```solidity
8	    event LogFeeToChanged(address indexed feeTo);
```

*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L8)


---

	 - src/blast/BlastMagicLP.sol

```solidity
11	    event LogFeeToChanged(address indexed feeTo);
...
12	    event LogOperatorChanged(address indexed, bool);
```

*GitHub* : [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L11), [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L12)


---

	 - src/blast/BlastOnboarding.sol

```solidity
67	    event LogBootstrapperChanged(address indexed bootstrapper);
...
71	    event LogFeeToChanged(address indexed feeTo);
...
73	    event LogTokenCapChanged(address indexed token, uint256 cap);
...
74	    event LogStateChange(State state);
```

*GitHub* : [67](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L67), [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L71), [73](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L73), [74](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L74)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
37	    event LogReadyChanged(bool ready);
...
41	    event LogStakingChanged(address indexed staking);
```

*GitHub* : [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L37), [41](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L41)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L34), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L36)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L14), [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L15)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [25](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L25), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L26), [27](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L27)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L21), [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L26), [28](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L28)

### [N-28]<a name="n-28"></a> Constant redefined elsewhere

Consider defining in only one contract so that values cannot become out of sync when only one location is updated. A [cheap way](https://medium.com/coinmonks/gas-cost-of-solidity-library-functions-dbe0cedd4678) to store constants in a single location is to create an `internal constant` in a `library`. If the variable is a local cache of another contract's value, consider making the cache variable internal or private, which will require external users to query the contract with the source of truth, so that callers don't get out of sync.

*There are 2 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
// @audit Variable redefined in: file `src/blast/BlastBox.sol`: `registry`, file `src/blast/BlastMagicLP.sol`: `registry`
20	    BlastTokenRegistry public immutable registry;
```

*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L20)


---

	 - src/blast/BlastMagicLP.sol

```solidity
// @audit Variable redefined in: file `src/blast/BlastBox.sol`: `registry`, file `src/blast/BlastMagicLP.sol`: `registry`
17	    BlastTokenRegistry public immutable registry;
```

*GitHub* : [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L17)

### [N-29]<a name="n-29"></a> Function ordering does not follow the Solidity style guide

According to the [Solidity style guide](https://docs.soliditylang.org/en/v0.8.17/style-guide.html#order-of-functions), functions should be laid out in the following order :`constructor()`, `receive()`, `fallback()`, `external`, `public`, `internal`, `private`, but the cases below do not follow this pattern

*There are 12 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
// @audit function `_onBeforeDeposit` is `internal` followed by function `claimGasYields` which is `external`
36	    function _onBeforeDeposit(
37	        IERC20 token,
38	        address /*from*/,
39	        address /*to*/,
40	        uint256 /*amount*/,
41	        uint256 /*share*/
42	    ) internal view override {
```

*GitHub* : [36..42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L36-L42)


---

	 - src/mimswap/MagicLP.sol

```solidity
// @audit function `getPMMState` is `public` followed by function `getPMMStateForCall` which is `external`
193	    function getPMMState() public view returns (PMMPricing.PMMState memory state) {
...
// @audit function `getMidPrice` is `public` followed by function `getReserves` which is `external`
215	    function getMidPrice() public view returns (uint256 midPrice) {
...
// @audit function `getQuoteInput` is `public` followed by function `version` which is `external`
232	    function getQuoteInput() public view returns (uint256 input) {
...
// @audit function `setParameters` is `public` followed by function `ratioSync` which is `external`
470	    function setParameters(
471	        address assetTo,
472	        uint256 newLpFeeRate,
473	        uint256 newI,
474	        uint256 newK,
475	        uint256 baseOutAmount,
476	        uint256 quoteOutAmount,
477	        uint256 minBaseReserve,
478	        uint256 minQuoteReserve
479	    ) public nonReentrant onlyImplementationOwner {
```

*GitHub* : [193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L193), [215](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L215), [232](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L232), [470..479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470-L479)


---

	 - src/mimswap/periphery/Factory.sol

```solidity
// @audit function `predictDeterministicAddress` is `public` followed by function `create` which is `external`
65	    function predictDeterministicAddress(
66	        address creator,
67	        address baseToken_,
68	        address quoteToken_,
69	        uint256 lpFeeRate_,
70	        uint256 i_,
71	        uint256 k_
72	    ) public view returns (address) {
```

*GitHub* : [65..72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L65-L72)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol

```solidity
// @audit function `_getReserves` is `internal` followed by function `latestAnswer` which is `public`
33	    function _getReserves() internal view virtual returns (uint256, uint256) {
...
// @audit function `latestAnswer` is `public` followed by function `latestRoundData` which is `external`
37	    function latestAnswer() public view override returns (int256) {
```

*GitHub* : [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L33), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L37)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
// @audit function `getRewards` is `public` followed by function `rewardData` which is `external`
191	    function getRewards() public virtual {
...
// @audit function `_earned` is `internal` followed by function `addReward` which is `public`
292	    function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {
```

*GitHub* : [191](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L191), [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L292), [300](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L300), [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361)

### [N-30]<a name="n-30"></a> Array indicies should be referenced via `enum`s rather than via numeric literals



*There are 3 instance(s) of this issue:*


---

	 - src/mimswap/periphery/Router.sol

```solidity
324	        address firstLp = path[0];
...
345	        address firstLp = path[0];
...
389	        address firstLp = path[0];
```

*GitHub* : [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L324), [345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L345), [389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L389)

### [N-31]<a name="n-31"></a> Use of `override` is unnecessary

Starting with Solidity version [0.8.8](https://docs.soliditylang.org/en/v0.8.20/contracts.html#function-overriding), using the `override` keyword when the function solely overrides an interface function, and the function doesn't exist in multiple base contracts, is unnecessary.

*There are 13 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
36	    function _onBeforeDeposit(
37	        IERC20 token,
38	        address /*from*/,
39	        address /*to*/,
40	        uint256 /*amount*/,
41	        uint256 /*share*/
42	    ) internal view override {
...
98	    function _configure() internal override {
...
103	    function isOwner(address _account) internal view override returns (bool) {
```

*GitHub* : [36..42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L36-L42), [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L98), [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L103)


---

	 - src/blast/BlastMagicLP.sol

```solidity
39	    function version() external pure override returns (string memory) {
...
98	    function _afterInitialized() internal override {
```

*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L39), [98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L98)


---

	 - src/blast/BlastOnboarding.sol

```solidity
226	    function _implementation() internal view override returns (address) {
```

*GitHub* : [226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L226)


---

	 - src/blast/BlastWrappers.sol

```solidity
59	    function init(bytes calldata data) public payable override {
```

*GitHub* : [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59)


---

	 - src/mimswap/MagicLP.sol

```solidity
155	    function name() public view override returns (string memory) {
...
159	    function symbol() public pure override returns (string memory) {
...
163	    function decimals() public view override returns (uint8) {
```

*GitHub* : [155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L155), [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L159), [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163), [593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L593)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L29), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L37)

### [N-32]<a name="n-32"></a> Unused function parameter

Comment out the variable name to suppress compiler warnings

*There are 13 instance(s) of this issue:*


---

	 - src/mimswap/periphery/Router.sol

```solidity
162	    function addLiquidity(
163	        address lp,
164	        address to,
165	        uint256 baseInAmount,
166	        uint256 quoteInAmount,
167	        uint256 minimumShares,
168	        uint256 deadline
169	    ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
170	        (baseAdjustedInAmount, quoteAdjustedInAmount) = _adjustAddLiquidity(lp, baseInAmount, quoteInAmount);
171	
172	        IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseAdjustedInAmount);
173	        IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteAdjustedInAmount);
174	
175	        shares = _addLiquidity(lp, to, minimumShares);
176	    }
...
178	    function addLiquidityUnsafe(
179	        address lp,
180	        address to,
181	        uint256 baseInAmount,
182	        uint256 quoteInAmount,
183	        uint256 minimumShares,
184	        uint256 deadline
185	    ) external ensureDeadline(deadline) returns (uint256 shares) {
186	        IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, baseInAmount);
187	        IMagicLP(lp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, lp, quoteInAmount);
188	
189	        return _addLiquidity(lp, to, minimumShares);
190	    }
...
192	    function addLiquidityETH(
193	        address lp,
194	        address to,
195	        address payable refundTo,
196	        uint256 tokenInAmount,
197	        uint256 minimumShares,
198	        uint256 deadline
199	    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
200	        uint256 wethAdjustedAmount;
201	        uint256 tokenAdjustedAmount;
202	        address token = IMagicLP(lp)._BASE_TOKEN_();
203	        if (token == address(weth)) {
204	            token = IMagicLP(lp)._QUOTE_TOKEN_();
205	            (baseAdjustedInAmount, quoteAdjustedInAmount) = _adjustAddLiquidity(lp, msg.value, tokenInAmount);
206	            wethAdjustedAmount = baseAdjustedInAmount;
207	            tokenAdjustedAmount = quoteAdjustedInAmount;
208	        } else if (IMagicLP(lp)._QUOTE_TOKEN_() == address(weth)) {
209	            (baseAdjustedInAmount, quoteAdjustedInAmount) = _adjustAddLiquidity(lp, tokenInAmount, msg.value);
210	            wethAdjustedAmount = quoteAdjustedInAmount;
211	            tokenAdjustedAmount = baseAdjustedInAmount;
212	        } else {
213	            revert ErrNotETHLP();
214	        }
215	
216	        weth.deposit{value: wethAdjustedAmount}();
217	        address(weth).safeTransfer(lp, wethAdjustedAmount);
218	
219	        // Refund unused ETH
220	        if (msg.value > wethAdjustedAmount) {
221	            refundTo.safeTransferETH(msg.value - wethAdjustedAmount);
222	        }
223	
224	        token.safeTransferFrom(msg.sender, lp, tokenAdjustedAmount);
225	
226	        shares = _addLiquidity(lp, to, minimumShares);
227	    }
...
229	    function addLiquidityETHUnsafe(
230	        address lp,
231	        address to,
232	        uint256 tokenInAmount,
233	        uint256 minimumShares,
234	        uint256 deadline
235	    ) external payable ensureDeadline(deadline) returns (uint256 shares) {
236	        address token = IMagicLP(lp)._BASE_TOKEN_();
237	        if (token == address(weth)) {
238	            token = IMagicLP(lp)._QUOTE_TOKEN_();
239	        } else if (IMagicLP(lp)._QUOTE_TOKEN_() != address(weth)) {
240	            revert ErrNotETHLP();
241	        }
242	
243	        weth.deposit{value: msg.value}();
244	        address(weth).safeTransfer(lp, msg.value);
245	
246	        token.safeTransferFrom(msg.sender, lp, tokenInAmount);
247	
248	        return _addLiquidity(lp, to, minimumShares);
249	    }
...
314	    function swapTokensForTokens(
315	        address to,
316	        uint256 amountIn,
317	        address[] calldata path,
318	        uint256 directions,
319	        uint256 minimumOut,
320	        uint256 deadline
321	    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
322	        _validatePath(path);
323	
324	        address firstLp = path[0];
325	
326	        // Transfer to the first LP
327	        if (directions & 1 == 0) {
328	            IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
329	        } else {
330	            IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, address(firstLp), amountIn);
331	        }
332	
333	        return _swap(to, path, directions, minimumOut);
334	    }
...
336	    function swapETHForTokens(
337	        address to,
338	        address[] calldata path,
339	        uint256 directions,
340	        uint256 minimumOut,
341	        uint256 deadline
342	    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
343	        _validatePath(path);
344	
345	        address firstLp = path[0];
346	        address inToken;
347	
348	        if (directions & 1 == 0) {
349	            inToken = IMagicLP(firstLp)._BASE_TOKEN_();
350	        } else {
351	            inToken = IMagicLP(firstLp)._QUOTE_TOKEN_();
352	        }
353	
354	        // Transfer to the first LP
355	        if (inToken != address(weth)) {
356	            revert ErrInTokenNotETH();
357	        }
358	
359	        weth.deposit{value: msg.value}();
360	        inToken.safeTransfer(address(firstLp), msg.value);
361	
362	        return _swap(to, path, directions, minimumOut);
363	    }
...
365	    function swapTokensForETH(
366	        address to,
367	        uint256 amountIn,
368	        address[] calldata path,
369	        uint256 directions,
370	        uint256 minimumOut,
371	        uint256 deadline
372	    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
373	        _validatePath(path);
374	
375	        uint256 lastLpIndex = path.length - 1;
376	        address lastLp = path[lastLpIndex];
377	        address outToken;
378	
379	        if ((directions >> lastLpIndex) & 1 == 0) {
380	            outToken = IMagicLP(lastLp)._QUOTE_TOKEN_();
381	        } else {
382	            outToken = IMagicLP(lastLp)._BASE_TOKEN_();
383	        }
384	
385	        if (outToken != address(weth)) {
386	            revert ErrOutTokenNotETH();
387	        }
388	
389	        address firstLp = path[0];
390	
391	        // Transfer to the first LP
392	        if (directions & 1 == 0) {
393	            IMagicLP(firstLp)._BASE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
394	        } else {
395	            IMagicLP(firstLp)._QUOTE_TOKEN_().safeTransferFrom(msg.sender, firstLp, amountIn);
396	        }
397	
398	        amountOut = _swap(address(this), path, directions, minimumOut);
399	        weth.withdraw(amountOut);
400	
401	        to.safeTransferETH(amountOut);
402	    }
...
404	    function sellBaseTokensForTokens(
405	        address lp,
406	        address to,
407	        uint256 amountIn,
408	        uint256 minimumOut,
409	        uint256 deadline
410	    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
411	        IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
412	        return _sellBase(lp, to, minimumOut);
413	    }
...
415	    function sellBaseETHForTokens(
416	        address lp,
417	        address to,
418	        uint256 minimumOut,
419	        uint256 deadline
420	    ) external payable ensureDeadline(deadline) returns (uint256 amountOut) {
421	        address baseToken = IMagicLP(lp)._BASE_TOKEN_();
422	
423	        if (baseToken != address(weth)) {
424	            revert ErrInvalidBaseToken();
425	        }
426	
427	        weth.deposit{value: msg.value}();
428	        baseToken.safeTransfer(lp, msg.value);
429	        return _sellBase(lp, to, minimumOut);
430	    }
...
432	    function sellBaseTokensForETH(
433	        address lp,
434	        address to,
435	        uint256 amountIn,
436	        uint256 minimumOut,
437	        uint256 deadline
438	    ) external ensureDeadline(deadline) returns (uint256 amountOut) {
439	        if (IMagicLP(lp)._QUOTE_TOKEN_() != address(weth)) {
440	            revert ErrInvalidQuoteToken();
441	        }
442	
443	        IMagicLP(lp)._BASE_TOKEN_().safeTransferFrom(msg.sender, lp, amountIn);
444	        amountOut = _sellBase(lp, address(this), minimumOut);
445	        weth.withdraw(amountOut);
446	        to.safeTransferETH(amountOut);
447	    }
```

*GitHub* : [162..176](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L162-L176), [178..190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L178-L190), [192..227](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192-L227), [229..249](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229-L249), [314..334](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L314-L334), [336..363](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336-L363), [365..402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L365-L402), [404..413](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L404-L413), [415..430](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L415-L430), [432..447](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L432-L447), [449..459](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L449-L459), [461..476](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L461-L476), [478..493](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L478-L493)

### [N-33]<a name="n-33"></a> Unused `event` definition

Note that there may be cases where an event superficially appears to be used, but this is only because there are multiple definitions of the event in different files. In such cases, the event definition should be moved into a separate file. The instances below are the unused definitions

*There are 3 instance(s) of this issue:*


---

	 - src/blast/BlastMagicLP.sol

```solidity
13	    event LogYieldClaimed(uint256 gasAmount, uint256 nativeAmount, uint256 token0Amount, uint256 token1Amount);
```

*GitHub* : [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L13)


---

	 - src/mimswap/periphery/Factory.sol

```solidity
26	    event LogSetMaintainer(address indexed newMaintainer);
```

*GitHub* : [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L26)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
26	    event LogRewardsDurationUpdated(address token, uint256 newDuration);
```

*GitHub* : [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L26)

### [N-34]<a name="n-34"></a> Function names should use lowerCamelCase

According to the Solidity [style guide](https://docs.soliditylang.org/en/latest/style-guide.html#function-names) function names should be in `mixedCase` (lowerCamelCase)

*There are 22 instance(s) of this issue:*


---

	 - src/mimswap/MagicLP.sol

```solidity
138	    function correctRState() external {
...
193	    function getPMMState() public view returns (PMMPricing.PMMState memory state) {
...
204	    function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
```

*GitHub* : [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L138), [193](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L193), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204)


---

	 - src/mimswap/libraries/Math.sol

```solidity
51	    function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {
...
79	    function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
...
131	    function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
```

*GitHub* : [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L79), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131)


---

	 - src/mimswap/libraries/PMMPricing.sol

```solidity
104	    function _ROneSellBaseToken(
105	        PMMState memory state,
106	        uint256 payBaseAmount
107	    )
108	        internal
109	        pure
110	        returns (
111	            uint256 // receiveQuoteToken
112	        )
113	    {
...
119	    function _ROneSellQuoteToken(
120	        PMMState memory state,
121	        uint256 payQuoteAmount
122	    )
123	        internal
124	        pure
125	        returns (
126	            uint256 // receiveBaseToken
127	        )
128	    {
...
134	    function _RBelowSellQuoteToken(
135	        PMMState memory state,
136	        uint256 payQuoteAmount
137	    )
138	        internal
139	        pure
140	        returns (
141	            uint256 // receiveBaseToken
142	        )
143	    {
...
147	    function _RBelowSellBaseToken(
148	        PMMState memory state,
149	        uint256 payBaseAmount
150	    )
151	        internal
152	        pure
153	        returns (
154	            uint256 // receiveQuoteToken
155	        )
156	    {
```

*GitHub* : [104..113](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L104-L113), [119..128](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L119-L128), [134..143](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L134-L143), [147..156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L147-L156), [162..171](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L162-L171), [175..184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L175-L184)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [73..81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L73-L81), [192..199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L192-L199), [229..235](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L229-L235), [274..281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L274-L281), [336..342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L336-L342), [365..372](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L365-L372), [415..420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L415-L420), [432..438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L432-L438), [461..466](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L461-L466), [478..484](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L478-L484)

### [N-35]<a name="n-35"></a> Overflows in unchecked blocks

While integers with a large number of bits are unlikely to overflow on human time scales, it is not strictly correct to use an `unchecked` block around them, because _eventually_ they will overflow, and `unchecked` blocks are meant for cases where it's mathematically impossible for an operation to trigger an overflow (e.g. a prior `require()` statement prevents the overflow case)

*There are 9 instance(s) of this issue:*


---

	 - src/mimswap/MagicLP.sol

```solidity
552	            unchecked {
553	                _BASE_PRICE_CUMULATIVE_LAST_ += getMidPrice() * timeElapsed;
554	            }
```

*GitHub* : [552..554](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L552-L554)


---

	 - src/mimswap/periphery/Router.sol

```solidity
555	            unchecked {
556	                ++i;
557	            }
```

*GitHub* : [555..557](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L555-L557)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
449	            unchecked {
450	                ++i;
451	            }
...
504	            unchecked {
505	                ++lockCount;
506	            }
...
549	            unchecked {
550	                ++i;
551	            }
...
565	            unchecked {
566	                ++i;
567	            }
...
584	                unchecked {
585	                    ++j;
586	                }
...
589	            unchecked {
590	                ++i;
591	            }
...
653	            unchecked {
654	                ++i;
655	            }
```

*GitHub* : [449..451](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L449-L451), [504..506](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L504-L506), [549..551](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L549-L551), [565..567](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L565-L567), [584..586](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L584-L586), [589..591](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L589-L591), [653..655](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L653-L655)

### [N-36]<a name="n-36"></a> Missing event and or timelock for critical parameter change

Events help non-contract tools to track changes, and timelocks prevent users from being surprised by changes

*There are 21 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
72	    function setFeeTo(address feeTo_) external onlyOwner {
...
81	    function setTokenEnabled(address token, bool enabled) external onlyOwner {
```

*GitHub* : [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81)


---

	 - src/blast/BlastGovernor.sol

```solidity
40	    function setFeeTo(address _feeTo) external onlyOwner {
```

*GitHub* : [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40)


---

	 - src/blast/BlastMagicLP.sol

```solidity
80	    function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
...
89	    function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```

*GitHub* : [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89)


---

	 - src/blast/BlastOnboarding.sol

```solidity
147	    function setFeeTo(address feeTo_) external onlyOwner {
...
175	    function setTokenSupported(address token, bool supported) external onlyOwner {
...
185	    function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
...
190	    function setBootstrapper(address bootstrapper_) external onlyOwner {
```

*GitHub* : [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
137	    function setStaking(LockingMultiRewards _staking) external onlyOwner {
```

*GitHub* : [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [470..479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470-L479), [528](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L528), [545](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L545), [560](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L560)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317)

### [N-37]<a name="n-37"></a> Setters should prevent re-setting of the same value

This especially problematic when the setter also emits the same value, which may be confusing to offline parsers

*There are 21 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
72	    function setFeeTo(address feeTo_) external onlyOwner {
...
81	    function setTokenEnabled(address token, bool enabled) external onlyOwner {
```

*GitHub* : [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L72), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81)


---

	 - src/blast/BlastGovernor.sol

```solidity
40	    function setFeeTo(address _feeTo) external onlyOwner {
```

*GitHub* : [40](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L40)


---

	 - src/blast/BlastMagicLP.sol

```solidity
80	    function setFeeTo(address feeTo_) external onlyImplementation onlyImplementationOwner {
...
89	    function setOperator(address operator, bool status) external onlyImplementation onlyImplementationOwner {
```

*GitHub* : [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L80), [89](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L89)


---

	 - src/blast/BlastOnboarding.sol

```solidity
147	    function setFeeTo(address feeTo_) external onlyOwner {
...
175	    function setTokenSupported(address token, bool supported) external onlyOwner {
...
185	    function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
...
190	    function setBootstrapper(address bootstrapper_) external onlyOwner {
```

*GitHub* : [147](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L147), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L185), [190](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L190)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
129	    function initialize(Router _router) external onlyOwner {
```

*GitHub* : [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129), [137](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L137), [146](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L146)


---

	 - src/blast/BlastTokenRegistry.sol


*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L14)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [91..98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L91-L98), [470..479](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L470-L479)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [46](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L46), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L57)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L96), [105](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L105)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [317](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L317), [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L536)

### [N-38]<a name="n-38"></a> Events may be emitted out of order due to reentrancy

Ensure that events follow the best practice of check-effects-interaction, and are emitted before external calls

*There are 16 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
81	    function setTokenEnabled(address token, bool enabled) external onlyOwner {
```

*GitHub* : [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L81)


---

	 - src/blast/BlastOnboarding.sol

```solidity
101	    function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
...
132	    function withdraw(address token, uint256 amount) external whenNotPaused onlySupportedTokens(token) {
...
175	    function setTokenSupported(address token, bool supported) external onlyOwner {
...
205	    function rescue(address token, address to, uint256 amount) external onlyOwner {
```

*GitHub* : [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L132), [175](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L175), [205](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L205)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
55	    function claim(bool lock) external returns (uint256 shares) {
...
96	    function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
```

*GitHub* : [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L55), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96)


---

	 - src/blast/libraries/BlastYields.sol

```solidity
20	    function enableTokenClaimable(address token) internal {
...
29	    function configureDefaultClaimables(address governor_) internal {
```

*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L20), [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L29)


---

	 - src/mimswap/MagicLP.sol

```solidity
290	    function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
```

*GitHub* : [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290), [413..420](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L413-L420), [461](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L461)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L170), [324](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L324), [361](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L361)

### [N-39]<a name="n-39"></a> Execution at deadlines should be allowed

The condition may be wrong in these cases, as when `block.timestamp` is equal to the compared `>` or `<` variable these blocks will not be executed.

*There are 4 instance(s) of this issue:*


---

	 - src/mimswap/MagicLP.sol

```solidity
421	        if (deadline < block.timestamp) {
```

*GitHub* : [421](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L421)


---

	 - src/mimswap/periphery/Router.sol

```solidity
48	        if (block.timestamp > deadline) {
```

*GitHub* : [48](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L48)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
379	        if (block.timestamp < reward.periodFinish) {
...
422	            if (locks[index].unlockTime > block.timestamp) {
```

*GitHub* : [379](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L379), [422](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L422)

### [N-40]<a name="n-40"></a> Function can return unassigned variable

Make sure that functions with a return value always return a valid and assigned value. Even if the default value is as expected, it should be assigned with the default value for code clarity and to reduce confusion.

*There are 1 instance(s) of this issue:*


---

	 - src/mimswap/libraries/DecimalMath.sol

```solidity
//@audit Variable `target` defined here, but never assigned
47	    function powFloor(uint256 target, uint256 e) internal pure returns (uint256) {
...
//@audit Variable returned here uninitialized
51	            return target;
```

*GitHub* : [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L51)

### [N-41]<a name="n-41"></a> Missing zero address check in initializer



*There are 1 instance(s) of this issue:*


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
129	    function initialize(Router _router) external onlyOwner {
130	        router = Router(payable(_router));
131	        factory = IFactory(router.factory());
132	        emit LogInitialized(_router);
133	    }
```

*GitHub* : [129..133](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L129-L133)

### [N-42]<a name="n-42"></a> Events should be emitted before external calls

Ensure that events follow the best practice of check-effects-interaction, and are emitted before external calls

*There are 38 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
// @audit functions: `nativeYieldTokens`, `enableTokenClaimable` called before this event
90	        emit LogTokenDepositEnabled(token, enabled);
```

*GitHub* : [90](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L90)


---

	 - src/blast/BlastOnboarding.sol

```solidity
// @audit functions: `safeTransferFrom` called before this event
120	        emit LogDeposit(msg.sender, token, amount, lock_);
...
// @audit functions: `safeTransfer` called before this event
140	        emit LogWithdraw(msg.sender, token, amount);
...
// @audit functions: `nativeYieldTokens`, `enableTokenClaimable` called before this event
182	        emit LogTokenSupported(token, supported);
...
// @audit functions: `safeTransfer` called before this event
211	        emit LogTokenRescue(token, to, amount);
```

*GitHub* : [120](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L120), [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L140), [182](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L182), [211](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L211)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
// @audit functions: `stakeFor` called before this event
71	        emit LogClaimed(msg.sender, shares, lock);
...
// @audit functions: `safeApprove`, `safeApprove`, `createPool`, `setOperator`, `transferOwnership`, `safeApprove` called before this event
124	        emit LogLiquidityBootstrapped(pool, address(staking), totalPoolShares);
...
// @audit functions: `factory` called before this event
132	        emit LogInitialized(_router);
```

*GitHub* : [71](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L71), [124](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L124), [132](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L132)


---

	 - src/blast/libraries/BlastYields.sol

```solidity
// @audit functions: `getConfiguration`, `configure` called before this event
26	        emit LogBlastTokenClaimableEnabled(address(this), token);
...
// @audit functions: `configure` called before this event
31	        emit LogBlastNativeClaimableEnabled(address(this));
```

*GitHub* : [26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L26), [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L31), [44](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L44), [57](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L57), [62](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L62), [72](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L72), [77](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L77)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [259](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L259), [264](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L264), [282](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L282), [287](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L287), [323](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L323), [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L325), [345](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L345), [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L347), [352](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L352), [409](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L409), [454](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L454), [467](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L467)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L88), [141](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L141), [152](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L152)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L183), [331](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L331), [392](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L392), [447](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L447), [475](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L475), [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L513), [638](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L638), [651](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L651)

### [N-43]<a name="n-43"></a> Use `@inheritdoc` for overridden functions

It is recommended to use `@inheritdoc` for overridden functions.

*There are 13 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
36	    function _onBeforeDeposit(
37	        IERC20 token,
38	        address /*from*/,
39	        address /*to*/,
40	        uint256 /*amount*/,
41	        uint256 /*share*/
42	    ) internal view override {
...
97	    /// @dev Called on DegenBox's constructor
98	    function _configure() internal override {
...
103	    function isOwner(address _account) internal view override returns (bool) {
```

*GitHub* : [36..42](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L36-L42), [97..98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L97-L98), [103](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L103)


---

	 - src/blast/BlastMagicLP.sol

```solidity
36	    /// VIEWS
37	    //////////////////////////////////////////////////////////////////////////////////////
38	
39	    function version() external pure override returns (string memory) {
...
95	    /// INTERNALS
96	    //////////////////////////////////////////////////////////////////////////////////////
97	
98	    function _afterInitialized() internal override {
```

*GitHub* : [36..39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L36-L39), [95..98](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L95-L98)


---

	 - src/blast/BlastOnboarding.sol

```solidity
223	    /// PROXY IMPLEMENTATION
224	    //////////////////////////////////////////////////////////////////////////////////////
225	
226	    function _implementation() internal view override returns (address) {
```

*GitHub* : [223..226](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L223-L226)


---

	 - src/blast/BlastWrappers.sol

```solidity
59	    function init(bytes calldata data) public payable override {
```

*GitHub* : [59](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L59)


---

	 - src/mimswap/MagicLP.sol

```solidity
152	    /// VIEWS
153	    //////////////////////////////////////////////////////////////////////////////////////
154	
155	    function name() public view override returns (string memory) {
...
159	    function symbol() public pure override returns (string memory) {
...
163	    function decimals() public view override returns (uint8) {
```

*GitHub* : [152..155](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L152-L155), [159](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L159), [163](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L163), [593](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L593)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L29), [37](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L37)

### [N-44]<a name="n-44"></a> Contract name does not follow the Solidity Style Guide

According to the [Solidity Style Guide](https://docs.soliditylang.org/en/latest/style-guide.html#contract-and-library-names), contracts and libraries should be named using the CapWords style.

*There are 7 instance(s) of this issue:*


---

	 - src/blast/BlastMagicLP.sol

```solidity
10	contract BlastMagicLP is MagicLP {
11	    event LogFeeToChanged(address indexed feeTo);
```

*GitHub* : [10..11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L10-L11)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
23	contract BlastOnboardingBootDataV1 is BlastOnboardingData {
24	    address public pool;
```

*GitHub* : [23..24](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L23-L24)


---

	 - src/blast/BlastWrappers.sol

```solidity
19	contract BlastMIMSwapRouter is Router {
20	    constructor(IWETH weth_, IFactory factory, address governor_) Router(weth_, factory) {
...
28	contract BlastMIMSwapFactory is Factory {
29	    constructor(
...
42	contract BlastCauldronV4 is CauldronV4 {
43	    error ErrInvalidGovernorAddress();
```

*GitHub* : [19..20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L19-L20), [28..29](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L28-L29), [42..43](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L42-L43)


---

	 - src/mimswap/MagicLP.sol

```solidity
25	contract MagicLP is ERC20, ReentrancyGuard, Owned {
26	    using Math for uint256;
```

*GitHub* : [25..26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L25-L26)


---

	 - src/mimswap/libraries/PMMPricing.sol

```solidity
20	library PMMPricing {
21	    enum RState {
```

*GitHub* : [20..21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L20-L21)

### [N-45]<a name="n-45"></a> Variable names for `immutable`s should use UPPER_CASE_WITH_UNDERSCORES

For `immutable` variable names, each word should use all capital letters, with underscores separating each word (UPPER_CASE_WITH_UNDERSCORES)

*There are 16 instance(s) of this issue:*


---

	 - src/blast/BlastBox.sol

```solidity
20	    BlastTokenRegistry public immutable registry;
```

*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L20)


---

	 - src/blast/BlastMagicLP.sol

```solidity
17	    BlastTokenRegistry public immutable registry;
```

*GitHub* : [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L17)


---

	 - src/blast/BlastWrappers.sol

```solidity
45	    address private immutable _governor;
```

*GitHub* : [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L45)


---

	 - src/mimswap/MagicLP.sol

```solidity
61	    MagicLP public immutable implementation;
```

*GitHub* : [61](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L61)


---

	 - src/mimswap/periphery/Router.sol

```solidity
33	    IWETH public immutable weth;
...
34	    IFactory public immutable factory;
```

*GitHub* : [33](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L33), [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L34)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol

```solidity
10	    IMagicLP public immutable pair;
...
11	    IAggregator public immutable baseOracle;
...
12	    IAggregator public immutable quoteOracle;
...
13	    uint8 public immutable baseDecimals;
```

*GitHub* : [10](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L10), [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L11), [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L12), [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L13), [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L14)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [83](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L83), [84](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L84), [85](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L85), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L86), [87](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L87)

### [N-46]<a name="n-46"></a> Use a single file for system wide constants

Consider grouping all the system constants under a single file.

*There are 22 instance(s) of this issue:*


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
13	address constant USDB = 0x4300000000000000000000000000000000000003;
...
14	address constant MIM = 0x76DA31D7C9CbEAE102aff34D3398bC450c8374c1;
...
15	uint256 constant FEE_RATE = 0.0005 ether; // 0.05%
...
16	uint256 constant K = 0.00025 ether; // 0.00025, 1.25% price fluctuation, similar to A2000 in curve
...
17	uint256 constant I = 0.998 ether; // 1 MIM = 0.998 USDB
...
18	uint256 constant USDB_TO_MIN = 1.002 ether; // 1 USDB = 1.002 MIM
...
19	uint256 constant MIM_TO_MIN = I;
```

*GitHub* : [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L13), [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L14), [15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L15), [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L16), [17](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L17), [18](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L18), [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L19)


---

	 - src/blast/libraries/BlastPoints.sol

```solidity
7	    address public constant BLAST_POINTS_OPERATOR = 0xD1025F1359422Ca16D9084908d629E0dBa60ff28;
...
8	    IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);
```

*GitHub* : [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L7), [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L8)


---

	 - src/blast/libraries/BlastYields.sol

```solidity
14	    IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);
```

*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L14)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64), [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L65), [66](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L66)


---

	 - src/mimswap/libraries/DecimalMath.sol


*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L21)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [31](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L31)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [16](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L16)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [78](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L78), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L79), [80](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L80), [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L81)

### [N-47]<a name="n-47"></a> Unsafe `uint` to `int` conversion

The `int` type in Solidity uses the [two's complement system](https://en.wikipedia.org/wiki/Two%27s_complement), so it is possible to accidentally overflow a very large `uint` to an `int`, even if they share the same number of bytes (e.g. a `uint256 number > type(uint128).max` will overflow a `int256` cast).

Consider using the [SafeCast](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/utils/math/SafeCast.sol) library to prevent any overflows.

*There are 1 instance(s) of this issue:*


---

	 - src/oracles/aggregators/MagicLpAggregator.sol

```solidity
45	        return int256(minAnswer * (baseReserve + quoteReserve) / pair.totalSupply());
```

*GitHub* : [45](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L45)

### [N-48]<a name="n-48"></a> Use SafeCast to safely downcast variables

Downcasting int/uints in Solidity can be unsafe due to the potential for data loss and unintended behavior. When downcasting a larger integer type to a smaller one (e.g., `uint256` to `uint128`), the value may exceed the range of the target type, leading to truncation and loss of significant digits. This data loss can result in unexpected state changes, incorrect calculations, or other contract vulnerabilities, ultimately compromising the contracts functionality and reliability. To prevent these risks, developers should carefully consider the range of values their variables may hold and ensure that proper checks are in place to prevent out-of-range values before performing downcasting. Also consider using OZ SafeCast functionality.

*There are 30 instance(s) of this issue:*


---

	 - src/mimswap/MagicLP.sol

```solidity
125	        _BLOCK_TIMESTAMP_LAST_ = uint32(block.timestamp % 2 ** 32);
...
139	        if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {
...
140	            _RState_ = uint32(PMMPricing.RState.ONE);
...
144	        if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {
...
145	            _RState_ = uint32(PMMPricing.RState.ONE);
...
256	        if (_RState_ != uint32(newRState)) {
...
258	            _RState_ = uint32(newRState);
...
279	        if (_RState_ != uint32(newRState)) {
...
281	            _RState_ = uint32(newRState);
...
320	            if (_RState_ != uint32(newRState)) {
```

*GitHub* : [125](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L125), [139](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L139), [140](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L140), [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L144), [145](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L145), [256](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L256), [258](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L258), [279](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L279), [281](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L281), [320](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L320), [322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L322), [342](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L342), [344](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L344), [438](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L438), [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439), [493](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L493), [494](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L494), [495](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L495), [513](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L513), [514](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L514), [517](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L517), [518](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L518), [536](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L536), [537](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L537), [538](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L538), [539](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L539), [540](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L540), [546](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L546)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [389](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L389), [533](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L533)

### [N-49]<a name="n-49"></a> Consider adding a block/deny-list

Doing so will significantly increase centralization, but will help to prevent hackers from using stolen tokens

*There are 5 instance(s) of this issue:*


---

	 - src/blast/BlastGovernor.sol

```solidity
7	contract BlastGovernor is OperatableV2 {
8	    event LogFeeToChanged(address indexed feeTo);
```

*GitHub* : [7..8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L7-L8)


---

	 - src/blast/BlastOnboarding.sol

```solidity
64	contract BlastOnboarding is BlastOnboardingData, Proxy {
65	    using SafeTransferLib for address;
```

*GitHub* : [64..65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L64-L65)


---

	 - src/mimswap/MagicLP.sol

```solidity
25	contract MagicLP is ERC20, ReentrancyGuard, Owned {
26	    using Math for uint256;
```

*GitHub* : [25..26](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L25-L26)


---

	 - src/mimswap/periphery/Router.sol

```solidity
12	contract Router {
13	    using SafeTransferLib for address;
```

*GitHub* : [12..13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L12-L13)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
14	contract LockingMultiRewards is OperatableV2, Pausable {
15	    using SafeTransferLib for address;
```

*GitHub* : [14..15](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L14-L15)

### [N-50]<a name="n-50"></a> Expressions for constant values should use `immutable` rather than `constant`

While it does not save gas for some simple binary expressions because the compiler knows that developers often make this mistake, it's still best to use the right tool for the task at hand. There is a difference between `constant` variables and `immutable` variables, and they should each be used in their appropriate contexts. `constants` should be used for literal values written into the code, and `immutable` variables should be used for expressions, or values calculated in, or passed into the constructor.

*There are 7 instance(s) of this issue:*


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
19	uint256 constant MIM_TO_MIN = I;
```

*GitHub* : [19](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L19)


---

	 - src/blast/libraries/BlastPoints.sol

```solidity
8	    IBlastPoints public constant BLAST_POINTS = IBlastPoints(0x2536FE9ab3F511540F2f9e2eC2A805005C3Dd800);
```

*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L8)


---

	 - src/blast/libraries/BlastYields.sol

```solidity
14	    IBlast constant BLAST_YIELD_PRECOMPILE = IBlast(0x4300000000000000000000000000000000000002);
```

*GitHub* : [14](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L14)


---

	 - src/mimswap/MagicLP.sol

```solidity
63	    uint256 public constant MAX_I = 10 ** 36;
...
64	    uint256 public constant MAX_K = 10 ** 18;
```

*GitHub* : [63](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L63), [64](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L64)


---

	 - src/mimswap/libraries/DecimalMath.sol

```solidity
20	    uint256 internal constant ONE = 10 ** 18;
...
21	    uint256 internal constant ONE2 = 10 ** 36;
```

*GitHub* : [20](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L20), [21](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L21)

### [N-51]<a name="n-51"></a> Lines are too long

Maximum suggested line length is 120 characters according to the [documentation](https://docs.soliditylang.org/en/latest/style-guide.html#maximum-line-length).

*There are 54 instance(s) of this issue:*


---

	 - src/blast/BlastGovernor.sol

```solidity
53	    function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
```

*GitHub* : [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L53)


---

	 - src/blast/BlastMagicLP.sol

```solidity
53	    function claimTokenYields() external onlyClones onlyImplementationOperators returns (uint256 token0Amount, uint256 token1Amount) {
```

*GitHub* : [53](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L53)


---

	 - src/blast/BlastOnboarding.sol

```solidity
101	    function deposit(address token, uint256 amount, bool lock_) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
...
123	    function lock(address token, uint256 amount) external whenNotPaused onlyState(State.Opened) onlySupportedTokens(token) {
```

*GitHub* : [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L101), [123](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L123)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
86	    function previewTotalPoolShares() external view returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
96	    function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
```

*GitHub* : [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L86), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L96)


---

	 - src/mimswap/MagicLP.sol

```solidity
32	    event Swap(address fromToken, address toToken, uint256 fromAmount, uint256 toAmount, address trader, address receiver);
...
36	    event ParametersChanged(uint256 newLpFeeRate, uint256 newI, uint256 newK, uint256 newBaseReserve, uint256 newQuoteReserve);
...
156	        return string(abi.encodePacked("MagicLP ", IERC20Metadata(_BASE_TOKEN_).symbol(), "/", IERC20Metadata(_QUOTE_TOKEN_).symbol()));
...
170	    ) public view returns (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) {
...
183	    ) public view returns (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) {
...
204	    function getPMMStateForCall() external view returns (uint256 i, uint256 K, uint256 B, uint256 Q, uint256 B0, uint256 Q0, uint256 R) {
...
290	    function flashLoan(uint256 baseAmount, uint256 quoteAmount, address assetTo, bytes calldata data) external nonReentrant {
...
310	            (uint256 receiveBaseAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newQuoteTarget) = querySellQuote(
...
325	            emit Swap(address(_QUOTE_TOKEN_), address(_BASE_TOKEN_), quoteInput, receiveBaseAmount, msg.sender, assetTo);
...
332	            (uint256 receiveQuoteAmount, uint256 mtFee, PMMPricing.RState newRState, uint256 newBaseTarget) = querySellBase(
...
347	            emit Swap(address(_BASE_TOKEN_), address(_QUOTE_TOKEN_), baseInput, receiveQuoteAmount, msg.sender, assetTo);
...
360	    function buyShares(address to) external nonReentrant returns (uint256 shares, uint256 baseInput, uint256 quoteInput) {
...
381	            shares = quoteBalance < DecimalMath.mulFloor(baseBalance, _I_) ? DecimalMath.divFloor(quoteBalance, _I_) : baseBalance;
...
402	            _BASE_TARGET_ = (uint256(_BASE_TARGET_) + DecimalMath.mulFloor(uint256(_BASE_TARGET_), mintRatio)).toUint112();
...
403	            _QUOTE_TARGET_ = (uint256(_QUOTE_TARGET_) + DecimalMath.mulFloor(uint256(_QUOTE_TARGET_), mintRatio)).toUint112();
...
439	        _QUOTE_TARGET_ = uint112(uint256(_QUOTE_TARGET_) - (uint256(_QUOTE_TARGET_) * shareAmount).divCeil(totalShares));
```

*GitHub* : [32](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L32), [36](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L36), [156](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L156), [170](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L170), [183](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L183), [204](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L204), [290](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L290), [310](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L310), [325](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L325), [332](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L332), [347](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L347), [360](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L360), [381](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L381), [402](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L402), [403](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L403), [439](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L439)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol

```solidity
34	    function getFeeRate(address trader, uint256 lpFeeRate) external view returns (uint256 adjustedLpFeeRate, uint256 mtFeeRate) {
```

*GitHub* : [34](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L34)


---

	 - src/mimswap/libraries/Math.sol

```solidity
51	    function _GeneralIntegrate(uint256 V0, uint256 V1, uint256 V2, uint256 i, uint256 k) internal pure returns (uint256) {
...
79	    function _SolveQuadraticFunctionForTarget(uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
...
131	    function _SolveQuadraticFunctionForTrade(uint256 V0, uint256 V1, uint256 delta, uint256 i, uint256 k) internal pure returns (uint256) {
...
184	        uint256 squareRoot = DecimalMath.mulFloor((DecimalMath.ONE - k) * 4, DecimalMath.mulFloor(k, V0) * V0); // 4(1-k)kQ0^2
```

*GitHub* : [51](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L51), [79](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L79), [131](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L131), [184](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L184)


---

	 - src/mimswap/libraries/PMMPricing.sol

```solidity
39	    function sellBaseToken(PMMState memory state, uint256 payBaseAmount) internal pure returns (uint256 receiveQuoteAmount, RState newR) {
...
55	                    // [Important corner case!] may enter this branch when some precision problem happens. And consequently contribute to negative spare quote amount
...
65	                receiveQuoteAmount = backToOneReceiveQuote + _ROneSellBaseToken(state, payBaseAmount - backToOnePayBase);
...
76	    function sellQuoteToken(PMMState memory state, uint256 payQuoteAmount) internal pure returns (uint256 receiveBaseAmount, RState newR) {
...
96	                receiveBaseAmount = backToOneReceiveBase + _ROneSellQuoteToken(state, payQuoteAmount - backToOnePayQuote);
...
129	        return Math._SolveQuadraticFunctionForTrade(state.B0, state.B0, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);
...
144	        return Math._GeneralIntegrate(state.Q0, state.Q + payQuoteAmount, state.Q, DecimalMath.reciprocalFloor(state.i), state.K);
...
185	        return Math._SolveQuadraticFunctionForTrade(state.B0, state.B, payQuoteAmount, DecimalMath.reciprocalFloor(state.i), state.K);
```

*GitHub* : [39](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L39), [55](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L55), [65](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L65), [76](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L76), [96](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L96), [129](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L129), [144](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L144), [185](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L185)


---

	 - src/mimswap/periphery/Factory.sol

```solidity
81	    function create(address baseToken_, address quoteToken_, uint256 lpFeeRate_, uint256 i_, uint256 k_) external returns (address clone) {
...
86	        IMagicLP(clone).init(address(baseToken_), address(quoteToken_), lpFeeRate_, address(maintainerFeeRateModel), i_, k_);
```

*GitHub* : [81](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L81), [86](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L86)


---

	 - src/mimswap/periphery/Router.sol

```solidity
88	        clone = IFactory(factory).create(useTokenAsQuote ? address(weth) : token, useTokenAsQuote ? token : address(weth), lpFeeRate, i, k);
...
101	        shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
...
138	            shares = quoteBalance < DecimalMath.mulFloor(baseBalance, i) ? DecimalMath.divFloor(quoteBalance, i) : baseBalance;
...
169	    ) external ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
199	    ) external payable ensureDeadline(deadline) returns (uint256 baseAdjustedInAmount, uint256 quoteAdjustedInAmount, uint256 shares) {
...
251	    function previewRemoveLiquidity(address lp, uint256 sharesIn) external view returns (uint256 baseAmountOut, uint256 quoteAmountOut) {
...
523	            uint256 shares = quoteInAmount < DecimalMath.mulFloor(baseInAmount, i) ? DecimalMath.divFloor(quoteInAmount, i) : baseInAmount;
...
541	    function _swap(address to, address[] calldata path, uint256 directions, uint256 minimumOut) internal returns (uint256 amountOut) {
```

*GitHub* : [88](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L88), [101](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L101), [138](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L138), [169](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L169), [199](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L199), [251](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L251), [523](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L523), [541](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L541)


---

	 - src/staking/LockingMultiRewards.sol

```solidity
11	/// @author Based from Curve Finance's MultiRewards contract https://github.com/curvefi/multi-rewards/blob/master/contracts/MultiRewards.sol
...
12	/// @author Based from Ellipsis Finance's EpsStaker https://github.com/ellipsis-finance/ellipsis/blob/master/contracts/EpsStaker.sol
...
13	/// @author Based from Convex Finance's CvxLockerV2 https://github.com/convex-eth/platform/blob/main/contracts/contracts/CvxLockerV2.sol
...
109	    /// @param _lockingBoostMultiplerInBips The multiplier for the locking boost. 30000 means if you stake 100, you get 300 locked
...
252	    // |                             ^ lock starts (adjusted)                                    ^ unlock ends (nextUnlockTime)
...
277	    function _rewardPerToken(address rewardToken, uint256 lastTimeRewardApplicable_, uint256 totalSupply_) public view returns (uint256) {
...
292	    function _earned(address user, uint256 balance_, address rewardToken, uint256 rewardPerToken_) internal view returns (uint256) {
...
322	    /// @notice This function can recover any token except for the staking token beyond the balance necessary for rewards.
...
533	        _rewardData[token_].lastUpdateTime = uint248(lastTimeRewardApplicable_); // safe to cast as this will never overflow
```

*GitHub* : [11](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L11), [12](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L12), [13](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L13), [109](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L109), [252](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L252), [277](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L277), [292](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L292), [322](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L322), [533](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L533)


```toml/n2solc = "0.8.20"
```

proof: 
https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2


*There are 20 instance(s) of this issue:*


---

	 - src/blast/BlastDapp.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastDapp.sol#L2)


---

	 - src/blast/BlastBox.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
3	pragma solidity >=0.8.0;
```

*GitHub* : [3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol#L3)


---

	 - src/blast/BlastGovernor.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol#L2)


---

	 - src/blast/BlastMagicLP.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
3	pragma solidity >=0.8.0;
```

*GitHub* : [3](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol#L3)


---

	 - src/blast/BlastOnboarding.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol#L2)


---

	 - src/blast/BlastOnboardingBoot.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol#L2)


---

	 - src/blast/BlastTokenRegistry.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol#L2)


---

	 - src/blast/BlastWrappers.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol#L2)


---

	 - src/blast/libraries/BlastPoints.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastPoints.sol#L2)


---

	 - src/blast/libraries/BlastYields.sol

```solidity
// @proof: https://github.com/code-423n4/2024-03-abracadabra-money/blob/1f4693fdbf33e9ad28132643e2d6f7635834c6c6/foundry.toml#L2
// @context ```toml/n2solc = "0.8.20"
```
2	pragma solidity >=0.8.0;
```

*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/libraries/BlastYields.sol#L2)


---

	 - src/mimswap/MagicLP.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol#L8)


---

	 - src/mimswap/auxiliary/FeeRateModel.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol#L8)


---

	 - src/mimswap/auxiliary/FeeRateModelImpl.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModelImpl.sol#L2)


---

	 - src/mimswap/libraries/DecimalMath.sol


*GitHub* : [7](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/DecimalMath.sol#L7)


---

	 - src/mimswap/libraries/Math.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/Math.sol#L8)


---

	 - src/mimswap/libraries/PMMPricing.sol


*GitHub* : [8](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/libraries/PMMPricing.sol#L8)


---

	 - src/mimswap/periphery/Factory.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol#L2)


---

	 - src/mimswap/periphery/Router.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol#L2)


---

	 - src/oracles/aggregators/MagicLpAggregator.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/oracles/aggregators/MagicLpAggregator.sol#L2)


---

	 - src/staking/LockingMultiRewards.sol


*GitHub* : [2](https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol#L2)