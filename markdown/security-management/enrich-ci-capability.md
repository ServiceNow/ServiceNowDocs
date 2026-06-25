---
title: Security Operations Integration- Enrich CI capability
description: The Enrich CI capability allows you to enrich data for configuration items associated with a security incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/enrich-ci-capability.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration- Enrich CI capability

The Enrich CI capability allows you to enrich data for configuration items associated with a security incident.

The **Enrich CI** capability has a flow, [Security Operations Integration - CI Enrichment flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integ-enrich-ci-wf.md). When the capability flow runs, it executes additional flows for the activated implementations. You can specify an implementation to use to perform enrichment on the selected CIs, or you can perform the enrichment using all implementations.

**Note:** This enriched data is not the type of data you would want to store in your CMDB as it is forensic data that is specific to a given investigation--for example, performing a memdump from a CI. Instead, the data is stored in the Configuration Item Enrichment \[sn\_sec\_cmn\_ci\_enrichment\_result\] table.

**Note:** If no implementations are available, capability actions are not displayed in product menus.

-   **[Security Operations Integration - CI Enrichment flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integ-enrich-ci-wf.md)**  
The Security Operations Integration - CI Enrichment flow allows you to enrich data in configuration items \(CI\) associated with a security incident.

**Parent Topic:**[Integration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability]()

[Security Operations Integration- Email Search and Delete capability]()

[Security Operations Integration- Enrich Observable capability]()

[Security Operations Integration- Get Network Statistics capability]()

[Security Operations Integration- Get Running Processes capability]()

[Security Operations Integration- Isolate Host capability]()

[Security Operations Integration- Publish to Watchlist capability]()

[Security Operations Integration- Sightings Search capability]()

[Security Operations Integration - Threat Lookup capability]()

[Change the order of flow execution]()

