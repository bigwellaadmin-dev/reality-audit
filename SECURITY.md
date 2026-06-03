# Security Policy

This is a static educational resource. The interactive tool runs entirely in the browser with no backend, no data persistence, no telemetry, and no third-party network requests — fonts are self-hosted under `tool/fonts/`.

## Reporting a Vulnerability

If you discover a security issue (for example, a way the tool could be made to leak data, an XSS vector in the rendered DOM, or a CSP misconfiguration that would let untrusted content execute), please report it privately rather than opening a public issue.

**Preferred channel:** [GitHub Private Vulnerability Reporting](https://github.com/bigwellaadmin-dev/reality-audit/security/advisories/new). This routes the report directly to the maintainer with no public disclosure.

**Alternative:** the contact form at https://bigwella.com if you do not have a GitHub account.

## Response commitments

| Stage | Target |
| --- | --- |
| Initial acknowledgement | within **7 days** of receiving a report |
| Triage decision (accepted / not a vulnerability / out of scope) | within **30 days** |
| Fix released or coordinated public disclosure | within **90 days** of triage |

Higher-severity issues (CVSS ≥ 7) will be prioritised inside those windows. If the timeline cannot be met for a specific report, the reporter will be notified and a revised target agreed.

## Supported versions

The current published release on `main` receives security fixes. The most recent tagged release also receives security fixes for 12 months after its release date. Older tagged versions are not maintained.

| Version | Supported |
| --- | --- |
| 1.0.x (current) | ✅ |
| Older | ❌ |

## Out of scope

- Misuse of the framework content itself (the framework is licensed CC BY 4.0 and can be adapted; that is not a security issue)
- Issues in third-party tools that integrate Reality Audit (those should be reported to the integrators)
- Self-XSS that requires the user to paste hostile content into their own browser console
