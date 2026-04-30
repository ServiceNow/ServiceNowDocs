---
title: Configure and enable Splunk integration
description: The Splunk Enrichment integration searches your logs and adds relevant sighting information.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Get started with Splunk Search integration, Configure Sighting Search, Sighting Search, TISC Enrichment Integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure and enable Splunk integration

The Splunk Enrichment integration searches your logs and adds relevant sighting information.

## Before you begin

Before you can use the Splunk Search, you must download it from the ServiceNow Store.

Role required: sn\_sec\_tisc.admin

-   The Threat Intelligence Security Center plugin must be installed and activated before you can use the Splunk Search integration.
-   Obtain the Splunk and obtain the Splunk Search and obtain the API Base URL, Link URL, Username and Password from your Splunk instance.

## Procedure

1.  Using your instance, access **Threat Intelligence Security Center**.

2.  [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

3.  When the installation is complete, navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

4.  Select **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations**.

5.  Alternatively, you can navigate to **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Sighting Search**

    The configured integrations appear as a series of cards.

6.  In the **Splunk Search** card, click **Configure New Enrichment** to configure **Splunk Search** integration.

7.  Fill in the fields on the Configure New Enrichment form.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the sighting search configuration.|
    |Vendor Name|Name of the vendor. The details of the selected vendor is populated by default. For example, Splunk.|
    |Integration Type|Type of integration that you selected. For example, Threat Lookup.|
    |Description|Enter the description for the Splunk integration. For example, The Splunk enrichment integration aids in the investigation of a observable by supporting the querying of logs in your Splunk deployment in relation to potentially malicious indicators..|
    |**Integration Configuration**|
    |Splunk API Base URL|The base URL you acquired from the Splunk site.|
    |Link URL|\[Optional\] The Link URL that links to the Splunk web interface, when available.|
    |Username|Your Intel Elasticsearch username.|
    |Password|Your Intel Elasticsearch password.|
    |Max Rows|The maximum number of rows you want to search.|
    |Earliest Result \(days\)|The earliest results you want to see in number of days.|
    |Include raw data samples in search results|Select this to include samples of raw data in your sightings search results. The amount of data returned depends on your setting in the number of rows of raw data property in [Security Incident Response properties](https://servicenow.com/docs/bundle/vancouver-security-management/page/product/security-incident-response/reference/installed-with-sir.html).|
    |On Premises Deployment|The On Premises Deployed environment.|
    |MID Server|Select Any to use any active MID Server, or select a specific MID Server name.|

    **Note:** Configuring this integration activates workflows. To manage the workflows, navigate to the Workflow Editor.

8.  Click **Save**.

    The integration details are validated, and by default the Splunk integration's status is disabled.

9.  Click **Enable** to enable the Splunk integration.


## Result

After it is configured, Splunk can be selected for performing sighting search on observables in Threat Intelligence Security Center.

**Parent Topic:**[Get started with Splunk Search integration](../concept/get-started-with-splunk-search-integration.md)

