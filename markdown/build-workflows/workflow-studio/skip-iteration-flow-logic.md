---
title: Skip Iteration flow logic
description: Skip the current iteration of a flow logic loop when the conditions of an If flow logic are met. Continue running the flow logic loop with the next item in the list. This flow logic is also known as continue.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Workflow Studio flow logic, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Skip Iteration flow logic

Skip the current iteration of a flow logic loop when the conditions of an If flow logic are met. Continue running the flow logic loop with the next item in the list. This flow logic is also known as continue.

## Valid Skip Iteration placement

You can only add Skip Iteration flow logic within certain portions of a flow. The Skip Iteration flow logic must be within a branch of a parent looping flow logic block such as For Each flow logic or Do the following until flow logic. In addition, the flow logic loop must define a set of conditions to skip an iteration. You can only add a Skip Iteration flow logic within a Then branch.

-   Then branch of an If flow logic block
-   Then branch of an Else If flow logic block
-   Then branch of an Else flow logic block

## Inputs

This flow logic has no inputs.

## Outputs

This flow logic has no outputs.

## Execution Details

When a flow skips an iteration, the Skip Iteration flow logic has a state of Completed for the item that was skipped. Any following steps in the same For Each or Do the following until flow logic loop have a status of Not Run for the skipped item.

## Skip iteration when an incident is an inquiry category

In this example, a flow generates a list of incidents assigned to a user. For each incident that is assigned to the user, the flow sends an email. If the current incident record is in the Inquiry/Help category, then the flow skips the current item. The flow continues with the next incident record in the For Each flow logic loop.

![Exit Loop flow logic within an If flow logic then branch](../images/flow-logic-exit-loop.png)

![Execution details of Skip Iteration flow logic](../images/flow-logic-skip-iteration-execution-details.png)

In this example, the first item is an incident in the Inquiry category, which meets the skip iteration conditions. The flow does not run the Send Email action for this iteration.

**Parent Topic:**[Workflow Studio flow logic](../concept/flow-logic.md)

**Related topics**  


[Assign subflow outputs flow logic](../concept/flow-logic-assign-subflow-outputs.md)

[Call a workflow flow logic](../concept/flow-logic-call-workflow.md)

[Do the following until flow logic](../concept/flow-logic-do-until.md)

[Do the following in parallel flow logic](../concept/flow-logic-do-following-in-parallel.md)

[Dynamic flows flow logic](../concept/flow-logic-dynamic-flow.md)

[End Flow flow logic](../concept/flow-logic-end-action.md)

[Exit Loop flow logic](exit-loop-flow-logic.md)

[For Each flow logic](../concept/flow-logic-for-each.md)

[Get Flow Outputs flow logic](get-flow-outputs-flow-logic.md)

[Go back to flow logic](go-back-to-flow-logic.md)

[If flow logic](../concept/flow-logic-if.md)

[Make a decision flow logic](../concept/flow-logic-make-decision.md)

[Set Flow Variables flow logic](../concept/flow-logic-set-flow-variables.md)

[Try flow logic](../concept/flow-logic-try.md)

[Wait for a duration flow logic](../concept/flow-logic-wait-for-a-duration.md)

