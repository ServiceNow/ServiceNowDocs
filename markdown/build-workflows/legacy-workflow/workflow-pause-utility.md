---
title: Workflow pause utility
description: Workflow Pause Utility provides functionality you can use to pause or resume all workflow contexts, a subset of qualified workflow contexts, or individual workflow contexts. You designate the data and time of day at which the paused workflows should resume, and can manually resume individual workflows as needed.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Workflow administration, Classic Workflow, Build workflows]
---

# Workflow pause utility

Workflow Pause Utility provides functionality you can use to pause or resume all workflow contexts, a subset of qualified workflow contexts, or individual workflow contexts. You designate the data and time of day at which the paused workflows should resume, and can manually resume individual workflows as needed.

Once activated, the Workflow Pause Utility plugin \(com.glideapp.workflow.pause\) updates several tables when you pause or resume workflows. Each table stores specific data related to each paused or resumed workflow.

-   **wf\_pause\_request**

    Records every workflow pause request. The system automatically updates and inserts records in this table whenever you pause workflow contexts. It tracks user-specified resume time, whether the pause request is still active, and the total number of workflow activities that paused or resumed.

-   **wf\_pause\_status**

    Records the status of each workflow context you pause. When you pause workflow contexts, the plugin waits until the current executing activity finishes, and pauses it before the next activity starts. It tracks the specific activity on which the workflow context was paused and whether it has resumed. If the workflow is paused, it tracks the time at which it is scheduled to resume.

-   **wf\_pause\_group\_request**

    Pauses the specific set of workflow contexts you designate using filtering in [Group Pause Requests](../task/pause-resume-all-multiple-workflows.md). You can manually pause all currently active workflows by clicking the **Pause All** check box.

-   **wf\_pause\_snapshot**

    Before pausing and after resuming a workflow, the table records a snapshot of the current state of the workflow context. The table also records the state of the currently executing activity on the paused workflow context.


## Use examples

When you take down an instance for maintenance, you can pause all or selected active workflow contexts, and then resume them after you complete the maintenance.

You have an integration workflow context that hits an internal service that is down for maintenance. You can pause all instances of that workflow context from progressing to the next activity, allowing time for the internal service to be restored. Then, the paused workflow contexts can be resumed.

-   **[Request workflow pause utility](../task/request-workflow-pause-utility.md)**  
You can request the Workflow Pause Utility plugin \(com.glideapp.workflow.pause\) if you have the admin role. This plugin may include demo data and activates related plugins if they are not already active.
-   **[Pause and resume individual workflows](../task/pause-resume-individual-workflows.md)**  
Pause individual workflow contexts. Specify the date and time of day at which the workflow context should resume.
-   **[Pause and resume all or multiple workflows](../task/pause-resume-all-multiple-workflows.md)**  
Use Workflow Pause Group Requests to pause, or resume, groups of workflows, or all active workflows. If pausing a group of workflows, use filtering functions to select the workflows. If pausing all active workflows, select the Pause All check box to indicate that all currently active workflows should be paused.
-   **[Monitor workflow pause requests](../task/monitor-workflow-pause-requests.md)**  
You can monitor the status of workflow pause requests using Workflow Pause Request.

**Parent Topic:**[Workflow administration](../../workflow/concept/c_WorkflowAdministration.md)

