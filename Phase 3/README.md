# Phase 3: Defensive Strategy for ProFTPD Vulnerability

## Overview
In this phase, we implemented a defense-in-depth strategy to mitigate the ProFTPD `mod_copy` vulnerability, using firewall rules, real-time monitoring, and file integrity validation.

## Defensive Measures

### 1. Network-Level Protection (iptables)
- Configured rules to allow FTP access only from trusted IPs (Kali Linux).
- Denied all other inbound FTP connections.

### 2. Real-Time FTP Traffic Monitoring
- Deployed a script to monitor FTP traffic.
- Detected `SITE CPFR` and `SITE CPTO` usage.
- Logged suspicious activity and blocked attacker IPs automatically.

### 3. File Integrity Monitoring
- Monitored MD5 hashes of critical system files.
- Alerted on any unauthorized changes suggesting compromise.

### 4. Persistent Firewall Rules
- Startup script saved at `/etc/network/if-pre-up.d/iptables`.
- Ensured `iptables` rules persisted across reboots.

## Defense Validation

### Before Implementation
- Exploit was successful (Phase 1).
- Demonstrated file access and command execution.

### After Implementation
- Exploit failed: system directory non-writable.
- Logs confirmed detection and IP blocking.

## Security Analysis
- **Prevention**: FTP access limited via IP restrictions.
- **Detection**: Monitoring identified exploit patterns.
- **Response**: Automated IP blocking in real time.
- **Verification**: File integrity checks caught changes.

## Key Lessons
1. Layered defenses are most effective.
2. Firewall rules are essential first-line defenses.
3. Real-time detection speeds up response.
4. File integrity monitoring confirms breaches.

## Recommendations
- Harden ProFTPD configuration.
- Regular patch management.
- Expand logging scope.
- Educate users on secure FTP usage.
- Perform periodic vulnerability assessments.

## Conclusion
Our layered security approach effectively neutralized the previously exploitable vulnerability. This defensive architecture enhances resilience against similar threats in real-world environments.
