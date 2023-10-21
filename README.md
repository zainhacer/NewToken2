# NewToken2
Explain All Features

* `name()`: Returns the name of the token.
* `symbol()`: Returns the symbol of the token.
* `decimals()`: Returns the number of decimals the token has.
* `totalSupply()`: Returns the total supply of the token.
* `balanceOf(address)`: Returns the balance of the given address.
* `allowance(address, address)`: Returns the allowance of the given spender for the given owner.
* `transfer(address, uint256)`: Transfers the given amount of tokens to the given address.
* `approve(address, uint256)`: Approves the given spender to transfer the given amount of tokens on behalf of the caller.
* `transferFrom(address, address, uint256)`: Transfers the given amount of tokens from the given sender to the given recipient.
* `renounceOwnership()`: Renounces ownership of the contract.
* `isSell(address)`: Returns whether the given address is selling tokens.
* `buyTax()`: Returns the buy tax.
* `sellTax()`: Returns the sell tax.
* `burningWallet()`: Returns the burning wallet address.

In addition to these functions, the contract also has the following modifiers:

* `onlyOwner`: Ensures that the caller is the owner of the contract.

**Explanation of functions:**

* `transfer(address, uint256)`: This function transfers the given amount of tokens from the caller's address to the given recipient address. If the caller is selling tokens, a sell tax will be applied. The sell tax is a percentage of the amount of tokens being sold that is sent to the burning wallet. The burning wallet is an address that is used to burn tokens, which reduces the circulating supply of the token.
* `approve(address, uint256)`: This function approves the given spender to transfer the given amount of tokens on behalf of the caller. For example, if a user wants to allow a decentralized exchange (DEX) to trade their tokens, they would call the `approve()` function on the token contract with the DEX's address and the amount of tokens they want to allow the DEX to trade.
* `transferFrom(address, address, uint256)`: This function transfers the given amount of tokens from the given sender address to the given recipient address. The caller must have been approved by the sender to transfer at least the given amount of tokens.
* `renounceOwnership()`: This function renounces ownership of the contract. Once ownership has been renounced, the contract cannot be modified.
* `isSell(address)`: This function returns whether the given address is selling tokens. An address is considered to be selling tokens if they are transferring tokens to an address other than the burning wallet or the owner of the contract.
* `buyTax()`: Returns the buy tax.
* `sellTax()`: Returns the sell tax.
* `burningWallet()`: Returns the burning wallet address.
