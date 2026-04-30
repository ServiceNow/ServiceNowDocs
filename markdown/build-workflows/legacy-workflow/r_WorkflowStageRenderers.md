---
title: Workflow stage renderers
description: Workflow stage renderers determine how a workflow displays stages in a workflow field.In most cases, the default workflow-driven renderer should be used. If you have specific requirements for displaying stages, you can select a different stage renderer.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Create a workflow stage field, Workflow stages, Workflow management, Classic Workflow, Build workflows]
---

# Workflow stage renderers

Workflow stage renderers determine how a workflow displays stages in a workflow field.

There are multiple renderers available.

**Note:** Most workflows should use the workflow-driven renderer. This renderer is used by default for all workflows. Use a different stage renderer only after careful consideration and to satisfy specific requirements for how the stages appear.

## Workflow-driven

Use the workflow-driven renderer as much as possible. This renderer displays icons for stages using the stage state controlled by the workflow. Icons are displayed in a way that is meaningful for many situations. This renderer can display stages from a main workflow and subflows. The order of the icons is determined by the expected path of the executing workflow. As the workflow progresses, stages on paths that the workflow did not take are removed from the display. Stages from paths other than the expected path are not included unless the workflow follows that path.

The **Stage order** field on the **Stages** tab has two options:

-   **Computed** uses the actual workflow path in order
-   **User-specified** uses the order specified in the **Order** column on the Workflow Stages record

**Note:** If the workflow context for a request item has been deleted, the stages for that request item can no longer be rendered. This stage history is stored on the workflow context.

## Main flow

The main flow renderer displays icons for stages defined in the main workflow only. Use this renderer when you do not want to expose the details of the subflows. For example, a single main workflow may run several subflows to handle implementation details. The stages in these subflows do not provide useful information for the user who starts the workflow, but are useful when editing the subflow. In this scenario, using the main flow renderer leads to the best user experience. The stage field displays the high-level process of the workflow without exposing unnecessary details.

The **Stage order** field on the **Stages** tab has two options:

-   **Computed** uses the actual workflow path in order
-   **User-specified** uses the order specified in the **Order** column on the Workflow Stages record

## Linear

Linear rendering displays all stage icons from the main workflow and all subflows within a single workflow field on a list or form. It displays icons in a linear sequence regardless of the paths the workflow follows as it executes. This renderer uses stages defined in both the main workflow and any subflows that the main flow launches. The icons appear in the user-specified order. Skipped stages do not appear.

