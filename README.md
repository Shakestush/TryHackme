# BugBounty Hacker - TryHackMe Challenge

## Overview
This repository documents my walkthrough of the "Bounty Hacker" room on TryHackMe - a beginner-friendly Capture The Flag (CTF) challenge that simulates a real-world scenario of penetration testing a misconfigured Linux-based web server.

## Challenge Objective
The goal was to identify and exploit weak credentials and misconfigurations to gain initial access, escalate privileges, and retrieve user and root flags.

## Skills Demonstrated
- **Enumeration** using Nmap to identify open ports and services
- **FTP analysis** and basic file transfers with anonymous login
- **Brute-force attack** using Hydra on SSH service
- **Linux privilege escalation** via sudo permission misconfiguration
- **Basic post-exploitation techniques**

## Walkthrough Summary

### 1. Initial Enumeration
Used Nmap to scan the target machine and identify open ports and services:
- Port 21 (FTP)
- Port 22 (SSH)
- Port 80 (HTTP)

### 2. Information Gathering
Accessed the FTP server with anonymous login credentials and discovered two critical files:
- `locks.txt` - A password list
- `task.txt` - A task list written by user "lin"

### 3. Gaining Initial Access
Used Hydra to brute-force SSH login with the discovered username and password list:
```
hydra -l lin -P locks.txt ssh://[target-ip]
```
Successfully obtained the password: `RedDr4gonSynd1cat3`

### 4. User Flag Capture
Logged in via SSH with the credentials and retrieved the user flag:
```
THM{CR1M3_SyNd1C4T3}
```

### 5. Privilege Escalation
Enumerated sudo permissions with `sudo -l` and discovered that the user could run `tar` with sudo privileges.
Exploited this misconfiguration using GTFOBins technique:
```
sudo /bin/tar -cf /dev/null /dev/null --checkpoint=1 --checkpoint-action=exec=/bin/sh
```

### 6. Root Flag Capture
Successfully escalated to root and obtained the root flag from `/root/root.txt`

## Tools Used
- Nmap
- Hydra
- SSH client
- Basic Linux commands

## Conclusion
This challenge reinforces the importance of:
- Proper access controls
- Strong password policies
- Regular security audits
- Careful configuration of sudo permissions

## Author
Prepared by: Manasseh Mutugi  gmail manasssehmutugi222@gmail.com 
Position: SOC Analyst  
Department: Cybersecurity Research  
Date: April 2025
