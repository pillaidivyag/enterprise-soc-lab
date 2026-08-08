# Threat Hunt Report

## Hunt: Account Discovery

**MITRE ATT&CK:** T1087 – Account Discovery
**Data Source:** Wazuh / Sysmon Event ID 1
**Endpoint:** Windows-11

## Objective

Identify account discovery activity that may indicate reconnaissance performed by an attacker.

## Finding

Wazuh captured multiple Sysmon process creation events involving:

* `net.exe accounts`
* `net user guest`
* `net user administrator`

The activity was successfully detected by Wazuh and mapped to **T1087 – Account Discovery**.

## Assessment

The telemetry provides sufficient process and command-line information to investigate account discovery activity, including the executable, command line, user context, parent process, and SHA256 hash.

## Result

**Hunt Status:** Detection confirmed

The existing Wazuh detection successfully identified the activity. No additional detection rule was required for this hunt.

## Recommendation

Continue monitoring account discovery activity and investigate unexpected execution from user or administrative processes.
