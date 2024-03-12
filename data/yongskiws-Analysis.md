| Section              | Description                                                                                               |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| Overview             | Introduction to the importance of structuring the code for analysis, efficiency, and improvement.         |
| Introduction        | Description of Abracadabra.money and its core product, Cauldrons, along with key concepts.                 |
| Cauldrons           | Explanation of Cauldrons, the heart of Abracadabra, and its features like collateral and leverage.         |
| Liquidations        | Description of the liquidation process in Abracadabra to maintain stability in the ecosystem.               |
| My Positions        | Overview of the section for users to manage their assets on Abracadabra.money.                             |
| Stake               | Explanation of staking mechanisms supported by Abracadabra for earning rewards.                             |
| Magic Tokens        | Description of Magic Tokens and their role in enhancing assets on Abracadabra.money.                       |
| Farms               | Explanation of yield farming on Abracadabra.money and how users can earn rewards efficiently.               |
| Swap                | Overview of the asset exchange feature on Abracadabra.money using the SWAP function.                        |
| Codebase quality and Systemic risks    | Detailed analysis of the code quality and recommendations for improvement.                                  |
| MagicLP             | Analysis of the MagicLP contract including issues and potential improvements.                               |
| LockingMultiRewards | Analysis of the LockingMultiRewards contract including issues and potential improvements.                   |
| Approach            | Overview of the approach followed during the code review process.                                           |
| Factory             | Analysis of the Factory contract for creating and registering MagicLP pools.                                 |
| Analysis of the code base and diagram architecture | Summary of the code analysis and diagram architecture of various contracts.                                  |
| Centralization Risk | Identification of centralization risks in the provided code snippets.                                        |
| Conclusion          | Summary of the analysis and recommendations for the Abracadabra Mimswap project.                             |


# Overview

Structuring the code is crucial for conducting a thorough analysis of the code base. This enables auditors to predict the level of contract difficulty, identify critical contracts, and determine security-critical features such as payment functions or assembly usage. Additionally, this approach accurately measures the time required to perform a detailed audit and helps determine the cost of a project audit. To achieve efficiency, clarity, and improvements, it is essential to have a comprehensive view of the entire architecture. This enables the identification of the basic structure, relationships between modules, and key design patterns. By understanding the big picture, we can analyze the complexity of the code and reveal its strengths and potential for improvement with confidence.

# Introduction

Abracadabra.money is Omnichain DeFi lending platform that brings magic to the world of decentralized finance. By leveraging interest-bearing tokens as collateral, Abracadabra allows users to mint Magic Internet Money (MIM), a USD-denominated stablecoin. This audit  aims to elucidate the workings of Abracadabra.money and its various offerings.

## Cauldrons: Heart of Abracadabra

At the heart of Abracadabra lies Cauldrons, its core product. Cauldrons are isolated lending markets built on Kashi Technology. They provide users with the ability to borrow against different forms of collateral. The key concepts to grasp here are:

- **Collateral:** Assets deposited into the Cauldron to secure MIM loans.
- **Borrow:** Obtaining MIM and receiving it in your wallet for personal use.
- **Leverage:** Using borrowed MIM to acquire more collateral and depositing it back into the Cauldron.
- **LTV (Loan to Value):** Ratio between collateral value and borrowed value.
- **MCR (Maximum Collateral Ratio):** Maximum LTV allowed for each market before liquidation.
- **Mint Fee:** Fee charged upon opening a position.
- **Interest Fee:** Interest charged on borrowed MIM.
- **Liquidation Fee:** Fee paid to liquidators in case of an insolvent position.

### Liquidations: Ensuring Stability

Liquidations are crucial in maintaining the stability of Abracadabra's ecosystem. When a position's collateral value falls below the borrowed amount, it becomes eligible for liquidation. Liquidators step in to repay the debt in exchange for a portion of the collateral. Abracadabra's isolated lending protocol ensures each position is treated independently.

### My Positions: Managing Assets

This section allows users to interact and monitor their positions on Abracadabra.money. Users can view Cauldrons, BentoBox, and DegenBox balances across supported chains. They can manage their positions, sort and filter them based on various parameters.

### Stake: Maximizing Returns

Staking offers users the opportunity to earn rewards by depositing assets into contracts. Abracadabra supports two staking methods:

- **sSPELL:** Stake SPELL tokens and earn more SPELL.
- **mSPELL:** Stake SPELL tokens and earn stablecoin income through MIM.

