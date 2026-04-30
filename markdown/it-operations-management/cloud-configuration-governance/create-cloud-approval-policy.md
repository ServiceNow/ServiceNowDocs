---
title: Create a cloud approval policy
description: A cloud approval policy specifies the users who must approve a specified cloud activity before the activity can proceed. Approvers can include the manager of the user making a request, a specified user or group, or users with a specified role. You can specify multiple approvers. Approvals occur in the order that you specify.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Policies for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create a cloud approval policy

A cloud approval policy specifies the users who must approve a specified cloud activity before the activity can proceed. Approvers can include the manager of the user making a request, a specified user or group, or users with a specified role. You can specify multiple approvers. Approvals occur in the order that you specify.

## Before you begin

Optional: [Create one or more cloud policy groups](create-cloud-policy-group-1.md).

Role required: sn\_cmp.cloud\_governor or admin

## About this task

In this example, a user requests a stack that triggers an approval policy.

1.  On the Cloud User Portal, a user submits a request to provision a particular blueprint. The process of provisioning the blueprint is the trigger that causes the policy engine to apply an approval policy. A cloud approval policy specifies the users who must approve a specified cloud activity before the activity can proceed.
2.  The policy engine determines that the request meets the condition specified in the rule for the policy. In this example, the condition evaluates to true whenever a particular blueprint is being provisioned.
3.  Because the condition is met, the policy engine performs the action that is also specified in the rule. In this example, the action is to create an approval action for the manager.
4.  While the approver \(the manager\) reviews the approval request, the user sees a "waiting for approval" status message on the Cloud User Portal.
5.  After the manager approves, the blueprint is provisioned.

![User waiting for approval](../image/user-awaiting-approval.png "User waiting for approval")

The targeted approval policies complement application-wide approval.

-   **on Stack operation \(approval\)**: Triggered during any stack operation on the Cloud User Portal.
-   **on Stack resource operation \(approval\)**: Triggered during any resource operation \(start, stop, provision, and so on\) on the Cloud User Portal.
-   **on Task remediation**: Triggered when a user resubmits a failed request.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Policies**.

2.  Click **New** and then fill in the form.

    ![Policies form](../image/approval-policy.png "Example approval policy")

<table id="table_zk1_ctq_fz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy name

</td><td>

Enter a descriptive name that includes the word `Policy`. Do not start the name with a number.

</td></tr><tr><td>

Description

</td><td>

Enter a description of the intent of the policy.

</td></tr><tr><td>

Policy group

</td><td>

Optional: Select a policy group. Each policy in the group is enforced.

</td></tr><tr><td>

Policy trigger

</td><td>

Select a trigger that specifies when the policy should be applied. The following triggers can start approval policies:-   on Blueprint provision \(approval\)
-   on Stack operation \(approval\)
-   on Stack resource operation \(approval\)
-   on Task remediation


</td></tr><tr><td>

Blueprint\[appears when the **on Blueprint provision \(approval\)** or **on Stack operation \(approval\)** trigger is selected\]

</td><td>

Select the blueprint that the policy applies to. -   If no blueprint is specified, then the policy applies for every blueprint. This setting can decrease performance.
-   You can assign multiple policies to a blueprint. Multiple policies running simultaneously, however, might decrease performance. Publish a policy only when it should be enforced.


</td></tr><tr><td>

Operation\[appears when the **on Stack resource operation \(approval\)** trigger is selected\]

 Reviewers: Does this also appear for on Stack operation \(approval\)?

</td><td>

Select the operation that the policy applies to. For example, a policy can apply to the Deprovision operation only or to all operations on the blueprint or catalog item.**Note:** If no operation is specified, then the policy applies for every operation. This condition can decrease performance.

 -   **All**: Any operation executes.
-   **Start**: The resource starts.
-   **Stop**: The resource stops.
-   **Provision**: The resource is provisioned.
-   **Deprovision**: The resource is no longer available to users.
-   **Execute Script**: A script runs on the resource.


</td></tr><tr><td>

Start Date / End Date

</td><td>

Specify the start date when the policy should be enforced and the end date when the policy should no longer be enforced.

</td></tr><tr><td>

Order of Execution

</td><td>

Specify a number that represents the order in which the policy is applied. A policy with a lower number runs before a policy with a higher number. For example, a policy with **Order** of **100** runs before a policy with an **Order** of **200**.

</td></tr><tr><td>

Status

</td><td>

A new policy is in **Draft** state. Click **Publish** on the form header to enforce the policy. After a policy is published, you must set it to the **Draft** state to update it.

</td></tr></tbody>
</table>3.  Right-click in the header and select **Save**.

4.  When you are ready to enforce the policy, click **Publish**.


## What to do next

[Configure one or more cloud policy rules](configure-cloud-policy-rule-1.md).

