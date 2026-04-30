---
title: Work on a deposit task for fulfillment
description: Work on a deposit task to perform a fulfillment activity for the parent deposit service case.
locale: en-US
release: yokohama
product: Financial Services Deposit Operations
classification: financial-services-deposit-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Financial Services Deposit Operations, Deposit Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Work on a deposit task for fulfillment

Work on a deposit task to perform a fulfillment activity for the parent deposit service case.

## Before you begin

Role required:

-   For a business deposit service task: sn\_bom\_deposit\_b2b.agent or sn\_bom\_deposit\_b2b.agent\_connector
-   For a personal deposit service task: sn\_bom\_deposit\_b2c.agent or sn\_bom\_deposit\_b2c.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

A deposit workflow automatically generates deposit tasks for the following activities in a deposit case:

-   Verify operating instructions for a standing order
-   Authorize a deposit request
-   Update a deposit account to fulfill and close the deposit request
-   Create and activate account for account origination
-   Send account opening kit to the customer for account origination
-   Delink an account from other financial accounts during account closure

**Note:** Depending on the deposit service type, the number of activities and deposit tasks may differ in a playbook.

Tasks in the playbook activities are also available in the **Tasks** tab of the case.

If assignment rules are configured, the task is automatically assigned to a deposit agent. The deposit agent can use the case playbook or the task form to work on a deposit task.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon.](../../fso-card-operations/image/list-icon.png)\).

3.  Open the task from the case playbook or the deposit task list.

<table id="choicetable_z4t_j3h_gmb"><thead><tr><th align="left" id="d66405e145">

Option

</th><th align="left" id="d66405e148">

Steps

</th></tr></thead><tbody><tr><td id="d66405e154">

**From the case playbook**

</td><td>

1.  In the **Lists** tab, under **Deposit service cases**, open the case list.
2.  Select the case that contains the deposit task.
3.  Select the **Playbook** tab.
4.  Under the playbook stages, select the task activity to work on.


</td></tr><tr><td id="d66405e187">

**From the Deposit task list**

</td><td>

1.  In the **Lists** tab, under **Deposit tasks**, open the task list.
    -   For your assigned tasks, click **Assigned to me**.
    -   For all deposit tasks, click **All**.
2.  In the list, select the task that you want to work on.


</td></tr></tbody>
</table>4.  To work on a task that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.

5.  Finish the work that is required to complete the deposit task in your core banking system.

6.  In the **Work notes** field, enter any comments.

7.  Close the deposit task.

<table id="choicetable_jcl_dyr_hsb"><thead><tr><th align="left" id="d66405e259">

Deposit task

</th><th align="left" id="d66405e262">

Action

</th></tr></thead><tbody><tr><td id="d66405e268">

**To verify operating instructions for a standing order**

</td><td>

Click **Approve** to approve or **Reject** to reject the request.

</td></tr><tr><td id="d66405e283">

**To authorize a deposit request**

</td><td>

Click **Approve** to approve or **Reject** to reject the request.**Note:** You can't authorize a deposit task if its parent deposit case is assigned to you.

</td></tr><tr><td id="d66405e301">

**-   To update a deposit account to fulfill and close the request
-   To create and activate account for account origination
-   To send account opening kit to the customer
-   To delink an account from other financial accounts during account closure
**

</td><td>

-   In case playbook, click **Mark complete** to close the task.
-   In task form, click **Close** to close the task.


</td></tr></tbody>
</table>
## Result

The deposit task moves to the Closed Complete state.

**Parent Topic:**[Using Financial Services Deposit Operations](../concept/using-deposit-ops.md)

