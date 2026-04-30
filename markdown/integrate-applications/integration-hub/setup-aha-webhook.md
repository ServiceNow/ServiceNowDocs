---
title: Set up a bi-directional webhook for the Aha! spoke
description: Configure a webhook to subscribe to events in the Aha! account with a ServiceNow callback URL.Create a token that will be embedded in the callback URL to Aha!.Register an Aha! webhook in to notify the app when certain events occur in Aha!.Register the webhook callback URL to the Aha! account.Create a webhook routing policy and subflow as per your requirement.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-06-12"
reading_time_minutes: 3
breadcrumb: [Aha! Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up a bi-directional webhook for the Aha! spoke

Configure a webhook to subscribe to events in the Aha! account with a ServiceNow callback URL.

## Before you begin

Role required: admin

## Procedure

1.  Generate the webhook callback URL from your ServiceNow instance.

    1.  Log in to your ServiceNow instance as an admin.

    2.  Navigate to **Aha! Spoke** &gt; **Webhook** &gt; **Webhook Registries**.

    3.  Open the record **Aha Webhook**.

    4.  Click **Callback URL**.

        Webhook callback URL is generated and displayed.

        ![Webhook callback URL.](../../../product/software-asset-management2/image/aha-webhoook-registry.png)

    5.  Copy and record the webhook callback URL.

2.  Specify the webhook routing policies in your ServiceNow instance.

    1.  Log in to your ServiceNow instance as an admin.

    2.  Navigate to **Aha! Spoke** &gt; **Webhook** &gt; **Webhook Routing Policies**.

    3.  Open the Aha! webhook routing policy record.

    4.  Specify **Condition** that must be met.

    5.  For **Answer**, select the required subflow that must be triggered when the specified condition is met.

        In the default routing policy record, the Process Aha webhooks subflow is selected as **Answer**.

    6.  Click **Update**.

3.  Register the webhook callback URL in Aha! account.

    1.  Log in to your Aha! account as an admin.

    2.  Navigate to **Settings** &gt; **Account**.

    3.  Create an activity webhook by clicking **+** beside **Integrations**.

    4.  Click **+ Activity webhook** in the **Activity webhook** tile.

    5.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Hook URL|Webhook callback URL you had copied from the ServiceNow instance.|
        |Selected Activities|Activities or events for which you want to subscribe.|

    6.  Click **Add activity**.


## Create a Token

Create a token that will be embedded in the callback URL to Aha!.

### Before you begin

Role required: admin

### Procedure

1.  In the navigation filter, enter `token_verification.list`.

    The system displays records in the Token Verifications table.

2.  Select **New**.

3.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Option to provide a unique name to identify the token. For example, `Aha! Callback URL token`.|
    |Description|Option to provide a description of the token.|
    |Token|Option to provide a unique authentication token. This token is encrypted and embedded in the URL.|

4.  Select **Submit**.


## Create an Aha! Webhook in ServiceNow

Register an Aha! webhook in to notify the app when certain events occur in Aha!.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Aha! Spoke** &gt; **Webhook** &gt; **Webhook Registries.**

2.  Select **New**.

3.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Name|Option to uniquely identify the record.|
    |Path|Option to provide the webhook path. Enter `api/sn_aha_spoke/aha_webhook`.|
    |Token|Option to specify the token you had created. See [Create a Token](setup-aha-webhook.md#).|

4.  Right-click the form header and click **Save**.

5.  Select **Callback URL**.

    The system displays the webhook callback URL.

6.  Copy and record the webhook callback URL.


## Add callback URL to Aha!

Register the webhook callback URL to the Aha! account.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your Aha! account as an admin.

2.  Navigate to **Settings** &gt; **Account**.

3.  Create an activity webhook by clicking **+** beside **Integrations**.

4.  Click **+ Activity webhook** in the **Activity webhook** tile.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Hook URL|Webhook callback URL you had copied from the ServiceNow instance.|
    |Selected Activities|Activities or events for which you want to subscribe.|

6.  Click **Add activity**.


## Set webhook routing policy

Create a webhook routing policy and subflow as per your requirement.

### Before you begin

Role required: admin

### About this task

The default routing policy in the Aha Webhook Decision Policy module triggers the Process Aha webhooks subflow and notifies the ServiceNow app when certain events occur in Aha!. See [Aha! Spoke](../concept/aha-spoke.md) for information about the fields that the default routing policy and subflows support. To use any other fields in your custom subflow and customize conditions in the routing policy, perform these steps.

### Procedure

1.  Navigate to **All** &gt; **Aha! Spoke** &gt; **Webhook** &gt; **Webhook Routing Policies.**

2.  Select **New**.

3.  Fill the form.

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

Option to specify if this is the default answer. The default answer is applicable when the conditions are not met.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the required events occur in Aha!.

</td></tr><tr><td>

Answer

</td><td>

Subflow that must be triggered when the specified conditions are met.1.  Click the lookup icon \(![Lookup icon](../image/lookup-icon.png)\).
2.  Select the required subflow from the **Document** list.

**Note:** Ensure that the **Table name** is `Flow [sys_hub_flow]`.

</td></tr></tbody>
</table>4.  Select **Submit**.


