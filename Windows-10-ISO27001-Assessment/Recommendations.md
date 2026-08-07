# Recommendations & Remediation Roadmap — Windows 10 GRC Assessment

This roadmap is based on the recommendations documented in the Windows 10 GRC Security Assessment Report.

## Immediate Actions

### 1. Encrypt Customer Data
**Finding:** No Data Encryption for Customer Data  
**Severity:** High  
**ISO 27001:** A.10.1.1  
**Status:** Open

Recommended actions:
- Enable encryption for folders containing customer data.
- Enforce BitLocker for full-disk encryption.
- Implement encryption at the application and database level for sensitive data.
- Regularly review encryption settings and monitor compliance.

### 2. Reduce Unrestricted Administrator Privileges
**Finding:** Admin Account With Unrestricted Privileges  
**Severity:** High  
**ISO 27001:** A.9.2.3  
**Status:** Open

Recommended actions:
- Apply the principle of least privilege.
- Use separate administrator accounts for administrative tasks.
- Remove unnecessary accounts from the local Administrators group.
- Use standard user accounts for daily activities.
- Enable UAC at the highest level.
- Implement role-based access control (RBAC).
- Enable logging and monitoring of administrative actions.
- Enforce MFA for privileged accounts.

## Strategic Security Recommendations

| Priority | Recommendation | Timeline | ISO Control |
|---|---|---|---|
| High | Plan migration from Windows 10 to a supported OS | 30 days | A.12.6.1 |
| High | Deploy SIEM for centralized log monitoring | 60 days | A.12.4.1 |
| Medium | Implement a formal patch management process | 60 days | A.12.6.1 |
| Medium | Implement DLP controls | 90 days | A.8.12 |
| Low | Establish security awareness training | 90 days | A.7.2.2 |
| Low | Establish quarterly backup/restore testing | Ongoing | A.12.3.1 |
| Low | Perform periodic access-rights reviews | Ongoing | A.9.2.5 |

## Follow-Up

The original assessment recommends a follow-up assessment within 90 days to verify closure of open findings, validate control effectiveness, and confirm continued alignment with the assessment framework.
