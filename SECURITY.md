# Security Policy

## Supported Versions
Only the latest released version of **Org Manager** is supported with security fixes.

## Reporting a Vulnerability
If you discover a security vulnerability, **please do not open a public issue**.

Instead, report it privately by contacting:

Mantainer of the repository.

When reporting, please include:
- A clear description of the vulnerability
- Steps to reproduce
- Potential impact
- Any suggested mitigations (if available)

We aim to acknowledge reports within **72 hours**.

## Secrets & Credentials
- Secrets must **never** be committed to the repository
- Use environment variables or an external secret manager (Vault, SSM, etc.)
- Example configuration files must always use placeholder values
- Logs and plan outputs must redact sensitive information

## Threat Model (High-Level)
Org Manager interacts with enterprise APIs and therefore assumes:
- Least-privilege API tokens
- Read-only access during `plan`
- Explicit approval before `apply`
- Full auditability via Git history and pipeline logs

## Responsible Disclosure
Please allow reasonable time to investigate and resolve reported issues
before any public disclosure.