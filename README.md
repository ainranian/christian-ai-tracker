# Christian AI Field Tracker

Living, sourced register of Christian institutions, research centres, ministry networks, startups, products, conferences, and journals working at the intersection of artificial intelligence and the Christian faith.

**Canonical repository:** https://github.com/ainranian/christian-ai-tracker

## Files

- [`DATABASE.md`](DATABASE.md) — current register plus append-only history log
- [`reports/`](reports/) — weekly delta reports; prior weeks are never overwritten

## Update cadence

A Grok automation runs every Sunday at 07:00 Africa/Johannesburg. Each run is required to:

1. Search and verify new or changed projects with primary URLs
2. Add new IDs without reusing old ones
3. Append a history line to each touched project
4. Commit an updated `DATABASE.md` and a new `reports/YYYY-MM-DD.md`

## Rules

- No unsourced claims
- If a training method (pretraining, fine-tuning, RAG, LoRA) is not published, record `not disclosed`
- Do not invent a ranked Top 200

## Status codes

`active` · `proposed` · `event` · `publication` · `prototype` · `unverified-method` · `dormant` · `closed`
