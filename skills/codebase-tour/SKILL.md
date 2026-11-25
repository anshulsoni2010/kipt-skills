---
name: codebase-tour
description: Gives a guided tour of an unfamiliar codebase, covering what it
  does, how it is laid out, how a request flows through it, and how to run it.
  Use when the user is new to a repo or asks how the code is organized,
  where something lives, or to explain the project.
---

# Codebase tour

1. Read the README, the package or build files, and the top-level folders.
2. Explain, in this order:
   - What the project does, in two sentences
   - The stack: languages, frameworks, database, hosting
   - The folder layout: one line per important folder
   - One real request or job traced end to end, naming each file it
     passes through
   - How to install, run and test it locally
   - Where to start for a typical first change
3. Name files with their paths so the user can open them.

Stay under 500 words unless the user asks for more. Say when you are
inferring something rather than reading it from the code.
