---
title: Set up a bi-directional webhook for the Box spoke
description: Configure a webhook to subscribe to Box with a ServiceNow callback URL.Specify an endpoint URL in your Box account to create a webhook for Box spoke.Create a Box webhook registry in ServiceNow to notify the ServiceNow app when certain events occur in your Box account.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Box Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a bi-directional webhook for the Box spoke

Configure a webhook to subscribe to Box with a ServiceNow callback URL.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Box spoke.
-   Role required: admin.

## Add an endpoint URL in a Box account

Specify an endpoint URL in your Box account to create a webhook for Box spoke.

### Before you begin

Role required: admin

### Procedure

1.  Log in to the [Box developer's console](https://app.box.com/developers/console).

2.  Create an app according to your requirements.

    For more information about app creation, see [Create an OAuth application](setup-box-spoke.md#).

3.  Generate a primary Key and secondary Key for your app and record the values.

    1.  In **My Apps**, select the application.

        You are in your application's **General Settings**.

    2.  Navigate to **Webhooks**.

    3.  Select **Manage Signature Keys**.

    4.  In the Primary Key section, select **Generate Key**.

    5.  In the Secondary Key section, select **Generate Key**.

    6.  Copy and save both key values for later.

4.  Navigate to the **Webhooks** section.

5.  To create a V1 webhook, select **Create Webhook** and select **V1**.

    1.  Complete the fields.

<table id="table_ngv_xcj_tzb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

`Update Chatter feed`

</td></tr><tr><td>

Description

</td><td>

`Automatically updates your Chatter feed when a change occurs`

</td></tr><tr><td>

Event Type

</td><td>

Enable at least one option

</td></tr><tr><td>

Endpoint URL

</td><td>

The endpoint URL of the ServiceNow instance in the following format: `https://<instance-name>.service-now.com/api/sn_box_spoke/box_spoke_webhook_endpoints/webhook_endpoint`

</td></tr><tr><td>

Payload format

</td><td>

Select the appropriate payload data format

</td></tr><tr><td>

Callback Parameters

</td><td>

Select **add callback parameter** to configure any GET or POST methods

</td></tr></tbody>
</table>    2.  Select **Save Webhoook**.

6.  To create a V2 webhook, select **Create Webhook** and select **V2**.

    **Note:** To create a V2 webhook, you must enable **Manage webhooks** in the **Configuration** settings. For more information, see [Create an OAuth application](setup-box-spoke.md#).

    1.  For the URL Address, enter the endpoint URL of the ServiceNow instance in the following format: `https://<instance-name>.service-now.com/api/sn_box_spoke/box_spoke_webhook_endpoints/webhook_endpoint`.

    2.  For The type of item to trigger a webhook, select **Choose an item**.

    3.  Select the webhook configured file or folders.

    4.  To confirm select **Choose**.

        A list of configured webhook triggers display in the **Create a Webhook** page.

    5.  Enable the appropriate GET and POST methods for each trigger.

    6.  To confirm, select **Create Webhook**.


### Result

The endpoint URL is added in your Box account. You can create webhook registries and subflows according to your requirements.

## Register a Box webhook in ServiceNow

Create a Box webhook registry in ServiceNow to notify the ServiceNow app when certain events occur in your Box account.

### Before you begin

Role required: admin.

### Procedure

1.  In your ServiceNow, navigate to **All** &gt; **Box** &gt; **Box Webhook Registry**.

2.  Select **New**.

3.  Fill in the fields.

<table id="table_bny_tg5_fpb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Optionally, name the webhook registry

</td></tr><tr><td>

Trigger Name

</td><td>

Select the appropriate event trigger

</td></tr><tr><td>

Primary Key

</td><td>

The primary key that you generated in [Add an endpoint URL in a Box account](setup-webhook-box-spoke.md#)

</td></tr><tr><td>

Flow Name

</td><td>

The flow that occurs when the event triggers

</td></tr><tr><td>

Secondary Key

</td><td>

The secondary key that you generated in [Add an endpoint URL in a Box account](setup-webhook-box-spoke.md#)

</td></tr><tr><td>

Description

</td><td>

Optionally, describe the purpose of the record

</td></tr></tbody>
</table>4.  To confirm, select **Submit**.


### Result

The Box webhook is registered in your ServiceNow instance.

