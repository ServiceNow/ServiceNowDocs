---
title: Set up a webhook
description: Configure a webhook to subscribe to Zendesk with a ServiceNow callback URL.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Zendesk Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a webhook

Configure a webhook to subscribe to Zendesk with a ServiceNow callback URL.

## Before you begin

Role required: admin

## Procedure

1.  Register a Zendesk webhook in ServiceNow to notify ServiceNow when certain events occur in Zendesk.

    1.  Log in to your ServiceNow instance as an admin.

    2.  Navigate to **Zendesk Spoke** &gt; **Webhook Registries**.

    3.  Click **New**.

    4.  Provide a name to identify the webhook registry record for **Name**.

    5.  Click the Generate Token related link.

        A secret token is generated and displayed. This values is also updated in **Token**.

    6.  Right-click the form header and click **Save**.

    7.  Click **Create Webhook**.

        A confirmation message is displayed that the webhook creation is initiated and value of **Webhook ID** is populated.

2.  In the Zendesk account, set up event-based rules that run every time a ticket is created or updated.

    1.  Log in to the Zendesk account.

    2.  Navigate to Zendesk Admin Center.

    3.  Navigate to **Objects and rules** &gt; **Business rules** &gt; **Triggers**.

    4.  Click **Add trigger**.

    5.  On the form, fill these values.

<table id="table_owm_ndb_hxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger name

</td><td>

Name to identify the trigger.

</td></tr><tr><td>

Category

</td><td>

Required event category. Select **Tickets**.

</td></tr><tr><td>

Conditions

</td><td>

Trigger conditions.Under **Meet ANY of the following conditions**, provide these conditions:![Trigger conditions.](../image/zendesk-trigger-condition.png)

</td></tr><tr><td>

Actions

</td><td>

Select **Notify active webhook** for **Notifications** and select the ServiceNow webhook.In **JSON body**, enter:

```
{ 
"id":"{{ticket.id}}", 
"priority":"{{ticket.priority}}", 
"status":"{{ticket.status}}", 
"subject":"{{ticket.title}}", 
"description":"{{ticket.description}}", 
"due_at":"{{ticket.due_date}}", 
"requester":"{{ticket.requester.name}}" 
}
```

</td></tr></tbody>
</table>    6.  Click **Create**.

        A confirmation message is displayed that the trigger is created.


## Result

The webhook is setup. When a ticket is created or updated in Zendesk, the details are stored in your ServiceNow instance. To access the Zendesk tickets in your ServiceNow instance, navigate to **Zendesk Spoke** &gt; **Webhook** &gt; **Tickets**.

