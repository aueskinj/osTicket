Setup CLI
========
Command-line utilities for installer/maintenance.

Contents
--------
- manage.php – CLI entrypoint for setup tasks.
- cleanup-codebase.sh – helper script for codebase cleanup.

Notes
-----
- Keep business logic in include/class.* services; CLI should orchestrate.
- Ensure scripts are executable in installer environments.
