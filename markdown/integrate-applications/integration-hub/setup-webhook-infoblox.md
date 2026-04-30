---
title: Set up a bi-directional webhook for the Infoblox spoke
description: Configure a webhook to subscribe to Infoblox with a ServiceNow callback URL.Register a Infoblox webhook in a ServiceNow instance to notify the ServiceNow application when certain events occur in Infoblox.Specify a webhook callback URL in Infoblox account to create a webhook.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Infoblox Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a bi-directional webhook for the Infoblox spoke

Configure a webhook to subscribe to Infoblox with a ServiceNow callback URL.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Infloblox spoke.
-   Role required: admin.

## Register a Infoblox webhook

Register a Infoblox webhook in a ServiceNow instance to notify the ServiceNow application when certain events occur in Infoblox.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Infoblox spoke** &gt; **Webhook Registry**.

2.  Click **New**.

3.  On the form, fill in these fields.

<table id="table_rwr_ybd_gqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the webhook registry.**Note:** The name must be only `Infoblox Webhook Authentication`.

</td></tr><tr><td>

Username

</td><td>

Username specified in the Infoblox outbound endpoint configuration.

</td></tr><tr><td>

Password

</td><td>

Password specified in the Infoblox outbound endpoint configuration.

</td></tr><tr><td>

Description

</td><td>

Description of the webhook registry.

</td></tr><tr><td>

Path

</td><td>

Infoblox webhook path. This is field is auto-populated with `api/sn_infoblox_spoke/infoblox_webhook`.

</td></tr></tbody>
</table>4.  Right-click the form header and click **Save**.

5.  Click **Callback URL**.

    The system displays the webhook callback URL.

6.  Copy and record the webhook callback URL.


## Add callback URL in Infoblox

Specify a webhook callback URL in Infoblox account to create a webhook.

### Before you begin

-   Register a Infoblox webhook
-   Download Infoblox outbound templates from the [KB0966373](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0966373)
-   Role required: admin

### Procedure

1.  Log in to your Infoblox account.

2.  Create a webhook in your Infoblox account.

    For more information, see [KB0966373](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0966373).

3.  Configure a outbound endpoint for your ServiceNow instance.

    For more information about configuring Infoblox outbound endpoints, see [About Outbound Templates](https://docs.infoblox.com/display/NAG8/About+Outbound+Templates#AboutOutboundTemplates-bookmark3405).

4.  Configure templates by uploading the templates from the [KB0966373](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0966373) article.

    |Template name|Description|
    |-------------|-----------|
    |Host\_Address\_IPv4\_Insert.txt|Template to configure notifications when a new IPv4 address is added to a host.|
    |Range\_IPv4\_Insert.txt|Template to configure notifications when a new IPv4 range is added.|
    |Network\_Insert.txt|Template to configure notifications when a new IPv4 network is added.|
    |Host\_Address\_IPv6\_Insert.txt|Template to configure notifications when a new IPv6 address is added to a host.|

5.  Configure notifications rules using the Notification Wizard.


