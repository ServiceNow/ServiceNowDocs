---
title: Do the following until flow logic
description: Apply one or more actions repeatedly until an end condition is met. You can use the flow data to specify the end conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/flow-logic-do-until.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
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

\[Omitted image "do-until-example-1.png"\] Alt text: Example Do the following until flow.

## Execution details

\[Omitted image "ex-details-do-until.png"\] Alt text: Example execution details for a do until flow.

1.  The header shows the state, start time, and runtime for the flow logic.
2.  This flow logic can run actions or subflows multiple times until it's condition is met. Use the arrow icons to select an iteration and its values.
3.  The Actions section shows details on the actions, flows, or subflows that are run during this loop iteration.

**Parent Topic:**[Workflow Studio flow logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-logic.md)

**Related topics**  


[Append to Flow Variables flow logic]()

[Assign subflow outputs flow logic]()

[Call a workflow flow logic]()

[Do the following in parallel flow logic]()

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

