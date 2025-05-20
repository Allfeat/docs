# 📡 Nodes

## Introduction

In a blockchain network like Allfeat, **nodes are the machines that run the protocol**. They are responsible for communicating with peers, producing blocks, validating transactions, and syncing data across the network.

Allfeat is built as a **Polkadot SDK–based solo chain**, which means its nodes follow a modular structure composed of two layers:

- The **Node Service Layer** (the outer host, often built in Rust)
- The **Runtime Layer** (compiled to WebAssembly and embedded inside each block)

This page explains how nodes work in Allfeat, what roles they play, and how they can evolve.

---

## 🧱 What Makes Up a Node?

A Polkadot SDK node (like Allfeat’s) consists of several key components:

| Component            | Description                                                           |
| -------------------- | --------------------------------------------------------------------- |
| **Networking**       | Handles peer discovery, block/transaction gossip, and sync            |
| **Executor**         | Runs the runtime logic (in Wasm) to apply extrinsics and update state |
| **Client**           | Coordinates block importing, chain database, and finalization         |
| **Consensus Engine** | Manages block production and finality (e.g., BABE and GRANDPA)        |
| **RPC Interfaces**   | Allows external apps to query and send transactions                   |

The runtime is **not compiled directly into the node** — instead, it’s stored on-chain and interpreted as needed. This allows nodes to be light, flexible, and upgradeable.

---

## ⚙️ Block Production: BABE

Allfeat uses **BABE** (Blind Assignment for Blockchain Extension) to produce blocks.

- BABE is a slot-based lottery where validators take turns producing blocks
- Slot leaders are chosen pseudorandomly using a VRF (Verifiable Random Function)
- This ensures **fair and predictable block authorship** across the validator set

Nodes running BABE continuously:

- Listen for new slot assignments
- Propose blocks with fresh extrinsics
- Broadcast their blocks to peers

---

## ✅ Finality: GRANDPA

Once blocks are proposed, **GRANDPA** (GHOST-based Recursive ANcestor Deriving Prefix Agreement) ensures they become final.

- Validators vote on chains of blocks
- Once a supermajority agrees, all ancestors are finalized

This provides **fast, provable finality** and allows nodes to safely prune forks or conflicting histories.

> BABE = block authoring ⏱️
>
> GRANDPA = finality 🎯

Both are embedded in the consensus engine of Allfeat nodes and work in tandem to secure the chain.

---

## 🌐 Why Different Nodes Can Exist

While Allfeat’s reference node is written in Rust (via the Polkadot SDK), in theory:

- **Any implementation** that respects the same consensus rules and runtime execution logic could be valid
- This includes nodes written in other languages (e.g., Go, C++, JavaScript)
- These can be optimized for lightweight clients, mobile use, or archival purposes

This flexibility encourages **multi-client diversity**, improving resilience and decentralization.

> Think of the node as a host, and the runtime as the embedded rules it enforces. As long as the host respects the rules, it’s compatible.

---

## 🧠 Roles of Nodes in the Network

In Allfeat, nodes can play different roles:

| Role           | Description                                              |
| -------------- | -------------------------------------------------------- |
| **Validator**  | Produces and finalizes blocks (runs BABE + GRANDPA)      |
| **Full Node**  | Verifies blocks, stores full chain history, gossips data |
| **Light Node** | Syncs headers only, fetches data on demand (in dev)      |
| **Indexer**    | Custom node variant used for querying and analytics      |

Validators are permissioned in Allfeat’s PoA system, but full nodes can be run by anyone to access public metadata.

---

## 🛠️ Developing Node Variants

Developers can:

- Fork the reference Allfeat node and extend it with custom RPCs
- Build indexers or gateways using tools like **Subxt**, **SubQuery**, or **GraphQL bridges**
- Embed nodes in larger applications (e.g., music platforms, metadata pipelines)

---

## 📘 See Also

- [⚙️ Runtime Architecture →](./runtime.md)
- [📦 Blocks in Allfeat →](./block.md)
- [🔁 Transactions →](./transaction.md)
- [🧩 Proof of Metadata →](../consensus/pom.md)
