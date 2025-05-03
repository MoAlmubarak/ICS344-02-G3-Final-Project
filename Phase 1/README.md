# Phase 1: Setup and Service Exploitation

## Overview
This phase focuses on establishing a penetration testing lab using Metasploitable3 and Kali Linux, discovering vulnerabilities, and exploiting them to simulate a real-world cyberattack scenario.

## Environment Setup
- **Target Machine**: Metasploitable3
- **Attacker Machine**: Kali Linux
- **Virtualization Platform**: VirtualBox
- **Network Configuration**: Host-only or Bridged network to ensure VM communication

## Steps Performed

### Metasploitable3 Setup
1. Downloaded Metasploitable3 OVA.
2. Imported it into VirtualBox.
3. Configured network settings.
4. Verified functionality and connectivity.

### Kali Linux Setup
1. Installed Kali Linux in VirtualBox.
2. Configured the network to allow communication with Metasploitable3.
3. Verified connectivity via ping.

## Vulnerability Discovery
- Conducted full port scans.
- Identified ProFTPD 1.3.5 running on port 21.

## Exploitation

### Using Metasploit
- Located and executed the `mod_copy` exploit in Metasploit.
- Successfully accessed and copied system files.

### Custom Script Exploit
- Developed a Python script to exploit the ProFTPD vulnerability.
- Demonstrated exploit effectiveness through file access.

## Security Implications
- Unauthenticated file access.
- Potential for web shell deployment.
- System file exposure.

## Recommendations
- Update ProFTPD.
- Disable unnecessary modules (e.g., `mod_copy`).
- Implement strong access controls and regular patching.

## Conclusion
We successfully identified and exploited a major vulnerability in a controlled environment, laying the groundwork for monitoring and defensive strategies in future phases.
