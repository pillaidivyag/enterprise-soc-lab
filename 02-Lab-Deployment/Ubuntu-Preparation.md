# Ubuntu Preparation

## Overview

This document covers the preparation of the Ubuntu Desktop virtual machine used as the SOC platform.

The objective is to ensure the system is ready for installation of Wazuh, OpenSearch and supporting security monitoring components.

---

# System Role

| Component | Details |
|---|---|
| Host Role | SOC Server |
| Operating System | Ubuntu Desktop LTS |
| Virtualisation | VMware Workstation Pro |
| Primary Function | SIEM and security monitoring platform |

---

# Preparation Objectives

The Ubuntu SOC system will be prepared by:

- Verifying system requirements.
- Updating operating system packages.
- Configuring hostname.
- Validating network connectivity.
- Installing required dependencies.
- Preparing storage and resources.

---

# System Requirements

Recommended minimum resources:

| Resource | Requirement |
|---|---|
| CPU | 4 cores |
| RAM | 8 GB minimum |
| Storage | 50 GB+ |
| Network | Internet access required |

Additional resources may improve performance when running Wazuh, OpenSearch and dashboards together.

---