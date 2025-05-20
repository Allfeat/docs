# 🔁 Transactions in Allfeat

## Introduction

At its core, **a blockchain transaction is a signed instruction** — a request made by someone to change the state of the network.

In Allfeat, almost everything a user does involves a transaction:

- Submitting a new MIDDS
- Certifying a MIDDS as a Truster
- Voting through the DAO.

Each of these actions results in a **transaction that is recorded on-chain**, permanently and transparently.

---

## 🧠 What Happens When You Submit a Transaction?

1. The user (or an app acting on behalf of the user) **creates a transaction**.
2. The transaction is **signed** using the user’s private key.
3. It is sent to the **Allfeat node**, which validates:

    - Signature and permissions
    - Required balance or collateral
    - The logical correctness of the action

4. If valid, it is added to the **next block proposal**.
5. Once included and finalized, it **modifies the on-chain state** — for example, storing a new MIDDS or marking one as certified.

> Transactions in Allfeat are **state mutations** backed by cryptographic identity and economic commitment.

---

## ⚙️ Under the Hood: Extrinsics (Polkadot SDK)

Allfeat is built on the **Polkadot SDK**, which defines all external interactions as **extrinsics**.

There are 3 types of extrinsics:

| Type       | Description                                                        |
| ---------- | ------------------------------------------------------------------ |
| `Signed`   | A regular user transaction — e.g., creating a MIDDS, certifying it |
| `Unsigned` | System-level extrinsics or automated logic (rarely exposed)        |
| `Inherent` | Extrinsics added by the node itself — e.g., timestamp setting      |

Only **signed extrinsics** are relevant to most users and apps.

Each extrinsic is structured as:

```plaintext
[ Call | Signature | Nonce | Tip ]
```

Where:

- `Call` is the function being executed (e.g., `register` of the MIDDS module)
- `Signature` proves the sender's identity
- `Nonce` prevents replay attacks
- `Tip` (optional) increases priority in block inclusion

---

## 📆 Examples of Common Extrinsics in Allfeat

| Pallet    | Extrinsic              | Purpose                            |
| --------- | ---------------------- | ---------------------------------- |
| `midds`   | `register`             | Create a new Musical Work MIDDS    |
| `balance` | `transfer_allow_death` | Transfer some tokens to an account |

Each of these is a callable function within a **runtime module (pallet)** and can be invoked:

- Via the Allfeat SDK
- From dApps using Polkadot-compatible wallets (e.g., Polkadot.js, Talisman)
- Through direct RPC calls to the node

---

## 🧹 Lifecycle of an Extrinsic in Allfeat

```plaintext
1. App/User submits extrinsic
     ↓
2. Node validates and adds it to mempool
     ↓
3. A validator (PoA) includes it in a block
     ↓
4. Block is finalized via GRANDPA
     ↓
5. State is updated: MIDDS created, certified, etc.
```

Once finalized, the **effect of the extrinsic is permanent and queryable**.

---

## 🔐 Economic Context: Collateral and Fees

- Allfeat extrinsics **consume weight** (compute cost), converted into **transaction fees**.
- Some extrinsics require **collateral staking**, especially when publishing MIDDS. This is separate from the fee.
- Complex actions (e.g., editing a large MIDDS or submitting multiple links) may cost more.

This system ensures that:

- The network remains performant and spam-resistant
- Contributors are economically aligned with the quality of their data

---

## 🛠️ Developer Tips

- You can query all supported extrinsics using the metadata exposed by any Allfeat node (`/state_getMetadata`)
- The Allfeat SDK wraps most relevant extrinsics with TypeScript helpers for ease of use
- Extrinsics are encoded using **SCALE**, the compact binary format used by the Polkadot SDK

---

## 📘 See Also

- [💡 What is a Blockchain →](./what_is_a_blockchain.md)
- [⚙️ Runtime Architecture →](./runtime_architecture.md)
- [📦 MIDDS Storage Model →](./midds_storage.md)
- [🧹 Proof of Metadata →](./pom.md)
