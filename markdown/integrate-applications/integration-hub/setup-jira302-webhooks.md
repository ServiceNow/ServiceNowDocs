---
title: Set up a bi-directional webhook for the Jira spoke
description: Configure a webhook to subscribe to Jira with a ServiceNow callback URL.Create a token to embed in the Jira webhook URL.Register a Jira webhook in ServiceNow to notify the ServiceNow app when certain events occur in Jira.Provide a webhook callback URL in yourJira Atlassian account to create a webhook.Create a webhook routing policy and subflow as per your requirement.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Jira Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a bi-directional webhook for the Jira spoke

Configure a webhook to subscribe to Jira with a ServiceNow callback URL.

## Before you begin

-   Request an Integration Hub subscription
-   Activate the Jira spoke
-   Role required: admin

## Create a token

Create a token to embed in the Jira webhook URL.

### Before you begin

Role required: admin

### Procedure

1.  In the navigation filter, enter `token_verification.list`.

    The system displays records in the Token Verifications table.

2.  Click **New**.

3.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the token. For example, `Jira token`.|
    |Description|Description of the token.|
    |Token|Authentication token. This token is used to authenticate incoming webhook requests.|


### Result

The token created is used to authenticate incoming webhook requests.

## Register a Jira webhook in ServiceNow

Register a Jira webhook in ServiceNow to notify the ServiceNow app when certain events occur in Jira.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Jira Webhooks** &gt; **Jira Webhook Registries**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the record. For example, `Jira webhook`.|
    |Description|Description of the record.|
    |Token|Authentication token. This token is used to authenticate incoming webhook requests.|
    |Path|Jira webhook path. By default, this path is set to `api/sn_jira_spoke/jira_webhook_callbacks/wh_entry`.|

4.  Right-click the form header and click **Save**.

5.  Choose how you want to authenticate callback requests and select one of the either options.

    |Callback URL Type|Description|
    |-----------------|-----------|
    |Token-based Callback URL|Uses a static token in the URL for simple authentication.|
    |HMAC-based Callback URL|Uses Hash-based Message Authentication Code \(HMAC\) for enhanced security and tamper-proof authentication.|

    The system displays either the token‑based callback URL or the HMAC‑based callback URL based on your selection.

6.  Copy and record the webhook callback URL.


### Result

The Jira webhook is registered in your ServiceNow instance.

## Add a callback URL in Jira

Provide a webhook callback URL in yourJira Atlassian account to create a webhook.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your Jira Atlassian account.

2.  Create a webhook in your Atlassian account.

3.  Enter the webhook callback URL in the **URL** field.

    See the [Atlassian Developer](https://developer.atlassian.com/docs/) portal documentation for instructions on creating a webhook.

    **Note:** If you select an HMAC-based callback URL while [registering a webhook](setup-jira302-webhooks.md#), enter the [secret token created](setup-jira302-webhooks.md#) from your ServiceNow instance in the webhook’s **Secret** field.

    ![Jira spoke webhook creation in Jira portal.](../image/jira-spoke-webhook-secret.png)

4.  Select the related events that should trigger the webhook.


### Result

The callback URL is added in your Jira Atlassian account. You can create routing policies and subflows as per your requirement. See [Customize a bi-directional webhook](setup-jira302-webhooks.md#) for information regarding the creation of new routing policies and subflows.

## Customize a bi-directional webhook

Create a webhook routing policy and subflow as per your requirement.

### Before you begin

Role required: admin

### About this task

The default routing policy in the Jira WebHook Routing Policies module triggers the Process Jira Webhooks subflow and notifies the ServiceNow app when certain events occur in Jira. See [Jira Spoke](../concept/jira-spoke-v3-0-2.md) for information about the fields that the default routing policy and subflows support. To use any other fields in your custom subflow and customize conditions in the routing policy, perform these steps.

### Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click **Subflows**.

3.  Create a copy of the default subflow, Process Jira Webhooks.

4.  Customize the subflow as per your requirement and publish it. See [Building subflows](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US) for more information about creating and using subflows and [Jira Spoke](../concept/jira-spoke-v3-0-2.md) for information about the fields that the default routing policy and subflows support.

5.  Navigate to **Jira Webhooks** &gt; **Jira WebHook Routing Policies**.

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

Conditions to be met when the required events occur in Jira. See [Jira webhooks](../concept/jira-spoke-v3-0-2.md) for information about the supported fields.

</td></tr><tr><td>

Answer

</td><td>

Subflow that must be triggered when the specified conditions are met.

</td></tr></tbody>
</table>8.  Click **Submit**.

    **Note:** These routing policies are saved in the Decision tables. Users are cautioned against directly updating or modifying data in these tables.


### Result

The routing policy and subflow are created.

