---
title: Security Operations Integration- Enrich CI capability
description: The Enrich CI capability allows you to enrich data for configuration items associated with a security incident.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration- Enrich CI capability

The Enrich CI capability allows you to enrich data for configuration items associated with a security incident.

The **Enrich CI** capability has a flow, [Security Operations Integration - CI Enrichment flow](../../security-operations-integrations/task/secops-integ-enrich-ci-wf.md). When the capability flow runs, it executes additional flows for the activated implementations. You can specify an implementation to use to perform enrichment on the selected CIs, or you can perform the enrichment using all implementations.

**Note:** This enriched data is not the type of data you would want to store in your CMDB as it is forensic data that is specific to a given investigation--for example, performing a memdump from a CI. Instead, the data is stored in the Configuration Item Enrichment \[sn\_sec\_cmn\_ci\_enrichment\_result\] table.

**Note:** If no implementations are available, capability actions are not displayed in product menus.

-   **[Security Operations Integration - CI Enrichment flow](../../security-operations-integrations/task/secops-integ-enrich-ci-wf.md)**  
The Security Operations Integration - CI Enrichment flow allows you to enrich data in configuration items \(CI\) associated with a security incident.

**Parent Topic:**[Integration capabilities](integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability](block-request-capability.md)

[Security Operations Integration- Email Search and Delete capability](email-search-capability.md)

[Security Operations Integration- Enrich Observable capability](enrich-observable-capability.md)

[Security Operations Integration- Get Network Statistics capability](get-network-statistics-capability.md)

[Security Operations Integration- Get Running Processes capability](get-running-processes-capability.md)

[Security Operations Integration- Isolate Host capability](isolate-host-capability.md)

[Security Operations Integration- Publish to Watchlist capability](pubish-to-watchlist-capability.md)

[Security Operations Integration- Sightings Search capability](sightings-search-capability.md)

[Security Operations Integration - Threat Lookup capability](sec-ops-threat-lookups-capability.md)

[Change the order of flow execution](../task/change-wf-execution-order.md)

