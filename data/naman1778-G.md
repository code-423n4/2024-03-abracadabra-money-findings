## [G-01] Use assembly to write address storage values

When writing value for variables whose type is address, make use of assembly code instead of solidity code.

There are 16 instances of this issue in 8 files:

    File: src/blast/BlastBox.sol	

    33: feeTo = feeTo_;

    77: feeTo = feeTo_;

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol

    File: src/blast/BlastGovernor.sol	

    20: feeTo = feeTo_;

    45: feeTo = _feeTo;

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol

    File: src/blast/BlastMagicLP.sol	

    33: feeTo = feeTo_;

    86: feeTo = feeTo_;

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol

    File: src/blast/BlastOnboarding.sol	

    94: feeTo = feeTo_;

    152: feeTo = feeTo_;

    191: bootstrapper = bootstrapper_;

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol

    File: src/blast/BlastWrappers.sol	

    55:  _governor = governor_;

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol

    File: src/mimswap/auxiliary/FeeRateModel.sol	

    27: maintainer = maintainer_;

    51: maintainer = maintainer_;

    58: implementation = implementation_;

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol

    File: src/mimswap/periphery/Factory.sol	

    45: implementation = implementation_;

    101: implementation = implementation_;

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol

    File: src/staking/LockingMultiRewards.sol	

    135: stakingToken = _stakingToken;

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol

#### Test Code

    contract GasTest is DSTest {
        Contract0 c0;
        Contract1 c1;

        function setUp() public {
            c0 = new Contract0();
            c1 = new Contract1();
        }

        function testGas() public {
            c0.setOwnerAssembly(0xFD2dabe9DFcc4d88a12A9D0D40D834E81217Cccf);
            c1.setOwner(0xFD2dabe9DFcc4d88a12A9D0D40D834E81217Cccf);
        }
    }

    contract Contract0 {

        address owner;
        function setOwnerAssembly(address _owner) public {
            assembly{
                sstore(owner.slot,_owner)
            }
        }

    }

    contract Contract1 {
        address owner;
        function setOwner(address _owner) public {
            owner = _owner;
        }

    }

#### Gas Report

|  Contract0 contract                       |                 |       |        |       |         |
|-------------------------------------------|-----------------|-------|--------|-------|---------|
| Deployment Cost                           | Deployment Size |       |        |       |         |
| 35287                                     | 207             |       |        |       |         |
| Function Name                             | min             | avg   | median | max   | # calls |
| setOwnerAssembly                          | 22324           | 22324 | 22324  | 22324 | 1       |

|  Contract1 contract                       |                 |       |        |       |         |
|-------------------------------------------|-----------------|-------|--------|-------|---------|
| Deployment Cost                           | Deployment Size |       |        |       |         |
| 48499                                     | 273             |       |        |       |         |
| Function Name                             | min             | avg   | median | max   | # calls |
| setOwner                                  | 22363           | 22363 | 22363  | 22363 | 1       |

## [G-02] Use nested if and, avoid multiple check combinations

Using nested is cheaper than using && multiple check combinations. There are more advantages, such as easier to read code and better coverage reports.
 
