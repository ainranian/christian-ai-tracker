# Report — 2026-09-10 source-watch baseline

Implemented Option 1: per-source HTTP validators and content hashes.

- Unique URLs watched: 74 (W-001–W-074)
- live 55 / blocked 16 / fail 3 / missing 0
- Hash method: SHA-256 of stripped HTML text (16 hex) or first 400k bytes
- Protocol: SOURCE-WATCH.md
- Human ledger: SOURCES.md
- Machine ledger: sources.json

Blocked on this probe (do not treat hashes as article text): NYT, AP, Axios, NCR, OSV, RNS, Lausanne, AI and Faith, ERLC, CUA policies, Biblica article host.

Fail: Magisterium overview 429; chai-global.org and kingdominnovations.us no response.

No project status codes were changed. This run only sets the baseline.
