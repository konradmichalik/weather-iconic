# Security Policy

## Supported Versions

Only the latest release line receives security updates.

| Version | Supported          |
| ------- | ------------------ |
| 2.x     | :white_check_mark: |
| < 2.0   | :x:                |

## Reporting a Vulnerability

Please **do not** report security vulnerabilities through public GitHub issues.

Instead, use GitHub's [private vulnerability reporting](https://github.com/konradmichalik/weather-iconic/security/advisories/new)
to disclose the issue privately. This lets us investigate and release a fix
before the details become public.

Please include as much of the following as you can:

- A description of the vulnerability and its impact
- Steps to reproduce or a proof of concept
- Affected version(s)
- Any suggested mitigation or fix

We aim to acknowledge reports within a few business days and will keep you
informed about the progress toward a fix.

## Scope

`weather-iconic` ships as a static icon set with **no runtime dependencies**,
so the published package has a very small attack surface. Security reports are
most relevant for the build tooling (`devDependencies`) and the generated
distribution artifacts.
