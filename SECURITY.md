# Security Policy

## Supported Versions

| Version | Supported |
| ------- | --------- |
| latest  | Yes       |

This repo distributes Homebrew casks. The casks always reference the latest release of the upstream project.

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

Use [GitHub Security Advisories](https://github.com/sydlexius/homebrew-tap/security/advisories/new)
to report vulnerabilities privately. This ensures the issue can be triaged and a
fix prepared before public disclosure.

When reporting, please include:

- A description of the vulnerability and its potential impact
- Steps to reproduce or a proof-of-concept
- The affected version(s) or commit(s)
- A suggested fix, if you have one

You should receive an initial acknowledgment within 72 hours. Critical issues
will be addressed as quickly as practical.

## Scope

In scope:

- The cask definitions in `Casks/` (checksum correctness, download URLs)
- The workflows in `.github/workflows/`

Out of scope:

- Vulnerabilities in the packaged software itself (report those on the
  project's own repository)
- Vulnerabilities in Homebrew (report those to Homebrew)

## Security Measures

- **Checksum pinning:** every cask pins a `sha256` for each artifact
- **Generated casks:** casks are produced by the upstream release pipeline
  rather than hand-edited, so the checksum always matches the released artifact
- **Pinned actions:** all GitHub Actions are pinned to a commit SHA
- **Secret scanning** with push protection is enabled
