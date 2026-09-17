# Sprint 1 Task List

Complete tasks in order. One task is one commit. F = frontend, B = backend, D = data, P = process.

## Stage 0 — Start

1. **P-01: Set up Git and project copy.** Fork, clone, make a branch, and make an initial commit. Commit to: repository root and your `work/student-*/sprint1/` folder.
2. **P-02: Explain the web path.** Write a short note showing client → server → database → response. Commit to: `work/student-*/sprint1/README.md`.

## Stage 1 — Static frontend

3. **F-01: Build the poll page.** Add the question, option list area, vote buttons, add-option form, total area, and result-bar area using HTML. Commit to: your Sprint 1 frontend folder.
4. **F-02: Style the readable page.** Add CSS for options, buttons, feedback, and empty result bars. Commit to: your Sprint 1 frontend folder.
5. **F-03: Render hardcoded options.** Store label and vote data in JavaScript and render it into the page. Commit to: your Sprint 1 frontend folder.
6. **F-04: Vote in memory.** Handle a button click, increase the hardcoded vote count, and redraw the page. Commit to: your Sprint 1 frontend folder. **Checkpoint:** refresh resets data, but voting updates the UI.

## Stage 2 — Backend

7. **B-01: Create the Node project.** Create `package.json`, install Express, and add a server start command. Commit to: your Sprint 1 backend folder.
8. **B-02: Add GET options route.** Start Express and return temporary option data from `GET /options`. Commit to: your Sprint 1 backend folder.

## Stage 3 — Persistence

9. **D-01: Create options table.** Create `options` with `id`, `label`, and `votes`; add a few starting rows. Commit to: your Sprint 1 database folder.
10. **D-02: Write SELECT query.** Select all option rows and sort by vote count descending. Commit to: your Sprint 1 database folder.
11. **B-03: Connect GET route to SQL.** Use `mysql2` so `GET /options` returns database rows. Commit to: backend and database folders. **Milestone:** the option list loads from MySQL.

## Stage 4 — Voting

12. **D-03: Write vote UPDATE.** Update an option with `votes = votes + 1`. Commit to: database folder.
13. **B-04: Add vote route.** Create `PUT /options/:id/vote` and run the update safely for that ID. Commit to: backend folder.
14. **F-05: Send vote request.** Use `fetch` with PUT, then refresh displayed options. Commit to: frontend folder. **Checkpoint:** a click updates MySQL and the UI.

## Stage 5 — Options

15. **D-04: Add INSERT and duplicate check.** Check label first, then insert only a new label. Commit to: database folder.
16. **B-05: Add POST options route.** Receive the form label, block duplicates, and return useful feedback. Commit to: backend folder.
17. **F-06: Submit new option.** Use a form and POST fetch request, then redraw results. Commit to: frontend folder.
18. **D-05: Write DELETE query.** Delete an option by ID. Commit to: database folder.
19. **B-06: Add DELETE options route.** Delete the selected option through `DELETE /options/:id`. Commit to: backend folder.
20. **F-07: Wire delete control.** Send the delete request and refresh the list. Commit to: frontend folder.

## Stage 6 — Product finish

21. **F-08: Show result bars and total.** Calculate vote shares for CSS widths and display total votes. Commit to: frontend folder.
22. **F-09: Polish duplicate feedback.** Present the duplicate error clearly after a failed add request. Commit to: frontend folder.

## Stages 7–9 — Honest finishing

23. **F-10: Add localStorage vote flag.** Stop a second accidental vote in the same browser and explain it is not security. Commit to: frontend folder.
24. **F-11: Auto-refresh results.** Use `setInterval` to re-fetch options every few seconds; label this as polling, not true real-time. Commit to: frontend folder.
25. **F-12: Add loading and error states.** Handle slow and failed fetch requests visibly. Commit to: frontend folder.
26. **P-03: Document and push.** Write the app README with setup, run steps, and stack; make final commits and push. Commit to: your Sprint 1 README.
27. **P-04: Sprint 1 demo.** Demonstrate browser → Express route → SQL → MySQL → response → UI. Commit to: demo notes if used. **Milestone: Sprint 1 demo.**