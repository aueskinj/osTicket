Vendor (laminas-mail)
=====================
Composer-installed vendor tree bundled with laminas-mail for osTicket.

Contents
--------
- autoload.php – Composer autoloader entry point.
- bin/ – Composer-generated helper scripts.
- composer/ – Composer runtime metadata and autoload maps.
- laminas/, psr/, symfony/, webmozart/ – upstream PHP packages required by laminas-mail.

Notes
-----
- Treat this directory as vendor code; do not edit directly. Update via upstream package releases and Composer when upgrading laminas-mail.
- Autoloading is driven by the Composer files in composer/; changing paths can break class resolution.
