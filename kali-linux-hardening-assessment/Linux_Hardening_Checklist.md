# Linux Hardening Checklist — 30-Point Methodology

A practical hardening methodology developed and applied against a deliberately misconfigured Kali Linux VM as a personal lab exercise. Each item below was identified, remediated, and verified.

| # | Item | Fix |
|---|------|-----|
| 1 | Weak root password | `passwd root` — enforce a strong, unique password |
| 2 | SSH root login enabled | `PermitRootLogin no` in `sshd_config` |
| 3 | Unnecessary SSH service running | `systemctl disable ssh` if not required |
| 4 | FTP without strong auth | Disable anonymous access or replace with SFTP |
| 5 | `/etc/passwd` permissions | `chmod 644` + `chown root:root` |
| 6 | Firewall disabled | Enable UFW with default-deny incoming |
| 7 | SSH private key exposed | `chmod 600` on key and `chmod 700` on `.ssh` |
| 8 | Insecure port open | Block unused services at the firewall |
| 9 | Automatic updates disabled | Install and configure `unattended-upgrades` |
| 10 | Credentials exposed in web root | Remove secrets from `/var/www` |
| 11 | SSH password authentication enabled | Prefer key-based authentication where appropriate |
| 12 | Sensitive commands in shell history | Protect sensitive shell history |
| 13 | API keys exposed via web server | Remove from web-accessible paths and verify exposure is closed |
| 14 | Excessive sudo privileges | Review sudoers and remove unnecessary grants |
| 15 | Unattended upgrades not configured | Configure security updates |
| 16 | Apache directory listing enabled | Disable directory indexing |
| 17 | Log directory permissions too open | Restrict log directory and file permissions |
| 18 | Auditd disabled | Enable the audit framework |
| 19 | Unexpected script in `/usr/local/bin` | Investigate and remove unrecognized executables |
| 20 | Unlimited SSH login attempts | Set `MaxAuthTries 3` |
| 21 | Unsafe cron permissions | Restrict `/etc/crontab` permissions |
| 22 | GPG keys not protected | Restrict `.gnupg` permissions |
| 23 | Plaintext passwords in `/etc` configs | Remove plaintext secrets and restrict configuration files |
| 24 | SELinux disabled | Configure mandatory access control where appropriate |
| 25 | No IPTables rules | Apply and persist a default-deny inbound policy |
| 26 | DNS service lacks access control | Restrict query, recursion, and transfer access |
| 27 | World-readable log files | Restrict log file permissions |
| 28 | Passwordless account + autologin | Set passwords and disable unnecessary autologin |
| 29 | `/tmp` without execution restrictions | Consider `noexec,nosuid,nodev` where appropriate |
| 30 | World-readable config files | Restrict sensitive configuration permissions |

## Follow-Up

- Deploy Fail2ban for automated brute-force blocking.
- Implement centralized logging/SIEM.
- Enforce password complexity through PAM.
- Add file-integrity monitoring such as AIDE.
- Schedule periodic vulnerability/configuration assessments.
- Map the baseline to CIS Benchmarks or ISO/IEC 27001 for formal organizational use.

This checklist is a practical lab baseline, not an exhaustive compliance checklist.
