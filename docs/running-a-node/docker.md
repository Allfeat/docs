# Running a Local Node with Docker

Running Allfeat within a Docker container simplifies the setup and ensures a consistent environment across all platforms. Follow these steps to run your local Allfeat node using Docker.

## Prerequisites

Ensure Docker is installed and running on your system. If you haven't installed Docker yet, please refer to the [Installing Allfeat with Docker](../installation/docker.md) section.

## Running the Allfeat Node

After building the Allfeat Docker image, you can start your local node connected to Harmonie Testnet with the following command:

```bash
docker run docker.io/allfeatnetwork/allfeat:master
```

This command runs the Allfeat node inside a Docker container and exposes the necessary ports for P2P networking and JSON-RPC interfaces.

## Running the Allfeat Development Node

You can also start a locel development network by running with `--dev` argument:

```bash
docker run docker.io/allfeatnetwork/allfeat:master --dev
```

## Verifying the Node is Running

To verify that your Allfeat node is running inside Docker, you can use the following command:

```bash
docker ps
```
You should see your Allfeat container listed among the running containers.

## Interacting with the Node

You can interact with your Allfeat node using the JSON-RPC interface or by connecting to it using a substrate frontend template. Make sure to adjust the port forwarding settings in the Docker run command if you modify the default ports in the Allfeat node configuration.

## Stopping the Node

To stop your Allfeat node running inside Docker, use the Docker stop command followed by the container ID or name:

```bash
docker stop <container_id_or_name>
```
Congratulations! You have successfully run an Allfeat node locally using Docker. This setup allows you to develop and test your DApps or smart contracts in an environment that closely mimics a live blockchain network.

For more advanced Docker configurations and options, refer to the official Docker documentation.
