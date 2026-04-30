---
title: Automatic security incident observable log data enrichment
description: When certain applications and integrations are set up, including Threat Intelligence and the Palo Alto Networks - Firewall integration, observables information in a security incident can be automatically enriched with threat log data whenever the Source IP for its observables is modified.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage observables, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automatic security incident observable log data enrichment

When certain applications and integrations are set up, including Threat Intelligence and the Palo Alto Networks - Firewall integration, observables information in a security incident can be automatically enriched with threat log data whenever the Source IP for its observables is modified.

When a modification occurs, a business rule initiates a workflow that retrieves data from threat logs on your firewall and enriches the observables information in the security incident.

Before observables can be enriched, the following steps must be performed.

-   [Threat Intelligence](../../threat-intelligence/concept/c_GetStartedWithThreatIntel.md#) must be activated.
-   The [Palo Alto Networks Firewall](../../secops-integration-sir/secops-integration-palo-alto-firewall/task/activate-config-firewall.md) integration must be activated and configured. This can also include [Set up SSH credentials to the MID Server](../../secops-integration-sir/secops-integration-palo-alto-firewall/task/set-up-and-config-MID-server.md).

After that setup has been completed, the act of changing the Source IP of observables associated with a security incident causes a business rule to execute the **Security Operations Palo Alto Networks - Get Log Data** workflow. Workflow activities queue up a search query on the firewall and return a Job ID that is used to retrieve threat logs data from the firewall and attach them as an XML file to the security incident.

**Related topics**  


[Get AutoFocus Session Info Enrichment Flow](../../secops-integration-sir/secops-integration-palo-alto-autofocus/task/search-for-malicious-content.md#)

[Palo Alto Networks Firewall Launcher Workflow](../../security-operations-integrations/task/secops-integration-paloalto-firewall-launcher-workflow.md)

[Security Operations Palo Alto Networks - Check and Block Value Workflow](../../secops-integration-sir/secops-integration-palo-alto-autofocus/task/check-and-block-values.md#)

[Get Log Data Flow](../../secops-integration-sir/secops-integration-palo-alto-firewall/task/get-threat-log-data.md#)

[Get WildFire Data Enrichment Flow](../../secops-integration-sir/secops-integration-palo-alto-wildfire/task/enrich-wildfire-data.md#)

