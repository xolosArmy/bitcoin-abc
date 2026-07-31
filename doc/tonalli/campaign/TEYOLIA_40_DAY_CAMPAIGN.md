# Teyolia - Tonalli Shield Node Research

Duration: 40 calendar days

Campaign objective: document, specify, and test the foundations of a subnet-ready privacy state machine from the Tonalli eCash Node research fork, without modifying consensus or using real funds.

## Campaign promise

The campaign finances evidence, code review, specifications, deterministic fixtures, and an honest technical decision. It does not sell anonymity, investment returns, an official subnet, or a mainnet product.

## Precondition

Implementation milestones are blocked until the stale Bitcoin ABC base is synchronized through a separate reviewed pull request. Documentation work may continue on the pinned base.

## Milestones

### Days 1-4 - Node identity and upstream traceability

- Pin official upstream and Tonalli SHAs.
- Record build inputs and repository status.
- Define the synchronization policy.
- Publish the documentation-zero pull request.

Gate: a reviewer can identify the exact base and reproduce the repository state.

### Days 5-8 - Current eCash capability map

Classify node, Chronik, Avalanche, RPC, regtest, script, and indexing capabilities as:

- `AVAILABLE`
- `PARTIAL`
- `REQUIRES_EXTENSION`
- `NOT_AVAILABLE`
- `UNKNOWN`

Gate: current capabilities are separated from future roadmap assumptions.

### Days 9-12 - Threat, privacy, and trust models

- Node versus indexer authority.
- Public versus private truth.
- Reorganizations and finality.
- Prover, wallet, bridge, and validator threats.
- Secret-handling and repository controls.

Gate: every trusted component and failure mode is explicit.

### Days 13-16 - State-machine specification

Specify deposit intent, accepted deposit, private transfer, withdrawal intent, finalized withdrawal, nullifier insertion, state-root update, rejection, replay protection, and recovery.

Gate: each transition has prior state, public inputs, private inputs, required proof, resulting state, and rejection conditions.

### Days 17-20 - L1 and future-subnet interface

Separate:

- interfaces available in the current node;
- interfaces simulated for research;
- interfaces dependent on future eCash subnet support.

Gate: no simulated function is represented as a current eCash capability.

### Days 21-24 - Deterministic simulator

- Reproduce state transitions from fixtures.
- Use only registered fixture-backed proof results.
- Reject unknown fixtures.
- Do not sign, broadcast, or modify consensus.

Gate: clean executions produce identical state roots and logs.

### Days 25-28 - Two-node regtest design

Test explicit event-driven scenarios:

- block production;
- network partition;
- competing branches;
- duplicated nullifiers;
- reorganization;
- rollback and replay;
- node/Chronik disagreement;
- restart and reconstruction.

Gate: tests do not depend on wall-clock sleeps for correctness.

### Days 29-32 - Backup and recovery model

Demonstrate the planned sequence:

`create note -> encrypt backup -> delete local state -> reconstruct public state -> import backup -> recover private authority`

Gate: corrupt or cross-domain backups are rejected.

### Days 33-36 - Read-only Tonalli Wallet interface

Specify or prototype display of node identity, state root, sequence, local notes, backup status, and simulated deposit or withdrawal previews.

Gate: no active signing, broadcast, or real-funds path exists.

### Days 37-40 - Reproducibility and final decision

Publish exact commits, build inputs, test commands, logs, hashes, known failures, residual risks, and one decision:

- `GO-REGTEST`
- `SUBNET-READY-WAITING`
- `REDESIGN`
- `NO-GO`

## Reporting cadence

A public update is published every four days. Each update records:

- completed work;
- exact commit;
- tests and evidence;
- new assumptions or risks;
- budget status;
- next milestone.

## Prohibited campaign claims

- production-ready privacy;
- guaranteed anonymity;
- official eCash subnet;
- operational L2;
- audited security;
- mainnet deposits or withdrawals;
- CashTokens compatibility with eCash.

## Principle

> We are not unilaterally creating an official eCash subnet. We are documenting, specifying, and testing from our own Tonalli eCash Node what protocol support would be required.
