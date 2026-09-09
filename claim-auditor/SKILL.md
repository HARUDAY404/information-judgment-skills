---
name: claim-auditor
description: Decompose consequential content into checkable claims, trace provenance, seek counterevidence and alternative explanations, and report what the evidence supports with explicit uncertainty. Use before relying on, sharing, or acting on a disputed or important claim. Do not decide the user's values or personal priorities.
---

# Claim Auditor

Determine how far the available evidence supports a claim. Audit claims, not people or entire articles.

## Scope the audit

Identify the consequential statement and the decision it may influence. Audit all claims only when the user requests a comprehensive review; otherwise prioritize claims that are central, surprising, causal, quantitative, predictive, universal, or action-changing.

When the audit will inform the user's own consequential judgment, confirm that a pre-audit view has been saved, but do not request or inspect its content when a blind audit is feasible. If no snapshot exists, invite the user to save one before presenting evidence; `undecided` is valid. Do not require this checkpoint for neutral fact-checking, urgent safety work, or when the user declines. If the user's prior position is already visible in the same context, label the audit `non-blind` and actively check whether the evidence review is merely agreeing with it. Preserve any incoming `signal_id` and assign stable `claim_id` values to audited claims.

## Decompose

Rewrite rhetoric into atomic statements without strengthening the author's language. Expose hidden premises. Classify each as:

- observable fact;
- interpretation or opinion;
- causal or explanatory inference;
- case under specific conditions;
- forecast with a future resolution;
- normative recommendation;
- promotional claim;
- unclear or currently untestable.

Facts require verification; causal claims require alternatives; cases require boundary conditions; forecasts require dates and resolution criteria; values require premise analysis rather than a false true/false verdict.

## Trace provenance

Follow citations toward the closest available original record. Record every material hop and detect circular sourcing. Separate independent corroboration from repeated reporting based on the same source.

Evaluate the claim with [references/evidence-rubric.md](references/evidence-rubric.md). A primary source is closer, not automatically correct. Examine methods, denominators, sample selection, incentives, missing data, and whether the source supports the wording actually used.

## Challenge

Search deliberately for credible counterevidence, failure cases, base rates, and alternative explanations. Apply the same quality standard to supporting and opposing evidence. State when access, time, language, paywalls, or missing data prevent a fair search.

## Produce a claim card

For each material claim report:

- `signal_id` when supplied and a stable `claim_id`;
- original wording and faithful atomic rewrite;
- claim type;
- provenance chain;
- supporting evidence;
- opposing evidence;
- alternative explanations;
- boundary conditions and conflicts of interest;
- evidence-strength dimensions with reasons;
- maximum conclusion justified by current evidence;
- remaining unknowns and evidence that would change the assessment.

Use conclusions such as directly supported, indirectly supported, plausible but underdetermined, case only, overgeneralized, contradicted, value-dependent, or insufficient evidence. Avoid binary verdicts when evidence is mixed.

## Boundaries

- Do not convert source prestige into proof.
- Do not treat several dependent reports as independent confirmation.
- Do not manufacture numerical precision from qualitative evidence.
- Do not treat agreement with the user's prior view as evidence that the audit is correct.
- Do not decide whether the claim matters personally to the user.
- Do not proceed to content production as though an uncertain hypothesis were established fact.
