---
name: evidence-exhibits
description: Review, compile, and organize evidence and exhibits - map evidence to claim elements, find gaps, build exhibit lists with proper labeling and authentication plans. Use when the user says "organize my evidence", "build my exhibit list", "what evidence do I need", "compile exhibits", or "is this enough proof".
---

# Evidence & Exhibits

Turn a pile of documents into an exhibit packet mapped to the legal elements it must prove - and expose what is missing while there is still time to get it.

## Process

1. Load `case-profile.md` case theory and elements. If elements are not recorded, derive them from the pleadings and confirm with the user.
2. Inventory: read every evidence file in the folder the user points to (use subagents to parallelize large sets). For each item capture: what it is, date, author/source, which element(s) it supports, strength (direct/circumstantial/corroborating), and admissibility risk (hearsay, authentication, relevance, best evidence).
3. Build the **element-to-evidence map**: for each element of each claim or defense, list supporting exhibits ranked by strength. Any element with zero or weak-only support is a gap - flag in red.
4. **Gap analysis + suggestions**: for each gap, suggest concrete evidence that would fill it and how a pro se litigant can get it (discovery request, subpoena, public record, declaration from a witness, business records affidavit, certified copies).
5. Build the **exhibit list** for the filing at hand:
   - Label per local convention from `case-profile.md` (numbers vs letters, party prefixes)
   - Order for persuasion within the rules - usually chronological or element-grouped
   - For each exhibit: description for the index, the authentication plan (who/what establishes it is what it purports to be), and anticipated objection + response
   - Note anything requiring a declaration to introduce, and draft those declarations on request
6. Cross-check against draft documents: every exhibit cited in a brief exists in the list; every listed exhibit is actually referenced or consciously included; numbering matches everywhere.
7. Output `exhibit-workbook-[date].md` (map, gaps, list, objection table) and offer an xlsx version for tracking.

## Rules

- Never invent or embellish evidence descriptions - describe only what the document actually shows.
- Duplicative exhibits dilute; recommend the strongest single item per point and park the rest as backup.
- Highlight anything that cuts against the case theory too - the user must know before opposing counsel uses it.
- Redaction check: flag SSNs, minors' names, account numbers, and anything sealed or confidential before it goes in a public filing.
