# Prerequisites for Running Allfeat

Before you dive into Allfeat, there are a few prerequisites you'll need to have in place. This guide outlines the necessary steps to prepare your environment for running a local node, developing DApps, or becoming a validator on the Allfeat network.

## System Requirements

To run Allfeat smoothly, your system should meet the following minimum requirements:

- **Operating System**: Ubuntu 18.04 or later, macOS, or a compatible Linux distribution
- **Processor**: Intel Core i5 or equivalent
- **Memory**: 8 GB RAM
- **Storage**: 50 GB available space

## Software Dependencies

### Docker

Allfeat nodes can be run inside Docker containers for ease of setup and isolation. If you choose to use Docker, you must install it first:

- **Ubuntu/Linux**: [Install Docker](https://docs.docker.com/engine/install/ubuntu/)
- **macOS**: [Install Docker Desktop for Mac](https://docs.docker.com/docker-for-mac/install/)
- **Windows**: [Install Docker Desktop for Windows](https://docs.docker.com/docker-for-windows/install/)

### Rust and required packages

For building Allfeat and running a node from source, Rust is required:

- **Install Rust**: Follow the instructions on the [official Rust website](https://www.rust-lang.org/tools/install).

To successfully build Allfeat, some external packages are required: 

### Git

Git is required to clone the Allfeat repository:

- **Install Git**: Follow the installation guide on the [Git website](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

## Additional Tools

Depending on your development needs, you might also need the following:

- **Node.js and npm**: For developing and testing DApps.
- **Web3.js or Ethers.js**: Libraries for interacting with Ethereum-based blockchains.

Once you have completed these steps, you're ready to start working with Allfeat. The next section of this documentation will guide you through the process of running a local node.

