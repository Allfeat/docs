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

## Hardhat Setup for Allfeat

To launch your smart contract on the Allfeat blockchain using Hardhat, follow these steps:

- Initialize `hardhat.config.js`:

```java
require("@nomicfoundation/hardhat-toolbox");
require("dotenv").config();
const { PRIVATE\_KEY\_1, PRIVATE\_KEY\_2, PRIVATE\_KEY\_3 } = process.env;

module.exports = {
solidity: "0.8.20",
    networks: {
        local: {
            url: "http://127.0.0.1:9944", // URL to your local blockchain
            accounts: \[PRIVATE\_KEY\_1, PRIVATE\_KEY\_2, PRIVATE\_KEY\_3\].filter((pk) => pk !== undefined) // Filter out undefined keys
        },
        testnet: {
            url: "https://harmonie-endpoint-02.allfeat.io", // URL to harmony testnet
            accounts: \[PRIVATE\_KEY\_1, PRIVATE\_KEY\_2, PRIVATE\_KEY\_3\].filter((pk) => pk !== undefined) // Filter out undefined keys
        }
    }
};
```

- Launch it on your local blockchain:

    ```
    npx hardhat run scripts/deploy.js --network local  # Run on the local node
    ```

- Launch it on the testnet:

    ```
    npx hardhat run scripts/deploy.js --network testnet  # Run on the testnet
    ```

Now, you're ready to deploy your smart contracts on the Allfeat blockchain using Hardhat.

You may use [Hardhat Documentation](https://hardhat.org/tutorial/testing-contracts) to test those contracts
