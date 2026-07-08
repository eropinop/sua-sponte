---
name: pressure-test
description: Adversarial red-team of documents before filing - attack them the way opposing counsel and a skeptical judge would, then propose fixes and tactics. Use when the user says "pressure test", "attack my filing", "poke holes", "how will they respond", "stress test this", or "where am I weak".
---

# Pressure Test

Attack the filing packet the way a competent, motivated opposing counsel would - then switch sides and harden it. This runs after doc-review, on documents already believed clean.

## Process

1. Load `case-profile.md`, `judge-profile.md`, and every document in the filing packet.
2. Spawn the `opposing-counsel` agent with the packet, the case theory, and what is known about actual opposing counsel. Instruct it to produce its attack memo without pulling punches.
3. Independently run judge-lens review: given the judge profile, where would THIS judge push back? (Preferences, past rulings on similar motions, known pet peeves.)
4. Merge into `pressure-test-[date].md`:
   - **Attack surface map** - each argument/claim ranked by exposure: Kill shot / Serious damage / Chip damage / Noise
   - For each attack: the exact counterargument opposing counsel would make, the authority they would cite, and the probability it lands
   - **Procedural attacks**: standing, jurisdiction, timeliness, wrong vehicle, failure to meet prerequisites - these kill filings more often than merits do; check them first
   - **Evidentiary attacks**: which factual assertions lack admissible support; which exhibits can be excluded and on what objection
   - **Fixes**: for every Kill shot and Serious damage item, concrete language changes, additional authority to cite, evidence to add, or arguments to preemptively address in the draft
   - **Tactical options**: what to concede strategically, what to front-load, what to hold for reply
5. Summarize in chat: the 3 biggest vulnerabilities and whether the packet is fight-ready.

## Rules

- Honesty over comfort. A weakness found here costs a revision; found in court it costs the case.
- Rank realistically - do not inflate Noise into Kill shots to seem thorough.
- If a vulnerability cannot be fixed by drafting (a genuinely bad fact or missing element), say so and present options: reframe, concede-and-distinguish, or reconsider filing.
- Preemptively addressing a weak point in the brief is often stronger than hoping opposing counsel misses it - but not always; flag when silence is the better tactic.
