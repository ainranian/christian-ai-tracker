# Open issues

Not a register. Each item has one ID. Do not reuse an ID.

## Status values

`open` · `in-progress` · `fixed` · `rejected`

## Rules

- New item: next OI-nnn, status `open`, opened date, one-line statement, source file if any.
- When work starts, set status `in-progress` and add a log line.
- When implemented or repaired, set status `fixed` and add a log line with the file or commit.
- When declined, set status `rejected` and add a log line with the reason.
- Do not delete a row. Status and the log are the history.
- The live register below holds `open` and `in-progress` only. `fixed` and `rejected` rows are in the closed table.

## Register

| ID | Status | Opened | Statement |
|---|---|---|---|
| OI-001 | open | 2026-10-01 | Cell audit is not finished for every note. Page checks on 2026-10-02 confirmed A-001, A-014, B-001, and F-027. Twenty-two rows still cite only https://faith.tools/artificial-intelligence-ai. Eighteen hosts still need a browser pass where curl returned 403. |
| OI-002 | open | 2026-10-01 | Curl returned HTTP 403 for NYT, AP, Axios, Lausanne, NCR, OSV, Religion News, Notre Dame ethics, aiandfaith.org, Catholic University policy, Commonweal, and Biblica. ERLC was confirmed by a page fetch: Artificial Intelligence: An Evangelical Statement of Principles. https://erlc.com/policy-content/artificial-intelligence-an-evangelical-statement-of-principles/ |
| OI-003 | open | 2026-10-01 | https://chai-global.org/ and https://www.kingdominnovations.us/ returned no HTTP response. https://sites.google.com/view/chai-global/ says the site moved and does not give the new domain. |
| OI-004 | open | 2026-10-01 | https://www.magisterium.com/overview loaded and describes Magisterium AI. The infrastructure blog URL for A-016 and A-017 was not re-fetched after the earlier HTTP 429. |
| OI-007 | open | 2026-10-01 | Twenty-two rows still cite only https://faith.tools/artificial-intelligence-ai. A dedicated product URL is still needed for each. |
| OI-010 | open | 2026-10-01 | The source ledger stops at W-074 and does not include G-013, G-014, or F-029. The ledger is the archival appendix of README.md. |
| OI-015 | open | 2026-10-02 | Review the no-reuse rule after the OI-006 exception. Vacated IDs A-015, A-018, A-019, A-020, F-013, F-020–F-026, G-010, G-011 stay unused. |
| OI-016 | open | 2026-10-02 | The source ledger in the README appendix is archival. It is not required once the DATABASE.md audit and verification (OI-001) is complete. |

## Closed

| ID | Status | Opened | Statement |
|---|---|---|---|
| OI-005 | fixed | 2026-10-01 | A-001 URL loaded as Antiqua et Nova, Note on the Relationship Between Artificial Intelligence and Human Intelligence, 28 January 2025. Curl 404 was a client block. https://www.vatican.va/roman_curia/congregations/cfaith/documents/rc_ddf_doc_20250128_antiqua-et-nova_en.html |
| OI-006 | fixed | 2026-10-01 | Exceptional renumber so ID prefix matches Cat. Old IDs not reused. |
| OI-008 | fixed | 2026-10-01 | F-027 source corrected from the Faith Assistant page to https://faith.tools/app/833-bible-vector-search. Page describes embedding search over BBE, open source, Antioch Tech. |
| OI-009 | fixed | 2026-10-01 | Removed "see local". Lilly, Zurich franc, and download figures marked as not in DATABASE.md. |
| OI-011 | rejected | 2026-10-01 | Requested filename DATABASE-WATCH.ms was not used. Content is in README.md. |
| OI-012 | fixed | 2026-10-02 | Landscape example URL set to the register rc_ddf_doc path. |
| OI-013 | rejected | 2026-10-02 | Duplicate of OI-003. |
| OI-014 | rejected | 2026-10-02 | Duplicate of OI-005. |

## Log

| Date | ID | From | To | Note |
|---|---|---|---|---|
| 2026-10-01 | OI-001 | — | open | Carried from the unnumbered list. |
| 2026-10-01 | OI-002 | — | open | Carried from the unnumbered list. |
| 2026-10-01 | OI-003 | — | open | Carried from the unnumbered list. |
| 2026-10-01 | OI-004 | — | open | Carried from the unnumbered list. |
| 2026-10-01 | OI-005 | — | open | Carried from the unnumbered list. |
| 2026-10-01 | OI-006 | — | open | Carried from the unnumbered list. |
| 2026-10-01 | OI-007 | — | open | Carried from the unnumbered list. |
| 2026-10-01 | OI-008 | — | open | Carried from the unnumbered list. |
| 2026-10-01 | OI-009 | — | open | Carried from the unnumbered list. |
| 2026-10-01 | OI-010 | — | open | Carried from the unnumbered list. |
| 2026-10-01 | OI-011 | open | rejected | .ms not used. Content now lives in README.md. |
| 2026-10-02 | OI-006 | open | fixed | Prefix renumber. |
| 2026-10-02 | OI-009 | open | fixed | Landscape stale note and unverified figures removed. |
| 2026-10-02 | OI-012 | open | fixed | Landscape URL corrected. |
| 2026-10-02 | OI-013 | open | rejected | Duplicate of OI-003. |
| 2026-10-02 | OI-014 | open | rejected | Duplicate of OI-005. |
| 2026-10-02 | OI-005 | open | fixed | Page fetch returned the 28 January 2025 note. |
| 2026-10-02 | OI-008 | open | fixed | F-027 source set to faith.tools app 833. |
| 2026-10-02 | OI-001 | open | open | Scope narrowed. Not every note page-checked. |
| 2026-10-02 | OI-002 | open | open | ERLC page confirmed. Other 403 hosts not all opened. |
| 2026-10-02 | OI-004 | open | open | Overview page loaded. Blog URL not re-fetched. |
