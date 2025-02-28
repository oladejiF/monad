# monad
forge init --template monad-developers/foundry-monad [project_name]

Alternatively, you can create a foundry project using the command below:

forge init [project_name]

4. Modify Foundry configuration
Update the foundry.toml file to add Monad Testnet configuration.

[profile.default]
src = "src"
out = "out"
libs = ["lib"]

# Monad Testnet Configuration
eth-rpc-url="https://testnet-rpc.monad.xyz"
chain_id = 10143

5. Write a smart contract
You can write your smart contracts under the src folder. There is already a Counter contract in the project located at src/Counter.sol.

// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.13;

contract Counter {
    uint256 public number;

    function setNumber(uint256 newNumber) public {
        number = newNumber;
    }

    function increment() public {
        number++;
    }
}

6. Compile the smart contract
forge compile

Compilation process output can be found in the newly created out directory, which includes contract ABI and bytecode.

7. Deploy the smart contract
note
For deploying contracts, we recommend using keystores instead of private keys.
contract adding
