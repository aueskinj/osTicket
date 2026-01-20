Storage Exceptions
==================
Exceptions used by laminas-mail storage backends.

Contents
--------
- ExceptionInterface.php – marker for storage exceptions.
- InvalidArgumentException.php – invalid parameters or configuration.
- OutOfBoundsException.php – access outside valid folder/message ranges.
- RuntimeException.php – runtime storage failures (I/O, protocol issues).

Notes
-----
- Vendor code; defer to upstream fixes. Upstream docs: https://docs.laminas.dev/laminas-mail/.
