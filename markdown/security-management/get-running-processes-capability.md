---
title: Security Operations Integration- Get Running Processes capability
description: The Get Running Processes capability retrieves a list of running processes on a configuration item \(CI\) from a host or endpoint. This capability is used for incident enrichment during investigations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/get-running-processes-capability.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration- Get Running Processes capability

The Get Running Processes capability retrieves a list of running processes on a configuration item \(CI\) from a host or endpoint. This capability is used for incident enrichment during investigations.

The Get Running Processes capability has two implementation flows:

-   [Security Operations Carbon Black Integration - Get Running Processes Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-cb-get-running-processes-workflow.md)
-   [Security Operations System Command Integration- Get Running Processes flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/obtain-WMI-retrieval-workflow.md)

**Note:** If no implementations are available, capability actions are not displayed in product menus.

Actions specific to this flow are described here. For more information on other actions, see [Common Security Operations integration flows and orchestration activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/common-wf-activities.md).

-   **[Security Operations Carbon Black Integration - Get Running Processes Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-cb-get-running-processes-workflow.md)**  
The Security Operations Carbon Black Integration - Get Running Processes is the implementation for the Carbon Black integration launched by the Security Operations Integration - Get Running Process flow.
-   **[Security Operations System Command Integration- Get Running Processes flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/obtain-WMI-retrieval-workflow.md)**  
The Security Operations System Command Integration - Get Running Processes flow retrieves the running processes of a configuration item when added or updated to a Windows or Unix-based security incident in the **Analysis** state.
-   **[Security Operations - Get Running Processes Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-get-running-processes-workflow.md)**  
The Security Operations - Get Running Processes flow is a high-level flow independent of integrations. It retrieves a list of running processes on a configuration item \(CI\) from a host. Use it to fulfill an integration, such as Carbon Black, or for a Windows-based security incident.

**Parent Topic:**[Integration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability]()

[Security Operations Integration- Email Search and Delete capability]()

[Security Operations Integration- Enrich CI capability]()

[Security Operations Integration- Enrich Observable capability]()

[Security Operations Integration- Get Network Statistics capability]()

[Security Operations Integration- Isolate Host capability]()

[Security Operations Integration- Publish to Watchlist capability]()

[Security Operations Integration- Sightings Search capability]()

[Security Operations Integration - Threat Lookup capability]()

[Change the order of flow execution]()

