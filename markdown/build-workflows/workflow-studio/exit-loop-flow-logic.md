---
title: Exit Loop flow logic
description: Exit from a flow logic loop when the conditions of an If flow logic are met. Continue running the flow from the next step after the flow logic loop. This flow logic is also known as break.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Workflow Studio flow logic, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Exit Loop flow logic

Exit from a flow logic loop when the conditions of an If flow logic are met. Continue running the flow from the next step after the flow logic loop. This flow logic is also known as break.

## Valid Exit Loop placement

You can only add Exit Loop flow logic within certain portions of a flow. The Exit Loop flow logic must be within a branch of a parent For Each or Do the following until flow logic block.

-   Then branch of an If flow logic block
-   Then branch of an Else If flow logic block
-   Then branch of an Else flow logic block

## Inputs

This flow logic has no inputs.

## Outputs

This flow logic has no outputs.

## Execution Details

When a flow exits a loop, the state of the Exit Loop flow logic block becomes Completed. Any remaining steps in the For Each or Do the following until flow logic block aren’t run.

## Exit a loop based on incident count

In this example, a flow generates a list of incidents assigned to a user. For each incident that is assigned to the user, the flow sends an email. If the list of incidents is greater than or equal to 5, then the flow exits the For Each flow logic loop and doesn’t send an email.

![Exit Loop flow logic within an If flow logic then branch](../images/flow-logic-exit-loop.png)

In this example, there are 19 incidents assigned to the user, which meets the exit conditions. The first item of the For Each flow logic counter shows the Exit Loop flow logic having a state of Completed.

![Execution details of an Exit Loop flow logic](../images/flow-logic-exit-loop-execution-details.png)

**Parent Topic:**[Workflow Studio flow logic](../concept/flow-logic.md)

**Related topics**  


[Assign subflow outputs flow logic](../concept/flow-logic-assign-subflow-outputs.md)

[Call a workflow flow logic](../concept/flow-logic-call-workflow.md)

[Do the following until flow logic](../concept/flow-logic-do-until.md)

[Do the following in parallel flow logic](../concept/flow-logic-do-following-in-parallel.md)

[Dynamic flows flow logic](../concept/flow-logic-dynamic-flow.md)

[End Flow flow logic](../concept/flow-logic-end-action.md)

[For Each flow logic](../concept/flow-logic-for-each.md)

[Get Flow Outputs flow logic](get-flow-outputs-flow-logic.md)

[Go back to flow logic](go-back-to-flow-logic.md)

[If flow logic](../concept/flow-logic-if.md)

[Make a decision flow logic](../concept/flow-logic-make-decision.md)

[Set Flow Variables flow logic](../concept/flow-logic-set-flow-variables.md)

[Skip Iteration flow logic](skip-iteration-flow-logic.md)

[Try flow logic](../concept/flow-logic-try.md)

[Wait for a duration flow logic](../concept/flow-logic-wait-for-a-duration.md)

