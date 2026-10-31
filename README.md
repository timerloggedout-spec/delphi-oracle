# delphi-oracle

D0 Weekend Challenge — Delphi Oracle entry package, ported verbatim
from `timerloggedout-spec/termux-monorepo` (`apps/weekend-challenge-delphi-oracle/`,
PR #1702 lineage), together with the decision kernel it loads
(`scripts/delphi/strands_oracle_mvp.py`, PR #1620) and its offline
test suite (`tests/`).

Layout mirrors the source repo: the package loads its kernel by
relative path (`agent.py` → `../../scripts/delphi/strands_oracle_mvp.py`)
and the tests locate the app the same way, so the layout is part of
the package.

Run:

- Demo (live, read-only): `cd apps/weekend-challenge-delphi-oracle && python3 demo.py`
- Tests (offline): `python3 -m pytest tests/`
- Lambda smoke (local): `python3 lambda_handler.py` in the app directory

Receipts (completion-verified 2026-10-30): asserted-only → ABSTAIN
(0 API calls) · PR #1620 fetched evidence → ALLOW_RECOMMENDATION
(2 calls, 103 items) · credential_mutation → ESCALATE.

Deployment: none claimed — the handler runs locally; no AWS account
exists (owner card rule).
