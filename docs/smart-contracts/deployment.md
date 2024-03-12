# Deployment of Smart Contracts on Allfeat

Deploying your smart contracts to the Allfeat blockchain is the final step in making your DApps accessible to users. This guide outlines the process of deploying smart contracts on Allfeat, including preparing for deployment and using deployment tools.

## Prerequisites

- Completion of a smart contract using Solidity as described in [Developing Smart Contracts on Allfeat](developing.md).
- A running local or remote Allfeat node accessible via HTTP or WebSocket.

## Deployment Tools

### Polkadot{.js} Apps

The Polkadot{.js} Apps UI is a versatile tool that allows you to interact with the Allfeat blockchain directly from your web browser. It includes functionalities for deploying and interacting with smart contracts.

- **Access the Polkadot{.js} Apps UI**: Navigate to [https://polkadot.js.org/apps/](https://polkadot.js.org/apps/) and connect to your Allfeat node.

## Deploying Your Smart Contract

1. **Using Polkadot{.js} Apps UI**: 
   - Navigate to the "Developer" -> "Contracts" section.
   - Click on "Deploy a code" and upload your contract's `.contract` bundle file.
   - Follow the UI instructions to deploy your contract.

## Verifying the Deployment

After deploying your contract, verify its presence on the blockchain:

- **Polkadot{.js} Apps UI**: Navigate to the "Contracts" section and see if your contract appears in the list.
- **Subscan Explorer**: Use Allfeat's instance of the Subscan explorer to search for your contract's address and examine its transactions and status.

Congratulations! You have successfully deployed a smart contract to the Allfeat blockchain. Your DApp is now ready for interaction by users.

For more detailed information on smart contract deployment and interaction, consult the Polkadot{.js} documentation.
