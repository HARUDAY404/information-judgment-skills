---
name: judgment-journal
description: Record a user's own initial judgment before AI critique, expose assumptions, attach confidence and testable predictions, and append outcome reviews without overwriting history. Use for consequential beliefs, decisions, forecasts, and recurring reasoning review. Do not fabricate the user's position or force a conclusion.
---

# Judgment Journal

Turn audited information into the user's explicit, revisable judgment. The journal exists to improve calibration, not to manufacture polished opinions.

## Use two passes when evidence will be audited

Use a pre-audit pass to save the user's initial view before detailed AI critique, then a post-audit pass to append what changed. Never place the first pass after `claim-auditor`. Carry forward available `signal_id` and `claim_id` values so the reasoning chain remains traceable.

## Preserve the user's voice first

For a consequential entry, ask the user for a rough initial judgment before proposing one. It may be incomplete. Preserve it verbatim or clearly label a faithful paraphrase. If the user declines or has no view, record `undecided`; do not synthesize an AI-authored opinion and attribute it to the user.

Low-risk material may be structured automatically, but the system must distinguish user statements, imported evidence, and AI analysis.

## Structure the judgment

Use the record in [references/record-schema.md](references/record-schema.md). Separate:

- descriptive belief about the world;
- value judgment about what matters;
- action judgment about what to do.

Expose key premises, supporting and opposing reasons, weakest link, scope, and the evidence that would change the view.

## Calibrate

Invite a confidence estimate only when the proposition is sufficiently clear. Explain that it is the user's current belief, not an objective evidence score. Convert important beliefs into forecasts with a deadline, resolution rule, expected observation, and known confounders.

Act as a fair red team after the initial judgment is saved. Offer the strongest plausible objection, alternate model, base rate, and missing stakeholder view. Let the user accept, reject, or revise. Preserve both the initial and revised versions.

## Review outcomes

At the resolution date, append rather than overwrite:

- actual outcome and evidence;
- whether the forecast resolved clearly;
- process quality versus outcome luck;
- error source: missing evidence, faulty inference, bad definition, execution, timing, or randomness;
- a narrow reusable lesson;
- updated judgment and confidence.

Do not count unresolved or ambiguously defined forecasts as successes. When enough comparable forecasts exist, summarize calibration by confidence band without claiming more precision than the sample supports.

## Boundaries

- Do not demand an opinion on every item.
- Do not reward confident language.
- Do not rewrite history or conceal changes of mind.
- Do not treat a good outcome as proof of good reasoning, or a bad outcome as proof of bad reasoning.
- Do not publish or transmit private entries without explicit user authorization.
- Preserve the user's chosen storage system; use portable Markdown when no adapter is available.
