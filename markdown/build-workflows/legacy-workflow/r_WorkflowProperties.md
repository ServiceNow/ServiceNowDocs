---
title: Workflow properties
description: In the properties of a workflow, you can configure settings such as its application scope, start conditions, schedule, inputs, stages, and run time metrics. You can also view information such as the workflow author, version, and history.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Create a workflow, Workflow management, Classic Workflow, Build workflows]
---

# Workflow properties

In the properties of a workflow, you can configure settings such as its application scope, start conditions, schedule, inputs, stages, and run time metrics. You can also view information such as the workflow author, version, and history.

When you create a new workflow, the following fields are available in the dialog box:

-   **Name**
-   **Table**
-   **Description**
-   **If condition matches**
-   **Condition**

If you click **Diagrammer view**, in **Related Lists**, the following UI sections are available in the dialog box:

-   General
-   Conditions
-   Inputs
-   Activities
-   Application
-   Schedule
-   Stages
-   Estimated Runtime

## General

<table id="table_GeneralWorkflowTab"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A name to identify the workflow.

</td></tr><tr><td>

Table

</td><td>

The table for the workflow to run on. Workflows that run on specific tables can still interact with other tables. Select **Global \[global\]** to run the workflow on all tables. **Note:** The list shows only tables and database views that are in the same scope as the workflow. Also, all users who edit the workflow must have access to the necessary tables and domains.

</td></tr><tr><td>

Checked out

</td><td>

\[Read-only\] When the workflow was checked out. Automatically set by the **Checkout** action in the workflow menu.

</td></tr><tr><td>

Checked out by

</td><td>

\[Read-only\] The user who has this workflow checked out. This value is automatically set by the **Checkout** action in the workflow menu.

</td></tr><tr><td>

Published

</td><td>

\[Read-only\] Check box to indicate whether the workflow has been published. Automatically set by the **Publish** action in the workflow menu.

</td></tr><tr><td>

Description

</td><td>

The purpose of the workflow.

</td></tr></tbody>
</table>## Conditions

Create conditions to trigger the workflow. The Conditions section does not appear if you select a table, such as sc\_req\_item, that does not require a condition.

<table id="table_WorkflowTab"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

If condition matches

</td><td>

When the condition evaluates to true, the workflow launches an active context:

-   **None**: The workflow is not automatically started by the workflow engine. To run this workflow, write a script to start the workflow.
-   **Run the Workflow**: The default value. The workflow engine starts the workflow if the information in the **Condition** field matches a record that is inserting into the table.
-   **Run if no other workflows match yet \(deprecated\)**: The workflow only runs if no other workflows are running on the execution thread that started this workflow. Avoid using.
-   **Run if no other workflows matched**: The workflow only runs if no other workflows are running on a specific record. For example, there are four workflows inserted into the Incident table, which have a condition such as **short\_desc** contains **test**. A new workflow, which has **If condition matches** is set to **Run if no other workflows match yet**, only runs if none of the four workflows have started running on the Incident record.

</td></tr><tr><td>

Condition

</td><td>

A condition builder for specifying workflow conditions that trigger the behavior selected from the If condition matches list.

</td></tr><tr><td>

Order

</td><td>

Numeric value that determines the order of the workflow, relative to other workflows. Workflows are evaluated in order from the lowest order number to the highest. A workflow runs if it is the first to match conditions.

</td></tr></tbody>
</table>## Inputs

The Inputs section lists all the activities in the current workflow that input data, the data type, and the default value. The Inputs section is only available after a workflow has been created. To create a variable, click **New**.

|Field|Description|
|-----|-----------|
|Label|Displayed column label. Localized depending on user locale.|
|Reference|Input field from another table.|
|Type|Data type. For example, integer or string.|
|Default value|Value used if you do not provide a value.|

## Activities

The Activities section enables you to set activity pinning and maximum activity count.

<table id="table_ActivitiesWorkflowTab"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity pinning

</td><td>

List of options that control updates to custom activities at the workflow level. Pinning protects custom activities from being updated automatically when downloaded from the ServiceNow Store. For more information, see [Workflow activity pinning](../../using-workflows/concept/c_ActivityPinning.md). The possible options are: -   **Set by activity**: Allows all activities in the workflow to use their own pinning settings. This is the default pinning option.
-   **Pin all activities**: Pins all activities in the workflow to their current version.
-   **Unpin all activities**: Allows all activities in the workflow to be updated.

