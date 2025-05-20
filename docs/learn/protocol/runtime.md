# ⚙️ Runtime Architecture

## Introduction

The **runtime** is the core logic engine of the Allfeat blockchain. It defines what the network can do, how the state evolves, and how rules are enforced.

In Allfeat, the runtime is built using the **Polkadot SDK**, and compiled to **WebAssembly (Wasm)**. The runtime itself is **written in Rust**, using the SDK's modular framework.

This runtime is deterministic, sandboxed, and governs the behavior of the network entirely — from metadata submission to certification, storage, staking, and beyond.

This page explains how the runtime fits into the overall node architecture, and how it powers every transaction and state change on the Allfeat network.

---

## 🧱 Node vs Runtime: What's the Difference?

In a Polkadot SDK–based blockchain like Allfeat, a node consists of two major components:

| Component   | Role                                                                     |
| ----------- | ------------------------------------------------------------------------ |
| **Node**    | The outer shell: networking, block production, gossiping, RPC, etc.      |
| **Runtime** | The inner logic: state transitions, extrinsics, storage, consensus rules |

The **node** is responsible for:

- Listening to the network
- Assembling and proposing blocks
- Handling RPC calls and peer sync

The **runtime** is responsible for:

- Executing transactions (extrinsics)
- Managing state updates
- Enforcing protocol rules (e.g., PoM logic)
- Defining how metadata is stored and validated

> You can think of the node as the machine, and the runtime as the operating system logic running inside.

---

## 🧠 How the Runtime Works

The runtime is written in **Rust** using Polkadot SDK primitives and is compiled to **WebAssembly** (Wasm). This makes it:

- **Deterministic**: all nodes run exactly the same code, producing the same result
- **Upgradeable**: the runtime can be updated on-chain without needing a hard fork
- **Isolated**: it runs in a sandbox, independent of node internals

When a block is created, the runtime is invoked to **execute each extrinsic** in order, update the storage, and emit any relevant events.

---

## 🧩 Structure of the Allfeat Runtime

Allfeat's runtime is made up of custom **pallets** (modules), each responsible for a part of the protocol logic:

| Pallet                                  | Responsibility                                        |
| --------------------------------------- | ----------------------------------------------------- |
| `midds`                                 | Handles creation, editing, and referencing of MIDDS   |
| `certification`                         | Governs the PoM process, review workflow, voting      |
| `staking`                               | Manages token collateral and deposits                 |
| `identity`                              | Internal management of pseudonymous identities        |
| `system`, `timestamp`, `balances`, etc. | Core Polkadot SDK pallets for block and account logic |

These pallets interact through the runtime and use shared storage and events to communicate changes.

---

## 🔄 Runtime Upgrades

One of the key strengths of the Polkadot SDK is the ability to **upgrade the runtime via governance**, without any chain split:

- Runtime logic is compiled to Wasm and stored on-chain
- Validators download and execute the latest version automatically
- Changes to MIDDS logic, staking rules, or consensus parameters can be deployed via governance or root extrinsics

This allows Allfeat to evolve over time while remaining secure and backwards-compatible.

---

## 🛠️ Developer Considerations

If you're building on Allfeat, it's important to understand:

- Extrinsics you call are routed to pallet functions in the runtime
- Storage you query reflects the runtime's state model
- Events emitted by the runtime are the main signals for dApps or indexers
- Runtime weights determine the cost (in fees) of each operation

> The runtime defines the rules. The node executes them and connects the network.

---

## 📘 See Also

- [📦 Blocks in Allfeat →](./block.md)
- [🔁 Transactions →](./transaction.md)
- [📚 MIDDS Storage Model →](./midds_storage.md)
- [🧩 Proof of Metadata →](./consenus/pom.md)
