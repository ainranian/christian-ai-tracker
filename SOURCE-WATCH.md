# Option 1 — per-source watch protocol

Applies to https://github.com/ainranian/christian-ai-tracker

Operational ledger: `SOURCES.md` (human) and `sources.json` (machine).
Register of projects: `DATABASE.md`.

## What is tracked

One watch (`W-nnn`) per unique cited URL. Several project IDs may share one watch.

Fields:

- `fetch`: `live` (HTTP 2xx/3xx), `blocked` (401/403), `missing` (404), `fail` (timeout/other)
- `http`: status code
- `etag`, `last_modified`: HTTP validators when the origin sends them
- `hash`: SHA-256 of stripped visible text (HTML) or first 400k bytes (other), first 16 hex chars
- `last_checked`: date of last fetch
- `last_changed`: date the hash, etag, last-modified, HTTP class, or URL target last differed

Validators follow HTTP conditional-request practice: https://httpwg.org/specs/rfc7232.html and https://developer.mozilla.org/en-US/docs/Web/HTTP/Conditional_requests

## Weekly procedure

1. Load `sources.json`.
2. For each watch, request the URL (HEAD then GET if needed) with `If-None-Match` / `If-Modified-Since` when those validators exist.
3. Compare, in this order:
   - HTTP class change (`live` ↔ `blocked`/`missing`/`fail`)
   - ETag change
   - Last-Modified change
   - Hash change (only treat as content change when `fetch` is `live`)
   - Redirect target change (`final_url`)
4. If nothing changed: update `last_checked` only.
5. If something changed:
   - write previous hash/etag/http into that week’s `reports/YYYY-MM-DD.md`
   - update the watch row
   - set `last_changed`
   - append a history line on every listed project ID in `DATABASE.md`
6. Add a new `W-nnn` when a new source URL is cited. Never reuse a watch ID.
7. Do not treat a blocked-page hash as article content. Re-check blocked URLs with a browser tool before changing project status.

## Status mapping from source health

- Source `missing` for two consecutive runs: consider project `dormant` only if no replacement official URL is found.
- Source `blocked`: keep project status; record fetch failure; do not invent a content change.
- Source `live` and page now says the programme ended: change project status with a quoted sentence and the URL.

## Noise control

Hash only stripped text, not full HTML with scripts. Ignore cookie banners and rotating home-page modules when a narrower official programme URL exists.
