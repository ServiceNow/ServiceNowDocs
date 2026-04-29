---
title: Get started with the Splunk Search integration for Security Operations
description: Splunk software searches, monitors, and analyzes machine-generated big data and integrates easily with Security Operations. Before you can use the Splunk - Incident Enrichment integration, you must download it from the ServiceNow Store and add the appropriate API Base URL and login credentials.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Splunk - Incident Enrichment integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with the Splunk Search integration for Security Operations

Splunk software searches, monitors, and analyzes machine-generated big data and integrates easily with Security Operations. Before you can use the Splunk - Incident Enrichment integration, you must download it from the ServiceNow Store and add the appropriate API Base URL and login credentials.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  [Download the integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

2.  When the installation is complete, access Splunk and obtain the API Key and API ID under your profile.

3.  In your instance, navigate to **Security Operations** &gt; **Integration Configuration**.

    The available security integrations appear as a series of cards.

4.  In the Splunk - Incident Enrichment card, click **New**.

    ![Splunk - Incident Enrichment Configuration](../image/splunk-new-config.png)

5.  Fill in the fields, as needed.

    |Field|Description|
    |-----|-----------|
    |Name|The name of this configuration.|
    |Splunk API Base URL|The base URL you acquired from the Splunk site.|
    |Link URL|\[Optional\] The Link URL that links to the Splunk web interface, when available.|
    |Username|Your Splunk username.|
    |Password|Your Splunk password.|
    |Max Rows|The maximum number of rows you want to search.|
    |Earliest Result \(days\)|The earliest results you want to see in number of days.|
    |Include raw data samples in search results|Select this to include samples of raw data in your sightings search results. The amount of data returned depends on your setting in the **number of rows of raw data** property in [Security Incident Response properties](../../../security-incident-response/reference/installed-with-sir.md).|
    |MID Server|Select **Any** to use any active MID Server, or select a specific MID Server name.|

    **Note:** Configuring this integration activates workflows. To manage the workflows, navigate to the **Workflow Editor**.

6.  Click **Submit**.

    The integration configuration card displays.

7.  When viewing the new configuration card, you can click **Configure** or **Delete** to change or delete the configuration, respectively.

8.  To return to the original list of integration configuration cards, select **No** from the **Show Configurations** drop-down list.


**Parent Topic:**[Splunk - Incident Enrichment integration](../reference/splunk-in-enrich-landing-page.md)

