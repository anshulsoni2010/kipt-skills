---
name: release-notes
description: Drafts release notes from pull requests merged since the last
  tag, grouped as Breaking, New, Improved and Fixed. Use when the user asks
  for release notes, a changelog, or what shipped since the last release.
---

# Release notes

1. Find the last tag (git describe --tags --abbrev=0) and list merged pull
   requests or commits since then. If there is no tag, ask where to start.
2. Drop internal work users won't notice: refactors, CI, test-only changes,
   dependency bumps without user impact.
3. Group the rest under Breaking, New, Improved and Fixed. Leave out empty
   groups.
4. Write one line per change from the user's point of view, starting with
   a verb: "Add CSV export to reports."
5. Under Breaking, say exactly what users must change.

Output Markdown with the version and today's date as the heading.
