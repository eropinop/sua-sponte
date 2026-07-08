# Sua Sponte

*"Of one's own accord."* A litigation toolkit for people representing themselves - built to make filings that hold up.

A complete workflow for preparing court filings without counsel - from case setup through the final pre-filing gate. Built to be jurisdiction-aware: every skill reads a per-case profile so output matches your state, county, court, and judge. Packaged as a Claude plugin (Cowork / Claude Code).

## Install

Zip the repo contents so `.claude-plugin/plugin.json` sits at the zip root, name it `sua-sponte.plugin`, and share it in a Claude Cowork chat to install:

```bash
git clone https://github.com/eropinop/sua-sponte && cd sua-sponte
zip -r sua-sponte.plugin . -x "*.git*"
```

## Workflow

1. **case-setup** - interview + research builds `case-profile.md`: court, judge, local formatting rules, signature/notary/service requirements, deadlines, case theory. Run once per matter, update as the case evolves.
2. **judge-research** - builds `judge-profile.md` from published opinions, standing orders, news, and evaluations: process preferences, tendencies, do/don't list.
3. **local-rules** - on-demand cited answers to any state/county procedure question.
4. **evidence-exhibits** - maps evidence to claim elements, finds gaps, builds exhibit lists with authentication plans and objection responses.
5. **doc-review** - six-pass deep review of any draft: citation verification (via cite-checker agent), legal sufficiency, tone/professionalism, formatting, completeness, stylistic tells.
6. **pressure-test** - adversarial red-team (via opposing-counsel agent) plus judge-lens review; attack map ranked Kill shot to Noise, with fixes and tactics.
7. **case-odds** - calibrated odds of prevailing: your prepared filings and evidence vs the opposition, scored across merit, procedure, evidence, authority, forum, and resource asymmetry; probability ranges, best/likely/worst scenarios, and the three levers that most move the odds.
8. **filing-check** - final GO/NO-GO gate: manifest completeness, signatures, notarization, service, e-filing mechanics, deadline math, final tell sweep.

## Agents

- **opposing-counsel** - attacks a packet the way real opposing counsel would.
- **cite-checker** - verifies every citation against live sources; flags fabrications as filing blockers.

## Notes

- Works best with a connected case folder per matter and CourtListener/Trellis connectors authorized for live docket and caselaw access; falls back to web search otherwise.
- This toolkit provides legal information and drafting support, not legal advice. You are the filer of record: verify citations, facts, and deadlines before signing, and comply with any court rules on AI-assisted drafting.
