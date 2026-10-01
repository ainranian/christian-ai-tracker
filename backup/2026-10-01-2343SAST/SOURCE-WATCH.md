# Source watches

Ledger: SOURCES.md
Register: DATABASE.md

One watch (W-nnn) per unique cited URL. Several project IDs may share a URL.

Check order: HTTP class (live/blocked/missing/fail) → ETag → Last-Modified → live text hash → redirect target.

- Unchanged: update last_checked only.
- Changed: record previous validators in reports/YYYY-MM-DD.md; update the watch; history line on linked IDs.
- New URL → new W-nnn.
- Blocked-page hashes are not content changes.
- HTTP validators: https://httpwg.org/specs/rfc7232.html
