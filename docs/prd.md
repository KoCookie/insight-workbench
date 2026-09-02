# Product Requirements Document

## 1. Objective

This PRD defines the first MVP release of Insight Workbench: a topic-based AI research workspace that helps users turn scattered sources into a structured research dashboard and analysis outputs.

The MVP should prove that users can move from a broad research topic to a useful, editable, source-grounded research board without relying on a one-off chat conversation.

## 2. MVP User Segment

The MVP focuses on people who need to quickly understand an industry, company, market, policy, or business topic from scattered sources.

Primary MVP users include:

- students and job seekers preparing for interviews, coursework, or applications
- early-career professionals doing industry, company, or trend research
- operators, marketers, sales teams, product managers, legal professionals, media workers, and creators who need a structured view of a new field
- analysts who need to turn source materials into a brief, evidence table, or initial dashboard

Professional consulting workflows will be supported through deeper analysis features, but they should not make the first-time user experience feel heavy. The same topic board should serve both casual research and advanced analysis through progressive depth.

## 3. User Problem

Users are not short of information sources. They often use social platforms, search engines, policy websites, company databases, recruiting platforms, news, video platforms, reports, and AI tools. The problem is that these sources are fragmented, inconsistent, and difficult to turn into a structured view.

Key pain points:

- **Information is scattered.** Users need to jump across files, websites, social posts, videos, reports, policies, and company pages.
- **Source quality is uneven.** Public opinions can conflict sharply, and users need help distinguishing facts, claims, sentiment, and evidence.
- **High-value sources may still require manual collection.** Some reports, filings, social discussions, platform content, and first-hand notes may not be reliably accessible through automation. Insight Workbench should guide users toward these sources, track whether they have been collected, and turn them into structured research assets once provided.
- **Research lacks structure.** Users may collect many links but still struggle to form a coherent view of market structure, trends, players, risks, and opportunities.
- **Updates are hard to maintain.** New events, policies, financial reports, hiring trends, and public discussions can change the research picture over time.

The product should reduce research effort in two ways:

1. **Assist with accessible public sources where possible.** For sources that are public, stable, and technically accessible, the product should help users discover, collect, and summarize relevant materials with minimal manual effort.
2. **Guide users toward hard-to-access or high-value sources.** For sources that require login, manual download, platform access, or human judgment, the product should provide a clear source checklist and explain why each missing source matters.

The product's value is not limited to summarization. It should help users know what to look for, what they are missing, how different sources conflict, and how to turn scattered materials into a structured research board.

## 4. Core User Flow

```text
Enter research topic
-> Choose research goal
-> Review AI-generated research blueprint
-> Add or confirm sources
-> Generate initial dashboard
-> Review gaps and follow-up questions
-> Iterate with AI and source checklist
-> Deepen analysis
-> Export outputs
```

The flow should not be treated as a single input-output sequence. The initial dashboard is a starting point for an iterative research process. Users should be able to add more sources, ask follow-up questions, revisit missing perspectives, and generate deeper analysis artifacts without losing the topic context.

## 5. Product Structure

The product should organize work around a `Topic Board`.

See [Information Architecture](information-architecture.md) for the detailed navigation model and page structure.

```text
Topic Board
-> Sources
-> Insight Cards
-> Research Coverage Checklist
-> Research Views
   -> Overview
   -> Job or Interview Prep
   -> Company Research
   -> Competitor Analysis
   -> Market Monitoring
   -> Consulting-style Analysis
   -> Content Research
-> Outputs
```

A topic board can support multiple research goals through multiple `Research Views`. These views should share the same source library and insight cards, so users do not need to create separate projects for every goal.

The first goal selected by the user becomes the primary view. Additional views can be added later.

## 6. Key Screens

### 6.1 Home

Purpose: provide a simple entry point.

Primary action:

- "What do you want to research?"

Inputs:

- Topic, company, industry, policy, technology, or business question

Outputs:

