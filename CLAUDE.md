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

- A numbered markdown list of anchor links to each day's heading.
- Example:
      1. 2025-08-06 — [Bottle Portage on Lac la Croix...](#2025-08-06-day-1-...)

### Daily entries

- Top-level heading (`##`) with date, optional day number, and destination.
  - Canoe/backpack: `## YYYY-MM-DD Day N: Origin to Destination`
  - Hunting: `## YYYY-MM-DDThh:mm±hh:mm (lat, lon) elevation feet: Location Name`
- The colon (`:`) in these triggers a warning from Markdownlink so each `:` must be escaped. Example
  1. `## 2025-10-11T15\:46-06\:00 (43.37613, -115.71122) 4746 feet\: Danskin Lookout Road`
- Timestamps often contain a second which should be removed. Example
  1. `2025-10-11T15\:46\:22-06\:00` to `2025-10-11T15\:46-06\:00`
- Sub-entries within a day use `###` with full ISO timestamp, coordinates,
  elevation, and optional location note. Remove the seconds.
- Horizontal rule (`---`) separates days.
- **No `<details>` or `<summary>` HTML tags.**

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