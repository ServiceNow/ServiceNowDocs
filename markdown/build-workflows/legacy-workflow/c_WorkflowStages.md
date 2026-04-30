---
title: Workflow stages
description: Workflows can indicate workflow progress by updating any field designated as a stage field.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Workflow management, Classic Workflow, Build workflows]
---

# Workflow stages

Workflows can indicate workflow progress by updating any field designated as a stage field.

For example, the Incident \[incident\] table has an **Incident state** field that indicates progress, but the service catalog uses the **Stage** field.

To indicate the workflow's progress through the possible stage values, the interface updates the **Stage field** selected in the workflow properties. Available fields depend on the table used by the workflow. If the field provides a choice list, then the choices are available as stage values for the workflow. If the field is a workflow field, it displays an icon to indicate the workflow's progress, as with the Service Catalog's **Stage** field.

![](../image/WorkflowFieldIcons.png "Service Catalog Stage field with icons")

After stages are added to the workflow, they can be assigned to each workflow activity. If an activity with an assigned stage is encountered when the workflow runs, the workflow engine assigns the stage to the record associated with the workflow context.

For workflows that use the Requested Item \[sc\_req\_item\] table, the stage field is automatically set to the **Stage** field of the table and cannot be changed. The stage state displayed for a workflow running on the Requested Item table is based on the state of the workflow activities.

-   If an activity is active, then the stage is shown with the state of **In progress**.
-   If an activity is in the **Pending** or **Completed** state, the stage reflects this state.
-   If an activity is canceled, **Request Cancelled** appears in the **Stage** field. The "Cancelled" label set in the wf\_stage table is a reserved word, and does not display in the **Stage** field.

## How stage values are derived

Stage values are derived from various sources in the interface.

**Note:** An updated method for managing workflow stages as a set is also available. For information about grouping and reusing stages, see [Workflow stage sets](c_WorkflowStageSets.md#).

Stage values are derived from the following sources:

-   **Choices for Stage column**: Choices defined for the column selected as the **Stage** column for the workflow.
-   **Default stages for table**: Stages defined in the Stage Default \[wf\_stage\_default\] table for the table selected.
-   **Workflow-specific stages**: Applied only to the workflow for which they were defined in the Workflow Stage \[wf\_stage\] table.
-   **Stage values in existing records**: Values from the designated **Stage** column in the table assigned to the workflow are inherited from existing records.

If the stage field for a workflow is the table column named **Stage**, then the progress of the workflow appears in any list view containing the **Stage** column.

![](../image/StagesInList.png "Stages in a list")

Stage values shown in the list views are accompanied by the state, based on the workflow activities being executed. If an activity has a stage specified for it, and the activity is currently active in the workflow, then the stage is shown with a state of **In progress**. Similarly, if the activity is in the **Pending** or **Completed** state, the stage reflects this state.

## Example

If the workflow table is Request Item \[sc\_req\_item\], then the stage field is automatically set to the **Stage** column of that table and cannot be changed. The following stage values for the request item are displayed in a choice list from the Dictionary Entry \[sys\_dictionary\] table:

-   Waiting for Approval
-   Fulfillment
-   Delivery

In addition, the Request Item table has the following default stages:

-   Request Cancelled
-   Completed

**Note:** If an activity is cancelled, Request Cancelled appears in the **Stage** field. The "Cancelled" label set in the wf\_stage table is a reserved word, and does not display in the **Stage** field.

When you edit available activity stages in the Workflow Editor, the list displays the following stage values:

-   Waiting for Approval
-   Fulfillment
-   Delivery
-   Request Cancelled
-   Completed

The following diagram depicts the process used to gather stage values from the Request Item table to populate the **Stages** list in workflow activities.

![Gathering stage values for workflow activities](../image/ScReqStagesDiagram.png)

**Note:** If you are creating a workflow with a table other than Request Item \[sc\_req\_item\], you must select a **Stage field** in the workflow properties for the workflow to have stages.

-   **[Use workflow stages](../task/t_UsingWorkflowStages.md)**  
You can add or modify workflow stages.
-   **[Add and translate stages](../task/add-translate-stages.md#)**  
You can add default stages to use for a table, and stages to existing workflow
-   **[Workflow stage sets](c_WorkflowStageSets.md#)**  
Stage sets are named groups of workflow stages commonly used together. Create a stage set and assign it as a default set to any number of tables. You can import the choice list values of a workflow field as stages for a workflow, and export a stage set to create a new one.
-   **[Create a workflow stage field](../../workflow-administration/task/t_CreateAWorkflowStageField.md)**  
Workflows can provide a summary of workflow progress by updating any field of the **Workflow** type. If the field is a workflow field, it displays an icon to indicate the workflow stage progress.
-   **[Workflow fields with deleted records](../../workflow-administration/concept/c_WorkflowFieldsWithDeletedRecords.md)**  
Workflow fields may indicate when a record required by the workflow is deleted.

**Parent Topic:**[Workflow management](../../workflow-administration/concept/managing-workflows.md)

