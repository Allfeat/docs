# Frequently Asked Questions (FAQ)

This FAQ section addresses common questions about using and interacting with the Allfeat network. From setting up your development environment to understanding the new Layer 2 architecture, find quick answers here.

## General Questions

### Q: What is Allfeat?
A: Allfeat is a blockchain platform specifically designed for the music industry. It provides a decentralized infrastructure for hosting, certifying, and monetizing music metadata, along with supporting decentralized applications (DApps) related to music. The platform includes a Decentralized Autonomous Organization (DAO) for inclusive governance, allowing stakeholders from the music industry to participate directly in decision-making.

### Q: How does Allfeat differ from other blockchain platforms?
A: Allfeat is focused on providing a dedicated metadata registry for the music industry. It leverages a unique **Proof-of-Metadata (PoM)** consensus mechanism to certify and store music metadata, ensuring durability and transparency. Unlike other general-purpose blockchains, Allfeat's Layer 1 uses **Substrate** for scalability and security, while a planned **Layer 2 rollup on Ethereum** will facilitate interaction with DApps through Solidity smart contracts.

### Q: What is the Layer 2 rollup and how will it be used?
A: The **Layer 2 rollup** on Ethereum will serve as the bridge for DApps to access metadata from Allfeat's Layer 1 blockchain. This architecture enables scalability while keeping the certification and core metadata functionality in a secure Layer 1. The Layer 2 rollup will ensure a seamless experience for developers wanting to interact with certified metadata using familiar Ethereum tools.

### Q: What happens to the Harmonie testnet?
A: The **Harmonie testnet** is being deprecated as we transition to a new Layer 2-focused testnet. All data and airdrop/incentive operations conducted on the Harmonie testnet will be migrated and preserved, ensuring continuity. Airdrops will be distributed as promised, and this transition supports Allfeat's technological evolution.

## Technical Questions

### Q: How do I set up my development environment for Allfeat?
A: Please refer to the [Prerequisites](prerequisites.md) and [Installing Allfeat from Source](installation/from-source.md) documents for detailed instructions on setting up your environment.

### Q: What programming languages can I use to develop smart contracts on Allfeat?
A: Smart contracts on the **Layer 2 rollup** will be developed using **Solidity**. While Layer 1 focuses on metadata management, Solidity ensures interoperability for developers already familiar with the Ethereum ecosystem.

### Q: Can I run Allfeat without Docker?
A: Yes, you can run Allfeat directly on your operating system without containerization. Please see [Running a Local Node without Docker](running-a-node/without-docker.md) for instructions.

### Q: How will the Layer 2 integration impact DApp development?
A: The new Layer 2 architecture will allow DApps to seamlessly interact with the Allfeat Layer 1 to read certified metadata. This means you can continue using Solidity and benefit from scalability improvements without needing to adjust your development process significantly.

## Validator Questions

### Q: How do I become a validator on Allfeat?
A: Becoming a validator involves setting up a node and being selected into the validator set through the **Proof-of-Authority (PoA)** mechanism. Validators are trusted nodes that ensure the security and stability of the network. More details will come in the later.

### Q: What are the risks of being a validator?
A: Validators have the responsibility of securing the network and can be penalized for improper actions such as double-signing or significant downtime. It's crucial to ensure your node is secure and operates consistently to avoid penalties.

## Proof-of-Metadata (PoM) Certification

### Q: How do I participate in the metadata certification process?
A: You can participate in the certification process as a **Metadata Certifier** or **Nominator**. Certifiers are responsible for verifying metadata and are elected by community members through staking. Nominators can stake their AFT tokens to support trusted certifiers, earning rewards for successful certifications. For more information, see the [Proof-of-Metadata Overview](intro/consensus.md).

### Q: What are MIDDS, and how are they used?
A: **Music Industry Decentralized Data Structures (MIDDS)** are metadata entities used on the Allfeat blockchain to represent different components of the music industry (e.g., artists, songs, releases). MIDDS ensure the fluidity and durability of data and are linked through their IDs to provide a comprehensive metadata registry.

## Troubleshooting

### Q: My node won't start. What should I do?
A: Check your node's logs for errors. Common issues include incorrect configurations or missing dependencies. Refer to [Running a Local Node](running-a-node/docker.md) for setup details. Ensure that your configurations are updated to reflect the transition from the Harmonie testnet if applicable.

## More Information

If your question is not covered in this FAQ, join the Allfeat Discord channel for support, or consult the additional documentation available. We're here to help you through the transition and beyond.
