---
title: Configure and enable Elasticsearch integration
description: Elasticsearch is a distributed, RESTful search and analytics engine that easily integrates with Security Operations.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Get started with Elasticsearch integration, Configure Sighting Search, Sighting Search, TISC Enrichment integrations, TISC Integrations, Integrate Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Configure and enable Elasticsearch integration

Elasticsearch is a distributed, RESTful search and analytics engine that easily integrates with Security Operations.

## Before you begin

Before you can use the Elasticsearch, you must download it from the ServiceNow Store.

Role required: sn\_sec\_tisc.admin

-   The Threat Intelligence Security Center plugin must be installed and activated before you can use the Elasticsearch integration.
-   Obtain the Elasticsearch API Base URL, Kibana Base URL, Username, and Password under your Elasticsearch profile.

## Procedure

1.  Using your instance, access **Threat Intelligence Security Center**.

2.  [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

3.  When the installation is complete, navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

4.  Select **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations**.

5.  Alternatively, you can navigate to **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Sighting Search**

    **Note:** The configured integrations appear as a series of cards.

6.  In the **Elasticsearch** card, click **Configure New Enrichment** to configure **Elasticsearch** integration.

7.  Fill in the fields on the Configure New Enrichment form.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the sighting search configuration.|
    |Vendor Name|Name of the vendor. The details of the selected vendor is populated by default. For example, Elasticsearch.|
    |Integration Type|Type of integration that you selected. For example, Threat Lookup.|
    |Description|Enter the description for the Elasticsearch integration. For example, The Elasticsearch enrichment integration aids in the investigation of an observable by supporting the querying of logs in your Elasticsearch deployment.|
    |**Integration Configuration**|
    |Elasticsearch API Base URL|The base URL you acquired from the Elasticsearch site.|
    |Kibana Base URL|The Kibana Base URL. \[Optional\] Links to a Kibana instance, when available.|
    |Username|Your Intel Elasticsearch username.|
    |Password|Your Intel Elasticsearch password.|
    |Elasticsearch Index|The Elasticsearch index. These in turn will hold documents that are unique to each index. Indices are identified by lowercase names that refer to actions that are performed actions \(such as searching and deleting\).|
    |Date range field|The timestamp of the configuration.|
    |Max Rows|The maximum number of rows you want to search.|
    |Earliest Result \(days\)|The earliest results you want to see in number of days.|
    |Include raw data samples in search results|Select this to include samples of raw data in your sightings search results. The amount of data returned depends on your setting in the number of rows of raw data property in [Security Incident Response properties](https://servicenow.com/docs/bundle/vancouver-security-management/page/product/security-incident-response/reference/installed-with-sir.html).|
    |MID Server|Select Any to use any active MID Server, or select a specific MID Server name.|

    **Note:** Configuring this integration activates workflows. To manage the workflows, navigate to the Workflow Editor.

8.  Click **Save**.

    The integration details are validated, and by default the Elasticsearch integration's status is disabled.

9.  Click **Enable** to enable the Elasticsearch integration.


## Result

After it is configured, Elasticsearch can be selected for performing sighting search on observables in Threat Intelligence Security Center.

**Parent Topic:**[Get started with Elasticsearch integration](../concept/get-started-with-elasticsearch-integration.md)

