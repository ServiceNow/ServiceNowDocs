---
title: Workflow editor title bar
description: When a workflow is opened in the canvas, the title bar displays the workflow title and the workflow status in italics. Possible states are Checked out by &lt;name&gt; and Published.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Workflow editor, Classic Workflow, Build workflows]
---

# Workflow editor title bar

When a workflow is opened in the canvas, the title bar displays the workflow title and the workflow status in italics. Possible states are **Checked out by &lt;name&gt;** and **Published**.

![](../image/WorkflowTitleBar.png "Workflow editor title bar")

Controls on the right side of the title bar manage the workflow.

-   **Workflow Properties** ![Workflow properties icon](../image/WorkflowPropertiesIcon.png): Opens the current workflow's properties form.
-   **Start** ![Run the workflow icon](../image/RunWorkflowIcon.png): Runs the workflow. This control is only available for workflows running on the Global table that are accessible from all application scopes. To test workflows that are on other tables, insert a record into that table that meets the condition of the workflow.
-   **Validate** ![Validate the workflow icon](../image/ValidateWorkflowIcon.png): Tests the workflow prior to publication. Validation detects potential problems that can prevent the workflow from publishing or cause the workflow to fail. For more information, see [Workflow Validation](../../workflow-validation/concept/c_WorkflowValidation.md).
-   **Help** ![Help icon](../image/HelpIcon.png): Opens documentation to help you create the workflow.

## Workflow menu

Click the menu icon in the title bar for additional options to configure the workflow.

![](../../workflow-administration/image/WorkflowTabMenu.png "Accessing the workflow menu")

These menu options are available:

|Option|Description|
|------|-----------|
|New Workflow|Creates a new workflow.|
|Open Existing|Opens another existing workflow.|
|Copy|Creates a duplicate of the workflow. Give the copy a different name.|
|Publish|Makes the personal workflow version public, overwriting the current published workflow version. This option is only available for checked out workflows.|
|Checkout|Creates a personal version of the workflow for you, which you can edit. This option is only available for published workflows.|
|Delete|Deletes the workflow. You cannot delete workflows that have contexts associated with them.|
|Set Inactive|Inactivates the workflow so that it cannot be used.|
|Expand Transitions|Redraws the transitions so that they do not overlap when they leave the activity condition.|
|Start Workflow|Starts a test run of the current workflow.|
|Validate Workflow|Runs validation tests on your workflow prior to publication. Use this validation to detect potential problems that can prevent the workflow from publishing or cause the workflow to fail. For more information, see [Work on workflows](../../workflow-administration/task/work-on-workflows.md#).|
|Collapse Transitions|Redraws the transitions so they overlap when they leave the activity condition.|
|Show Contexts|Displays all the [contexts](../../workflow-administration/reference/r_AdministeringWorkflowContexts.md) for the current workflow. You can use this option to troubleshoot a workflow.|
|Properties|Opens the Workflow Properties form, which defines the workflow's attributes.|
|Edit Inputs|Opens the Workflow Inputs list of variables that the workflow can accept when used as a subflow. For more information, see [Pass a variable from a workflow to a subflow](../../workflow-activities/task/t_VariableWorkflowSubflow.md#).|
|Edit Stages|Opens the Workflow Stages list. For more information, see [Workflow stages](../../using-workflows/concept/c_WorkflowStages.md). For tables with a column of Type = Workflow.|

**Parent Topic:**[Workflow editor](workflow-editor.md)

