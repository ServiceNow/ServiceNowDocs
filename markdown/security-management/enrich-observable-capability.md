---
title: Security Operations Integration- Enrich Observable capability
description: The Enrich Observable capability allows you to enrich observables with additional information from a variety of sources using implementation flows. This capability is used during incident response investigations to contain an identified threat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/enrich-observable-capability.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration- Enrich Observable capability

The Enrich Observable capability allows you to enrich observables with additional information from a variety of sources using implementation flows. This capability is used during incident response investigations to contain an identified threat.

The Enrich Observable capability has a flow, [Security Operations Integration - Enrich Observable flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-enrich-observ-wf.md). When the capability flow runs, it executes additional flows for the activated implementations. You can specify an implementation to use to perform enrichment on the selected observables, or you can perform the enrichment using all implementations that match the supported observable types.

**Note:** If no implementations are available, capability actions are not displayed in product menus.

-   **[Security Operations Integration - Enrich Observable flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-enrich-observ-wf.md)**  
The Security Operations Integration - Enrich Observable sub flow allows you to enrich observables with additional information from a variety of sources using implementation flow designer.

**Parent Topic:**[Integration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability]()

[Security Operations Integration- Email Search and Delete capability]()

[Security Operations Integration- Enrich CI capability]()

[Security Operations Integration- Get Network Statistics capability]()

[Security Operations Integration- Get Running Processes capability]()

[Security Operations Integration- Isolate Host capability]()

[Security Operations Integration- Publish to Watchlist capability]()

[Security Operations Integration- Sightings Search capability]()

[Security Operations Integration - Threat Lookup capability]()

[Change the order of flow execution]()

