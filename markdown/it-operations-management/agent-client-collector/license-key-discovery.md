---
title: License key discovery
description: License key discovery in Agent Client Collector for Visibility - Content automatically collects software license keys from the Windows registry on managed endpoints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/license-key-discovery.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-05-27"
reading_time_minutes: 1
keywords: [license key discovery, ACC-VC, Windows registry, software license, agent client collector]
breadcrumb: [ACC Discovery, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# License key discovery

License key discovery in Agent Client Collector for Visibility - Content automatically collects software license keys from the Windows registry on managed endpoints.

License key discovery enables the Agent Client Collector for Visibility - Content \(ACC-VC\) Windows agent to read software license keys stored in the Windows registry on managed endpoints. When a device is discovered, the agent reads registry values defined by an admin-configured list of registry paths and value names, and reports the results in your instance.

The feature is off by default and must be explicitly enabled using a system property.

## Why use license key discovery

License key discovery helps administrators track software license keys across managed Windows devices. By linking discovered keys to device CIs and SAM products, it supports software asset management and license tracking efforts. Administrators can detect duplicate licenses, track compliance, and manage license costs.

## Who can use license key discovery

Specific roles are required to configure and view license key discovery data. For details, see the Access control table on the [License key discovery and access control tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/license-key-discovery-reference.md) page.

No role can delete license key records. If a key that was previously detected is no longer found on a device, it is marked as **Absent** rather than deleted, preserving the audit trail.

-   **[Configure license key discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/configure-license-key-discovery.md)**  
Enable license key discovery and define the registry paths and values you want the Agent Client Collector for Visibility - Content Windows agent to collect from managed endpoints.

**Parent Topic:**[Agent Client Collector Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-discovery.md)

