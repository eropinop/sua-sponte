---
name: case-odds
description: Calibrated assessment of the odds of prevailing - your prepared filings and evidence versus what you're up against, with scenario ranges and the factors that move them. Use when the user asks "what are my odds", "chances of winning", "am I going to get eaten alive", "realistic outlook", "should I even file this", or "how does this play out".
---

# Case Odds

Produce an honest, calibrated read of how this fight goes - for the whole case or a single motion. The user needs a real number range and the reasons behind it, not reassurance and not doom. Both false confidence and false despair cost money and cases.

## Inputs

Gather before scoring; note explicitly which are missing and how that widens the error bars:
1. `case-profile.md` - case theory, elements, posture, deadlines
2. `judge-profile.md` - tendencies on this motion type / case type
3. Latest `pressure-test-*.md` - attack map (if stale or absent, offer to run pressure-test first; odds without a red-team are guesses)
4. `exhibit-workbook-*.md` - element coverage and gaps
5. The opposition: their filings so far, counsel's firm and track record (research them - web search, court records, Trellis/CourtListener if connected), resources, and observed strategy
6. Base rates: research grant/denial rates for this motion type in this court or state where findable (e.g., summary judgment grant rates, custody modification outcomes). Say when only national or analogous data exists.

## Method

Score each dimension 1-5 with a one-line justification tied to a specific fact or document:
- Legal merit - elements supported by admissible evidence
- Procedural posture - clean or exposed (timeliness, vehicle, prerequisites)
- Evidence strength vs their likely evidence
- Authority - controlling law for vs against
- Forum - judge tendencies, how this judge treats pro se parties
- Asymmetry - their counsel's skill/resources vs a prepared pro se; where that gap bites (motion practice, objections, procedure) and where it doesn't (facts, documents, preparation)
- Survivability of the attack map - how many Kill shots remain unfixed (any unfixed Kill shot caps the ceiling; say so)

Then produce:
- **Probability range** for the specific decision point (e.g., "motion granted in full: 30-45%; granted in part: 60-75%"), anchored to base rates and adjusted by the scores. Ranges, never point estimates. State confidence in the range itself (low/medium/high) based on input completeness.
- **Best / likely / worst scenario** narratives - what each looks like procedurally and what happens next in each.
- **The three levers** - the changes that would most move the odds (evidence to obtain, argument to add, defect to cure), each with estimated impact.
- **Eaten-alive check** - blunt paragraph: the ways an experienced opponent exploits a pro se party in THIS posture, and the specific countermeasure for each.
- **Decision aid** when the question is "should I file": expected value framing - upside if granted, cost if denied (fees, precedent in the case, credibility with the judge, exposure to fee-shifting), and any settlement-leverage effects either way.

## Rules

- Calibration over comfort. If it's 25%, say 25%, then show the levers.
- Never present odds as prediction or advice - litigation is high variance and this is information for the user's own decision. Say this once, plainly, not as boilerplate on every line.
- Distinguish what is scored from documents (strong basis) vs assumption (weak basis). No score without a stated reason.
- Re-run automatically after major events (ruling, new filing from opposition, new evidence) - odds are a snapshot, date-stamp the output.
- Output `case-odds-[scope]-[date].md`; keep prior versions so the trend line is visible.
