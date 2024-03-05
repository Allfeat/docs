# Developing Smart Contracts on Allfeat

Developing smart contracts on Allfeat enables you to build powerful decentralized applications (DApps). This guide introduces you to the tools and frameworks required to start developing smart contracts on the Allfeat platform.

## Prerequisites

Before you begin, ensure you have a solid understanding of Rust programming language and smart contract basics. Familiarity with blockchain technology is also recommended.

## Smart Contract Development Tools

Allfeat supports smart contract development with multiple tools and frameworks. Here are some essential tools to get you started:

- **Ink!**: A Rust-based eDSL for writing Wasm smart contracts for blockchains built on the Substrate framework. It provides a seamless development experience for building on Allfeat.
  
  ```bash
  cargo install cargo-contract --force
  ```

- **Solang**: A Solidity compiler that targets Substrate and Solana, allowing you to write smart contracts in Solidity and deploy them on Allfeat.
  
  ```bash
  https://github.com/hyperledger-labs/solang
  ```

## Setting Up Your Development Environment

To set up your environment for Ink! development:

1. **Install Rust and Cargo**: Follow the instructions in the [Prerequisites](../prerequisites.md) section.
2. **Install the `cargo-contract` CLI tool**: This tool helps in creating, building, and testing smart contracts written in Ink!.

   ```bash
   cargo install cargo-contract --force
   ```

3. **Start a Local Allfeat Node**: Follow the instructions in [Running a Local Node without Docker](../running-a-node/without-docker.md) or [with Docker](../running-a-node/docker.md) to start your local Allfeat node.

## Developing Your First Smart Contract

To create your first smart contract with Ink!:

1. **Create a New Ink! Project**:

   ```bash
   cargo contract new my_contract
   ```

2. **Navigate to Your Project Directory**:

   ```bash
   cd my_contract
   ```

3. **Build Your Smart Contract**:

   ```bash
   cargo contract build
   ```

4. **Test Your Smart Contract**:

   ```bash
   cargo contract test
   ```

5. **Deploy Your Smart Contract**: Use the Polkadot{.js} Apps UI or any other method to deploy your smart contract to the Allfeat node.

## Next Steps

- **Explore Ink! Documentation**: Deep dive into the Ink! documentation to learn more about smart contract development.
- **Join the Allfeat Developer Community**: Engage with other developers and share your experiences.

Congratulations! You have taken your first steps into smart contract development on Allfeat. The world of blockchain development is vast and exciting—keep building and exploring!

