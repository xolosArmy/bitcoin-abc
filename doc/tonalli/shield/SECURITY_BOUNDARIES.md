# Security boundaries

## Public state authority

The eCash node is authoritative for public chain facts available under its configured validation and finality policy:

- block and transaction ordering;
- UTXO existence and spend status;
- chain reorganizations;
- confirmation state;
- published commitments;
- published nullifiers;
- public deposit and withdrawal records.

Chronik may discover and index these facts, but disagreement between Chronik and the node must fail closed.

## Private spending authority

Tonalli Wallet is authoritative for user-held private material:

- wallet seed and private keys;
- note secrets and blind factors;
- witness material;
- local proof-generation inputs;
- user approval;
- encrypted backups.

The node, indexer, adapter, campaign infrastructure, and remote services must not receive this material.

## Prover boundary

A future prover must be local or otherwise designed so that private witness data is not disclosed to an untrusted service. The first simulator may use only a fixture-backed test verifier that accepts registered vectors by exact hash. A permissive verifier that returns success for arbitrary input is prohibited.

## Network boundary

- RPC remains private.
- Public Chronik access must be treated as untrusted input until node-confirmed.
- Mainnet activation cannot be controlled by a simple environment variable.
- Test-only components must be excluded from production builds, not merely disabled at runtime.

## Repository boundary

Never commit:

- wallet files;
- RPC credentials or cookies;
- Avalanche or staking private keys;
- mnemonic phrases;
- WIF keys;
- note or witness secrets;
- prover secrets;
- live `.env` files;
- private infrastructure addresses or unredacted operational logs.

`.gitignore` is not a security control by itself. Future implementation phases require local hooks and CI secret scanning.

## Fail-closed conditions

The system must reject or pause when:

- upstream identity is unknown;
- network, genesis, protocol version, profile, or instance does not match;
- the node and indexer disagree;
- history is incomplete or reordered;
- a nullifier is duplicated;
- a state root cannot be reproduced;
- a proof or fixture is unknown;
- finality requirements are not met;
- recovery data is corrupt or belongs to another domain.
