---
title: Security Operations Integration- Isolate Host capability
description: The Isolate Host capability restricts system connections to other devices. Isolate host is executed against a configuration item \(CI\).
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration- Isolate Host capability

The **Isolate Host** capability restricts system connections to other devices. Isolate host is executed against a configuration item \(CI\).

The **Isolate Host** capability has a flow, [Security Operations - Isolate Host Flow](../../security-operations-integrations/task/secops-integration-isolate-host-workflow.md) that accepts one or more CIs and optionally an implementation. You can specify an implementation to use to isolate the host or for the flow to attempt to isolate the host using all implementations.

**Note:** While not integrated with a capability, a flow, [Security Operations Carbon Black Integration- Remove Host Isolation Flow](../../security-operations-integrations/task/secops-integration-cb-remove-host-isolation-workflow.md) is available for orchestration to restore communication with an isolated host.

**Note:** If no implementations are available, capability actions are not displayed in product menus.

-   **[Run Isolate Host](../task/run-isolate-host.md)**  
**Isolate Host** restricts system connections to other devices.
-   **[Security Operations - Isolate Host Flow](../../security-operations-integrations/task/secops-integration-isolate-host-workflow.md)**  
The **Security Operations - Isolate Host** flow is a high-level flow independent of integrations. It uses the configured queries to search for a set of configuration items. Use it to fulfill an integration, such as Carbon Black.
-   **[Security Operations Carbon Black Integration - Isolate Host Flow](../../security-operations-integrations/task/secops-integration-cb-isolate-host-workflow.md)**  
The Security Operations Carbon Black Integration - Isolate Host is the implementation for the Carbon Black integration launched by the Security Operations Integration - Isolate Host flow.
-   **[Security Operations Carbon Black Integration- Remove Host Isolation Flow](../../security-operations-integrations/task/secops-integration-cb-remove-host-isolation-workflow.md)**  
The **Security Operations Carbon Black Integration - Remove Host Isolation** flow unblocks communication with a specified host or endpoint in a Carbon Black system.

**Parent Topic:**[Integration capabilities](integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability](block-request-capability.md)

[Security Operations Integration- Email Search and Delete capability](email-search-capability.md)

[Security Operations Integration- Enrich CI capability](enrich-ci-capability.md)

[Security Operations Integration- Enrich Observable capability](enrich-observable-capability.md)

[Security Operations Integration- Get Network Statistics capability](get-network-statistics-capability.md)

[Security Operations Integration- Get Running Processes capability](get-running-processes-capability.md)

[Security Operations Integration- Publish to Watchlist capability](pubish-to-watchlist-capability.md)

[Security Operations Integration- Sightings Search capability](sightings-search-capability.md)

[Security Operations Integration - Threat Lookup capability](sec-ops-threat-lookups-capability.md)

[Change the order of flow execution](../task/change-wf-execution-order.md)