Staking not only provides revenue but also grants voting power in the governance of the Abracadabra DAO.

### Magic Tokens: Enhancing Assets

Magic tokens enable users to transform regular assets into yield-bearing assets. These tokens can be stored in wallets, transferred, and sometimes used as collateral in Abracadabra. They employ state-of-the-art strategies to amplify token yields.

### Farms: Yield Farming

Farming involves deploying liquidity in specific pools to receive incentives from the protocol. Users can access farming positions through the interface, stake or unstake LP tokens, and earn rewards efficiently.

### Swap: Convenient Asset Exchange

The SWAP feature allows users to exchange MIM stablecoins for other stablecoins through curve.fi. Users can specify the amount, select the desired stablecoin, set slippage and gas price, and confirm the transaction.

In essence, Abracadabra.money offers a comprehensive suite of services, DeFi lending with its innovative approach and user-friendly interface. Through Cauldrons, Liquidations, Staking, Magic Tokens, Farms, and Swaps, users can maximize their returns and navigate the decentralized financial landscape with ease.



# Codebase quality and Systemic risks

Overall, I consider the quality of the Abracadabra Mimswap codebase to be excellent. The code appears to be very mature and well-developed. We have noticed the implementation of various standards adhere to appropriately. Details are explained below:

## Router

| Issue                                            | Recommendation                                                                                                                |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| No check for weth_ and factory_ being a contract | Add a check to ensure that weth_ and factory_ are contract addresses, not EOA addresses. This can be done using type(IWETH).interfaceId and type(IFactory).interfaceId. |
| No event for creating a new pool                | Consider emitting an event when a new pool is created to enable easier tracking and monitoring of pool creations.           |
| No check for token being a contract             | Add a check to ensure that token is a contract address, not an EOA address. This can be done using type(IERC20).interfaceId. |
| No event for creating a new pool with ETH       | Consider emitting an event when a new pool with ETH is created to enable easier tracking and monitoring of pool creations with ETH. |
| No event for adding liquidity                   | Consider emitting an event when liquidity is added to a pool to enable easier tracking and monitoring of liquidity additions. |
| No event for adding liquidity with ETH          | Consider emitting an event when liquidity with ETH is added to a pool to enable easier tracking and monitoring of liquidity additions with ETH. |
| No event for removing liquidity                 | Consider emitting an event when liquidity is removed from a pool to enable easier tracking and monitoring of liquidity removals. |
| No event for removing liquidity with ETH        | Consider emitting an event when liquidity with ETH is removed from a pool to enable easier tracking and monitoring of liquidity removals with ETH. |
| No event for swapping tokens                   | Consider emitting an event when tokens are swapped to enable easier tracking and monitoring of token swaps.               |
| No event for selling base tokens               | Consider emitting an event when base tokens are sold to enable easier tracking and monitoring of base token sales.         |
| No event for selling quote tokens              | Consider emitting an event when quote tokens are sold to enable easier tracking and monitoring of quote token sales.       |

# MagicLP

1. **No access control for `init()` function:** 
   The `init()` function, responsible for initializing the contract, lacks access control modifiers. This exposes the contract to potential overwrite of initial configurations by anyone who calls this function.

2. **Lack of input validation in some functions:** 
   Functions like `sellBase()`, `sellQuote()`, and `flashLoan()` lack thorough validation of input parameters. For instance, there's no check to ensure that the `baseAmount` and `quoteAmount` parameters in the `flashLoan()` function are non-zero.

3. **Potential integer overflows:** 
   The contract utilizes unsigned integer types for arithmetic operations, which can lead to integer overflows. For example, the `_BASE_PRICE_CUMULATIVE_LAST_` variable is incremented by the product of `getMidPrice()` and `timeElapsed` without checking for overflow.

4. **Lack of event logs in some critical functions:** 
   Critical functions like `_resetTargetAndReserve()` do not emit any event logs. This absence can make it challenging for external parties to track changes to the contract state.

5. **Inconsistent naming conventions:** 
   The contract employs inconsistent naming conventions for function parameters. For instance, while the `sellBase()` function uses `to` as a parameter name, the `sellShares()` function uses `to` as well as `assetTo`.

6. **Lack of documentation:** 
   The contract suffers from insufficient documentation, making it challenging for external parties to understand its functionality and potential risks.


# LockingMultiRewards

1. **Lack of Input Validation**: Some functions such as `stake()`, `lock()`, and `withdraw()` lack thorough input parameter validation. For instance, the `stake()` function does not verify if the `amount` parameter is non-zero.

