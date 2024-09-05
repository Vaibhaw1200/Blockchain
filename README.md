MyToken Smart Contract
Overview
This Solidity program defines a simple ERC-20-like token called KABADDICHAMPION with symbol KCC. The contract allows minting and burning of tokens, along with managing token balances for each user. This contract can be used as a foundation for creating your own cryptocurrency or in applications that require token management on the Ethereum blockchain.

Features
Mint Tokens: The mint function allows adding new tokens to the total supply and assigning them to a specified address.
Burn Tokens: The burn function enables reducing the token supply by burning tokens from a specific address.
Manage Balances: The contract maintains a balance for each address that holds tokens.
Supply Tracking: The total supply of tokens is tracked and updated through minting and burning operations.
Code Overview
State Variables
tokenName: The name of the token (KABADDICHAMPION).
tokenAbbrv: The abbreviation or symbol of the token (KCC).
totalSupply: Tracks the total number of tokens in circulation.
balances: A mapping that associates each address with its token balance.
Functions
mint(address _to, uint256 _value):

Mints new tokens and adds them to the balance of the specified address (_to).
The total supply of tokens increases by the value of _value.
Prevents minting to the zero address (0x0000000000000000000000000000000000000000).
burn(address _from, uint256 _value):

Burns tokens from the balance of the specified address (_from), decreasing the total supply.
Ensures that the _from address has enough tokens to burn.
Prevents burning from the zero address.
How to Run
Prerequisites
You will need a Solidity compiler (such as Remix) to deploy and interact with the contract.
Steps to Deploy and Test
Deploy the Contract:

Copy the Solidity code into Remix.
Set the compiler version to 0.8.18.
Deploy the contract on the desired Ethereum test network or local blockchain environment.
Minting Tokens:

Use the mint function to add tokens to any address.
Example: Call mint(0xYourAddress, 1000) to add 1000 tokens to your account.
Burning Tokens:

Use the burn function to burn tokens from a specific address.
Example: Call burn(0xYourAddress, 500) to burn 500 tokens from your balance.
Check Balances:

The balances mapping allows you to check the token balance of any address.
Example: Call balances(0xYourAddress) to see the current balance.
Example Usage
solidity
Copy code
// Mint 1000 tokens to an address
mint(0x123...abc, 1000);

// Burn 500 tokens from the same address
burn(0x123...abc, 500);

// Check the balance of an address
balances(0x123...abc); // returns 500
