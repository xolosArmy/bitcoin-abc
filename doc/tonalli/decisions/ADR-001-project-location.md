# ADR-001: Project location

Status: Accepted for the documentation-zero phase

## Decision

Protocol-facing research, node capability mapping, regtest evidence, and the L1 interface specification live under `doc/tonalli/` in the xolosArmy Bitcoin ABC fork.

Wallet secrets, user approval, signing, proof generation, and encrypted note recovery remain outside the node boundary. Shield Core may be extracted into a separate repository once its interface stabilizes.

## Rationale

Keeping node-facing assumptions near the node source makes unsupported consensus, Chronik, Avalanche, RPC, and regtest claims easier to detect. Keeping private authority outside the node prevents the fork from becoming a custodian or an unnecessarily invasive consensus patch.

## Consequences

- The fork is the documentary home of public-state research.
- It is not necessarily the permanent home of all cryptographic implementation.
- Changes remain modular and capability-specific.
