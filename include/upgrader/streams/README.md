Upgrader Streams
================
Signed migration stream packages used by the upgrader.

Contents
--------
- core.sig – signature file for the core migration stream.
- core/ – ordered migration payloads (SQL patches and task scripts).

Notes
-----
- Files are applied by the upgrader; do not modify or reorder.
- Keep signatures in sync with payloads when updating streams.
- Ensure new migrations remain idempotent and safe for in-place upgrades.
