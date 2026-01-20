Transport
========
Mail transport implementations for laminas-mail.

Contents
--------
- TransportInterface.php – contract for mail transports.
- Sendmail.php – sendmail-based transport.
- Smtp.php, SmtpOptions.php – SMTP transport and options.
- File.php, FileOptions.php – file transport for writing messages to disk.
- InMemory.php – in-memory transport for testing.
- Envelope.php – envelope representation.
- Factory.php – factory for constructing transports.
- Exception/ – transport-specific exceptions (DomainException, InvalidArgumentException, RuntimeException, ExceptionInterface).

Notes
-----
- Vendor code; avoid local edits. Upstream docs: https://docs.laminas.dev/laminas-mail/.
- Transport changes can impact mail delivery; prefer upstream updates.
