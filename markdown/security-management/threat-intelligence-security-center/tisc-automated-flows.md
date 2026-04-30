---
title: Working with automated flows
description: Use these defined steps to learn how you can use the automated flows in TISC and its capabilities.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer, Threat Intelligence Security Center, Security Operations]
---

# Working with automated flows

Use these defined steps to learn how you can use the automated flows in TISC and its capabilities.

Create flows that run with TISC roles. In TISC the flows are created for the following:

-   Automated IOC Enrichment
-   Analyze, assess and disseminate on the IoC’s related to threat
-   Analyze, assess the IoC’s related to the threat and create incident.
-   Vulnerability Management Support.
-   Zero-day vulnerability tracking.

**Note:** All the flows are templates which are shipped in draft state for the users to customize or copy according to their own needs.

## Reusable Actions

|Flow action|Description|
|-----------|-----------|
|Add Tag To Entity|Adding tags support to entities representing observables, indicators, and objects.|
|Remove tag from entity|Removing tags support to entities representing observables, indicators, and objects.|
|Add Taxonomy To Entity|Adding taxonomy values support to entities representing observables, indicators, and objects.|
|Remove Taxonomy from entity|Removing taxonomy values support to entities representing observables, indicators, and objects.|
|Check if IP address is in CIDR range|Checking if an IP address in inside a CIDR range.|
|Check if IP address is in range|Checking if an IP address is in between from and to range.|

-   **[Automated IOC Enrichment](../task/tisc-ioc-enrichment.md)**  
Learn how to automate enrichment of IOC’s using flows when they match a certain criterion.
-   **[Analyze, assess, and disseminate observables](../task/tisc-disseminate-observables.md)**  
Learn how to analyze and disseminate observables which are related to threat.
-   **[Analyze and assess threat IoC’s](../task/tisc-analyze-ioc.md)**  
Learn how to analyze an IOC’s which are a threat and notifying the security incident team.
-   **[Vulnerability Management Support](../task/tisc-vul-mgmt.md)**  
Learn how a new vulnerability is created in TISC with a related vulnerability in VR.
-   **[Zero-day vulnerability tracking](../task/tisc-zero-vul.md)**  
Learn how to analyze RSS Feeds coming into the system.
-   **[Automated flows tables](tisc-flows-tables.md)**  
The following tables helps you to understand the relationship tables between entities and enrichment tables that are used in automated flows.