- A draft topic title
- Topic classification
- Suggested research goal options
- Example topics to reduce blank-page friction

Examples:

- "AI transformation in a traditional industry"
- "New energy vehicle industry"
- "Xiaohongshu business model"
- "Semiconductor supply chain"

Acceptance criteria:

- A user can start a topic from one short text input.
- The page should not require users to understand consulting frameworks before starting.
- Example prompts should show that the product supports industries, companies, policies, technologies, and broad business questions.
- The system should identify whether the input fits the supported research scope.

Topic classification categories:

- Industry or market
- Company or organization
- Policy or regulation
- Technology or trend
- Competitor or product
- Content research topic
- General factual question
- Unsupported, too broad, or unclear

If the input looks like a general factual question, the product should explain that Insight Workbench is optimized for structured industry, company, market, policy, and topic research. It may offer to continue as a lightweight brief or help the user reframe the input as a supported research topic.

### 6.2 Goal Selection

Purpose: adapt the research board to the user's goal.

Goal options:

- Quick industry overview
- Job or interview preparation
- Company research
- Competitor analysis
- Consulting-style analysis
- Coursework or academic research
- Investment or market monitoring
- Content research for writing, video, or media production

Outputs:

- Selected research goal
- Goal-specific dashboard template
- Goal-specific source checklist
- Primary research view

Acceptance criteria:

- The selected goal changes the recommended modules and sources.
- Users can continue with a default goal if they are unsure.
- The goal selection should feel like choosing a research mode, not filling out a long form.
- Users can add additional research views later without duplicating the topic board.

### 6.3 Research Blueprint

Purpose: show the user how the topic will be researched before building the board.

AI-generated content:

- Suggested dashboard modules
- Key research questions
- Recommended source categories
- Suggested analysis frameworks
- Update frequency recommendation
- Initial research coverage checklist

User actions:

- Confirm blueprint
- Edit focus areas
- Remove or add modules
- Continue without changes

This should be a lightweight confirmation step, not a heavy configuration screen.

Acceptance criteria:

- The blueprint gives users a clear research direction before they collect sources.
- Users can confirm the blueprint without editing.
- Users can remove irrelevant modules or add missing focus areas.
- The blueprint should make the next step obvious: source collection.
- The blueprint should preserve unfinished research areas so users and AI can return to them later.

### 6.4 Sources

Purpose: help users collect and manage evidence.

Source input methods:

- Upload local files
- Paste links
- Add manual notes
- Use AI-recommended source checklist

MVP source checklist categories:

- Official websites
- Company reports
- Regulatory or policy sources
- Industry associations
- Consulting or research reports
- News sources
- Competitor websites
- Company databases
- Recruiting or job market sources
- Social or community discussions
- Video or article references
- User notes and first-hand observations

AI actions:

- Extract facts
- Extract entities
- Extract timelines
- Extract claims
- Separate facts, opinions, and sentiment
- Identify evidence gaps
- Suggest missing source categories
- Flag unsupported or low-confidence claims

Acceptance criteria:

- A user can add at least one source manually.
- A user can paste links or add notes even when file upload is unavailable.
- The page shows which recommended source categories are covered and which are missing.
- AI extraction should create draft facts and insight cards that users can review.

### 6.5 Workspace Dashboard

Purpose: provide the main research board.

Default widgets:

- Executive brief
- Key facts
- Source coverage
- Key trends
- Major players
- Timeline
- Risks and opportunities
- Evidence gaps
- Suggested next analysis
- Research coverage checklist

Widgets should be editable, removable, and reorderable in future versions.

Acceptance criteria:

- The dashboard should be useful even if the user stops here.
- Every major claim should show supporting sources or be marked as an inference.
- The dashboard should highlight missing evidence instead of hiding uncertainty.
- Users should be able to continue from the dashboard into deeper analysis.
- The dashboard should show unfinished research areas so users can continue iterating.

