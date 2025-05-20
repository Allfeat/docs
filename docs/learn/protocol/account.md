# 👤 Accounts

## Introduction

In traditional Web2 platforms, a user account is often tied to an email, phone number, or social login. It’s stored in a central database and controlled by a service provider.

In Allfeat — like in any blockchain-based protocol — **accounts are not created or assigned by a central authority**. Instead, they are derived from **cryptographic keys** that the user controls directly.

This brings more freedom, more control — but also new responsibilities.

---

## 🔐 Public and Private Keys

Every account in Allfeat is based on a **keypair**:

| Component       | Purpose                                                        |
| --------------- | -------------------------------------------------------------- |
| **Private Key** | Your secret. Used to sign transactions. **Must be kept safe**. |
| **Public Key**  | Your identifier. It’s used to derive your on-chain address.    |

Your **address** (what others see and interact with) is derived from your public key. When you sign a transaction, your private key proves it’s really you — without revealing itself.

> You don’t need a username or email. You control your account simply by owning its keys.

---

## 🔷 How Accounts Work in the Polkadot SDK

Allfeat is built with the **Polkadot SDK**, and therefore uses its native account format:

- Accounts are represented internally as `AccountId32`
- This means all addresses are 32-byte hashes
- The default key type used is **SR25519**, based on Schnorr signatures

This differs from Ethereum-based systems, which typically use **ECDSA** (Elliptic Curve Digital Signature Algorithm).

The SR25519 system offers:

- Better performance for certain cryptographic operations
- Built-in support for hierarchical key derivation (useful for role separation)
- Stronger resistance to replay and signature malleability attacks

> While users see a friendly address (like `5GZ...xyz`), under the hood, it’s a 32-byte `AccountId` derived from a public SR25519 key.

---

## 🧑‍🚀 Pseudonymity, Not Anonymity

Allfeat accounts are **pseudonymous**:

- They are not linked to a real-world identity by default.
- But all actions tied to an account are **public and traceable**.

That means:

- Anyone can see what a specific account has done (submissions, votes, certifications...)
- But unless the user chooses to reveal themselves, no one knows who is behind the account

This makes Allfeat:

- 🌐 **Open**: anyone can participate
- 🧾 **Transparent**: all activity is auditable
- 🔐 **Respectful of privacy**: users decide what to share

---

## 🔄 Managing Multiple Accounts

Because accounts are just keypairs, users can generate multiple accounts — for example:

- One for submitting metadata (provider role)
- One for certifying metadata (truster role)
- One for treasury/rewards separation

This is often called **key separation** and can be a best practice for security and role isolation.

Tools like Polkadot.js, Talisman, Ledger, and browser extensions make this easier to manage.

---

## 🧠 Responsibilities of Account Ownership

With great control comes great responsibility:

- **Lose your private key?** You lose access — forever. There is no password reset.
- **Share your private key?** Anyone can act on your behalf.
- **Use unsafe apps?** You may sign transactions you didn’t mean to.

Allfeat never stores or has access to your keys. Use secure wallets and always verify what you sign.

> Your account is only as secure as the device and practices you use to protect it.

---

## 📘 See Also

- [🔁 Transactions →](./transactions.md)
- [🧹 Proof of Metadata →](./pom.md)
- [⚙️ Runtime Architecture →](./runtime_architecture.md)
