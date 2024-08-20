---

# Martinez ERC20 Token & Vault on Avalanche Subnet

## Project Overview
The **Martinez** project is a decentralized ERC20 token system deployed on a custom blockchain network, the Martinez network, powered by the Avalanche Subnet. This setup allows for high performance, scalability, and customization, making the Martinez network uniquely suited for its token and vault operations. The Martinez token is represented by the symbol `mat`, and operates with 18 decimals for precision in transactions.

### Why Avalanche Subnet?
The Martinez network utilizes Avalanche Subnets, a framework that enables the creation of a customized, isolated blockchain. This allows the network to maintain:
- **Scalability:** Supports high throughput with low latency, ensuring efficient transaction processing even as the network grows.
- **Customizability:** Tailors blockchain parameters such as consensus rules, virtual machines, and governance models to suit the Martinez ecosystem's specific needs.
- **Interoperability:** Facilitates seamless interaction with the broader Avalanche ecosystem and other blockchain networks through cross-chain bridges, enhancing the utility and reach of the Martinez token.

## ERC20 Token Contract

### Key Features:
- **Name:** Martinez
- **Symbol:** `mat`
- **Decimals:** 18
- **Total Supply:** The total supply of `mat` tokens is dynamic, controlled by the minting and burning functions.

### Functions:
- **transfer:** Transfers `mat` tokens from the sender to a specified recipient.
- **approve:** Approves a spender to manage a certain amount of tokens on behalf of the owner.
- **transferFrom:** Allows a spender to transfer tokens from an approved address.
- **mint:** Increases the total supply by minting new tokens to the caller's address.
- **burn:** Decreases the total supply by burning tokens from the caller's address.

## Vault Contract

### Overview:
The Vault contract is a secure repository that allows users to deposit `mat` tokens and receive shares that represent their stake in the vault's total token balance. These shares can be redeemed for `mat` tokens at a later time.

### Key Functions:
- **deposit:** Users deposit `mat` tokens into the vault and receive a proportional number of shares. The shares represent ownership of a fraction of the total tokens held in the vault.
- **withdraw:** Users redeem their shares for `mat` tokens. The amount received is proportional to the number of shares redeemed relative to the total supply of shares.

### Mathematical Details:
- **Deposit:** When depositing, the number of shares minted is calculated as follows:
  \[
  \text{shares} = \frac{\text{amount} \times \text{totalSupply}}{\text{vaultBalance}}
  \]
- **Withdraw:** When withdrawing, the amount of tokens returned is calculated as:
  \[
  \text{amount} = \frac{\text{shares} \times \text{vaultBalance}}{\text{totalSupply}}
  \]

## Installation and Deployment

### Prerequisites:
- Solidity compiler version 0.8.17 or higher.
- Ethereum development environment (e.g., Hardhat, Truffle).
- Access to the Martinez network via the Avalanche Subnet (Chain ID: 20240819).

### Deployment:
1. **Compile Contracts:** Use your development environment to compile the ERC20 and Vault contracts.
2. **Deploy ERC20 Contract:** Deploy the ERC20 token contract on the Martinez network.
3. **Deploy Vault Contract:** Deploy the Vault contract, passing in the address of the ERC20 token contract.

### Interaction:
- **Tools:** Use Web3-compatible interfaces such as Remix, Hardhat, or Truffle to interact with the contracts.
- **Functions:** Interact with the `deposit`, `withdraw`, `transfer`, `approve`, and `transferFrom` functions via the deployed contract addresses.

## Avalanche Subnet Integration

The Martinez network is built on the Avalanche Subnet, which ensures:
- **Enhanced Security:** The Avalanche consensus protocol provides strong security, ensuring the integrity and safety of transactions on the Martinez network.
- **Custom Governance:** The network can implement unique governance structures, allowing for tailored decision-making processes.
- **Energy Efficiency:** The Avalanche consensus is optimized for energy efficiency, minimizing the environmental impact of running the Martinez network.

## Author

This project was developed and maintained by:

- **Martins M** - Developer

## License
This project is licensed under the MIT License. For more details, see the [LICENSE](LICENSE) file.

---

This README provides a comprehensive overview of the project, highlighting the key aspects of the Martinez ERC20 token and Vault contracts, as well as the critical role of the Avalanche Subnet in the network's creation.
