# Journal Editing Context

## About this journal

This is a personal journal shared with a small group of close friends and family.
All readers know each other well and share common context. Entries do not need to
explain recurring people, places, or dogs.

## People readers know

- **Ben Voris** — the author. Refers to himself as "I" or "Ben".
- **Leslie Davidson** — Ben's wife of 30+ years. Occasionally hunts because she
  loves to see the dogs run. Manages home logistics during canoe and backpacking
  trips.
- **Royce Dunbar** — Ben's close friend since college (age 21). Primary canoe
  trip companion. Highly capable and organized outdoorsman.
- **Ian Dunbar** — Royce's oldest son, nearly 40. Has canoed with Ben and Royce
  since he was 8.
- **Harrison Dunbar** — Royce's younger son. Appears less often.
- **Jim Lovin** — Friend of Ben's. Not a hunter but knows the dogs well.

## Dogs readers know

- **Finnegan** — 6-year-old male English Pointer (often just "pointer"). History
  of seizures; Ben manages his workload carefully (hydration, snacks, jacket in
  cold/damp conditions, kept mostly under 15 miles/day).
- **Katie** — 10-year-old female Wirehaired Pointing Griffon (aka "griff").
  Slowing down but still covers ground enthusiastically. Breathtaking point.

## Hunting locations

All hunting locations are known to readers. No explanation needed for place names
like Danskin Lookout Road, Cornell Boise River WMA, Immigrant Road, etc.

## Canoe trip locations

Canoe trip locations (Quetico, BWCA, specific lakes and portages) may benefit
from brief context since not all readers paddle.

## Editing guidelines

### Voice and tone

- Ben writes in a spare, understated, first-person style.
- Sentence fragments are intentional and part of his voice — preserve them.
- Casual register throughout; do not formalize.
- If a full sentence would improve flow or readability, suggest it — but flag it
  as a suggestion rather than silently changing it.
- Primary organizer is chronological (time/events in sequence).

### What to check

- Flow and organization — the main concern
- Coherence — does each entry follow naturally from the last?
- Readability — would a non-specialist reader follow this?
- Grammar and syntax — fix errors, but preserve intentional fragments and
  informal constructions
- Context — flag any reference that readers might not understand

### What not to change

- GPS coordinates, elevations, and timestamps — never alter these
- Dog mileage and ascent figures — never alter these
- Image links and alt text — never alter these
- Location names — never alter these

## Image links

Image links follow this format:

    ![alt text](Attachments/YYYY-MM-DD-HH-MM-SS.jpeg "alt text")

The alt text in square brackets and the quoted title must always be identical.
If you see a link where they differ, flag it.

Map screenshots follow the same format but filenames contain `_map`.

## Document structure

### Summary (top of file, before any headings)

- A few paragraphs of polished prose summarizing the trip or season.
- Written in Ben's voice.
- This is what most readers read first (and sometimes only).
- Should stand alone without requiring the reader to read the detail entries.

### Index (after summary, before daily entries)

- A `## Index` heading, then a numbered list with one entry per day.
- Each entry is date, location, and a short hook about what happened that day:

      1. [2025-10-11 Danskin Lookout Road &ndash; first hunt, a point and a miss](#day-1--2025-10-11-danskin-lookout-road)

- Hooks are drafted one day at a time, from that day's entries only, and Ben
  approves each one. Keep them short enough for a phone. Credit the dogs
  fairly; don't blame a dog for something the notes don't say it did. Ben's
  shooting stays out of hooks unless he asks.
- End the index, and every day, with a back-link: `[index ↑](#index)`

### Daily entries

- Top-level heading (`##`) starts with the day number so that it begins with a
  letter (see "Anchor links" below):
  - Hunting: `## Day N &ndash; YYYY-MM-DD Location Name`
  - Canoe/backpack: `## Day N &ndash; YYYY-MM-DD Origin to Destination`
- Day N counts days out, not only days hunted (e.g. a day training a friend's
  puppy counts).
- One `##` per date. If the day moved locations, name both
  (`Danskin camp to Long Tom Reservoir Road`) and put each location in its
  `###` sub-entry's location note.
- The day's starting timestamp, coordinates, and elevation go on a plain line
  under the heading, with no escapes:

      2025-10-11T15:46-06:00 (43.37613, -115.71122) 4746 feet

  If the time is unknown, leave it out (`2025-12-11 (43.27090, -115.66930) 3933
  feet`). Never invent one.
- Sub-entries within a day use `###` with full ISO timestamp, coordinates,
  elevation, and optional location note. A colon in a heading triggers a
  markdownlint warning, so escape each one:
  `### 2025-11-08T12\:52-07\:00 (43.28391, -115.53843) 5018 feet\: Long Tom Reservoir Road`
- Remove seconds from timestamps: `15\:46\:22` → `15\:46`.
- Horizontal rule (`---`) separates days.
- **No `<details>` or `<summary>` HTML tags.** With the summary on top and an
  index, readers who want the overview stop reading; readers who want a day
  jump to it; readers who want the whole season just scroll.

### Anchor links

Readers use the GitHub Pages site, not github.com. Pages builds heading IDs by
dropping everything before the first letter, lowercasing, removing punctuation,
and turning spaces into hyphens. A heading that starts with a date or time gets
an ID that github.com doesn't, and links break. Starting every `##` with
`Day N` gives the same ID on both:

    ## Day 1 &ndash; 2025-10-11 Danskin Lookout Road  →  #day-1--2025-10-11-danskin-lookout-road

After publishing, check that every index link matches an `id` on the live page.

### Punctuation

- Prose: closed em dash, written as an entity: `eye&mdash;seemingly`.
- Index entries and headings: spaced en dash: ` &ndash; `.
- Contractions are the default; this is casual writing.

### End-of-day summary

- A short paragraph after the final "Truck" entry (hunting) or "Tent" entry
  (canoe/backpack).
- Written in Ben's voice.
- Captures the feel of the day, not just the facts.

## Generating summaries

When asked to draft a summary (top-of-file or end-of-day):

- Read all entries for the relevant scope first.
- Write in Ben's voice: spare, understated, first-person.
- Do not invent details not present in the notes.
- Flag anything you are uncertain about rather than guessing.
- Present the draft and ask Ben to review before finalizing.

## Working with Claude

- When proposing a change for a specific day, open the file there in the
  current VS Code window (`code -r -g README.md:<line>`) and include a
  clickable `README.md:<line>` link.
- Make one edit at a time and wait for it to finish. Parallel edits stack up
  review diffs in VS Code and are hard to follow.
- Commit locally after each approved change (squash later if wanted). Don't
  push without asking; pushing republishes the site.
- Ben may lock README.md with "Set Active Editor Read-only in Session" to avoid
  accidental typing. Claude's edits still go through.
