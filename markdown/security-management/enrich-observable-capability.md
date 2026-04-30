---
title: Security Operations Integration- Enrich Observable capability
description: The Enrich Observable capability allows you to enrich observables with additional information from a variety of sources using implementation workflows. This capability is used during incident response investigations to contain an identified threat.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration- Enrich Observable capability

The Enrich Observable capability allows you to enrich observables with additional information from a variety of sources using implementation workflows. This capability is used during incident response investigations to contain an identified threat.

The Enrich Observable capability has a workflow, [Security Operations Integration - Enrich Observable workflow](../../security-operations-integrations/task/secops-integration-enrich-observ-wf.md). When the capability workflow runs, it executes additional workflows for the activated implementations. You can specify an implementation to use to perform enrichment on the selected observables, or you can perform the enrichment using all implementations that match the supported observable types.

**Note:** If no implementations are available, capability actions are not displayed in product menus.

-   **[Security Operations Integration - Enrich Observable workflow](../../security-operations-integrations/task/secops-integration-enrich-observ-wf.md)**  
The Security Operations Integration - Enrich Observable sub flow allows you to enrich observables with additional information from a variety of sources using implementation flow designer.

**Parent Topic:**[Integration capabilities](integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Block Request capability](block-request-capability.md)

[Security Operations Integration- Email Search and Delete capability](email-search-capability.md)

[Security Operations Integration- Enrich CI capability](enrich-ci-capability.md)

[Security Operations Integration- Get Network Statistics capability](get-network-statistics-capability.md)

[Security Operations Integration- Get Running Processes capability](get-running-processes-capability.md)

[Security Operations Integration- Isolate Host capability](isolate-host-capability.md)

[Security Operations Integration- Publish to Watchlist capability](pubish-to-watchlist-capability.md)

[Security Operations Integration- Sightings Search capability](sightings-search-capability.md)

[Security Operations Integration - Threat Lookup capability](sec-ops-threat-lookups-capability.md)

[Change the order of workflow execution](../task/change-wf-execution-order.md)

