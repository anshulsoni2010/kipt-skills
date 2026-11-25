---
name: bug-triage
description: Triages a bug report into a clear issue with steps to
  reproduce, expected and actual behavior, likely cause, severity and owner
  area. Use when the user pastes a bug report, error, crash log or customer
  complaint and asks what is wrong or to file it.
---

# Bug triage

1. Restate the problem in one sentence.
2. Pull out or ask for: steps to reproduce, expected result, actual
   result, environment (version, browser or OS), and how often it happens.
3. Search the codebase for the error message, route or component named in
   the report. Name the most likely file and function, and say how sure
   you are.
4. Set severity:
   - Critical: data loss, security, or the main flow is down for everyone
   - High: a core feature is broken with no workaround
   - Medium: broken with a workaround, or affects few users
   - Low: cosmetic
5. Output a ready-to-file issue: title, the fields above, likely cause,
   and a suggested first step to fix.

Never mark something Critical without saying which rule it meets.