2. **Potential Integer Overflows**: The contract employs unsigned integer types for arithmetic operations, potentially leading to integer overflows. For example, the `totalSupply` function calculates the total supply without ensuring that the sum doesn't exceed the maximum value of a `uint256`.

3. **Missing Event Logs**: Critical functions like `_stakeFor()` and `_createLock()` do not emit any event logs. This omission can hinder external parties from tracking changes to the contract state effectively.

4. **Inconsistent Naming Conventions**: The contract employs inconsistent naming conventions for function parameters. For instance, the `stake()` function uses `lock_` as a parameter name, while the `lock()` function utilizes `lock` as a function name.

5. **Lack of Documentation**: The contract lacks comprehensive documentation, which complicates understanding its functionality and potential risks for external parties.


# Approach we followed when reviewing the code


# Router

For creating liquidity pools, adding liquidity, removing liquidity, swapping tokens, and selling tokens for ETH or other tokens.

## Main Functions:

- `createPool`: Creates a new liquidity pool with the provided baseToken, quoteToken, lpFeeRate, i, k, to, baseInAmount, and quoteInAmount. It also validates the decimals of the base and quote tokens.
- `createPoolETH`: Creates a new liquidity pool with ETH as one of the tokens. It can be used to create a pool with ETH as the base or quote token.
- `previewCreatePool`: Calculates the estimated base and quote amounts and shares that would be created when a new liquidity pool is created.
- `previewAddLiquidity`: Calculates the estimated base and quote amounts and shares that would be added to an existing liquidity pool.
- `addLiquidity`: Adds liquidity to an existing liquidity pool with the provided baseInAmount, quoteInAmount, minimumShares, and deadline.
- `addLiquidityUnsafe`: Adds liquidity to an existing liquidity pool without checking for slippage.
- `addLiquidityETH`: Adds liquidity to an existing liquidity pool with ETH as one of the tokens.
- `addLiquidityETHUnsafe`: Adds liquidity to an existing liquidity pool with ETH as one of the tokens without checking for slippage.
- `previewRemoveLiquidity`: Calculates the estimated base and quote amounts that would be received when removing liquidity from a pool.
- `removeLiquidity`: Removes liquidity from a pool and transfers the base and quote tokens to the specified address.
- `removeLiquidityETH`: Removes liquidity from a pool and transfers the ETH and quote tokens to the specified address.
- `swapTokensForTokens`: Swaps tokens by routing through one or more liquidity pools.
- `swapETHForTokens`: Swaps ETH for tokens by routing through one or more liquidity pools.
- `swapTokensForETH`: Swaps tokens for ETH by routing through one or more liquidity pools.
- `sellBaseTokensForTokens`: Sells base tokens for other tokens in a liquidity pool.
- `sellBaseETHForTokens`: Sells base tokens for other tokens in a liquidity pool with ETH as the quote token.
- `sellBaseTokensForETH`: Sells base tokens for ETH in a liquidity pool.
- `sellQuoteTokensForTokens`: Sells quote tokens for other tokens in a liquidity pool.
- `sellQuoteETHForTokens`: Sells quote tokens for other tokens in a liquidity pool with ETH as the base token.
- `sellQuoteTokensForETH`: Sells quote tokens for ETH in a liquidity pool.

## Internal Functions:

- `_addLiquidity`: Internal function to add liquidity to a pool with slippage checking.
- `_adjustAddLiquidity`: Internal function to adjust input amounts based on the current reserves in a pool.
- `_swap`: Internal function to swap tokens by routing through one or more liquidity pools.
- `_sellBase`: Internal function to sell base tokens in a liquidity pool.
- `_sellQuote`: Internal function to sell quote tokens in a liquidity pool.
- `_validatePath`: Internal function to validate the swap path.
- `_validateDecimals`: Internal function to validate the decimals of base and quote tokens.

# MagicLP

MagicLP is a sophisticated DEX pool contract that implements the PMM algorithm for stable price trading of two tokens. It provides various functionalities for trading, managing the pool's state, and setting parameters, and includes comprehensive error handling and modifier mechanisms and for trading two tokens with a stable price. It is adapted from the DODOEX DSP and implements a price range algorithm called Proactive Market Making (PMM).

## Events:

Defines several events that are emitted during various actions, such as buying shares, selling shares, swapping tokens, changing parameters, and flash loans.

## Error Handling:

Defines various error messages for different error conditions that may occur during contract execution.

