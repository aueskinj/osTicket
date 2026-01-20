Vendor (mPDF)
============
Composer-installed vendor tree bundled with mPDF for osTicket.

Contents
--------
- autoload.php – Composer autoloader entry point.
- composer/ – Composer runtime metadata and autoload maps.
- mpdf/ – upstream mPDF library sources and assets.
- myclabs/, paragonie/, psr/, setasign/ – additional upstream packages required by mPDF.

Notes
-----
- Treat this directory as vendor code; do not edit directly. Update via upstream package releases.
- Autoloading is driven by the Composer files in composer/; changing paths can break class resolution.
