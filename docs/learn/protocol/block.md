# 📦 Blocks

## Introduction

In any blockchain network, **blocks** are the core units of data that make the chain function. Each block contains a batch of transactions, a reference to the previous block, and metadata necessary for finality and verification.

In Allfeat, which is built using the **Polkadot SDK**, blocks follow the same fundamental structure and behavior defined by the Polkadot ecosystem.

This page explains how blocks are created, what they contain, and how **metadata (MIDDS)** is stored and referenced on-chain.

---

## 🧱 What Is a Block?

A block in Allfeat contains:

- A **header**
- A list of **extrinsics** (transactions and inherent data)
- A **state root**, representing the new state after processing the block
- A **parent hash**, linking to the previous block

Each new block extends the chain and updates the global state of the protocol.

---

## 🔄 Block Lifecycle (Polkadot SDK)

1. A validator is selected via BABE to propose the next block
2. The node bundles **extrinsics** (signed transactions, timestamp, etc.)
3. The runtime executes each extrinsic in order:

    - State transitions are applied
    - Storage values are updated

4. A new **state root** is generated
5. The block is broadcast to peers
6. Finality is reached via **GRANDPA**, locking the block in the chain

This process happens roughly every 6 seconds on Allfeat, depending on configuration.

---

## 🧩 What Happens When a MIDDS Is Submitted?

Let’s say a user submits a new `MusicalWork` MIDDS:

1. The action is encoded into an **extrinsic** (`midds::submit_musical_work`)
2. It is signed and sent to the network
3. The extrinsic is included in the next block
4. When the block is executed:

    - The runtime stores the MIDDS in the `midds` pallet
    - An `Allfeat ID` is assigned
    - A storage event is emitted (e.g., `MIDDSRegistered`)

5. The block is finalized

Now the MIDDS exists in the blockchain’s **state trie** and can be queried or referenced by future blocks.

> Note: The actual data is not stored “in” the block body, but rather in on-chain **storage**, whose new root hash is committed to the block.

---

## 🧬 Data Storage Model

The Polkadot SDK uses a **key-value storage model**. Each pallet (module) has its own namespace. For example:

```plaintext
midds::MusicalWorks => { <AllfeatID> => MusicalWork struct }
```

When a block is executed:

- The storage is updated according to the extrinsics
- The result is a new **Merkleized state root** (hashed for verification)
- This root is included in the block header

This ensures full traceability of what data led to a given state — even if that data itself isn’t written directly inside the block body.

---

## 🔎 How to Query a Block

You can query any finalized block using RPC:

- `chain_getBlock` → returns block header and extrinsics
- `state_getStorage` → retrieves stored MIDDS values
- `state_getStorageAt` → gets storage values at a past block

This allows external apps and indexers to reconstruct the full context of any MIDDS over time.

---

## ✅ Summary

- A block contains transactions, timestamp, parent reference, and state transitions
- Allfeat follows the Polkadot SDK’s block structure (header + extrinsics)
- MIDDS data is written to on-chain storage, not directly into the block body
- The block commits to this storage via a new **state root**
- You can query any past or present block and storage value via RPC

---

## 📘 See Also

- [🔁 Transactions →](./transaction.md)
- [📦 MIDDS Storage Model →](./midds_storage.md)
- [🧩 Proof of Metadata →](../consensus/pom.md)
- [🛠️ Runtime Architecture →](./runtime_architecture.md)
