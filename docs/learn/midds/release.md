# 🧾 Release

## Overview

The **Release MIDDS** represents a **musical product** made available to the public — such as an **album**, **EP**, **single**, or **mixtape**.

It groups multiple Tracks under a unified release, defines the associated artist and producers, and includes both **distribution metadata** and **physical/digital characteristics**.

This is the final layer in the Allfeat metadata graph, where multiple components (works, recordings, contributors) converge into a **published product**.

---

## 🧠 Why It Matters

A single song might appear in multiple contexts — an original album, a remix EP, a reissue, a greatest hits release.

The `Release` MIDDS captures this **context**:

- It documents **how** and **when** a group of tracks was published.
- It links the creative chain (Track → Work → Artist) to the **distribution side**.
- It anchors **real-world release events** into a **public, verifiable graph**.

By structuring release data, Allfeat enables clear identification, cataloging, and attribution across the entire music lifecycle.

---

## 🏗️ Structure Summary

| Field                | Type                       | Description                                                                 |
| -------------------- | -------------------------- | --------------------------------------------------------------------------- |
| `ean_upc`            | `Ean`                      | Global release ID (EAN/UPC barcode), used in physical/digital distribution. |
| `artist`             | `MiddsId`                  | Main Party Identifier MIDDS (primary artist or group).                      |
| `producers`          | `ReleaseProducers`         | List of Party Identifier MIDDS who produced the release.                    |
| `tracks`             | `ReleaseTracks`            | List of Track MIDDS included in the release.                                |
| `distributor_name`   | `ReleaseDistributor`       | Free-text name of the distributor.                                          |
| `manufacturer_name`  | `ReleaseManufacturer`      | Free-text name of the physical manufacturer (if applicable).                |
| `cover_contributors` | `ReleaseCoverContributors` | List of Party Identifiers (photographers, designers, etc.).                 |
| `title`              | `ReleaseTitle`             | Official release title.                                                     |
| `title_aliases`      | `ReleaseTitleAliases`      | Optional list of alternate titles or translations.                          |
| `release_type`       | `ReleaseType`              | Enum describing whether it's a Single, EP, Album, Mixtape, etc.             |
| `format`             | `ReleaseFormat`            | Medium of release (CD, Vinyl, Cassette, Digital...).                        |
| `packaging`          | `ReleasePackaging`         | Physical packaging (Jewel Case, Digipack, etc.).                            |
| `status`             | `ReleaseStatus`            | Status of the release (Official, Promo, Remastered, etc.).                  |
| `date`               | `Date`                     | Date of release (YYYY-MM-DD).                                               |
| `country`            | `Country`                  | Country of release.                                                         |

---

## 🧬 Identifiers and Linking

Like other MIDDS, a `Release` uses:

| Type           | Description                                                                                    |
| -------------- | ---------------------------------------------------------------------------------------------- |
| **Allfeat ID** | Unique on-chain ID assigned at creation.                                                       |
| **RW-ID**      | EAN or UPC — a real-world code used by retailers, distributors, and physical/digital catalogs. |

This duality enables:

- Web2 → Web3 linking via standard distribution codes.
- Long-term traceability of release metadata across ecosystems.

---

## 🔗 Usage in the Allfeat Graph

The Release MIDDS brings everything together:

- It **references Track MIDDS**, each of which references Musical Works and Party Identifiers.
- It can be **queried by artist, title, country, or release type**.
- It acts as the **final layer** in the metadata structure — the public product that users see, buy, and stream.

---

## 🚀 Who Creates This MIDDS?

- **Providers**: typically labels, distributors, or artists submitting a new release.
- **Trusters**: reviewers who verify the accuracy and completeness of the data.

Collateral is calculated based on the **size of the MIDDS** (number of tracks, alias length, contributors, etc.), ensuring fairness and protection against spam.

---

## 🛠️ Example Use Case

> A label wants to register a 3-track EP released in France on CD and digital.

Steps:

1. Register each Track MIDDS first (with ISRC, title, contributors...).
2. Create a Release MIDDS with:
    - EAN/UPC: `5054197648011`
    - Artist: [Artist MIDDS ID]
    - Tracks: list of 3 Track MIDDS IDs
    - Title: "Reflections EP"
    - Format: CD + Digital
    - Packaging: Digipack
    - Type: EP
    - Status: Official
    - Distributor: "Label Services France"
    - Country: France
    - Date: 2023-11-02
    - Cover contributors: graphic designer + photographer
3. Stake collateral proportional to size.
4. Submit and wait for certification.

Once validated, this release becomes a public, verifiable entry in the Allfeat catalog — usable by platforms, aggregators, and apps.

---

## 📘 See Also

- [🎧 Track →](./track.md)
- [🎼 Musical Work →](./musical-work.md)
- [🏢 Party Identifier →](./party-identifier.md)
- [📚 MIDDS Overview →](./overview.md)
- [🧩 Proof of Metadata →](../consensus/overview.md)
