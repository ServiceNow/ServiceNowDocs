---
title: TISC Enrichment integrations
description: The Threat Intelligence Security Center base system does not include any pre-configured integrations. This section provides instructions for configuring both ServiceNow and third-party integrations.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# TISC Enrichment integrations

The Threat Intelligence Security Center base system does not include any pre-configured integrations. This section provides instructions for configuring both ServiceNow and third-party integrations.

**Important:**

Make sure that you’ve installed the required third-party app integrations. You can see the observables, sighting search, and threat lookup details only for the third-party apps that are installed.

## All Integration Configurations

All the integrations are separate applications that needs to be installed. TISC supports integrations with third party vendors. Any installed integrations can be configured here.

This section displays cards for each of the configured integration implementations that you can activate and use.

Each enrichment type’s section would be visible only if at least one of the corresponding integration for that enrichment type is installed. For example, the **Threat Lookup** section would be visible under **Enrichment Integrations** only if at least one Threat Lookup integration is installed.

The configured integration cards can be viewed by navigating to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations**.

![Threat Intelligence integrations](../image/enrich-all-integrations.png)

## Actions on the All Integrations view

The All Integration view enables you to perform the following actions.

<table id="table_ols_yx1_nzb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All

</td><td>

Use this dropdown menu to filter integrations based on their current state. You can filter based on the following states:-   **All**: Displays all the integrations on the page. This is the default option.
-   **Enabled**: Displays all the integrations that are in an enabled state.
-   **Disabled**: Displays all the integrations that are in a disabled state.
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
</table>## Configure new enrichment from All Integrations view

You can configure new enrichments from the All Integrations view or directly from the Observable Enrichment, Sighting Search, or Threat Lookup sections respectively. To configure the new enrichment from all the All Integrations view, perform the following steps.

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.
2.  Click the **Integrations** icon, and select the **All Integrations** section.

    ![Configure new enrichment from All Integrations view](../image/enrich-all-integrations.png)

3.  Click the **Configure new enrichment** action.

    The Configure new enrichment pop-up appears with three enrichment types, which are Observable Enrichment, Sighting Search, or Threat Lookup. You need to choose which type of enrichment you want to configure.

    ![Configure the enrichment type](../image/enrich-popup-observables.png)

4.  Select an enrichment type, and click **Next**.

    This takes you to the pop-up that displays the available integrations. You need to choose the integration you want to configure.

5.  Select an integration from the list of available integrations, and click **Select**.

    This takes you to the Create New Enrichment Integration page of the selected integration. This page is pre-filled with details of the selected integration by default. For example, WHOIS integration.

6.  On the Create New Integration form, fill the fields.

<table id="table_ygj_ykc_nzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the new enrichment integration. For example, `WHOIS1`.

</td></tr><tr><td>

Vendor Name

</td><td>

Name of the vendor. The details of the selected vendor are pre-filled by default. For example, `WHOIS`.

</td></tr><tr><td>

Integration Type

</td><td>

Type of integration that you selected. For example, Observable Enrichment. The details of the selected integration type are pre-filled by default.The following Integration Types are supported:

-   Observable Enrichment
-   Sighting Search
-   Threat Lookup


</td></tr><tr><td>

Description

</td><td>

Enter a unique description for the new enrichment integration.

</td></tr></tbody>
</table>7.  In the Integration Configuration section, configure the integration details based on your requirements.

    The Integration Configuration section includes configuration details like API key, API Client ID or secret, username, password, and so on, which you need to fill in. These configuration details vary for different integrations.

8.  Click the **Save** action to store and create the enrichment integration configuration.

    The provided details are validated, and by default the enrichment integration's status is disabled.

9.  \(Optional\) Click the **Save as Draft** action to only store the integration configurations as draft. Users cannot enable an integration when it is saved in draft

    If you're not sure about the configuration details, you can use the **Save as Draft** option. After you get the configuration details, you can fill the remaining information in the draft version and create it.

10. To enable the enrichment integration, click **Enable**.

    The enrichment integration is enabled successfully.

11. You can also enable, disable, or delete a particular enrichment integration by using the Actions menu of the required integration tile on the Catalog page or the Enrichment Integrations page.

-   **[Configure Observable Enrichment](../task/configure-observable-enrichment.md)**  
You can perform threat intelligence enrichment on one or more observables to determine whether they’re associated with known security threats. The implementations that run depend on the ones you’ve activated.
-   **[Sighting Search](tisc-sighting-search.md)**  
This section describes the TISC Sighting Search and Elastic Search integrations.
-   **[Threat Lookup](tisc-threat-lookup.md)**  
The Threat Lookup - VirusTotal and CrowdStrike Falcon intelligence workflow performs a lookup on selected observables. If the observables are of a type recognized by VirusTotal and as well as CrowdStrike, the observables are scanned for malware, and the results are returned.

**Parent Topic:**[TISC Integrations](tisc-integrations.md)

**Related topics**  


[TISC Security Tools integrations](tisc-edr-integrations.md)

