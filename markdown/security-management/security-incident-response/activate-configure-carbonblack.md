---
title: Get started with the Carbon Black integration
description: Carbon Black is an advanced security system easily integrating with Security Operations. Before you can use the Carbon Black integration, you must download the integration from the ServiceNow Store and add the appropriate Endpoint Base and API Token.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Carbon Black integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with the Carbon Black integration

Carbon Black is an advanced security system easily integrating with Security Operations. Before you can use the Carbon Black integration, you must download the integration from the ServiceNow Store and add the appropriate Endpoint Base and API Token.

## Before you begin

Role required: sn\_si\_admin

## Procedure

1.  [Download the integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

2.  When the installation is complete, access the Carbon Black website and obtain the Endpoint Base URL and API Token under your profile.

3.  In your instance, navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

    The available security integrations appear as a series of cards.

4.  In the Carbon Black card, click **New**.

    ![Carbon Black Configuration](../../secops-integration-carbonblack-inc-enrichment/image/carbonblack-config.png)

5.  Fill in the fields, as needed.

    |Field|Description|
    |-----|-----------|
    |Name|The name of this configuration.|
    |Endpoint Base|The endpoint base you acquired from the Carbon Black site.|
    |API Token|The API token you acquired from the Carbon Black site.|
    |Use MID Server|Select this check box if it is not already checked.|
    |MID Server|Select **Any** to use any active MID Server, or select a specific MID Server name.|
    |Enable Isolate Host|Select this check box to allow selected configuration items to be isolated from the **Configuration Items** related list tab in a security incident.|

    **Note:** Configuring this integration activates workflows. To manage the workflows, navigate to the **Workflow Editor**.

6.  Click **Submit**.

    The integration configuration card displays.

7.  To return to the original list of integration configuration cards, select **No** from the **Show Configurations** drop-down list.


