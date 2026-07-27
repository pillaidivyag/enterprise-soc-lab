# Lab Deployment

## Overview

This phase covers the deployment of the core SOC platform used throughout the Enterprise SOC Lab.

The objective is to build a centralised security monitoring environment capable of collecting, processing and visualising security telemetry from endpoints, network sensors and cloud services.

---

## Deployment Scope

The following components will be deployed:

| Component | Purpose |
|---|---|
| Ubuntu Desktop | SOC server platform |
| Wazuh Manager | SIEM, log collection and security monitoring |
| OpenSearch | Event indexing and storage |
| OpenSearch Dashboards | Security visualisation and investigation |
| Supporting tools | System monitoring and validation |

---

## Deployment Architecture

```
Windows Endpoint
       |
       |
Wazuh Agent
       |
       |
       v
+----------------+
| Wazuh Manager  |
|    Ubuntu      |
+----------------+
       |
       |
       v
+----------------+
|  OpenSearch    |
+----------------+
       |
       |
       v
+----------------------+
| OpenSearch Dashboard |
+----------------------+
```

---

## Deployment Objectives

The deployment phase will achieve:

- Installation of the SOC monitoring platform.
- Configuration of the SIEM components.
- Verification of service availability.
- Validation of dashboard access.
- Preparation for endpoint onboarding.

---

## Deployment Sequence

The deployment will be completed in the following order:

1. Prepare Ubuntu SOC system.
2. Install Wazuh Manager.
3. Install OpenSearch.
4. Configure OpenSearch Dashboards.
5. Validate platform health.
6. Prepare environment for asset onboarding.

---

## Prerequisites

Required environment:

| Component | Details |
|---|---|
| Virtualisation | VMware Workstation Pro |
| SOC Platform | Ubuntu Desktop |
| Endpoint | Windows 11 Home |
| Attack Platform | Kali Linux |
| Network | Internal VMware virtual network |

---

## Validation Criteria

The deployment phase is complete when:

- Wazuh Manager is running successfully.
- OpenSearch services are operational.
- Dashboard interface is accessible.
- System resources are stable.
- The platform is ready to receive security events.

---

## Deliverables

Completed outputs:

- Wazuh deployment documentation.
- OpenSearch deployment documentation.
- Dashboard configuration documentation.
- Validation evidence.
- Screenshots and logs stored in `10-Evidence`.

---

## Next Phase

After successful deployment, assets will be connected in:

`03-Asset-Onboarding`

This will include Windows endpoint monitoring, Sysmon deployment, Ubuntu agent onboarding and cloud telemetry integration.