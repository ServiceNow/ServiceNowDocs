---
title: Create an action for an 'approval' policy
description: A policy that is triggered by one of the approval triggers can start approval workflows. The approval triggers are \( on Blueprint provision \(approval\), on Stack operation \(approval\), on Stack resource operation \(approval\), and on Task remediation .
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create a cloud policy, Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create an action for an 'approval' policy

A policy that is triggered by one of the approval triggers can start approval workflows. The approval triggers are \(on Blueprint provision \(approval\), on Stack operation \(approval\), on Stack resource operation \(approval\), and on Task remediation.

## Before you begin

Optional: [Create one or more cloud policy groups](create-cloud-policy-group-1.md).

[Configure a cloud policy rule](configure-cloud-policy-rule-1.md) and associated conditions.

Role required: sn\_cmp.cloud\_governor or admin

## About this task

When multiple "approval" policies apply, the policies are applied in the following order. \(The approval policies are on Blueprint provision \(approval\), on Stack operation \(approval\), on Stack resource operation \(approval\), and on Task remediation\):

1.  Only the first successful approval policy is applied and no other approval policies are applied.
2.  If the applied approval policy has multiple rules, only the first successful rule is used.
3.  If a rule has multiple actions, only the first successful action is performed.
4.  If the applied approval policy includes both a custom approval and a Service Now approval, only the custom approval process is performed.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Open a cloud policy and set the policy to the **Draft** state if needed.

3.  Open the rule that should perform the action and then click **New** on the Policy Rule Actions related list.

4.  On the popup, click **Create** for the type of action to perform.

    ![Create Action popup](../image/create-approval-action-cloud-mgt.png)

5.  Select any of the following actions.

    -   **Custom Approval** runs the workflow that you specify. The workflow should return a value of **approved** to complete the operation. Follow **Service Now Approval** for use case.
    -   **Service Now Approval** supports differing approvers based on the trigger for the policy:

<table id="table_y1w_fz4_31c"><thead><tr><th>

Trigger

</th><th>

Workflow

</th><th>

Available approvers

</th></tr></thead><tbody><tr><td>

on Blueprint provision \(approval\)

</td><td>

Cloud Approval Workflow

</td><td>

-   Manager Approval
-   Assignment Group
-   User \(lock\)


</td></tr><tr><td>

on Stack operation \(approval\)

</td><td>

Cloud Operation Change Request Workflow

</td><td>

Assignment Group

</td></tr><tr><td>

on Stack resource operation \(approval\)

</td><td>

Cloud Operation Change Request Workflow

</td><td>

Assignment Group

</td></tr></tbody>
</table>6.  On the Approval form, specify a unique and meaningful **Action Name**.

    ![Approval policy action](../image/service-now-approval.png "Action in the rule")

7.  If you select **Custom Approval**, specify the workflow and then click **Submit** and if you select **ServiceNow Approval**, specify who should approve the cloud activity.

<table id="table_fdg_nr4_sfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Manager Approval

</td><td>

One or all of the following:-   Select the **Manager Approval** check box to require the manager of the approver to also approve the request. The default approval workflow goes to the manager first, then to the group, and finally to the user.
-   Select a user group from the **Assignment Group** list.
-   Unlock the **User** lock, select a user from the list, then close the lock.


</td></tr><tr><td>

Assignment group

</td><td>

Select the assignment group that can approve the request. Any user in the group can approve the action using the default workflow. The approval then goes to the users in the **User** field.**Note:** Users in an assignment group that do not have the itil role still receive an approval record and notification by default, but they cannot perform the approval. Assign the itil role to any users or user groups that must make operational and provisioning approvals.

</td></tr><tr><td>

User

</td><td>

Select one or more users to whom the approval action applies. All selected users must approve the action using the default workflow.

</td></tr></tbody>
</table>
