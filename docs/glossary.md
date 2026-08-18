# Glossary and Product Language Rules

## 1. Purpose

This document defines the core product terms and language rules for Insight Workbench.

The goal is to keep product documentation, UI copy, issues, and future implementation consistent. Insight Workbench should sound like a structured research workspace, not a generic AI chatbot, a heavy consulting system, or an enterprise document repository.

## 2. Product Language Principles

### 2.1 Use Workspace Language

Preferred language:

- research workspace
- topic board
- source library
- insight card
- research view
- coverage checklist
- analysis artifact
- dashboard
- output

Avoid language that makes the product feel like a simple chat interface:

- chatbot
- chat wrapper
- AI Q&A page
- prompt box as the main product

The product may include chat-like interactions, but the primary product surface should be structured boards, sources, checklists, dashboards, and artifacts.

### 2.2 Use Topic Language Instead of Heavy Project Language

Preferred user-facing term:

- Topic Board

Use carefully:

- project
- repository
- workspace repository

Reason: users should feel they are researching and tracking a topic, not managing a complex consulting project. The backend may still use project-like data models, but the UI should stay lightweight.

### 2.3 Make AI an Embedded Workflow Engine

Preferred language:

- AI action
- AI-assisted
- AI-generated draft
- suggested next step
- source-grounded synthesis
- evidence gap
- follow-up question

Avoid implying that the product trains a new AI model:

- train a consulting AI model
- proprietary AI model
- custom foundation model
- AI model built from scratch

The product should be described as integrating existing AI models with workflow-level configuration, prompts, retrieval, templates, and product-specific actions.

### 2.4 Keep Claims Source-grounded

Preferred language:

- source-grounded claim
- supporting evidence
- explicit assumption
- inferred conclusion
- low-confidence claim
- conflicting claims

Avoid presenting AI-generated analysis as final truth.

The product should help users distinguish:

- facts
- claims
- opinions
- sentiment
- assumptions
- inferred conclusions

### 2.5 Use Progressive Depth

Preferred language:

- start with an overview
- deepen analysis
- add a research view
- continue from a gap
- generate an analysis artifact

Avoid splitting the product into disconnected user modes such as:

- casual module
- intern module
- consultant module

All users should begin from the same Topic Board. Advanced workflows should appear as deeper views and actions.

## 3. Core Product Terms

### Insight Workbench

Definition: an AI research workspace that helps users turn scattered sources into structured, source-grounded research boards, dashboards, and outputs.

Use when referring to the full product.

### Topic Board

Definition: the main workspace for one research topic.

A Topic Board contains sources, insight cards, research views, coverage checklist items, dashboard widgets, analysis artifacts, and outputs.

Use instead of "project" in user-facing product copy unless technical context requires otherwise.

### Research Topic

Definition: the subject the user wants to understand.

Examples:

- an industry
- a company
- a market
- a policy area
- a technology trend
- a competitor set
- a content research topic

The product should help users reframe unsupported or overly broad inputs into researchable topics.

### Research Goal

Definition: the user's intended purpose for researching a topic.

Examples:

- quick industry overview
- job or interview preparation
- company research
- competitor analysis
- consulting-style analysis
- coursework or academic research
- investment or market monitoring
- content research

The first selected goal becomes the primary Research View.

### Research View

Definition: a goal-specific view inside a Topic Board.

Research Views allow one topic to support multiple use cases without duplicating sources or insight cards.

Examples:

- Overview
- Job or Interview Prep
- Company Research
- Competitor Analysis
- Market Monitoring
- Consulting-style Analysis
- Content Research

### Source

Definition: any material used as evidence or context for research.

Examples:

- uploaded file
- pasted link
- manual note
- public report
- policy document
- company page
- news article
- user observation

Sources should be stored in the Source Library and connected to claims, insight cards, dashboard widgets, and outputs.

### Source Library

Definition: the collection of sources attached to a Topic Board.

The Source Library should show what has been added, what has been extracted, and what source categories may still be missing.

### Source Checklist

Definition: a list of recommended source categories for the user's topic and goal.

The Source Checklist helps users know what to collect. It is especially important when some high-value sources require manual download, login access, or human judgment.

### Research Coverage Checklist

Definition: a visible checklist of research areas that have been covered, are missing, or need follow-up.

The Research Coverage Checklist helps users and AI maintain shared context across iterative research. It should not be hidden inside prompts or model memory.

### Insight Card

Definition: a structured unit of research insight.

An Insight Card may include a claim, supporting evidence, source links, confidence level, tags, and related analysis actions.

Insight Cards should be editable and reviewable. They are not final conclusions by default.

