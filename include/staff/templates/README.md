Staff Templates (Shared)
========================
Shared view templates and partials used across the staff control panel.

Contents
--------
- *.tmpl.php – fragments for queues, searches, navigation, dynamic forms/fields, plugins, org/user helpers, ticket/task actions, schedules, exports/prints, email settings, and modal flows.

Notes
-----
- Templates assume data prepared by staff controllers; avoid embedding business logic here.
- Keep strings translatable via the i18n helpers.
- Align visibility and permission checks with server-side rules (tickets, tasks, queues, orgs, users).
