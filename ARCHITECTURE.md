Architecture Overview
=====================
This document maps the top-level layout, request flows, and extension points in osTicket.

Request Flows
-------------
- Client portal: public entrypoints (index.php, open.php, tickets.php, profile.php, login.php, pwreset.php) bootstrap via bootstrap.php and client.inc.php, render pages/templates from include/client/ with shared business logic in include/class.*.
- Staff control panel: scp/index.php (and scp/login.php) bootstraps with staff.inc.php, dispatches through scp/*.php modules, and shares core models/services from include/.
- Public API: api/http.php (JSON over HTTP), api/pipe.php (email piping), and api/cron.php (cron callback) load api.inc.php and route via include/class.dispatcher.php and API controllers; authentication uses API keys and optional IP locks.

Bootstrapping and Configuration
-------------------------------
- bootstrap.php wires autoloading, configuration, and error handling used by both client and staff entrypoints; main.inc.php and secure.inc.php provide shared runtime helpers.
- Installation writes include/ost-config.php (based on include/ost-sampleconfig.php) holding database credentials and salts; installer lives under setup/.
- Session/state helpers live in include/class.session.php and include/class.usersession.php; CSRF handling is in include/class.csrf.php.

Core Domain Layer (include/)
----------------------------
- Core models and services are implemented via class.* files (tickets, tasks, threads, users, orgs, teams, SLAs, email, mailfetch, PDF, search, queues, schedules, OAuth2, i18n, etc.).
- Web controllers: ajax.*.php and api.*.php expose staff/client AJAX and REST endpoints; client/ and staff/ subfolders hold view partials/templates.
- CLI utilities under include/cli/ provide console tasks; upgrader/ contains migration logic; plugins/ hosts plugin scaffolding and loaders.

Presentation and Assets
-----------------------
- css/ and js/ host shared styles and scripts for both client and staff UIs; assets/ contains themeable resources (default skin, fonts) referenced by those bundles.
- images/ holds shared artwork (favicons, avatars, captcha assets); scp/css/, scp/js/, scp/images/ complement staff-only assets; setup/css|js|images/ serve the installer.
- kb/, pages/, and apps/ are lightweight front controllers/dispatchers for knowledgebase, simple pages, and auxiliary apps.

Background Work and Integrations
--------------------------------
- Email fetching and piping run via api/pipe.php, include/class.mailfetch.php, and cron drivers (api/cron.php, scp/autocron.php); queues and signals orchestrate asynchronous work.
- Outbound mail uses include/class.mailer.php (Laminas Mail) with templates from include/class.template.php.

Setup and Upgrade
-----------------
- setup/ delivers the installer/upgrader UI (install.php, upgrade.php, tips.php) plus scripts/ and doc/ developer notes (API, ORM, forms, signals, streams, i18n).
- In-place upgrades use include/upgrader/ and scp/upgrade.php; see UPGRADING.txt for runbook.

Extensibility and Customization
-------------------------------
- Plugins live in include/plugins/ and register via include/class.plugin.php; sample plugins ship alongside vendor dependencies.
- Theming uses assets/default/ (images, LESS/CSS guidance) and overrides in css/ and scp/css/; see assets/default/doc/Theme-How-To.rst for skinning tips.
- Localization packs live under include/i18n/; translator guidance is in setup/doc/i18n.md and README in include/i18n/.

Third-Party Libraries
---------------------
- Bundled vendor code resides under include/ (laminas-mail, mpdf/fpdi, pear, phpseclib, htmLawed, etc.). Each subfolder carries its own upstream README; this repo documents only how core code integrates them.

See Also
--------
- README.md for project overview and requirements.
- UPGRADING.txt and WHATSNEW.md for release and migration notes.
- Per-folder README files (api/, apps/, assets/, css/, images/, include/, js/, kb/, pages/, scp/, setup/) for focused details.