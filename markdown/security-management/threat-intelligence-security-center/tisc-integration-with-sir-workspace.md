---
title: TISC integration with SIR Workspace
description: TISC integration with SIR Workspace provides threat intelligence context for observables and threat entities in the security incident workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/threat-intelligence-security-center/tisc-integration-with-sir-workspace.html
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-08-18"
reading_time_minutes: 1
breadcrumb: [Use, Threat Intelligence Security Center, Security Operations]
---

# TISC integration with SIR Workspace

TISC integration with SIR Workspace provides threat intelligence context for observables and threat entities in the security incident workspace.

Any new observables from Security Incident Response Workspace can be sent to TISC for further analysis by the CTI team using the UI actions provided on the screens.

Any enrichment results from integrations only available in Security Incident Response Workspace can also be pushed to TISC using the UI actions provided in the workspace.

You can associate TISC entities directly with a security incident, without first creating a TISC case. The supported entities are threat actor, malware, campaign, intrusion set, vulnerability, and threat report. A direct association keeps the entity context on the incident and supports reporting on the threat actors and malware families observed in your environment.

You can create these associations from either application:

-   From the **TISC Context** tab in Security Incident Response Workspace, link and unlink TISC records for each list.
-   From the **Internal Intelligence** tab on a TISC record in the TISC Workspace, link and unlink security incidents.

The **TISC Context** tab lists every TISC observable linked to the security incident, whether or not a matching threat intelligence observable exists in Security Incident Response Workspace.

Each link action posts one consolidated work note in the security incident activity stream for traceability.

