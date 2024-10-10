# Architecture and Vision (Layer 1 and Layer 2)

Allfeat is built on a two-layer architecture designed to optimize the management of metadata in the music industry, ensuring decentralization, transparency, and efficiency.

## Layer 1: The Core of Allfeat

**Layer 1** of Allfeat is built using **Substrate**, a highly adaptable and performant blockchain framework. It is dedicated to the hosting, certification, and monetization of **Music Industry Decentralized Data Structures (MIDDS)**, which represent metadata entities (such as artists, recordings, works, etc.). The focus of Layer 1 includes:

- **Metadata Registry**: Allfeat provides a decentralized and immutable platform where music industry data is stored and certified through the **Proof-of-Metadata (PoM)**. This unique mechanism enables stakeholders in the music industry to submit metadata, which is then validated by community-elected certifiers.

- **Proof-of-Metadata (PoM) Consensus**: PoM is the core of the Layer 1 architecture, ensuring that every submitted metadata is verified transparently and immutably. Key actors in the PoM, such as metadata providers and certifiers, guarantee the quality and accuracy of the data while being rewarded for their contributions.

- **Proof-of-Authority (PoA) Node Consensus**: To ensure network security and efficiency, Layer 1 utilizes a **Proof-of-Authority (PoA)** consensus for node validation. This approach relies on a trusted selection of validators, enabling fast transaction processing and governance tailored to the music industry's needs. Validators are selected through a **DAO** (Decentralized Autonomous Organization), allowing the community to participate in the network's governance.

Layer 1 is primarily focused on metadata management and certification, while EVM compatibility is handled through a higher layer, ensuring a clear separation of roles and functionalities.

## Layer 2: Extending to the Ethereum Ecosystem

**Layer 2** of Allfeat is an **Ethereum rollup** designed to enable decentralized applications (DApps) in the Ethereum ecosystem to leverage certified metadata from Allfeat. Layer 2 plays a crucial role in making Allfeat's data accessible to developers and users on Ethereum while maintaining the advantages of the Allfeat blockchain.

- **Bridge for Metadata Access**: The Layer 2 includes a **bridge** that allows Solidity smart contracts deployed on Layer 2 to read certified metadata stored on Allfeat’s Layer 1. This bridge ensures smooth communication between the two layers, enabling DApps to request information in a secure and transparent manner.

- **Service Managed by Allfeat Labs**: The Layer 2 is maintained and managed by **Allfeat Labs**. This approach offers optimized services to DApps while ensuring the security of interactions between Layer 1 and Layer 2. **Service fees** may apply for metadata requests to support the bridge's operation and associated infrastructure.

- **Scalability and Interoperability**: By handling EVM interactions on Layer 2, Allfeat ensures greater scalability and reduces the load on Layer 1, improving metadata management and the security of the main network. The Layer 2 also allows DApp developers to benefit from Ethereum’s rich infrastructure while accessing data verified and certified by Allfeat.

## A Vision of Interoperability and Transparency

Allfeat's two-layer architecture offers a comprehensive solution for the music industry, combining the robustness and specialization of Layer 1 for metadata management with the flexibility and interoperability of Layer 2 for DApp development.

With this approach, Allfeat aims to create an ecosystem where music metadata can be certified in a decentralized manner and utilized by applications within the Ethereum ecosystem, while offering governance and security tailored to the unique needs of the music industry.