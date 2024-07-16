# Smart Contract Development Guide

This resource is designed to assist you in harnessing the power of the Allfeat blockchain to develop and deploy your decentralized applications (DApps).
Whether you are a seasoned developer or new to the blockchain space, our guide will provide you with the necessary tools and knowledge to craft innovative solutions within the music industry and beyond.

The Allfeat blockchain is built with compatibility in mind, supporting Ethereum Virtual Machine (EVM)-compatible smart contracts written in Solidity.
This ensures a smooth transition for developers already familiar with EVM chains and a straightforward learning curve for newcomers. To kickstart your journey, we've curated a selection of resources that cover the basics of Solidity and smart contract development on EVM-compatible chains:

- [Solidity Documentation](https://docs.soliditylang.org/en/v0.8.25/introduction-to-smart-contracts.html): The official Solidity documentation is an essential resource for developers of all levels. It offers a thorough overview of the language, including syntax, contract structures, and advanced features.
- [CryptoZombies](https://cryptozombies.io/): CryptoZombies is an interactive code school that teaches you to write smart contracts in Solidity through building your own crypto-collectibles game.
- [Ethereum Development Documentation](https://ethereum.org/en/developers/docs/): This collection of documentation provides a wealth of information on Ethereum-based development, including smart contracts, DApps, and more.
- [Remix IDE](https://remix.ethereum.org/): Remix is a powerful, open-source tool that helps you write Solidity contracts straight from the browser. It is designed for small contracts and quick prototyping.

Armed with these resources and the unique features of the Allfeat blockchain, you are well-equipped to start developing smart contracts that can revolutionize the music industry and create new opportunities for artists, fans, and stakeholders alike. Let's dive in and explore the limitless possibilities of blockchain technology together.

## Deploy your own smart contract using Foundry

In order to deploy your own smart contract, you can use [Foundry](https://book.getfoundry.sh/)

First you will need an `EVM compatible` wallet filled with `HMY` tokens. You can use our [faucet](https://faucet.allfeat.com/) to get some.

Once your contract is ready, you will have to build it first:

  ```bash
  forge build
  ```

Then deploy the contract:

  ```bash
  forge create --rpc-url https://harmonie-endpoint-02.allfeat.io --private-key <YOUR_PRIVATE_KEY> <YOUR_CONTRACT> --legacy
  ```

Don't forget to replace the placeholders:

- `<YOUR_PRIVATE_KEY>`: is the private key of your wallet
- `<YOUR_CONTRACT>`: is the name of your contract

If you want to verify your contract upon deployment, you can add an argument like so:

  ```bash
  forge create --rpc-url https://harmonie-endpoint-02.allfeat.io --private-key <YOUR_PRIVATE_KEY> <YOUR_CONTRACT> --legacy --verify --verifier blockscout --verifier-url https://evm.allfeat.com/api
  ```

You can then check your contract has been deployed on the [EVM explorer](https://evm.allfeat.com/).

If you have any troubles deploying your contract, we suggest you check [Foundry's documentation](https://book.getfoundry.sh/forge/deploying) or reach out to the [Allfeat youtube tutorial](https://www.youtube.com/watch?v=oxr3fZqrnpg). You can also reach us by joining our [Discord server](https://discord.allfeat.com/).

Now, you're ready to deploy your smart contracts on the `Allfeat` blockchain using `Foundry` !
