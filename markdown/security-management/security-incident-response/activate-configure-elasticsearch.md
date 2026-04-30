---
title: Get started with the Elasticsearch - Incident Enrichment integration
description: Elasticsearch is a distributed, RESTful search and analytics engine that easily integrates with Security Operations. Before you can use the Elasticsearch - Incident Enrichment integration, you must download it from the ServiceNow Store and add the appropriate API Base URL and login credentials.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Elasticsearch Incident Enrichment integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with the Elasticsearch - Incident Enrichment integration

Elasticsearch is a distributed, RESTful search and analytics engine that easily integrates with Security Operations. Before you can use the Elasticsearch - Incident Enrichment integration, you must download it from the ServiceNow Store and add the appropriate API Base URL and login credentials.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  [Download the integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

2.  When the installation is complete, access Elasticsearch and obtain the API Base URL under your Elasticsearch profile.

3.  In your instance, navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

    The available security integrations appear as a series of cards.

4.  In the Elasticsearch - Incident Enrichment card, click **New**.

    ![Elastic configuration](../image/elastic-config.png)

5.  Fill in the fields, as needed.

    |Field|Description|
    |-----|-----------|
    |Name|The name of this configuration.|
    |Elasticsearch API Base URL|The base URL you acquired from the Elasticsearch site.|
    |Link URL|\[Optional\] Links to a Kibana instance, when available|
    |Username|Your Intel Elasticsearch username.|
    |Password|Your Intel Elasticsearch password.|
    |Max Rows|The maximum number of rows you want to search.|
    |Earliest Result \(days\)|The earliest results you want to see in number of days.|
    |Include raw data samples in search results|Select this to include samples of raw data in your sightings search results. The amount of data returned depends on your setting in the **number of rows of raw data** property in [Security Incident Response properties](../../../security-incident-response/reference/installed-with-sir.md).|
    |MID Server|Select **Any** to use any active MID Server, or select a specific MID Server name.|

    **Note:** Configuring this integration activates workflows. To manage the workflows, navigate to the **Workflow Editor**.

6.  Click **Submit**.

    The integration configuration card displays.

7.  When viewing the new configuration card, you can click **Configure** or **Delete** to change or delete the configuration, respectively.

8.  To return to the original list of integration configuration cards, select **No** from the **Show Configurations** drop-down list.


## Result

After it is configured, the Elasticsearch - Incident Enrichment integration can be selected for publishing observables to watchlists in Security Incident Response.

**Parent Topic:**[Elasticsearch Incident Enrichment integration](../reference/elasticsearch-landing-page.md)

