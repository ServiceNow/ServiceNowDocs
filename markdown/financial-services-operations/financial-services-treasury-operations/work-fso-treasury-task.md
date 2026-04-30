---
title: Work on a treasury task for due diligence or fulfilment
description: Work on a treasury task to perform due diligence or fulfilment activities for the parent treasury service case.
locale: en-US
release: xanadu
product: Financial Services Treasury Operations
classification: financial-services-treasury-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Financial Services Treasury Operations, Financial Services Treasury Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a treasury task for due diligence or fulfilment

Work on a treasury task to perform due diligence or fulfilment activities for the parent treasury service case.

## Before you begin

Role required: sn\_bom\_treasury.agent or sn\_bom\_treasury.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

A treasury workflow automatically generates treasury tasks for the following activities in a treasury case:

-   Perform due diligence

    **Note:** This task is generated only for an RDC treasury case.

-   Activate treasury service in core system
-   Send treasury service activation email to the customer
-   Initiate customer training for the treasury service

If assignment rules are configured, the task is automatically assigned to a treasury agent. The treasury agent can use the case playbook or the task form to work on a treasury task.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon.](../../fso-card-operations/image/list-icon.png)\).

3.  Open the task from the case playbook or the treasury task list.

<table id="choicetable_z4t_j3h_gmb"><thead><tr><th align="left" id="d36449e124">

Option

</th><th align="left" id="d36449e127">

Steps

</th></tr></thead><tbody><tr><td id="d36449e133">

**From the case playbook**

</td><td>

1.  In the **Lists** tab, under **Treasury Service Cases**, open the case list.
2.  In the list, select the case that contains the treasury task.
3.  Select the **Playbook** tab.
4.  Under the **Due diligence** or **Fulfilment** stage, select the task activity to work on.

**Note:** The Due diligence activity is available only for an RDC treasury case.

</td></tr><tr><td id="d36449e174">

**From the Treasury task list**

</td><td>

1.  In the **Lists** tab, under **Treasury Tasks**, open the task list.
    -   For your assigned tasks, click **Assigned to me**.
    -   For all treasury tasks, click **All**.
2.  In the list, select the task that you want to work on.


</td></tr></tbody>
</table>4.  To work on a task that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.

5.  Finish the work that is required to complete the treasury task in your core banking system.

6.  In the **Work notes** field, enter any comments.

7.  Close the task from the playbook activity or the treasury task form.

    -   In case playbook, click **Mark complete** to close the task.
    -   In task form, click **Close** to close the task.

## Result

The treasury task moves to the Closed Complete state.

**Parent Topic:**[Using Financial Services Treasury Operations](../concept/using-treasury-ops.md)

