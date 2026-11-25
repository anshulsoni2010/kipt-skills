---
name: code-review
description: Reviews a diff or pull request for bugs, edge cases, security
  issues and missing tests, and suggests the smallest fix for each. Use when
  the user asks for a code review, a PR review, or to check changes before
  merging.
---

# Code review

1. Get the changes: the diff the user gave, or git diff against the main
   branch if none was given.
2. Read the surrounding code for every changed function, including callers,
   before judging it.
3. Look for, in this order:
   - Bugs and wrong behavior
   - Unhandled edge cases: empty input, null, large input, concurrency
   - Security: injection, missing auth checks, secrets, unsafe file paths
   - Missing or weak tests for the changed behavior
4. For each finding give: file and line, severity (high, medium, low),
   why it matters in one sentence, and the smallest fix.
5. Skip formatting and naming nits unless they hide a bug.

End with a one-line verdict: "Ready to merge", "Merge after fixes" or
"Needs another pass". If there are no findings, say so in one line.
