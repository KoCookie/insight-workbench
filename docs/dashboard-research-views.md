# Dashboard and Research View Requirements

## 1. Purpose

This document defines the required structure for the Topic Board dashboard and Research Views before visual wireframing begins.

The goal is to make the dashboard useful as both an initial research summary and a launch point for deeper analysis.

## 2. Product Intent

The dashboard should help users answer:

- What is the current understanding of this topic?
- Which claims are supported by sources?
- What is missing or uncertain?
- What should I investigate next?
- Which Research View am I working in?

Research Views should help users apply different lenses to the same Topic Board without duplicating sources.

## 3. Dashboard Structure

Recommended dashboard regions:

```text
Topic header
-> Research View selector
-> Source and coverage summary
-> Main dashboard widgets
-> Evidence gaps and next steps
-> Contextual AI actions
```

## 4. Topic Header

Purpose: orient the user.

Required elements:

- Topic title
- Topic type
- Primary research goal
- Source coverage summary
- Last updated timestamp
- Main action button

Possible main actions:

- Add source
- Generate dashboard
- Update dashboard
- Export brief

## 5. Research View Selector

Purpose: let users switch the lens without creating separate boards.

Recommended display options:

- tabs
- segmented control
- compact dropdown

MVP recommendation:

- Use tabs or segmented controls when there are few views.
- Use a dropdown later when users can create many custom views.

Default views:

- Overview
- Primary selected goal

Additional views can be added later from inside the Topic Board.

## 6. Default Dashboard Widgets

Required MVP widgets:

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

Each widget should define:

- purpose
- input sources
- output content
- evidence links
- confidence state
- available AI actions

## 7. Goal-specific Widget Behavior

Research Views should change widget emphasis.

### 7.1 Overview

Focus:

- broad topic understanding
- key facts
- trends
- players
- risks
- evidence gaps

### 7.2 Job or Interview Prep

Focus:

- industry basics
- company context
- role-relevant trends
- interview talking points
- questions to ask

### 7.3 Company Research

Focus:

- business model
- products or services
- market position
- recent events
- risks and opportunities

### 7.4 Competitor Analysis

Focus:

- comparable players
- positioning
- strengths and weaknesses
- market map
- comparison table

### 7.5 Market Monitoring

Focus:

- recent updates
- policy changes
- market signals
- weak evidence
- follow-up sources

### 7.6 Consulting-style Analysis

Focus:

- structured frameworks
- issue decomposition
- value chain
- priority matrix
- evidence table

### 7.7 Content Research

Focus:

- audience questions
- explainable background
- key narratives
- opposing views
- source-backed talking points

## 8. Contextual AI Actions

AI actions should appear on widgets, insight cards, sources, coverage items, and outputs.

Recommended actions:

- Find evidence
- Explain this
- Challenge this claim
- Deepen analysis
- Add missing sources
- Rewrite for brief
- Compare with another source
- Generate output

AI actions should be phrased as product commands, not open-ended chat prompts.

## 9. Deep Analysis Entry Points

Users should enter deeper analysis from a clear object or gap.

Valid triggers:

- Click a coverage item
- Click an evidence gap
- Click an insight card
- Click a dashboard widget action
- Choose an analysis action from the Research View

Examples:

- Explore this gap
- Build SWOT
- Compare companies
- Analyze policy impact
- Create value chain
- Investigate opposing views
- Build priority matrix
- Deepen this insight

## 10. Empty, Loading, and Error States

### 10.1 Empty Dashboard

Show:

- starter blueprint summary
- source checklist
- prompt to add first source
- explanation that source-grounded analysis requires sources

### 10.2 Loading State

Show:

- which step is running
- expected output
- ability to continue reviewing sources

### 10.3 Weak Evidence State

Show:

- low-confidence labels
- missing source categories
- suggested next actions

### 10.4 Contradictory Evidence State

Show:

- competing claims
- supporting sources for each claim
- option to investigate contradiction

### 10.5 AI Failure State

Show:

- what failed
- retry option
- manual edit option
- source remains available

## 11. Wireframe Requirements

The future wireframe should show:

- Home to Topic Board transition
- Topic header
- Research View selector
- Dashboard widget grid
- Source coverage summary
- Coverage checklist component
- AI action placement
- Empty and weak-evidence states
- Path from dashboard to analysis and outputs

## 12. MVP Requirements

Required for the first prototype:

- Topic header
- Research View selector
- Dashboard widget grid
- Source coverage summary
- Coverage checklist component
- Contextual AI action buttons
- Evidence gap display

Can be simplified:

- Widgets can use static sample content.
- Research View switching can update visible sections without full data persistence.
- AI actions can be mocked before real AI integration.

Out of scope:

- Fully customizable dashboard layout
- Drag-and-drop widgets
- Complex chart builder
- Multi-user dashboard comments
- Advanced permission states

## 13. Open Questions

- Should dashboard widgets use a masonry grid or fixed sections?
- Should the coverage checklist be a sidebar, widget, or drawer?
- Should Research Views appear above the dashboard or in side navigation?
- Which AI actions should be visible by default versus hidden in a menu?
- How much editing should be supported in the first prototype?
