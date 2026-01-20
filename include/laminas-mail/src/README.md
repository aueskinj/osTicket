laminas-mail Source
===================
Upstream Laminas Mail component sources bundled with osTicket for composing, parsing, and transporting email.

Contents
--------
- Address.php, AddressList.php – value objects for email addresses and collections.
- Headers.php, Message.php, MessageFactory.php, Storage.php, ConfigProvider.php, Module.php – entry points for composing messages, header handling, service wiring, and storage abstraction.
- Address/ – address interfaces and helpers.
- Header/ – header field implementations (From/To/Cc/Bcc/Subject/etc.) plus loaders/locators and header-specific exceptions.
- Protocol/ – IMAP, POP3, and SMTP protocol clients and helpers (including XOAUTH2 support) with protocol-specific exceptions.
- Storage/ – mailbox abstractions (IMAP, POP3, Maildir, Mbox) with message/part helpers and writable variants.
- Transport/ – transports for Sendmail, SMTP, file, and in-memory delivery with related options and exceptions.
- Exception/ – common exception types for the component.

Notes
-----
- This is vendor code; avoid modifying directly. Upstream docs live at https://docs.laminas.dev/laminas-mail/.
- Application code expects upstream APIs; changes here can break mail send/fetch behavior.
