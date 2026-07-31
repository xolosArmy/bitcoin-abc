# ADR-004: Subnet-ready, not an operational subnet

Status: Accepted

## Decision

The first Tonalli Shield cycle describes its architecture as `subnet-ready research`. It does not claim to implement an official eCash subnet or production L2.

## Rationale

The project does not currently have a public, implemented eCash interface for subnet registration, validator rules, shared security, or native L1 deposit and withdrawal enforcement. Simulating an abstract interface is useful; claiming infrastructure that does not exist would be misleading.

## Consequences

- L1-to-Shield interfaces are explicitly marked current, simulated, or future-dependent.
- No AVAX Avalanche subnet tooling is treated as eCash subnet infrastructure.
- The final campaign decision may be `SUBNET-READY-WAITING` even when the state-machine work succeeds.
- Public campaign language must follow `TERMINOLOGY.md`.
