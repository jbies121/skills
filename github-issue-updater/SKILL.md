---
name: github-issue-updater
description: Link development to GitHub issues, post commit updates, and close issues on completion.
compatibility: opencode
---

## What I do
1. **Context Mapping**: I automatically identify the relevant GitHub issue by checking the current branch name (e.g., `feature/123-auth`) or searching `gh issue list`.
2. **User Confirmation**: Before I begin tracking, I will ask you: "I've linked this task to issue #<ID>. Would you like me to post updates to it when I commit and close it once the task is fully finished?"
3. **Progress Updates**: After every successful commit, I post a comment to the issue using:
   `gh issue comment <ID> --body "[hash] - [commit message]"`
4. **Lifecycle Management**: When the high-level task is complete and all requirements are met, I close the issue with:
   `gh issue close <ID> --reason "completed" --comment "Closed by agent after task completion."`

## When to use me
Use me whenever you are working on a project with an active GitHub issue tracker. I help keep the issue history in sync with the actual code changes without manual intervention.
