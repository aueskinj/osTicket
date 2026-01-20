Core Migration Stream
=====================
Ordered core upgrade payloads consumed by the upgrader.

Contents
--------
- *.patch.sql – schema/data migration statements.
- *.task.php – procedural tasks to accompany SQL changes.
- *.cleanup.sql – cleanup steps executed after the main patch when present.

Notes
-----
- File names encode ordering and pairing; do not rename or reorder.
- Keep SQL and task files idempotent to support interrupted upgrades.
- Changes must be reflected in the corresponding signature (core.sig) when stream content changes.
