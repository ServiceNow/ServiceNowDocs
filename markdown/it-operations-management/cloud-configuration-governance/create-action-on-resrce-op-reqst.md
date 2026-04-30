---
title: Create an action for an 'on Resource operation request start/end' policy
description: A policy that is triggered by the on Resource operation request start or on Resource operation request end trigger can run a script or override a user-requested attribute value.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a cloud policy, Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create an action for an 'on Resource operation request start/end' policy

A policy that is triggered by the on Resource operation request start or on Resource operation request end trigger can run a script or override a user-requested attribute value.

## Before you begin

-   Role required: sn\_cmp.cloud\_governor or admin
-   Optional: [Create one or more cloud policy groups](create-cloud-policy-group.md).
-   [Configure a cloud policy rule](configure-cloud-policy-rule.md) and associated conditions.

## About this task

-   The on Resource operation request start trigger fires after a user submits a resource operation request \(Start, Stop, Deprovision\).
-   The on Resource operation request end trigger fires before completion of a life cycle operation on a resource \(Start, Stop, Deprovision\).

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Open a cloud policy and set the policy to the **Draft** state if needed.

3.  Open the rule that should perform the action and then click **New** on the Policy Rule Actions related list.

4.  On the popup, click **Create** for the type of action to perform, enter a unique and meaningful **Action Name**, and then fill in the form for the action.

    ![Create Action popup](../image/action-on-cat-item-startstop.png)

<table id="table_nbq_j2h_sfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action Script Category

</td><td>

Select a category.

</td></tr><tr><td>

Action Script Name

</td><td>

Specify a unique and meaningful name for the script.

</td></tr><tr><td>

Action Script

</td><td>

Create the script in the text box.See [Create a policy action script](create-policy-script-1.md) for details.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Action Name|Specify a unique and meaningful name for the action that starts the workflow.|
    |Workflow|Select the workflow to execute.|

    ![Selecting a workflow as the policy action](../image/action-wf-on-cat-item-end.png "Configuring an 'Execute a Workflow' action to run the base-system 'Change Request' workflow")


**Parent Topic:**[Create a cloud policy](create-cloud-policy.md)

