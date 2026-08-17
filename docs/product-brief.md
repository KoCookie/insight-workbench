# Product Brief

## Product Name

Insight Workbench

## One-line Description

An AI research workspace for turning scattered sources into structured, source-grounded research boards.

## Problem

People often need to understand an industry, company, policy, technology trend, or business question quickly. Their materials are usually scattered across PDFs, reports, websites, notes, news, and internal documents. Existing AI chat tools can summarize information, but they often fail to provide a persistent research structure, source traceability, editable analysis artifacts, and update workflows.

The core problem is not just "answer a question." The core problem is helping users build and maintain a structured understanding of a topic over time.

This creates three recurring pain points:

1. **Research starts from a blank page.** Users often do not know which questions to ask, which sources to collect, or which analysis structure fits the topic.
2. **Sources do not become reusable assets.** Important facts, claims, citations, and data points remain buried inside documents or chat transcripts.
3. **Research outputs are hard to update.** Once a brief or report is written, new information does not naturally flow back into the user's analysis.

## Product Positioning

Insight Workbench is a topic-based AI research workspace.

It should not feel like a wrapped AI chatbot. The user should primarily interact with research boards, source libraries, insight cards, dashboards, matrices, timelines, frameworks, and outputs. AI should operate as an embedded engine that extracts, organizes, challenges, and updates the user's research.

The product should feel lightweight for casual users and progressively deeper for advanced users. A first-time user should be able to create a topic board and get an initial research brief without learning consulting frameworks. A more advanced user should be able to continue into structured analysis, evidence management, and reusable outputs from the same board.

## Target Users

### Primary Users for MVP

- Students preparing for interviews, applications, or coursework
- Interns and junior analysts doing early-stage industry, company, or trend research
- Early-career professionals who need structured research outputs quickly

### Future Users

- Consultants who need reusable research assets and evidence management
- Senior analysts who need project-level source governance and visualization
- Teams that need to track topic updates over time

## Core Use Cases

1. A student wants to understand an industry before applying for jobs.
2. An intern needs to turn a topic into a structured research brief.
3. A junior analyst needs to organize sources, extract facts, and build analysis frameworks.
4. A consultant wants to track evidence, update a research board, and reuse project templates.
5. A user wants to monitor changes in a company, industry, or policy area over time.

## MVP Focus

The MVP should focus on one complete research workflow:

```text
Create topic -> choose research goal -> review blueprint -> add sources -> generate dashboard -> export brief
```

The first version should prove that a user can move from a vague research topic to a structured, editable, source-grounded research board faster than they could with manual note-taking or one-off AI chat.

## Product Principles

### 1. One Topic, Continuous Tracking

The product should frame research as a topic board rather than a heavy project management workflow. Users should feel they are following a topic, not maintaining a complex repository.

### 2. AI as Workflow Engine, Not Main Interface

AI should appear through actions such as extract facts, generate blueprint, find evidence, build matrix, update board, challenge claim, and export brief. A chat assistant can exist, but it should not be the core product surface.

### 3. Progressive Depth

All users start from the same topic board. Casual users can stop at the research brief and dashboard. Advanced users can continue into consulting-style frameworks, evidence systems, and output generation.

### 4. Source-grounded Insight

Every important claim should be traceable to a source, a note, or an explicit AI-generated assumption. The product should help users distinguish evidence, inference, and opinion.

### 5. Editable Analysis Artifacts

Dashboards, matrices, frameworks, timelines, and insight cards should be editable. AI should generate a starting point, not a locked final answer.

### 6. Public-safe by Default

The product and repository should avoid storing sensitive or confidential details in public documentation or sample data. Private benchmark materials can be used locally for validation, but public examples should remain generic or use openly available sources.

## MVP Hypothesis

If users can create a topic, receive an AI-generated research blueprint, add sources with guidance, and receive an editable structured dashboard, they will find the product more valuable than one-off AI chat for research tasks.

## MVP Non-goals

The MVP should not attempt to solve every research workflow at once.

Out of scope for the first version:

- fully automated web crawling or real-time monitoring
- team collaboration and enterprise permissions
- complete report or slide deck generation
- complex version control for every insight
- paid data integrations
- a general-purpose chatbot as the main product interface

## AI Role

The MVP assumes integration with existing AI models and workflow-level configuration, not training a new domain-specific foundation model.

AI should be involved at five moments:

1. Research setup: generate blueprint, key questions, suggested modules, and source checklist.
2. Source ingestion: extract facts, entities, timelines, quotes, data points, and claims.
3. Analysis generation: create briefs, matrices, frameworks, scores, charts, and insight cards.
4. Update monitoring: identify new information and suggest which conclusions may need revision.
5. Output creation: convert the research board into a report, slide outline, interview notes, or executive summary.

## Initial Validation Plan

The first validation case will use a private benchmark research project kept outside the public repository.

The platform should attempt to generate:

- industry brief
- key fact cards
- value chain view
- structured analysis matrix
- maturity or readiness assessment
- priority matrix
- phased roadmap

These outputs will be compared with existing human research deliverables to identify gaps in structure, evidence quality, reasoning, and usability.
