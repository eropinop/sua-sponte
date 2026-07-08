---
name: case-setup
description: Set up or update a case profile for a litigation matter - jurisdiction, court, judge, case type, deadlines, local formatting rules. Use when the user says "new case", "set up my case", "case setup", "update my case profile", or starts working on a matter with no profile on file.
---

# Case Setup

Build a per-case profile that every other skill in this toolkit reads before doing anything. One profile per matter, stored in the user's case folder (ask them to connect a folder if none is connected) as `case-profile.md`.

## Process

1. Check for an existing `case-profile.md` in the working folder. If found, load it, show a one-line summary, and ask what to update instead of re-interviewing.
2. Interview the user (use AskUserQuestion, batch questions, skip anything already known from conversation or documents):
   - Case caption, case number, parties, and the user's role (plaintiff/defendant/petitioner/respondent)
   - Case type (civil, family, small claims, landlord-tenant, probate, other)
   - State, county, specific court and division/department
   - Assigned judge (name, department)
   - Opposing counsel or party (name, firm)
   - Current posture: what has been filed, what deadlines are pending
   - Filing method: e-filing portal, in person, mail - and whether the court requires pro se litigants to file on paper
3. Research and fill in what the user should not have to know by hand (web search; use CourtListener/Trellis tools if connected):
   - Court's local rules URL, standing orders, and any judge-specific rules
   - Document formatting requirements: paper size, margins, font, line spacing, line numbering, caption format, page limits by motion type, exhibit tab conventions
   - Signature requirements: wet vs electronic, verification/declaration requirements (e.g., "under penalty of perjury" language and the state's required form)
   - Notarization rules: which document types require notarization in this jurisdiction, and whether remote online notarization is accepted
   - Service rules: who must be served, how, and proof-of-service format
   - Fee schedule and fee waiver availability
   - Any AI-use disclosure requirements: check the court's and judge's standing orders for rules about AI-assisted drafting. Record what is required. Never advise concealing AI use where disclosure is mandated.
4. Write `case-profile.md` using `references/case-profile-template.md`. Cite the source (URL) for every researched rule so it can be re-verified.
5. Offer to run `judge-research` next to build the judge profile, and to schedule a periodic docket/deadline check.

## Rules

- Verify every local rule against a current official source (court website, published local rules). Local rules change - date-stamp everything researched.
- If state and county sources conflict, flag it and cite both.
- Keep the profile factual and source-cited. It is the single source of truth for the other skills; wrong data here propagates everywhere.
