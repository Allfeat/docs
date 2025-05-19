# 🧾 Musical Work MIDDS

## Overview

The **Musical Work MIDDS** represents the **underlying composition** — the creative idea behind a song.  
It defines the musical structure, authorship, and identity of a piece of music, independently from how or when it's recorded.

This MIDDS is essential for connecting all recordings, adaptations, and releases back to their **original intellectual source**.

---

## 🧠 Why It Matters

In the music industry, the composition and lyrics of a song are **legally and artistically separate** from the recording.  
Many versions (studio, live, remixes) may come and go — but the work remains the foundation.

The Musical Work MIDDS allows Allfeat to:

- Document musical creations **at the source**,
- Reference them across multiple tracks and versions,
- Link contributors (composers, lyricists, arrangers) with clear roles,
- Make the **creative authorship verifiable and permanent**.

---

## 🏗️ Structure Summary

| Field           | Type                      | Description                                                                      |
| --------------- | ------------------------- | -------------------------------------------------------------------------------- |
| `iswc`          | `Iswc`                    | International Standard Work Code – the global ID for a composition.              |
| `title`         | `MusicalWorkTitle`        | The official or main title of the work.                                          |
| `creation_year` | `MusicalWorkCreationYear` | 4-digit Gregorian year the work was created.                                     |
| `instrumental`  | `bool`                    | Indicates if the work is purely instrumental.                                    |
| `language`      | `Option<Language>`        | Language of lyrics (if applicable).                                              |
| `bpm`           | `Option<MusicalWorkBpm>`  | Tempo in beats per minute (optional).                                            |
| `key`           | `Option<Key>`             | Musical key (e.g., C, F#, etc.) (optional).                                      |
| `mode`          | `Option<Mode>`            | Musical mode (major, minor, etc.) (optional).                                    |
| `work_type`     | `MusicalWorkType`         | Original, adaptation, mashup, or medley.                                         |
| `participants`  | `MusicalWorkParticipants` | List of Party Identifier MIDDS (e.g., authors, composers), each with their role. |

---

## 🧬 Identifiers and Linking

Like other MIDDS, a Musical Work uses:

| Type           | Description                                                         |
| -------------- | ------------------------------------------------------------------- |
| **Allfeat ID** | Unique on-chain identifier.                                         |
| **RW-ID**      | `ISWC`, used globally in publishing databases (SACEM, ASCAP, etc.). |

This ensures:

- Strong traceability between on-chain and traditional metadata,
- Trust in the connection between works, recordings, and rights claims.

---

## 🔗 Usage in the Allfeat Graph

Musical Work MIDDS are referenced by:

- `Track` MIDDS → every time the work is recorded or performed.
- `Party Identifier` MIDDS → for assigning authorship roles.
- `Release` MIDDS → indirectly, through the Tracks included.

This makes the Musical Work a **central node** in the music metadata graph — anchoring intellectual creation to all derived assets.

---

## 🚀 Who Creates This MIDDS?

- **Providers**: songwriters, publishers, catalog managers, or anyone registering a musical work.
- **Trusters**: validators who confirm the accuracy and uniqueness of the metadata.

Like other MIDDS, the cost to publish depends on **data weight** — more detail = more collateral.

---

## 🛠️ Example Use Case

> A songwriter wants to register their new composition titled "Midnight Echoes".

Steps:

1. Set the ISWC: `T-123.456.789-0` (or leave blank if not yet assigned).
2. Title: "Midnight Echoes"
3. Creation Year: 2024
4. Instrumental: false
5. Language: English
6. BPM: 102
7. Key: G major
8. Mode: Major
9. Work Type: Original
10. Participants: two authors (linked via Party Identifier MIDDS), one lyricist, one composer
11. Submit and stake required collateral
12. Wait for Trusters to review and certify

Once certified, this work can be reused in multiple Tracks, across multiple Releases, with persistent attribution.

---

## 📘 See Also

- [🎧 Track →](./track.md)
- [📦 Release →](./release.md)
- [🏢 Party Identifier →](./party-identifier.md)
- [📚 MIDDS Overview →](./overview.md)
- [🧩 Proof of Metadata →](../consensus/pom.md)
