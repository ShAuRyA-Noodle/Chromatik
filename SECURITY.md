# Security Policy

**Report a vulnerability privately** by emailing shauryapunj404@gmail.com (subject `[Chromatik SECURITY] ...`) or by using GitHub's "Security › Report a vulnerability" tab.

Acknowledgement within 48 hours; critical issues aim for a patch within 7 days.

## Controls

- CodeQL static analysis runs on push, pull request, and a weekly schedule.
- Dependabot runs weekly for version updates.
- Branch protection on `main`: required CodeQL status check, no force-push, no deletion.
- The jQuery CDN script is pinned with a Subresource Integrity (SRI) hash and `crossorigin="anonymous"`.
