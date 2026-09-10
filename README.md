# Christian AI Field Tracker

Living, sourced register of Christian institutions, research centres, ministry networks, startups, products, conferences, and journals working at the intersection of artificial intelligence and the Christian faith.

**Canonical repository:** https://github.com/ainranian/christian-ai-tracker

## Files

- [`DATABASE.md`](DATABASE.md) — project register plus append-only history
- [`SOURCES.md`](SOURCES.md) — Option 1 per-source watch ledger (human)
- [`sources.json`](sources.json) — same ledger (machine)
- [`SOURCE-WATCH.md`](SOURCE-WATCH.md) — how hashes, ETags, and status changes are recorded
- [`reports/`](reports/) — weekly deltas; prior weeks are never overwritten

## Update cadence

A Grok automation runs every Sunday at 07:00 Africa/Johannesburg. Each run must:

1. Load `sources.json` and re-fetch every watch URL
2. Record hash / ETag / Last-Modified / HTTP-class changes
3. Search for new projects and verify with primary URLs
4. Commit updated `DATABASE.md`, `SOURCES.md`, `sources.json`, and a new `reports/YYYY-MM-DD.md`

## Rules

- No unsourced claims
- If a training method is not published, record `not disclosed`
- Do not invent a ranked Top 200
- Blocked-page hashes are not content changes