</td></tr><tr><td>

Max activity count

</td><td>

The maximum number of activities performed by the workflow. This value is used to prevent infinite loops and is set to **100** by default. When the stated maximum count is reached, the workflow is canceled. If this field is blank, the maximum count is set to **-1**, and the workflow is canceled.

</td></tr></tbody>
</table>## Application

The Application section enables you to see application scope and scope restrictions.

<table id="table_ApplicationWorkflowTab"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application

</td><td>

\[Read-only\] Scope of this activity. For more information, see Application Scope.

</td></tr><tr><td>

Accessible from

</td><td>

Scope restrictions for this workflow. Possible settings are: -   **All application scopes**: Workflow is accessible to all application scopes.
-   **This application scope only**: Workflow access is limited to the scope named in the **Application** field.

 For more information see [Workflow scope](../../using-workflows/concept/c_WorkflowScope.md#).

</td></tr></tbody>
</table>## Schedule

Use the Schedule section to create a schedule for this workflow using the schedule builder.

<table id="table_ScheduleWorkflowTab"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Delivery based on

</td><td>

The schedule type for this workflow. Possible types are:

 -   **User-specified duration**: Duration based on a user-specified value. This is the default schedule type.
-   **Relative duration**: Duration calculated from a preconfigured schedule, such as **8-5 weekdays**.

</td></tr><tr><td>

Expected time

</td><td>

User-defined interval. This field is visible when the schedule type is **User-specified duration**.

</td></tr><tr><td>

Schedule

</td><td>

Preconfigured schedule that determines when this workflow runs.

</td></tr><tr><td>

Timezone

</td><td>

Time zone for this instance.

</td></tr></tbody>
</table>## Stages

The Stages section appears if you select a table with **Type** = **Workflow**.

|Field|Description|
|-----|-----------|
|Stage|Displays the workflow stage progress on the selected table. Optionally, select **Stage rendering** and **Stage order** schemes to customize the appearance of the stage field. The default values cover typical scenarios.|
|Stage rendering|The renderer to use when displaying stage icons on a form or list view. For more information about renderers, see [Workflow stage renderers](r_WorkflowStageRenderers.md#).|
|Stage order|The order of workflow stages when you view a workflow field in a list. Select **Computed** to let the workflow engine compute the stage order from the order of execution in the workflow. Select **User Specified** to use the **Order** field from that [Workflow stages](../../using-workflows/concept/c_WorkflowStages.md).|
|Name|The name of the stage as it appears in workflow fields..|
|Duration|Time allocated for the specific stage.|
|Order|The order of workflow stages when you view a workflow field in a list. Select **Computed** to let the workflow engine compute the stage order from the order of execution in the workflow. Select **User Specified** to use the **Order** field from that [Workflow stages](../../using-workflows/concept/c_WorkflowStages.md).|
|Value|The value of the stage when it is referenced from elsewhere in the system, such as in a script.|

## Estimated Runtime

The **Estimated Runtime** section opens the controls for configuring the **ERT** for the workflow. Core workflows included in the base system are not configured for estimated run time by default. All new workflows are configured with default ERT values automatically. You can edit existing run time estimates or configure new ones for any existing workflow. For details about how estimated run times are configured and calculated, see [Workflow run time metrics](../../using-workflows/concept/c_WorkflowRunTimeMetrics.md#).

<table id="table_EstimatedRuntimeWorkflowTab"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requires ERT

</td><td>

Check box to indicate that this workflow requires an estimated runtime configuration. You can use the ERT calculations to determine if workflows are running longer or shorter than expected and to identify errors in workflow processing. By default, new workflows require an ERT.

</td></tr><tr><td>

Estimated Run Time

</td><td>

The initial estimate for the workflow's run time.

</td></tr><tr><td>

Number of data points

</td><td>

\[Read only\] The number of times the system has compared the estimated run time to an actual run time result.

</td></tr><tr><td>

Outlier Percentage Threshold for ERT

</td><td>

\[Required\] The percentage deviation from the estimated run time that identifies an outlier workflow run time. The system uses a default value of 20. For more information, see [Outlying workflow run times](../../using-workflows/concept/c_WorkflowRunTimeMetrics.md#).

</td></tr></tbody>
</table>**Parent Topic:**[Create a workflow](../task/t_CreateAWorkflow.md)

