# MyToken Solidity Contract

## Overview
The `MyToken` contract is a basic token implementation written in Solidity. It provides functionality for minting and burning tokens and tracks balances associated with addresses. This is a minimalistic example of how a token system works on the Ethereum blockchain.

### Key Features:
- Mint new tokens to a specific address.
- Burn tokens from a specific address (given sufficient balance).
- Track balances of different addresses.
- Track the total supply of tokens.

## Token Details
- **Token Name**: MyToken
- **Token Symbol**: MTK
- **Solidity Version**: 0.8.18

## Contract Details

### State Variables
- `string public tokenName`: Holds the name of the token, which is set as `"MyToken"`.
- `string public tokenAbbrv`: Holds the abbreviation of the token, set as `"MTK"`.
- `uint256 public totalSupply`: Tracks the total supply of the token in circulation.
- `mapping(address => uint256) public balances`: Stores the balance of each address.

### Functions

#### 1. `mint(address _to, uint256 _value)`
Mints new tokens and assigns them to a specific address.

- **Parameters**:
  - `_to`: The address to which the newly minted tokens are assigned.
  - `_value`: The number of tokens to mint.
  
- **Behavior**:
  - Increases the `totalSupply` by the `_value`.
  - Increases the balance of the `_to` address by `_value`.

- **Example**:
  ```solidity
  mint(0x1234567890abcdef, 100);  // Mints 100 tokens to the specified address.
