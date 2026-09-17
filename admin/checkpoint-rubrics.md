# Sprint 1 Checkpoint Rubrics

Use this checklist alongside [docs/task-list.md](../docs/task-list.md). Mark each item as demonstrated, needs revision, or not yet attempted.

## Stage 0 — Start

- [ ] Student can describe client, server, request, and response for Poll Maker.
- [ ] Student has a fork, clone, branch, and task-sized commit.

## Stage 1 — Static frontend

- [ ] Page shows question, options, controls, and result areas.
- [ ] Hardcoded JavaScript data renders into the page.
- [ ] A vote click updates the in-memory UI.
- [ ] Student explains why refresh resets this version.

## Stage 2 — Backend

- [ ] Node project starts successfully.
- [ ] Express `GET /options` returns temporary option data.

## Stage 3 — Persistence

- [ ] `options` table has `id`, `label`, and `votes`.
- [ ] Student can explain a row, column, and primary key.
- [ ] `GET /options` uses SQL SELECT and returns database rows. **Milestone**

## Stage 4 — Voting

- [ ] SQL update increases the selected option's votes.
- [ ] PUT route receives an option ID and updates its row.
- [ ] Frontend fetch updates the database and the UI.

## Stage 5 — Options

- [ ] POST adds a non-duplicate option.
- [ ] Duplicate labels are blocked.
- [ ] DELETE removes an option from MySQL and the UI.

## Stage 6 — Product finish

- [ ] Results sort highest votes first.
- [ ] Total votes and CSS vote-share bars are accurate.
- [ ] Duplicate feedback is clear.

## Stages 7–9 — Honest finishing

- [ ] localStorage blocks an accidental repeat vote in one browser.
- [ ] Student explains why this is not real security.
- [ ] Auto-refresh re-fetches results and student explains polling is not true real-time.
- [ ] Loading and failed-request states are visible.
- [ ] README gives setup and run steps.
- [ ] Student demo traces browser → Express route → SQL → MySQL → response → UI. **Milestone**

## End-of-sprint outcomes

- [ ] Student explains what happens when someone clicks Vote, layer by layer.
- [ ] Student explains why browser-only data is not permanent.
- [ ] Student can rebuild one layer—frontend, backend, or database—from scratch when asked.