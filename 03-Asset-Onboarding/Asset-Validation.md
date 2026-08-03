# Asset Validation

## Overview

This document validates that enterprise assets have been successfully onboarded to the Wazuh Security Operations Center (SOC) and are communicating with the Wazuh Manager.

The validation process confirms successful agent deployment, secure connectivity, and log collection prior to enabling advanced monitoring, threat detection, and incident response.

---

## Onboarded Assets

| Asset | Operating System | Role | Status |
|--------|------------------|------|--------|
| soc-01 | Ubuntu 24.04 LTS | Wazuh Manager | Operational |
| Windows-11 | Windows 11 Home | Monitored Endpoint | Operational |

---

## Validation Activities

The following validation activities were completed:

- Verified Wazuh Manager service availability.
- Confirmed Windows 11 endpoint registration with the Wazuh Manager.
- Verified successful agent authentication and enrollment.
- Confirmed secure communication between the endpoint and the Wazuh Manager.
- Validated endpoint visibility within the Wazuh Dashboard.
- Confirmed Windows security logs are successfully ingested by Wazuh.

---

## Validation Commands

### Ubuntu

```bash
sudo /var/ossec/bin/agent_control -l
```

Expected output:

```
ID: 000  soc-01 (server)
ID: 001  Windows-11
```

### Windows

Verify the Wazuh Agent service is running.

```powershell
Get-Service WazuhSvc
```

Expected Status:

```
Running
```

---

## Validation Evidence

Evidence collected during asset onboarding includes:

- Firewall configuration
- Windows Wazuh Agent installation
- Agent registration
- Wazuh Agents Management view
- Endpoint connection status
- Initial Windows security events

---

## Outcome

Asset onboarding was successfully completed. The Windows 11 endpoint is enrolled with the Wazuh Manager and is ready for endpoint monitoring, detection engineering, threat hunting, and incident response activities.

The SOC environment is now prepared for advanced telemetry collection through Sysmon deployment and attack simulation exercises.