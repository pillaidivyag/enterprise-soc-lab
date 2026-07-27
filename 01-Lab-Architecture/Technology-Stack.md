# Technology Stack

## Document Information

| Field | Value |
|-------|-------|
| Project | Enterprise SOC Lab: Detection Engineering & Incident Response with Wazuh |
| Document | Technology Stack |
| Version | 1.0 |
| Status | Approved |
| Author | Divya Pillai |

---

# 1. Purpose

This document describes the technologies selected for the Enterprise SOC Lab, explains their role within the environment, and outlines the reasons they were chosen.

The primary design goals were:

- Build a production-inspired SOC using only free and open-source technologies.
- Demonstrate practical security operations skills.
- Integrate endpoint, network and cloud telemetry into a single monitoring platform.
- Produce a portfolio that reflects enterprise security practices.

---

# 2. Design Principles

The technology stack was selected using the following principles:

- Free and open-source where possible.
- Enterprise relevance.
- Active community support.
- Integration with other security tools.
- Practical experience applicable to Security Analyst and SOC Analyst roles.

---

# 3. Technology Overview

| Category | Technology | Purpose |
|----------|------------|---------|
| SIEM | Wazuh | Central security monitoring and alerting |
| Search Engine | OpenSearch | Log indexing and search |
| Dashboards | OpenSearch Dashboards | Visualisation and reporting |
| Endpoint Monitoring | Wazuh Agent | Collect endpoint telemetry |
| Windows Logging | Sysmon | Detailed Windows event logging |
| IDS | Suricata | Network intrusion detection |
| Network Analysis | Zeek | Network metadata and protocol analysis |
| Packet Capture | Wireshark / tcpdump | Packet inspection and troubleshooting |
| Vulnerability Management | Greenbone Community Edition (OpenVAS) | Vulnerability scanning |
| Attack Simulation | Atomic Red Team | Safe security testing |
| Threat Mapping | MITRE ATT&CK Navigator | ATT&CK technique mapping |
| Cloud | AWS Free Tier | Cloud audit logging and monitoring |
| Version Control | Git / GitHub | Source control and documentation |
| Documentation | Markdown | Project documentation |

---

# 4. Security Information and Event Management (SIEM)

## Wazuh

### Purpose

Wazuh serves as the central Security Information and Event Management platform for the SOC.

### Responsibilities

- Log collection
- Security event correlation
- Alert generation
- File Integrity Monitoring
- Vulnerability detection
- Security configuration assessment
- Endpoint monitoring

### Why Wazuh?

Wazuh was selected because it:

- Is fully open source.
- Integrates well with Windows and Linux.
- Supports enterprise security monitoring.
- Includes built-in detection capabilities.
- Is widely used in SOC laboratories and professional environments.

---

# 5. Search and Analytics

## OpenSearch

OpenSearch stores and indexes security events collected by Wazuh.

### Responsibilities

- Fast log searching
- Event indexing
- Historical log storage
- Correlation support

### Why OpenSearch?

OpenSearch provides scalable search capabilities while remaining fully open source.

---

# 6. Dashboards

## OpenSearch Dashboards

Dashboards provide visual representation of security events.

Examples include:

- Alert trends
- Failed logins
- Endpoint activity
- MITRE ATT&CK coverage
- Detection statistics
- Incident summaries

---

# 7. Endpoint Monitoring

## Wazuh Agent

Installed on monitored endpoints.

Responsibilities:

- Collect operating system logs.
- Forward security events.
- Monitor file changes.
- Support vulnerability detection.

---

## Sysmon

Sysmon provides detailed Windows telemetry that exceeds the standard Windows Event Log.

Examples include:

- Process creation
- Network connections
- Driver loading
- Registry modifications
- DLL loading
- Parent-child process relationships

This additional visibility significantly improves detection engineering.

---

# 8. Network Security Monitoring

## Suricata

Suricata provides signature-based intrusion detection.

Detects:

- Known attacks
- Malware traffic
- Command and Control activity
- Port scanning
- Suspicious protocols

---

## Zeek

Unlike Suricata, Zeek focuses on network behaviour.

Produces metadata for:

- DNS
- HTTP
- SSL/TLS
- FTP
- SMTP
- SMB

This information supports threat hunting and forensic investigations.

---

# 9. Packet Analysis

## Wireshark

Wireshark is used for graphical packet inspection.

Typical use cases include:

- Traffic validation
- Protocol analysis
- Malware investigations

---

## tcpdump

tcpdump provides lightweight command-line packet capture for Linux systems.

---

# 10. Vulnerability Management

## Greenbone Community Edition (OpenVAS)

Used to:

- Discover vulnerabilities
- Prioritise remediation
- Validate security posture
- Support vulnerability reporting

---

# 11. Attack Simulation

## Atomic Red Team

Atomic Red Team enables safe simulation of attacker behaviour.

Examples include:

- PowerShell execution
- Credential access
- Persistence
- Privilege escalation

These simulations validate detection capabilities without using real malware.

---

# 12. Threat Intelligence

## MITRE ATT&CK Navigator

Used to:

- Map attacker techniques
- Classify detections
- Improve investigation consistency
- Measure detection coverage

---

# 13. Cloud Security

The project incorporates a limited AWS Free Tier environment.

Cloud monitoring focuses on:

- IAM activity
- CloudTrail audit events
- Amazon S3 events

This demonstrates hybrid security monitoring while maintaining a zero-cost objective.

---

# 14. Version Control

Git and GitHub are used to:

- Track project changes
- Maintain documentation
- Demonstrate development history
- Publish the portfolio

---

# 15. Summary

The selected technology stack provides comprehensive visibility across endpoint, network and cloud environments while remaining entirely based on free and open-source technologies or free cloud services. Together, these components enable the implementation of a realistic enterprise-inspired Security Operations Center capable of monitoring, detecting, investigating and responding to security incidents.