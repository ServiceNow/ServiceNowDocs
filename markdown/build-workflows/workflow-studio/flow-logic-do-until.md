---
title: Do the following until flow logic
description: Apply one or more actions repeatedly until an end condition is met. You can use the flow data to specify the end conditions.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Workflow Studio flow logic, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Do the following until flow logic

Apply one or more actions repeatedly until an end condition is met. You can use the flow data to specify the end conditions.

You can use **Do the following until** flow logic to create a loop that repeatedly applies one or more actions. This flow logic requires a condition specifying when to stop the loop.

**Note:** When you set a data pill value from inside a Do the following branch of flow logic, the data pill value is only available to other actions in the same branch. Referencing a data pill value that was set inside a Do the following branch from outside of the flow logic branch produces a null value.

## Inputs

-   **Condition label**

    Data type: **String**

    Text description of the condition that you want to display in the flow.

-   **Conditions**

    Data type: **Conditions**

    Conditions under which the loop terminates. You could, for example, end a loop when the state of an incident changes. If the end condition is true when the flow starts, the loop runs once and then stops.

    **Tip:** You can use flow variables to check for custom conditions such as the number of times a loop has run.


## Outputs

This flow logic produces no outputs.

## Send a daily email until an incident is resolved

In this example, the flow sends a daily email about the incident, until the incident is in a closed or canceled state. Inside the **Do the following** branch, there is a step for looking up the incident record.

![Example Do the following until flow.](../images/do-until-example-1.png)

## Execution details

![Example execution details for a do until flow.](../images/ex-details-do-until.png "Execution details for Do the following until")

1.  The header shows the state, start time, and runtime for the flow logic.
2.  This flow logic can run actions or subflows multiple times until it's condition is met. Use the arrow icons to select an iteration and its values.
3.  The Actions section shows details on the actions, flows, or subflows that are run during this loop iteration.

**Parent Topic:**[Workflow Studio flow logic](flow-logic.md)

**Related topics**  


[Assign subflow outputs flow logic](flow-logic-assign-subflow-outputs.md)

[Call a workflow flow logic](flow-logic-call-workflow.md)

[Do the following in parallel flow logic](flow-logic-do-following-in-parallel.md)

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

