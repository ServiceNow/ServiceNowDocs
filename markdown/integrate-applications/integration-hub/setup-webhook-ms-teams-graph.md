---
title: Set up a bi-directional webhook for the Microsoft Teams Graph spoke
description: Configure a webhook to subscribe to Microsoft Teams with a ServiceNow callback URL.Register Microsoft Teams in your ServiceNow instance to notify the ServiceNow app when certain events occur in Microsoft Teams.Create a webhook subscription for the required channel in a team by testing the Subscribe Webhook subflow.Customize the required subflow that is shipped along with the spoke by creating a copy of it.Create webhook routing policy and subflow according to your requirements.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Microsoft Teams Graph Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a bi-directional webhook for the Microsoft Teams Graph spoke

Configure a webhook to subscribe to Microsoft Teams with a ServiceNow callback URL.

Demonstrates how to set up bi-directional webhook for the Microsoft Teams Graph spoke. 

## Before you begin

-   Request the required IntegrationHub subscription
-   Activate the Microsoft Teams Graph spoke
-   Role required: admin

## Register a Microsoft Teams Graph webhook in ServiceNow instance

Register Microsoft Teams in your ServiceNow instance to notify the ServiceNow app when certain events occur in Microsoft Teams.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Microsoft Teams Graph Spoke** &gt; **Webhook Registry**.

2.  Click **New**.

3.  On the form, fill in these fields:

    | | |
    |---|---|
    |Name|Name to identify the webhook registry. For example, `MS Teams Graph webhook registry`.|
    |Client State|Client State|
    |Path|Microsoft Teams Graph webhook path. This field is auto-populated to `api/sn_msteams_ahv2/ms_teams_webhook`.|
    |Description|Description of the webhook registry.|

4.  Right-click the form header and click **Save**.

5.  Click **Callback URL**.

    The system auto-populates the webhook callback URL.


## Create webhook subscription for a channel

Create a webhook subscription for the required channel in a team by testing the Subscribe Webhook subflow.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Process Automation** &gt; **Workflow Studio**.

2.  Click **Subflows**.

3.  Open the **Subscribe Webhook** subflow.

4.  Click **Test**.

5.  On the form, fill in these values.

    |Field|Description|
    |-----|-----------|
    |Webhook Registry Record Name|Name of the webhook record you had provided when you [registered the webhook in ServiceNow instance](setup-webhook-ms-teams-graph.md#). For example, `MS Teams Graph webhook registry`.|
    |Change Type|Type of change in the subscribed resource that should send a change notification. The supported values are: `created`, `updated`, and `deleted`. You can provide multiple comma-separated values.|
    |Team ID|Unique identifier of the team.|
    |Channel ID|Unique identifier of the channel.|

    ![Test the Subscribe Webhook subflow for the required change types.](../image/test-subscribe-subflow.png "Test the Subscribe Webhook subflow")

6.  Click **Run Test**.

    Subscription for the required channel is created.

    See Building subflows for more information about testing subflows.


## Customize a spoke subflow

Customize the required subflow that is shipped along with the spoke by creating a copy of it.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Process Automation** &gt; **Workflow Studio**.

2.  Click **Subflows**.

3.  Open the required subflow that is shipped along with the Microsoft Teams Graph spoke.

    For example, **Process Inbound Notifications** subflow.

4.  Click the more actions icon \(![More actions menu](../../integrationhub/images/more-actions-menu-icon.png)\) and select **Copy subflow**.

5.  In **New flow name**, enter a unique name you want the copied subflow to have.

    For example, **Copy of Process Inbound Notifications** subflow.

6.  Click **Copy**.

    A copy of the subflow is created.

7.  Customize the subflow according to your requirement and publish it.

    See Building subflows for more information about creating and using subflows.


## Configure Microsoft Teams Graph webhook decision policy

Create webhook routing policy and subflow according to your requirements.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Microsoft Teams Graph Spoke** &gt; **Webhook Decision Policy**

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ht1_kr2_4qb"><thead><tr><th>

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

Subflow that should be triggered when the conditions are met.

 1.  Click the Lookup icon.
2.  Select the required subflow from the **Document**: list. For example, **Copy of Process Inbound Notifications**.


</td></tr><tr><td>

Default Answer

</td><td>

Option to specify if this answer is the default answer. Default answer is applicable when the conditions are not met.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the incoming webhook delivers data from Microsoft Teams.

</td></tr></tbody>
</table>4.  Click **Submit**.

    **Note:** These routing policies are saved in the Decision tables. Users are cautioned against directly updating or modifying data in these tables.


