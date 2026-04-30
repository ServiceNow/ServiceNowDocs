---
title: Set up a bi-directional webhook for Zoom spoke
description: Configure a webhook to subscribe to Zoom with a ServiceNow callback URL.Specify an endpoint URL in your Zoom account to create a webhook for Zoom spoke.Register a Zoom webhook in ServiceNow to notify the ServiceNow app when certain events occur in Zoom.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zoom Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up a bi-directional webhook for Zoom spoke

Configure a webhook to subscribe to Zoom with a ServiceNow callback URL.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Zoom spoke.
-   Role required: admin.

## Add an endpoint URL in Zoom account

Specify an endpoint URL in your Zoom account to create a webhook for Zoom spoke.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your Zoom account.

2.  Create a webhook app according to your requirements.

    For more information about Zoom webhook only app, see [Create a Webhook-only App](https://developers.zoom.us/docs/api/rest/webhook-only-app/).

3.  Generate a verification token and secret token and record the token values.

4.  Create a webhook validation for Zoom spoke.

5.  1.  Log in to your ServiceNow instance.
2.  Navigate to **Zoom spoke** &gt; **Zoom Webhook Validations.**
3.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the webhook validation record. For example, Zoom spoke webhook validation.|
    |Secret Token|Secret token of the app in your Zoom account.|
    |Verification Token|Verification token of the app in your Zoom account.|

4.  Click Submit.
6.  Enable Event Subscriptions and enter the Event notification endpoint URL in the following format.

    `https://<instance-name>.service-now.com/api/sn_zoom_spoke/zoom_webhook_endpoint/webhook`

7.  Validate the event notification endpoint URL.

    For more information, see [Validate your webhook endpoint](https://developers.zoom.us/docs/api/rest/webhook-reference/#validate-your-webhook-endpoint).![Validate event notification endpoint URL in your Zoom account](../image/zoom-spoke-webhook-validate.png)

8.  Specify the Event Types according to your requirement.


### Result

The endpoint URL is added in your Zoom account. You can create webhook registries and subflows according to your requirements.

## Register a Zoom webhook in ServiceNow

Register a Zoom webhook in ServiceNow to notify the ServiceNow app when certain events occur in Zoom.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Zoom Spoke** &gt; **Zoom Webhook Registries**.

2.  Click **New**.

3.  On the form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Trigger Type|Type of the Zoom event that triggers the subflow.|
    |Token|Verification token from your Zoom account used for validating event notification.|
    |Subflow Name|Subflow which is to be triggered when the specified conditions are met.|
    |Input|Input for the webhook registry.|
    |Trigger Object|Zoom object which is used to trigger the subflow.|
    |Name|Name of the webhook registry.|


