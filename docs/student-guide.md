# Student Git Guide

These are the mechanics for keeping your own Sprint 1 work safe and reviewable.

## Fork and clone

1. On GitHub, open the cohort repository and choose **Fork**. This makes your own GitHub copy.
2. In your fork, choose **Code**, copy the HTTPS address, then in VS Code terminal run:

```bash
git clone PASTE-YOUR-COPIED-ADDRESS-HERE
cd fullstack-cohort
```

## Create a branch

Before one task, make a named work area:

```bash
git switch -c F-01-static-page
```

Use the task ID from [task-list.md](task-list.md). `git switch` changes where your next work is saved.

## Commit

After completing one task, check changed files and save them as a commit:

```bash
git status
git add path/to/changed-file
git commit -m "F-01 build static poll page"
git push -u origin F-01-static-page
```

`git add` chooses changes for the commit. A commit is a saved checkpoint. `git push` sends it to your GitHub fork.

## Open a pull request

1. GitHub shows a **Compare & pull request** button after a push; select it.
2. Title it `TASK-ID: short description`.
3. Describe what works and how to check it.
4. Request a teammate review, respond to comments, then merge without squash-merging.

Return to your main branch only after the pull request is merged:

```bash
git switch main
git pull
```