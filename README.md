

# MyToken Contract

This contract implements a basic token contract with minting and burning functions.

## Requirements

1. The contract has public variables that store the details about the token, including:
   - `tokenname`: A string variable representing the name of the token (e.g., "Ether").
   - `tokenabriv`: A string variable representing the abbreviation of the token (e.g., "Eth").
   - `supply`: An unsigned integer variable representing the total supply of the token.

2. The contract has a mapping of addresses to balances. Each address is associated with a balance of tokens.

3. The contract has a `mint` function that takes two parameters: an address and a value. This function increases the total supply by the specified value and increases the balance of the "sender" address by that amount.

4. The contract has a `burn` function that works opposite to the `mint` function. It takes an address and a value as parameters. This function deducts the specified value from the total supply and from the balance of the "sender" address.

5. The `burn` function includes conditionals to ensure that the balance of the "sender" is greater than or equal to the amount that is supposed to be burned.

## Usage

The contract provides the following functions:

### `mint(address _address, uint a)`

This function mints new tokens and increases the total supply and balance of the specified address.

- `address _address`: The address for which the tokens will be minted.
- `uint a`: The amount of tokens to mint.

### `burn(address _address, uint a)`

This function burns tokens and decreases the total supply and balance of the specified address.

- `address _address`: The address from which the tokens will be burned.
- `uint a`: The amount of tokens to burn.

Please note that when calling the `burn` function, the balance of the "sender" address must be greater than or equal to the amount to be burned, otherwise the burn operation will not be executed.

## License

This contract is released under the MIT License. You can find the full license text in the contract file.