There are 9 instances of this issue in 5 files:

    File: src/blast/BlastMagicLP.sol	

    120: if (!BlastMagicLP(address(implementation)).operators(msg.sender) && msg.sender != implementation.owner()) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol

    File: src/blast/BlastOnboarding.sol	

    114: if (caps[token] > 0 && totals[token].total > caps[token]) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol

    File: src/mimswap/MagicLP.sol	

    139: if (_RState_ == uint32(PMMPricing.RState.BELOW_ONE) && _BASE_RESERVE_ < _BASE_TARGET_) {

    144: if (_RState_ == uint32(PMMPricing.RState.ABOVE_ONE) && _QUOTE_RESERVE_ < _QUOTE_TARGET_) {

    302: if (baseBalance < _BASE_RESERVE_ && quoteBalance < _QUOTE_RESERVE_) {

    549: if (timeElapsed > 0 && _BASE_RESERVE_ != 0 && _QUOTE_RESERVE_ != 0) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol

    File: src/mimswap/periphery/Router.sol	

    527: if (quoteReserve > 0 && baseReserve > 0) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol

    File: src/staking/LockingMultiRewards.sol	

    326: if (tokenAddress == stakingToken && tokenAmount > stakingToken.balanceOf(address(this)) - stakingTokenBalance) {

    417: if (index == lastLockIndex[user] && locks.length > 1) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol

#### Test Code

    contract GasTest is DSTest {
        Contract0 c0;
        Contract1 c1;

        function setUp() public {
            c0 = new Contract0();
            c1 = new Contract1();
        }

        function testGas() public {
            c0.checkAge(19);
            c1.checkAgeOptimized(19);
        }
    }

    contract Contract0 {

        function checkAge(uint8 _age) public returns(string memory){
            if(_age>18 && _age<22){
                return "Eligible";
            }
        }

    }

    contract Contract1 {

        function checkAgeOptimized(uint8 _age) public returns(string memory){
            if(_age>18){
                if(_age<22){
                    return "Eligible";
                }
            }
        }
    }

#### Gas Report

| Contract0 contract                        |                 |     |        |     |         |
|-------------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                           | Deployment Size |     |        |     |         |
| 76923                                     | 416             |     |        |     |         |
| Function Name                             | min             | avg | median | max | # calls |
| checkAge                                  | 651             | 651 | 651    | 651 | 1       |

| Contract1 contract                        |                 |     |        |     |         |
|-------------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                           | Deployment Size |     |        |     |         |
| 76323                                     | 413             |     |        |     |         |
| Function Name                             | min             | avg | median | max | # calls |
| checkAgeOptimized                         | 645             | 645 | 645    | 645 | 1       |

## [G-03] Using XOR (^) and AND (&) bitwise equivalents

Given 4 variables a, b, c and d represented as such:

    0 0 0 0 0 1 1 0 <- a
    0 1 1 0 0 1 1 0 <- b
    0 0 0 0 0 0 0 0 <- c
    1 1 1 1 1 1 1 1 <- d

To have a == b means that every 0 and 1 match on both variables. Meaning that a XOR (operator ^) would evaluate to 0 ((a ^ b) == 0), as it excludes by definition any equalities.Now, if a != b, this means that there’s at least somewhere a 1 and a 0 not matching between a and b, making (a ^ b) != 0.Both formulas are logically equivalent and using the XOR bitwise operator costs actually the same amount of gas.However, it is much cheaper to use the bitwise OR operator (|) than comparing the truthy or falsy values.These are logically equivalent too, as the OR bitwise operator (|) would result in a 1 somewhere if any value is not 0 between the XOR (^) statements, meaning if any XOR (^) statement verifies that its arguments are different.

There are 4 instances of this issue in 2 files:

    File: src/mimswap/MagicLP.sol	

    102: if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {

    462: if (token == _BASE_TOKEN_ || token == _QUOTE_TOKEN_) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol

    File: src/mimswap/periphery/Router.sol	

    39: if (address(weth_) == address(0) || address(factory_) == address(0)) {

    599: if (baseDecimals == 0 || quoteDecimals == 0) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol

#### Test Code

    contract GasTest is DSTest {
        Contract0 c0;
        Contract1 c1;
        function setUp() public {
            c0 = new Contract0();
            c1 = new Contract1();
        }
        function testGas() public {
            c0.not_optimized(1,2);
            c1.optimized(1,2);
        }
    }
    
    contract Contract0 {
        function not_optimized(uint8 a,uint8 b) public returns(bool){
            return ((a==1) || (b==1));
        }
    }
    
    contract Contract1 {
        function optimized(uint8 a,uint8 b) public returns(bool){
            return ((a ^ 1) & (b ^ 1)) == 0;
        }
    }

#### Gas Report

| Contract0 contract                        |                 |     |        |     |         |
|-------------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                           | Deployment Size |     |        |     |         |
| 46099                                     | 261             |     |        |     |         |
| Function Name                             | min             | avg | median | max | # calls |
| not_optimized                             | 456             | 456 | 456    | 456 | 1       |


| Contract1 contract                        |                 |     |        |     |         |
|-------------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                           | Deployment Size |     |        |     |         |
| 42493                                     | 243             |     |        |     |         |
| Function Name                             | min             | avg | median | max | # calls |
| optimized                                 | 430             | 430 | 430    | 430 | 1       |

## [G-04] Use assembly to check for address(0)

Checking zero address can be improved by replacing the require statement with Assembly.Solidity has a lot of guardrails that can be removed (with care) for optimization purposes, especially for simple functionality like checking if an address is zero.

There are 26 instances of this issue in 12 files:

    File: src/blast/BlastBox.sol	

    25: if (feeTo_ == address(0)) {

    28: if (address(registry_) == address(0)) {

    73: if (feeTo_ == address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastBox.sol

    File: src/blast/BlastGovernor.sol	

    16: if (feeTo_ == address(0)) {

    41: if(_feeTo == address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastGovernor.sol

    File: src/blast/BlastMagicLP.sol	

    25: if (feeTo_ == address(0)) {

    28: if (address(registry_) == address(0)) {

    82: if (feeTo_ == address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastMagicLP.sol

    File: src/blast/BlastOnboarding.sol	

    85: if (address(registry_) == address(0)) {

    89: if (feeTo_ == address(0)) {

    148: if (feeTo_ == address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol

    File: src/blast/BlastOnboardingBoot.sol	

    97: if (pool != address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol

    File: src/blast/BlastTokenRegistry.sol	

    15: if (token == address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastTokenRegistry.sol

    File: src/blast/BlastWrappers.sol	

    21: if (governor_ == address(0)) {

    35: if (governor_ == address(0)) {

    48: if (governor_ == address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastWrappers.sol

    File: src/mimswap/MagicLP.sol	

    102: if (mtFeeRateModel == address(0) || baseTokenAddress == address(0) || quoteTokenAddress == address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/MagicLP.sol

    File: src/mimswap/auxiliary/FeeRateModel.sol	

    23: if (maintainer_ == address(0)) {

    35: if (implementation == address(0)) {

    47: if (maintainer_ == address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/auxiliary/FeeRateModel.sol

    File: src/mimswap/periphery/Factory.sol	

    39: if (implementation_ == address(0)) {

    42: if (address(maintainerFeeRateModel_) == address(0)) {

    97: if (implementation_ == address(0)) {

    106: if (address(maintainerFeeRateModel_) == address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Factory.sol

    File: src/mimswap/periphery/Router.sol	

    39: if (address(weth_) == address(0) || address(factory_) == address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol

    File: src/staking/LockingMultiRewards.sol	

    301: if (rewardToken == address(0)) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol

#### Test Code

    contract GasTest is DSTest {
        Contract0 c0;
        Contract1 c1;
        function setUp() public {
            c0 = new Contract0();
            c1 = new Contract1();
        }
        function testGas() public {
            c0.not_optimized(0x0000000000000000000000000000000000000001);
            c1.optimized(0x0000000000000000000000000000000000000001);
        }
    }
    
    contract Contract0 {
    
         function not_optimized(address addr) public pure{
             if(addr == address(0)){
                revert();
             }
         }
    }
    
    contract Contract1 {
    
         function optimized(address addr) public pure{
             assembly {
               if iszero(addr) {
                   revert(0x00, 0x20)
               }
             }
         }
    }

#### Gas Report

| Contract0 contract                        |                 |     |        |     |         |
|-------------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                           | Deployment Size |     |        |     |         |
| 41893                                     | 240             |     |        |     |         |
| Function Name                             | min             | avg | median | max | # calls |
| not_optimized                             | 258             | 258 | 258    | 258 | 1       |

| Contract1 contract                        |                 |     |        |     |         |
|-------------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                           | Deployment Size |     |        |     |         |
| 37687                                     | 219             |     |        |     |         |
| Function Name                             | min             | avg | median | max | # calls |
| optimized                                 | 252             | 252 | 252    | 252 | 1       |

## [G-05] Instead of counting down in *for* statements, count up

Counting down is more gas efficient than counting up because neither we are making zero variable to non-zero variable and also we will get gas refund in the last transaction when making non-zero to zero variable.

There are 8 instances of this issue in 3 files:

    File: src/blast/BlastOnboarding.sol	

    165: for (uint256 i = 0; i < tokens.length; i++) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboarding.sol

    File: src/mimswap/periphery/Router.sol	

    544: for (uint256 i = 0; i < iterations; ) {

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/mimswap/periphery/Router.sol

    File: src/staking/LockingMultiRewards.sol	

    405: for (uint256 i; i < users.length; ) {
    449:     unchecked {
    450:         ++i;
    451:     }

    547: for (uint256 i; i < rewardTokens.length; ) {
    549:     unchecked {
    550:         ++i;
    551:     }

    561: for (uint256 i; i < rewardTokens.length; ) {
    565:     unchecked {
    566:         ++i;
    567:     }

    575: for (uint256 i; i < rewardTokens.length; ) {
    589:     unchecked {
    590:         ++i;
    591:     }

    580: for (uint256 j; j < users.length; ) {
    584:     unchecked {
    585:         ++j;
    586:     }

    614: for (uint256 i; i < rewardTokens.length; ) {
    653:     unchecked {
    654:         ++i;
    655:     }

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/staking/LockingMultiRewards.sol

#### Test Code

    contract GasTest is DSTest {
        Contract0 c0;
        Contract1 c1;
        function setUp() public {
            c0 = new Contract0();
            c1 = new Contract1();
        }
        function testGas() public {
            c0.AddNum();
            c1.AddNum();
        }
    }


    contract Contract0 {
        uint256 num = 3;
        function AddNum() public {
            uint256 _num = num;
            for(uint i=0;i<=9;i++){
                _num = _num +1;
            }
            num = _num;
        }
    }


    contract Contract1 {
        uint256 num = 3;
        function AddNum() public {
            uint256 _num = num;
            for(uint i=9;i>=0;i--){
                _num = _num +1;
            }
            num = _num;
        }
    }

#### Gas Report

| Contract0 contract                        |                 |      |        |      |         |
|-------------------------------------------|-----------------|------|--------|------|---------|
| Deployment Cost                           | Deployment Size |      |        |      |         |
| 77011                                     | 311             |      |        |      |         |
| Function Name                             | min             | avg  | median | max  | # calls |
| AddNum                                    | 7040            | 7040 | 7040   | 7040 | 1       |

| Contract1 contract                        |                 |      |        |      |         |
|-------------------------------------------|-----------------|------|--------|------|---------|
| Deployment Cost                           | Deployment Size |      |        |      |         |
| 73811                                     | 295             |      |        |      |         |
| Function Name                             | min             | avg  | median | max  | # calls |
| AddNum                                    | 3819            | 3819 | 3819   | 3819 | 1       |

## [G-06] Stack variable used as a cheaper cache for a state variable is only used once

If the variable is only accessed once, it’s cheaper to use the state variable directly that one time, and save the 3 gas the extra stack assignment would spend.

There are 2 instances of this issue in 1 file:

    File: src/blast/BlastOnboardingBoot.sol	

    87: uint256 baseAmount = totals[MIM].locked;

    88: uint256 quoteAmount = totals[USDB].locked;

https://github.com/code-423n4/2024-03-abracadabra-money/blob/main/src/blast/BlastOnboardingBoot.sol

#### Test Code 

    contract GasTest is DSTest {
        Contract0 c0;
        Contract1 c1;
        function setUp() public {
            c0 = new Contract0();
            c1 = new Contract1();
        }
        function testGas() public {
            c0.not_optimized();
            c1.optimized();
        }
    }
    
    contract Contract0 {
        uint256 num = 5;
        uint256 sum;
        function not_optimized() public returns(bool){
            uint256 num1 = num;
            sum = num1 + 2;
        }
    }
    
    contract Contract1 {
        uint256 num = 5;
        uint256 sum;
        function optimized() public returns(bool){
            sum = num + 2;
        }
    }

#### Gas Report

| Contract0 contract                        |                 |       |        |       |         |
|-------------------------------------------|-----------------|-------|--------|-------|---------|
| Deployment Cost                           | Deployment Size |       |        |       |         |
| 63799                                     | 244             |       |        |       |         |
| Function Name                             | min             | avg   | median | max   | # calls |
| not_optimized                             | 24462           | 24462 | 24462  | 24462 | 1       |

| Contract1 contract                        |                 |       |        |       |         |
|-------------------------------------------|-----------------|-------|--------|-------|---------|
| Deployment Cost                           | Deployment Size |       |        |       |         |
| 63599                                     | 243             |       |        |       |         |
| Function Name                             | min             | avg   | median | max   | # calls |
| optimized                                 | 24460           | 24460 | 24460  | 24460 | 1       |