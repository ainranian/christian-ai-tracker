# Verification report 2026-10-01

Scope: 135 register rows, 87 unique source URLs. HTTP HEAD with redirects, 15-second timeout, browser user-agent.

## Changes made

- Folded G-013, G-014, and F-029 into the register table. They had been separated by a blank line, so they rendered outside the table. IDs unchanged. Total remains 135.
- F-023 Doctrinally.AI source corrected from https://faith.tools/app/13774-agentic-jesus (Agentic Jesus page) to https://faith.tools/app/13826-doctrinally-ai. The faith.tools page describes a church assistant trained on that church's sermons and documents, with a site widget. https://faith.tools/app/13826-doctrinally-ai
- Split rules, categories, and history out of DATABASE.md into DATABASE-WATCH.md.
- Copied the SOURCE-WATCH.md method into DATABASE-WATCH.md. SOURCE-WATCH.md is now a pointer.

## URL check

- HTTP 200: 63
- HTTP 403 (bot or paywall; URL not treated as missing): 18
- HTTP 000 (no response): 2 — https://chai-global.org/ and https://www.kingdominnovations.us/
- HTTP 429: 2 — magisterium.com overview and infrastructure blog
- HTTP 202: 1 — https://www.luthscitech.org/from-despair-to-hope-princeton-center-explores-theology-in-light-of-ai-developments/
- HTTP 404 to this client: 1 — Antiqua et Nova URL. A page fetch of the same URL on 2026-10-01 returned the 28 January 2025 note. URL kept. https://www.vatican.va/roman_curia/congregations/cfaith/documents/rc_ddf_doc_20250128_antiqua-et-nova_en.html

## Claims checked against a page, not only a status code

- G-013 Equip: https://www.ministrybrands.com/ names Equip as an AI sermon-preparation and content-repurposing tool and states sermon content is not used to train AI models.
- G-014 Theo: https://www.einpresswire.com/article/939461650/experience-church-launches-theo-an-ai-assistant-built-to-answer-fast describes a website assistant that identifies itself as AI and hands crisis topics to a pastor.
- F-029: https://jointheos.io/ is Theos Scripture Intelligence, an AI Bible-study product, not the UK think tank Theos (B-016).
- B-020: https://aichristian.org/guidelines/ is titled AI Guidelines for Christian Ministry. The press release date on that page is 14 July 2026.
- E-007: https://chai-global.org/ did not resolve. https://sites.google.com/view/chai-global/ identifies CHAI as Christians in AI and says the site moved. The new domain was not stated in the fetched text, so the source cell was not changed.

## Not changed

No other Core AI note was rewritten. A 403 or a catalog URL is not evidence that the note is false. Rows whose only source is https://faith.tools/artificial-intelligence-ai were not individually re-read. That is recorded in OPENISSUES.md.
