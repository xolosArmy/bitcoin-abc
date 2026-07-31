# Tonalli Shield

Tonalli Shield is a research project for a privacy-oriented state machine that may be adapted to future eCash subnet infrastructure.

Current classification: **subnet-ready research, not an operational subnet**.

## Research question

Can a non-custodial system of private notes, public commitments, nullifiers, deterministic state reconstruction, and zero-knowledge verification be designed for eCash without weakening the user's control of keys or making unsupported assumptions about current eCash subnet capabilities?

## Architectural boundary

```text
Bitcoin ABC / eCash L1
        |
Tonalli node adapter
        |
Tonalli Shield Core
        |
Tonalli Wallet + local prover
```

The node establishes public chain facts. Shield Core defines the privacy state machine. Tonalli Wallet retains private spending authority and user approval.

## Reference implementation

ShieldKit-SDK is a research reference. Its BCH-specific network configuration, CashTokens-dependent state mechanism, scripts, profiles, and production assumptions are not portable to eCash by renaming prefixes. Each component must be classified independently as portable, adaptable, redesign-required, unsupported, or unknown.

## Initial outcome

The first 40-day cycle produces documentation and evidence supporting one decision:

- `GO-REGTEST`
- `SUBNET-READY-WAITING`
- `REDESIGN`
- `NO-GO`

No decision authorizes mainnet or real funds.
