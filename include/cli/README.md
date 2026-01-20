CLI Framework
============
Command runner used by manage.php and automated tasks.

Contents
--------
- cli.inc.php – bootstraps the console runtime and argument parsing.
- modules/ – individual commands (agent, cron, deploy, export, file, i18n, import, list, org, package, serve, unpack, upgrade, user).

Notes
-----
- Add new commands as modules/*.php and register them in cli.inc.php.
- Keep commands thin; reuse services in class.* files rather than duplicating business logic.
- Commands should exit with non-zero status on failure for scripting compatibility.
