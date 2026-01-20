CLI Modules
===========
Command implementations loaded by include/cli.inc.php and executed via manage.php.

Modules
-------
- agent.php – manage agents (create/list/update).
- cron.php – run scheduled tasks (ticket fetch, alerts, maintenance).
- deploy.php – helper for deployment/package publishing workflows.
- export.php – export data sets (tickets, users, orgs, etc.).
- file.php – file operations used by other commands.
- i18n.php – translation utilities (pack/unpack language files).
- import.php – import data from supported sources.
- list.php – manage dynamic lists and options.
- org.php – manage organizations.
- package.php – build or inspect osTicket packages.
- serve.php – lightweight PHP server bootstrap for local testing.
- unpack.php – unpack osTicket releases or language packs.
- upgrade.php – run upgrade routines from the CLI.
- user.php – manage end users.

Notes
-----
- New commands should live alongside these modules and be wired through cli.inc.php.
- Keep modules thin; delegate business logic to class.* services for consistency and testability.
- Return non-zero exit codes on failure to support scripting and CI.
