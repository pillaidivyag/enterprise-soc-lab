# Lab Architecture

## Overview

This phase defines the architecture and design foundation of the Enterprise SOC Lab.

The objective is to document the planned security monitoring environment, including system components, technologies, assets and security data flows before deployment begins.

---

## Objectives

This phase focuses on:

- Defining the SOC architecture.
- Identifying required assets and systems.
- Documenting security technologies.
- Designing infrastructure and data flow diagrams.
- Establishing the foundation for deployment.

---

## Architecture Components

The lab consists of the following primary components:

| Component | Purpose |
|---|---|
| Ubuntu Desktop | Central SOC platform |
| Windows 11 Home | Enterprise endpoint simulation |
| Kali Linux | Attack simulation platform |
| AWS Services | Cloud security monitoring |
| Wazuh | SIEM and security monitoring |
| OpenSearch | Log storage and analysis |
| Suricata | Network intrusion detection |
| Zeek | Network traffic analysis |
| Greenbone Community Edition | Vulnerability assessment |

---

## Documents

| Document | Description |
|---|---|
| SOC-Architecture.md | High-level SOC design and architecture overview |
| Technology-Stack.md | Security tools and technologies used in the lab |
| Asset-Inventory.md | List of systems, roles and configurations |
| Architecture-Diagram.drawio | Visual representation of the SOC architecture |
| Security-Data-Flow.drawio | Security telemetry flow between components |
| SOC-Network-Architecture.puml | Network architecture source diagram |

---

## Architecture Design Principles

The architecture follows these principles:

- Separation of security monitoring and attack simulation environments.
- Centralised security event collection.
- Visibility across endpoint, network and cloud environments.
- Documentation aligned with enterprise security practices.
- Design supporting detection engineering and incident response activities.

---

## Deliverables

Completed outputs from this phase:

- SOC architecture documentation.
- Asset inventory.
- Technology selection.
- Architecture diagram.
- Security data flow diagram.

---

## Next Phase

The next phase is:

`02-Lab-Deployment`

This phase will deploy the SOC platform components, including Wazuh, OpenSearch and dashboards on the Ubuntu SOC system.