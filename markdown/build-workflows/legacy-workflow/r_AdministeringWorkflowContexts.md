---
title: Administering workflow contexts
description: The workflow context performs the activities and transitions defined in the workflow with the new record as current.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/legacy-workflow/r\_AdministeringWorkflowContexts.html
release: zurich
product: Legacy Workflow
classification: legacy-workflow
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Workflow administration, Classic Workflow, Build workflows]
---

# Administering workflow contexts

The workflow context performs the activities and transitions defined in the workflow with the new record as current.

Workflow in ServiceNow names a running workflow a Workflow Context. The Workflow Context maintains the state of the overall process in the Workflow Context record. The Workflow Context maintains the state of the individual activities as they execute in a series of related lists. These lists maintain the state of currently executing activities, the result of finished activities, and the execution path the workflow took through the process model.

The Workflow Context canvas provides a visual representation of the execution path the workflow took through the process model. The state of each activity \(finished, executing, cancelled, error\) is represented using the color palette. The executed paths are represented in the color blue; the non-executed paths are represented in grey. Active and historic workflow contexts, as well as the activities within them, can be viewed using the Live Workflows section of the Workflow application menu.

## Viewing a workflow context

Workflow contexts can be found in two places:

-   From the **Workflow Context** related link on the form of the task being powered by the workflow.
-   By navigating to **Workflow** &gt; **All Contexts** and selecting an active context.

## Displaying workflow progress

Two related links on the Workflow Context form allow you to view the progress of a workflow in different formats.

-   **Show Timeline** displays the workflow context as a [timeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/legacy-workflow/c_WorkflowTimelines.md).
-   **Show Workflow** displays the workflow context in the graphical Workflow Editor.

## Graphical interface

To view the workflow context in the graphical Workflow Editor interface, click the **Show Workflow** link from either the workflow context record or the current record.

\[Omitted image "ShowWorkflow.png"\] Alt text:

In the top right hand corner are two controls:

<table id="simpletable_rqj_gls_s4"><tbody><tr><td>

\[Omitted image "WorkflowRefreshIcon.png"\] Alt text: Refresh icon

</td><td>

Refreshes the workflow context.

</td></tr><tr><td>

\[Omitted image "WorkflowKeyIcon.png"\] Alt text: Color key icon

</td><td>

Displays a key of the colors used in the workflow to denote the state of activities and transitions:\[Omitted image "WorkflowState.png"\] Alt text: Workflow state

</td></tr></tbody>
</table>## Execution order

View tooltip text in the workflow context graphical view to see the execution order of individual activities.

In **Workflow** &gt; **Live Workflows** &gt; **Active Contexts** or **All Contexts**, Open the context you want to examine. Click **Show Workflow**, and point to a finished or executing activity. The tooltip shows error data, execution time, and the order in which the activity executed in the workflow. Use this data to help troubleshoot activities in an error state.

\[Omitted image "ExecutionOrderWorkflow.png"\] Alt text: View the order in which a context executed

-   **[Cancel a workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/legacy-workflow/t_CancelingAWorkflow.md)**  
Canceling a workflow stops the workflow from executing and sets the workflow context **State** to **Canceled**. To cancel an executing workflow, you can use the cancelContext\(context\) script. You can define an onCancel script to clean up unresolved workflow activities.

**Parent Topic:**[Workflow administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/legacy-workflow/c_WorkflowAdministration.md)

