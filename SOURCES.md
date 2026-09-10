# Source watches

Option 1 ledger: one row per unique cited URL. Multiple project IDs may share a URL.

- Baseline check: 2026-09-10 18:10 SAST
- Hash: SHA-256 of stripped visible text (first 80k chars), truncated to 16 hex. For non-HTML, SHA-256 of first 400k bytes.
- `etag` / `last_modified` taken from HTTP response when present (RFC 7232 / RFC 9110).
- `fetch`: `live` = HTTP 2xx/3xx; `blocked` = 401/403; `missing` = 404; `fail` = timeout or other error.
- Blocked/fail hashes are the error-body hash, not the article. Re-check those with a browser tool next run.
- Do not overwrite prior rows. On change, set `last_changed`, keep previous hash in the weekly report, append a history line on each listed project ID.

| Watch | Project IDs | Fetch | HTTP | Hash | ETag | Last-Modified | Last checked | Last changed | URL |
|---|---|---|---|---|---|---|---|---|---|
| W-001 | A-001 | live | 200 | `e8221471161ca729` | — | — | 2026-09-10 | 2026-09-10 | https://www.vatican.va/roman_curia/congregations/cfaith/documents/rc_ddf_doc_20250128_antiqua-et-nova_en.html |
| W-002 | A-002 | live | 200 | `97a05dfa7dbe746e` | — | — | 2026-09-10 | 2026-09-10 | http://www.vatican.va/content/leo-xiv/en/speeches/2026/may/documents/20260525-presentazione-enciclica.html |
| W-003 | A-003 | live | 200 | `1d5c05a324ffcbdf` | — | — | 2026-09-10 | 2026-09-10 | https://www.romecall.org/the-call/ |
| W-004 | A-004 | live | 200 | `7657b4df7062eb85` | — | — | 2026-09-10 | 2026-09-10 | https://www.romecall.org/renaissance-foundation/ |
| W-005 | A-005 | live | 200 | `887b68a09771bb1c` | — | Tue, 01 Sep 2026 01:54:33 GMT | 2026-09-10 | 2026-09-10 | https://www.vaticannews.va/en/pope/news/2023-03/pope-francis-minerva-dialogues-technology-artificial-intelligenc.html |
| W-006 | A-006 | blocked | 403 | `26ffb5aeac08e19c` | — | — | 2026-09-10 | 2026-09-10 | https://nytimes.com/2024/02/09/world/europe/italy-artificial-intelligence-ethics.html |
| W-007 | A-007,B-006,C-006 | blocked | 403 | `ae0b26c68939e821` | — | — | 2026-09-10 | 2026-09-10 | https://aiandfaith.org/research/ |
| W-008 | A-008 | live | 200 | `63dde940f9b65b1f` | — | — | 2026-09-10 | 2026-09-10 | https://ethics.nd.edu/programs/delta/ |
| W-009 | A-009 | live | 200 | `0e0af670cbf9d0d2` | — | — | 2026-09-10 | 2026-09-10 | https://leonum.catholic.edu/ |
| W-010 | A-010 | blocked | 403 | `ae0b26c68939e821` | — | — | 2026-09-10 | 2026-09-10 | https://policies.catholic.edu/ai/index.html |
| W-011 | A-011 | live | 200 | `285e9b8dadc4fee5` | — | — | 2026-09-10 | 2026-09-10 | https://www.georgetown.edu/artificial-intelligence/ |
| W-012 | A-012 | blocked | 403 | `ae0b26c68939e821` | — | — | 2026-09-10 | 2026-09-10 | https://www.ncronline.org/news/catholic-colleges-and-universities-jumping-quick-moving-ai-field |
| W-013 | A-013 | blocked | 403 | `ae0b26c68939e821` | — | — | 2026-09-10 | 2026-09-10 | https://www.oursundayvisitor.com/new-catholic-university-embraces-relationship-of-faith-and-science/ |
| W-014 | A-014 | fail | 429 | `8999c4d69c170b82` | — | — | 2026-09-10 | 2026-09-10 | https://www.magisterium.com/overview |
| W-015 | A-015 | live | 200 | `968f86326e3e18b3` | — | Thu, 20 Aug 2026 23:15:38 GMT | 2026-09-10 | 2026-09-10 | https://www.catholicmom.com/articles/ai-for-catholics-six-apps-you-should-know-about |
| W-016 | B-001 | blocked | 403 | `b1b51a7af28c84f2` | — | — | 2026-09-10 | 2026-09-10 | https://erlc.com/policy-content/artificial-intelligence-an-evangelical-statement-of-principles/ |
| W-017 | B-002 | live | 200 | `e8b49c66e99229d1` | — | Thu, 18 Dec 2025 13:39:18 GMT | 2026-09-10 | 2026-09-10 | https://www.thegospelcoalition.org/ai-christian-benchmark/ |
| W-018 | B-003 | live | 200 | `ab1560fe2de14719` | — | — | 2026-09-10 | 2026-09-10 | https://aichristian.org/ |
| W-019 | B-004 | live | 200 | `c5ea51e5e9f5d17c` | — | — | 2026-09-10 | 2026-09-10 | https://www.faraday.cam.ac.uk/research/project/ai-for-humanity-a-research-hub/?rtn=https:/www.faraday.cam.ac.uk/research/research-hubs/ |
| W-020 | B-005 | live | 200 | `6981b06676289ded` | 1789052188-0 | Thu, 10 Sep 2026 14:56:28 GMT | 2026-09-10 | 2026-09-10 | https://www.theology.ox.ac.uk/article/launch-oxford-collaboration-theology-and-artificial-intelligence-octai |
| W-021 | B-007 | blocked | 403 | `ae0b26c68939e821` | — | — | 2026-09-10 | 2026-09-10 | https://aiandfaith.org/events/world-evangelical-alliance-review/ |
| W-022 | B-008 | blocked | 403 | `ae0b26c68939e821` | — | — | 2026-09-10 | 2026-09-10 | https://lausanne.org/global-analysis/november-2025-issue-overview |
| W-023 | B-009 | live | 200 | `b4528b59c5e7195c` | — | Thu, 10 Sep 2026 16:11:51 GMT | 2026-09-10 | 2026-09-10 | https://futureoflife.org/grant-program/rfp-on-religious-projects/ |
| W-024 | B-010 | blocked | 403 | `ae0b26c68939e821` | — | — | 2026-09-10 | 2026-09-10 | https://lausanne.org/global-analysis/ai-ethical-framework |
| W-025 | B-011 | live | 200 | `f89d47f9cfe27b4a` | — | — | 2026-09-10 | 2026-09-10 | https://pcusa.org/news-storytelling/news/2025/9/2/charting-faithful-future-artificial-intelligence |
| W-026 | B-012 | blocked | 403 | `ae0b26c68939e821` | — | — | 2026-09-10 | 2026-09-10 | https://www.axios.com/2025/11/12/christian-ai-chatbot-jesus-god-satan-churches |
| W-027 | B-013,B-014,C-004 | live | 200 | `9c48d940871c2eba` | — | — | 2026-09-10 | 2026-09-10 | https://pcusa.org/news-storytelling/news/2025/7/17/pcusas-office-innovation-co-organizing-summit-ai-and-church |
| W-028 | B-015 | live | 200 | `f02a5613daf776e4` | — | — | 2026-09-10 | 2026-09-10 | https://newsroom.churchofjesuschrist.org/article/faith--ethics--and-human-dignity-in-an-age-of-artificial-intelligence--a-call-to-action |
| W-029 | C-001 | live | 200 | `ef7d7489189f133a` | W/"1789056715" | Thu, 10 Sep 2026 16:11:55 GMT | 2026-09-10 | 2026-09-10 | https://calvin.edu/people/derek-schuurman |
| W-030 | C-002 | live | 200 | `41fbd0183d13a9fc` | W/"1789055994" | Thu, 10 Sep 2026 15:59:54 GMT | 2026-09-10 | 2026-09-10 | https://calvin.edu/node/38452 |
| W-031 | C-003 | blocked | 403 | `ae0b26c68939e821` | — | — | 2026-09-10 | 2026-09-10 | https://religionnews.com/2026/07/27/this-historic-divinity-school-is-offering-the-first-doctoral-degree-in-ai-and-moral-agency/ |
| W-032 | C-005 | live | 202 | `e3b0c44298fc1c14` | — | — | 2026-09-10 | 2026-09-10 | https://www.luthscitech.org/from-despair-to-hope-princeton-center-explores-theology-in-light-of-ai-developments/ |
| W-033 | C-007 | live | 200 | `1dce978419f06dc2` | — | Sun, 06 Sep 2026 17:49:55 GMT | 2026-09-10 | 2026-09-10 | https://ccg.fas.harvard.edu/conference-pages/christianity-and-ai |
| W-034 | C-008 | live | 200 | `5db3b33a3e96c40e` | — | Thu, 10 Sep 2026 16:13:31 GMT | 2026-09-10 | 2026-09-10 | https://digitaltheology.jp/ |
| W-035 | C-009,C-011 | live | 200 | `7471b1384d225dfb` | — | — | 2026-09-10 | 2026-09-10 | https://www.oikoumene.org/news/new-handbook-launched-to-explore-digital-theology-in-faith-and-practice |
| W-036 | C-010 | live | 200 | `a7e56e692265651d` | — | Wed, 17 Sep 2025 12:04:34 GMT | 2026-09-10 | 2026-09-10 | http://www.theologie.uzh.ch/dam/jcr:e271df79-d549-4b96-9485-9be02d249a27/Church%20and%20AI%20-Zurich%202026_Call%20for%20Papers_Schlag_Oorschot.pdf |
| W-037 | C-012 | live | 200 | `88133f55c0e83d63` | — | — | 2026-09-10 | 2026-09-10 | https://www.uni-bremen.de/en/hospo/news/details/religious-agency-in-the-digital-age |
| W-038 | C-013 | live | 200 | `c3a059f53d3cf83a` | — | — | 2026-09-10 | 2026-09-10 | https://nethki.digital/ |
| W-039 | C-014 | live | 200 | `1e693d053c7be74d` | W/ee1f8a7d1a5de448 | — | 2026-09-10 | 2026-09-10 | https://jmt.scholasticahq.com/issue/4236 |
| W-040 | C-015 | live | 200 | `be6922aa25a767d5` | 6a9d6d7d-5146 | Sun, 06 Sep 2026 13:41:17 GMT | 2026-09-10 | 2026-09-10 | https://icmi-proceedings.com/ |
| W-041 | C-016 | live | 200 | `731862b171ed1f8e` | — | — | 2026-09-10 | 2026-09-10 | https://cefe.ai/ |
| W-042 | C-017,F-004 | live | 200 | `c1a110d66a44f656` | — | Fri, 21 Aug 2026 00:00:00 GMT | 2026-09-10 | 2026-09-10 | https://faith.tools/app/533-bible-chat |
| W-043 | D-001,D-002 | live | 200 | `cd02720c31c8abcd` | — | Thu, 20 Aug 2026 00:00:00 GMT | 2026-09-10 | 2026-09-10 | https://faith.tools/app/837-scripture-forge |
| W-044 | D-003,D-005 | live | 200 | `84874c04baf35d6b` | — | — | 2026-09-10 | 2026-09-10 | https://wycliffe.net/2025/05/20/thats-what-good-tools-do/ |
| W-045 | D-004 | live | 200 | `f7dcf730e47c0d97` | — | — | 2026-09-10 | 2026-09-10 | https://www.youtube.com/watch?v=-kRwZwBuKLk |
| W-046 | D-006 | blocked | 403 | `30b5101c66ebc689` | — | — | 2026-09-10 | 2026-09-10 | https://www.biblica.com/articles/redemptive-ai-using-technology-to-serve-the-kingdom/ |
| W-047 | D-007 | live | 200 | `7bb25139065fdcc1` | — | Thu, 10 Sep 2026 16:13:39 GMT | 2026-09-10 | 2026-09-10 | https://ministrywatch.com/how-artificial-intelligence-is-transforming-bible-translation/ |
| W-048 | D-008 | live | 200 | `d15bce7dd62ca60a` | 38pjn7z62w57i3 | — | 2026-09-10 | 2026-09-10 | https://www.air1.com/faith/news/positive-people/come-and-see-foundation-using-cutting-edge-translation-tech-to-bring-biblical-stories-to-the-ends-of-the-earth-and-podcast-58431 |
| W-049 | D-009 | live | 200 | `ac841916a7ce7042` | — | — | 2026-09-10 | 2026-09-10 | https://connect.frontierventures.org/mission-frontiers/church-centric-innovation-for-finishing-the-task |
| W-050 | D-010 | live | 200 | `5b12033070d731e2` | — | — | 2026-09-10 | 2026-09-10 | https://transformiran.com/our-work/kairos/ |
| W-051 | E-001 | live | 200 | `17e3a426a758fea9` | 34d6fa4312f4a136 | Wed, 09 Sep 2026 20:23:07 GMT | 2026-09-10 | 2026-09-10 | https://gloo.com/flourishing-hub/research |
| W-052 | E-002 | live | 200 | `f1b2e977dcc8fef6` | pcl4yspbd46a3b | — | 2026-09-10 | 2026-09-10 | https://docs.gloo.com/learn-more/benchmarking |
| W-053 | E-003 | live | 200 | `7c7a152a2a5c02d0` | — | Fri, 21 Aug 2026 00:00:00 GMT | 2026-09-10 | 2026-09-10 | https://faith.tools/app/816-faith-assistant |
| W-054 | E-004 | live | 200 | `2efd74be5d7c3f8b` | — | Thu, 10 Sep 2026 14:20:49 GMT | 2026-09-10 | 2026-09-10 | https://faithtech.com/ |
| W-055 | E-005 | live | 200 | `0e4fefd29017c916` | — | Thu, 27 Aug 2026 22:21:46 GMT | 2026-09-10 | 2026-09-10 | https://missional.ai |
| W-056 | E-006 | live | 200 | `2eb3d8e38f111371` | cabfa964f088093f | Wed, 09 Sep 2026 23:03:11 GMT | 2026-09-10 | 2026-09-10 | https://gloo.com/resources/blog/building-for-human-flourishing |
| W-057 | E-007 | fail | err | `empty` | — | — | 2026-09-10 | 2026-09-10 | https://chai-global.org/ |
| W-058 | E-008 | fail | err | `empty` | — | — | 2026-09-10 | 2026-09-10 | https://www.kingdominnovations.us/ |
| W-059 | E-009 | live | 200 | `2832053bbf9644f8` | 7b7d3c63e7ac6695 | — | 2026-09-10 | 2026-09-10 | https://www.poulterventures.com/ |
| W-060 | E-010 | live | 200 | `83055151f7cab9e4` | — | — | 2026-09-10 | 2026-09-10 | https://jlgarrettgroup.ai/ai-scholars |
| W-061 | F-001,F-002,F-003 | blocked | 403 | `26ffb5aeac08e19c` | — | — | 2026-09-10 | 2026-09-10 | https://www.nytimes.com/2025/09/14/us/chatbot-god.html |
| W-062 | F-005 | live | 200 | `ec401bdb8759c234` | — | Tue, 25 Aug 2026 00:00:00 GMT | 2026-09-10 | 2026-09-10 | https://faith.tools/app/26-bible-ai |
| W-063 | F-006 | live | 200 | `84adedb422324b26` | — | — | 2026-09-10 | 2026-09-10 | https://textwith.me/en/jesus/ |
| W-064 | F-007 | blocked | 403 | `ae0b26c68939e821` | — | — | 2026-09-10 | 2026-09-10 | https://apnews.com/article/religious-chatbots-ai-technology-jesus-buddhabot-e1ed4832b25a23ee85292da681a0ec37 |
| W-065 | F-008 | live | 200 | `e787e03b93d94095` | SaE36s2iLfhz1y9Z | — | 2026-09-10 | 2026-09-10 | https://apps.apple.com/us/app/faithgpt-christian-ai/id6755321573 |
| W-066 | F-009,F-010 | live | 200 | `e64e430db5cc6772` | — | — | 2026-09-10 | 2026-09-10 | https://faith.tools/apologetics |
| W-067 | F-011 | live | 200 | `308734842789d429` | — | Fri, 05 Jun 2026 22:18:21 GMT | 2026-09-10 | 2026-09-10 | https://www.jubileeintelligence.com/ |
| W-068 | F-012 | live | 200 | `51e448cb72e2ca95` | — | — | 2026-09-10 | 2026-09-10 | https://www.outlookmag.org/pastor-wintley-phipps-introduces-gospeltruth-ai/ |
| W-069 | G-001,G-003 | live | 200 | `83344aac2ab789af` | — | — | 2026-09-10 | 2026-09-10 | https://aligned.church/blog/best-ai-for-churches-comparison-2026 |
| W-070 | G-002 | live | 200 | `1a451f67c4bd00e8` | — | — | 2026-09-10 | 2026-09-10 | https://aligned.church/blog/best-ai-sermon-writer-comparison-2026 |
| W-071 | G-004 | live | 200 | `0b0a1608066ff07e` | — | Fri, 14 Aug 2026 00:00:00 GMT | 2026-09-10 | 2026-09-10 | https://faith.tools/app/408-pastors-ai |
| W-072 | G-005 | live | 200 | `36efb7c1ef0b61ae` | d02390aa2a11d960 | — | 2026-09-10 | 2026-09-10 | https://sermon-clips.com/blog/best-ai-tools-for-pastors |
| W-073 | G-006 | blocked | 403 | `26ffb5aeac08e19c` | — | — | 2026-09-10 | 2026-09-10 | https://www.nytimes.com/2026/07/30/us/ai-twin-pastor-justin-lester-california-church.html |
| W-074 | G-007 | blocked | 403 | `ae0b26c68939e821` | — | — | 2026-09-10 | 2026-09-10 | https://apnews.com/article/finland-lutheran-church-artificial-intelligence-64135cc5e58578a89dcbaf0c227d9e3e |
