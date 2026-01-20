Transport Exceptions
====================
Exceptions used by laminas-mail transports.

Contents
--------
- ExceptionInterface.php – marker for transport exceptions.
- InvalidArgumentException.php – invalid transport parameters.
- DomainException.php – domain-specific transport errors.
- RuntimeException.php – runtime transport failures.

Notes
-----
- Vendor code; prefer upstream fixes. Upstream docs: https://docs.laminas.dev/laminas-mail/.
- Transport exceptions surface delivery issues; changes may affect error handling semantics.
