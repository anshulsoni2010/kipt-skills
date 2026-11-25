# Agent Skills for everyday engineering work

14 small, practical [Agent Skills](https://agentskills.io) for code review, commit messages, pull requests, release notes, tests, docs, bug triage and more. Each is one `SKILL.md` file you can read in a minute and edit to match how your team works.

They follow the open Agent Skills format, so the same folder works in Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI and other agents that read it.

## Install

Every skill, for all your projects, into the agents you choose:

```bash
npx skills add https://github.com/anshulsoni2010/kipt-skills.git --all -g -a claude-code -a codex
```

One skill:

```bash
npx skills add https://github.com/anshulsoni2010/kipt-skills.git --skill release-notes -g
```

Or copy a folder from `skills/` into your agent's skills folder by hand, for example `~/.claude/skills/` for Claude Code or `~/.agents/skills/` for Codex.

Read a skill before you install it. Skills are instructions your agent follows.

## The skills

| Skill | What it does |
| --- | --- |
| [`code-review`](skills/code-review/SKILL.md) | Reviews a diff or pull request for bugs, edge cases, security issues and missing tests, and suggests the smallest fix for each. Use when the user asks for a code review, a PR review, or to check changes before merging. |
| [`commit-message`](skills/commit-message/SKILL.md) | Writes a commit message from the staged changes in the Conventional Commits style. Use when the user asks to commit, asks for a commit message, or says "write the commit". |
| [`pr-description`](skills/pr-description/SKILL.md) | Writes a pull request title and description from the branch's commits and diff, with summary, changes, testing notes and risks. Use when the user asks for a PR description, PR body, or to open a pull request. |
| [`release-notes`](skills/release-notes/SKILL.md) | Drafts release notes from pull requests merged since the last tag, grouped as Breaking, New, Improved and Fixed. Use when the user asks for release notes, a changelog, or what shipped since the last release. |
| [`writing-style`](skills/writing-style/SKILL.md) | Applies the team's writing style to docs, READMEs, emails, announcements and UI text. Use when the user asks to write, edit, rewrite or proofread text, or to make something clearer or shorter. |
| [`write-tests`](skills/write-tests/SKILL.md) | Writes unit tests for a function, module or change, following the project's existing test framework and patterns. Use when the user asks for tests, more test coverage, or to test a function or bug fix. |
| [`api-docs`](skills/api-docs/SKILL.md) | Writes reference documentation for REST API endpoints from the route handlers and types, with parameters, request and response examples, and errors. Use when the user asks to document an API, an endpoint or a route. |
| [`bug-triage`](skills/bug-triage/SKILL.md) | Triages a bug report into a clear issue with steps to reproduce, expected and actual behavior, likely cause, severity and owner area. Use when the user pastes a bug report, error, crash log or customer complaint and asks what is wrong or to file it. |
| [`db-migration`](skills/db-migration/SKILL.md) | Plans and reviews a database schema migration with a safety checklist covering locking, backfills, rollbacks and deploy order. Use when the user is adding, changing or removing tables, columns or indexes, or asks to write or review a migration. |
| [`dependency-upgrade`](skills/dependency-upgrade/SKILL.md) | Upgrades a package or framework to a newer version by reading its changelog, finding affected code, making the changes and running the tests. Use when the user asks to upgrade, update or bump a dependency, or to fix deprecation warnings. |
| [`incident-postmortem`](skills/incident-postmortem/SKILL.md) | Writes a blameless incident postmortem from notes, timelines, logs and chat transcripts, with impact, root cause and action items. Use when the user asks for a postmortem, incident report, incident review or RCA. |
| [`codebase-tour`](skills/codebase-tour/SKILL.md) | Gives a guided tour of an unfamiliar codebase, covering what it does, how it is laid out, how a request flows through it, and how to run it. Use when the user is new to a repo or asks how the code is organized, where something lives, or to explain the project. |
| [`accessibility-review`](skills/accessibility-review/SKILL.md) | Reviews UI code such as React, Vue or HTML components for accessibility problems against WCAG basics, with fixes. Use when the user asks for an accessibility or a11y review, or to check a component, form or page for screen reader and keyboard support. |
| [`meeting-notes`](skills/meeting-notes/SKILL.md) | Turns a meeting transcript or rough notes into short notes with decisions, action items with owners, and open questions. Use when the user pastes a transcript or notes and asks for a summary, minutes, recap or action items. |

## Make them yours

These are starting points. Change the steps, the output format and the description to match your team. The description decides when an agent picks a skill up, so put the words you actually type in it.

The walkthrough behind each skill is in [14 Claude skills examples](https://kipt.me/guides/claude-skills-examples) on kipt.me, which also covers how to write your own.

## License

MIT. See [LICENSE](LICENSE).
