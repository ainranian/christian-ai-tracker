# Register process — stop dropping records

## Why 44+ session items were missing

The 10 Sep 2026 GitHub seed stored a **condensed** table (86 IDs). The session survey had named more initiatives. The condensation:

1. Merged distinct products into one row (example: A-015 bundled Credo Chat, Catholic AI, and Truthly).
2. Treated alliance members as already covered by the alliance (Theos, Youthscape, ECLAS, EEA sat only inside B-003).
3. Treated vendor stack products as already covered by the parent (Alexandria Hub and Vulgate sat only inside A-014 Magisterium).
4. Never wrote the long survey to a file before seeding GitHub, so there was no checklist to reconcile against.

That was a process error, not a finding that those projects were invalid.

## Rules for every future run

1. **One named thing = one ID.** Organisation, product, document, conference, journal, degree, or funded working group each get their own ID if they have a public name and a URL.
2. **Alliances do not absorb members.** B-003 AICP stays. Theos, Faraday, Youthscape, ECLAS, EEA also stay as their own rows.
3. **Platforms do not absorb products.** Gloo, Longbeard, SIL, FaithTech stay. Each shipped product under them gets its own ID.
4. **Do not delete or reuse IDs.** If two rows are the same project, mark one `alias-of: ID` in the note. Keep both rows until a source proves they are identical legal entities.
5. **Reconcile before finishing a run.** Count IDs. Diff this week’s name list against last week’s. Any name that disappears must be explained in the weekly report (merged-with-ID / closed / never-existed).
6. **New names from faith.tools, Missional AI, Vatican, Lausanne, AICP go in the same week they are seen**, even if the method card is `not disclosed`.
7. **Source watches.** New URL → new `W-nnn`. Shared URL is allowed; shared ID is not.

## Target size

There is no cap at 86 or 130. 130 was the session survey size, not a ceiling. Add every sourced name.
