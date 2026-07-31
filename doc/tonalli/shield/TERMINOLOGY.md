# Terminology

| Term | Meaning in this project |
|---|---|
| Tonalli eCash Node | A documented xolosArmy fork/profile based on Bitcoin ABC. It is not a separate consensus network. |
| Tonalli Shield | The privacy research project. |
| Shield Core | The chain-independent state machine for notes, commitments, nullifiers, and proof verification. |
| Subnet-ready | Designed around an abstract future subnet interface. It does not mean an eCash subnet exists. |
| Subnet | Reserved for infrastructure officially specified and supported by eCash. Not claimed in the first cycle. |
| L2 | Not used as a current technical description. |
| Private note | User-controlled private data representing spending authority within the experimental state machine. |
| Public commitment | A public cryptographic commitment to private note data. |
| Nullifier | A public value intended to prevent a private note from being spent more than once without revealing the note itself. |
| Public state truth | Chain facts verified by the eCash node under an explicit finality policy. |
| Private authority truth | User-held secrets and approvals retained by Tonalli Wallet. |
| Chronik | An indexed node interface used for discovery and UX. It is not a consensus oracle. |
| Fixture-backed verifier | A test-only verifier that accepts only exact, registered, hashed vectors. |
| Real verifier | A future implementation that cryptographically verifies the selected proof system. |
| Mainnet | Explicitly outside the first 40-day campaign. |
| Saldo privado | A simulated or future note balance; not a mainnet product claim during this phase. |

## Communication rule

Public communication must prefer precise status language:

- "research"
- "simulation"
- "regtest planning"
- "subnet-ready"
- "not audited"
- "no real funds"

It must not imply:

- production privacy;
- guaranteed anonymity;
- an official eCash subnet;
- an operational L2;
- a completed bridge;
- audited security.
