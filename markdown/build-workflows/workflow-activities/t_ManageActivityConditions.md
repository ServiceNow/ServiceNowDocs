---
title: Manage workflow activity conditions
description: Activities contain default conditions that determine which transitions are followed.The result value specified by an activity controls the condition through which the activity transitions.
locale: en-US
release: yokohama
product: Workflow Activities
classification: workflow-activities
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow activities, Classic Workflow, Build workflows]
---

# Manage workflow activity conditions

Activities contain default conditions that determine which transitions are followed.

## Before you begin

Role required: admin

## About this task

For example, the **Approval - User** activity has two conditions, **Approved** and **Rejected**.

![](../../workflow-activities/image/WFActivityConditions.png "Example of activity conditions")

You can use a JavaScript condition check to create custom conditions on Core workflow activities. Custom activities do not support this feature.

## Procedure

1.  Right-click the activity and select **Add Condition** from the context menu.

2.  In the New Workflow Condition dialog box, fill in the fields as appropriate \(see table\).

<table id="table_idk_3yx_3r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The label that is displayed on the workflow.

</td></tr><tr><td>

Activity

</td><td>

Name of the activity for which this condition is submitted. This value is populated automatically by the system.

</td></tr><tr><td>

Short description

</td><td>

Brief description of this condition.

</td></tr><tr><td>

Condition

</td><td>

A JavaScript condition check. The following variables are available: -   **current**: Current record that the workflow is running against.
-   **activity.result**: Result value set by the activity upon completion.
-   **activity**: Workflow Executing Activity \(wf\_executing\) record. Used for advanced condition checks.
-   **activity.vars**: Variables associated with the Workflow Executing Activity record. Used for advanced condition checks.


</td></tr><tr><td>

Skip during generate

</td><td>

If selected, the [**Generate** activity](https://www.servicenow.com/docs/access?context=r_Generate&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) does not follow this transition to generate approvals or tasks.

</td></tr></tbody>
</table>3.  Click **Submit**.

4.  To change the order in which conditions appear on the workflow activity, right-click the activity and select **Reorder Conditions**.

    A dialog box appears, with a list of the available conditions.

    ![](../image/WorkflowReorderConditions.png "List of conditions in the current activity")

5.  Drag the conditions to a new position in the list.

6.  Click **OK**.


## Activity result value

The `result` value specified by an activity controls the condition through which the activity transitions.

Use the `result` value as part of the **Condition** field in the activity. For example, if the **Condition** field of an **Approval - User** activity contains `activity.result == 'rejected'`, the activity transitions through that condition when a rejection is received from the approver. Result values are set in the **Script** field of the activity definition.

