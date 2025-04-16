# Snort IDS-IPS: Comprehensive Implementation Study

## Overview
This repository documents my hands-on implementation and analysis of Snort, an open-source network intrusion detection and prevention system (IDS/IPS). The project demonstrates practical application of Snort in various operational modes, packet analysis, and custom rule creation.

## About Snort
Snort is a widely-used open-source solution developed by Martin Roesch in 1998 for real-time traffic analysis and packet logging. It helps security professionals detect and prevent network-based attacks through signature-based detection.

## Security Importance

| Security Aspect | How Snort Helps |
|-----------------|-----------------|
| Intrusion Detection | Identifies known attacks using signature-based detection |
| Intrusion Prevention | Blocks malicious traffic before it reaches the target |
| Traffic Monitoring | Analyzes network traffic for suspicious behavior |
| Compliance | Helps organizations meet security standards (PCI-DSS, HIPAA, GDPR) |
| Threat Intelligence | Continuously updated rule sets improve threat visibility |

## Project Components

### 1. Basic Configuration & Setup
- Installation and verification of Snort build (v149)
- Configuration file testing and rule loading validation
- Implementation of different configuration approaches

### 2. Operational Modes Implemented

#### Packet Logger Mode
- Traffic capture and detailed packet analysis
- Source/destination port identification
- IP ID tracking and HTTP referrer analysis
- TCP acknowledgment number examination

#### IDS/IPS Mode
- Real-time traffic monitoring and alert generation
- HTTP method detection and tracking
- Automated threat identification

#### PCAP Investigation
- Analysis of captured network traffic
- Alert generation and pattern recognition
- TCP segment queue analysis
- HTTP header extraction and examination

### 3. Custom Rule Development
- Creation of custom detection rules for specific threats
- Implementation of rules to filter based on:
  - IP identification
  - TCP flags (Push-Ack)
  - Source/destination matching
- Performance testing of custom rules against sample traffic

## Skills Demonstrated
- Network traffic analysis
- Intrusion detection configuration
- Custom rule writing and optimization
- PCAP file investigation
- Alert analysis and interpretation
- Security threat identification

## Tools & Environment
- Snort IDS/IPS
- PCAP analysis tools
- Linux environment
- TryHackMe virtual lab

## Author
**Prepared by:** Manasseh Mutugi  
**Position:** SOC Analyst  
**Department:** Cybersecurity Research  
**Date:** March 2025

