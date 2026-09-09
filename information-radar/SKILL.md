---
name: information-radar
description: Monitor sources around a user's current questions, cluster duplicates, and return a deliberately small set of decision-relevant signals. Use for recurring intelligence scans, reading-list triage, daily or weekly digests, and source-watchlist review. Do not use to verify a claim in depth or declare it true.
---

# Information Radar

Turn a large stream into a small candidate set. Optimize the user's attention, not collection volume.

## Establish the scan contract

Before collecting, pass two lightweight gates. Do not turn them into an endless framing exercise; infer reasonable defaults and ask only when a missing choice would materially change the search.

### Question gate

Clarify what decision or understanding the scan should support, whether the question is decision-led or exploratory, what its key terms mean in context, and what would make the scan worth the user's attention. Reframe an unbounded topic into an answerable question without pretending the first wording is final.

Establish:

- the decision or question this scan should inform;
- time window, affected population, geography, and domain;
- attention budget and strictness profile;
- whether community experience, scientific evidence, product updates, market signals, or practitioner cases are needed.

### Coverage gate

Map each evidence need to suitable source roles before collection. Separate sources into `available`, `important_but_missing`, and `unlockable`. For every material source type, state what it can establish and what it cannot. Use a suitable source profile from [references/source-profiles.md](references/source-profiles.md); combine profiles when the question spans multiple evidence types.

Only propose a login, QR scan, browser-cookie access, paid service, or API setup when the missing source would materially improve the answer. Before asking, explain what evidence it adds, what data or permission is involved, cost when known, where outputs are stored, and the limitation if the user declines. A declined or unavailable source becomes an explicit coverage gap, not a reason to fabricate completeness.

Do not start broad collection until both gates are adequate for the chosen mode. A small exploratory scan may proceed with incomplete coverage when that limitation is stated.

## Collect and normalize

Preserve the original URL, author or organization, publication time, retrieval time, content type, and available primary source. Never treat multiple reposts of one origin as independent confirmation.

Group semantically equivalent items into an event cluster. Choose the closest authoritative or original item as the primary entry; retain only interpretations that add independent evidence, a distinct implication, or a meaningful disagreement.

## Triage

Score attention value with the stable rubric in [references/scoring.md](references/scoring.md). The score measures whether an item deserves attention, not whether its claim is true.

Apply the selected profile by changing the inclusion threshold and maximum item count, not by silently changing the rubric. Preserve weak signals in exploratory mode and require stronger evidence or decision impact in strict mode.

Maintain diversity deliberately. When available and relevant, include original sources, independent practitioners, credible disagreement, and adjacent-domain evidence. Do not infer authority from followers, verification badges, or popularity alone.

## Output

Return no more than the attention budget. Zero items is a valid result.

For each retained signal provide:

- a stable `signal_id` that can be carried into later review;
- concise event or claim;
- why it matters to the stated question;
- signal type: new event, new evidence, disagreement, weak signal, or repeated narrative;
- primary source and useful independent interpretation;
- attention-value dimensions and selection reason;
- whether it should proceed to `claim-auditor`;
- what may be missed by ignoring it.

End with a compact account of clustered duplicates, excluded noise, coverage gaps, and notable opposing evidence. Do not turn the digest into a long essay.

## Boundaries

- Do not declare truth from a Radar score.
- Do not confuse a topic with a research question, or available sources with adequate coverage.
- Do not fill a quota on a quiet day.
- Do not update a watchlist silently. Recommend additions, removals, or tier changes with reasons.
- Do not optimize future recommendations from clicks or likes alone. Prefer downstream signals such as changed decisions, completed experiments, durable reuse, and later accuracy.
- Preserve the user's chosen platform and storage system; output portable structured text when no integration is available.
