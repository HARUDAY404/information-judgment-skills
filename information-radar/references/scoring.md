# Radar Scoring and Calibration

## Dimensions

Score each dimension 0–3 and retain a one-sentence reason:

- `question_relevance`: connection to the active question or decision;
- `information_gain`: change beyond what is already known;
- `potential_impact`: plausible effect on a decision, model, or experiment;
- `timeliness`: value lost if reviewed later;
- `distinctiveness`: independent evidence, unusual perspective, or credible disagreement;
- `actionability`: supports a concrete next question, check, decision, or experiment.

Keep source proximity, source tier, and promotional incentives as separate signals. Do not hide them inside the content score.

## Profiles

- `exploratory`: lower inclusion threshold, more weak signals, maximum 8 items;
- `standard`: balanced threshold, maximum 5 items;
- `strict`: higher threshold and evidence requirement, maximum 3 items.

Changing profile changes threshold and capacity, not the dimensions already assigned to an item.

## Calibration

Maintain a frozen evaluation set containing valuable primary updates, credible disagreement, community weak signals, duplicates, promotional items, unsupported claims, and attractive noise.

For every rubric or weight revision:

1. save the proposed version and reason;
2. replay the frozen set under old and new versions;
3. inspect newly included and newly excluded items;
4. compare valuable misses and noise admitted;
5. approve the change explicitly or keep the old version.

Do not add a rule solely to fix one recent example. Never allow the system to rewrite scoring rules or source tiers silently.

