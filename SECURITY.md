# Security Policy

## Supported Versions

This project is actively maintained. Security updates will be provided for the following versions:

| Version | Supported          |
| ------- | ------------------ |
| Latest  | :white_check_mark: |

## Reporting a Vulnerability

We take the security of our project seriously. If you believe you have found a security vulnerability, please report it to us as described below.

### How to Report Security Issues

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please send an email to the project maintainers with:

1. **Description**: A clear description of the vulnerability
2. **Impact**: Potential impact of the vulnerability
3. **Steps**: Steps to reproduce the issue
4. **Evidence**: Any supporting evidence (screenshots, logs, etc.)

### What to Expect

- **Acknowledgment**: We will acknowledge receipt of your report within 48 hours
- **Investigation**: We will investigate and validate the reported vulnerability
- **Updates**: We will provide regular updates on our progress
- **Resolution**: We will work to resolve critical vulnerabilities promptly

### Security Considerations for HR Data

This project deals with HR analytics data. Please be aware of the following security considerations:

#### Data Privacy
- **Anonymization**: Always anonymize personal data before analysis
- **Access Control**: Implement proper access controls for HR data
- **Encryption**: Use encryption for data at rest and in transit
- **Compliance**: Ensure compliance with data protection regulations (GDPR, CCPA, etc.)

#### Tableau Security Best Practices
- **Data Source Security**: Secure connections to data sources
- **User Authentication**: Implement proper user authentication
- **Row-Level Security**: Apply row-level security where appropriate
- **Extract Encryption**: Use extract encryption for sensitive data

#### General Security Guidelines
1. **Regular Updates**: Keep Tableau Desktop/Server updated
2. **Strong Passwords**: Use strong, unique passwords
3. **Network Security**: Secure network connections
4. **Audit Logs**: Monitor and review access logs
5. **Backup Security**: Secure backup storage and transmission

### Tableau-Specific Security

#### Data Connection Security
- Use secure connection protocols (SSL/TLS)
- Avoid embedding credentials in workbooks
- Implement proper database user permissions
- Regular credential rotation

#### Workbook Security
- Remove sensitive data from packaged workbooks
- Use data extracts instead of live connections when possible
- Implement proper filter security
- Regular security audits of published content

### Incident Response

In case of a security incident:

1. **Immediate Action**: Disconnect affected systems if necessary
2. **Assessment**: Assess the scope and impact of the incident
3. **Containment**: Contain the incident to prevent further damage
4. **Communication**: Notify relevant stakeholders
5. **Recovery**: Implement recovery procedures
6. **Post-Incident**: Conduct post-incident analysis and improvements

### Security Resources

- [Tableau Security Best Practices](https://help.tableau.com/current/server/en-us/security_auth.htm)
- [Data Privacy Guidelines](https://gdpr.eu/)
- [HR Data Security Standards](https://www.shrm.org/resourcesandtools/tools-and-samples/toolkits/pages/managinghrdata.aspx)

### Contact Information

For security-related questions or concerns, please contact the project maintainers through appropriate channels.

---

**Note**: This security policy is designed to protect both the project and users handling sensitive HR data. Always prioritize data privacy and security when working with employee information.
