Protocols
========
Protocol clients and helpers for IMAP, POP3, SMTP, and XOAUTH2 in laminas-mail.

Contents
--------
- AbstractProtocol.php, ProtocolTrait.php – shared helpers for protocol clients.
- Imap.php, Pop3.php – mail retrieval clients.
- Smtp.php – SMTP client.
- SmtpPluginManager.php, SmtpPluginManagerFactory.php – plugin manager wiring for SMTP features.
- Exception/ – protocol-level exceptions (ExceptionInterface, InvalidArgumentException, RuntimeException).
- Pop3/ – POP3-specific helpers (Response.php) and XOAUTH2 support for POP3.
- Smtp/ – SMTP auth implementations (Auth/Crammd5.php, Login.php, Plain.php, Xoauth2.php).
- Xoauth2/ – XOAUTH2 client helper (Xoauth2.php) and provider-specific handlers.

Notes
-----
- Vendor code; avoid local changes. Upstream docs: https://docs.laminas.dev/laminas-mail/.
- Protocol changes can break mail send/fetch interoperability; prefer upstream upgrades.
