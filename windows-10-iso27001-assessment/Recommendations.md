# Recommendations & Remediation Roadmap

## Immediate Actions

### Encrypt Customer Data
**Severity:** High  
**ISO 27001:** A.10.1.1  
**Status:** Open

- Enable encryption for folders containing customer data.
- Enforce BitLocker for full-disk encryption.
- Implement encryption at application/database level for sensitive data.
- Review encryption settings periodically.

### Reduce Unrestricted Administrator Privileges
**Severity:** High  
**ISO 27001:** A.9.2.3  
**Status:** Open

- Apply least privilege.
- Use separate administrator accounts for administrative tasks.
- Remove unnecessary local Administrators memberships.
- Use standard accounts for daily work.
- Enable strong UAC settings.
- Implement RBAC where appropriate.
- Log and monitor privileged activity.
- Enforce MFA for privileged accounts.

## Strategic Recommendations

| Priority | Recommendation | Timeline | ISO Control |
|---|---|---|---|
| High | Plan migration from Windows 10 to a supported OS | 30 days | A.12.6.1 |
| High | Deploy SIEM for centralized log monitoring | 60 days | A.12.4.1 |
| Medium | Implement formal patch management | 60 days | A.12.6.1 |
| Medium | Implement DLP controls | 90 days | A.8.12 |
| Low | Establish security awareness training | 90 days | A.7.2.2 |
| Low | Establish quarterly backup/restore testing | Ongoing | A.12.3.1 |
| Low | Perform periodic access-rights reviews | Ongoing | A.9.2.5 |

A follow-up assessment should verify closure of open findings and continued control effectiveness.
