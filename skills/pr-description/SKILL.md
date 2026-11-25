---
name: pr-description
description: Writes a pull request title and description from the branch's
  commits and diff, with summary, changes, testing notes and risks. Use when
  the user asks for a PR description, PR body, or to open a pull request.
---

# Pull request description

1. Compare the current branch with the base branch (main unless told
   otherwise). Read the commit messages and the diff.
2. Title: under 70 characters, imperative, says the outcome.
3. Body, in this order:
   - **Summary**: two or three sentences on what changes for users or
     developers, and why.
   - **Changes**: bullet list grouped by area. One line each.
   - **How to test**: numbered steps a reviewer can follow.
   - **Risks**: anything that could break, migrations, flags, rollbacks.
     Write "None known" if there are none.
4. Mention screenshots are needed if UI files changed.
5. Link the issue only if its number appears in a commit or branch name.

Keep the whole body under 250 words.
