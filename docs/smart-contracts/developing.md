# Smart Contract Development Guide

## Allfeat Blockchain

Develop your smart contracts (DAPPS) on the Allfeat blockchain. The [Allfeat Contracts repository](https://github.com/Allfeat/allfeat-contracts) serves as an excellent starting point for contract development and deployment. It includes a comprehensive set of examples, such as AFT22, AFT34, and AFT37. Refer to the following documentations for a quick start:

- [Allfeat Documentation](https://docs.allfeat.org/)
- [Substrate Documentation](https://docs.substrate.io/)

## Ethereum Compatibility

If you prefer to develop smart contracts on Ethereum (EVM compatible), consult the [OpenZeppelin documentation](https://docs.openzeppelin.com/) – the reference for Ethereum smart contract development, here is a tutorial using Hardhat just below.

## Hardhat Setup for Allfeat

To launch your smart contract on the Allfeat blockchain using Hardhat, follow these steps:

- Initialize `hardhat.config.js`:

```java
require("@nomicfoundation/hardhat-toolbox");
require("dotenv").config();
const { PRIVATE\_KEY\_1, PRIVATE\_KEY\_2, PRIVATE\_KEY\_3 } = process.env;

module.exports = {
solidity: "0.8.19",
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
