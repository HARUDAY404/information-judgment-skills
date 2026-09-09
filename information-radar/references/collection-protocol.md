# Collection Protocol and Evidence Receipt

Use this reference when a scan informs a real decision, may be published, uses algorithmically ranked platforms, or needs to be compared across models.

## Choose the mode

- `quick`: answer a low-stakes exploratory question with sensible defaults and a short receipt. Do not pause unless a missing choice would materially change the result.
- `guided`: propose the question, evidence map, and collection plan; ask the user to correct the few consequential choices before broad collection.
- `auditable`: freeze the protocol before collection, preserve a complete search ledger and exclusion log, and make the resulting pool reproducible as far as access permits.

Mode changes the amount of interaction and documentation, not the obligation to state limitations.
It is separate from the exploratory, standard, or strict triage profile in `scoring.md`, which controls the inclusion threshold and item limit.

## Build an evidence map

Break the question into subquestions. For each, specify:

| Field | Meaning |
|---|---|
| subquestion | The bounded thing the scan needs to learn |
| evidence_role | Product record, population estimate, outcome evidence, lived experience, policy, disagreement, or another justified role |
| suitable_sources | Source types capable of supporting that subquestion |
| cannot_establish | Conclusions those source types cannot support |
| minimum_coverage | What must be present before synthesis |

Do not use source variety as a substitute for this map. Several communities may all provide lived experience while leaving outcome evidence absent; several articles may all repeat one vendor report.

## Freeze the material choices

Record before collection when applicable:

- decision or intended use;
- time window and whether older background evidence is allowed;
- population, geography, domain, and language;
- query families and synonyms;
- queries designed to find disagreement, failures, or alternative explanations;
- inclusion and exclusion criteria;
- sorting, filters, and number of results inspected per query;
- deduplication unit: URL, original report, event, claim, or another explicit unit;
- stop rule.

A useful stop rule is reached when the required evidence roles are adequately covered, every central claim has had a counterevidence search, new searches mostly return duplicates or lower-value material, and remaining gaps are named. Stopping because the desired story already looks convincing is invalid.

## Treat platform samples honestly

Search engines and social feeds are usually ranked, personalized, access-limited, and unstable. Record the visible sorting and filters, retrieval time, account or personalization caveat, number inspected, and selection rule.

Call such material a structured search sample, purposive sample, or platform-ranked sample as appropriate. Do not call it representative without a population and defensible sampling frame. Community posts can establish that an experience or narrative exists; they do not alone establish frequency, population consensus, or causal effect.

## Keep the search ledger

For every search route preserve:

```yaml
channel:
query_or_route:
retrieved_at:
scope_filters:
ordering:
inspected_count:
access_limitations:
notes:
```

For each retained or materially excluded item preserve the original source, publication date, source role, original origin when reposted, and exclusion or retention reason.

## Audit coverage before synthesis

Label each planned evidence role:

- `covered`: suitable evidence matching the important scope is present;
- `partially_covered`: relevant evidence exists but has material method, scope, independence, or access limitations;
- `missing`: the scan did not find suitable evidence;
- `unavailable`: suitable evidence is known or likely to exist but could not be accessed.

If a central evidence role is partial or missing, continue searching only when the expected information gain justifies the cost. Otherwise narrow the question or state which conclusion is prohibited.

## Produce the evidence receipt

The receipt should let a reader answer:

1. What exactly was researched?
2. Where and how was it searched?
3. How were items selected and deduplicated?
4. What evidence roles are strong, partial, or absent?
5. What could this process systematically miss?
6. Which conclusions are not justified?

Keep the reader-facing digest short. Put the search ledger and detailed exclusions in an expandable or separate appendix when possible.

## Comparing models

Freeze the same question, protocol, accessible tools, time budget, and evaluation set. Compare citation validity, original-source recovery, scope compliance, duplicate handling, opposing-evidence retrieval, important misses, and human-accepted signal yield. Do not choose a model from prose quality or item count alone.
