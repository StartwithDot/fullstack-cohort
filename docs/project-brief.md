# Poll Maker: Sprint 1 Project Brief

## What we are building

Poll Maker is one shared poll with one hardcoded question and answer options. Anyone can view results, vote, add an option, or delete an option. The browser shows vote totals, vote-share bars, and highest-voted options first.

The project lets us follow one action end to end: browser → server → database → response → updated page. See [glossary.md](glossary.md) for these terms.

## Why

A vote is a meaningful update: it must survive a refresh and server restart. This introduces create, read, update, and delete (CRUD) in a small, demonstrable application.

## Required features

1. Show the question, every option, and current vote counts.
2. Vote and show the new result immediately.
3. Add and delete options.
4. Reject duplicate labels with helpful feedback.
5. Show vote shares as CSS bars and show total votes.
6. Sort options highest vote count first.
7. Use a `localStorage` flag to discourage a second vote from one browser.
8. Re-fetch results every few seconds.

## Locked stack

| Layer | Technology | Use |
| --- | --- | --- |
| Frontend | HTML, CSS, vanilla JavaScript | Page, clicks, and DOM updates. |
| Backend | Node.js + Express | Routes for options and votes. |
| Database | MySQL + raw SQL through `mysql2` | Save labels and vote counts. |
| Process | Git + GitHub | One task per commit and review. |

The only table is `options`: `id` (auto-increment primary key), `label` (option text), and `votes` (integer starting at 0). There is no `polls` table; there is one global poll and its question is hardcoded in the frontend.

## Out of scope

Multiple polls require a second table and a relationship, so they are excluded. The localStorage vote check is cosmetic: private browsing or cleared storage bypasses it; real enforcement needs authentication, deferred beyond this sprint. Auto-refresh is polling, not true real-time WebSockets. React, MongoDB, authentication, testing frameworks, TypeScript, styling frameworks, and ORMs are not in Sprint 1.

Build in the order in [task-list.md](task-list.md).