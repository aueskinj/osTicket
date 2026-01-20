SMTP Auth
========
Authentication mechanisms for laminas-mail SMTP client.

Contents
--------
- Crammd5.php – CRAM-MD5 SASL auth.
- Login.php – LOGIN auth.
- Plain.php – PLAIN auth.
- Xoauth2.php – XOAUTH2 auth.

Notes
-----
- Vendor code; avoid local changes. See https://docs.laminas.dev/laminas-mail/.
- Auth behavior affects SMTP interoperability; prefer upstream updates.
