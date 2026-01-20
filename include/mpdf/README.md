mPDF Bundle
===========
mPDF library distribution used for PDF generation within osTicket.

Contents
--------
- vendor/ – upstream mPDF and dependencies as installed by composer.
- composer.json / composer.lock – pinned dependency metadata from the upstream package.

Notes
-----
- Application code relies on mPDF for rendering ticket, FAQ, and export PDFs; avoid modifying vendor code directly.
- To upgrade, follow the versions defined in composer.json and test PDF outputs for regressions.
