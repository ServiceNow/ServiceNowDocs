---
title: Completed subflow values in scripts
description: The Parallel Flow Launcher activity exposes additional variables you can use in scripts.
locale: en-US
release: zurich
product: Workflow Activities
classification: workflow-activities
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Parallel Flow Launcher workflow activity, Subflow activities in workflow, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Completed subflow values in scripts

The **Parallel Flow Launcher** activity exposes additional variables you can use in scripts.

<table id="table_hc3_rm1_hr"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

coordinator

</td><td>

The WorkflowCoordinator used when running the subflows. You can use this variable in the **Finished script** to perform any final operations. Additionally, you can use the WorkflowCoordinator in a later workflow activity by passing the activity name or sys\_id to the WorkflowCoordinator.load\('&lt;Activity&gt;'\) function. For example, to load the WorkflowCoordinator object from a **Parallel Flow Launcher** activity called **Launch Subflows**, enter `var coord = WorkflowCoordinator.load('Launch Subflows');` in a later activity.

</td></tr><tr><td>

flow

</td><td>

The subflow launched by the activity that completed most recently. You can use this variable in the **Flow complete** script to perform any post-processing operations on each subflow. To get a complete subflow from a coordinator object, use `var flow = coord.getFlow(I);` where I is the numeric index of the subflow based on the order it was launched. These values are available from the completed subflow:

-   index: the numerical index of this subflow based on the order it was launched
-   workflow: the sys\_id or name, depending on which you passed to the WorkflowCoordinator constructor, of the workflow used for this subflow
-   inputs: any input values provided to the launched subflow
-   status: status of the subflow context
-   output: the value returned by the subflow
-   contextId: the sys\_id of the workflow context for the subflow

</td></tr></tbody>
</table>**Parent Topic:**[Parallel Flow Launcher workflow activity](../reference/r_ParallelFlowLauncher.md)

