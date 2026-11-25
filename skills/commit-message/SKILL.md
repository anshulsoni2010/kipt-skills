---
name: commit-message
description: Writes a commit message from the staged changes in the
  Conventional Commits style. Use when the user asks to commit, asks for a
  commit message, or says "write the commit".
---

# Commit message

1. Read the staged diff with git diff --staged. If nothing is staged,
   say so and stop.
2. Pick one type: feat, fix, docs, refactor, perf, test, build or chore.
3. Add a scope in parentheses when one area is clearly affected:
   fix(auth): ...
4. Write the subject in the imperative, under 72 characters, no period:
   "fix(cart): handle empty cart totals"
5. If the change is not obvious from the subject, add a body after a
   blank line that explains why, not what. Wrap at 72 characters.
6. If the diff mixes unrelated changes, suggest splitting the commit and
   list the groups.

Never invent a ticket number. Add "BREAKING CHANGE:" in the footer only
when public behavior changes.
