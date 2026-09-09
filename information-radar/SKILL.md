---
name: information-radar
description: Monitor sources around a user's current questions, cluster duplicates, and return a deliberately small set of decision-relevant signals. Use for recurring intelligence scans, reading-list triage, daily or weekly digests, and source-watchlist review. Do not use to verify a claim in depth or declare it true.
---

# Information Radar

Turn a large stream into a small candidate set. Optimize the user's attention, not collection volume. Make the selection process inspectable so the user can judge not only the retained items, but also how the evidence pool was built.

## Establish the scan contract

Before collecting, pass three lightweight gates. Do not turn them into an endless framing exercise. Propose reasonable defaults and ask the user only about choices that would materially change the evidence pool or intended use.

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

### Collection-protocol gate

For decision-relevant, publishable, or strict scans, show a compact proposed collection protocol before broad collection and let the user correct material assumptions. Define:

- subquestions and the evidence role needed for each;
- discovery channels, queries or keyword families, including credible opposing searches;
- time, geography, population, language, and content-type boundaries;
- inclusion and exclusion rules;
- sampling or result-selection method for algorithmic platforms;
- deduplication unit and stopping rule.

For quick exploratory scans, the protocol may be generated and executed without pausing when the defaults are low-risk, but it must still appear in the acquisition record. Read [references/collection-protocol.md](references/collection-protocol.md) when designing a new scan, using an algorithmically ranked platform, or preparing research for a decision or publication.

Do not describe open-web search as representative or scientific sampling unless a defined population and defensible sampling frame justify that wording. More channels, queries, or items do not by themselves establish adequate coverage.

Do not start broad collection until all three gates are adequate for the chosen mode. A small exploratory scan may proceed with incomplete coverage when that limitation is stated.

## Collect and normalize

Preserve the original URL, author or organization, publication time, retrieval time, content type, and available primary source. Never treat multiple reposts of one origin as independent confirmation.

Keep a search ledger with the channel, query, retrieval time, ordering or filter, number inspected, and access limitation. For algorithmically ranked feeds, record that the sample is platform-selected or personalized and avoid prevalence claims unless a suitable denominator exists.

Group semantically equivalent items into an event cluster. Choose the closest authoritative or original item as the primary entry; retain only interpretations that add independent evidence, a distinct implication, or a meaningful disagreement.

After collection and before synthesis, audit coverage against the planned evidence roles. Distinguish `covered`, `partially_covered`, `missing`, and `unavailable`. A source category is not covered merely because one item was found; check scope, method, independence, recency, and conflicts. If a material gap could change the result, either continue collection, ask for a justified unlock, narrow the question, or explicitly prohibit the unsupported conclusion.

## Triage

Score attention value with the stable rubric in [references/scoring.md](references/scoring.md). The score measures whether an item deserves attention, not whether its claim is true.

Apply the selected profile by changing the inclusion threshold and maximum item count, not by silently changing the rubric. Preserve weak signals in exploratory mode and require stronger evidence or decision impact in strict mode.

Maintain diversity deliberately. When available and relevant, include original sources, independent practitioners, credible disagreement, and adjacent-domain evidence. Do not infer authority from followers, verification badges, or popularity alone.

## Output

Return an evidence packet, not an invisible feed ranking. Keep the main digest within the attention budget; zero retained items is a valid result.

Start with a compact research contract and acquisition receipt:

- the operational question, scope, mode, and evidence roles;
- channels and query families actually used;
- counts inspected, deduplicated, excluded, and retained when available;
- major exclusion reasons, access limits, and algorithmic-sampling caveats;
- coverage status and conclusions that the evidence cannot support.

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

When the packet will precede the user's own judgment, present source material and evidence roles before a persuasive synthesis. Clearly separate source statements from Radar's selection rationale so the digest does not silently become the user's conclusion.

## Boundaries

- Do not declare truth from a Radar score.
- Do not confuse a topic with a research question, or available sources with adequate coverage.
- Do not claim completeness, representativeness, or scientific coverage from search volume or platform variety.
- Do not infer prevalence or consensus from engagement, top-ranked results, or a purposive community sample.
- Do not silently change the agreed question, geography, population, time window, or intended decision during collection.
- Do not fill a quota on a quiet day.
- Do not update a watchlist silently. Recommend additions, removals, or tier changes with reasons.
- Do not optimize future recommendations from clicks or likes alone. Prefer downstream signals such as changed decisions, completed experiments, durable reuse, and later accuracy.
- Preserve the user's chosen platform and storage system; output portable structured text when no integration is available.
