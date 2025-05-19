# 🧱 What Are MIDDS?

In Allfeat, everything revolves around **metadata** — but not just any metadata.

To make it usable, trustworthy, and interoperable, we’ve created a set of structured objects called **MIDDS**:  
**Music Industry Decentralized Data Structures**

Think of MIDDS as the building blocks of the Allfeat metadata layer.  
They define _what kind of data_ can be stored, _how it’s structured_, and _how it connects_ to the rest of the network.

---

## 🎯 Why Create MIDDS?

Music metadata is everywhere — in streaming platforms, PROs, labels, spreadsheets, backends — but it’s often:

- Incomplete
- Incompatible
- Opaque
- Privately stored
- Lost in closed systems

MIDDS solve this by offering:

✅ **Clear structures**: Each MIDDS follows a strict format, easy to index, query, and validate  
✅ **Public consistency**: Once validated, a MIDDS is the same for everyone, everywhere  
✅ **Durability**: It lives forever in a tamper-proof network  
✅ **Transparency**: Anyone can read, reference, and build upon it

---

## 🎵 The 4 MIDDS Types (for now)

These are the core units that represent different layers of the music ecosystem:

### 1. `Party Identifier`

Represents any person or entity in the music industry with a recognized public identifier, such as **IPI** (Interested Party Information) or **ISNI** (International Standard Name Identifier).  
This can include performers, authors, publishers, labels, or organizations.  
The type (person vs company) is specified in the MIDDS itself.

### 2. `Song`

The underlying musical work — such as a composition or lyrics.  
Structured using fields like ISWC and title, it's the blueprint behind all recordings.

### 3. `Track`

A recorded performance of a song — often linked to an ISRC code.  
Includes references to its performers (Party Identifiers), the related Song, and release information.

### 4. `Release`

A packaged musical product, like a single, album, or compilation.  
Groups multiple Tracks under a title and release date.

Each MIDDS only includes **public-level metadata**: names, codes, dates, titles, and references.  
There is **no ownership or private contractual data** stored on-chain.

---

## 🆔 Dual Identity: Network vs. Real World

Every MIDDS has two key identifiers:

| Identifier Type              | Description                                                                    |
| ---------------------------- | ------------------------------------------------------------------------------ |
| 🧬 **Allfeat ID**            | Unique hash-like ID assigned when the MIDDS is created on-chain                |
| 🌍 **Real World ID (RW-ID)** | Pre-existing industry-standard ID embedded in the data (e.g. ISNI, ISWC, ISRC) |

This separation is fundamental:

- The **Allfeat ID** ensures decentralized traceability inside the network
- The **RW-ID** allows verification and cross-referencing with Web2 systems (e.g., rights societies, catalogs, DSPs)

By anchoring real-world identifiers in MIDDS, Allfeat becomes a bridge between the existing metadata ecosystem and a new public, decentralized standard.

---

## ⚙️ Optimized for a Network Context

Traditional metadata lives in files, documents, or private APIs.  
But in a decentralized, shared network, we need data that is:

- 🪶 **Lightweight**: Designed to minimize blockchain storage costs
- 🔗 **Composable**: MIDDS can reference each other (e.g., a `Track` links to its `Song` and `Party Identifiers`)
- 🔍 **Verifiable**: Every change, creation, or certification is recorded and auditable
- 🧩 **Modular**: Metadata is broken into logical, reusable units

This design allows Allfeat to scale into a **global, interoperable metadata layer** — maintained by the music industry, for the music industry.

---

## 💰 Collateral and Data Weight

Submitting a MIDDS to the Allfeat blockchain requires **collateral staking** in AFT tokens.

But this cost isn’t fixed — it’s **proportional to the data size**:

| 📦 Data Size (Bytes)                                     | 🔐 Required Collateral (AFT) |
| -------------------------------------------------------- | ---------------------------- |
| Small (e.g., minimal metadata)                           | Low collateral               |
| Large (e.g., full aliases, long titles, many references) | Higher collateral            |

This dynamic system ensures:

- 🛡️ **Security**: Protects the chain from spam or oversized data (anti-DoS mechanism)
- ⚖️ **Fairness**: Heavy users contribute more to storage usage
- 🌱 **Sustainability**: Keeps on-chain metadata lightweight and efficient

> 💡 _The more metadata you anchor on-chain, the more you commit to its importance — via economic collateral._

This approach aligns incentives: serious contributors are rewarded, while excessive or frivolous data becomes economically unviable.

---

## 📌 Summary

- MIDDS are structured objects to represent public music metadata on Allfeat
- They’re built for clarity, consistency, and verification
- Current types include: Party Identifier, Song, Track, Release
- Every MIDDS includes both a **network-level ID** and a **real-world ID**
- Their structure is optimized for a decentralized, scalable, and transparent system

They are the **language** of the Allfeat metadata protocol — the raw material for trust, coordination, and innovation across music data.

---

## 🔗 Related Pages

- [📚 Metadata Philosophy](../metadata.md)
