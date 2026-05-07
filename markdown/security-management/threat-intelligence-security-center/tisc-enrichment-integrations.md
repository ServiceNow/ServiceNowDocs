---
title: TISC Enrichment integrations
description: The Threat Intelligence Security Center base system does not include any pre-configured integrations. This section provides instructions for configuring both ServiceNow and third-party integrations.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# TISC Enrichment integrations

The Threat Intelligence Security Center base system does not include any pre-configured integrations. This section provides instructions for configuring both ServiceNow and third-party integrations.

**Important:**

Verify that you have installed the required third-party app integrations. You can see the observables, sighting search, and threat lookup details only for the third-party apps that are installed.

## All Integration Configurations

All integrations are separate applications that need to be installed. TISC supports integrations with third-party vendors. Any installed integrations can be configured here.

This section displays cards for each of the configured integration implementations that you can activate and use.

Each enrichment type section appears only if at least one corresponding integration for that enrichment type is installed. For example, the **Threat Lookup** section appears under **Enrichment Integrations** only if at least one Threat Lookup integration is installed.

The configured integration cards can be viewed by navigating to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations**.

![Threat Intelligence integrations](../image/enrich-all-integrations.png)

## Actions on the All Integrations view

You can perform the following actions in the All Integration view.

<table id="table_ols_yx1_nzb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All

</td><td>

Use this list to filter integrations based on their current state. You can filter based on the following states:-   **All**: Displays all the integrations on the page. This is the default option.
-   **Enabled**: Displays all the integrations that are in an enabled state.
-   **Disabled**: Displays all the integrations that are in an inactive state.
-   **Draft**: Displays all the integrations that are in a draft state.

</td></tr><tr><td>

![Card view](../image/enrich-card-view.png)

</td><td>

Use this action to view all the integrations in the form of cards.

</td></tr><tr><td>

![List view](../image/enrich-list-view.png)

</td><td>

Use this action to view all the integrations in the form of lists.

</td></tr><tr><td>

![Refresh](../image/enrich-refresh-icon.png)

</td><td>

Use this action to refresh the All Integrations page.

</td></tr><tr><td>

![Sort](../image/enrich-sort-icon.png)

</td><td>

Use this action to sort all the integrations based on the following:-   **Last Modified \(recent\)**
-   **Last Modified \(oldest\)**
-   **Name \(A-Z\)**
-   **Name \(Z-A\)**

</td></tr><tr><td>

Search in catalog

</td><td>

Use this action to search for configured integrations based on name and description within the catalog.

</td></tr></tbody>
</table>-   **[Configure new enrichment](../task/tisc-config-new-enrich.md)**  
Set up threat intelligence enrichment integrations to automatically gather additional context about observables, search for sightings, or perform threat lookups from external security vendors.
-   **[Configure Observable Enrichment](../task/configure-observable-enrichment.md)**  
Enrich one or more observables to identify whether they're associated with known threats. The results are based on the enrichment integrations active in your environment.
-   **[Configure Sighting Search](../task/configure-sighting-search.md)**  
Configure sighting search integration to search your organization logs for one or more observables to determine how many times each observable appears, within a specified date range or number of days.
-   **[Configure Threat Lookup](../task/configure-threat-lookup.md)**  
Scan selected observables for malware using Threat Intelligence to determine if they are malicious. Use this lookup to assess security threats from IP addresses, URLs, file hashes, and other observable types.
-   **[Threat Lookup](tisc-threat-lookup.md)**  
Scan selected observables for malware using VirusTotal and CrowdStrike Falcon Intelligence. This workflow checks observables against both threat intelligence sources and returns detailed security analysis results.

**Parent Topic:**[TISC Integrations](tisc-integrations.md)

**Related topics**  


[TISC Security Tools integrations](tisc-edr-integrations.md)

