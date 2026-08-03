# Windows 11 Agent

## Overview

This document describes the deployment and registration of the Wazuh Agent on the Windows 11 endpoint.

The Windows endpoint will provide security telemetry including Windows Event Logs, authentication events, process creation, PowerShell activity and system changes for centralised monitoring in the Wazuh platform.

---

## System Information

| Component | Value |
|---|---|
| Asset Name | Windows-11 |
| Operating System | Windows 11 Home |
| Role | Enterprise Workstation |
| Monitoring | Wazuh Agent + Sysmon |

---

## Objectives

- Install the Wazuh Agent.
- Register the endpoint with the Wazuh Manager.
- Verify agent connectivity.
- Confirm security events are received by Wazuh.

---

## Installation

### 1. Download the Wazuh Agent

Download the latest Windows Wazuh Agent from the official Wazuh website.

---

### 2. Install the Agent

Run the installer as Administrator.

During installation, specify:

| Setting | Value |
|---|---|
| Manager Address | Ubuntu SOC Server IP |
| Agent Name | Windows-11 |
| Group | default |

Complete the installation.

---

### 3. Start the Service

Verify the Wazuh Agent service is running.

Expected service:

```
Wazuh Agent
Status: Running
```

---

## Validation

The installation is successful when:

- Windows-11 appears in **Agents Management**.
- Agent status is **Active**.
- Windows security events are received.
- Endpoint inventory is available.

---

## Evidence

Capture the following screenshots:

- Wazuh Agent Windows service
- Windows-11 listed in Agents Management
- Agent details page
- Initial security events

Store screenshots in:

`10-Evidence/Screenshots/`

---

## Next Phase

After successful onboarding, Sysmon will be installed to enhance endpoint telemetry and improve threat detection.