---
title: Automatic security incident observable log data enrichment
description: When certain applications and integrations are set up, including Threat Intelligence and the Palo Alto Networks - Firewall integration, observables information in a security incident can be automatically enriched with threat log data whenever the Source IP for its observables is modified.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/si-observ-data-enrich.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage observables, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automatic security incident observable log data enrichment

When certain applications and integrations are set up, including Threat Intelligence and the Palo Alto Networks - Firewall integration, observables information in a security incident can be automatically enriched with threat log data whenever the Source IP for its observables is modified.

When a modification occurs, a business rule initiates a workflow that retrieves data from threat logs on your firewall and enriches the observables information in the security incident.

Before observables can be enriched, the following steps must be performed.

-   [Threat Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/c_GetStartedWithThreatIntel.md) must be activated.
-   The [Palo Alto Networks Firewall](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/activate-config-firewall.md) integration must be activated and configured. This can also include [Set up SSH credentials to the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/set-up-and-config-MID-server.md).

After that setup has been completed, the act of changing the Source IP of observables associated with a security incident causes a business rule to execute the **Security Operations Palo Alto Networks - Get Log Data** workflow. Workflow activities queue up a search query on the firewall and return a Job ID that is used to retrieve threat logs data from the firewall and attach them as an XML file to the security incident.

**Related topics**  


[Get AutoFocus Session Info Enrichment Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/search-for-malicious-content.md)

[Palo Alto Networks Firewall Launcher Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/secops-integration-paloalto-firewall-launcher-workflow.md)

[Get Log Data Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/get-threat-log-data.md)

[Get WildFire Data Enrichment Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/enrich-wildfire-data.md)

