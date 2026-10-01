# CHRISTIAN-AI-LANDSCAPE

Updated 2026-10-02 from the copy in archive/2026-10-02/CHRISTIAN-AI-LANDSCAPE.md. Counts match DATABASE.md (135 rows). Each category's analysis now follows that category's description.

# The Christian AI Landscape: A Ten-Minute Story

**Source:** ainranian/christian-ai-tracker — 135 initiatives in DATABASE.md. Categories: Holy See / Catholic magisterial and university (17), Protestant / evangelical / ecumenical research (24), Digital theology centres, journals, working groups (20), Bible translation and missions engineering (13), Faith-tech platforms, incubators, networks (14), Consumer Bible / prayer / companion apps (27), Church operations and sermon tools (20).
**Purpose:** A spoken narrative for explaining the landscape in about ten minutes. Companion to DATABASE.md (the register). This file is the story; the register is the table.
**Status:** Draft. Not verified against every row. The source ledger in the README appendix is archival and stops at W-074.

---

## The frame

The landscape splits into two halves: **institutions that think about AI**, and **products that use it**. The institutions are mostly Catholic and Protestant research bodies, universities, and networks. The products are overwhelmingly consumer apps and church tools.

The single most important technical finding across all 135 initiatives: almost nobody has published how their models are actually trained. The one exception is Bible translation — SIL's Scripture Forge, Serval, and Slingshot are the only initiatives with real fine-tuning documentation. Everything else is RAG, prompt constraints, or undisclosed wrappers on commercial models. That is the honest baseline.

---

## Holy See / Catholic magisterial and university

