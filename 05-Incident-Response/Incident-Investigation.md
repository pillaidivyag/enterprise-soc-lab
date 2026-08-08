# Incident Investigation

## Incident Overview

A controlled security test was executed against the Windows 11 endpoint using Atomic Red Team to validate the SOC incident response process.

## Detection

Wazuh detected account discovery activity through Sysmon process creation telemetry.

* Endpoint: Windows11
* IP: 192.168.52.141
* MITRE ATT&CK: T1087 – Account Discovery
* Wazuh Rules: 92031, 92039
* Sysmon Event: 1 – Process Creation

## Investigation

The Wazuh alert showed execution of `net user` and `net accounts` commands.

The Sysmon telemetry provided process details including command line, parent process, user context and file hashes.

The activity was traced to the Windows endpoint and confirmed as the expected Atomic Red Team simulation.

## Containment

The incident response procedure identified the endpoint for isolation if the activity represented a real compromise.

Because this was a controlled lab simulation, the endpoint was not actually disconnected from the network.

## Recovery

The simulated command execution had completed and no `net.exe` process remained active on the endpoint.

The Wazuh agent remained operational and continued providing endpoint telemetry.

## Incident Closure

The simulated incident was closed after confirming:

* The detection successfully triggered.
* The activity was investigated using endpoint telemetry.
* The simulated process was no longer running.
* Wazuh monitoring remained operational.

## Evidence

* Wazuh T1087 detection
* Sysmon process creation event
* Windows endpoint identification
* Wazuh agent health verification

## Lessons Learned

The exercise demonstrated an end-to-end incident response workflow from detection and investigation through containment decision and recovery verification.

The lab also confirmed that Sysmon and Wazuh provide sufficient endpoint telemetry for initial incident investigation.
