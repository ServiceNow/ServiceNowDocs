---
title: Security Operations Integration- Get Running Processes capability
description: The Get Running Processes capability retrieves a list of running processes on a configuration item \(CI\) from a host or endpoint. This capability is used for incident enrichment during investigations.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration- Get Running Processes capability

The Get Running Processes capability retrieves a list of running processes on a configuration item \(CI\) from a host or endpoint. This capability is used for incident enrichment during investigations.

The Get Running Processes capability has two implementation flows:

-   [Security Operations Carbon Black Integration - Get Running Processes Flow](../../security-operations-integrations/concept/secops-integration-cb-get-running-processes-workflow.md)
-   [Security Operations System Command Integration- Get Running Processes flow](../../security-incident-response-orchestration/task/obtain-WMI-retrieval-workflow.md)

**Note:** If no implementations are available, capability actions are not displayed in product menus.

Actions specific to this flow are described here. For more information on other actions, see [Common Security Operations integration flows and orchestration activities](common-wf-activities.md).

-   **[Security Operations Carbon Black Integration - Get Running Processes Flow](../../security-operations-integrations/concept/secops-integration-cb-get-running-processes-workflow.md)**  
The Security Operations Carbon Black Integration - Get Running Processes is the implementation for the Carbon Black integration launched by the Security Operations Integration - Get Running Process flow.
-   **[Security Operations System Command Integration- Get Running Processes flow](../../security-incident-response-orchestration/task/obtain-WMI-retrieval-workflow.md)**  
The Security Operations System Command Integration - Get Running Processes flow retrieves the running processes of a configuration item when added or updated to a Windows or Unix-based security incident in the **Analysis** state.
-   **[Security Operations - Get Running Processes Flow](../../security-operations-integrations/concept/secops-integration-get-running-processes-workflow.md)**  
The Security Operations - Get Running Processes flow is a high-level flow independent of integrations. It retrieves a list of running processes on a configuration item \(CI\) from a host. Use it to fulfill an integration, such as Carbon Black, or for a Windows-based security incident.

**Parent Topic:**[Integration capabilities](integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability](block-request-capability.md)

[Security Operations Integration- Email Search and Delete capability](email-search-capability.md)

[Security Operations Integration- Enrich CI capability](enrich-ci-capability.md)

[Security Operations Integration- Enrich Observable capability](enrich-observable-capability.md)

[Security Operations Integration- Get Network Statistics capability](get-network-statistics-capability.md)

[Security Operations Integration- Isolate Host capability](isolate-host-capability.md)

[Security Operations Integration- Publish to Watchlist capability](pubish-to-watchlist-capability.md)

[Security Operations Integration- Sightings Search capability](sightings-search-capability.md)

[Security Operations Integration - Threat Lookup capability](sec-ops-threat-lookups-capability.md)

[Change the order of flow execution](../task/change-wf-execution-order.md)

