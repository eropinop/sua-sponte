---
name: judge-research
description: Build or refresh a profile of the assigned judge - published opinions, rulings in similar cases, news, standing orders, and procedural preferences. Use when the user says "research my judge", "judge profile", "what does Judge X like", "how does my judge rule on", or after case-setup assigns a judge.
---

# Judge Research

Produce a practical `judge-profile.md` in the case folder: not a biography, a playbook for how this judge runs their courtroom and what persuades them.

## Process

1. Read `case-profile.md` for the judge's name, court, and case type. If missing, ask.
2. Research, in parallel where possible (web search; CourtListener/Trellis tools if connected):
   - Published opinions and notable rulings, weighted toward the case's subject matter - extract reasoning patterns, what arguments won, what the judge criticized
   - The judge's standing orders and department rules (courtesy copies, tentative rulings, oral argument practices, meet-and-confer requirements, page-limit strictness, AI-disclosure orders)
   - Recent news and current high-profile cases before the judge
   - Bar association reviews, judicial evaluations, attorney forum commentary (mark as anecdotal)
   - Background: appointment, prior practice (prosecutor, civil defense, plaintiff's bar), tenure - as context for leanings, not prediction
3. Distill into `judge-profile.md`:
   - Process preferences (the actionable core): formatting pet peeves, punctuality on deadlines, tentative ruling practice, how they treat pro se litigants, oral argument style
   - Substantive tendencies in this case type, each backed by a cited ruling or source
   - Do / Don't list for filings and hearings before this judge
   - Sources with dates
4. Flag anything in the user's current draft documents that conflicts with a known preference.

## Rules

- Distinguish evidence tiers: published opinions (strong) > standing orders (binding) > news (moderate) > forum anecdotes (weak, label as such).
- Never present tendencies as guarantees. Judges rule case by case.
- Date-stamp the profile; suggest a refresh before any major hearing.
- If little is public (common for newer or lower-court judges), say so plainly and pivot to the court's general practices instead of padding with speculation.
