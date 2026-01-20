Setup Includes
==============
Installer/upgrader helpers, fragments, and sample config.

Contents
--------
- class.installer.php – installer logic.
- install.inc.php, install-prereq.inc.php, install-done.inc.php – installer steps and fragments.
- file-*.inc.php – file requirement checks.
- header.inc.php, footer.inc.php – shared layout.
- subscribe.inc.php – subscription prompt.
- ost-sampleconfig.php – sample config stub.
- streams/ – installation stream payloads.

Notes
-----
- Do not modify sample config paths without aligning installer logic.
- Streams must stay in sync with signatures and installer expectations.
