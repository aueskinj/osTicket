PEAR Net_DNS2 (Local Note)
==========================
DNS client implementation and records.

Contents
--------
- Core: DNS2.php, supporting helpers (Resolver, Packet, Question, RR, etc.).
- Cache/ – DNS cache backends.
- Packet/ – request/response helpers.
- RR/ – resource record implementations.
- Socket/ – socket abstractions.

Notes
-----
- Vendor code; do not edit. DNS lookups in mail/SRV contexts depend on this.
