---
title: Configure Sighting Search
description: Configure sighting search integration to search your organization logs for one or more observables to determine how many times each observable appears, within a specified date range or number of days.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-04-22"
reading_time_minutes: 3
breadcrumb: [TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure Sighting Search

Configure sighting search integration to search your organization logs for one or more observables to determine how many times each observable appears, within a specified date range or number of days.

## Before you begin

**Important:** The enrichment integrations appears only if at least one enrichment integration is installed and active.

The Threat Intelligence Security Center supports Sightings Search for the following integrations only:

-   Splunk Search
-   Elasticsearch

Role required: sn\_sec\_tisc.admin

**Note:** The Sightings Search section lists integrations of the Sightings Search type. Each configured integration appears as a card, which you can enable or disable.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Integrations** icon.

    ![Sighting Search page showing three enabled enrichment integration cards: two Splunk integrations and one Elasticsearch integration, each with a last-modified timestamp and View button.](../image/enrich-sighting-section.png)

3.  Select the **Configure new enrichment** action.

    A dialog displays the available integrations. You must select the integration that you want to configure.

4.  **Select** an integration from the list of available integrations.

    The Configure new enrichment page for the selected integration opens. This page is pre filled with details of the selected integration by default. For example, Splunk integration.

    ![Create Enrichment Integration form with Vendor Name set to Splunk, Integration Type set to Sighting Search, and the Integration Configuration section visible.](../image/enrich-sighting-config.png)

5.  On the Create Integration form, fill the fields.

<table id="table_rrp_bwk_kdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Enrichment Integration

</td></tr><tr><td>

Name

</td><td>

Name of the new enrichment integration. For example, `Splunk-1`.

</td></tr><tr><td>

Vendor Name

</td><td>

Name of the vendor.**Note:** The details of the selected vendor are pre-filled by default. For example, `Splunk`.

</td></tr><tr><td>

Integration Type

</td><td>

Type of the selected integration.**Note:** This field is automatically set to **Sighting Search** and prefilled by default.

</td></tr><tr><td>

Description

</td><td>

Unique description of the new enrichment integration.

</td></tr></tbody>
</table>    ![Create Enrichment Integration form with Vendor Name set to Splunk and Integration Type set to Sighting Search.](../image/enrich-sighting-splunk.png)

6.  In the **Integration Configuration** section, configure the integration details based on your requirements.

    The **Integration Configuration** section includes configuration details such as the API key, API Client ID or Secret, username, and password. The required details vary depending on the integration.

7.  Select **Save** to create the enrichment integration configuration.

    The provided details are validated and the enrichment integration is inactive by default.

8.  Select **Save as Draft** to save the enrichment configuration as inactive.

    You can activate it later.

    **Note:** If you're unsure about the configuration details, select **Save as Draft**. After you obtain the required details, open the draft and enter the remaining information, and select **Save** to activate the integration.

9.  Select **Enable** to enable the enrichment integration.

    The enrichment integration is enabled. You can also enable a particular enrichment integration from the **Actions** on the integration tile on the **Catalog**.


-   **[Create Sighting Search queries](../concept/manage-sighting-search-configurations.md)**  
Sighting search configurations define queries that search for observables across your security environment during investigations. Configure these queries to determine how often specific indicators appear in your data sources.
-   **[Using Sighting Search parameters](../concept/manage-sighting-search-parameters.md)**  
Configure advanced search parameters to create complex queries with logic operators and other features supported by your log store. Use these parameters when basic search criteria are insufficient for your investigation needs.
-   **[Get started with Sighting Search Configurations](../concept/tisc-get-sighting-configs.md)**  
Sighting Search Configurations define how threat intelligence data is searched and matched against your environment. Configure these settings to customize threat detection and improve security monitoring accuracy.
-   **[TISC add-on for Splunk overview](../concept/tisc-addon-splunk.md)**  
Configure the Threat Intelligence Security Center \(TISC\) integration with Splunk to import threat intelligence data, set up indicator collections, and analyze search matches using dashboards.

**Parent Topic:**[TISC Enrichment integrations](../concept/tisc-enrichment-integrations.md)

