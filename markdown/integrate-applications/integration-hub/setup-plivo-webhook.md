---
title: Set up a bi-directional webhook for the Plivo spoke
description: Configure a webhook to subscribe to your Plivo account with a ServiceNow callback URL.Register a Plivo webhook in your ServiceNow instance to notify the ServiceNow app when certain events occur in Plivo.Provide a webhook callback URL in your Plivo account to create a webhook.Create a webhook routing policy and subflow as per your requirement.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Plivo Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a bi-directional webhook for the Plivo spoke

Configure a webhook to subscribe to your Plivo account with a ServiceNow callback URL.

## Before you begin

-   Request Integration Hub subscription.
-   Activate the Plivo spoke.
-   [Set up the Plivo spoke](plivo-setup.md#)
-   Role required: sn\_plivo\_spoke.Plivo\_Admin and decision\_table\_admin.

## Register a Plivo webhook in ServiceNow

Register a Plivo webhook in your ServiceNow instance to notify the ServiceNow app when certain events occur in Plivo.

### Before you begin

Role required: sn\_plivo\_spoke.Plivo\_Admin and decision\_table\_admin

### Procedure

1.  Navigate to **All** &gt; **Plivo Spoke** &gt; **Plivo Webhook Registries**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the record. For example, `Plivo webhook`.|
    |Description|Description of the record.|
    |Path|Plivo webhook path. By default, this path is set to `api/sn_plivo_spoke/plivo_webhook_handler/wh_entry`.|

4.  Right-click the form header and click **Save**.

5.  Click **Callback URL**.

    The system displays the webhook callback URL.

6.  Copy and record the webhook callback URL.


### Result

The Plivo webhook is registered in your ServiceNow instance.

## Add a callback URL in Plivo

Provide a webhook callback URL in your Plivo account to create a webhook.

### Before you begin

Role required: sn\_plivo\_spoke.Plivo\_Admin and decision\_table\_admin

### Procedure

1.  Log in to your Plivo console.

2.  Create an application in the Plivo console as per your requirement.

    For more information about creating an application in the Plivo console, see the Create an Application section in the [Make your first Outbound Call](https://www.plivo.com/docs/voice#make-your-first-outbound-call) page of the [Plivo documentation](https://www.plivo.com/docs/). You can also refer to the [Plivo Application documentation](https://www.plivo.com/docs/account/api/application/) for more information about creating and updating an application using Plivo APIs.

3.  Enter the webhook callback URL in **MESSAGE URL** and **ANSWER URL**, and configure the application as per your requirement.


### Result

The callback URL is added in your Plivo account. You can create routing policies and subflows as per your requirement. See [Create routing policy and customize webhook](setup-plivo-webhook.md#) for information regarding the creation of new routing policies and subflows.

## Create routing policy and customize webhook

Create a webhook routing policy and subflow as per your requirement.

### Before you begin

Role required: sn\_plivo\_spoke.Plivo\_Admin and decision\_table\_admin

### About this task

Routing policy in the Plivo WebHook Routing Policy module triggers the subflows and notifies the ServiceNow instance when certain events occur in your Plivo account. See [Plivo Spoke](../concept/plivo-spoke.md) for information about the fields that the routing policy and subflows support.

### Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click **Subflows**.

3.  Create a copy of the default subflow.

    Two subflows are available along with Plivo spoke; Plivo Call Handler and Plivo SMS Handler. You can create a copy of either of these subflows as per your requirement.

4.  Customize the subflow as per your requirement and publish it.

    See [Building subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/subflows.md) for more information about creating and using subflows, and [Plivo Spoke](../concept/plivo-spoke.md) for information about the supported fields.

5.  Navigate to **Plivo Spoke** &gt; **Plivo WebHook Routing Policy**.

6.  Click **New**.

7.  On the form, fill in the fields.

<table id="table_awj_xgv_z3b"><thead><tr><th>

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

Option to specify if this is the default answer. The default answer is applicable when the conditions are not met.1.  Click the lookup icon \(![Lookup icon](../image/lookup-icon.png)\).
2.  Select the required subflow from the Document list.

**Note:** Ensure that the **Table name** is `Flow [sys_hub_flow]`.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the required events occur in Plivo.

</td></tr><tr><td>

Answer

</td><td>

Subflow that must be triggered when the specified conditions are met.

</td></tr></tbody>
</table>    Routing policies and subflows support these Plivo fields:

    -   Keywords
    -   Call Event
    -   Caller Name
    -   Event Type
    -   SMS Text
    -   To Number
    -   Show Related Fields
8.  Click **Submit**.

    **Note:** These routing policies are saved in the Decision tables. Users are cautioned against directly updating or modifying data in these tables.


### Result

The routing policy and subflow are created.

