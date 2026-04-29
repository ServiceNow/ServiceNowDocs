---
title: Set up triggers for the Jamf spoke
description: Set up triggers for the Jamf spoke for the required events. The endpoint enables webhooks to connect with your ServiceNow instance.Configure endpoint for webhooks in the Jamf that support the token authentication.Create an outbound webhook in your Jamf Pro cloud instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-28"
reading_time_minutes: 1
breadcrumb: [Jamf Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up triggers for the Jamf spoke

Set up triggers for the Jamf spoke for the required events. The endpoint enables webhooks to connect with your ServiceNow instance.

## Before you begin

Role required: admin

## Configure triggers in ServiceNow instance

Configure endpoint for webhooks in the Jamf that support the token authentication.

### Before you begin

Role required: flow\_designer and connection\_admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Toggle and enable the **Inbound** connections.

4.  Locate the **Jamf Spoke** endpoint and click **View Details**.

5.  For the **Jamf External Trigger** end point, click **Configure**.

    ![](../image/jamf-ext-trigger.jpg)

6.  Select the user who can trigger the endpoint and click **Activate**.

    ![](../image/jamf-conf-trigger-user.jpg)

    The values **Token** and **URL** are generated.

7.  Copy the generated endpoint URL for later use.

    ![](../image/jamf-conf-trigger4.jpg)


## Create an outbound webhook

Create an outbound webhook in your Jamf Pro cloud instance.

### Before you begin

Role required: admin

### Procedure

1.  Log in to the Jamf cloud account as an admin.

2.  Click **Settings**.

3.  Click the **Global** tab and click the **Webhooks** tile.

4.  Click **+ New**.

5.  On the form, fill these values.

<table id="table_l22_ndb_t3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

A display name to identify the webhook.

</td></tr><tr><td>

Webhook URL

</td><td>

URL the webhook should post to. Paste the URL that was generated when you configured triggers in ServiceNow instance. For more information, see [Configure triggers in ServiceNow instance](jamf-setup-triggers.md#).

</td></tr><tr><td>

Authentication Type

</td><td>

Type of authentication required to connect to the webhook. Choose the **Header Authentication** option.When you select **Header Authentication**, another **Header Authentication** field is displayed. Provide the header metadata in JSON format that is used for authentication. For example, enter `{"Authorization":"Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdX", "Date":"Fri, 22 Nov 2024 16:56:32 GMT"}`.

</td></tr><tr><td>

Connection timeout

</td><td>

Connection timeout for the webhook.

</td></tr><tr><td>

Read Timeout

</td><td>

Read timeout for the webhook.

</td></tr><tr><td>

Content Type

</td><td>

Format for sending the webhook information. Select **JSON**.

</td></tr><tr><td>

Webhook Event

</td><td>

Event that will trigger the webhook. Select one of the supported events. For the list of supported events, see the [Spoke triggers](../concept/jamf-spoke.md#section_ijs_vfb_t3c) section.

</td></tr></tbody>
</table>    For more information about configuring the webhook, see [Configuring a Webhook](https://learn.jamf.com/r/en-US/jamf-pro-documentation-11.15.0/Webhooks) in [Jamf Learning Hub](https://learn.jamf.com/home).

6.  Click **Save**.


