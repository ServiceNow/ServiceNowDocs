---
title: Get started with the HPE ArcSight Logger - Incident Enrichment integration
description: HPE ArcSight Logger streams real-time data and categorizes them into specific logs and easily integrates with Security Operations. Before you can use the HPE ArcSight Logger - Incident Enrichment integration, you must download it from the ServiceNow Store and add API URL and login credentials.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [HPE ArcSight Logger - Incident Enrichment integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with the HPE ArcSight Logger - Incident Enrichment integration

HPE ArcSight Logger streams real-time data and categorizes them into specific logs and easily integrates with Security Operations. Before you can use the HPE ArcSight Logger - Incident Enrichment integration, you must download it from the ServiceNow Store and add API URL and login credentials.

## Before you begin

Role required: sn\_si\_admin

## Procedure

1.  [Download the integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

2.  When the installation is complete, navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

    The available security integrations appear as a series of cards.

3.  In the HPE ArcSight Logger - Incident Enrichment card, click **New**.

    ![HPE ArcSight Logger configuration](../image/arcsight-config.png)

4.  Fill in the fields, as needed.

    |Field|Description|
    |-----|-----------|
    |Name|The name of this configuration.|
    |ArcSight Logger API Base URL|The base URL you acquired from the HPE Security ArcSight Logger site.|
    |Link URL|\[Optional\] The Link URL that links to an HPE Security ArcSight Logger instance, when available.|
    |Username|Your Intel HPE ArcSight Logger username.|
    |Password|Your Intel HPE ArcSight Logger password.|
    |Earliest Result \(days\)|The earliest results you want to see in number of days.|
    |Max Rows|The maximum number of rows you want to search.|
    |All Peers|The default is unchecked and searches only the local logger you are connected to. When checked, it searches all the loggers that are connected to one another.|
    |Include raw data samples in search results|Select this to include samples of raw data in your sightings search results. The amount of data returned depends on your setting in the **number of rows of raw data** property in [Security Incident Response properties](../../../security-incident-response/reference/installed-with-sir.md).|
    |MID Server|Select **Any** to use any active MID Server, or select a specific MID Server name.|

    **Note:** Configuring this integration activates workflows. To manage the workflows, navigate to the **Workflow Editor**.

5.  Click **Submit**.

    The integration configuration card displays.

6.  When viewing the new configuration card, you can click **Configure** or **Delete** to change or delete the configuration, respectively.

7.  To return to the original list of integration configuration cards, select **No** from the **Show Configurations** drop-down list.


**Parent Topic:**[HPE ArcSight Logger - Incident Enrichment integration](../reference/arcsight-logger-landing-page.md)

