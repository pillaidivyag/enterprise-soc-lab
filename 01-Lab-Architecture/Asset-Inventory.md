# Asset Inventory

## Document Information

| Field | Value |
|-------|-------|
| Project | Enterprise SOC Lab: Detection Engineering & Incident Response with Wazuh |
| Document | Asset Inventory |
| Version | 1.1 |
| Status | Approved |
| Author | Divya Pillai |
| Classification | Portfolio Project |

---

# 1. Purpose

This document provides a complete inventory of all assets deployed within the Enterprise SOC Lab.

Maintaining an accurate asset inventory is a fundamental security practice that supports security monitoring, vulnerability management, incident response, threat hunting and risk assessment.

The inventory will be updated throughout the project as additional security tools and cloud resources are introduced.

---

# 2. Lab Environment

The Enterprise SOC Lab is hosted on VMware Workstation Pro using isolated virtual machines.

The objective of the environment is to simulate a small enterprise network where security events are generated, collected, analysed and investigated through a central Security Operations Center (SOC).

The current lab consists of:

- Ubuntu Desktop LTS (SOC Platform)
- Windows 11 Home (Enterprise Endpoint Simulation)
- Kali Linux (Attack Simulation Platform)
- AWS Free Tier (Cloud Monitoring - Later Project Phase)

The project has been designed to use free and open-source technologies together with AWS Free Tier services, maintaining a total project cost target of **£0**.

---

# 3. Asset Classification

| Asset Category | Description |
|----------------|-------------|
| SOC Platform | Central security monitoring infrastructure |
| Endpoint | Windows workstation used for monitoring and attack simulations |
| Attack Platform | Kali Linux used for authorised security testing |
| Cloud Services | AWS Free Tier resources used for cloud monitoring |

---

# 4. Asset Inventory

| Asset ID | Hostname | Asset Type | Operating System | Purpose | Criticality | Monitoring Status |
|----------|----------|------------|------------------|----------|-------------|-------------------|
| AST-001 | SOC-01 | Virtual Machine | Ubuntu Desktop LTS | Central SOC Platform | Critical | Planned |
| AST-002 | WIN11-CLIENT | Virtual Machine | Windows 11 Home | Enterprise Endpoint Simulation | High | Planned |
| AST-003 | KALI-ATTACK | Virtual Machine | Kali Linux | Attack Simulation | Medium | Planned |
| AST-004 | AWS-CLOUD | Cloud | AWS Free Tier | Cloud Security Monitoring | Medium | Planned |

---

# 5. Asset Details

## AST-001 — SOC-01

### Description

SOC-01 hosts the core Security Operations Center platform.

Ubuntu Desktop LTS has been selected for the lab because it simplifies deployment, troubleshooting and documentation while providing the same security monitoring capabilities required for the project.

### Operating System

Ubuntu Desktop LTS

### Planned Software

- Wazuh Manager
- OpenSearch
- OpenSearch Dashboards
- Suricata
- Zeek
- Greenbone Community Edition (OpenVAS)
- Git
- OpenSSH Server

### Responsibilities

- Centralised log collection
- Security event correlation
- Alert generation
- Dashboard hosting
- Threat hunting
- Vulnerability management
- Incident investigation support

### Business Criticality

Critical

---

## AST-002 — WIN11-CLIENT

### Description

WIN11-CLIENT represents a standard enterprise user workstation.

Although the lab uses Windows 11 Home, the endpoint will be configured with enterprise security tooling to simulate a managed corporate workstation.

### Operating System

Windows 11 Home

### Planned Software

- Wazuh Agent
- Sysmon
- Microsoft Defender
- Atomic Red Team
- PowerShell

### Responsibilities

- Generate endpoint security telemetry
- Simulate enterprise user activity
- Validate detection rules
- Support incident investigations

### Business Criticality

High

---

## AST-003 — KALI-ATTACK

### Description

Dedicated security testing workstation used exclusively for authorised attack simulations within the isolated lab environment.

### Operating System

Kali Linux

### Planned Software

- Nmap
- Hydra
- Netcat
- Burp Suite Community Edition
- Gobuster
- Nikto
- Metasploit Framework (Optional)

### Responsibilities

- Attack simulation
- Network reconnaissance
- Detection validation
- Security testing

### Business Criticality

Medium

---

## AST-004 — AWS-CLOUD

### Description

AWS Free Tier environment used to demonstrate hybrid cloud security monitoring.

Only Free Tier eligible services will be used.

### Planned Services

- AWS IAM
- AWS CloudTrail
- Amazon S3

### Responsibilities

- Cloud audit logging
- Identity monitoring
- Cloud security event generation

### Business Criticality

Medium

---

# 6. Security Monitoring Coverage

| Asset | Log Collection | Endpoint Monitoring | Network Monitoring | Vulnerability Scanning | Incident Investigation |
|--------|---------------|--------------------|-------------------|-----------------------|------------------------|
| SOC-01 | Yes | Yes | Yes | Yes | Yes |
| WIN11-CLIENT | Yes | Yes | Indirect | Planned | Yes |
| KALI-ATTACK | Basic System Logs | Limited | Indirect | Planned | Limited |
| AWS-CLOUD | CloudTrail | N/A | N/A | Configuration Review | Yes |

---

# 7. Network Overview

The laboratory consists of isolated virtual machines hosted on VMware Workstation Pro.

The virtual network enables communication between:

- SOC Platform
- Windows Endpoint
- Kali Linux
- AWS Free Tier services (later project phase)

The environment is completely isolated from production systems.

---

# 8. Asset Naming Standard

| Asset Type | Naming Convention | Example |
|------------|------------------|---------|
| SOC Platform | SOC-01 | SOC-01 |
| Windows Endpoint | WIN11-CLIENT | WIN11-CLIENT |
| Kali Platform | KALI-ATTACK | KALI-ATTACK |
| Cloud Resources | AWS-<Service> | AWS-CloudTrail |

---

# 9. Future Assets

Future project phases may introduce:

- Additional Windows endpoints
- OWASP Juice Shop
- Additional AWS Free Tier services

Every new asset will be documented before deployment.

---

# 10. Asset Lifecycle

Every asset follows the same management process:

1. Deploy the asset.
2. Configure the operating system.
3. Assign a hostname.
4. Record the asset in this inventory.
5. Install security software.
6. Enable monitoring.
7. Validate telemetry.
8. Include the asset in dashboards and detection rules.

---

# 12. Conclusion

The asset inventory provides the foundation for effective security operations by maintaining a structured record of all monitored systems within the Enterprise SOC Lab. As the project evolves, this document will be updated to reflect newly deployed assets and cloud services while ensuring consistency across deployment, monitoring and incident response activities.