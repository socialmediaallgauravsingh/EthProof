# MyToken

The MyToken contract is an ERC-20 token implemented in Solidity. It allows for the creation, destruction, and management of tokens on the Ethereum network.
##Requirements
1. The contract has public variables that store the details about the coin:
   - `tokenName`: The name of the token (string).
   - `abbrv`: The abbreviation of the token (string).
   - `totalSupply`: The total supply of the token (unsigned integer).

2. The contract uses a mapping called balances to associate addresses with their corresponding token balances.

3. mint function: This function increases the total supply and the balance of a specified address by a given value.

- Parameters:
- Parameters:
     - `_address_of_eth`: The address to which the tokens will be minted.
     - `_value_of_int`: The amount of tokens to be minted.
   - Actions:
     - Increase the `totalSupply` by `_value_of_int`.
     - Increase the balance of the `_address_of_eth` by `_value_of_int`.
4. burn function: This function decreases the total supply and the balance of a specified address by a given value, here require statement also checks wheather Balance of that particular account is greater than or equal to No. of tokens to be burned, if it not meets the criteria then it throws an error by saying "Your Account have low Balance".

Parameters:
 - `_address_of_eth`: The address from which the tokens will be burned.
- `_value_of_int`: The amount of tokens to be burned.
- Actions:
- Checks if the balance of the _address_of_eth is greater than or equal to _value_of_int.
- If true, decreases the totalSupply by _value_of_int.
- Decreases the balance of the _address_of_eth by _value_of_int.

## Usage
1. Deploy the MyToken contract to a supported Ethereum network.

2. Once deployed, you can interact with the contract by calling the following functions:

- `mint`: Creates new tokens and assigns them to a specified address.

- Parameters:
 - `_address_of_eth`: The address to which the tokens will be minted.
- `_value_of_int`:  The amount of tokens to be minted.
- `burn`: Destroys existing tokens by reducing the total supply and the balance of a specified address.

- Parameters:
- `_address_of_eth`: The address from which the tokens will be burned.
- `_value_of_int`: The amount of tokens to be burned.
## License
This contract is licensed under the MIT License. SPDX-License-Identifier: MIT.
