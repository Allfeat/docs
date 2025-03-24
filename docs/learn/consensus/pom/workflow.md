# Proof-of-Metadata (PoM) Generic Workflow

### 1. **MIDDS Submission**

-   **Provider Action**:

    -   Submits a MIDDS entity to the blockchain.
    -   Pays transaction fees $F$ and locks collateral $C$.

-   **Outcome**:

    -   MIDDS becomes **immutable** (sealed) with status: `Non-Certified`.

---

### 2. **Certification Process**

#### Staking Phase

-   **Truster Participation**:
    -   Trusters stake tokens $T_{i}$ to support certification.
    -   Individual stake cap: $T_{i} ≤ T_{max}$ (prevents dominance).
-   **Certification Threshold**:

    -   Total required stake: $T_{total} ≥ T_{min}$
    -   Certification achieved when:
        $sum_{i=1}^{n} T_i \geq T_{min}$

---

### 3. **Reward Distribution**

-   **Reward Pool Composition**:

    $R_{pool} = R_{tips} + R_{treasury}$

    -   $R_{tips}$: Voluntary contributions from Provider
    -   $R_{treasury}$: Protocol incentives

-   **Reward Allocation**:
    -   Each Truster receives proportionally to their stake:
        `R_i = (T_i / T_total) * R_pool`

---

### 4. **Contestation Mechanism**

-   **Time Window**: Fixed duration $τ$ called **pre-certification** period.
-   **Contestation Logic**:
    -   Any party can contest by staking $C_{contest}$ ≥ $C_{min}$.
    -   Fairness determined via decentralized voting.
-   **Outcomes**:
    -   **Fair Contest**:
        -   MIDDS purged from chain.
        -   Slashing: Trusters lose $S_{slash} * T_{i}$.
    -   **Unfair Contest**:
        -   MIDDS remains certified.
        -   Contestator loses $C\_{contest}$

---