## Variables:

Defines several variables related to the pool's state, such as base and quote tokens, reserves, block timestamp, price cumulative last, base and quote targets, fee rate model, and PMM parameters.

## Public Functions:

Provides several public functions for syncing the pool, correcting the R state, querying the sell base and quote amounts, getting the PMM state, and getting the mid-price.

## Views:

Provides several view functions for getting the pool's name, symbol, decimals, querying the sell base and quote amounts, getting the PMM state, getting the mid-price, getting the user's fee rate, getting the base and quote inputs, and getting version.

## Trade Functions:

For selling base and quote tokens, and performing flash loans.

## Buy & Sell Shares:

For buying and selling shares in the pool.

## Admin Functions:

For rescuing tokens, setting parameters, and syncing the pool's reserves and targets.

## Internal Functions:

Provides several internal functions for resetting the pool's targets and reserves, updating the time-weighted average price (TWAP), setting the pool's reserves, syncing the pool's state, transferring tokens, minting tokens, and managing contract modifiers.

## Modifiers:

Provides modifiers for ensuring that only the implementation owner, clones, or the implementation itself can call certain functions.

# LockingMultiRewards

It is based on Curve Finance's MultiRewards, Ellipsis Finance's EpsStaker, and Convex Finance's CvxLockerV2. allows users to lock their tokens for a period of time to get a boost on their rewards.

## Variables:

maxLocks, lockingBoostMultiplerInBips, rewardsDuration, lockDuration, stakingToken, and mappings for storing user balances, locked balances, and reward data.

## Public Functions:

Including stake, lock, withdraw, withdrawWithRewards, getRewards, and various views for retrieving data.

## Internal Functions:

Has several internal functions for handling staking, locking, and reward distribution.

## Modifiers:

Uses the `whenNotPaused` modifier to prevent function execution when is paused.

## Events:

Emits various events when certain actions are taken, such as staking, locking, unlocking, and reward distribution.

# Factory

Create and register MagicLP pools. From Owned contract from the solmate library, which provides basic authorization control.

## Imported Contracts:

Owned from "solmate/auth/Owned.sol"
LibClone from "solady/utils/LibClone.sol"
IFeeRateModel from "/mimswap/interfaces/IFeeRateModel.sol"
IMagicLP from "/mimswap/interfaces/IMagicLP.sol"
MagicLP from "/mimswap/MagicLP.sol"

## Events:

- `LogCreated`: Logs the creation of a new pool
- `LogPoolAdded`: Logs the addition of a pool to the registry
- `LogPoolRemoved`: Logs the removal of a pool from the registry
- `LogSetImplementation`: Logs the change of the lp implementation
- `LogSetMaintainer`: Logs the change of the maintainer
- `LogSetMaintainerFeeRateModel`: Logs the change of the maintainer fee rate model

## Errors:

- `ErrInvalidUserPoolIndex`: Error for an invalid user pool index
- `ErrZeroAddress`: Error for a zero address

## Variables:

- `implementation`: The address of the MagicLP implementation
- `maintainerFeeRateModel`: The fee rate model for the maintainer
- `pools`: A mapping of base tokens to quote tokens and their respective pools
- `userPools`: A mapping of creators to their respective pools

## Public Functions:

- `predictDeterministicAddress`: Computes the deterministic address of a new pool
- `create`: Creates a new pool with the given parameters and adds it to the registry

## Admin Functions:

- `setLpImplementation`: Changes the lp implementation
- `setMaintainerFeeRateModel`: Changes the maintainer fee rate model
- `addPool`: Registers a pool to the list
- `removePool`: Removes a pool from the list

## Internal Functions:

- `_addPool`: Adds a pool to the registry
- `_computeSalt`: Computes the salt used to predict the deterministic address of a new pool

# Analysis of the code base and diagram architecture


