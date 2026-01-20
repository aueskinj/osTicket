Include Directory
=================
Core server-side code: models, controllers, configuration, localization, plugins, vendor bundles, and upgrade utilities.

Structure
---------
- class.*.php – domain models and services (tickets, tasks, users/orgs, teams, SLAs, queues, schedules, mail fetch/delivery, PDF, search, OAuth2, i18n, etc.).
- ajax.*.php – AJAX endpoints for staff/client UIs.
- api.*.php – REST controllers backing api/http.php routes.
- index.php / .htaccess – front-controller guard to prevent direct listing.
- ost-sampleconfig.php – template for include/ost-config.php written by installer.
- cli/ – console framework and commands.
- client/ and staff/ – view templates/partials for the client portal and staff control panel.
- config/ – auxiliary configuration helpers (caching, connections) loaded by bootstrap.
- i18n/ – shipped language packs and translator README.
- laminas-mail/, mpdf/, pear/, fpdf/, phpseclib, htmLawed.php, etc. – bundled vendor libraries referenced by mail/PDF/security features.
- plugins/ – plugin framework and sample plugins.
- upgrader/ – migration logic invoked during upgrades.
- api.cron.php / api.tickets.php – legacy API entry scripts.

Notes
-----
- Prefer adding new business logic as class.* services and surface them via dedicated controllers (ajax.* or api.*) rather than coupling to front controllers.
- Vendor subfolders include their own upstream READMEs; this repository does not duplicate vendor documentation (Option A).
