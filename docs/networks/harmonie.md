# Overview of the Allfeat Testnet Strategy

## Introduction to Testnets

In the realm of blockchain technology, a testnet plays a crucial role in the development and testing of decentralized applications (DApps), smart contracts, and other blockchain functionalities. A testnet is essentially a simulation environment, mirroring the main network (mainnet) in functionality but without the risk of real asset loss. It provides a sandbox for developers to experiment, debug, and validate their projects under real-world conditions without incurring the costs and risks associated with the mainnet.

## Evolution of the Harmonie Testnet

The current **Harmonie testnet** serves as Allfeat's official testnet and is designed for developers in the music blockchain space. It simulates the Allfeat mainnet environment, offering a testing ground for DApps, smart contracts, and other blockchain interactions.

However, **with the removal of Frontier**, which currently enables EVM compatibility directly on the Layer 1, the Harmonie testnet will gradually be deprecated. The focus will shift toward a new **Layer 2 rollup testnet on Ethereum**, aligned with Allfeat's strategy of decoupling the EVM from the Layer 1 and leveraging a dedicated Layer 2 for smart contract interactions.

This shift will allow the Allfeat Layer 1 to focus exclusively on the **decentralized registry of metadata** through the Proof-of-Metadata (PoM) mechanism while enabling DApps and smart contracts to interact with this data through the Layer 2 rollup on Ethereum.

### Airdrops and Incentives: Data Migration Assurance

It’s important to note that **all airdrop and incentive operations conducted on the Harmonie testnet will be preserved**. Data gathered through these operations will be migrated and securely saved as we transition to the new Layer 2 testnet. Airdrops will be distributed as promised, ensuring that all efforts and contributions made on the Harmonie testnet are not lost.

This continuity ensures that previous communications remain valid and consistent while supporting a sustainable technological advancement for the Allfeat ecosystem. Developers and community members can be confident that their participation in the Harmonie testnet will translate into rewards and recognition on the new platform.

### Current Network Specifications (Harmonie)

For developers who continue to use the Harmonie testnet during this transition, the following table outlines the key specifications:

| Specification      | Description                                                                                               |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| **Network Name**   | Harmonie                                                                                                  |
| **Native Token**   | HMY                                                                                                       |
| **Token Decimals** | 18                                                                                                        |
| **Endpoint URL**   | harmonie-endpoint-02.allfeat.io                                                                           |
| **Faucet URL**     | https://faucet.allfeat.com/                                                                               |
| **Chain ID**       | 441                                                                                                       |

### Explorers

During the transition period, the following explorers are available for monitoring network activity:

- **[EVM Explorer](https://evm.allfeat.com)**: Useful for DApp developers to interact with deployed contracts during the interim period while EVM functionality remains on the Layer 1.
- **[Substrate Explorer](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fharmonie-endpoint-02.allfeat.io#/explorer)**: Allows deeper inspection of Substrate-based functionality, such as querying the storage of pallets and interacting with the core blockchain data.

### Transitioning to the Layer 2 Rollup

As we move toward a **Layer 2 rollup testnet on Ethereum**, developers should prepare to adapt their development processes:

1. **Configure Your Development Environment**: Adjust your tools and wallets to connect to the upcoming Layer 2 testnet, and familiarize yourself with the new endpoints.
2. **Obtain Testnet Tokens**: Testnet tokens will still be available through a faucet for the Layer 2 environment to support testing of smart contracts and metadata requests.
3. **Deploy and Test on the Layer 2**: Utilize the Layer 2 environment for deploying smart contracts that interact with Allfeat's metadata via the bridge to the Layer 1.

### Best Practices During the Transition

- **Prepare for Migration**: Start migrating your smart contracts and DApp logic to be compatible with the Layer 2 environment.
- **Engage with the Allfeat Community**: Stay updated on the transition process through community channels and developer forums for support and insights.
- **Ensure Flexibility**: Design your applications with future Layer 2 interactions in mind to ensure a smoother transition to the new architecture.

By embracing the new Layer 2 testnet approach, developers can continue to innovate while benefiting from the scalability of Ethereum and the dedicated metadata registry of Allfeat's Layer 1. This transition marks a pivotal step in enhancing the usability and interoperability of the Allfeat ecosystem.
