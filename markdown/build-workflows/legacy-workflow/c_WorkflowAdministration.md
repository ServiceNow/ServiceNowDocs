---
title: Workflow administration
description: Tailor workflows exactly the way you want them.
locale: en-US
release: yokohama
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Classic Workflow, Build workflows]
---

# Workflow administration

Tailor workflows exactly the way you want them.

-   **[Workflow roles](../reference/r_WorkflowRoles.md)**  
Certain roles are required to use workflows.
-   **[Administering workflow contexts](../../workflow-administration/reference/r_AdministeringWorkflowContexts.md)**  
The workflow context performs the activities and transitions defined in the workflow with the new record as current.
-   **[Scheduling a workflow](../../workflow-administration/reference/r_SchedulingAWorkflow.md)**  
In addition to being run based on conditions, workflows can also be scheduled to perform at a particular time, similar to a scheduled job.
-   **[Workflow movement with update sets](../../workflow-administration/concept/c_WorkflowMovementWithUpdateSets.md#)**  
The system tracks workflows in update sets differently than other records because workflow information is stored across multiple tables.
-   **[Input variable movement](../../workflow-administration/concept/c_InputVariableMovement.md)**  
You can add input variables to existing workflows and add them to update sets.
-   **[Workflow timelines](../../workflow-administration/concept/c_WorkflowTimelines.md#)**  
The system provides a timeline view of history activities associated with a workflow context.
-   **[Workflow error handling](../../workflow-administration/concept/c_WorkflowErrorHandling.md)**  
The personalized JavaScript that users create in workflow activity variables is vulnerable to run-time syntax errors. Available error information is available in a tooltip when you point to a workflow activity in an error state.
-   **[Workflow run time metrics](../../using-workflows/concept/c_WorkflowRunTimeMetrics.md#)**  
You can enable the collection of workflow run time metrics to determine whether workflows are performing as expected or consuming additional resources.
-   **[Workflow pause utility](../../workflow-administration/concept/workflow-pause-utility.md)**  
Workflow Pause Utility provides functionality you can use to pause or resume all workflow contexts, a subset of qualified workflow contexts, or individual workflow contexts. You designate the data and time of day at which the paused workflows should resume, and can manually resume individual workflows as needed.
-   **[Encrypted workflow scratchpad](../../workflow-administration/concept/encrypted-workflow-scratchpad.md#)**  
The Encrypted Workflow Scratchpad plugin \(com.snc.encrypted.scratchpad\) provides encrypted scratchpad support for workflow context and workflow executing activities.

**Parent Topic:**[Classic Workflow](c_WorkflowOverview.md)

