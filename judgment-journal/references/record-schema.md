# Judgment Record Schema

Use a stable ID and append-only revisions. Render as Markdown, table fields, or database records without changing the semantics.

```yaml
id:
created_at:
question:
scope:
source_claim_ids: []
user_initial_judgment:
judgment_type: descriptive | value | action | mixed
supporting_reasons: []
opposing_reasons: []
key_assumptions: []
weakest_link:
confidence_percent:
change_my_mind_evidence: []
forecast:
  proposition:
  resolution_date:
  success_rule:
  failure_rule:
  confounders: []
planned_action:
ai_red_team:
user_revision:
status: open | resolved | ambiguous | retired
reviews: []
```

Each review should include date, observed evidence, outcome, process assessment, error type, lesson, and updated view. Never replace the initial judgment or an earlier review.

## Storage mappings

- Markdown or Obsidian: one file per judgment with YAML frontmatter and appended dated sections.
- Feishu Base, Notion, or Airtable: one judgment table plus a linked review table.
- Spreadsheet: one row per judgment and a separate append-only review sheet.
- Database: immutable judgment version rows linked by stable judgment ID.

Store source URLs and timestamps. Do not store only an AI summary when the original evidence can be referenced.

