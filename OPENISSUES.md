# Open issues

Tracked for later implementation. Not a register.

- Full cell-by-cell fact audit of all 135 notes is unfinished. This run checked HTTP status for 87 URLs and page text for G-013, G-014, F-029, B-020, F-023, and E-007 only.
- Eighteen source URLs return HTTP 403 to a non-browser client (NYT, AP, Axios, ERLC, Lausanne, NCR, OSV, Religion News, Notre Dame ethics, aiandfaith.org, Catholic University policy, Commonweal, Biblica). Re-check in a browser before treating a note as confirmed or failed.
- https://chai-global.org/ (E-007) and https://www.kingdominnovations.us/ (E-008) returned no HTTP response. CHAI has a Google Sites page at https://sites.google.com/view/chai-global/ that says the site moved. New URL not captured.
- Magisterium.com URLs (A-014, A-016, A-017) returned HTTP 429.
- A-001 Antiqua et Nova URL returns 404 to curl and the document to a page fetch. Keep both results until a browser check.
- Fourteen rows have an ID prefix that differs from Cat (A-015, A-018, A-019, A-020, F-013, F-020–F-026, G-010, G-011). Left as in the 2026-09-10 register. Renumbering would violate the no-reuse rule.
- Many F and G notes cite only https://faith.tools/artificial-intelligence-ai. A dedicated product URL is still needed for each.
- F-027 Bible Vector Search cites the Faith Assistant app page. Confirm that is the right source.
- LANDSCAPE-STORY.md still says the register is local and “see local”, and it states figures (Lilly grant, download counts, Zurich funding) that are not in DATABASE.md and were not re-verified.
- SOURCES.md watches stop at W-074 and do not include G-013, G-014, or F-029.
- Requested filename DATABASE-WATCH.ms was saved as DATABASE-WATCH.md so it matches the rest of the repo.
