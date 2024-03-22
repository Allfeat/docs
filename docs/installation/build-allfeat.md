# Building Allfeat

Once your environment is correctly set up, you can build Allfeat from the sources by following these steps.

## Cloning the Allfeat Repository

Begin by cloning the Allfeat repository to your local machine and navigating to the Allfeat directory:

```bash
git clone https://github.com/Allfeat/Allfeat.git && cd Allfeat
```

## Compiling Allfeat

Use the command below to compile the Allfeat binary:

```bash
cargo build --locked --release
```

This process might take a while as it compiles the Allfeat codebase into an executable binary.

## Verifying the Installation

After the build is complete, confirm that Allfeat has been properly installed by checking the version of the compiled binary:

```bash
./target/release/allfeat -V
```

You should see Allfeat's version number in your terminal.

Congratulations! You have successfully built and installed Allfeat from the source. You are now ready to start your local Allfeat node, whether for development, testing, or as a validator node.

Refer to other sections in this documentation for information on node operation and advanced configuration options.