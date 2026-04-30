---
title: Workflows used as subflows
description: A workflow can launch another workflow as an activity.
locale: en-US
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Workflow management, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflows used as subflows

A workflow can launch another workflow as an activity.

The parent workflow triggers the subflow and then waits for the subflow to complete before continuing. Run the workflow validation tool prior to publishing to detect missing subflows and other dependency problems, such as those involving update sets.

The **Workflows** tab in the Workflow Editor contains a list of the workflows available for use as subflows.

![Workflows available to use as subflows](../image/WorkflowsUsedAsSubflows.png "Workflows available to use as subflows")

Make sure that the selected subflow is active. If the subflow is inactive, the main workflow will hang with a **Loading** message. If you place an inactive subflow into a workflow, the subflow appears with a red banner, indicating that it cannot run. An active subflow is highlighted in blue when selected.

![Workflow with active subflows](../image/ActiveSubflowsInAWorkflow.png "Workflow with active subflows")

## Subflows and the Create Task activity

If a workflow contains a [**Create Task**](r_CreateTask.md) activity that has executed on the current record, additional task activities in the workflow might not execute as expected.

This can happen when the same subflow containing a Create Task activity runs more than once in a parent flow. When the subflow reruns and attempts to execute the **Create Task** activity again, the system reopens the first task activity instead and does not create an additional task.

**Note:** An alternative to creating duplicate subflows that use the **Create Task** activity is to add a [**Run Script**](r_RunScriptActivity.md) activity to the workflow that creates a task with a script.

![](../image/WorkflowCreateTaskSubflowDiagram.png "The same create task activity runs twice in a workflow")

In this configuration, the workflow does not run the same subflow containing a **Create Task** activity more than once. This allows the workflow to create additional tasks.

![](../image/WorkflowCreateTaskSubflow2Diagram.png "Running different subflows containing the Create Task activity")

-   **[Pass a variable from a workflow to a subflow](../task/t_VariableWorkflowSubflow.md#)**  
Use this process to pass variables from a parent workflow to a subflow.
-   **[Prepare a subflow](../task/t_PrepareASubflow.md#)**  
Review the process of preparing a subflow for use in a parent workflow, and for preparing the parent workflow to use a subflow.

**Parent Topic:**[Workflow management](../../workflow-administration/concept/managing-workflows.md)

