---
title: Security Operations Integration- Get Network Statistics capability
description: The Get Network Statistics capability retrieves a list of active network connections from a host or endpoint. It can be used for incident enrichment during investigations. This capability is triggered automatically when a configuration item is added to a security incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/get-network-statistics-capability.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration- Get Network Statistics capability

The Get Network Statistics capability retrieves a list of active network connections from a host or endpoint. It can be used for incident enrichment during investigations. This capability is triggered automatically when a configuration item is added to a security incident.

The **Get Network Statistics** capability has a flow, [Security Operations Integrations - Get Network Statistics flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-get-network-stats-workflow.md) that accepts one or more CIs and tasks. The flow iterates over each implementation and each CI and re-invokes the implementation flow.

**Note:** If no implementations are available, capability actions are not displayed in product menus.

-   **[Security Operations Integrations - Get Network Statistics flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-get-network-stats-workflow.md)**  
The Security Operations Integrations - Get Network Statistics flow retrieves a list of active network connections from a host or endpoint.
-   **[Security Incident Response- Get Network Statistics flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/obtain-network-statistics-workflow.md)**  
The **Security Incident Response** &gt; **Get Network Statistics** flow retrieves the network statistics for an affected Windows-based resource when added to a security incident in the **Analysis** state.

**Parent Topic:**[Integration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability]()

[Security Operations Integration- Email Search and Delete capability]()

[Security Operations Integration- Enrich CI capability]()

[Security Operations Integration- Enrich Observable capability]()

[Security Operations Integration- Get Running Processes capability]()

[Security Operations Integration- Isolate Host capability]()

[Security Operations Integration- Publish to Watchlist capability]()

[Security Operations Integration- Sightings Search capability]()

[Security Operations Integration - Threat Lookup capability]()

[Change the order of flow execution]()

