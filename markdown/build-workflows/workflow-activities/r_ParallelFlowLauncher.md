---
title: Parallel Flow Launcher workflow activity
description: The Parallel Flow Launcher activity launches multiple subflows in parallel.
locale: en-US
release: yokohama
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Subflow activities in workflow, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Parallel Flow Launcher workflow activity

The **Parallel Flow Launcher** activity launches multiple subflows in parallel.

Workflows running in parallel execute simultaneously and may complete in any order. The activity can launch a single subflow or multiple subflows as needed. You can manage the input values and values returned for each subflow.

**Note:** The Parallel Flow Launcher activity waits until all subflows are completed before proceeding. If any subflow does not finish, the activity waits indefinitely.

Do not launch a large number of subflows with the Parallel Flow Launcher activity. If overused, this activity can overburden the instance. For launching very large numbers of subflows, consider putting the Parallel Flow Launcher inside a loop controlled by a turnstile or other conditional activity and having it do batches.

## Activity variables

Activity variables determine the initial behavior of the activity.

<table id="table_rvx_lj1_hr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="subhead" colspan="2">

Parallel Flow Launcher configuration

</td></tr><tr><td>

Name

</td><td>

A unique name for the activity.

</td></tr><tr><td>

Stage

</td><td>

The stage to display when the workflow reaches the activity.

</td></tr><tr><td>

Inputs

</td><td>

Inputs to the subflows to run. Specify an array of name: value pairs for each input defined in the workflow being launched. The name and data type of each input variable entered must match those used by the subflow that this activity launches. For a detailed example, see [Parallel Flow Launcher Example](r_ParallelFlowLauncherExample.md).

</td></tr><tr><td class="subhead" colspan="2">

Parallel Flow Launcher selection

</td></tr><tr><td>

Workflow

</td><td>

The workflow to run.

</td></tr><tr><td>

Advanced

</td><td>

Check **Advanced**, to enter a script that uses a WorkflowCoordinator object to manage the subflows. When you check Advanced, a text box appears where you can enter a script that specifies a unique workflow for each set of input variables. See [WorkflowCoordinator object](../concept/c_WorkflowCoordinatorObject.md) for more information.

</td></tr><tr><td class="subhead" colspan="2">

Parallel Flow Launcher iterationSpecify parameters to tune the performance of batched workflows.

</td></tr><tr><td>

Count

</td><td>

If not specified by an input set, **Count** determines the number of subflows executed in parallel from this activity. If the **Advanced** option is not selected, ensure that this field is populated with a valid number.

</td></tr><tr><td>

Max flows

</td><td>

The maximum number of workflows this activity can launch. If this value is a positive integer, it overrides the max parameter used in the WorkflowCoordinator constructor.

</td></tr><tr><td>

Max simultaneous

</td><td>

The maximum number of parallel workflows this activity can run at one time. If this value is a positive integer, it overrides the poolsize parameter used in the WorkflowCoordinator constructor.

</td></tr><tr><td class="subhead" colspan="2">

Parallel Flow Launcher Process

</td></tr><tr><td>

Process flow complete

</td><td>

To specify a script that runs after each subflow completes, check **Process flow complete**. If you check this field, a text box labelled **Flow complete** appears, where you can enter the script to run.

</td></tr><tr><td>

Flow complete

</td><td>

The script that runs each time a subflow finishes. This field is available when the **Process flow complete** option is selected. The same script functions and variables available in other workflow scripts, such as those in the Run Script activity, are available here. For more information, see [Completed subflow values in scripts](../concept/c_CompletedSubflowValuesInScripts.md).

 The variable "flow" is available to this script. It is an object that contains the following information about the flow that is finishing:

 **flow.output \(String\)**: The value that the subflow returns to the parent if it executed a Return Value activity before ending.

 **flow.index \(Number\)**: The zero-relative index of the subflow that finished.

 **flow.contextId \(String\)**: The sys\_id of the workflow context for the completed subflow.

 **flow.inputs \(Object\)**: The inputs that were passed to the subflow when its context was created and started.

 **flow.status \(String\)**: The final state of the context. This corresponds to the **state** column in the subflow context record, which has possible values of **executing**, **finished**, **cancelled**, or **faulted**. \(Since the flow is completed, it cannot be **executing** at this point.\)

</td></tr><tr><td class="subhead" colspan="2">

Parallel Flow Launcher Split

</td></tr><tr><td>

Process finished

</td><td>

To specify a script that runs after all subflows have finished, check **Process finished**. If you check this field, a text box labelled **Finished Script**appears where you can enter the script to run. The ‘coordinator’ variable is made available to this script and is an object that allows access to any of the finished subflows using the getFlow\(index\) method. For example:```
for (var i = 0; i < coordinator.getNumFlows(); i++) 
```

```
writeFlowResultsToTable( i, coordinator.getFlow(i) );
```

</td></tr><tr><td>

Finished script

</td><td>

The script that runs after all subflows launched by the activity are complete. You can use variables that contain completed flow information in this script. The ‘coordinator’ variable is made available to this script and is an object that allows access to any of the finished subflows using the getFlow\(index\) method. For example:

 ```
for (var i = 0; i < coordinator.getNumFlows(); i++) 
```

```
writeFlowResultsToTable( i, coordinator.getFlow(i) );
```

This field is available when **Process finished** is selected.

</td></tr></tbody>
</table>## States

The activity state tells the workflow engine what to do with the activity. To view an activity's state, point to the activity. A pop-up window shows the **State** and **Result** of the activity. If the activity is in an error state, the pop-up window provides a brief **Fault Description**.

|State|Description|
|-----|-----------|
|Waiting|The activity is waiting for all subflows to finish. All subflows have started and some may have finished.|
|Finished|The activity successfully completed all of the subflows.|
|Error|The activity encountered an error.|

-   **[WorkflowCoordinator object](../concept/c_WorkflowCoordinatorObject.md)**  
A WorkflowCoordinator object specifies which subflows to run and the input variables to pass to those subflows.
-   **[Completed subflow values in scripts](../concept/c_CompletedSubflowValuesInScripts.md)**  
The **Parallel Flow Launcher** activity exposes additional variables you can use in scripts.
-   **[Parallel Flow Launcher example](r_ParallelFlowLauncherExample.md)**  
This example shows how to use the **Parallel Flow Launcher**activity with an array of input values and with a WorkflowCoordinator object.

**Parent Topic:**[Subflow activities in workflow](../concept/c_SubflowActivities.md)

