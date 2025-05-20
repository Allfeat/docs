# 🛠️ Allfeat Protocol Overview

## Introduction

**Allfeat** is a decentralized network built using the **Polkadot SDK** — a modular blockchain framework designed for high-performance, application-specific blockchains.

Allfeat uses this framework to implement a public protocol focused entirely on **music metadata**, governed through a unique combination of **technical and social consensus**.

While previous sections explain _what_ Allfeat is and _why_ it exists, this section explains **how it actually works** — in precise, technical terms.

---

## ⚙️ A Blockchain-Based Metadata Protocol

Allfeat is not just a registry — it is a **fully decentralized protocol** that:

- Anchors public metadata on-chain in a permanent and verifiable way
- Validates the quality and legitimacy of metadata through collective governance
- Defines a custom execution environment tailored to music industry needs

The network is powered by a blockchain built with the **Polkadot SDK**, meaning it:

- Has its own runtime logic (compiled to WebAssembly)
- Defines its own state machine and transaction formats
- Uses a dual-layer consensus (PoA + PoM) to manage infrastructure and data governance

---

## 🔍 What You'll Find Here

This section dives into the **technical architecture** of the Allfeat protocol, including:

- **Runtime Architecture** – How chain state, logic, and upgrades are handled
- **Consensus Design** – Details on BABE, GRANDPA (PoA), and Proof-of-Metadata (PoM)
- **MIDDS Storage Model** – How metadata is stored, linked, and validated
- **Extrinsics & Transactions** – How data flows through the system and affects state
- **On-chain Economics** – Collateral, transaction fees, reward pools, and DoS protections
- **Identifier Model** – How on-chain IDs and Real World IDs are mapped and verified
- **Modular Pallets** – Overview of the protocol’s internal modules (storage, certification, access control)
- **Security & Governance** – How the protocol evolves while remaining transparent and tamper-resistant

---

## 🧠 Who This Is For

This section is designed for:

- **Web3 developers** building integrations, dApps, SDKs, or analytics tools
- **Music tech builders** who need to understand metadata verification and usage at the protocol level
- **Blockchain engineers** interested in Polkadot SDK–based networks
- **Researchers** analyzing decentralized data models in creative industries

Some familiarity with blockchain principles (transactions, consensus, runtimes, extrinsics) is assumed.

---

## 🚧 Specification in Progress

> This section reflects the current design of the protocol.  
> Certain areas — especially around **PoM certification logic and reward mechanics** — are still being refined as we test and iterate.

We are committed to keeping this section up to date with each version of the protocol.

---

## 📚 Suggested Starting Points

- [Runtime Architecture →](./runtime_architecture.md)
- [MIDDS Storage Model →](./midds_storage.md)
- [Extrinsics & Transactions →](./extrinsics.md)

---

> Allfeat is a **public metadata protocol** built on a decentralized, auditable foundation —  
> designed to give the music industry a shared source of truth, powered by open infrastructure.

This section shows you **how the engine works**.
