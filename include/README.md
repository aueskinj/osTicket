Include Directory
=================
Server-side core for osTicket. This folder holds the domain models, transport layers (AJAX/API/CLI), templates for the client and staff UIs, installer and upgrader helpers, translation packs, and bundled vendor libraries.

Top-level PHP entry points
--------------------------
- class.*.php – domain models and services (tickets, tasks, users/orgs, teams, SLAs, queues, schedules, mail fetch/delivery, PDF rendering, search, OAuth2, i18n, etc.).
- ajax.*.php – AJAX controllers used by staff and client web UIs.
- api.*.php – REST controllers backing api/http.php routes (legacy compatibility scripts live here as well).
- api.cron.php / api.tickets.php – older API entry scripts retained for backward compatibility.
- index.php and .htaccess – request guards that block directory listing and direct execution.
- ost-sampleconfig.php – template copied to include/ost-config.php by the installer.

Key subdirectories
------------------
- cli/ – console framework plus command modules (agent, cron, deploy, export, file, i18n, import, list, org, package, serve, unpack, upgrade, user). Loaded via include/cli.inc.php and used by manage.php.
- client/ and staff/ – view templates and partials for the client portal and the staff control panel.
- config/ – auxiliary configuration files (for example filetype.yaml) consumed by bootstrap code.
- i18n/ – shipped language packs and the translator README describing Crowdin-based workflows.
- plugins/ – plugin framework bootstrap and bundled sample plugins.
- upgrader/ – upgrade flow components (prerequisite checks, rename helpers, stream readers, and finalization steps).
- Vendor bundles – laminas-mail (mail transport), mpdf/fpdf (PDF generation), phpseclib (crypto), pear (MIME/IMAP helpers), htmLawed.php and html2text.php (HTML and text utilities), tnef_decoder.php (winmail.dat decoder), and other third-party helpers referenced throughout the codebase.

Development notes
-----------------
- Add new business logic as class.* services and surface them via thin controllers (ajax.* or api.*) rather than embedding logic in front controllers.
- Keep installer/upgrader changes in upgrader/ to preserve upgrade safety for existing deployments.
- When adding CLI functionality, place the module under cli/modules and wire it through cli.inc.php rather than creating ad-hoc scripts.
- Translation updates belong in i18n/ and should follow the Crowdin workflow; avoid editing generated language files manually.
- Vendor subfolders carry their upstream READMEs; refer there for third-party specifics instead of duplicating content.
