# Detection Engineering

## Overview

Detection engineering focuses on designing, implementing, and validating security detections that identify malicious or suspicious activity within the enterprise environment. In this phase, endpoint telemetry is enhanced using Sysmon, ingested by Wazuh, and used to develop detection rules aligned with real-world attack techniques.

## Objectives

* Deploy Sysmon for enhanced endpoint telemetry.
* Configure Wazuh to collect and process Sysmon events.
* Develop custom detection rules for common attack techniques.
* Map detections to the MITRE ATT&CK framework.
* Validate detections through attack simulation and event analysis.

## Deliverables

* Sysmon deployment and configuration
* Sysmon event collection in Wazuh
* Custom detection rules
* MITRE ATT&CK mapping
* Detection validation evidence

## Contents

* **Sysmon-Configuration.md** – Installation and configuration of Sysmon on the Windows endpoint.
* **Custom-Detection-Rules.md** – Custom Wazuh detection rules for suspicious activities.
* **MITRE-Mapping.md** – Mapping of implemented detections to MITRE ATT&CK techniques.
* **Sysmon-Service-Running.png** – Evidence of successful Sysmon installation.
* **Sysmon-Events.png** – Wazuh dashboard displaying Sysmon event collection.
* **Detection-Rule-Validation.png** – Evidence of successful detection rule execution.

## Outcome

At the end of this phase, the SOC is capable of collecting detailed endpoint telemetry, detecting malicious behavior using custom rules, and mapping security events to the MITRE ATT&CK framework, providing a solid foundation for threat hunting and incident investigations.
