API Directory
=============
Public-facing API entrypoints and helpers.

Contents
--------
- api.inc.php – bootstrap for API requests (auth, config, error handling).
- http.php – JSON/REST endpoint dispatcher; maps API routes to include/api.* handlers.
- pipe.php – email piping target for MTAs; turns inbound mail into tickets.
- cron.php – HTTP-triggered cron hook for queue maintenance, mail fetch, and scheduled tasks.
- index.php – legacy/front-controller shim; loads api.inc.php and hands off to dispatchers.
- .htaccess – protects direct access patterns.

Notes
-----
- API keys and optional IP restrictions are configured in the staff panel; requests reach domain logic in include/class.* and api.* controllers.
- Mail piping and cron typically run from system services (MTA aliases, scheduled jobs) hitting pipe.php/cron.php directly.
