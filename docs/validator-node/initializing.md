# Initializing a Validator Node on Allfeat

Becoming a validator on the Allfeat network involves setting up and initializing your node to participate in the consensus process. This guide provides the steps necessary to prepare your node for validator duties.

## Prerequisites

Before initializing your node, ensure you have:

- Successfully installed Allfeat from source or Docker as described in the [Installation and Configuration](../installation/docker.md) section.
- A secure and reliable server environment that meets the recommended [system requirements](../prerequisites.md).

## Initializing the Node

1. **Download the Genesis File**: Obtain the latest genesis file (`harmonie-raw.json`) from the Allfeat repository or your network administrator.

2. **Initialize Your Node**:
   
   Using the genesis file, initialize your node's database:

```bash
./target/release/allfeat --chain=./path/to/harmonie-raw.json --base-path /path/to/node/data init
```
   Replace `/path/to/harmonie-raw.json` with the actual path to the genesis file and `/path/to/node/data` with the desired location for your node's data.

## Setting Up Validator Keys

Validators must securely manage their keys. Allfeat uses the SR25519 and ED25519 key types for validator operations.

1. **Generate Keys**:

   - **Session Key**:
   
```bash
./target/release/allfeat key generate-session-keys --base-path /path/to/node/data
```
2. **Insert Keys into the Keystore**:

   Use the Polkadot{.js} Apps UI or command-line tools to insert your keys into the node's keystore.

## Configuring Your Node as a Validator

After initializing your node and setting up the keys, configure it to run as a validator:

```bash
./target/release/allfeat --base-path /path/to/node/data --name MyValidatorNode --validator
```
Replace `MyValidatorNode` with your desired node name.

## Verifying the Setup

Ensure your node is correctly set up and synced with the network before declaring your intentions to validate. Use telemetry or the Polkadot{.js} Apps UI to monitor your node's status and connectivity.

Congratulations! Your node is now initialized and configured to operate as a validator on the Allfeat network. The next steps involve staking and declaring your validator intentions on the network.

For detailed instructions on staking and participating in consensus, refer to the Allfeat staking guide and validator resources.
