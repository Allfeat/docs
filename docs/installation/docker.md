# Installing Allfeat with Docker

Docker provides a straightforward and isolated environment for running Allfeat nodes. This guide walks you through the process of setting up Allfeat using Docker.

## Installing Docker

Before running Allfeat inside a Docker container, you must have Docker installed on your machine. Please refer to the [Prerequisites](../prerequisites.md) section for Docker installation instructions.

## Cloning the Allfeat Repository

First, clone the Allfeat repository to your local machine:

```bash
git clone https://github.com/Allfeat/Allfeat.git && cd Allfeat
```

## Building the Docker Image

Once you have the repository, you can build the Docker image using the Dockerfile provided:

```bash
docker build -t allfeat .
```

This command builds a Docker image named `allfeat` based on the instructions in the Dockerfile.

## Verifying the Docker Image

After the build process completes, you can verify that the Docker image has been created successfully:

```bash
docker images | grep allfeat
```

You should see the `allfeat` image listed in the output.

## Running Allfeat Inside Docker

To run Allfeat inside a Docker container, use the following command:

```bash
docker run -p 9944:9944 -p 9933:9933 -p 30333:30333 allfeat
```

This command starts a container from the Allfeat image and maps the necessary ports for the Allfeat node to communicate with the outside world.

Congratulations! You've successfully set up and run Allfeat inside a Docker container. This setup allows you to run a local Allfeat node for development, testing, or validation purposes.

For additional configurations and advanced Docker options, refer to the official Docker documentation.
