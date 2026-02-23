# Security Policy

## Security Commitment

MeridianAlgo is committed to maintaining the security and integrity of our open-source projects. We take security vulnerabilities seriously and encourage responsible disclosure.

## Supported Versions

The following versions of our projects are currently supported with security updates:

| Project | Version(s) | Support Status |
|---------|------------|----------------|
| All repositories | Latest stable version | ✅ Supported |
| All repositories | Previous major version | ⚠️ Best effort |
| All repositories | Older versions | ❌ Unsupported |

## Reporting a Vulnerability

### How to Report

**Do not open a public issue** for security vulnerabilities. Instead, report them privately:

1. **Email**: security@meridianalgo.org
2. **Include in your report**:
   - Type of vulnerability (e.g., XSS, SQL injection, etc.)
   - Affected project and version
   - Steps to reproduce the issue
   - Potential impact assessment
   - Any proof-of-concept code or screenshots

### Response Timeline

- **Initial Response**: Within 48 hours
- **Detailed Assessment**: Within 7 business days
- **Resolution Timeline**: Depends on severity, typically 2-4 weeks

### What to Expect

1. **Confirmation**: We will acknowledge receipt of your report
2. **Validation**: Our security team will investigate and validate the vulnerability
3. **Coordination**: We will work with you to understand and resolve the issue
4. **Disclosure**: We will coordinate public disclosure after the fix is deployed

## Vulnerability Severity Classification

We classify vulnerabilities using the CVSS (Common Vulnerability Scoring System):

### Critical (9.0-10.0)
- Remote code execution
- Privilege escalation
- Data breaches affecting multiple users

### High (7.0-8.9)
- Authentication bypass
- Significant data exposure
- Denial of service attacks

### Medium (4.0-6.9)
- Limited data exposure
- Cross-site scripting (XSS)
- CSRF vulnerabilities

### Low (0.1-3.9)
- Information disclosure
- Minor security misconfigurations

## Security Best Practices

### For Contributors

- **Never commit secrets**: API keys, passwords, tokens, or credentials
- **Use environment variables**: For all configuration and sensitive data
- **Validate inputs**: Sanitize and validate all user inputs
- **Follow secure coding practices**: OWASP guidelines and language-specific security recommendations
- **Keep dependencies updated**: Regularly update and scan for vulnerabilities

### For Users

- **Keep software updated**: Use the latest stable versions
- **Review permissions**: Apply principle of least privilege
- **Monitor for updates**: Subscribe to security announcements
- **Report suspicious activity**: Contact us if you notice unusual behavior

## Security Features

Our projects implement the following security measures:

- **Input validation and sanitization**
- **Secure authentication and authorization**
- **Encryption of sensitive data at rest and in transit**
- **Regular security audits and penetration testing**
- **Dependency vulnerability scanning**
- **Secure development lifecycle practices**

## Disclosure Policy

### Private Disclosure Process

1. **Report Received**: Vulnerability reported to security team
2. **Assessment**: Team validates and classifies severity
3. **Development**: Fix is developed and tested
4. **Deployment**: Fix is deployed to affected versions
5. **Public Disclosure**: Security advisory is published

### Public Disclosure

- **Security advisories** are published on GitHub
- **CVE numbers** are requested for critical and high-severity issues
- **Credit** is given to reporters (with permission)
- **Timeline**: Typically within 90 days of initial report

## Security Team

Our security team includes:

- **Security Engineers**: Vulnerability assessment and remediation
- **Development Leads**: Code review and secure implementation
- **Infrastructure Team**: System security and monitoring
- **Legal Counsel**: Compliance and disclosure coordination

## Legal Considerations

### Safe Harbor

We commit to not take legal action against security researchers who:

- Report vulnerabilities in good faith
- Follow our disclosure policy
- Do not exploit vulnerabilities beyond what's necessary for demonstration
- Do not damage or disrupt our services

### Requirements

Researchers must:

- Comply with applicable laws
- Not access or exfiltrate user data
- Not use automated tools that could cause disruption
- Respect user privacy and system integrity

## Security Resources

- **OWASP Top 10**: [https://owasp.org/www-project-top-ten/](https://owasp.org/www-project-top-ten/)
- **CVE Database**: [https://cve.mitre.org/](https://cve.mitre.org/)
- **National Vulnerability Database**: [https://nvd.nist.gov/](https://nvd.nist.gov/)
- **GitHub Security Advisories**: [https://github.com/security/advisories](https://github.com/security/advisories)

## Contact Information

- **Security Team**: security@meridianalgo.org
- **General Inquiries**: contact@meridianalgo.org
- **Security Issues**: security@meridianalgo.org (for vulnerability reports only)

## Acknowledgments

We thank the security community for helping us maintain secure and reliable open-source software. Your contributions make our projects safer for everyone.

---

*This policy is regularly updated to reflect current security practices and threat landscapes. Last updated: January 2026*