### Dashboard

Definition: the main visual summary of a Topic Board.

The dashboard should contain widgets such as executive brief, key facts, trends, players, timeline, risks, opportunities, source coverage, evidence gaps, and suggested next actions.

The initial dashboard is a starting point for research, not the final output.

### Dashboard Widget

Definition: an individual block inside the dashboard.

Examples:

- Executive Brief
- Key Facts
- Major Players
- Timeline
- Risks and Opportunities
- Evidence Gaps
- Suggested Next Analysis

Widgets should eventually be editable, removable, and reorderable.

### Analysis Artifact

Definition: a structured analysis output generated from a Topic Board and its sources.

Examples:

- SWOT
- PEST
- value chain
- competitor comparison
- priority matrix
- maturity assessment
- evidence table

Analysis artifacts should preserve links back to source evidence where possible.

### Output

Definition: a shareable deliverable generated from the research board.

Examples:

- research brief
- interview preparation notes
- report outline
- evidence table

Future outputs may include slide outlines, Markdown export, PDF export, or presentation drafts.

### AI Action

Definition: a specific AI-powered product action attached to a source, insight card, dashboard widget, checklist item, or analysis artifact.

Examples:

- Generate blueprint
- Extract facts
- Find evidence
- Challenge this claim
- Deepen analysis
- Add missing sources
- Build matrix
- Generate brief

AI Actions should feel like product commands, not generic chat prompts.

### AI Side Panel

Definition: a secondary AI interaction surface tied to the current Topic Board.

It can show the active Research View, coverage checklist, suggested next steps, follow-up input, and recent AI actions.

The AI Side Panel should support iterative research without becoming the main product experience.

### Command Bar

Definition: a lightweight way to run direct AI or workspace actions.

Examples:

- `/summarize sources`
- `/find gaps`
- `/build matrix`
- `/generate brief`
- `/compare companies`

The Command Bar is optional for the first prototype but useful as a future interaction pattern.

### Source-grounded Claim

Definition: a claim that is connected to one or more sources, notes, or explicit assumptions.

The product should prefer source-grounded claims over unsupported AI statements.

### Evidence Gap

Definition: a missing source, missing perspective, weakly supported claim, or unresolved contradiction that limits research confidence.

Evidence gaps should be visible and actionable.

### Assumption

Definition: a statement that may be reasonable but is not directly supported by available sources.

Assumptions should be labeled clearly.

### Private Benchmark

Definition: a private research case used locally to evaluate whether the product can produce useful structured outputs.

Private benchmark details should not be included in the public repository.

## 4. Preferred Terms

| Use This | Avoid This | Reason |
| --- | --- | --- |
| Topic Board | Project | Feels lighter and more accessible for general users |
| Research View | Module for user type | Supports multiple goals without splitting users into rigid segments |
| Source Library | File dump | Emphasizes reusable evidence, not storage only |
| Insight Card | AI answer | Makes insight structured, reviewable, and source-linked |
| Research Coverage Checklist | Hidden AI memory | Makes iterative research visible and controllable |
| AI Action | Chat prompt | Positions AI as workflow support |
| Source-grounded claim | AI-generated truth | Avoids overclaiming |
| Evidence gap | Missing data | Broader and more actionable |
| Output | Final report | Keeps MVP flexible and lightweight |

## 5. Public Documentation Rules

Public repository content should:

- use generic or openly available examples
- describe private validation only as a private benchmark
- avoid confidential organization, project, or dataset details
- avoid implying that private materials are stored in the public repository

Public repository content should not include:

- confidential project names
- confidential organization names
- private source documents
- internal research findings from non-public work
- sensitive business context from private work

## 6. UI Copy Rules

### Good UI Copy

- "What do you want to research?"
- "Choose a research goal"
- "Review your research blueprint"
- "Add sources to ground the board"
- "Generate initial dashboard"
- "Review evidence gaps"
- "Deepen this insight"
- "Export brief"

### Copy to Avoid

- "Ask the AI anything"
- "Chat with your research assistant"
- "Generate a perfect report"
- "Automatically research everything"
- "Train your own consulting model"
- "Replace analyst judgment"

## 7. Naming Rules for Future Work

Use consistent object names in product, design, and code:

- `Topic`
- `TopicBoard`
- `ResearchGoal`
- `ResearchView`
- `Source`
- `SourceChecklistItem`
- `ResearchCoverageItem`
- `InsightCard`
- `DashboardWidget`
- `AnalysisArtifact`
- `Output`
- `AIAction`

These names may evolve during implementation, but changes should be intentional and reflected in this glossary.
