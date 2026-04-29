---
title: Troubleshoot workflows
description: Troubleshooting tools for workflows enable administrators to isolate execution paths, compare contexts, and track incomplete activities.Use the controls in a workflow timeline to isolate specific execution paths or compare multiple execution paths over time.Highlight execution paths and rollbacks to locate activities that may have been left in an unresolved state.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Troubleshoot workflows

Troubleshooting tools for workflows enable administrators to isolate execution paths, compare contexts, and track incomplete activities.

**Important:** As of the Zurich release, new customers no longer receive the legacy workflows created and published by ServiceNow, Inc.. All legacy workflow functionality has been replaced by Workflow Studio content. Only customers who upgraded from prior versions retain the ability to use and edit existing legacy workflows. While all customers retain the ability to create legacy workflows, you are strongly encouraged to instead use Workflow Studio to create process automation content. Only Workflow Studio will receive new features and enhancements.

The workflow timeline provides a visual representation of the workflow, including transitions and the elapsed time for each activity. A troubleshooting tool for highlighting execution paths helps users perform forensics on a workflow. The highlighting feature can group multiple execution paths in various colors and can isolate [rollback](../../workflow-activities/concept/c_ApprovalAndRollbackActivities.md) processing. Use the workflow highlighter to isolate incomplete tasks and approvals. You can also enable a workflow performance timing feature to troubleshoot slow workflows.

**Parent Topic:**[Classic Workflow](c_WorkflowOverview.md)

## Execution path troubleshooting in timelines

Use the controls in a workflow timeline to isolate specific execution paths or compare multiple execution paths over time.

Timelines show how the activities in the workflow progressed in relation to one another over time. Isolate execution paths and follow transition lines between subflows and the main flow. Processing times provide a view of the workflow that you cannot get from the workflow diagram. Tooltips give precise information about each activity, such as duration.

![](../image/WorkflowTimelineTroubleshooting.png "Workflow timeline troubleshooting")

## Execution history table

Highlight execution paths and rollbacks to locate activities that may have been left in an unresolved state.

### About this task

Rollbacks, cancels, and deletions during the execution of a workflow can prevent some activities from fully completing. Use highlighting in the execution history table to determine which activities in the workflow were left in an unresolved state.

### Procedure

1.  Run the workflow.

2.  Navigate to **Workflow** &gt; **All Contexts**.

3.  Select a context to troubleshoot.

4.  In the Workflow Context form, select the **Workflow Activity History** related list.

5.  Right-click an activity and select **Workflow Debug** &gt; **Toggle Execution Path Highlighting** from the context menu.

    All activities in that execution path are highlighted in a color selected by the platform. The debug path shows all activities that completed successfully during the workflow.

    ![Workflow highlight path](../image/WorkflowHighlightPath2.png)

6.  Right-click a rollback activity and select **Workflow Debug** &gt; **Toggle Rollback Highlighting** from the context menu.

    The platform highlights the rollback path \(restarted activities\) in a different color. Each color represents a group of activities that were part of the same rollback execution. The highlighting includes the activity that initiated the rollback. If you right-click an activity that was not part of a rollback, no rows are highlighted.

    **Note:** The rollback activity itself appears in both execution path and rollback highlighting.

    ![Workflow highlight path](../image/WorkflowHighlightPath1.png)

7.  To remove highlighting, right-click in the list and select an option to clear execution path or rollback highlighting.

    You can clear individual rollback paths or all rollback highlighting.


