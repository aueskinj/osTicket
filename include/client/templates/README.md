Client Templates (Shared)
========================
Shared view templates reused across client portal pages.

Contents
--------
- dynamic-form.tmpl.php – renders dynamic form fields and values.
- inline-form.tmpl.php – inline form rendering helper.
- sidebar.tmpl.php – client sidebar layout and navigation.
- thread-entries.tmpl.php – collection renderer for thread entries.
- thread-entry.tmpl.php – single thread entry (message/note) rendering.
- thread-event.tmpl.php – thread event display block.
- thread-export.tmpl.php – printable/exportable thread formatting.
- ticket-print.tmpl.php – ticket print view layout.

Notes
-----
- Templates assume data is prepared by client controllers; avoid embedding business logic.
- Keep strings translatable; rely on i18n helpers and language packs.
- Ensure thread-related templates stay consistent with server-side visibility rules (internal vs. public notes).
