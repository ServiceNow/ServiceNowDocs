---
title: Security Operations Integration- Block Request capability
description: The Block Action capability blocks observables associated with a security incident on a firewall, web proxy, or other control point using implementation flows. This capability is used during incident response investigations to contain an identified threat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/block-request-capability.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration- Block Request capability

The Block Action capability blocks observables associated with a security incident on a firewall, web proxy, or other control point using implementation flows. This capability is used during incident response investigations to contain an identified threat.

The Block Request capability has a flow, [Security Operations Integration - Block Request Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-block-request-workflow.md), that executes the request to block. This flow accepts a list of observables, finds any implementing capabilities, and executes the request based on the configured flow.

**Note:** If no implementations are available, capability actions are not displayed in product menus.

-   **[Run Block Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/run-block-request.md)**  
Blocks communication with observables associated with a security incident.
-   **[Security Operations Integration - Block Request Flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/secops-integration-block-request-workflow.md)**  
The Security Operations Integration - Block Request flow is a high-level flow independent of integrations. It blocks observables associated with a security incident. Use it to fulfill an integration such as Palo Alto Networks - Firewall.

**Parent Topic:**[Integration capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/integration-capabilities.md)

**Related topics**  


[Security Operations Integration- Email Search and Delete capability]()

[Security Operations Integration- Enrich CI capability]()

[Security Operations Integration- Enrich Observable capability]()

[Security Operations Integration- Get Network Statistics capability]()

[Security Operations Integration- Get Running Processes capability]()

[Security Operations Integration- Isolate Host capability]()

[Security Operations Integration- Publish to Watchlist capability]()

[Security Operations Integration- Sightings Search capability]()

[Security Operations Integration - Threat Lookup capability]()

[Change the order of flow execution]()

