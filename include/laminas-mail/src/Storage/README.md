Storage
=======
Mailbox storage abstractions and helpers for laminas-mail.

Contents
--------
- AbstractStorage.php, ParamsNormalizer.php – base storage handling and parameter normalization.
- Imap.php, Pop3.php, Maildir.php, Mbox.php – storage backends for IMAP, POP3, Maildir, and Mbox.
- Folder.php – folder representation.
- Message.php, Part.php – message and part abstractions.
- Exception/ – storage-specific exceptions (InvalidArgumentException, OutOfBoundsException, RuntimeException, ExceptionInterface).
- Folder/ – folder interfaces and backend-specific folder implementations (Maildir, Mbox).
- Message/ – message file adapter and interface.
- Part/ – part file adapter, interfaces, and exceptions.
- Writable/ – writable Maildir implementation and interface for mutable stores.

Notes
-----
- Vendor code; avoid local edits. Upstream docs: https://docs.laminas.dev/laminas-mail/.
- Changes can impact mailbox compatibility; prefer upstream updates.
