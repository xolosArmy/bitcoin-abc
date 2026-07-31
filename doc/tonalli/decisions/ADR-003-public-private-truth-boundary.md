# ADR-003: Public and private truth boundary

Status: Accepted

## Decision

Tonalli Shield separates two authorities.

### Public-state authority

The eCash node determines public chain facts under an explicit validation and finality policy, including transaction order, UTXO status, reorganizations, published commitments, and published nullifiers.

### Private spending authority

Tonalli Wallet retains note secrets, wallet keys, proof witness material, encrypted backups, user approval, and signing authority.

## Rationale

A privacy protocol node can validate public proofs and state transitions without knowing the user's complete private state. Treating the node as the owner of all truth would either be inaccurate or require disclosure of secrets that must remain with the user.

## Consequences

- Loss of private note backups may make funds unrecoverable even when public state remains available.
- The node cannot reconstruct private authority.
- The wallet cannot override public chain state.
- Node/indexer disagreement fails closed.
