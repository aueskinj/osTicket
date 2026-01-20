Storage Parts
=============
MIME part abstractions for laminas-mail storage backends.

Contents
--------
- PartInterface.php – contract for message parts.
- File.php – file-based part adapter.
- Exception/ – part-specific exceptions (ExceptionInterface, InvalidArgumentException, RuntimeException).

Notes
-----
- Vendor code; avoid local edits. Upstream docs: https://docs.laminas.dev/laminas-mail/.
- Part handling impacts MIME parsing; prefer upstream updates.