The Vatican leads the institutional world. Antiqua et Nova (2025 doctrinal note) and Magnifica Humanitas (Leo XIV's 2026 encyclical calling for AI to be "disarmed") set the tone. The Rome Call for AI Ethics offers six principles, and Paolo Benanti at the Gregorian University advises the Vatican, Italy, and the UN. Notre Dame's DELTA Network is in the register (A-008). A Lilly grant figure is not in DATABASE.md and is not restated here.

**Example:** https://www.vatican.va/roman_curia/congregations/cfaith/documents/rc_ddf_doc_20250128_antiqua-et-nova_en.html

**Theological concern:** magisterial authority is real, but it can become a substitute for personal engagement with Scripture — and the Vatican's framework is natural-law based, not explicitly biblical.

### Analysis

Antiqua et Nova and Magnifica Humanitas are sophisticated — real doctrinal work, real institutional weight. But the framework is natural law, not Scripture. When the church's AI ethics rest on reason rather than revelation, the Bible becomes optional. The Vatican's "disarm AI" language can slide into control rather than discernment.

---

## Protestant / evangelical / ecumenical research

The ERLC's 2019 statement grounds AI in the imago Dei. The Gospel Coalition built an AI Christian Benchmark. The AI Christian Partnership in the UK unites Theos, Faraday, Youthscape, and ECLAS. Oxford's OCTAI and the Faraday Institute study dignity and agency. The Lausanne Movement published a November 2025 global analysis.

**Example:** https://erlc.com/policy-content/artificial-intelligence-an-evangelical-statement-of-principles/

**Theological concern:** evangelical statements are often reactive — responding to Catholic documents rather than building their own positive vision — and the benchmark work is still early.

### Analysis

Less sophisticated but more biblically grounded. The ERLC's imago Dei framing is the strongest theological anchor in the landscape — humans as image-bearers, tools as servants. The weakness: it is reactive. Most evangelical statements exist because the Vatican moved first. The Lausanne dossier and the WEA's TRUST framework are better — they build positive vision, not just red lines.

---

## Digital theology centres, journals, working groups

Calvin University's Derek Schuurman hosts a Wisdom in the Age of AI conference (October 2026). Durham's CODEC is the foundational UK digital theology center. Zurich has a Church and AI 2026 call (C-010). A franc figure is not in DATABASE.md and is not restated here. Shaw University is planning the first doctoral degree in AI and moral agency.

**Example:** https://calvin.edu (search: Wisdom in the Age of AI)

**Theological concern:** academic theology can become descriptive rather than confessional — studying AI's effect on religion without asking whether the technology itself serves the gospel.

### Analysis

The most sophisticated category technically, but the most theologically diffuse. Zurich's Church and AI work describes AI's effect on religion rather than asking whether AI serves Christ. The exception is Calvin's Schuurman — Reformed, confessional, building from the inside. Shaw's doctoral track in AI and moral agency is the boldest institutional move, but it is still a proposal.

---

## Bible translation and missions engineering

This is the most technically sophisticated and most aligned category. SIL's tools draft Scripture for minority languages, with human review built in. Biblica, Avodah Connect, and Frontier Ventures extend this.

**Example:** https://www.sil.org (search: Scripture Forge)

**Theological concern:** AI can accelerate translation, but it can also flatten the cultural particularity that makes Scripture land in a language — and the human review step is where the real theological work happens.

### Analysis

The gold standard. SIL's Scripture Forge, Serval, and Slingshot are the only initiatives with published fine-tuning methodology — real LoRA work on real language data. Theologically the most aligned category because it treats AI as a tool under human authority, with review built in. The concern is subtle: AI can flatten the cultural particularity that makes Scripture land. A translation that reads smoothly everywhere may lose the roughness that makes it true somewhere.

---

## Faith-tech platforms, incubators, networks

Gloo is the biggest player, with a judge-LLM benchmark called FAI-C. FaithTech, Missional Labs, and CHAI Global build community. The Missional AI Global Summit drew about 650 attendees in Silicon Valley. CHAI's former host, chai-global.org, returned no HTTP response on 2026-10-02; the Google Sites page says the site moved and does not give the new domain.

**Example:** https://gloo.com

**Theological concern:** platform power concentrates in a few hands, and Gloo's "flourishing" metric is commercial as much as theological.

### Analysis

The most commercially sophisticated and the most theologically ambiguous. Gloo's FAI-C benchmark is real engineering — a judge-LLM scoring other models on flourishing metrics. But "flourishing" is a commercial metric as much as a theological one. When a platform defines what Christian flourishing looks like, it defines the church's vocabulary.

---

## Consumer Bible / prayer / companion apps

Bible Chat, Pray.com, and Hallow are in the register (F-001, F-002, F-003). Download counts are not in DATABASE.md and are not restated here. Text With Jesus does biblical-figure roleplay. Just Like Me sells a paid video Jesus. A Cambridge study found chatbot bias in Bible apps.

**Example:** https://biblechat.ai

**Theological concern:** this is where idolatry risk is highest — a chatbot can become a substitute for prayer, community, and the Holy Spirit. Nearly all are "unverified-method": you cannot check what they are trained on.

### Analysis

The least sophisticated technically — almost all unverified-method, meaning nobody knows what is in the training data — and the highest risk theologically. Bible Chat and Pray.com are large consumer apps in the register. Download counts are not in DATABASE.md. Text With Jesus and Just Like Me cross a line: they do not serve prayer, they replace it. A chatbot Jesus cannot suffer, cannot die, cannot rise — and that is the whole gospel.

---

## Church operations and sermon tools

Logos Bible Software grounds AI in your library. Sermon AI and Pulpit AI multiply content. Pastors.ai adds live translation. Justin Lester built a digital twin of himself as a pastor. Helsinki's St. Paul's experimented with ChatGPT, Suno, and Synthesia for liturgy.

**Example:** https://www.logos.com

**Theological concern:** sermon multiplication can become content farming — volume over depth — and a pastor's digital twin raises questions about whether preaching is a person or a product.

### Analysis

Sit in the middle. Logos is the most grounded — it works from your library, your texts, your tradition. Sermon AI and Pulpit AI are content multipliers, fine for volume but dangerous for depth. Justin Lester's digital twin is the sharpest edge: a pastor's voice, corpus, and presence, without the pastor. The Helsinki experiment is the most honest about what it is doing, which makes it the most useful case study.

---

## The through-line

Three concerns recur everywhere:

1. **Authority** — who trains the model, on what data, with what review.
2. **Embodiment** — AI has no body, no incarnation, no suffering, and Christianity is built on all three.
3. **The Holy Spirit** — no chatbot has him, and no system can substitute for him.

The most aligned work treats AI as a servant. The least aligned treats it as a savior. The most aligned category is translation, where AI serves human review. The least aligned is consumer roleplay, where AI replaces human relationship.

---

## Logos deep-dive (from conversation, 2026-10-01)

This sits with church operations (G-001). It is kept here because it is longer than the category analysis.

Logos does not train its own model. It uses off-the-shelf models from OpenAI, Google, Microsoft, and Anthropic, picking whichever fits each task: speed, accuracy, creativity, or theological precision.

- **Smart Search / Smart Synopsis:** the model receives only your library's top results — the answer is a synthesis of your own books with citations, not the model's general knowledge. Newer versions highlight which sentences came from which source; hovering shows the original text.
- **Creative tasks** (sermon illustrations): crafted prompts rather than data restriction, since restricting output to curated data would kill creativity.
- Logos explicitly does not fine-tune, and claims your library, notes, and searches are never saved or reused to train models for other users.
- **Thompson Chain Reference:** the AI does not read Thompson's cross-reference chains as a system. Cross-references are a separate Logos feature (search a verse with the crossRef field); Smart Bible Search finds related verses through its own trained data, not through Thompson's numbering.
- Logos never discloses which specific model handled a given query. Citations are fully auditable; the model behind them is not.

**Bias assessment (user's framing, endorsed):** if Gemini is more biased than Grok on biblical, Christian, philosophical, psychological, or sociological questions, that bias bleeds into the connective language of a synopsis even when the underlying Bible text and citations are correct — and the user would not know, because there is no per-query model tracking. The synopsis is constrained to the user's top five results (limiting hallucination) but that constraint does not eliminate framing bias: a model can still choose which sources to emphasize, which sentences to quote, and how to connect them.

**Practical mitigations:** treat the synopsis as a starting point, not a finished product; read the cited sources directly; run the same query in Precise mode (no AI) and compare.

---

## Open questions

- DATABASE.md on main is the register (135 rows, with a Concerns column drawn from OPENISSUES.md).
- Decide whether CHRISTIAN-AI-LANDSCAPE.md should be updated by the Sunday automation or maintained manually.
- Visualization layer (maps, matrices) discussed but not started.
- Cell-by-cell page checks are still open (OI-001). This narrative is not that audit.
