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

Directory Index
---------------
- Auth: [Auth/README.local.md](Auth/README.local.md)
	- SASL mechanisms: [Auth/SASL/README.local.md](Auth/SASL/README.local.md)
- Crypt: [Crypt/README.local.md](Crypt/README.local.md)
- Mail: [Mail/README.local.md](Mail/README.local.md)
- Math: [Math/README.local.md](Math/README.local.md)
- Net: [Net/README.local.md](Net/README.local.md)
	- Net_DNS2: [Net/DNS2/README.local.md](Net/DNS2/README.local.md)
		- Cache: [Net/DNS2/Cache/README.local.md](Net/DNS2/Cache/README.local.md)
		- Packet: [Net/DNS2/Packet/README.local.md](Net/DNS2/Packet/README.local.md)
		- RR: [Net/DNS2/RR/README.local.md](Net/DNS2/RR/README.local.md)
		- Socket: [Net/DNS2/Socket/README.local.md](Net/DNS2/Socket/README.local.md)
	- Socket: [Net/Socket/README.local.md](Net/Socket/README.local.md)
- PEAR core: [PEAR/README.local.md](PEAR/README.local.md)
