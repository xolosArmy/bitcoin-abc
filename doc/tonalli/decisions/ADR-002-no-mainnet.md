# ADR-002: No mainnet in the first cycle

Status: Accepted

## Decision

The first Tonalli Shield cycle cannot construct, sign, broadcast, or accept real-funds Shield operations on eCash mainnet.

## Enforcement requirements

- No mainnet Shield transaction builder.
- No mainnet broadcast path.
- No real-funds deposit address or pool.
- Test-only verification cannot be enabled by an environment variable in a production build.
- Mainnet activation requires a later architecture decision, independent review, audit evidence, and explicit human authorization.

## Rationale

The current project has no selected production proof system, no audited verifier, no native subnet interface, no demonstrated bridge, and no current implementation base. A mainnet path would create risk without defensible security evidence.

## Consequence

A successful 40-day campaign may authorize only a later regtest phase.
