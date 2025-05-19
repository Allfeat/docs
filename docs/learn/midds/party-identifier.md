# 🧾 Party Identifier

## Overview

The **Party Identifier MIDDS** is the data structure used in Allfeat to represent any **party** in the music industry — whether an individual (e.g., an artist, composer) or a legal entity (e.g., a label, publisher).

This MIDDS acts as a **unique reference point** to identify, verify, and link people and organizations across music metadata, thanks to the integration of **Real World Identifiers** like **ISNI** and **IPI**.

It is the foundation for representing relationships in songs, recordings, and releases on-chain.

---

## 🧠 Why It Matters

In the music industry, **who did what** is a fundamental question — and often a complicated one to answer.  
Many people or companies share similar names, use pseudonyms, change their branding, or operate under multiple aliases.

The Party Identifier MIDDS solves this by:

- **Standardizing identity** around IPI and ISNI identifiers.
- Allowing fine-grained representation of people and entities.
- Serving as a **reliable anchor** for relationships in other MIDDS (e.g., linking a performer to a Track).

---

## 🏗️ Structure Summary

| Field        | Type        | Description                                                                                                    |
| ------------ | ----------- | -------------------------------------------------------------------------------------------------------------- |
| `isni`       | `Isni`      | A standard 16-digit **International Standard Name Identifier**. Helps match the party across global databases. |
| `ipi`        | `Ipi`       | A unique 11-digit **Interested Parties Information** code, widely used in rights management.                   |
| `party_type` | `PartyType` | Enum that indicates whether the party is a `Person` or an `Entity` and includes their respective data.         |

---

## 🧬 `PartyType` Enum

### 👤 `Person`

| Field         | Type             | Description                                                                     |
| ------------- | ---------------- | ------------------------------------------------------------------------------- |
| `full_name`   | `PersonFullName` | The legal or official name.                                                     |
| `aliases`     | `PersonAliases`  | Optional list of stage names, nicknames, etc.                                   |
| `person_type` | `PersonType`     | Indicates whether the person is a solo artist, part of a group, or other roles. |
| `genre`       | `PersonGender`   | Declared gender identity, used for descriptive classification.                  |

### 🏢 `Entity`

| Field         | Type         | Description                                                               |
| ------------- | ------------ | ------------------------------------------------------------------------- |
| `name`        | `EntityName` | The name of the organization or company.                                  |
| `entity_type` | `EntityType` | The role of the organization, such as label, publisher, distributor, etc. |

---

## 🆔 Identifiers and Linking

All Party Identifier MIDDS carry two kinds of identifiers:

| Type                              | Description                                                                                                         |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **On-Chain ID**                   | Automatically assigned by the Allfeat blockchain at creation. Used internally by the network.                       |
| **Real World Identifier (RW-ID)** | Provided within the MIDDS: `ISNI`, `IPI`. These are **globally recognizable IDs** from traditional music databases. |

This dual-ID model ensures that:

- Web2 platforms can **map existing data** into the blockchain without loss.
- Web3 applications can **verify relationships** using stable, known references.

---

## 🔗 Usage in the Allfeat Graph

The Party Identifier MIDDS is used as a **linkable node** in many other structures:

- `Song` MIDDS references the authors and composers.
- `Track` MIDDS references performers and producers.
- `Release` MIDDS references rights holders and publishers.

By isolating identity as its own verifiable object, Allfeat enables:

- **reusability** across multiple works,
- **accuracy** in attribution,
- and **transparency** in rights and data curation.

---

## 🚀 Who Creates This MIDDS?

- **Providers**: anyone who wants to register a person or organization with a valid RW-ID.
- **Trusters**: validators who review and endorse the information before it becomes certified.

All entries must meet verification standards and are subject to **staking-based validation** under the **Proof-of-Metadata** mechanism.

---

## 🛠️ Example Use Case

> A contributor wants to register _Kendrick Lamar_ as a songwriter.

They would:

1. Create a PartyIdentifier with his IPI and ISNI.
2. Choose `Person` as the party type.
3. Fill in:
    - Full name: "Kendrick Lamar Duckworth"
    - Aliases: "Kendrick Lamar", "K.Dot"
    - Gender: Male
    - Person type: Solo artist
4. Stake tokens to submit the MIDDS.
5. Wait for trusters to certify it.

Once accepted, this MIDDS can be linked in future Song or Track MIDDS, ensuring consistent, traceable identity across all contributions.

---

## 📘 See Also

- [Metadata Philosophy →](./metadata_philosophy.md)
- [MIDDS Overview →](./midds_overview.md)
- [Proof of Metadata (PoM) →](./pom.md)
