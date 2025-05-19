# 🧠 Consensus Overview

In any decentralized system, there is no single authority deciding what is true. Instead, participants must **agree** on a shared version of reality.

This is what we call **consensus** — a method for making decisions and validating information in a distributed environment.

---

## ❓ Why is Consensus Needed?

In traditional systems, a central authority validates and stores data. But in a decentralized network like Allfeat:

- There is **no central database**
- **Multiple participants** can propose and submit data
- Everyone needs to agree on **what data is valid**, **when it was submitted**, and **who submitted it**

Without a consensus mechanism, the system would be vulnerable to:

- Retroactive tampering
- Spam and invalid submissions
- False claims on metadata contributions

Consensus ensures that all data is:

- Authentic
- Immutable
- Agreed upon by a transparent process

---

## 🧱 Two Layers of Consensus in Allfeat

Allfeat separates consensus into **two complementary layers**, each with a distinct responsibility.

---

### 🔒 1. Technical Consensus – Proof of Authority (PoA)

This layer handles the **infrastructure** of the network:

- Writes and orders new blocks
- Executes transactions
- Maintains system-level timestamps

PoA relies on a small, trusted set of **pre-approved validators** who:

- Run reliable nodes
- Are publicly known and accountable
- Are compensated through **transaction fees and protocol reserves**, not inflation

It ensures **network efficiency, cost control, and technical stability** — perfect for an industry-driven platform.

---

### 🧩 2. Functional Consensus – Proof of Metadata (PoM)

This layer governs the **metadata** itself — what is accepted into Allfeat’s public database.

- Anyone can submit a MIDDS by locking AFT tokens
- Trusted participants (Trusters) review and vote on the data
- If approved or unchallenged, the MIDDS becomes **certified and immutable**

PoM is a form of **social and peer consensus**, reflecting **professional validation** within the music industry.

---

## 🧠 Why Two Layers?

| Layer  | Role                      | Participants        | Purpose                          |
| ------ | ------------------------- | ------------------- | -------------------------------- |
| 🔒 PoA | Infrastructure & security | Validators          | Fast and stable block production |
| 🧩 PoM | Metadata validation       | Providers, Trusters | Community-approved data quality  |

PoM relies on the secure and ordered block production ensured by PoA. Together, they form the full consensus mechanism of Allfeat.

This separation lets Allfeat scale efficiently while preserving **data trustworthiness** and **operational reliability**.

---

## 🧾 Summary

- Consensus is how Allfeat agrees on a single version of truth
- **PoA** secures the network and writes the blocks
- **PoM** ensures metadata is valid and reviewed by real professionals
- The two systems work together to maintain a **credible and open public metadata layer**

---

## 📚 Learn more

- [ Proof of Authority (PoA)](./poa.md)
- [ Proof of Metadata (PoM)](./pom.md)
