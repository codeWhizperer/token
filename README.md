# MyToken Solidity Smart Contract

## Overview
This Solidity smart contract, named MyToken, is designed to create and manage a basic ERC-20 token. The contract includes functionality for minting new tokens and burning existing tokens, along with storage for essential token details.

## Token Details
- **Name**: [Token Name]
- **Symbol**: [Token Symbol]
- **Total Supply**: [Initial Total Supply]

## Functions

### Mint
The contract provides a `mint` function, allowing the creation of new tokens. This function takes two parameters: the recipient's address and the amount of tokens to be minted. The total supply is increased by the specified amount, and the recipient's balance is updated accordingly.

```solidity
function mint(address _recipient, uint256 _amount) external
```
### Burn
To reduce the total supply and eliminate existing tokens, the contract includes a burn function. Similar to the mint function, the burn function requires the recipient's address and the amount of tokens to be burned. The function checks if the sender's balance is sufficient before deducting the specified amount from both the total supply and the sender's balance.

```solidity
function burn(address _recipient, uint256 _amount) external
```

### Usage
- Deploy the MyToken contract, providing the token name and symbol as constructor parameters.
- Utilize the mint function to create new tokens, specifying the recipient's address and the amount to be minted.
- Use the burn function to eliminate existing tokens, ensuring that the sender's balance is sufficient for the specified burn amount.

### Example

```solidity
MyToken myToken = new MyToken("MyTokenName", "MTN");
myToken.mint(address1, 1000);
myToken.burn(address1, 500);
```

