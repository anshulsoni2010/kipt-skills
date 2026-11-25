---
name: dependency-upgrade
description: Upgrades a package or framework to a newer version by reading
  its changelog, finding affected code, making the changes and running the
  tests. Use when the user asks to upgrade, update or bump a dependency, or
  to fix deprecation warnings.
---

# Dependency upgrade

1. Note the current and target versions. If no target is given, use the
   latest stable release.
2. Read the changelog or migration guide for every major version in
   between. List the breaking changes that could affect this project.
3. Search the codebase for each affected API and list the files.
4. Upgrade the package with the project's package manager and update
   the lockfile.
5. Fix each affected call site. Keep changes minimal: no unrelated
   refactors.
6. Run the type checker, linter and tests. Fix what the upgrade broke.
7. Summarize: versions, breaking changes handled, files changed, and
   anything left to check by hand.

Upgrade one major version at a time if the jump spans more than one.
