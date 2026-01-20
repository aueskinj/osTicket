Staff Control Panel Directory
=============================
Administrative/staff UI entrypoints and assets.

Structure
---------
- index.php, login.php, logout.php – staff entry and authentication.
- admin.php, staff.php, tickets.php, tasks.php, queues.php, users.php, orgs.php, plugins.php, settings.php, system.php, etc. – module controllers for managing tickets, tasks, queues, users, orgs, SLAs, plugins, and system settings.
- admin.inc.php, staff.inc.php – shared staff-side bootstrap and layout helpers.
- ajax.php – staff AJAX front controller.
- upgrade.php – in-place upgrade trigger for authenticated admins.
- apps/ – staff-scoped app dispatchers.
- css/, js/, images/ – staff-only assets.

Notes
-----
- Staff controllers rely on shared models/services in include/class.*; staff templates live in include/staff/.

Directory Index
---------------
- apps/ – dispatcher: see apps/README.md
- css/ – staff styles: see css/README.md
- images/ – staff images: see images/README.md
	- icons/ – icon assets: see images/icons/README.md
- js/ – staff scripts: see js/README.md
