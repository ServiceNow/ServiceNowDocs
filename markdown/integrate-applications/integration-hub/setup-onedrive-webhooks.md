---
title: Set up a bi-directional webhook for the Microsoft OneDrive spoke
description: Configure a webhook to subscribe to OneDrive with a ServiceNow callback URL.Register a OneDrive webhook in ServiceNow to notify the ServiceNow app when certain events occur in OneDrive.Create a webhook routing policy and subflow according to your requirement.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft OneDrive Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a bi-directional webhook for the Microsoft OneDrive spoke

Configure a webhook to subscribe to OneDrive with a ServiceNow callback URL.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft OneDrive spoke.
-   Role required: admin.

## Register a OneDrive webhook in ServiceNow

Register a OneDrive webhook in ServiceNow to notify the ServiceNow app when certain events occur in OneDrive.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Microsoft OneDrive Spoke** &gt; **OneDrive Webhook Registries**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_rzb_htl_fpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name to identify the record. For example, `OneDrive webhook`.

</td></tr><tr><td>

Description

</td><td>

Description of the record.

</td></tr><tr><td>

Path

</td><td>

OneDrive path. By default, this path is set to `api/sn_onedrive_spoke/onedrive/subscription`

</td></tr><tr><td>

Secret Key

</td><td>

Secret key for accessing OneDrive webhook. **Note:** The **Secret Key** field value is auto-populated when the webhook registry record is saved.

</td></tr></tbody>
</table>4.  Right-click the form header and click **Save**.

5.  Click **CallBack URL**.

    The system displays the webhook callback URL.

6.  Copy and record the webhook callback URL.


## Customize OneDrive bi-directional webhook

Create a webhook routing policy and subflow according to your requirement.

### Before you begin

Role required: admin

### About this task

Routing policies in the OneDrive Webhook Routing Policy module triggers the subflows and notifies the ServiceNow instance when certain events occur in your OneDrive account. See OneDrive spoke for information about the fields that the routing policy and subflows support.

### Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click **Subflows**.

3.  Create a copy of any of the default subflows, for example, Sync Changes.

4.  Customize the subflow according to your requirement and publish it.

    See Building subflows for more information about creating and using subflows, and [OneDrive spoke v1.6](../concept/onedrive-spoke.md) for information about the supported subflows.

5.  Navigate to **Microsoft OneDrive Spoke** &gt; **OneDrive Webhook Routing Policy**.

6.  Click **New**.

7.  On the form, fill in the fields.

<table id="table_yvd_g5r_fpb"><thead><tr><th>

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

**Note:** Ensure that the Table name is `Flow [sys_hub_flow]`.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the required events occur in OneDrive.

</td></tr><tr><td>

Answer

</td><td>

Subflow which is triggered when the specified conditions are met.

</td></tr></tbody>
</table>8.  Click **Submit**.


### Result

The routing policy and subflow are created.

