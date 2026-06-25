---
title: Do the following in parallel flow logic
description: Run actions and subflows in separate paths within an isolated flow logic block.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/flow-logic-do-following-in-parallel.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Do the following in parallel flow logic

Run actions and subflows in separate paths within an isolated flow logic block.

With this flow logic, you can run actions and subflows in separate paths. If any action within the Do the following in parallel flow logic block must wait, other actions run until all paths within the block finish processing.

\[Omitted image "flow-logic-do-in-parallel.png"\] Alt text: Multiple paths in a Do the following in parallel flow logic block

**Note:** Paths in a Do the following in parallel flow logic block do not run in multiple threads, since a flow execution context runs in a single thread. However, there may be times when you want to run flows within separate contexts even though this may consume more of your instance's resources. To run subflows in separate flow contexts within the same flow, see [Dynamic flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-logic-dynamic-flow.md).

## Inputs

Do the following in parallel flow logic does not have field inputs. Instead, it displays a plus \(\[Omitted image "plus-icon.png"\] Alt text: New Branch Icon\) icon that enables you to create a path with actions or subflows.

The actions and subflows in each path run until all tasks within the flow logic block have completed.

## Outputs

This flow logic has no outputs, but actions and subflows in each path may have outputs. While the flow is running, outputs from a path are only accessible to other actions in the same path. After the Do the following in parallel flow logic completes, its final outputs are accessible to the rest of the flow.

## Create two tasks in parallel when a change request is created

In this example, a flow triggers when a new change request is created. Using **Do the following in Parallel**, two tasks are created in separate paths and are assigned to different groups. The flow uses the **Number** field data pill from the triggering change request to display the number in the short description for the task record.

\[Omitted image "parallel-example-1.png"\] Alt text: Do the following in parallel example

## Execution details

\[Omitted image "ex-details-do-following-parallel.png"\] Alt text: Example execution details for a do the following in parallel flow

1.  The header shows the state, start time, and runtime for the flow logic.
2.  The Configuration Details section shows the state, start time, and runtime for each path in the flow logic block.

## General guidelines

-   **Avoid creating data dependencies between paths**

    Since a flow can run paths in any order, avoid creating data dependencies between separate paths. For example, do not have one path that creates a record and another path that updates the same record. The update record path may run before the create record path.

-   **Do not share data between paths**

    Workflow Studio prevents you from dragging data pills between paths because the system cannot determine which path will finish first to supply the output value.


**Parent Topic:**[Workflow Studio flow logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-logic.md)

**Related topics**  


[Append to Flow Variables flow logic]()

[Assign subflow outputs flow logic]()

[Call a workflow flow logic]()

[Do the following until flow logic]()

[Dynamic flows flow logic]()

[End Flow flow logic]()

[Exit Loop flow logic]()

[For Each flow logic]()

[Get Flow Outputs flow logic]()

[Go back to flow logic]()

[If flow logic]()

[Make a decision flow logic]()

[Set Flow Variables flow logic]()

[Skip Iteration flow logic]()

[Try flow logic]()

[Wait for a duration flow logic]()

