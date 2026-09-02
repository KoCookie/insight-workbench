# Source Library and Coverage Checklist Structure

## 1. Purpose

This document defines how Insight Workbench should help users collect, organize, and evaluate sources inside a Topic Board.

The goal is to make source collection guided and structured, especially when some useful materials require manual collection or human judgment.

## 2. Product Intent

The Source Library should help users answer:

- What sources have I added?
- Which source categories are still missing?
- Which sources have been processed?
- Which claims are supported by which sources?
- What should I collect next?

The Coverage Checklist should help users answer:

- Which research areas are covered?
- Which research areas are weak or missing?
- Which gaps should I investigate next?
- Which gaps are intentionally skipped?

## 3. Source Library Structure

Required sections:

- Source input area
- Recommended source checklist
- Added sources list
- Source status indicators
- Extraction status indicators
- Source category coverage
- AI actions

Recommended layout:

```text
Sources
-> Add source
-> Recommended source categories
-> Added sources
-> Extraction results
-> Missing source categories
```

## 4. Source Input Methods

MVP input methods:

- Upload file
- Paste link
- Add manual note
- Add source from recommended checklist

Future input methods:

- Browser clipping
- Connected data integrations
- Scheduled source refresh
- Cross-topic source reuse

## 5. Source Category Taxonomy

MVP source categories:

- Official website
- Company report
- Policy or regulation
- Industry association
- Research report
- News
- Competitor website
- Company database
- Recruiting or job market
- Social or community discussion
- Video or article
- First-hand observation
- Other

Each source category should include:

- category name
- reason it matters
- example source types
- status
- linked sources

## 6. Source Status Values

Recommended source status values:

- `recommended`
- `added`
- `extracting`
- `extracted`
- `failed`
- `ignored`

User-facing labels:

- Recommended
- Added
- Processing
- Processed
- Needs attention
- Skipped

Status rules:

- A recommended source category can exist before a source is added.
- A source can fail extraction without being removed.
- A skipped source category should remain visible so the user understands coverage tradeoffs.

## 7. Extraction Status Values

Recommended extraction status values:

- `pending`
- `extracting`
- `extracted`
- `reviewed`
- `failed`

Extraction outputs:

- facts
- claims
- entities
- timeline events
- quotes
- data points
- sentiment
- summary
- possible insight cards

AI-generated extraction results should be reviewable before they become trusted research assets.

## 8. Research Coverage Checklist

Coverage item status values:

- `not_started`
- `needs_sources`
- `in_progress`
- `covered`
- `skipped`
- `needs_follow_up`

User-facing labels:

- Not started
- Needs sources
- In progress
- Covered
- Skipped
- Needs follow-up

Example coverage areas:

- Market size and growth
- Policy or regulatory context
- Competitive landscape
- Value chain or ecosystem
- Key companies or players
- Demand behavior
- Risks and constraints
- International or comparative perspective
- Opposing views or negative signals
- Primary or authoritative sources

## 9. Missing Source and Weak Coverage Display

The product should show weak coverage clearly without blocking the user.

Recommended patterns:

- Missing category badge
- Low-confidence label
- "Needs sources" state
- Evidence gap card
- Suggested next action
- Source checklist progress indicator

Example message:

```text
Policy context is not covered yet. Add a policy source or mark this area as skipped.
```

## 10. AI Recommendations

AI should recommend missing source categories based on:

- topic type
- selected Research View
- existing sources
- coverage checklist status
- generated insight gaps

AI should explain why a source category matters.

Example:

```text
Recruiting or job market sources may help you understand which skills and roles are growing in this field.
```

## 11. Source-grounding Rules

Dashboard Widgets, Insight Cards, Analysis Artifacts, and Outputs should reference source IDs where possible.

If a claim is not source-grounded, it should be labeled as:

- assumption
- inference
- unsupported
- low-confidence

Contradictory claims should be shown as competing claims rather than forced into one conclusion.

## 12. MVP Requirements

Required for the first prototype:

- Add file, link, or manual note
- Show source category checklist
- Show added source list
- Show source and extraction status
- Show missing source categories
- Connect source IDs to insight cards or dashboard claims

Can be simplified:

- Extraction can be mocked or template-generated before real AI integration.
- Source reliability can use simple labels instead of a complex score.
- Coverage status can be manually editable.

Out of scope:

- Fully automated web crawling
- Guaranteed access to closed or restricted platforms
- Paid data integrations
- Real-time source monitoring
- Cross-topic global source library

## 13. Open Questions

- Should source categories be fixed, AI-generated, or a hybrid?
- Should reliability be manually selected, AI-estimated, or both?
- How should social or community sources be weighted?
- Should source extraction results appear inline or in a separate review queue?
- What is the minimum useful citation format for the first prototype?
