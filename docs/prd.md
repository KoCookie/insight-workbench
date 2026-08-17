# Product Requirements Document Draft

## 1. Objective

Build an MVP for Insight Workbench: a topic-based AI research workspace that helps users turn scattered sources into a structured research dashboard and analysis outputs.

## 2. MVP User Segment

The MVP focuses on students, interns, junior analysts, and job seekers who need to quickly understand an industry, company, or business topic.

Professional consulting workflows will be supported through deeper analysis features, but they should not make the first-time user experience feel heavy.

## 3. Core User Flow

```text
Enter research topic
-> Choose research goal
-> Review AI-generated research blueprint
-> Add sources
-> Generate initial dashboard
-> Deepen analysis
-> Export outputs
```

## 4. Key Screens

### 4.1 Home

Purpose: provide a simple entry point.

Primary action:

- "What do you want to research?"

Inputs:

- Topic, company, industry, policy, technology, or business question

Examples:

- "AI transformation in a traditional industry"
- "New energy vehicle industry"
- "Xiaohongshu business model"
- "Semiconductor supply chain"

### 4.2 Goal Selection

Purpose: adapt the research board to the user's goal.

Goal options:

- Quick industry overview
- Job or interview preparation
- Company research
- Competitor analysis
- Consulting-style analysis
- Coursework or academic research

### 4.3 Research Blueprint

Purpose: show the user how the topic will be researched before building the board.

AI-generated content:

- Suggested dashboard modules
- Key research questions
- Recommended source categories
- Suggested analysis frameworks
- Update frequency recommendation

User actions:

- Confirm blueprint
- Edit focus areas
- Remove or add modules
- Continue without changes

This should be a lightweight confirmation step, not a heavy configuration screen.

### 4.4 Sources

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

AI actions:

- Extract facts
- Extract entities
- Extract timelines
- Extract claims
- Identify evidence gaps
- Suggest missing source categories

### 4.5 Workspace Dashboard

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

Widgets should be editable, removable, and reorderable in future versions.

### 4.6 Analysis Lab

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

### 4.7 Outputs

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

## 5. AI Intervention Points

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

## 6. MVP Scope

### In Scope

- Topic creation
- Goal selection
- AI-generated research blueprint
- Source upload and link collection
- Source checklist
- Fact and insight extraction
- Initial dashboard generation
- Basic analysis tools
- Research brief output
- Private benchmark research dataset

### Out of Scope for MVP

- Fully automated web crawling
- Paid subscription integrations
- Multi-user collaboration
- Full version control
- Automatic slide deck generation
- Real-time monitoring infrastructure
- Enterprise permission management

## 7. Initial Data Objects

### Topic

- id
- title
- research_goal
- created_at
- updated_at
- status

### Source

- id
- topic_id
- title
- type
- url_or_file_path
- source_date
- reliability_level
- tags

### Insight Card

- id
- topic_id
- title
- claim
- supporting_evidence
- source_ids
- confidence_level
- tags

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

## 8. Success Metrics

MVP success should be evaluated by:

- Time from topic creation to usable dashboard
- Number of useful insight cards generated per source
- User rating of dashboard usefulness
- Percentage of claims linked to sources
- Ability to reproduce a meaningful structured analysis from existing benchmark materials

## 9. Open Questions

- Should the first prototype be a local demo or a deployed web app?
- What AI model and retrieval architecture should be used?
- How should source reliability be scored?
- How much editing flexibility should dashboard widgets support in the first version?
- Should the first version include authentication or stay single-user?
