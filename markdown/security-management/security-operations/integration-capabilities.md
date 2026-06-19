---
title: Integration capabilities
description: The Integration Capabilities framework provides a consistent architecture to support interoperability with third-party integrations. This abstracted interface and data model insulates integrations from changes to the core application and ensures a consistent experience for similar types of integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-operations/integration-capabilities.html
release: zurich
product: Security Operations
classification: security-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Integration capabilities

The Integration Capabilities framework provides a consistent architecture to support interoperability with third-party integrations. This abstracted interface and data model insulates integrations from changes to the core application and ensures a consistent experience for similar types of integrations.

Each integration capability persists in the Integration Capability `[sn_sec_cmn_capability]` table. Integration capability flows cannot be executed alone, and require the launch of an implementation flow. Any plugin that provides an implementation of the capability adds their implementation to the child table: Integration Capability Implementation`[sn_sec_cmn_capability_implementation]`.

**Note:** As of version 13.3.1 and later, integration capability settings are stored in the Capabilities `[sn_sec_cmn_capability]` table instead of the Integration Capability `[sn_sec_cmn_integration_capability]` table.

The implementation specifies the flow to be executed, the related integration \(plugin id\), and the capability it implements. These flows can be executed in parallel using the parallel flow launcher; however, sequential execution is the default in the base system. If needed, you can [change the order of execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/change-wf-execution-order.md).

**Note:** If no implementations are available, capability actions are not displayed in product menus.

-   **[Security Operations Integration- Block Request capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/block-request-capability.md)**  
The Block Action capability blocks observables associated with a security incident on a firewall, web proxy, or other control point using implementation flows. This capability is used during incident response investigations to contain an identified threat.
-   **[Security Operations Integration- Email Search and Delete capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/email-search-capability.md)**  
The Email Search and Delete capability returns the number of threat emails from an email server search and, optionally, returns details for each email found. After the email search is completed, you can delete the emails.
-   **[Security Operations Integration- Enrich CI capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/enrich-ci-capability.md)**  
The Enrich CI capability allows you to enrich data for configuration items associated with a security incident.
-   **[Security Operations Integration- Enrich Observable capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/enrich-observable-capability.md)**  
The Enrich Observable capability allows you to enrich observables with additional information from a variety of sources using implementation flows. This capability is used during incident response investigations to contain an identified threat.
-   **[Security Operations Integration- Get Network Statistics capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/get-network-statistics-capability.md)**  
The Get Network Statistics capability retrieves a list of active network connections from a host or endpoint. It can be used for incident enrichment during investigations. This capability is triggered automatically when a configuration item is added to a security incident.
-   **[Security Operations Integration- Get Running Processes capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/get-running-processes-capability.md)**  
The Get Running Processes capability retrieves a list of running processes on a configuration item \(CI\) from a host or endpoint. This capability is used for incident enrichment during investigations.
-   **[Security Operations Integration- Isolate Host capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/isolate-host-capability.md)**  
The **Isolate Host** capability restricts system connections to other devices. Isolate host is executed against a configuration item \(CI\).
-   **[Security Operations Integration- Publish to Watchlist capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/pubish-to-watchlist-capability.md)**  
The Publish to Watchlist capability adds observables and indicators associated with a security incident to a third-party watchlist that monitors for security events and generates alerts. This capability is used as part of incident response during investigations.
-   **[Security Operations Integration- Sightings Search capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/sightings-search-capability.md)**  
The **Sightings Search** capability accepts a set of observables, finds any integrations that support a Sightings Search, then executes these searches.
-   **[Security Operations Integration - Threat Lookup capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/sec-ops-threat-lookups-capability.md)**  
The **Threat Lookups** capability performs threat intelligence lookups to determine whether one or more observables are associated with known security threats.
-   **[Change the order of flow execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/change-wf-execution-order.md)**  
Integration capability implementations specify the flow to be executed. In the base system, flows are executed sequentially, in the order specified in the implementation. You can change the order as needed.

**Parent Topic:**[Security Operations Integration Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/secops-integ-ref.md)

