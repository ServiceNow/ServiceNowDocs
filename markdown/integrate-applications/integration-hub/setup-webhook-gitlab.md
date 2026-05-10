---
title: Set up bi-directional webhook for the GitLab spoke
description: Configure a webhook to subscribe to GitLab with a ServiceNow callback URL.Register GitLab in ServiceNow to notify the ServiceNow app when certain events occur in GitLab.Create webhook routing policy and subflow as per your requirement in the GitLab spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [GitLab Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up bi-directional webhook for the GitLab spoke

Configure a webhook to subscribe to GitLab with a ServiceNow callback URL.

## Before you begin

-   Request Integration Hub subscription
-   Activate the GitLab spoke
-   Role required: admin

## Register GitLab webhook in ServiceNow instance

Register GitLab in ServiceNow to notify the ServiceNow app when certain events occur in GitLab.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **GitLab Webhooks** &gt; **GitLab Webhook Registries**.

2.  To retrieve the existing webhooks GitLab account, click **Get All Webhooks**.

3.  To create a webhook, click **New**.

4.  On the form, fill in the fields:

    |Fields|Description|
    |------|-----------|
    |Name|Name of the webhook. For example, `Job webhook`.|
    |Description|Description of the record.|
    |Project ID|Unique identifier of the project for which the webhook should be created.|
    |Trigger and SSL|Events in the projects you want to subscribe to. When one of these events occurs, the webhook is triggered.|

5.  Click the **Generate Secret Token** related link.

    The secret token is generated and displayed. Also, the date on which the secret expires is populated in **Secret Expires**.

    **Note:** The secret is regenerated and updated every 30 days. This secret is also updated in GitLab.

6.  Right-click the form header and click **Save**.

7.  Click **Create Webhook**.

    The webhook is created in GitLab and its ID is populated in **Webhook ID**.


### What to do next

To update details of the webhooks or change the subscribed events, click **Update Webhook**.

## Customize a bi-directional webhook in the GitLab spoke

Create webhook routing policy and subflow as per your requirement in the GitLab spoke.

### Before you begin

Role required: admin

### About this task

The default routing policy in the GitLab WebHook Routing Policies modules triggers the relevant GitLab subflow and notifies the ServiceNow app when certain events occur in GitLab. To use any other fields in your custom subflow and customize conditions in the routing policy, perform these steps.

### Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click **Subflows**.

3.  Create a copy of the required subflow.

4.  Customize the required subflow as per your requirement and publish it.

    See [Building subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/subflows.md) for more information about creating and using subflows and [GitLab spoke](../concept/gitlab-spoke.md) for information about the GitLab fields that the default routing policy supports and the GitLab events that the subflows support.

5.  Navigate to **All** &gt; **GitLab Webhooks** &gt; **GitLab Webhook Routing Policies**.

    Five routing policies are available along with the spoke. You can configure them as per your requirement or create a routing policy.

6.  To create a routing policy, click **New**.

7.  On the form, fill in the fields.

<table id="table_iqz_j5s_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label to identify the routing policy.

</td></tr><tr><td>

Default answer

</td><td>

Option to specify if this is the default answer. Default answer is applicable when the conditions are not met. 1.  Click the Lookup icon.
2.  Select the required subflow from the **Document:** list.

**Note:** Ensure that the **Table name** is `Flow [sys_hub_flow]`.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the required events occur in GitLab.

</td></tr><tr><td>

Answer

</td><td>

Subflow that has to be triggered when the specified conditions are met.

</td></tr></tbody>
</table>8.  Click **Submit**.

    **Note:** These routing policies are saved in the Decision tables. Users are cautioned against directly updating or modifying data in these tables.


### Result

Routing policy and subflow are created.

