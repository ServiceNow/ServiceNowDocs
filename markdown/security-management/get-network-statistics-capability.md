---
title: Security Operations Integration- Get Network Statistics capability
description: The Get Network Statistics capability retrieves a list of active network connections from a host or endpoint. It can be used for incident enrichment during investigations. This capability is triggered automatically when a configuration item is added to a security incident.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration- Get Network Statistics capability

The Get Network Statistics capability retrieves a list of active network connections from a host or endpoint. It can be used for incident enrichment during investigations. This capability is triggered automatically when a configuration item is added to a security incident.

The **Get Network Statistics** capability has a flow, [Security Operations Integrations - Get Network Statistics flow](../../security-operations-integrations/task/secops-integration-get-network-stats-workflow.md) that accepts one or more CIs and tasks. The flow iterates over each implementation and each CI and re-invokes the implementation flow.

**Note:** If no implementations are available, capability actions are not displayed in product menus.

-   **[Security Operations Integrations - Get Network Statistics flow](../../security-operations-integrations/task/secops-integration-get-network-stats-workflow.md)**  
The Security Operations Integrations - Get Network Statistics flow retrieves a list of active network connections from a host or endpoint.
-   **[Security Incident Response- Get Network Statistics Flow](../../security-incident-response-orchestration/task/obtain-network-statistics-workflow.md)**  
The **Security Incident Response** &gt; **Get Network Statistics** flow retrieves the network statistics for an affected Windows-based resource when added to a security incident in the **Analysis** state.

**Parent Topic:**[Integration capabilities](integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability](block-request-capability.md)

[Security Operations Integration- Email Search and Delete capability](email-search-capability.md)

[Security Operations Integration- Enrich CI capability](enrich-ci-capability.md)

[Security Operations Integration- Enrich Observable capability](enrich-observable-capability.md)

[Security Operations Integration- Get Running Processes capability](get-running-processes-capability.md)

[Security Operations Integration- Isolate Host capability](isolate-host-capability.md)

[Security Operations Integration- Publish to Watchlist capability](pubish-to-watchlist-capability.md)

[Security Operations Integration- Sightings Search capability](sightings-search-capability.md)

[Security Operations Integration - Threat Lookup capability](sec-ops-threat-lookups-capability.md)

[Change the order of flow execution](../task/change-wf-execution-order.md)

