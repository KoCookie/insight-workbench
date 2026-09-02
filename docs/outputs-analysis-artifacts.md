# Output and Analysis Artifact Structure

## 1. Purpose

This document defines how Insight Workbench should turn Topic Board content into structured analysis artifacts and shareable outputs.

The goal is to make outputs useful without over-scoping the MVP into full report automation or slide generation.

## 2. Product Intent

Analysis Artifacts help users think more deeply.

Outputs help users share, reuse, or present what the Topic Board currently knows.

Both should be generated from board content, sources, insight cards, and coverage state. They should not be generated from isolated prompts.

## 3. Analysis Artifact Types

Required MVP artifact types:

- SWOT
- PEST
- competitor comparison
- evidence table

Optional MVP artifact types:

- value chain
- priority matrix
- maturity assessment
- timeline

Future artifact types:

- issue tree
- market map
- scenario ranking model
- technology-to-scenario matrix
- Three Horizons roadmap
- weighted scoring model

## 4. Analysis Artifact Structure

Each Analysis Artifact should include:

- title
- artifact type
- source Topic Board
- Research View, if applicable
- generated content
- source references
- confidence state
- assumptions
- last generated timestamp
- edit status

Recommended states:

- draft
- reviewed
- edited
- needs update

## 5. Artifact Generation Rules

An artifact should be generated from:

- selected Research View
- relevant Sources
- relevant Insight Cards
- relevant Coverage Checklist items
- user-selected focus area, if provided

An artifact should show:

- what evidence was used
- which claims are weak
- which assumptions were made
- which source gaps affect the analysis

## 6. MVP Output Types

Required MVP output:

- Research brief

Recommended MVP output:

- Evidence table

Optional MVP outputs:

- Interview preparation notes
- Report outline

Future outputs:

- Markdown export
- PDF export
- slide outline
- presentation draft
- recurring update summary

## 7. Research Brief Structure

A research brief should include:

- topic title
- research goal
- executive summary
- key facts
- key trends
- major players or stakeholders
- risks and opportunities
- evidence gaps
- source references
- suggested next steps

The brief should preserve uncertainty. It should not hide weak evidence or unsupported assumptions.

## 8. Evidence Table Structure

An evidence table should include:

- claim
- source
- source category
- evidence type
- confidence level
- related insight card
- notes

The evidence table is important for professional workflows but can also help casual users understand why the dashboard says what it says.

## 9. Output Generation Flow

```text
Open Topic Board
-> Select Research View
-> Choose output type
-> Review included sections
-> Generate draft
-> Edit draft
-> Copy or export
```

MVP simplification:

- The first prototype can generate output from the current dashboard state.
- Users do not need advanced section selection in the first version.
- Copy or Markdown export is enough before PDF or slide export.

## 10. Source Reference Rules

Outputs should preserve source references where possible.

Reference levels:

- source-linked claim
- source-linked section
- source list at the end
- assumption label when no source is available

The MVP should avoid implying that every statement is fully verified. If source support is weak, the output should say so.

## 11. Difference Between Widgets, Artifacts, and Outputs

Dashboard Widget:

- lives on the Topic Board dashboard
- summarizes part of the current research state
- helps users decide what to do next

Analysis Artifact:

- deeper structured analysis generated from board content
- supports reasoning and comparison
- may later feed an output

Output:

- shareable or reusable deliverable
- organized for reading outside the dashboard
- should include source references and caveats

## 12. MVP Requirements

Required for the first prototype:

- Generate a research brief from the current board
- Generate or display an evidence table
- Preserve source references where possible
- Mark unsupported assumptions
- Allow users to edit generated text

Can be simplified:

- Export can be copyable text or Markdown.
- Artifacts can be generated from mock or sample content.
- Source references can use simple source names before full citation formatting.

Out of scope:

- Full slide deck generation
- PDF layout engine
- Complex report builder
- Multi-format publishing workflow
- Automated recurring reports
- Collaborative review workflow

## 13. Open Questions

- Should the first prototype include one output type or multiple?
- Should Evidence Table be treated as an artifact, output, or both?
- What minimum citation format is credible enough for the MVP?
- Should users choose which widgets feed the output?
- How much editing should happen inside the product versus after export?
