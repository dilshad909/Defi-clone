# ERC20 and Vault Smart Contracts

This repository contains an implementation of an ERC20 token and a vault contract in Solidity. The ERC20 token follows the standard token interface, while the vault allows users to deposit and withdraw tokens, managing shares in return.

## Table of Contents

- [Overview](#overview)
- [ERC20 Token](#erc20-token)
- [Vault Contract](#vault-contract)
- [Usage](#usage)
- [License](#license)

## Overview

The smart contracts implemented in this repository provide the functionality to create an ERC20 token and manage a vault for holding and handling token deposits and withdrawals.

## ERC20 Token

The `ERC20` contract implements the ERC20 token standard with the following features:

- **Total Supply**: Keeps track of the total supply of tokens.
- **Balance Tracking**: Maintains a mapping of addresses to their token balances.
- **Allowance Management**: Allows users to approve other addresses to spend tokens on their behalf.
- **Transfer Functionality**: Enables the transfer of tokens between users.
- **Minting and Burning**: Allows for the creation and destruction of tokens.

### Key Functions

- `transfer(address recipient, uint amount)`: Transfers tokens from the caller to the recipient.
- `approve(address spender, uint amount)`: Approves a spender to use a certain amount of tokens.
- `transferFrom(address sender, address recipient, uint amount)`: Transfers tokens from one address to another using the allowance mechanism.
- `mint(uint amount)`: Mints new tokens and increases the total supply.
- `burn(uint amount)`: Burns tokens, reducing the total supply.

## Vault Contract

The `Vault` contract interacts with the ERC20 token to manage deposits and withdrawals of tokens while issuing shares in return.

### Key Functions

- `deposit(uint _amount)`: Allows users to deposit tokens into the vault, minting shares based on the deposited amount.
- `withdraw(uint _shares)`: Allows users to withdraw tokens from the vault by burning their shares.

## Usage

To deploy these contracts, you will need:

1. A compatible Ethereum wallet (e.g., MetaMask).
2. A development environment (e.g., Hardhat or Truffle).
3. The relevant Solidity compiler version (0.8.17).

### Deployment Steps

1. Compile the contracts.
2. Deploy the `ERC20` token contract.
3. Deploy the `Vault` contract, passing the address of the `ERC20` token as a parameter.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
