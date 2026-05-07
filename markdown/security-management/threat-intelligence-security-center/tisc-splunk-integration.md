---
title: Configure and enable Splunk integration
description: Configure the Splunk Enrichment integration to automatically search your logs and add relevant sighting information to threat intelligence data.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Get started with Sighting Search Configurations, Configure Sighting Search, TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure and enable Splunk integration

Configure the Splunk Enrichment integration to automatically search your logs and add relevant sighting information to threat intelligence data.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Important:**

-   Download the Splunk Search app from the ServiceNow Store to get started.
-   Install and activate the Threat Intelligence Security Center plugin to enable the Splunk Search integration.
-   From your Splunk instance, copy the API Base URL, Link URL, Username, and Password.

## Procedure

1.  In your instance, navigate to **Threat Intelligence Security Center**.

2.  [Download the integration from the ServiceNow Store](../../security-incident-response/reference/download-app-first-time.md).

3.  When the installation is complete, navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

4.  Select **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations**.

5.  Navigate to **Integrations** &gt; **Enrichment Integrations** &gt; **All Integrations** &gt; **Sighting Search**

    The configured integrations appear as a series of cards.

6.  In the **Splunk Search** card, select **Configure New Enrichment** to configure **Splunk Search** integration.

7.  Complete the fields on the Configure New Enrichment form.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the sighting search configuration.|
    |Vendor Name|Name of the vendor. The details of the selected vendor is populated by default. For example, Splunk.|
    |Integration Type|Type of integration that you selected. For example, Threat Lookup.|
    |Description|Description for the Splunk integration. For example, The Splunk enrichment integration aids in the investigation of an observable by supporting the querying of logs in your Splunk deployment in relation to potentially malicious indicators.|
    |**Integration Configuration**|
    |Splunk API Base URL|Base URL from the Splunk site.|
    |Link URL|\[Optional\] The URL that links to the Splunk web interface, when available.|
    |Username|Your Intel Splunk username.|
    |Password|Your Intel Splunk password.|
    |Max Rows|Maximum number of rows to search.|
    |Earliest Result \(days\)|Displays earliest results in number of days.|
    |Include raw data samples in search results|When selected, includes samples of raw data in sightings search results. The amount of data returned depends on your setting in the number of rows of raw data property in [Security Incident Response properties](https://servicenow.com/docs/bundle/vancouver-security-management/page/product/security-incident-response/reference/installed-with-sir.html).|
    |On Premises Deployment|Indicates whether the deployment is on premises.|
    |MID Server|Select **Any** option to use any active MID Server, or select a specific MID Server name.|

    **Note:** Configuring this integration activates workflows. To manage the workflows, navigate to the **Flow Designer** &gt; **Flows** and make necessary changes in the workflow editor, if required.

8.  Select **Save** to apply the changes.

    The integration details are validated, and by default the Splunk integration's status is turned off.

9.  Select **Enable** to enable the Splunk integration.


## What to do next

After you configure the integration, you can select Splunk to perform sighting searches on observables in Threat Intelligence Security Center.

**Parent Topic:**[Get started with Sighting Search Configurations](../concept/tisc-get-sighting-configs.md)

