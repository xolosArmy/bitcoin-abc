# Tonalli eCash Node Research

Status: **documentation-only research**

This directory is the documentation home for xolosArmy Network research that must be grounded in the behavior, interfaces, and security boundaries of an eCash node.

The work is complementary infrastructure for eCash. It is not a hostile fork, an alternative consensus network, or a claim that xolosArmy can unilaterally create an official eCash subnet.

> Sovereignty is not isolation. Sovereignty is the ability to verify.

## Scope

The initial research track is **Tonalli Shield**, a subnet-ready privacy state-machine study inspired by ShieldKit-SDK. The first cycle is limited to documentation, capability mapping, threat modeling, deterministic simulation, and regtest planning.

The node-side research establishes the public facts that applications may rely on:

- transaction inclusion and ordering;
- UTXO existence and spend status;
- chain reorganizations;
- confirmation and finality policy;
- public commitments and published nullifiers;
- reproducible fixtures and node observations.

Tonalli Wallet remains responsible for private authority:

- note secrets;
- spending authority;
- local proof generation;
- user approval;
- signing keys;
- encrypted backup and recovery.

The node must never require custody of wallet seeds, private keys, note secrets, witness secrets, or prover secrets.

## Repository policy

- `master` is intended to track Bitcoin ABC source releases and must not receive Tonalli experiments directly.
- Tonalli changes are developed in isolated branches and draft pull requests.
- Documentation, simulators, regtest harnesses, and any future node changes must be separated by capability.
- Consensus, RPC, and production behavior are out of scope for the documentation-zero pull request.
- Every research cycle must pin an exact upstream commit and an exact Tonalli commit.

See [UPSTREAM_TRACKING.md](UPSTREAM_TRACKING.md) before using this fork as a technical base.

## Tonalli Shield documents

- [Project overview](shield/README.md)
- [Project charter](shield/PROJECT_CHARTER.md)
- [Current status](shield/CURRENT_STATUS.md)
- [Security boundaries](shield/SECURITY_BOUNDARIES.md)
- [Terminology](shield/TERMINOLOGY.md)
- [40-day Teyolia campaign](campaign/TEYOLIA_40_DAY_CAMPAIGN.md)

## Architecture decisions

- [ADR-001: Project location](decisions/ADR-001-project-location.md)
- [ADR-002: No mainnet](decisions/ADR-002-no-mainnet.md)
- [ADR-003: Public and private truth boundary](decisions/ADR-003-public-private-truth-boundary.md)
- [ADR-004: Subnet-ready, not a subnet](decisions/ADR-004-subnet-ready-not-subnet.md)

## Non-goals of the first 40 days

The first campaign does not deliver:

- an official eCash subnet;
- a production L2;
- a mainnet shielded pool;
- a native L1-to-subnet bridge;
- production zero-knowledge circuits;
- an audited prover or verifier;
- real-funds deposits or withdrawals;
- consensus changes to Bitcoin ABC.

The intended result is a documented decision supported by reproducible evidence: `GO-REGTEST`, `SUBNET-READY-WAITING`, `REDESIGN`, or `NO-GO`.
