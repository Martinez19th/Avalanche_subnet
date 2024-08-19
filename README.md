# Defi Empire

Defi Empire is a simplified clone of a DeFi Kingdom, implemented on Avalanche Subnets using Solidity smart contracts. The project aims to provide a straightforward example of how decentralized finance applications can be built on Avalanche leveraging on their subnet, focusing on basic functionalities like token management and a vault system.

## Smart Contracts Overview

### ERC20 Token

The `ERC20` contract defines a basic ERC20 token with functionalities for transferring tokens, approving spending, minting new tokens, and burning existing tokens and it follows the ERC20 standard.

### Vault

The `Vault` contract manages user deposits and withdrawals of ERC20 tokens. Users can deposit tokens into the vault, which mints shares for the depositor based on the deposited amount and current vault holdings. Shares can later be burned to withdraw tokens, with the amount withdrawn based on the proportion of shares held relative to the total shares in the vault.

## Usage

### Setting Up

To deploy and interact with the contracts:
1. Deploy the `ERC20` token contract on Avalanche Subnets.
2. Deploy the `Vault` contract, specifying the address of the deployed ERC20 token contract.

### Interacting with the Contracts

- **ERC20 Token**: Use standard ERC20 functions (`transfer`, `approve`, `transferFrom`, `balanceOf`, etc.) to manage tokens.
  
- **Vault**: 
  - **Deposit**: Call `deposit(uint _amount)` to deposit tokens into the vault. If it's the first deposit, shares will be minted based on the deposited amount.
  - **Withdraw**: Call `withdraw(uint _shares)` to burn shares and withdraw tokens based on the proportion of shares burned relative to the total shares in the vault.
