---
name: filing-check
description: Final pre-filing gate - verify every document in the packet is complete, signed, notarized where required, properly served, correctly formatted, and free of stylistic tells before it goes to the court. Use when the user says "final check", "ready to file", "filing checklist", "am I missing anything", or "check the packet".
---

# Filing Check

The last gate before the courthouse. Assume doc-review and pressure-test already ran on content; this pass is about the packet as a physical/electronic filing. Be pedantic - clerks reject filings for mechanical defects daily, and a rejection can blow a deadline.

## Process

1. Load `case-profile.md`. Confirm with the user exactly which documents are being filed and the target filing date.
2. Build the required-document manifest for this filing type from the local rules (e.g., motion + memorandum + declaration + proposed order + proof of service + cover sheet). Compare against what the user has. Missing items are Blockers.
3. Run `references/pre-filing-checklist.md` against every document. Verify what is verifiable from the files (captions, case numbers, dates, page limits, exhibit references, hearing date consistency, placeholder text); produce a manual-check list for what only the user can confirm (wet signatures, notary seal, copies, fees).
4. Signature and notarization audit:
   - Every signature block present, dated, and matching the required form from the profile
   - Verification/declaration language exactly as the jurisdiction requires
   - Every document the profile flags as requiring notarization: is it notarized, is the notary block complete, is the method (in-person/RON) accepted by this court
5. Final stylistic-tell sweep: run `doc-review` pass 6 (style-tells reference) across the packet one last time - final edits often reintroduce tells. If the court or judge has an AI-disclosure standing order recorded in the profile, confirm the required disclosure is included; compliance is non-negotiable.
6. Service check: correct parties, correct method, proof of service filled and signed, service deadline math correct for the method used.
7. Output `filing-readiness-[date].md`: GO / NO-GO verdict up top, then Blockers, then the manual-check list formatted as a print-friendly checklist, then a filing-day sequence (what order to do things, deadlines, fees, copies to bring).

## Rules

- NO-GO on any Blocker. Do not soften it. A rejected filing near a deadline is a catastrophe; a one-day revision is not.
- Recompute every deadline independently - do not trust dates typed in documents.
- If e-filing: check file format, size limits, bookmarking/text-searchability requirements, and redaction of protected identifiers per the court's e-filing rules.
- The user is the filer of record and signs everything. State clearly what they must physically verify themselves.