### 6.6 Analysis Lab

Purpose: support deeper structured analysis.

Initial analysis tools:

- PEST
- SWOT
- Value chain
- Competitor comparison
- Priority matrix
- Maturity assessment
- Timeline
- Evidence table

Future analysis tools:

- Technology-to-scenario matrix
- Three Horizons roadmap
- Issue tree
- Market map
- Similarity analysis
- Scenario ranking model

Acceptance criteria:

- Analysis artifacts should be generated from the topic board and sources, not from an isolated prompt.
- Users should be able to edit generated frameworks or matrices.
- AI-generated analysis should preserve links back to source evidence where possible.
- Deep analysis begins when a user selects a specific analysis action from a dashboard widget, checklist item, source, or insight card.

Examples of deep analysis triggers:

- Explore this gap
- Build SWOT
- Compare companies
- Analyze policy impact
- Create value chain
- Investigate opposing views
- Build priority matrix
- Deepen this insight

### 6.7 Outputs

Purpose: turn research assets into shareable deliverables.

Initial outputs:

- Research brief
- Interview preparation notes
- Report outline
- Evidence table

Future outputs:

- Slide outline
- Markdown export
- PDF export
- PPT draft

Acceptance criteria:

- Users can generate a concise research brief from the current board.
- Outputs should preserve source references where possible.
- The MVP should support useful text outputs before attempting full slide or PDF generation.

## 7. Research Coverage Checklist

The research coverage checklist is a visible coordination layer between the user and AI. It should help the product avoid relying only on hidden prompts or model memory.

The checklist should track which research areas have been covered, which are missing, and which need follow-up.

Example checklist areas for an industry or market topic:

- Market size and growth
- Policy or regulatory context
- Competitive landscape
- Value chain or ecosystem
- Key companies or players
- Customer, demand, or user behavior
- Risks and constraints
- International or comparative perspective
- Opposing views or negative signals
- Primary or authoritative sources

Acceptance criteria:

- The checklist should be generated during blueprint creation.
- Users can mark items as covered, skipped, or needs follow-up.
- AI can use the checklist to recommend next steps.
- The checklist should persist across follow-up AI interactions and research views.

## 8. AI Interaction Model

Users should be able to interact with AI without turning the product into a chat-first interface.

The MVP should support three AI interaction patterns:

### 8.1 Contextual AI Actions

AI actions should appear near sources, insight cards, dashboard widgets, and analysis artifacts.

Examples:

- Find evidence
- Explain this
- Challenge this claim
- Deepen analysis
- Add missing sources
- Rewrite for brief
- Compare with another source

### 8.2 AI Side Panel

The AI side panel should act as a research assistant tied to the current topic board.

It may show:

- Current research goal
- Active research view
- Coverage checklist
- Suggested next steps
- Follow-up input box
- Recent AI actions

### 8.3 Command Bar

A lightweight command bar can support direct actions without making chat the main interface.

Examples:

- `/summarize sources`
- `/find gaps`
- `/build matrix`
- `/generate brief`
- `/compare companies`

## 9. AI Requirements

AI should appear as embedded actions:

- Generate blueprint
- Recommend sources
- Extract facts
- Create insight cards
- Find evidence
- Challenge this claim
- Build matrix
- Update dashboard
- Generate report brief

AI chat may exist as a secondary command interface, but the MVP should not be centered around chat.

The MVP assumes integration with existing AI models and workflow-level configuration. It does not require training a new domain-specific foundation model.

AI behavior requirements:

- AI should guide users toward useful source categories and research questions.
- AI should recommend what to look for next, not only summarize materials already provided.
- AI should explain why missing source categories matter for the user's research goal.
- AI should use the research coverage checklist to maintain visible context across iterative exploration.
- AI should organize source material into facts, claims, entities, timelines, and insight cards.
- AI should synthesize across sources, but it should show uncertainty when evidence is weak.
- AI should separate source-grounded statements from assumptions or inferred conclusions.
- AI should help users identify missing perspectives, such as policy context, company filings, international sources, or opposing viewpoints.
- AI should not fabricate sources or imply access to materials that were not provided or connected.
- AI should not make the product feel like a generic chatbot with a dashboard skin.

