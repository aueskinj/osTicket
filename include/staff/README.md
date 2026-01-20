Staff Templates
===============
View templates and partials for the staff control panel.

Contents
--------
- *.inc.php / *.tpl.php – page fragments for tickets, tasks, users, orgs, knowledgebase, settings, plugins, queues, schedules, SLAs, and authentication flows.
- templates/ – shared snippets reused across staff pages.
- index.php – guard front controller for the directory.

Notes
-----
- Templates expect data prepared by staff controllers; keep business logic in class.* services and controllers.
- Ensure new UI strings are translatable and align with the i18n catalogs.
- Coordinate changes with AJAX endpoints when adding interactive features.
