# Running a Local Node without Docker

For developers and validators who prefer or need to run Allfeat directly on their native operating system without Docker, this guide will walk you through the process.

## Prerequisites

Ensure you have compiled Allfeat from source as described in the [Installing Allfeat from Source](../installation/from-source.md) section. Additionally, make sure your system meets the prerequisites outlined in the [Prerequisites](../prerequisites.md) document.

## Running the Allfeat Node

After compiling Allfeat, you can start your local node with the following command from the root of the Allfeat directory:

```bash
./target/release/allfeat --dev
```
This command starts the Allfeat node in development mode, making it easier to develop and test your DApps or smart contracts. The `--dev` flag resets the state with every restart, providing a fresh environment for each session.

## Verifying the Node is Running

To verify that your Allfeat node is running, open a new terminal window and use curl or any other tool to make a JSON-RPC call to the node:

```bash
curl -H "Content-Type: application/json" --data '{"jsonrpc":"2.0","method":"system_health","params":[],"id":1}' http://localhost:9933
```
You should receive a response indicating that the node is running and healthy.

## Stopping the Node

To stop your Allfeat node, simply press `Ctrl+C` in the terminal where the node is running. This will gracefully shut down the node and preserve the current state if not in `--dev` mode.

Congratulations! You have successfully run an Allfeat node locally without using Docker. This setup allows for deeper integration with your local development environment and can be more suitable for certain testing scenarios or continuous integration setups.

For more information on node configuration and advanced run options, refer to the Allfeat documentation and command-line help.
