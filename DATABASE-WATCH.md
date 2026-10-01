# DATABASE-WATCH

Companion to DATABASE.md. This file holds rules, categories, status values, the source-watch method, and history. The register table is only in DATABASE.md. The per-URL ledger remains SOURCES.md.

## Rules

- One named organisation, product, document, or conference = one ID.
- Alliances and platforms do not absorb members or child products.
- Do not delete or reuse IDs.
- Every fact needs a full URL. Unpublished training method = `not disclosed` / `unverified-method`.
- Parent = owning or hosting organisation used for grouping.
- Weekly run: update DATABASE.md in place; put superseded copies in `backup/` or `archive/`.
- ID prefix and Cat may differ. Cat is the product type. The ID prefix is the original cluster. Do not renumber to force a match.

## Status

`active` · `proposed` · `event` · `publication` · `prototype` · `unverified-method` · `dormant` · `closed`

## Categories

- A Holy See / Catholic magisterial and university
- B Protestant / evangelical / ecumenical research
- C Digital theology centres, journals, working groups
- D Bible translation and missions engineering
- E Faith-tech platforms, incubators, networks
- F Consumer Bible / prayer / companion apps
- G Church operations and sermon tools

## Source-watch method

Ledger: SOURCES.md. Register: DATABASE.md.

One watch (W-nnn) per unique cited URL. Several project IDs may share a URL.

Check order: HTTP class (live/blocked/missing/fail) → ETag → Last-Modified → live text hash → redirect target.

- Unchanged: update last_checked only.
- Changed: record previous validators in reports/YYYY-MM-DD.md; update the watch; history line on linked IDs.
- New URL → new W-nnn.
- Blocked-page hashes are not content changes.
- HTTP validators: https://httpwg.org/specs/rfc7232.html

## History

### 2026-10-01 split
- DATABASE.md reduced to the register table. Rules, categories, and history moved here.
- G-013, G-014, and F-029, which sat below a blank line and outside the table, folded into the table. 135 IDs.
- SOURCE-WATCH.md protocol copied here. SOURCE-WATCH.md kept as a pointer.

### 2026-10-01 restore
- Restored after commit 7658343 replaced DATABASE.md with the 9-byte string `see local`.
- 132 rows from blob 1fb9da98f138d6914edd514461a679949f30312b (commit d48afd6).
- Three rows researched 2026-09-13 appended: G-013, G-014, F-029.

### 2026-09-10
- Unified seed (86) + restored session records (46). Total 132.
- Added Parent column.
- Older split files moved to archive/2026-09-10/.
