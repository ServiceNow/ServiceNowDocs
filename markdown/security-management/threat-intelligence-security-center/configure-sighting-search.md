---
title: Configure Sighting Search
description: You can perform sightings search on one or multiple observables to determine the number of times the observables are sighted in your organisation logs. You can perform sighting search on observables within a selected number of days or within a date range.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Sighting Search, TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure Sighting Search

You can perform sightings search on one or multiple observables to determine the number of times the observables are sighted in your organisation logs. You can perform sighting search on observables within a selected number of days or within a date range.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Note:** Enrichment Integrations module is only shown if at least one of the integration supporting any of the capability is installed in the application.

The Threat Intelligence Security Center supports Sighting Search only for the following integrations:

-   Splunk Search
-   ElasticSearch

## About this task

The Sightings Search section contains only the integrations with the integration type as sightings search.

This section displays cards for each of the configured integration implementations that you can activate and use.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click the **Integrations** icon, and select the **Sighting Search** section.

    ![Sighting Search integrations](../image/enrich-sighting-section.png)

3.  Click the **Configure new enrichment** action.

    This takes you to the pop-up that displays the available integrations. You need to choose the integration that you need to configure.

4.  Select an integration from the list of available integrations, and click **Select**.

    This takes you to the Create New Enrichment Integration page of the selected integration. This page is pre-filled with details of the selected integration by default. For example, Splunk integration.

    ![Select and integration from the list of available integrations](../image/enrich-sighting-config.png)

5.  On the Create New Integration form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |**Enrichment Integration**| |
    |**Name**|Enter a name for the new enrichment integration. For example, `Splunk-1`.|
    |**Vendor Name**|Name of the vendor. The details of the selected vendor are pre-filled by default. For example, `Splunk`.|
    |**Integration Type**|Type of integration that you selected, which is Sighting Search. The details of the selected integration type are pre-filled by default.|
    |**Description**|Enter a unique description for the new enrichment integration.|

    ![Create new enrichment integration form](../image/enrich-sighting-splunk.png)

6.  In the Integration Configuration section, configure the integration details based on your requirements.

    The Integration Configuration section includes configuration details like API key, API Client ID or secret, username, password, and so on, which you need to fill in. These configuration details vary for different apps.

7.  Click the **Save** action to store and create the new enrichment integration configuration.

    The provided details are validated, and by default the enrichment integration's status is disabled.

8.  Click **Save as Draft** action to only store the updates made to the enrichment configuration and not create it.

    If you're not sure about the configuration details, you can use the **Save as Draft** option. After you get the configuration details, you can fill the remaining information in the draft version and create it.

9.  To enable the enrichment integration, click **Enable**.

    The enrichment integration is enabled successfully. You can also enable a particular enrichment integration by using the Actions menu of the required integration tile on the Catalog page or the All Integration page.


-   **[Define queries for Sighting Search](../concept/manage-sighting-search-configurations.md)**  
You can use sighting search configurations for defining the queries used to find the prevalence of observables in your environment as part of observable investigation.
-   **[Using Sighting Search Parameters](../concept/manage-sighting-search-parameters.md)**  
You can use sighting search parameters that define more complex queries, which include logic and other operators supported by the specified log store.
-   **[Get started with Elasticsearch integration](../concept/get-started-with-elasticsearch-integration.md)**  
The Elasticsearch enrichment integration searches your logs and adds relevant sighting information to your observables.
-   **[Get started with Splunk Search integration](../concept/get-started-with-splunk-search-integration.md)**  
Splunk software searches, monitors, and analyzes machine-generated big data and integrates easily with Security Operations. Before you can use the Splunk Sighting Search integration, you must download it from the ServiceNow Store.
-   **[TISC add-on for Splunk overview](../concept/tisc-addon-splunk.md)**  
The Threat Intelligence Security Center \(TISC\) for Splunk app offers integration between TISC and Splunk that enables users to seamlessly import the latest threat intelligence from TISC into Splunk for monitoring and enriching alerts. Users can configure indicator collections, perform searches and utilize dashboards to analyse search matches and indicator collections effectively.

**Parent Topic:**[Sighting Search](../concept/tisc-sighting-search.md)

