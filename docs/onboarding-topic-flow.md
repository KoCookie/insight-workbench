# Onboarding and Topic Creation Flow

## 1. Purpose

This document defines the first-time user flow from opening Insight Workbench to creating a usable Topic Board.

The goal is to make onboarding lightweight, action-oriented, and useful without turning the product into a generic AI chat page or a long setup form.

## 2. Product Intent

The onboarding flow should help users answer four questions quickly:

1. What do I want to research?
2. Is this a supported research topic?
3. What is my research goal?
4. What should I collect or review next?

The user should feel guided, not tested. The product should provide enough structure to reduce blank-page friction while still allowing users to move forward quickly.

## 3. Flow Overview

```text
Home
-> Enter research topic
-> Topic classification
-> Choose research goal
-> Review research blueprint
-> Create Topic Board
-> Add or confirm sources
```

## 4. Step 1: Home

Purpose: provide a simple entry point for a new user.

Primary prompt:

```text
What do you want to research?
```

Input examples:

- "New energy vehicle industry"
- "Xiaohongshu business model"
- "Semiconductor supply chain"
- "AI transformation in a traditional industry"
- "A company I am interviewing with"

Required UI elements:

- Topic input
- Example prompts
- Recent Topic Boards, if available
- Clear create action

Guidance rule: the page should not explain the whole product. It should help the user start.

## 5. Step 2: Topic Classification

Purpose: determine whether the input fits the product's research scope.

Supported classifications:

- Industry or market
- Company or organization
- Policy or regulation
- Technology or trend
- Competitor or product
- Content research topic

Special classifications:

- General factual question
- Unsupported
- Too broad
- Unclear

Behavior:

- If the topic is supported, continue to goal selection.
- If the topic is too broad, suggest narrower research angles.
- If the topic is unclear, ask for a short clarification.
- If the topic is a general factual question, offer to reframe it into a research topic or continue as a lightweight brief.
- If the topic is unsupported, explain the product scope and suggest a supported format.

Example reframing:

```text
Original input: "Which is healthier, apples or bananas?"
Suggested reframing: "Consumer demand and market trends for healthy fruit snacks"
```

## 6. Step 3: Goal Selection

Purpose: adapt the Topic Board to the user's intent.

Goal options:

- Quick industry overview
- Job or interview preparation
- Company research
- Competitor analysis
- Consulting-style analysis
- Coursework or academic research
- Investment or market monitoring
- Content research for writing, video, or media production

Default behavior:

- If the user is unsure, use `Quick industry overview`.
- The first selected goal becomes the primary Research View.
- Additional Research Views can be added later from inside the Topic Board.

## 7. Step 4: Research Blueprint

Purpose: show the user the initial research plan before source collection.

Blueprint sections:

- Draft topic title
- Topic classification
- Selected research goal
- Suggested dashboard modules
- Key research questions
- Recommended source categories
- Initial Research Coverage Checklist
- Suggested next action

User actions:

- Confirm blueprint
- Edit focus areas
- Remove irrelevant modules
- Add missing modules
- Continue without changes

Design rule: blueprint review should be skimmable. A first-time user should not need to configure every detail.

## 8. Step 5: Create Topic Board

Purpose: convert the topic, goal, and blueprint into a persistent workspace.

Created objects:

- Topic Board
- Primary Research View
- Source Checklist
- Research Coverage Checklist
- Empty or starter Dashboard Widgets

The first Topic Board can be useful even before sources are added, but it should clearly show that source-grounded analysis requires sources.

## 9. First Meaningful User Effort

The first meaningful user effort should be source collection, not product configuration.

The product should guide users toward source collection by showing:

- Recommended source categories
- Why each category matters
- Which categories are already covered
- Which categories are missing
- What the user can add manually
- What the product may assist with automatically later

## 10. New User Guidance Rules

Use guidance that is:

- short
- contextual
- action-oriented
- attached to the current step
- easy to ignore once the user understands the flow

Avoid:

- long tutorials
- generic product tours
- large explanation modals
- "ask AI anything" language
- forcing users to understand consulting frameworks before starting

## 11. Empty and Edge States

### 11.1 Empty Topic Input

Show examples and a short prompt to start with any industry, company, market, policy, or trend.

### 11.2 Too Broad Topic

Allow the user to continue, but suggest narrower Research Views or follow-up angles.

### 11.3 Unsupported Topic

Explain that Insight Workbench is optimized for structured research topics and offer a reframing.

### 11.4 No Sources Yet

Show a starter dashboard with clear source gaps and recommended next steps.

### 11.5 User Skips Blueprint Editing

Allow the user to continue. Editing the blueprint should be optional.

## 12. MVP Requirements

Required for the first prototype:

- Home topic input
- Example prompts
- Topic classification result
- Goal selection
- Research blueprint review
- Create Topic Board action
- Source collection next step

Can be simplified:

- Topic classification can be rule-based or mocked before AI integration.
- Blueprint content can be generated from templates before real AI integration.
- Recent Topic Boards can use mock data.

Out of scope:

- Full account onboarding
- Multi-step profile setup
- Tutorial center
- Personalized onboarding by profession
- Full automatic source collection

## 13. Open Questions

- Should topic classification appear before or after goal selection?
- Should users be allowed to skip goal selection entirely?
- How many example prompts should be shown on Home?
- Should the first prototype include recent Topic Boards or only topic creation?
- Should the blueprint be a full page or an inline step inside topic creation?
