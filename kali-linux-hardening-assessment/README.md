# Kali Linux Security & Hardening Assessment

A practical 30-point security hardening assessment performed against a deliberately misconfigured Kali Linux lab VM.

## Scope

- Authentication and password policy
- SSH configuration
- Firewall and network access control
- Filesystem permissions
- Apache/web-server configuration
- Logging and audit framework
- Scheduled tasks
- Sensitive data exposure
- Privilege management
- DNS access control
- Mandatory access control
- Automatic updates

## Assessment Approach

Each control was identified, remediated, and verified during a hands-on hardening pass. The checklist is intended as a practical baseline for Debian/Ubuntu-based Linux systems.

## Key Hardening Areas

- Disable unnecessary services and insecure remote access.
- Enforce strong authentication and SSH key-based access where appropriate.
- Apply least privilege to users and sudo permissions.
- Enable and configure firewall controls.
- Protect sensitive files, logs, keys, and configuration files.
- Enable audit logging and automatic security updates.
- Reduce web-server information exposure.
- Restrict DNS and network services.
- Apply filesystem mount protections such as `noexec`, `nosuid`, and `nodev` where appropriate.

## Follow-Up Recommendations

- Deploy Fail2ban for automated brute-force protection.
- Centralize logs in a SIEM.
- Enforce password quality through PAM.
- Add file-integrity monitoring such as AIDE.
- Perform recurring vulnerability and configuration assessments.
- Map the baseline to a formal standard such as CIS Benchmarks or ISO/IEC 27001 when used for a real organizational assessment.

## Disclaimer

This assessment was performed against a controlled Kali Linux lab VM with deliberately introduced misconfigurations. It is an educational hardening baseline, not a formal compliance certification.

---
**Author:** Fares Khzouz
