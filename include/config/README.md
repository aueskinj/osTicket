Config Assets
============
Auxiliary configuration artifacts loaded by bootstrap and services.

Contents
--------
- filetype.yaml – MIME type and extension hints used by upload/attachment validation.

Notes
-----
- Keep entries synchronized with server-side validation logic in class.file.php and related upload handlers.
- Avoid adding sensitive data; runtime credentials belong in include/ost-config.php.
