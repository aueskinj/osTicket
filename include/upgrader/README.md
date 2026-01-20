Upgrader
========
Scripts and helpers used during version upgrades.

Contents
--------
- prereq.inc.php – checks environment prerequisites before upgrading.
- rename.inc.php – handles file/directory renames during migrations.
- streams/ – streaming readers used for migration payloads.
- aborted.inc.php / done.inc.php – views shown on failure or completion.
- upgrade.inc.php – main upgrade harness.

Notes
-----
- Keep schema/data migration logic in upgrader steps to maintain backward compatibility.
- Avoid invoking application services that assume a fully upgraded schema; the upgrader runs in constrained contexts.
- Test upgrades on representative datasets before releasing.
