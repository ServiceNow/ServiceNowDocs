---
title: Create an action for an 'on Resource Limit exceeded' policy
description: Set the on Resource limits exceeded policy to automatically run approval workflows or send notifications when an order form is submitted for a template-based catalog item that exceeds the defined resource limit or quota values.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a cloud policy, Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create an action for an 'on Resource Limit exceeded' policy

Set the **on Resource limits exceeded** policy to automatically run approval workflows or send notifications when an order form is submitted for a template-based catalog item that exceeds the defined resource limit or quota values.

## Before you begin

You must have configured the following items:

-   One or more cloud policy groups
-   A cloud policy
-   An approval policy
-   An email notification
-   A workflow using the [Workflow editor](https://www.servicenow.com/docs/access?context=workflow-editor&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)

Role required: sn\_cmp.cloud\_governor or cloud\_admin

## About this task

The **On resource limit exceeded** base system policy action has a default ServiceNow approval policy rule configured by default. If you want to trigger other actions such as notifications or a custom approval workflow when the resource limit is exceeded, you can either modify the base system policy action or create a custom policy for your instance.

## Procedure

1.  Modify or create a cloud policy action to use the **on Resource limit exceeded** trigger.

    1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

    2.  Modify a base system policy or create a new policy record.

    -   1.  Open the base system **Resource Order Control** policy.
2.  Modify the policy name, start, and end dates and order of execution.
3.  Modify the policy rules conditions.
    -   Click **New** to create a new policy record.

        For more information, see [Create a cloud policy](create-cloud-policy.md).

2.  In the Rules related list, modify the base system rule or create a new rule.

    -   Open the base system **approveresourcelimit** rule that should perform the action and customize it.
    -   Create a policy rule.

        For more information, see [Configure a cloud policy rule](configure-cloud-policy-rule.md).

3.  Specify a policy action.

    1.  In the Policy Rule Actions related list, click **New**.

    2.  Click **Create** next to the action you want to occur when the quota is exceeded.

<table id="choicetable_xpc_mhp_znb"><thead><tr><th align="left" id="d313716e240">

Option

</th><th align="left" id="d313716e243">

Steps

</th></tr></thead><tbody><tr><td id="d313716e249">

**Initiate a base system ServiceNow approval workflow.**

</td><td>

1.  Enter a unique name for the action in the **Action Name** field.
2.  Select the **Manager Approval** option to automatically send the request for manager's approval.
3.  Select the **Assignment group** to which this action applies.


</td></tr><tr><td id="d313716e282">

**Initiate a custom approval workflow.**

</td><td>

1.  Enter a unique name for the action in the **Action Name** field.
2.  Select an existing custom workflow in the **Workflow** field.


</td></tr><tr><td id="d313716e306">

**Send an email notification to the catalog item requester and the manager.**

</td><td>

1.  Enter a unique name for the action in the **Action Name** field.
2.  Select a notification template in the **Notification** field.

The base system notification email for the 'on Resource Limit exceeded' policy action appears in the lookup table if you're using the base system policy.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Create a cloud policy](create-cloud-policy.md)

