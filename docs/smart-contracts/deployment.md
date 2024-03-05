# Deployment of Smart Contracts on Allfeat

Deploying your smart contracts to the Allfeat blockchain is the final step in making your DApps accessible to users. This guide outlines the process of deploying smart contracts on Allfeat, including preparing for deployment and using deployment tools.

## Prerequisites

- Completion of a smart contract using Ink! or Solang as described in [Developing Smart Contracts on Allfeat](developing.md).
- A running local or remote Allfeat node accessible via HTTP or WebSocket.

## Deployment Tools

### Polkadot{.js} Apps

The Polkadot{.js} Apps UI is a versatile tool that allows you to interact with the Allfeat blockchain directly from your web browser. It includes functionalities for deploying and interacting with smart contracts.

- **Access the Polkadot{.js} Apps UI**: Navigate to [https://polkadot.js.org/apps/](https://polkadot.js.org/apps/) and connect to your Allfeat node.

### cargo-contract CLI

The `cargo-contract` CLI tool, used for developing Ink! smart contracts, also provides functionalities for deploying contracts.

```bash
cargo contract deploy --node <node_url> --suri <secret_uri> --name <contract_name>
```
Replace `<node_url>`, `<secret_uri>`, and `<contract_name>` with your node's WebSocket URL, your account's secret URI, and the name of your contract, respectively.

## Preparing for Deployment

1. **Build Your Smart Contract**: Ensure your smart contract is compiled and optimized for deployment.

   ```bash
cargo contract build --release
```
2. **Generate Contract Metadata**: Generate metadata for your contract, which is necessary for interaction after deployment.

   ```bash
cargo contract generate-metadata
```
## Deploying Your Smart Contract

1. **Using Polkadot{.js} Apps UI**: 
   - Navigate to the "Developer" -> "Contracts" section.
   - Click on "Deploy a code" and upload your contract's `.contract` bundle file.
   - Follow the UI instructions to deploy your contract.

2. **Using cargo-contract CLI**:
   - Ensure your local node is running or you have the URL of a remote Allfeat node.
   - Use the `cargo contract deploy` command with the appropriate flags for your contract and account.

## Verifying the Deployment

After deploying your contract, verify its presence on the blockchain:

- **Polkadot{.js} Apps UI**: Navigate to the "Contracts" section and see if your contract appears in the list.
- **Subscan Explorer**: Use Allfeat's instance of the Subscan explorer to search for your contract's address and examine its transactions and status.

Congratulations! You have successfully deployed a smart contract to the Allfeat blockchain. Your DApp is now ready for interaction by users.

For more detailed information on smart contract deployment and interaction, consult the Ink! and Polkadot{.js} documentation.

