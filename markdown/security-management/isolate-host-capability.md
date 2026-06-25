---
title: Security Operations Integration- Isolate Host capability
description: The Isolate Host capability restricts system connections to other devices. Isolate host is executed against a configuration item \(CI\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/isolate-host-capability.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration- Isolate Host capability

The **Isolate Host** capability restricts system connections to other devices. Isolate host is executed against a configuration item \(CI\).

The **Isolate Host** capability has a flow, [Security Operations - Isolate Host Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-isolate-host-workflow.md) that accepts one or more CIs and optionally an implementation. You can specify an implementation to use to isolate the host or for the flow to attempt to isolate the host using all implementations.

**Note:** While not integrated with a capability, a flow, [Security Operations Carbon Black Integration- Remove Host Isolation Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-cb-remove-host-isolation-workflow.md) is available for orchestration to restore communication with an isolated host.

**Note:** If no implementations are available, capability actions are not displayed in product menus.

-   **[Run Isolate Host](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/run-isolate-host.md)**  
**Isolate Host** restricts system connections to other devices.
-   **[Security Operations - Isolate Host Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-isolate-host-workflow.md)**  
The **Security Operations - Isolate Host** flow is a high-level flow independent of integrations. It uses the configured queries to search for a set of configuration items. Use it to fulfill an integration, such as Carbon Black.
-   **[Security Operations Carbon Black Integration - Isolate Host Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-cb-isolate-host-workflow.md)**  
The Security Operations Carbon Black Integration - Isolate Host is the implementation for the Carbon Black integration launched by the Security Operations Integration - Isolate Host flow.
-   **[Security Operations Carbon Black Integration- Remove Host Isolation Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-cb-remove-host-isolation-workflow.md)**  
The **Security Operations Carbon Black Integration - Remove Host Isolation** flow unblocks communication with a specified host or endpoint in a Carbon Black system.

**Parent Topic:**[Integration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability]()

[Security Operations Integration- Email Search and Delete capability]()

[Security Operations Integration- Enrich CI capability]()

[Security Operations Integration- Enrich Observable capability]()

[Security Operations Integration- Get Network Statistics capability]()

[Security Operations Integration- Get Running Processes capability]()

[Security Operations Integration- Publish to Watchlist capability]()

[Security Operations Integration- Sightings Search capability]()

[Security Operations Integration - Threat Lookup capability]()

[Change the order of flow execution]()

