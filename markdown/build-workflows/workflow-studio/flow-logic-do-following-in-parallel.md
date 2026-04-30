---
title: Do the following in parallel flow logic
description: Run actions and subflows in separate paths within an isolated flow logic block.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Workflow Studio flow logic, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Do the following in parallel flow logic

Run actions and subflows in separate paths within an isolated flow logic block.

With this flow logic, you can run actions and subflows in separate paths. If any action within the Do the following in parallel flow logic block must wait, other actions run until all paths within the block finish processing.

![Multiple paths in a Do the following in parallel flow logic block](../images/flow-logic-do-in-parallel.png "Paths in a Do the following in parallel flow logic block")

**Note:** Paths in a Do the following in parallel flow logic block do not run in multiple threads, since a flow execution context runs in a single thread. However, there may be times when you want to run flows within separate contexts even though this may consume more of your instance's resources. To run subflows in separate flow contexts within the same flow, see [Dynamic flows](flow-logic-dynamic-flow.md).

## Inputs

Do the following in parallel flow logic does not have field inputs. Instead, it displays a plus \(![New Branch Icon](../../../build/app-engine-studio/image/plus-icon.png)\) icon that enables you to create a path with actions or subflows.

The actions and subflows in each path run until all tasks within the flow logic block have completed.

## Outputs

This flow logic has no outputs, but actions and subflows in each path may have outputs. While the flow is running, outputs from a path are only accessible to other actions in the same path. After the Do the following in parallel flow logic completes, its final outputs are accessible to the rest of the flow.

## Create two tasks in parallel when a change request is created

In this example, a flow triggers when a new change request is created. Using **Do the following in Parallel**, two tasks are created in separate paths and are assigned to different groups. The flow uses the **Number** field data pill from the triggering change request to display the number in the short description for the task record.

![Do the following in parallel example](../images/parallel-example-1.png "Do the following in parallel flow logic inputs")

## Execution details

![Example execution details for a do the following in parallel flow](../images/ex-details-do-following-parallel.png "Do the following in parallel execution details")

1.  The header shows the state, start time, and runtime for the flow logic.
2.  The Configuration Details section shows the state, start time, and runtime for each path in the flow logic block.

## General guidelines

-   **Avoid creating data dependencies between paths**

    Since a flow can run paths in any order, avoid creating data dependencies between separate paths. For example, do not have one path that creates a record and another path that updates the same record. The update record path may run before the create record path.

-   **Do not share data between paths**

    Workflow Studio prevents you from dragging data pills between paths because the system cannot determine which path will finish first to supply the output value.


**Parent Topic:**[Workflow Studio flow logic](flow-logic.md)

**Related topics**  


[Assign subflow outputs flow logic](flow-logic-assign-subflow-outputs.md)

[Call a workflow flow logic](flow-logic-call-workflow.md)

[Do the following until flow logic](flow-logic-do-until.md)

[Dynamic flows flow logic](flow-logic-dynamic-flow.md)

[End Flow flow logic](flow-logic-end-action.md)

[Exit Loop flow logic](../reference/exit-loop-flow-logic.md)

[For Each flow logic](flow-logic-for-each.md)

[Get Flow Outputs flow logic](../reference/get-flow-outputs-flow-logic.md)

[Go back to flow logic](../reference/go-back-to-flow-logic.md)

[If flow logic](flow-logic-if.md)

[Make a decision flow logic](flow-logic-make-decision.md)

[Set Flow Variables flow logic](flow-logic-set-flow-variables.md)

[Skip Iteration flow logic](../reference/skip-iteration-flow-logic.md)

[Try flow logic](flow-logic-try.md)

[Wait for a duration flow logic](flow-logic-wait-for-a-duration.md)

