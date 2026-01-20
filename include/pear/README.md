PEAR Bundles
===========
Bundled PEAR packages used for legacy mail, MIME, and utility features.

Contents
--------
- Mail/, Net/, Auth/, Math/, Crypt/ – PEAR components required by mail fetch/delivery and related helpers.
- PEAR.php / PEAR5.php – PEAR core autoloaders.
- BUNDLE – marker file from upstream distribution.

Notes
-----
- These libraries are vendor copies; avoid modifying them directly.
- Mail handling in class.mailfetch.php and related components depends on this bundle.
- When upgrading, verify compatibility with PHP versions supported by osTicket.
