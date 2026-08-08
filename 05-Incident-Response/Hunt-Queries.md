# Threat Hunting Queries

## Objective

Use existing Wazuh and Sysmon telemetry to proactively identify suspicious activity that may indicate attacker behaviour.

## Hunt 1 — PowerShell Activity

**MITRE ATT&CK:** T1059.001 – PowerShell

Search for unusual PowerShell execution, particularly encoded commands, hidden windows, or suspicious command-line arguments.

**Data source:** Sysmon Event ID 1

## Hunt 2 — Account Discovery

**MITRE ATT&CK:** T1087 – Account Discovery

Search for commands such as `net user`, `net accounts`, and other account enumeration activity.

**Data source:** Sysmon Event ID 1

## Hunt 3 — Suspicious Process Execution

**MITRE ATT&CK:** T1059 – Command and Scripting Interpreter

Review unusual command interpreters and parent-child process relationships.

**Data source:** Sysmon Event ID 1

## Hunt 4 — Network Activity

**MITRE ATT&CK:** T1049 – System Network Connections Discovery

Review endpoint network connection telemetry for unusual destinations, processes, or connection patterns.

**Data source:** Endpoint and network telemetry

## Hunt 5 — Persistence

**MITRE ATT&CK:** T1547 – Boot or Logon Autostart Execution

Search for suspicious processes or configuration changes associated with persistence mechanisms.

**Data source:** Sysmon and Windows event telemetry

## Hunting Outcome

Hunt findings should be investigated, documented, and converted into new detection rules where existing controls do not adequately identify the activity.