## 10. MVP Scope

### In Scope

- Topic creation
- Topic classification
- Goal selection
- Multiple research views under one topic board
- AI-generated research blueprint
- AI-assisted discovery of accessible public source categories
- Source upload and link collection
- Source checklist
- Research coverage checklist
- Fact and insight extraction
- Initial dashboard generation
- Basic analysis tools
- Research brief output
- Private benchmark research dataset
- Source coverage and evidence gap indicators

### Out of Scope for MVP

- Fully automated web crawling
- Guaranteed access to closed, login-gated, paywalled, or platform-restricted sources
- Paid subscription integrations
- Multi-user collaboration
- Full version control
- Automatic slide deck generation
- Real-time monitoring infrastructure
- Enterprise permission management
- Public community posting or expert contribution system
- Training a new AI model
- Full replacement for professional research judgment
- Universal general-purpose question answering

## 11. Initial Data Objects

Product terms should follow [Glossary and Product Language Rules](glossary.md).

### Topic

- id
- title
- research_goal
- created_at
- updated_at
- status
- topic_type
- source_coverage_summary

### Source

- id
- topic_id
- title
- type
- url_or_file_path
- source_date
- reliability_level
- tags
- source_category
- extraction_status

### Insight Card

- id
- topic_id
- title
- claim
- supporting_evidence
- source_ids
- confidence_level
- tags
- insight_type

### Dashboard Widget

- id
- topic_id
- type
- title
- content
- source_ids
- order

### Analysis Artifact

- id
- topic_id
- type
- title
- content
- source_ids
- created_at

### Research View

- id
- topic_id
- view_type
- title
- goal
- dashboard_template
- created_at

### Source Checklist Item

- id
- topic_id
- category
- recommendation
- status
- source_ids

### Research Coverage Item

- id
- topic_id
- view_id
- area
- status
- related_source_ids
- related_insight_ids

## 12. Failure and Edge States

The MVP should handle common research workflow failures:

- **No sources added:** show a lightweight starter dashboard and a clear source checklist.
- **Weak source coverage:** mark conclusions as low-confidence and suggest missing source categories.
- **Contradictory sources:** show competing claims instead of forcing one conclusion.
- **Unsupported AI output:** label it as an assumption or ask the user for supporting material.
- **Extraction failure:** keep the source in the library and allow retry or manual notes.
- **Unsupported topic:** explain the product's research scope and suggest a supported reframing.
- **Overly broad topic:** generate a broad overview but recommend narrower research views or follow-up questions.

## 13. Success Metrics

MVP success should be evaluated by whether users can move from a broad research topic to a useful, editable, source-grounded research board faster and more clearly than they could with manual note-taking or one-off AI chat.

Primary MVP metrics:

- Time to useful research board
- First core flow completion rate
- Dashboard usefulness rating
- Percentage of major claims linked to sources, notes, or explicit assumptions
- Number and quality of useful research gaps identified
- Percentage of users who continue from the dashboard into at least one follow-up action

See [MVP Success Metrics](success-metrics.md) for detailed metric definitions, validation questions, failure signals, and metrics that should not drive the first MVP.

## 14. Open Questions

- Should the first prototype be a local demo or a deployed web app?
- What AI model and retrieval architecture should be used?
- How should source reliability be scored?
- How much editing flexibility should dashboard widgets support in the first version?
- Should the first version include authentication or stay single-user?
- How should social or community sources be represented without over-weighting low-quality opinions?
- What is the minimum useful version of source coverage scoring?
- How much of topic classification should happen before board creation versus after the initial blueprint?
- Should research views be visible as tabs, sidebar items, or dashboard modes?
