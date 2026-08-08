# Incident Response Playbook

## Purpose

Define a repeatable process for investigating and responding to security incidents detected by the SOC.

## Response Lifecycle

1. **Identification** – Review alerts and determine whether activity is suspicious.
2. **Investigation** – Analyse affected hosts, processes, users, commands, and related telemetry.
3. **Containment** – Isolate or restrict affected systems to prevent further activity.
4. **Eradication** – Remove malicious activity and address the underlying cause.
5. **Recovery** – Restore normal operations and monitor for recurring activity.
6. **Lessons Learned** – Document findings, evidence, and improvements.

## Incident Evidence

The investigation should capture:

* Alert and detection rule
* Affected endpoint
* Process and command-line activity
* Relevant Sysmon events
* MITRE ATT&CK technique
* Timeline of activity
* Containment and remediation actions
* Final incident outcome

## Incident Classification

| Severity | Description                                         |
| -------- | --------------------------------------------------- |
| Low      | Suspicious activity with limited impact             |
| Medium   | Confirmed malicious activity affecting an endpoint  |
| High     | Significant compromise or multiple affected systems |
| Critical | Widespread compromise or major business impact      |

## Outcome

This playbook provides a consistent workflow for progressing from security alert identification through investigation, containment, recovery, and lessons learned.
