# 🧾 Track

## Overview

The **Track MIDDS** represents a **specific recorded performance** or **production** of a musical work.

It connects a performance to its **underlying composition**, the **people involved in its production**, and **technical metadata** like tempo, genre, and location of creation.

Each Track has a globally recognized **ISRC** and links to:

- the `Musical Work` it's based on,
- the `Party Identifiers` of performers, producers, engineers, and contributors.

---

## 🧠 Why It Matters

In music metadata, tracks are where **creative intent becomes tangible**.  
They are what listeners hear, what gets distributed to platforms, and what generates royalties.

Yet many different recordings can stem from the same musical work (e.g., original, live, acoustic, remix).  
That’s why Allfeat treats each Track as a **distinct, structured MIDDS**, allowing:

- Precise attribution of every participant,
- Accurate linking to the source composition,
- Transparent technical metadata about the recording.

---

## 🏗️ Structure Summary

| Field             | Type                  | Description                                                                          |
| ----------------- | --------------------- | ------------------------------------------------------------------------------------ |
| `isrc`            | `Isrc`                | The **International Standard Recording Code**, a global ID for this exact recording. |
| `musical_work`    | `MiddsId`             | Reference to the registered **Musical Work MIDDS** it is based on.                   |
| `artist`          | `MiddsId`             | Main performer or credited artist (Party Identifier MIDDS).                          |
| `producers`       | `TrackProducers`      | List of producers involved (Party Identifier MIDDS).                                 |
| `performers`      | `TrackPerformers`     | All musicians and vocalists performing in the track.                                 |
| `contributors`    | `TrackContributors`   | Other contributors like sound engineers, featured artists, etc.                      |
| `title`           | `TrackTitle`          | Official title of the track.                                                         |
| `title_aliases`   | `TrackTitleAliases`   | Optional list of alternate or local titles.                                          |
| `recording_year`  | `TrackRecordYear`     | The year the track was recorded (Gregorian year).                                    |
| `genre`           | `TrackGenre`          | Primary musical genre of the track.                                                  |
| `genre_extras`    | `TrackGenreExtras`    | Optional list of secondary genres.                                                   |
| `version`         | `TrackVersion`        | Type/version of the recording (Remix, Live, Acoustic...).                            |
| `duration`        | `TrackDuration`       | Duration in seconds.                                                                 |
| `bpm`             | `TrackBeatsPerMinute` | Tempo in beats per minute.                                                           |
| `key`             | `Key`                 | Musical key of the track.                                                            |
| `mode`            | `Mode`                | (Optional) Musical mode (major/minor).                                               |
| `recording_place` | `TrackRecordingPlace` | Free-text field for where the track was recorded.                                    |
| `mixing_place`    | `TrackMixingPlace`    | Free-text field for where mixing occurred.                                           |
| `mastering_place` | `TrackMasteringPlace` | Free-text field for where mastering was done.                                        |

---

## 🧬 Identifiers and Linking

All Track MIDDS follow the **dual-identifier principle**:

| Type           | Description                                                          |
| -------------- | -------------------------------------------------------------------- |
| **Allfeat ID** | Internal on-chain identifier generated at creation.                  |
| **RW-ID**      | The `ISRC`, used globally to identify this specific sound recording. |

These allow:

- Web2 → Web3 traceability for existing recordings,
- Easy linkability with platforms, DSPs, or catalog systems,
- Reliable reuse in Releases, Playlists, and Music Graphs.

---

## 🔗 Usage in the Allfeat Graph

Track MIDDS are highly connected objects in the metadata graph:

- Linked to `Musical Work` MIDDS → to reflect what was performed.
- Linked to `Party Identifier` MIDDS → to reflect who performed, produced, mixed, etc.
- Referenced by `Release` MIDDS → when compiled into an album or single.

This architecture enables:

- Transparent **attribution**,
- Rich **relational data** across contributors and creations,
- Support for reuse, versioning, and derivative metadata.

---

## 🚀 Who Creates This MIDDS?

- **Providers**: professionals or organizations registering new or existing tracks.
- **Trusters**: validators who verify that metadata is coherent and corresponds to real-world releases.

Publishing a Track requires **staking collateral** proportional to the **byte size** of the metadata (e.g., more aliases, detailed credits = higher cost).

This prevents spam and ensures economic alignment.

---

## 🛠️ Example Use Case

> A label wants to register the studio version of “Blinding Lights” by The Weeknd.

They would:

1. Provide the ISRC of the recording.
2. Reference the existing Musical Work MIDDS it is based on.
3. Set the artist as The Weeknd (Party Identifier).
4. Add producers, performers, sound engineers.
5. Specify:
    - Title: "Blinding Lights"
    - Version: Studio
    - Recording Year: 2019
    - BPM: 171
    - Key: F minor
    - Duration: 200s
6. Optionally fill in recording/mixing/mastering locations if known.
7. Stake tokens and submit the MIDDS.
8. Wait for Trusters to validate it.

Once certified, the Track MIDDS is available to reference in Releases, analytics, or rights data.

---

## 📘 See Also

- [🎼 Musical Work →](./musical-work.md)
- [🏢 Party Identifier →](./party-identifier.md)
- [📦 Release →](./release.md)
- [📚 MIDDS Overview →](./overview.md)
- [🧩 Proof of Metadata →](../consensus/pom.md)
