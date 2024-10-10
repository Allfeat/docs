# Installing Allfeat with Docker

Docker provides a straightforward and isolated environment for running Allfeat nodes. This guide walks you through the process of setting up Allfeat using Docker.

## Installing Docker

Before running Allfeat inside a Docker container, you must have Docker installed on your machine. Please refer to the [Prerequisites](../prerequisites.md) section for Docker installation instructions.

## Pulling the docker image

First, pull the docker image based on the Master branch of the Allfeat repository:

```bash
docker pull allfeatnetwork/allfeat:master 
```

## Running Allfeat Inside Docker

Then, to run Allfeat inside a Docker container, simply use the following command:

```bash
docker run docker.io/allfeatnetwork/allfeat:master
```

Congratulations! You've successfully set up and run Allfeat inside a Docker container. This setup allows you to run a local Allfeat node for development, testing, production and validation purposes.

For additional configurations and advanced Docker options, refer to the official Docker documentation.
