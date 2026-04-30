---
title: Set up the webhook
description: Configure a webhook to subscribe to GovNotify with a ServiceNow callback URL.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [GovNotify Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the webhook

Configure a webhook to subscribe to GovNotify with a ServiceNow callback URL.

## Before you begin

-   [Set up the GovNotify spoke](govnotify-setup.md)
-   Role required: admin

## Procedure

1.  Copy the scripted REST API URL for the GovNotify spoke from your ServiceNow instance.

    1.  Navigate to **System Web Services** &gt; **Scripted REST APIs**.

    2.  Open the record, **GovNotify Callback**.

    3.  Copy and record the value of **Base API path** for later use.

2.  Add the callback URL in GovNotify account.

    1.  Log in to your GovNotify account as admin.

    2.  Navigate to **API integration** and click **Callbacks**.

        ![Callback URL.](../image/govnotify-callback.png)

    3.  On the form, enter these values.

        |Field|Description|
        |-----|-----------|
        |URL|Callback URL in this format: `https://<ServiceNow-instance>.com/<base-api-path>`.|
        |Bearer token|Token to authenticate the request. Enter a token as per your requirement.|

    4.  Click **Save**.

3.  Create client record in your ServiceNow instance.

    1.  Navigate to **GovNotify Spoke** &gt; **Client Details**.

    2.  Click **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the client record.|
        |Authorization Key|Bearer token you had provided in the GovNotify account.|

    4.  Click **Submit**.

4.  Create webhook answer record in your ServiceNow instance.

    1.  Navigate to **GovNotify Spoke** &gt; **Webhook Decision Answers**.

    2.  Click **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Subflow|Subflow that needs to be triggered. Select the default subflow or the subflow you had configured as per your requirement.|
        |Description|Description of the webhook decision answer.|

    4.  Click **Submit**.

5.  Configure the webhook decision policy in your ServiceNow instance.

    1.  Navigate to **System Definition** &gt; **Decision Tables**.

    2.  Open the record, **GovNotify Webhook Decision Policy**.

    3.  In the **Decisions** tab, open the **Default decision** record.

    4.  For **Answer**, select the sys\_ID of the webhook answer record you had created.

    5.  Click **Update**.

        The subflow that is configured in the webhook answer record is triggered when conditions in the webhook decision policy are met.


