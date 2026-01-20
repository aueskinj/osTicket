Storage Folders
===============
Folder abstractions for laminas-mail storage backends.

Contents
--------
- FolderInterface.php – contract for folder representations.
- Maildir.php – Maildir folder implementation.
- Mbox.php – Mbox folder implementation.

Notes
-----
- Vendor code; avoid local edits. Upstream docs: https://docs.laminas.dev/laminas-mail/.
- Folder behavior affects listing and traversal; prefer upstream changes for protocol compatibility.
