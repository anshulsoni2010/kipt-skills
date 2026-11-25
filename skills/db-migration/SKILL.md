---
name: db-migration
description: Plans and reviews a database schema migration with a safety
  checklist covering locking, backfills, rollbacks and deploy order. Use when
  the user is adding, changing or removing tables, columns or indexes, or
  asks to write or review a migration.
---

# Database migration

Work through this checklist and report each item as OK, Risk or N/A:

1. **Locking**: will this lock a large table? Prefer adding indexes
   concurrently and adding nullable columns first.
2. **Backwards compatibility**: can the currently deployed code run against
   the new schema? If not, split into expand and contract steps.
3. **Backfill**: is data being moved or filled? Do it in batches, outside
   the migration, and make it safe to re-run.
4. **Defaults and NOT NULL**: add the column, backfill, then add the
   constraint in a later migration.
5. **Rollback**: write the down migration, or explain why it is one-way.
6. **Deploy order**: list the steps in order, for example
   migrate, deploy, backfill, then constrain.
7. **Data loss**: flag any drop or type change that loses data, and ask
   for confirmation before writing it.

Then write the migration in the project's existing migration tool.
