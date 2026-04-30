---
title: WorkflowCoordinator object
description: A WorkflowCoordinator object specifies which subflows to run and the input variables to pass to those subflows.
locale: en-US
release: yokohama
product: Workflow Activities
classification: workflow-activities
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Parallel Flow Launcher workflow activity, Subflow activities in workflow, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# WorkflowCoordinator object

A WorkflowCoordinator object specifies which subflows to run and the input variables to pass to those subflows.

When using a WorkflowCoordinator object, you can create a **Parallel Flow Launcher** activity that launches multiple subflows. When using the activity without a WorkflowCoordinator object, you can only launch a single subflow multiple times. Use one of the following methods to specify a WorkflowCoordinator object for the activity when the **Advanced** activity input variable is selected.

-   Reference a workflow scratchpad variable that contains an existing WorkflowCoordinator object. To save a WorkflowCoordinator object to the scratchpad, call the save\(variableName\) function on the WorkflowCoordinator object. You can reference the object using the value passed in the **variableName** parameter. For example, you can create a WorkflowCoordinator object in a **Run Script** activity, save the object using `<object>.save('coord')`, and then call this object by entering `coord` in the **Workflow** activity variable of a subsequent **Parallel Flow Launcher** activity.
-   Define the WorkflowCoordinator within the **Workflow** activity variable. Add the `javascript:` identifier at the beginning of the script. The [Parallel Flow Launcher example](../reference/r_ParallelFlowLauncherExample.md) shows how to use a WorkflowCoordinator object in this way.
-   Create a factory class to define the WorkflowCoordinator object. The system does not provide a factory class for WorkflowCoordinator by default.

**Parent Topic:**[Parallel Flow Launcher workflow activity](../reference/r_ParallelFlowLauncher.md)

