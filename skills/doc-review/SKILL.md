---
name: doc-review
description: Deep multi-pass review of a legal document draft - citation accuracy, legal sufficiency, tone and professionalism, formatting compliance, completeness, and stylistic tells. Use when the user says "review this motion", "check my brief", "review my filing", "is this ready", "tone check", or shares a draft for feedback.
---

# Document Review

Run a draft through six independent passes. Never combine passes into one skim - each has a different failure mode. Output a single review report plus a corrected redline draft.

## Passes

**1. Citation accuracy.** Delegate to the `cite-checker` agent: every statute, rule, and case cited must (a) exist, (b) say what the draft claims, (c) still be good law, (d) be cited in correct format for this jurisdiction. Verify against live sources - never trust a citation from memory, including citations this toolkit previously drafted. Flag any quote that does not match the source verbatim.

**2. Legal sufficiency.** Map the document against what it must legally do (elements of each claim/defense, standard of review, burden). Check `case-profile.md` case theory. Flag: elements with no supporting fact alleged, facts with no evidentiary support identified, arguments missing controlling authority, counterarguments ignored.

**3. Tone and professionalism.** Hunt for and rewrite: emotional language, sarcasm, hyperbole, personal attacks on opposing party or counsel, editorializing adverbs (clearly, obviously, outrageously), ALL CAPS or excessive emphasis, first-person grievance narration, speculation about motives. Convert every emotional passage into the factual assertion underneath it - the fact is the persuasive part. Preserve legitimate forcefulness; the goal is controlled, credible, not limp.

**4. Formatting compliance.** Check against the Formatting Requirements section of `case-profile.md`: caption, margins, font, spacing, line numbers, page limits, signature block, verification language, proof of service, exhibit references. Flag anything unverifiable so the user can check the physical document.

**5. Completeness.** Nothing important missed: all requested relief actually stated in the prayer, all exhibits referenced actually attached and correctly numbered, dates and names consistent throughout, no orphan defined terms, no [PLACEHOLDER] or TODO left in, procedural prerequisites recited (meet-and-confer, notice) where required.

**6. Stylistic tells.** Apply `references/style-tells.md` - patterns that read as machine-drafted or amateur and undermine credibility with clerks and judges. Rewrite flagged passages in plain, direct legal English.

## Output

Write `review-[docname]-[date].md` containing: a severity-ranked issue list (Blocker / Should fix / Polish), the reasoning for each, and proposed replacement text for every flagged passage. Then produce the corrected draft as a separate file - never overwrite the user's original. Summarize the top 5 issues in chat.

## Rules

- Severity honestly: a bad citation or missed element is a Blocker; a comma is Polish.
- If pass 2 reveals the document may be the wrong vehicle entirely (wrong motion type, missed deadline making it moot), say so at the top before any line edits.
- The user signs under penalty of perjury / Rule 11 equivalents - never let an unverified factual assertion or citation stand silently.
