---
title: Get started with the Carbon Black - Incident Enrichment integration
description: The Carbon Black incident enrichment facilitates the investigation of a security incident by querying logs for potentially malicious indicators. Before you can use the Carbon Black - Incident Enrichment integration, you must download it from the ServiceNow Store and add the appropriate Endpoint Base URL and MID server.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Carbon Black - Incident Enrichment integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with the Carbon Black - Incident Enrichment integration

The Carbon Black incident enrichment facilitates the investigation of a security incident by querying logs for potentially malicious indicators. Before you can use the Carbon Black - Incident Enrichment integration, you must download it from the ServiceNow Store and add the appropriate Endpoint Base URL and MID server.

## Before you begin

Role required: sn\_si\_admin

## Procedure

1.  [Download the integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

2.  When the download is complete, access the Carbon Black website and obtain the Endpoint Base URL and API Token under your profile.

3.  In your instance, navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configuration**.

4.  In the Carbon Black - Incident Enrichment card, click **Configure**.

    ![Configure Carbon Black - Incident Enrichment integration](../image/carbonblack-config-inc.png)

5.  Fill in the fields, as needed.

    |Field|Description|
    |-----|-----------|
    |Name|The name of this configuration.|
    |Endpoint Base|The endpoint URL you acquired from the Carbon Black site.|
    |Link URL|The Link URL that links to a Carbon Black instance, when available.|
    |API Token|The API token you acquired from the Carbon Black site.|
    |Max Rows|The maximum number of rows you want to search. The default is 1000 rows.|
    |Earliest Result \(days\)|The earliest results you want to see in number of days.|
    |Perform binary and process search|Select this to perform binary searches to find binary files such as file hashes, and process searches for .exe processes that may have run.|
    |Include raw data samples in search results|Select this to include samples of raw data in your sightings search results. The amount of data returned depends on your setting in the **number of rows of raw data** property in [Security Incident Response properties](../../../security-incident-response/reference/installed-with-sir.md).|
    |MID Server|Select **Any** to use any active MID Server, or select a specific MID Server name.|

    **Note:** Configuring this integration activates workflows. To manage the workflows, navigate to the **Workflow Editor**.

6.  Click **Submit**.

    The integration configuration card displays.

7.  To return to the original list of integration configuration cards, select **No** from the **Show Configurations** drop-down list.


