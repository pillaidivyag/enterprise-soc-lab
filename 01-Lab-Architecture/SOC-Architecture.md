# Enterprise SOC Architecture

## Document Information

| Field | Value |
|-------|-------|
| Project | Enterprise SOC Lab: Detection Engineering & Incident Response with Wazuh |
| Document | SOC Architecture |
| Version | 1.0 |
| Status | Approved |
| Author | Divya Pillai |
| Classification | Portfolio Project |

---

# 1. Introduction

## Purpose

This document defines the architecture of the Enterprise SOC Lab. The environment has been designed to simulate the day-to-day operations of a Security Operations Center (SOC) responsible for monitoring, detecting, investigating and responding to cyber security threats across endpoint, server, network and cloud environments.

The objective is to build a realistic enterprise-inspired SOC using free and open-source technologies while following industry best practices for security monitoring and incident response.

---

# 2. Business Scenario

A fictional organisation, **Contoso Retail Ltd.**, operates a hybrid IT environment consisting of Windows workstations, Linux servers and cloud services.

The organisation stores sensitive customer information, internal business data and operational systems that require continuous security monitoring.

To strengthen its cyber defence capability, the organisation has implemented a centralised Security Operations Center responsible for:

- Continuous monitoring of security events
- Endpoint protection
- Network intrusion detection
- Threat detection
- Incident investigation
- Threat hunting
- Vulnerability management
- Security reporting

The SOC receives telemetry from multiple systems and correlates security events to identify malicious activity before it impacts business operations.

---

# 3. Project Objectives

The primary objectives of this project are to:

- Deploy an enterprise-style Security Information and Event Management (SIEM) platform.
- Centralise logs from Windows, Linux and network devices.
- Monitor endpoint activity using endpoint detection capabilities.
- Detect suspicious behaviour using custom detection rules.
- Simulate real-world cyber attacks.
- Investigate security incidents using structured workflows.
- Perform proactive threat hunting.
- Conduct vulnerability assessments.
- Integrate cloud audit events.
- Produce professional documentation suitable for security operations teams.

---

# 4. Scope

The project covers the complete security monitoring lifecycle.

Included within scope:

- SIEM deployment
- Endpoint monitoring
- Network monitoring
- Detection engineering
- Threat hunting
- Incident response
- Vulnerability management
- Cloud security monitoring
- MITRE ATT&CK mapping
- Security dashboards
- Incident documentation

Items outside the scope include:

- High availability deployments
- Production-scale infrastructure
- Multi-region disaster recovery
- Commercial security products

---

# 5. SOC Architecture Overview

The Enterprise SOC consists of four primary components.

## Security Monitoring Platform

Ubuntu Server hosts the central SOC platform including:

- Wazuh Manager
- OpenSearch
- OpenSearch Dashboards
- Suricata
- Zeek
- Greenbone Community Edition (OpenVAS)

This server receives, processes and analyses security telemetry from monitored assets.

---

## Endpoint Systems

### Windows 11 Endpoint

The Windows workstation represents a standard enterprise user device.

Installed software includes:

- Sysmon
- Wazuh Agent

Security events generated on the endpoint are forwarded to the Wazuh Manager for analysis.

---

### Ubuntu Server

The Ubuntu Server hosts the SOC platform while also generating Linux security logs that are monitored by Wazuh.

---

## Attack Platform

A dedicated Kali Linux virtual machine is used to simulate attacker activity.

Typical attack simulations include:

- Port scanning
- Password attacks
- Privilege escalation
- Reverse shells
- PowerShell abuse
- Web application attacks
- Network reconnaissance

These activities generate realistic security events for investigation.

---

## Cloud Environment

A small AWS Free Tier environment will be integrated during later project phases.

Cloud monitoring will include:

- AWS IAM activity
- CloudTrail audit logs
- Amazon S3 events

This demonstrates hybrid enterprise security monitoring without introducing paid cloud services.

---

# 6. Architecture Principles

The SOC has been designed around the following principles.

## Centralised Visibility

All security telemetry is collected into a single monitoring platform to improve visibility and reduce investigation time.

---

## Defence in Depth

