# Running Your Node as a Validator on Allfeat

After initializing your node as detailed in the [Initializing a Validator Node on Allfeat (prerequisites)](prerequisites.md) section, you're ready to start your journey as a validator. This guide will walk you through running your node as a validator and joining the Allfeat validator set.

## Prerequisites

Ensure that your node has been:

- Configured with the necessary validator keys. ([here](prerequisites.md))

## Starting Your Validator Node

To start your node in validator mode, run the following command:

```bash
./target/release/allfeat --base-path /path/to/node/data --name MyValidatorNode --telemetry-url 'wss://telemetry.polkadot.io/submit/ 0' --validator
```
Make sure to replace `/path/to/node/data` with your actual data directory and `MyValidatorNode` with the name you want to give your node.

## Joining the Validator Set

To participate in the consensus and be eligible for block production and rewards, your node must be selected into the validator set. This involves:

1. **Staking Tokens**: Lock a certain amount of tokens as stake. This acts as a security deposit, ensuring validators act in the network's best interest.

      - Use the Polkadot{.js} Apps UI to stake tokens and nominate your validator.

2. **Setting Session Keys**: Inform the network about your validator's session keys.

      - This is done through a transaction, which can also be submitted via the Polkadot{.js} Apps UI.

3. **Waiting for the Next Era**: Validator selection happens at the beginning of each era. Your node will start validating if it's chosen for the active validator set.

## Monitoring Your Validator

It's crucial to monitor your validator's performance and status:

- **Telemetry**: Connect your node to Allfeat's telemetry service to monitor its status and metrics.
- **Logs**: Regularly check your node's logs for warnings, errors, or any signs of misbehavior.

## Maintaining Your Validator

Running a validator node requires diligent maintenance:

- **Keep Your Node Updated**: Regularly update your node software to the latest version.
- **Secure Your Validator**: Implement security best practices to protect your node from attacks.
- **Be Active**: Ensure your node remains online and active. Downtime can result in penalties or slashing.

Congratulations! You are now running a validator node on Allfeat. By participating as a validator, you play a critical role in securing the network and processing transactions.

Remember, being a validator comes with responsibilities. Maintaining your node's security and operation is crucial for the health of the network and the security of your staked tokens.