Use this renderer when the workflow stages must display in a consistent order and the actual details of how the workflow runs are less important. For example, a workflow may revisit or revert to previous stages based on one or more [Condition Workflow activities](https://www.servicenow.com/docs/access?context=r_ConditionActivites&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). Displaying these loops in the stage field does not provide useful information to the user. In this scenario, using the linear renderer leads to the best user experience. The stage field displays the predefined process, including stages from subflows, in a consistent order.

For example, you can create a service catalog workflow that uses a subflow to complete delivery of the requested item. The following images illustrate the main flow and subflow for ordering corporate-branded supplies.

![](../image/600pxLinearMainflow.png "Linear main flow")

![](../image/600pxLinearSubflow.png "Linear subflow")

The linear renderer displays all these stages in one workflow field. The parent workflow specifies the **Waiting for approval**, **Fulfillment**, and **Completed** stages. The subflow specifies the **Delivery** and **Waiting for Task**, and **Delivery OK** stages.

## Progress bar

The progress bar renderer displays a single progress bar instead of a sequence of stage icons. This renderer is particularly useful when you want to display the general progress of the workflow as a percent. Each stage in the workflow controls an equal percentage of the progress bar. For example, if a workflow has 10 stages, reaching each stage causes the workflow field to display an additional 10% of the progress bar. Stage names do not appear in the progress bar.

The progress bar renderer provides a way to display the status of a workflow that has a large number of stages. Other rendering options may provide a better user experience when rendering fewer than four stages in a single workflow.

The **Stage order** field on the **Stages** tab has two options:

-   **Computed** uses the actual workflow path in order
-   **User-specified** uses the order specified in the **Order** column on the Workflow Stages record

![](../image/WfFieldProgressRenderer.png "Workflow field progress bar")

## Legacy

The legacy renderer displays stages in the same way as releases prior to Dublin. When an instance is upgraded from a release prior to Dublin, all existing workflows are set to use the legacy renderer. Whenever possible, use a different stage renderer instead. If you want your workflow to maintain pre-Dublin behavior, use the Legacy option. The legacy renderer sometimes assigns incorrect data to and/or reports incorrect data from the workflow stage field. If possible, we recommend all workflows use the Workflow-driven renderer.

With the legacy renderer, you can create and reference a custom workflow field icon set by setting the icons attribute to a new script include. For example, to use the WorkflowIconsSCR script include to define which icons to use, add the attribute **icons=WorkflowIconsSCR** to the **Attributes** field of the dictionary entry for the workflow field. To use the default icon display behavior, use the attribute **icons=WorkflowIconsStages**.

The legacy renderer works with all tables except the Requested item \[sc\_req\_item\] table. In this case, use the requested item renderer instead.

## Requested item

The requested item renderer functions the same way as the legacy renderer, but is for use with the Requested item \[sc\_req\_item\] table.

Only in Now Mobile, default stage renderer is used.

**Parent Topic:**[Create a workflow stage field](../task/t_CreateAWorkflowStageField.md)

## Select a stage renderer

In most cases, the default workflow-driven renderer should be used. If you have specific requirements for displaying stages, you can select a different stage renderer.

### Before you begin

Consider the following when selecting a stage renderer:

-   Use the workflow-driven renderer if possible. This is the default renderer that should be used in most cases.
-   Use the legacy renderer only if your instance was upgraded from a release prior to Dublin and you want your workflow to maintain pre-Dublin behavior.

To use linear, main flow, or progress bar rendering, satisfy the following requirements.

<table id="table_tl3_xnp_3r"><thead><tr><th>

Renderer

</th><th>

Requirements

</th></tr></thead><tbody><tr><td>

Linear

</td><td>

-   The parent workflow and all subflows must modify the same current record.
-   In the properties for all subflows, the **Stage field** value for all subflows must match that of the parent workflow.
-   The parent flow and all subflows must contain the same stages. Use a stage set to ensure the parent flow and all subflows have the same stages.
-   On the workflow canvas, each workflow needs only the stages used directly by that workflow. It is not necessary to add stages from subflows to activities on the parent flow, or stages from the parent flow to activities on the subflows.

</td></tr><tr><td>

Main flow

</td><td>

-   The workflow contains subflows.
-   You do not want or need to reveal the details about the subflows.

</td></tr><tr><td>

Progress bar

</td><td>

-   The workflow properties must have a **Stage ordering** value of **User-defined**
-   There must be workflow stages within the workflow.
-   Because stage names do not appear in a workflow field when using the progress bar renderer, you can simplify stage names to represent a percentage of the workflow. For example, if a process has four main steps, name the workflow stages as 25%, 50%, 75%, and 100%. Enter the numerical value of each stage, such as 25, in the **Value** and **Order** fields.

</td></tr></tbody>
</table>### About this task

To select a stage renderer:

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  Open and check out the workflow.

3.  In the title bar, click the menu icon and select **Properties**.

4.  In the Workflow Properties dialog box, click the **Stages** tab.

5.  From the **Stage rendering** list, select a stage renderer.

    -   If you are using two workflows to update two unique workflow fields on a single record, both workflows must use a non-legacy renderer. You can select a different stage renderer for each workflow but do not select **Legacy** for either one.
    -   If you want to use the linear renderer, make sure you select **Linear** in the properties for the parent workflow and all subflows.
6.  Click **Update**.


