Client Templates
================
View templates and partials for the public client portal.

Contents
--------
- *.inc.php – page fragments for ticket creation, login, profile management, knowledgebase browsing, password resets, and ticket viewing.
- templates/ – shared HTML snippets used across client pages.

Notes
-----
- Templates assume controller data prepared by client-facing controllers; avoid embedding business logic here.
- Keep UI strings translatable; rely on the i18n helpers and language packs.