Security controls operate across multiple layers:

- Endpoint
- Network
- Server
- Cloud

No single control is relied upon to detect malicious behaviour.

---

## Detection Before Response

Accurate detection is prioritised before incident response activities to minimise false positives.

---

## Least Privilege

Administrative access is limited wherever possible and privileged actions are monitored.

---

## Evidence Preservation

Security logs and investigation evidence are retained throughout the incident lifecycle to support forensic analysis.

---

# 7. Technology Stack

| Category | Technology |
|-----------|------------|
| SIEM | Wazuh |
| Search Platform | OpenSearch |
| Dashboards | OpenSearch Dashboards |
| Endpoint Detection | Wazuh Agent |
| Windows Logging | Sysmon |
| IDS | Suricata |
| Network Analysis | Zeek |
| Packet Capture | Wireshark |
| Vulnerability Scanner | Greenbone Community Edition |
| Attack Simulation | Atomic Red Team |
| Operating Systems | Ubuntu Server, Windows 11, Kali Linux |
| Cloud | AWS Free Tier |
| Version Control | Git |
| Documentation | Markdown |

---

# 8. Security Monitoring Strategy

The SOC continuously monitors:

### Windows

- Authentication events
- PowerShell execution
- Process creation
- Service creation
- Registry modifications
- User account changes
- Privilege escalation
- Scheduled tasks

---

### Linux

- SSH authentication
- Sudo activity
- User management
- Cron jobs
- File integrity changes
- System services

---

### Network

- Port scans
- DNS activity
- HTTP traffic
- SMB connections
- Suspicious protocols
- Intrusion detection alerts

---

### Cloud

- IAM policy changes
- Console logins
- MFA events
- CloudTrail activity
- S3 bucket modifications

---

# 9. Data Flow

Security telemetry follows the workflow below.

1. Activity occurs on an endpoint or network.
2. Logs are generated by the operating system or security tool.
3. Wazuh agents forward endpoint logs to the Wazuh Manager.
4. Suricata and Zeek generate network security events.
5. Wazuh normalises and analyses incoming events.
6. OpenSearch indexes security data.
7. Dashboards provide visualisation and alerting.
8. Security analysts investigate alerts and determine appropriate response actions.

---

# 10. Detection Strategy

The project combines signature-based and behaviour-based detection techniques.

Detection categories include:

- Suspicious PowerShell execution
- Brute force attacks
- Privilege escalation
- Credential access
- Persistence mechanisms
- Lateral movement
- Malware execution
- Network reconnaissance
- Cloud privilege changes

Custom detection rules will be developed throughout the project.

---

# 11. Incident Response Workflow

Every detected security event follows a consistent investigation process.

1. Alert received.
2. Validate alert legitimacy.
3. Collect supporting evidence.
4. Identify indicators of compromise (IOCs).
5. Map attacker behaviour to the MITRE ATT&CK framework.
6. Determine root cause.
7. Recommend containment actions.
8. Document findings.
9. Capture lessons learned.

This structured workflow ensures consistency across all incident investigations.

---

# 12. Expected Outcomes

Upon completion, the SOC will be capable of:

- Monitoring Windows, Linux and cloud environments
- Detecting simulated attacks
- Investigating security incidents
- Performing threat hunting
- Assessing vulnerabilities
- Producing executive and technical reports
- Demonstrating enterprise security operations using open-source technologies

---

# 13. Assumptions

The project assumes:

- VMware Workstation Pro hosts all virtual machines.
- Windows 11, Ubuntu Server and Kali Linux are isolated within a virtual lab environment.
- AWS usage remains within the Free Tier.
- Internet connectivity is available for software installation and updates.
- No production systems are connected to the lab environment.

---

# 14. Conclusion

The Enterprise SOC Lab provides a realistic implementation of a modern Security Operations Center using entirely free and open-source technologies. The environment has been designed to demonstrate practical skills in SIEM administration, detection engineering, incident response, threat hunting, vulnerability management and cloud security monitoring.

By combining structured documentation with hands-on implementation and realistic attack simulations, the project showcases the complete operational lifecycle of a security analyst working within an enterprise SOC.