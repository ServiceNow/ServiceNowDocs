---
title: Add Slack connection in ServiceNow instance
description: Add the Slack connection in Workflow Studio to configure the Slack spoke.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up Slack spoke, Slack Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Add Slack connection in ServiceNow instance

Add the Slack connection in Workflow Studio to configure the Slack spoke.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

    **Note:** You can add multiple connections for your Slack spoke; one for each Slack workspace.

4.  On the Slack spoke tile, click **View Details**.

5.  In the Connections page, click **Configure**.

    The pop-up window displays a blank Configure Connection form.

6.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Connection URL|URL to connect to Slack. Enter `https://slack.com`.|
    |Credential Name|Name to identify the credential record. For example, `Slack Cred`.|
    |OAuth Name|Name to identify the OAuth record. For example, `Slack OAuth`.|
    |OAuth Client ID|Client ID of your Slack app.|
    |OAuth Client Secret|Client Secret of your Slack app.|
    |OAuth Redirect URL|Redirect URL provided in your Slack app. This value is auto-populated.|

7.  Click **Configure and Get OAuth Token**.

8.  In the pop-up window, click **Allow**.

    The OAuth Access token is generated for the Slack spoke.


