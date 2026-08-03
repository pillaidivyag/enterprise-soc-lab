# Asset Onboarding

## Overview

This phase integrates endpoints and cloud services into the Wazuh platform, enabling centralised security monitoring across the Enterprise SOC Lab.

Once onboarded, security events from Windows, Linux and AWS will be collected, correlated and analysed through the Wazuh Dashboard.

---

## Objectives

- Register endpoints with Wazuh.
- Collect operating system and security logs.
- Enable endpoint telemetry.
- Validate agent communication.
- Prepare assets for attack simulation and incident investigation.

---

## Assets

| Asset | Operating System | Purpose |
|---|---|---|
| SOC Server | Ubuntu Desktop | SIEM platform and monitored Linux endpoint |
| Endpoint | Windows 11 Home | Enterprise workstation simulation |
| Attacker | Kali Linux | Attack simulation platform |
| Cloud | AWS | Cloud security monitoring using CloudTrail |

---

## Validation Criteria

Asset onboarding is complete when:

- All required agents are connected.
- Endpoint telemetry is visible.
- Security events are received.
- Assets report a healthy status in Wazuh.

---

## Deliverables

- Ubuntu agent deployment
- Windows agent deployment
- Sysmon configuration
- AWS CloudTrail integration
- Asset validation evidence

---

## Next Phase

Following successful onboarding, the environment will be used for attack simulations and detection engineering.