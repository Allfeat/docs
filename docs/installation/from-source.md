# Installing Allfeat from Source

Compiling Allfeat from the source code offers the most flexibility for customization and optimization. Follow these steps to set up your Allfeat node by compiling it directly from the source.

## Prerequisites

Ensure you have Rust and Cargo installed on your system. For Rust installation, please refer to the [Prerequisites](../prerequisites.md) document. You also need Git for cloning the repository.

## Cloning the Allfeat Repository

To get started, clone the Allfeat repository to your local machine:

```bash
git clone https://github.com/Allfeat/Allfeat.git && cd Allfeat
```


## Updating Rust and Adding Necessary Components

Make sure your Rust installation is up to date, and add the necessary components for compiling Allfeat:

```bash
rustup update && rustup show
rustup target add wasm32-unknown-unknown
rustup component add rust-src
```

## Compiling Allfeat

Compile the Allfeat binary with the following command:

```bash
cargo build --locked --release
```

This step may take some time as it compiles the entire Allfeat codebase into a runnable binary.

## Verifying the Installation

Once the build process is complete, you can verify that Allfeat has been installed correctly by checking the version of the compiled binary:

```bash
./target/release/allfeat -V
```

You should see the version number of Allfeat displayed in your terminal.

Congratulations! You have successfully compiled and installed Allfeat from the source code. You're now ready to run your local Allfeat node for development, testing, or even as a validator node.

For more information on running your node and advanced configuration options, refer to the following sections of this documentation.
