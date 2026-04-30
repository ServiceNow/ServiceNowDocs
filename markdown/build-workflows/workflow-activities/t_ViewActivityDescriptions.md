---
title: View workflow activity descriptions
description: Tooltips are available for workflow activities to help you understand how to use each activity.Each activity can specify a number of elements that control the behavior of the activity or are controlled by the activity.
locale: en-US
release: yokohama
product: Workflow Activities
classification: workflow-activities
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow activities, Classic Workflow, Build workflows]
---

# View workflow activity descriptions

Tooltips are available for workflow activities to help you understand how to use each activity.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  To view an activity description in the [Workflow Editor](../../workflow/reference/workflow-editor.md), point to the icon for the activity in the palette.

    ![Viewing activity tooltips in the palette](../../workflow-activities/image/ActivityTooltips.png)

2.  To modify activity descriptions, navigate to **Workflow** &gt; **Administration** &gt; **Activity Definitions** and edit the **Description** field.

    **Note:** To view more information about an activity, double-click the activity on the canvas and then click the help icon in the title bar of the Activity Properties window.


## Elements in workflow activity definitions

Each activity can specify a number of elements that control the behavior of the activity or are controlled by the activity.

Not all activities specify all possible elements. See [Workflow activities](../concept/c_WorkflowActivities.md) for links to the activities provided by default. Each activity description includes a detailed explanation of the specific elements offered by that activity.

<table id="table_e53_zfy_3r"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Results

</td><td>

The possible **activity.results** value. The activity result usually determines which condition the activity transitions through.

</td></tr><tr><td>

Scratchpad entries

</td><td>

Scratchpad variables the activity depends on to run, or variables the activity writes to the scratchpad.

</td></tr><tr><td>

Input variables

</td><td>

Values that control the behavior of the activity. Fields to set these values appear on the Activity Properties form when a new activity is added to a workflow. See [Activity variables](../concept/c_UsingVariablesInAWorkflow.md#) for more information.

</td></tr><tr><td>

Conditions

</td><td>

Determines which transition the activity follows after completing. See [Manage workflow activity conditions](t_ManageActivityConditions.md#) for more information.

</td></tr><tr><td>

States

</td><td>

Determines how the workflow handles the record being executed.

</td></tr></tbody>
</table>