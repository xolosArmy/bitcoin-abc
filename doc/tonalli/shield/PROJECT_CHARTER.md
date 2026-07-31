# Tonalli Shield project charter

## Mission

Produce reproducible evidence about whether a private-note state machine can be responsibly adapted to eCash and prepared for future subnet infrastructure.

## First-cycle scope

The first cycle is limited to:

- node and upstream traceability;
- current eCash capability mapping;
- BCH-to-eCash compatibility analysis;
- public/private authority boundaries;
- threat and privacy modeling;
- state-machine specification;
- note, commitment, and nullifier models;
- deterministic fixture-backed simulation;
- two-node regtest planning;
- wallet-node interface specification;
- backup and recovery design.

## Mandatory constraints

- No mainnet Shield transactions.
- No real funds.
- No consensus changes.
- No production RPC additions.
- No automatic signing or broadcasting.
- No remote service receives seeds, private keys, note secrets, witness secrets, or prover secrets.
- No CashTokens assumptions are treated as native eCash capabilities.
- Chronik is an indexed observation interface, not a consensus oracle.
- Unknown or conflicting state fails closed.
- Fixture test proof verification accepts only registered, hashed test vectors.

## Success criteria

The cycle succeeds when it produces an honest, reproducible decision, including a negative result. Shipping a mainnet feature is not a success criterion.

## Governance

- One capability per issue and pull request.
- Draft pull requests by default.
- Exact upstream and head SHAs recorded before review.
- Documentation, simulator, regtest, cryptography, wallet integration, and node changes remain separate.
- Security-relevant exceptions require an architecture decision record.
- Public claims must link to code, tests, logs, or explicitly identified assumptions.
