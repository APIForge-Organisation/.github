# Security Policy

## Supported versions

Only the latest minor release of each SDK is actively maintained for security patches.

| Repository | Supported |
|---|---|
| sdk-nodejs `latest` | Yes |
| sdk-nodejs `< latest` | No |

## Reporting a vulnerability

**Do not report security vulnerabilities through public GitHub issues.**

If you discover a security vulnerability, please send a report to:

**security@apiforge.dev**

Include as much of the following as possible:

- The repository and version affected
- A description of the vulnerability
- Steps to reproduce
- Potential impact
- Any suggested fix (optional)

We will acknowledge your report within **48 hours** and aim to release a fix within **14 days** for critical issues.

We do not currently have a bug bounty program, but we will publicly credit reporters (unless you prefer to remain anonymous) in the release notes.

## Security design principles

APIForge SDKs are built privacy-first by architecture:

- The SDK **never** reads request or response bodies
- The SDK **never** captures headers, cookies, or tokens
- The SDK **never** stores or transmits user-identifying data
- Route parameters are captured as patterns only (`/users/:id` — never `/users/12345`)
- In local mode, **no data leaves the host machine**

If you believe any of these guarantees are violated, that is a critical vulnerability — please report it immediately.
