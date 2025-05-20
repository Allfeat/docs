# ⛓️ What Is a Blockchain (and What It Means for Allfeat)

## Introduction

To understand how Allfeat works — and especially how metadata behaves over time — you need to understand **what a blockchain really is**.

Many misunderstandings come from thinking that data on a blockchain is either:

- **permanently frozen and can never change**, or
- **completely editable like a regular database**.

The truth is: it’s neither.  
Let’s clarify.

---

## 📦 A Blockchain Is a History of Blocks

A **blockchain** is a continuously growing list of **blocks**, each containing:

- A batch of validated transactions
- A reference to the previous block (via a cryptographic hash)
- A timestamp and other metadata

Together, blocks form a **linked, immutable chain** — meaning:

- You can always read the full history
- You cannot modify blocks that are already finalized
- The state of the system is **reconstructed by replaying all blocks in order**

This applies to Allfeat too.

---

## 🧠 What Gets Stored in Allfeat's Blocks?

In Allfeat, every **action on metadata** is a transaction:

- Submitting a new MIDDS
- Certifying a MIDDS
- Marking it as ready for review
- Proposing an edit
- Linking two MIDDS together

Each of these actions is **written into a block**.  
The result is a verifiable timeline of **who did what, when, and how**.

---

## 🔄 Can MIDDS Change Over Time?

Yes — but not by modifying the past.

Here’s how it works:

> ❌ You cannot edit a block.  
> ✅ But you can **submit a new transaction** that modifies the state.

That means:

- If you submitted a MIDDS and later realize you forgot a detail, you can **propose an update**
- If the update is accepted and validated, it becomes part of a **new block**
- The new state replaces the previous one — but the **history is preserved forever**

This is called **append-only logic**:  
You don’t delete or overwrite, you **add** new instructions.

---

## 🛡️ What Does "Immutable" Really Mean?

"Immutable" does not mean “frozen forever.”  
It means that **the history of actions cannot be altered**.

In Allfeat, this brings real benefits:

- 🕵️ **Auditable**: Anyone can track how a MIDDS was created, updated, or certified
- 🧾 **Traceable**: Conflicts or fraud can be detected by comparing past actions
- 🔗 **Dependable**: Apps, organizations, and people can rely on a single public source of truth

> Even when a MIDDS evolves, its **historical path remains visible and provable**.

---

## 🔗 How MIDDS Evolve

Here’s a simple example of how a MIDDS lifecycle might look on-chain:

1. 🎶 **Block #421**: A Musical Work is submitted
2. ✅ **Block #426**: The work is certified by Trusters
3. ✏️ **Block #490**: A correction is submitted (wrong BPM)
4. 📌 **Block #491**: The correction is approved and the state is updated

At any point, someone can query:

- The **current version** of the MIDDS
- The **full change history** (who submitted what and when)

This gives Allfeat **both durability and flexibility** — a powerful combination that traditional metadata systems often lack.

---

## ✅ In Summary

- A blockchain is a **permanent record of events**, not a database you “edit”
- Allfeat stores **metadata changes as events** across time
- A MIDDS can evolve — but always through new transactions, never by modifying the past
- This ensures a balance of **immutability, transparency, and data evolution**

---

## 📘 See Also

- [🛠️ Allfeat Protocol Overview →](./protocol_overview.md)
- [📦 MIDDS Storage Model →](./midds_storage.md)
- [🧩 Proof of Metadata →](./pom.md)
