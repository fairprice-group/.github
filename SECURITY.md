# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in any FairPrice Group repository,
please report it privately rather than opening a public issue.

### How to Report

Use [GitHub's private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability)
to submit a report directly on the affected repository.

### What to Include

- Description of the vulnerability
- Steps to reproduce the issue
- Potential impact
- Any suggested fixes (optional)

### Response Timeline

- **Acknowledgement**: Within 3 business days
- **Initial Assessment**: Within 7 business days
- **Resolution**: Depends on severity and complexity

## Out of Scope

This policy does not cover the following:

- Reports from automated scanners without a proof-of-concept
- Social engineering or phishing attacks
- Physical attacks against FairPrice Group employees, offices, or data centres
- Denial of service attacks

## Supported Versions

Unless otherwise stated in a repository's own security policy, only the latest
release and the current `main` branch are supported with security updates.

## Security Best Practices

When contributing to any FairPrice Group repository:

- Never commit secrets, API keys, or credentials
- Use environment variables or secret management tools
- Validate and sanitise all external inputs
- Follow the principle of least privilege for service accounts
- Keep dependencies up to date and review them for known vulnerabilities
