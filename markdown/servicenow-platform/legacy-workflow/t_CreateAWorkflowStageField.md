---
title: Create a workflow stage field
description: Workflows can provide a summary of workflow progress by updating any field of the Workflow type. If the field is a workflow field, it displays an icon to indicate the workflow stage progress.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workflow stages, Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a workflow stage field

Workflows can provide a summary of workflow progress by updating any field of the **Workflow** type. If the field is a workflow field, it displays an icon to indicate the workflow stage progress.

## Before you begin

Role required: admin

## About this task

In a form, the workflow field displays the current stage as a choice list value.

In a list, the workflow field displays stage icons that represent the series of states, stages, phases, or tasks within a workflow. The stage icons are populated using the activity stages from the associated workflow. For more information, see [Workflow stages](../../using-workflows/concept/c_WorkflowStages.md).

![Workflow stage field in a list](../image/400pxWorkflowList.png)

To create a workflow stage field:

## Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Default Stages \(by table\)**.

2.  Right-click near a column header and select **Configure** &gt; **List Layout**.

3.  Create a new field in lower right.

4.  On the form view of the table used by the workflow, create a field with the **Type** set to **Workflow**.

    For detailed steps, see [Add and customize a field in a table](https://www.servicenow.com/docs/access?context=t_CreatingNewFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

5.  Click **Save**.

6.  Right-click the field label and select **Configure Dictionary**.

7.  Open a dictionary entry.

8.  In the Choice List Specification section of the Dictionary Entries form, select **Dropdown with --None--** from the **Choice** list.

9.  Click **Update**.

10. To ensure that the workflow field properly displays stages on the form, define a choice for each workflow stage.

    -   To create workflow stages using a choice list that already has choices, you can import the stages from the choice list. A stage is created for each choice defined for the **Stage field** selected in the workflow properties. For detailed steps about importing a choice list, see [Import stages from a choice list](../../using-workflows/concept/c_WorkflowStageSets.md#).
    -   The **Value** of each choice must match the **Value** of the corresponding workflow stage.
    -   Do not use spaces in the **Value** field for either choices or stages. Use underscores in place of spaces.
    -   Make the choice list read-only. If a user changes the stage value for a record from the choice list rather than allowing the workflow to control the value, the workflow-driven, legacy, and linear renders may not work as intended. You can also use business rules or events to ensure the workflow progresses accordingly.
    For detailed steps on defining choice lists, see [Define an option for a choice list](https://www.servicenow.com/docs/access?context=t_ViewChoiceListDefinitions&version=australia&pubname=australia-platform-administration&section=t_DefineAnOptionForAChoiceList&ft:locale=en-US).

11. To see workflow stages as icons, add the field to the list layout of the workflow table.

    For detailed steps, see [Configure the list layout](https://www.servicenow.com/docs/access?context=t_ConfigureTheListLayout&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


## What to do next

After you create or update the workflow field:

-   Unless the workflow uses the Requested Item \[sc\_req\_item\] table, ensure that the workflow field is selected from the **Stage field** list in the workflow properties. For detailed steps, see [Select a stage field](t_SelectAStageField.md). If a workflow uses the Requested Item table, the stage field is automatically set to the **Stage** field of the table and cannot be changed.
-   Work through the workflow. Any other updates made to the workflow field, such as updates from business rules or other scripts, can interfere with displaying workflow stages.

-   **[Select a stage field](t_SelectAStageField.md)**  
A **Stage field** allows the workflow context to show additional workflow information, such as the stage name and the estimated completion time for an activity.
-   **[Display approvers in workflow stage fields](display-approvers-workflow-stages.md)**  
Enable workflow stage fields to display approvers, change the number of approvers to display, or disable displaying approvers.
-   **[Workflow stage field icons and tooltips](../reference/r_WorkflowFieldIcons.md#)**  
A workflow stage field displays icons to indicate the workflow stage.
-   **[Workflow stage renderers](../reference/r_WorkflowStageRenderers.md#)**  
Workflow stage renderers determine how a workflow displays stages in a workflow field.

**Parent Topic:**[Workflow stages](../../using-workflows/concept/c_WorkflowStages.md)

