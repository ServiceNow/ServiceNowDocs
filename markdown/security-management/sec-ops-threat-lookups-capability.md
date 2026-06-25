---
title: Security Operations Integration - Threat Lookup capability
description: The Threat Lookups capability performs threat intelligence lookups to determine whether one or more observables are associated with known security threats.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sec-ops-threat-lookups-capability.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration - Threat Lookup capability

The **Threat Lookups** capability performs threat intelligence lookups to determine whether one or more observables are associated with known security threats.

The **Threat Lookups** capability has a workflow, [Security Operations Integration - Threat Lookup Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sec-ops-integ-threat-lookup.md). When the capability workflow runs, it executes additional workflows for the activated implementations. You can specify an implementation to use to perform a lookup on the selected observables, or you can perform the lookup using all implementations.

**Note:** If no implementations are available, capability actions are not displayed in product menus.

-   **[Security Operations Integration - Threat Lookup Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sec-ops-integ-threat-lookup.md)**  
The **Security Operations Integration - Threat Lookup** capability flow accesses available threat lookup implementations and executes the implementation flows associated with each to perform threat lookups of selected observables.

**Parent Topic:**[Integration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability]()

[Security Operations Integration- Email Search and Delete capability]()

[Security Operations Integration- Enrich CI capability]()

[Security Operations Integration- Enrich Observable capability]()

[Security Operations Integration- Get Network Statistics capability]()

[Security Operations Integration- Get Running Processes capability]()

[Security Operations Integration- Isolate Host capability]()

[Security Operations Integration- Publish to Watchlist capability]()

[Security Operations Integration- Sightings Search capability]()

[Change the order of flow execution]()

