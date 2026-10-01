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

## Register

| ID | Status | Opened | Statement |
|---|---|---|---|
| OI-001 | open | 2026-10-01 | Full cell-by-cell fact audit of all 135 notes is unfinished. The 2026-10-01 run checked HTTP status for 87 URLs and page text for G-013, G-014, F-029, B-020, F-023, and E-007 only. |
| OI-002 | open | 2026-10-01 | Eighteen source URLs return HTTP 403 to a non-browser client (NYT, AP, Axios, ERLC, Lausanne, NCR, OSV, Religion News, Notre Dame ethics, aiandfaith.org, Catholic University policy, Commonweal, Biblica). Re-check in a browser before treating a note as confirmed or failed. |
| OI-003 | open | 2026-10-01 | https://chai-global.org/ (E-007) and https://www.kingdominnovations.us/ (E-008) returned no HTTP response. CHAI has a Google Sites page at https://sites.google.com/view/chai-global/ that says the site moved. New URL not captured. |
| OI-004 | open | 2026-10-01 | Magisterium.com URLs (A-014, A-016, A-017) returned HTTP 429. |
| OI-005 | open | 2026-10-01 | A-001 Antiqua et Nova URL returns 404 to curl and the document to a page fetch. Keep both results until a browser check. |
| OI-006 | open | 2026-10-01 | Fourteen rows have an ID prefix that differs from Cat (A-015, A-018, A-019, A-020, F-013, F-020–F-026, G-010, G-011). Left as in the 2026-09-10 register. Renumbering would violate the no-reuse rule. |
| OI-007 | open | 2026-10-01 | Many F and G notes cite only https://faith.tools/artificial-intelligence-ai. A dedicated product URL is still needed for each. |
| OI-008 | open | 2026-10-01 | F-027 Bible Vector Search cites the Faith Assistant app page. Confirm that is the right source. |
| OI-009 | open | 2026-10-01 | CHRISTIAN-AI-LANDSCAPE.md (formerly LANDSCAPE-STORY.md) says the register is local and "see local", and it states figures (Lilly grant, download counts, Zurich funding) that are not in DATABASE.md and were not re-verified. |
| OI-010 | open | 2026-10-01 | The source ledger stops at W-074 and does not include G-013, G-014, or F-029. The ledger is now the appendix of README.md. |
| OI-011 | rejected | 2026-10-01 | Requested filename DATABASE-WATCH.ms was saved as DATABASE-WATCH.md. Rejected: the repo uses .md, and that file was later merged into README.md. |
| OI-012 | open | 2026-10-02 | CHRISTIAN-AI-LANDSCAPE.md cites https://www.vatican.va/roman_curia/congregations/cfaith/documents/rc_con_cfaith_doc_20250128_antiqua-et-nova_en.html and that URL returned HTTP 404. The register uses the rc_ddf_doc path. |
| OI-013 | open | 2026-10-02 | Link check of the four live files on 2026-10-02: https://chai-global.org/ and https://www.kingdominnovations.us/ returned no HTTP response. Same hosts as OI-003. |
| OI-014 | open | 2026-10-02 | Link check of the four live files on 2026-10-02: https://www.vatican.va/roman_curia/congregations/cfaith/documents/rc_ddf_doc_20250128_antiqua-et-nova_en.html returned HTTP 404 to curl. Same URL as OI-005. A page fetch on 2026-10-01 returned the note. |

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
| 2026-10-01 | OI-009 | — | open | Carried from the unnumbered list. File name updated after the rename. |
| 2026-10-01 | OI-010 | — | open | Carried from the unnumbered list. |
| 2026-10-01 | OI-011 | open | rejected | .ms not used. Content now lives in README.md. |
| 2026-10-02 | OI-012 | — | open | Landscape example URL rc_con_cfaith_doc returned 404. |
| 2026-10-02 | OI-013 | — | open | Repeat of OI-003 hosts from the live-file link check. |
| 2026-10-02 | OI-014 | — | open | Repeat of OI-005 from the live-file link check. |
