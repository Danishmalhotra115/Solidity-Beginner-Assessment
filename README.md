# MyToken-Smart-Contract

## Overview
MyToken is a simple ERC-20-like token smart contract written in Solidity. This contract allows minting and burning of tokens, and keeps track of token balances for different addresses.

## Requirements
The contract has public variables that store details about the token:

Token Name
Token Abbreviation
Total Supply
The contract maintains a mapping of addresses to token balances.

The contract includes a mint function to increase the total supply and the balance of a specified address.

The contract includes a burn function to decrease the total supply and the balance of a specified address, with a condition that ensures the address has sufficient tokens to burn.

## Contract Details
### Public Variables
string public tokenName - Stores the name of the token (e.g., "DANISH").
string public tokenAbbrv - Stores the abbreviation of the token (e.g., "DNS").
uint public totalSupply - Stores the total supply of the token, initialized to 0.
### Mapping
mapping(address => uint) public balances - Maps addresses to their token balances.
### Functions
function mint(address _address, uint _value) public:

Increases the total supply by _value.
Increases the balance of _address by _value.
function burn(address _address, uint _value) public:

Checks if _address has a balance greater than or equal to _value.
Decreases the total supply by _value.
Decreases the balance of _address by _value.
## Usage
### Deploying the Contract
To deploy the contract, use a Solidity-compatible development environment such as Remix, Truffle, or Hardhat. Ensure you have the appropriate version of the Solidity compiler (0.8.18).

Copy the contract code into your development environment.
Compile the contract.
Deploy the contract to your desired Ethereum network (e.g., local development network, testnet, or mainnet).
## Interacting with the Contract
After deployment, you can interact with the contract using the following functions:

mint(address _address, uint _value):

Mint new tokens by specifying the recipient address and the amount of tokens to mint.
burn(address _address, uint _value):

Burn existing tokens by specifying the address and the amount of tokens to burn. Ensure the specified address has a sufficient balance.
