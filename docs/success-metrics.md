# MVP Success Metrics

## 1. Purpose

This document defines how Insight Workbench will evaluate whether the MVP is valuable enough to continue building.

The goal is not to prove that the product is complete. The goal is to prove that a user can move from a broad research topic to a structured, editable, source-grounded research board faster and more clearly than they could with manual note-taking or one-off AI chat.

## 2. North Star Metric

**Time to useful research board**

Definition: the time it takes for a user to create a topic, choose a goal, add or confirm sources, and reach a dashboard that they consider useful for understanding the topic or deciding what to research next.

Why this matters:

- It captures the product's core promise: turning scattered information into structured understanding.
- It keeps the MVP focused on workflow value, not feature volume.
- It can be tested with both casual and more advanced research tasks.

Target for MVP validation:

- A first-time user should be able to reach a useful initial board within 10-15 minutes when using a small source set.
- A user should be able to explain what the board helped them understand and what they should investigate next.

## 3. Primary Success Metrics

### 3.1 Activation

Metric: percentage of users who complete the first core flow.

Core flow:

```text
Create topic
-> Choose research goal
-> Review blueprint
-> Add or confirm at least one source
-> Generate initial dashboard
```

MVP success signal:

- Users can complete the flow without needing additional explanation.
- Users do not abandon the product before source collection or dashboard generation.

### 3.2 Dashboard Usefulness

Metric: user rating of the initial dashboard's usefulness.

Suggested rating question:

> How useful is this dashboard for understanding the topic or deciding what to research next?

Suggested scale:

- 1: Not useful
- 2: Slightly useful
- 3: Somewhat useful
- 4: Useful
- 5: Very useful

MVP success signal:

- Most tested users rate the initial dashboard 4 or above.
- Users can point to specific widgets, insight cards, or gap indicators that helped them.

### 3.3 Source-grounding Quality

Metric: percentage of major claims linked to sources, notes, or explicit assumptions.

MVP success signal:

- Important claims in the dashboard are not presented as unsupported conclusions.
- Users can see which claims are source-grounded and which are inferred.
- Unsupported or weakly supported claims are clearly marked.

### 3.4 Research Coverage

Metric: number and quality of useful research gaps identified by the product.

MVP success signal:

- The product identifies missing source categories or missing research perspectives that users recognize as relevant.
- Users act on at least one suggested follow-up from the research coverage checklist.
- The checklist helps users continue research instead of treating the first AI output as final.

### 3.5 Iteration Depth

Metric: percentage of users who continue from the initial dashboard into at least one follow-up action.

Follow-up actions include:

- Adding another source
- Opening a missing coverage item
- Asking a follow-up question through the AI side panel
- Running a contextual AI action
- Creating an analysis artifact
- Exporting a brief

MVP success signal:

- Users naturally continue from the dashboard into at least one deeper step.
- Users understand that the dashboard is a research starting point, not a one-shot final answer.

## 4. Secondary Success Metrics

### 4.1 Source-to-insight Conversion

Metric: number of useful insight cards generated per source.

MVP success signal:

- Uploaded or linked sources produce reviewable facts, claims, entities, timelines, or insight cards.
- Users can edit or reject generated cards without breaking the workflow.

### 4.2 Output Usefulness

Metric: usefulness of generated research briefs or evidence tables.

MVP success signal:

- Users can reuse the generated brief as a starting point for study, work, writing, analysis, or presentation preparation.
- Outputs preserve source references where possible.

### 4.3 Reframing Quality

Metric: quality of the product's response when a topic is too broad, unsupported, or closer to a general factual question.

MVP success signal:

- The product explains its research scope clearly.
- The product helps users reframe vague inputs into useful research topics.
- Users do not feel blocked when their first input is imperfect.

## 5. Qualitative Validation Questions

During user testing or self-evaluation, ask:

- What did the board help you understand faster?
- Which part felt more useful than asking a generic AI chatbot?
- Which source categories did you realize you were missing?
- Which dashboard widget or insight card was most useful?
- Which AI action felt like a real workflow improvement?
- What still felt manual, repetitive, or unclear?
- Would you use this again for another industry, company, or topic?

## 6. Failure Signals

The MVP is not working well if:

- Users treat the product as just another AI chat page.
- Users cannot tell what to do after the initial dashboard appears.
- Users do not trust the dashboard because claims are not source-grounded.
- Users feel that manual source collection makes the product not worth using.
- Users cannot distinguish facts, opinions, assumptions, and conflicting claims.
- The source checklist feels generic and does not help users collect better materials.
- The AI side panel answers questions but does not help users move the research forward.

## 7. Metrics Not Prioritized in MVP

These metrics may matter later, but they should not drive the first MVP:

- Total registered users
- Daily active users
- Team collaboration frequency
- Long-term retention
- Revenue
- Enterprise adoption
- Number of supported integrations
- Fully automated source monitoring accuracy
- Public community contribution volume

The MVP should prioritize research workflow quality over growth or monetization metrics.

## 8. Validation Method

MVP validation should use small, concrete research tasks.

Suggested validation setup:

1. Choose a research topic.
2. Prepare a small source set with 3-5 materials.
3. Ask the user to create a topic board and generate an initial dashboard.
4. Observe whether the user understands the flow without extra explanation.
5. Ask the user to rate dashboard usefulness.
6. Check whether major claims are linked to sources or marked as assumptions.
7. Ask the user to continue with one follow-up action.
8. Record what was useful, missing, confusing, or still too manual.

The first benchmark can use a private research project kept outside the public repository. Public validation examples should use generic or openly available materials.
