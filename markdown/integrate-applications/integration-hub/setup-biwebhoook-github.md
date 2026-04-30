---
title: Set up bi-directional webhook for the GitHub spoke
description: Configure webhook to subscribe to GitHub with a ServiceNow callback URL.Register a GitHub in ServiceNow to notify the ServiceNow app when certain events occur in GitHub.Provide Webhook Callback URL in GitHub account to create webhook.Create webhook routing policy and subflow as per your requirement in the GitHub spoke.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-10-14"
reading_time_minutes: 3
breadcrumb: [GitHub Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up bi-directional webhook for the GitHub spoke

Configure webhook to subscribe to GitHub with a ServiceNow callback URL.

Demonstrates setting up bi-directional webhook for the GitHub spoke. 

## Before you begin

-   Request Integration Hub subscription
-   Activate the GitHub spoke
-   Role required: admin

## Register GitHub webhook in ServiceNow

Register a GitHub in ServiceNow to notify the ServiceNow app when certain events occur in GitHub.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **GitHub Webhooks** &gt; **GitHub Webhook Registries**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the record. For example, `GitHub webhook`.|
    |Description|Description of the record.|

4.  Right-click the form header and click **Save**.

5.  Click **Callback URL**.

    The system displays the **Webhook Callback URL** and **Webhook Secret**.

    ![Values of the generated Webhook Callback URL and Webhook Secret.](../image/github-webhook-url-secret.png)

6.  Copy and record the values of **Webhook Callback URL** and **Webhook Secret**.


### Result

The GitHub webhook is registered in your ServiceNow instance.

## Add Callback URL in GitHub

Provide Webhook Callback URL in GitHub account to create webhook.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your GitHub account.

2.  Navigate to the required repository.

3.  Select **Settings**.

4.  On the left panel, select, **Webhooks**.

5.  Select **Add Webhook**.

6.  Enter Webhook Callback URL in **Payload URL** and Secret in **Secret**.

    See the [GitHub Developer](https://developer.github.com/) documentation for instructions on creating and configuring a webhook.

    **Note:** GitHub spoke supports **application/json** payload. Configure the GitHub webhook accordingly. See the [GitHub Developer](https://developer.github.com/) documentation for instructions on creating and configuring a webhook.


### Result

The Callback URL is added in the GitHub account. You can create routing policies and subflows as per your requirement. See [Customize a bi-directional webhook](setup-jira302-webhooks.md#) for information regarding creating new routing policies and subflows.

## Customize bi-directional webhook in the GitHub spoke

Create webhook routing policy and subflow as per your requirement in the GitHub spoke.

### Before you begin

Role required: admin

### About this task

The default routing policy in the GitHub WebHook Routing Policies modules triggers the relevant GitHub subflow and notifies the ServiceNow app when certain events occur in GitHub. See [GitHub Spoke](../concept/github-spoke.md) for information about the GitHub fields that the default routing policy supports and the GitHub events that the subflows support. To use any other fields in your custom subflow and customize conditions in the routing policy, perform these steps.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click **Subflows**.

3.  Create a copy of the required subflow.

4.  Customize the required subflow as per your requirement and publish it.

    See [Building subflows](https://www.servicenow.com/docs/access?context=subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) for more information about creating and using subflows and [GitHub Spoke](../concept/github-spoke.md) for information about the GitHub fields that the default routing policy supports and the GitHub events that the subflows support.

5.  Navigate to **GitHub Webhooks** &gt; **GitHub WebHook Routing Policies**.

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

Option to specify if this is the default answer. Default answer is applicable when the conditions are not met.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the required events occur in GitHub. See [GitHub Spoke](../concept/github-spoke.md) for information about the supported fields.

</td></tr><tr><td>

Answer

</td><td>

Subflow that has to be triggered when the specified conditions are met.1.  Click the Lookup icon.
2.  Select the required subflow from the **Document:** list.

**Note:** Ensure that the **Table name** is `Flow [sys_hub_flow]`.

</td></tr></tbody>
</table>8.  Click **Submit**.

    **Note:** These routing policies are saved in the Decision tables. Users are cautioned against directly updating or modifying data in these tables.


### Result

Routing policy and subflow are created.

