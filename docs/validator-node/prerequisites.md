# Prerequisites to become a Validator Node on Allfeat

Becoming a validator on the Allfeat network involves setting up and initializing your node to participate in the consensus process. This guide provides the steps necessary to prepare your node for validator duties.

## Prerequisites

Before initializing your node, ensure you have:

- Successfully installed Allfeat from source or Docker as described in the [Installation and Configuration](../installation/docker.md) section.
- A secure and reliable server environment that meets the recommended [system requirements](../prerequisites.md).

## Generate your keys

You will need to have [subkey](https://docs.substrate.io/reference/command-line-tools/subkey/) installed

- Firstly you need to generate a GRANDPA key (Gossiping Finality GRANDPA)
```bash
subkey generate --scheme Ed25519
```
- Seclondly you will need to generate a BABE (Blind Assignment for Blockchain Extension) key
```bash
subkey generate --scheme Sr25519
```
- Thirdly you will need to generate an ImOnline key
```bash
subkey generate --scheme Sr25519
```
- And fourthly you will need to generate an Authority Discovery key
```bash
subkey generate --scheme Sr25519
```

## Insert your keys

- Grandpa key (using his secret)
```bash
./target/release/allfeat key insert --base-path "$NODE_PATH" --chain testnet --scheme Ed25519 --suri "grandpaSecretKey" --key-type gran
```
- Babe key (using his secret)
```bash
./target/release/allfeat key insert --base-path "$NODE_PATH" --chain testnet --scheme Sr25519 --suri "babeSecretKey" --key-type babe
```
- Imon key (using his secret)
```bash
./target/release/allfeat key insert --base-path "$NODE_PATH" --chain testnet --scheme Sr25519 --suri "imonSecretKey" --key-type imon
```
- Audi key (using his secret)
```bash
./target/release/allfeat key insert --base-path "$NODE_PATH" --chain testnet --scheme Sr25519 --suri "audiSecretKey" --key-type audi
```

These commands generate key pairs (public and private) that you can use to configure your validators or authorities in your Substrate blockchain. Note that using these keys in a production environment should be done with care, including securing the private keys and never sharing them.
