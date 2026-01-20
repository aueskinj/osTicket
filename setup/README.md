Setup Directory
===============
Installer and upgrader UI plus supporting assets and developer docs.

Structure
---------
- index.php, install.php – web installer frontends that write include/ost-config.php and seed the database.
- upgrade.php – web upgrader entrypoint.
- tips.php, ajax.php – helper endpoints for installer UI hints and AJAX.
- setup.inc.php – shared bootstrap for setup pages.
- css/, js/, images/ – assets used only by the installer/upgrader UI.
- inc/ – installer/upgrader helpers and page fragments.
- scripts/ – automation scripts executed during install/upgrade steps.
- cli/ – command-line installer utilities.
- test/ – installation/upgrader tests and fixtures.
- doc/ – developer notes (API, forms, i18n, ORM, packages, signals, streams) referenced by core documentation.

Notes
-----
- After a successful install, removing setup/ from production deployments is recommended for security.

Directory Index
---------------
- cli/ – CLI utilities: see cli/README.md
- css/ – installer styles: see css/README.md
- doc/ – developer docs: see doc/README.md
	- api/: see doc/api/README.md
- images/ – installer images: see images/README.md
	- icons/: see images/icons/README.md
- inc/ – installer helpers: see inc/README.md
	- streams/: see inc/streams/README.md
		- core/: see inc/streams/core/README.md
- js/ – installer scripts: see js/README.md
- scripts/ – setup automation scripts: see scripts/README.md
- test/ – installer/upgrader tests: see test/README.md
	- tests/: see test/tests/README.md
