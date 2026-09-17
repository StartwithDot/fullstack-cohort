# Sprint 1 Delivery Brief: Poll Maker

**Prepared:** Before Sprint 1 begins

## Agreement

Each student will independently deliver Poll Maker: one shared voting poll with a hardcoded question. Users can read options and counts, vote, add and delete options, see total votes and CSS result bars, and see options sorted by votes. The page will re-fetch results every few seconds.

## Technical agreement

The frontend uses HTML, CSS, and vanilla JavaScript. Node.js and Express provide API routes. MySQL stores one `options` table (`id`, `label`, `votes`) through raw SQL using `mysql2`. Work is committed in Git and reviewed through GitHub.

## Acceptance checks

- `GET /options` reads option rows from MySQL.
- A vote uses `PUT /options/:id/vote` and changes the stored count.
- Add and delete controls use server routes and persist after refresh.
- Duplicate labels are blocked.
- Results have total, sorted counts, and vote-share bars.
- A localStorage browser flag prevents accidental repeat votes, with an explicit note that it is not real security.
- Results auto-refresh through polling, with an explicit note that this is not true real-time.

## Boundaries

There are no accounts, multiple polls, React, MongoDB, WebSockets, testing frameworks, TypeScript, styling frameworks, ORMs, or authentication in Sprint 1. See [../docs/project-brief.md](../docs/project-brief.md) for the full scope and [../docs/task-list.md](../docs/task-list.md) for delivery order.