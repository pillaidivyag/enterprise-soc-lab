# Asset Onboarding

## Overview

This phase focuses on onboarding enterprise assets into the Security Operations Center (SOC) by deploying and enrolling endpoints with the Wazuh Manager. Successful onboarding ensures assets are authenticated, actively communicating, and capable of sending security telemetry required for monitoring and threat detection.

## Objectives

* Deploy the Wazuh Agent on enterprise endpoints.
* Register and authenticate assets with the Wazuh Manager.
* Verify successful agent communication.
* Validate endpoint visibility within the Wazuh Dashboard.
* Prepare endpoints for security monitoring and detection engineering.

## Deliverables

* Windows 11 Wazuh Agent deployment
* Agent registration and authentication
* Asset connectivity validation
* Endpoint onboarding evidence

## Contents

* Windows11-Agent.md – Installation, configuration, and enrollment of the Windows 11 Wazuh Agent.
* Asset-Validation.md – Validation of successful endpoint registration, connectivity, and communication with the Wazuh Manager.
* Firewall-Rules.png – Firewall configuration allowing secure agent communication.
* Ubuntu-Agent-Control-Active.png – Evidence of active agent registration from the Wazuh Manager.
* Wazuh-Agent-Running.drawio – Diagram illustrating the endpoint onboarding and agent communication workflow.
* Wazuh-Agents-Management.png – Wazuh Dashboard showing the successfully onboarded Windows endpoint.

## Outcome

The Windows 11 endpoint is successfully onboarded to the Wazuh Manager and actively sending telemetry. The SOC environment is now ready for endpoint monitoring, detection engineering, threat hunting, and incident response.
