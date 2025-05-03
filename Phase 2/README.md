# Phase 2: Splunk Installation and Configuration

## Overview
This phase involves setting up a Splunk Enterprise SIEM system to collect and analyze security events from the attacker and victim machines, enabling attack detection and pattern analysis.

## Splunk Installation
- Installed Splunk Enterprise on a dedicated server.
- Configured admin account and enabled data receiving.

## Data Collection Configuration

### On Victim Machine (Metasploitable3)
- Installed Splunk Universal Forwarder.
- Collected:
  - ProFTPD logs (`/tmp/ftp_traffic.log`)
  - Authentication logs (`/var/log/auth.log`)
  - System logs (`/var/log/syslog`)

### On Attacker Machine (Kali Linux)
- Installed Splunk Universal Forwarder.
- Monitored:
  - Metasploit logs (`/root/.msf4/logs`)
  - Auth logs, system logs, and custom script logs.

## Attack Replay and Data Generation
- Re-executed Phase 1 attack to generate log data for analysis.
- Used both Metasploit and custom scripts.

## Dashboard Development

### FTP Attack Detection
- Search Query:
  ```spl
  source="*proftpd*" OR sourcetype="*ftp*" OR "ProFTPD"
