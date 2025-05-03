# ICS344-02-G3-Final-Project
# ICS344 Cybersecurity Project

## Team Information

### Group Number: 02

### Team Members:
- **Mohammed Almubarak** - 202024880
- **Ammar Alabdullah** - 202024140
- **Ahmed Alajwad** - 201935930

## Work Distribution

### Phase 1: Setup and Compromise the Service
- **Mohammed Almubarak**: Environment setup, reconnaissance, vulnerability identification, metasploit exploitation, documentation, Custom script development, testing

### Phase 2: Visual Analysis with a SIEM Dashboard
- **Ammar Alabdullah**: Splunk server setup, forwarder configuration Log, integration, dashboard creation, visualization, pattern analysis

### Phase 3: Defensive Strategy Proposal
- **Mohammed, Ammar, Ahmed**: Network-level defenses, testing, File permission hardening, documentation, User account security, before/after comparison

## Project Overview

This repository contains our comprehensive work for the ICS344 Cybersecurity Project, which involved setting up and attacking a vulnerable service, analyzing the attack with a SIEM platform, and proposing a defensive strategy.

### Phase 1: Setup and Compromise the Service
In this phase, we set up Metasploitable3 as our victim machine and Kali Linux as our attack platform. We identified vulnerabilities in the ProFTPD service and successfully exploited them using the Metasploit Framework and a custom Python script.

### Phase 2: Visual Analysis with a SIEM Dashboard
We implemented Splunk as our SIEM solution, collecting and analyzing logs from the victim and attacker machines. We created comprehensive dashboards to visualize attack patterns and established detection mechanisms for FTP-based attacks.

### Phase 3: Defensive Strategy Proposal
Based on our findings from previous phases, we implemented multiple layers of defense to protect against the ProFTPD vulnerability. Our defense strategy included network filtering with iptables, file permission hardening, and user account restrictions. We demonstrated the effectiveness of our defenses through comprehensive testing.

## Repository Structure

```
ICS344-Project/
├── README.md                   # This file
├── Phase1/                     # Setup and exploitation
│   ├── README.md               # Phase 1 documentation
│   └── ...                     # Scripts, screenshots, etc.
├── Phase2/                     # SIEM analysis
│   ├── README.md               # Phase 2 documentation
│   └── ...                     # Dashboard configs, screenshots, etc.
└── Phase3/                     # Defense strategy
    ├── README.md               # Phase 3 documentation
    └── ...                     # Defense implementation, testing evidence, etc.
```

## Tools and Technologies Used

- **Virtual Environments**: VirtualBox
- **Vulnerable Target**: Metasploitable3
- **Attack Platform**: Kali Linux
- **SIEM Solution**: Splunk Enterprise
- **Security Tools**: Metasploit Framework, iptables, custom Python scripts
