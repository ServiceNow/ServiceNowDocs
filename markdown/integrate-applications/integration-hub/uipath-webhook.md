---
title: Set up the webhook
description: Configure a webhook to subscribe to events in the UiPath account with a ServiceNow callback URL.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [UiPath Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the webhook

Configure a webhook to subscribe to events in the UiPath account with a ServiceNow callback URL.

## Before you begin

-   [Set up the UiPath spoke](conf-alias-uipath.md#)
-   Role required: sn\_uipath\_spoke.uipath\_webhook\_registry\_user and decision\_table\_writer, or admin

## Procedure

1.  Create webhook registry in your ServiceNow instance.

    1.  Log in to your ServiceNow instance.

    2.  Navigate to **UiPath** &gt; **UiPath Webhook Registry**.

    3.  Click **New**.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the webhook registry record,|
        |Description|Description of the webhook registry.|

    5.  Click **Generate Callback URL and Secret**.

        Webhook callback URL and secret are generated and displayed.

        ![Webhook callback URL and secret.](../image/uipath-webhook-registry.png)

    6.  Copy and record the values of webhook callback URL and secret.

        **Note:** You can change the webhook secret periodically by clicking **Generate New Secret**. After changing the secret, the value must be updated in the UiPath account.

2.  Specify the webhook routing policies in your ServiceNow instance.

    1.  Log in to your ServiceNow instance.

    2.  Navigate to **UiPath** &gt; **UiPath WebHook Routing Policies**.

        Three routing policies are available along with the spoke. You can configure these records and can also create more records as per your requirement.

    3.  Open the required record.

    4.  Specify **Condition** that must be met.

    5.  For **Answer**, select the required subflow that must be triggered when the specified condition is met.

    6.  Click **Update**.

3.  Register the callback URL in the UiPath account.

    1.  Log in to your UiPath account as an admin.

    2.  Navigate to **Orchestrator** &gt; **Tenant**.

    3.  Click the **Webhooks** tab.

    4.  Click **+ Add webhook**.

    5.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |URL|Webhook callback URL you had copied from your ServiceNow instance.|
        |Enabled|Select this check box.|
        |Secret|Webhook secret you had copied from your ServiceNow instance.|
        |Event Type|Events for which you want to subscribe.|

    6.  Click **Save**.


