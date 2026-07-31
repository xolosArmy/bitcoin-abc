# Upstream tracking

## Current pinned base

| Field | Value |
|---|---|
| Tonalli repository | `xolosArmy/bitcoin-abc` |
| Tonalli default branch | `master` |
| Tonalli pinned base SHA | `87a9b0f93fd9e65e9b65d6042ed2646652365aa4` |
| Base commit date | 2025-08-21 UTC |
| Official public repository | `Bitcoin-ABC/bitcoin-abc` |
| Official public tip observed | `600dd060bd242d809a06ff1fcee5900acf363867` |
| Observation date | 2026-07-31 UTC |
| Public upstream distance | 1,943 commits ahead of the Tonalli base |

## Consequence

The current Tonalli fork is suitable only as a pinned documentation base. It must not be treated as a current implementation base for protocol, Chronik, Avalanche, RPC, consensus, or security claims.

No implementation work for Tonalli Shield may begin until an explicit upstream synchronization decision is reviewed and recorded.

## Required synchronization procedure

1. Identify the intended official Bitcoin ABC release or exact upstream commit.
2. Record the release tag, commit SHA, release date, and source location.
3. Compare the Tonalli fork against that base.
4. Review security-sensitive changes affecting:
   - consensus;
   - script validation;
   - Chronik;
   - Avalanche finality;
   - RPC;
   - regtest;
   - build and dependency systems.
5. Synchronize through a dedicated branch and pull request.
6. Run the upstream build and test requirements before accepting the new base.
7. Record the resulting Tonalli base SHA in this document.

## Development source note

The Bitcoin ABC repository documentation states that GitHub contains source code releases while active development takes place through the Bitcoin ABC review system. Tracking must therefore consider official releases and reviewed upstream changes, not blindly rebase against an assumed daily GitHub development branch.

## Policy

- Never overwrite `master` with Tonalli experiments.
- Never force-push the default branch.
- Never mix upstream synchronization with Tonalli Shield implementation.
- Every campaign evidence package must include the exact upstream and Tonalli SHAs.
- A stale base must produce a fail-closed implementation gate.
