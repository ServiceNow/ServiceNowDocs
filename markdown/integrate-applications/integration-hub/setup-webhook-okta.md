---
title: Set up a bi-directional webhook for Okta spoke
description: Configure a webhook to subscribe to Okta with a ServiceNow callback URL.Register an Okta webhook in your ServiceNow instance to notify the ServiceNow app when certain events occur in Okta.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Okta Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a bi-directional webhook for Okta spoke

Configure a webhook to subscribe to Okta with a ServiceNow callback URL.

## Before you begin

-   Request an Integration Hub subscription
-   Install or activate the Okta spoke plugin
-   Role required: admin

## Register Okta webhook

Register an Okta webhook in your ServiceNow instance to notify the ServiceNow app when certain events occur in Okta.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Okta Spoke** &gt; **Okta Webhook Registry**.

2.  Select **New**.

3.  On the form, fill in these fields.

<table id="table_ogy_zk3_gqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name to identify the webhook registry.**Note:** The name must be only `Okta Webhook Authentication`.

</td></tr><tr><td>

Description

</td><td>

Short description of the webhook registry.

</td></tr><tr><td>

Authentication Key

</td><td>

Authentication key used for connecting to Okta webhook.

</td></tr><tr><td>

Authentication Value

</td><td>

Authentication value used for connecting to Okta webhook.

</td></tr></tbody>
</table>4.  Select **Submit**.