## Router
![Routersol](https://github.com/yongsxyz/Audit-Analysis/assets/39027215/51d3b845-832a-4512-9628-3c8236c4c286)

## MagicLP
![MagicLPsol](https://github.com/yongsxyz/Audit-Analysis/assets/39027215/91fa4ada-7ebf-489d-bdf3-e83e38e91115)

## LockingMultiRewards

## Factorysol
![Factorysol](https://github.com/yongsxyz/Audit-Analysis/assets/39027215/142949a1-3519-4851-bd3f-b1a5d15f3727)

## BlastWrappers

## BlastOnboardingBoot
![BlastOnboardingBootsol](https://github.com/yongsxyz/Audit-Analysis/assets/39027215/6e0e4d66-ab14-4230-9838-513b52f40ce5)

## BlastOnboarding
![BlastOnboardingsol](https://github.com/yongsxyz/Audit-Analysis/assets/39027215/f6bda35e-6894-4d1a-b44b-50ad27bb94b4)

## BlastMagicLP
![BlastMagicLPsol](https://github.com/yongsxyz/Audit-Analysis/assets/39027215/c5a477be-7d34-4251-b854-f3c3e61ede6b)

## BlastGovernor
![BlastGovernorsol](https://github.com/yongsxyz/Audit-Analysis/assets/39027215/183c6e44-4a66-4fe0-8729-fbcb1be1fb02)

## BlastBox
![BlastBoxSol](https://github.com/yongsxyz/Audit-Analysis/assets/39027215/c10b1550-a60c-48e5-92f2-5444a23dc622)


# Centralization Risk

this risk can arise from several factors, such as the concentration of power within a single contract, the potential for malicious behavior by the contract owner, or the reliance on external precompiled contracts.

In the provided code snippets, several functions are marked as "onlyOwner", which means they can only be called by the contract owner. This can potentially lead to centralization risk if the owner becomes too powerful or influential within the system.
```
contract LockingMultiRewards is OperatableV2, Pausable {
contract MagicLP is ERC20, ReentrancyGuard, Owned {
contract Factory is Owned {
contract BlastOnboardingData is Owned, Pausable {

BlastBox.sol
68:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
BlastBox.sol
72:  function setFeeTo(address feeTo_) external onlyOwner {
BlastBox.sol
81:     function setTokenEnabled(address token, bool enabled) external onlyOwner {
BlastGovernor.sol
40:     function setFeeTo(address _feeTo) external onlyOwner {
BlastGovernor.sol
49:     function callBlastPrecompile(bytes calldata data) external onlyOwner {
BlastGovernor.sol
53:  function execute(address to, uint256 value, bytes calldata data) external onlyOwner returns (bool success, bytes memory result) {
BlastOnboarding.sol
147:     function setFeeTo(address feeTo_) external onlyOwner {
BlastOnboarding.sol
156:  function callBlastPrecompile(bytes calldata data) external onlyOwner {
BlastOnboarding.sol
160:     function claimGasYields() external onlyOwner returns (uint256) {
BlastOnboarding.sol
164:     function claimTokenYields(address[] memory tokens) external onlyOwner {
BlastOnboarding.sol
175:     function setTokenSupported(address token, bool supported) external onlyOwner {
BlastOnboarding.sol
185:     function setCap(address token, uint256 cap) external onlyOwner onlySupportedTokens(token) {
BlastOnboarding.sol
190:     function setBootstrapper(address bootstrapper_) external onlyOwner {
BlastOnboarding.sol
195:     function open() external onlyOwner onlyState(State.Idle) {
BlastOnboarding.sol
200: function close() external onlyOwner onlyState(State.Opened) {
BlastOnboarding.sol
205:     function rescue(address token, address to, uint256 amount) external onlyOwner {
BlastOnboarding.sol
214:     function pause() external onlyOwner {
BlastOnboarding.sol
218:     function unpause() external onlyOwner {
BlastOnboardingBoot.sol
96:     function bootstrap(uint256 minAmountOut) external onlyOwner onlyState(State.Closed) returns (address, address, uint256) {
BlastOnboardingBoot.sol
129:     function initialize(Router _router) external onlyOwner {
BlastOnboardingBoot.sol
137:     function setStaking(LockingMultiRewards _staking) external onlyOwner {
LockingMultiRewards.sol
317:    function setMinLockAmount(uint256 _minLockAmount) external onlyOwner {
LockingMultiRewards.sol
324:     function recover(address tokenAddress, uint256 tokenAmount) external onlyOwner {
LockingMultiRewards.sol
337:     function pause() external onlyOwner {
```
    

# Conclusion

In general, the Abracadabra Mimswap project exhibits an interesting and well-developed architecture we believe the team has done a good job regarding the code, but the identified risks need to be addressed, and measures should be implemented to protect the protocol from potential malicious use cases. Additionally, it is recommended to improve the documentation and comments in the code to enhance understanding and collaboration among developers. It is also highly recommended that the team continues to invest in security measures such as mitigation reviews, audits, and bug bounty programs to maintain the security and reliability of the project.



### Time spent:
23 hours