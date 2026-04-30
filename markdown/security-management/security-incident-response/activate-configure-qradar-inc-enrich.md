---
title: Get started with the IBM QRadar - Incident Enrichment integration
description: IBM QRadar is an enterprise security information and event management \(SIEM\) product that integrates easily with Security Operations. Before you can use the IBM QRadar - Incident Enrichment integration, you must download it from the ServiceNow Store and add the appropriate API Base URL and API Key.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [IBM QRadar - Incident Enrichment Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with the IBM QRadar - Incident Enrichment integration

IBM QRadar is an enterprise security information and event management \(SIEM\) product that integrates easily with Security Operations. Before you can use the IBM QRadar - Incident Enrichment integration, you must download it from the ServiceNow Store and add the appropriate API Base URL and API Key.

## Before you begin

Role required: sn\_si\_admin

## Procedure

1.  [Download the integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

2.  When the installation is complete, access IBM QRadar and obtain the API Base URL and API Key under your IBM QRadar profile.

3.  In your instance, navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

    The available security integrations appear as a series of cards.

4.  In the IBM QRadar - Incident Enrichment card, click **New**.

    ![IBM QRadar - Incident Enrichment Configuration](../image/QRadar-config.png)

5.  Fill in the fields, as needed.

    |Field|Description|
    |-----|-----------|
    |Name|The name of this configuration.|
    |QRadar API Base URL|The base URL you acquired from the IBM QRadar site.|
    |Link URL|\[Optional\] The Link URL that links to an IBM QRadar instance, when available.|
    |Version|The IBM QRadar version; 5.0 is the default.|
    |API Key|The API key you obtained from the IBM QRadar site.|
    |Max Rows|The maximum number of rows you want to search.|
    |Earliest Result \(days\)|The earliest results you want to see in number of days.|
    |Include raw data samples in search results|Select this to include samples of raw data in your sightings search results. The amount of data returned depends on your setting in the **number of rows of raw data** property in [Security Incident Response properties](../../../security-incident-response/reference/installed-with-sir.md).|
    |MID Server|Select **Any** to use any active MID Server, or select a specific MID Server name.|

    **Note:** Configuring this integration activates workflows. To manage the workflows, navigate to the **Workflow Editor**.

6.  Click **Submit**.

    The integration configuration card displays.

7.  When viewing the new configuration card, you can click **Configure** or **Delete** to change or delete the configuration, respectively.

8.  To return to the original list of integration configuration cards, select **No** from the **Show Configurations** drop-down list.


**Parent Topic:**[IBM QRadar - Incident Enrichment Integration](../reference/qradar-landing-page.md)

