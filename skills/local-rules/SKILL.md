---
name: local-rules
description: Answer a specific procedural or local-rule question for the case's jurisdiction - deadlines, service, motion practice, form requirements, county quirks. Use when the user asks "what's the rule on", "how many days do I have", "does this county require", "local rule for", or any state/county procedure question.
---

# Local Rules Lookup

Answer jurisdiction-specific procedure questions with current, cited authority - state rules of procedure, county local rules, and court standing orders, in that stack.

## Process

1. Read `case-profile.md` for jurisdiction and court. If the question targets a different jurisdiction, confirm before answering.
2. Identify the full rule stack that could govern: state statute/rule of procedure, state rules of court, county local rules, department standing orders, judge preferences. Lower layers can add requirements but rarely remove them.
3. Search current official sources (legislature site, court rules pages, court website; CourtListener if connected). Do not answer deadline or service questions from memory - rules change and counties differ.
4. Answer in this shape:
   - Direct answer first (the number, the requirement, the form name)
   - Rule citation(s) with links and the date verified
   - How the layers interact if more than one applies
   - Trap warnings: counting method (court days vs calendar days), extensions for service method, holiday rules, local quirks
5. If the answer affects a recorded deadline, offer to update `case-profile.md`.

## Rules

- If sources are ambiguous or conflict, present both readings and recommend the conservative one (earlier deadline, stricter requirement).
- Always state that this is legal information, not legal advice, when the question is judgment-laden rather than mechanical.
- Cache stable findings into `case-profile.md` under local quirks so repeat lookups are free.
