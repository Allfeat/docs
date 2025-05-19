# 🔒 Proof of Authority (PoA)

The Proof of Authority (PoA) system in Allfeat ensures that the network technically works **securely**, **smoothly**, and **without interruption**.

Unlike fully open networks where anyone can try to validate blocks, PoA relies on a **pre-selected group of validators** — trusted participants who run the network's infrastructure.

---

## 🧠 Why Do We Use PoA?

The music industry needs:

- ✅ Fast confirmations
- ✅ Reliable infrastructure
- ✅ Predictable and affordable costs

PoA offers all of that by **avoiding energy-heavy mining** or complex economic games. It focuses on **trust and performance**, making it ideal for a professional, use-case-oriented chain like Allfeat.

Validators in PoA are:

- Known and identifiable entities
- Chosen for their technical reliability and neutrality
- Accountable for maintaining uptime and fairness

They don’t receive newly minted tokens (no inflation), but they do earn:

- 🔁 A share of transaction fees
- 💰 Protocol rewards from a fixed treasury

---

## 🏗️ How It Works Behind the Scenes

Even if validators are pre-selected, we still need a system that:

- Randomly chooses **who creates the next block**
- Makes sure **all validators agree on the correct version of the chain**

Allfeat uses two mechanisms to do this:

---

### 🎯 BABE – Block Assignment

BABE (Blind Assignment for Blockchain Extension) is the engine that picks **which validator will produce the next block**.

Here’s how it works in simple terms:

- At regular time intervals, validators are asked to propose a block
- BABE randomly assigns the right to produce the block to one of them
- If a validator is unavailable, another one can step in after a short delay

This creates a steady rhythm for the network and spreads the load fairly among validators.

---

### 🧓 GRANDPA – Finalization

Once blocks are proposed, the network needs to **agree on which blocks are final and can never be changed**.

This is where GRANDPA (GHOST-based Recursive ANcestor Deriving Prefix Agreement) comes in.

- Validators vote on which blocks they consider finalized
- If a **majority** agree, those blocks become **permanent**
- This ensures everyone sees the same version of history, even if some nodes are offline temporarily

GRANDPA makes it **very hard to rewrite the chain** or trick the system with fake versions of events.

---

## 👥 Who Can Become a Validator?

At launch, Allfeat operates with a **curated set of validators** to guarantee stability. Over time, the validator set may expand, with new members added based on:

- Their uptime and performance
- Their neutrality and transparency
- The trust they build with the Allfeat community

Note: this system is different from networks that allow anyone to join. It’s a **pragmatic choice** that ensures professional-grade service from day one.

---

## 📌 Summary

- **PoA** is the foundation of Allfeat’s infrastructure layer
- It uses a **trusted pool of validators** to process and secure transactions
- Two key tools make it possible:
    - **BABE**: chooses who produces each block
    - **GRANDPA**: finalizes and agrees on block history
- It provides a **fast, cost-efficient and reliable network** tailored to the needs of the music ecosystem

---

## 🔗 Related Pages

- [🧩 Proof of Metadata (PoM)](./pom.md)
- [🧠 Consensus Overview](./overview.md)
