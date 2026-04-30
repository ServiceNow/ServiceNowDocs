---
title: Display approvers in workflow stage fields
description: Enable workflow stage fields to display approvers, change the number of approvers to display, or disable displaying approvers.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a workflow stage field, Workflow stages, Workflow management, Classic Workflow, Build workflows]
---

# Display approvers in workflow stage fields

Enable workflow stage fields to display approvers, change the number of approvers to display, or disable displaying approvers.

## Before you begin

Role required: admin

## About this task

By default, only workflow stage fields that use the Workflow-driven renderer can display a list of approvers. Only these [workflow stage renderer](../reference/r_WorkflowStageRenderers.md#) types support displaying approvers.

-   Linear renderer
-   Main flow renderer
-   Workflow-driven renderer

## Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Administration** &gt; **Properties**.

    The system displays the Workflow Properties page.

2.  Set the following properties.

<table id="table_r1g_315_b2b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number of approvers to show if approvers are displayed for workflow stages. Only valid for supported list v2 renderers.glide.workflow.renderer.show\_approver\_limit

</td><td>

Sets the maximum number of approvers to display within a workflow stage field. The system displays an ellipsis character when there are more approvers than the display limit allows.-   Type: integer
-   Default value: 5


</td></tr><tr><td>

Show approvers when displaying workflow stages with the Linear renderer.glide.workflow.renderer.linear.show\_approver

</td><td>

Enables \(true\) or disables \(false\) the Linear renderer to display approvers.-   Type: true \| false
-   Default value: false


</td></tr><tr><td>

Show approvers when displaying workflow stages with the Main flow renderer.glide.workflow.renderer.mainflow.show\_approver

</td><td>

Enables \(true\) or disables \(false\) the Main flow renderer to display approvers.-   Type: true \| false
-   Default value: false


</td></tr><tr><td>

Show approvers when displaying workflow stages with the Workflow-driven renderer.glide.workflow.renderer.workflowdriven.show\_approver

</td><td>

Enables \(true\) or disables \(false\) the Workflow-driven renderer to display approvers.-   Type: true \| false
-   Default value: true


</td></tr></tbody>
</table>3.  Click **Save**.

4.  Add stages to workflows that have associated workflow stage fields.

    **Note:** If you add stages to a subflow, the parent workflow must also have stages.

5.  For each approval activity you want to display approvers, select a **Stage** value.

    For example, the sample workflow **Service Catalog Item Request** has two approval activities. The first **Approval - User** activity has a **Stage** value of `Dept. Head Approval`. The second **Approval - User** activity has a **Stage** value of `CIO Approval`.


## Result

The workflow stage field renderers you enabled display approvers up to the approver display limit. For example, a Workflow-driven stage field displays up to five approvers when the workflow reaches an approval stage.

**Parent Topic:**[Create a workflow stage field](t_CreateAWorkflowStageField.md)

