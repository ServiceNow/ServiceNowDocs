---
title: Set up bi-directional webhook for the monday.com spoke
description: Configure a webhook to subscribe to monday.com with a ServiceNow callback URL.Register a monday webhook in ServiceNow to notify the ServiceNow app when certain events occur in monday.comSpecify a webhook callback URL in your monday account to create a webhook.Create a webhook routing policy and customize a subflow according to your requirements.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [monday.com Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up bi-directional webhook for the monday.com spoke

Configure a webhook to subscribe to monday.com with a ServiceNow callback URL.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the monday.com spoke.
-   [Set up the monday.com spoke](setup-monday.md#).
-   Role required: admin.

## Register the monday webhook in ServiceNow

Register a monday webhook in ServiceNow to notify the ServiceNow app when certain events occur in monday.com

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Monday Spoke** &gt; **Webhook** &gt; **Routing Policies** &gt; **Webhook Registry**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the webhook registry. For example, `monday spoke webhook registry`.|
    |Path|monday webhook path.|
    |Token|Authentication token from your ServiceNow instance which is used for validating monday.com spoke requests.|

4.  Right-click the form header and click **Save**.

5.  Click **Callback URL**.

    The system displays the webhook callback URL.

6.  Copy and record the webhook callback URL.


### Result

The monday webhook is registered in your ServiceNow instance and callback URL is generated.

## Add a callback URL in monday.com

Specify a webhook callback URL in your monday account to create a webhook.

### Before you begin

-   Register monday webhook and generate callback URL in your ServiceNow instance.
-   Role required: admin

### Procedure

1.  Login to [monday.com](https://monday.com/).

2.  Navigate to **Workspace** &gt; **Integrate** &gt; **Integrations Center** &gt; **Webhooks** &gt; **Add to board**.

3.  Open a workspace and right-click on **Integrate**.

4.  In the **Integrations Center** tab, click **Webhooks**.

5.  Select an event type and click **Add to board**.

6.  Specify the generated callback URL from ServiceNow instance and click **Connect**.


## Customize the bi-directional webhook in the monday.com spoke

Create a webhook routing policy and customize a subflow according to your requirements.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click **Subflows**.

3.  Create a copy of one of the available sublflows.

4.  Customize the subflow according to your requirement and publish it.

5.  Navigate to **Monday Spoke** &gt; **Routing Policies**.

6.  Click **New**.

7.  On the form, fill in the fields.

<table id="table_ryv_cgt_2wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label to identify the routing policy.

</td></tr><tr><td>

Answer

</td><td>

Option to specify if this answer is the default answer. Default answer is applicable when the conditions are not met.1.  Click the Lookup icon.
2.  Select the required subflow from the **Document**: list.
 **Note:** Ensure that the **Table name** is `Flow [sys_hub_flow].`

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the incoming webhook delivers data from monday.com.

</td></tr></tbody>
</table>8.  Click **Submit**.

    **Note:** These routing policies are saved in the Decision tables. Users are cautioned against directly updating or modifying data in these tables.


