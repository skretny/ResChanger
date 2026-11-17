# Security Policy

## Supported versions

| Version | Supported |
|---|---|
| 1.0.x | Yes |

## Reporting a vulnerability

Please do not open a public issue for security problems.

Use the repository's **Security → Report a vulnerability** page (GitHub Security Advisories). Include:

- affected version;
- Windows version;
- display configuration, if relevant;
- steps to reproduce;
- expected and actual behavior;
- whether the problem requires local access.

## Scope

ResChanger is a local desktop application and does not make network requests. Security-relevant areas include display mode changes, global hotkeys, the autostart registry value under `HKCU`, the single-instance named pipe, and parsing of the local settings file.
