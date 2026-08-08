# Incident Investigation

## Incident Overview

A controlled security incident was generated on the Windows 11 endpoint using Atomic Red Team to validate the SOC's incident response capability.

## Detection

Wazuh detected account discovery activity generated through Sysmon process creation telemetry.

* **Endpoint:** Windows11
* **IP:** 192.168.52.141
* **MITRE ATT&CK:** T1087 – Account Discovery
* **Wazuh Rules:** 92031, 92039
* **Sysmon Event:** Event ID 1 – Process Creation

The Wazuh rules used during the exercise were existing Wazuh detection rules and were not custom rules created for this project.

## Investigation

The alert showed execution of account discovery commands including `net user` and `net accounts`.

Sysmon provided process information including command line, parent process, user context and file hashes.

The endpoint's established network connections were also reviewed. The Wazuh agent communication with the manager was identified on TCP port 1514.

Associated processes were reviewed using their process IDs to determine which applications were responsible for the observed network connections.

## Assessment

The activity was confirmed as the expected Atomic Red Team simulation rather than an uncontrolled compromise.

No active `net.exe` process remained after the simulation.

## Containment

For a real incident, the affected endpoint would be isolated from the network while preserving evidence.

Because this was a controlled lab simulation, network isolation was not performed so that SOC monitoring could continue normally.

## Recovery

The Wazuh agent service was verified as running after the investigation.

The endpoint remained under monitoring and no active `net.exe` process was present.

## Closure

The simulated incident was closed after:

* Detection was confirmed.
* Endpoint activity was investigated.
* Network connections were reviewed.
* Associated processes were identified.
* The simulated activity ended.
* Wazuh monitoring remained operational.

## Lessons Learned

The exercise demonstrated an end-to-end incident response workflow using real endpoint telemetry.

The investigation showed the value of combining Sysmon process data, Wazuh alerts, endpoint information and network connection analysis when triaging suspicious activity.
