---
title: Set up a webhook
description: Configure a webhook to subscribe to Trello with a ServiceNow callback URL.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Trello Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up a webhook

Configure a webhook to subscribe to Trello with a ServiceNow callback URL.

## Before you begin

Role required: admin

## Procedure

1.  Log in to your ServiceNow instance as an admin.

2.  Copy the value of base API path.

    1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted REST APIs**.
    2.  Locate the record, **Trello Webhooks**.
    3.  Copy the value populated in **Base API path** and record it for later use.
3.  Create a webhook registry for the Trello spoke.

    1.  Navigate to **All** &gt; **Trello Spoke** &gt; **Webhook** &gt; **Webhook Registries**.
    2.  Click **New**.
    3.  On the form, fill the values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the webhook registry record.|
        |Path|Base API path URL you had copied.|
        |Token|Token record as per your requirement.|

    4.  Right-click the form header and click **Save**.
    5.  Click **Callback URL**.

        The webhook callback URL is generated and displayed.

    6.  Copy the webhook callback URL and record it for later use.

## What to do next

Provide the webhook callback URL when you run the Create Webhook spoke action. For the required board the webhook is created.

