---
title: Go back to flow logic
description: Return to a prior step in the flow to repeat a sequence of actions.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-02-07"
reading_time_minutes: 5
breadcrumb: [Workflow Studio flow logic, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Go back to flow logic

Return to a prior step in the flow to repeat a sequence of actions.

## Family release requirements

You can only add Go back to flow logic to new flows created from the Washington DC family release and forward. Flows that were created in versions prior to the Washington DC family release do not support Go back to flow logic.

## Valid Go back to placement

You can only add Go back to flow logic within certain portions of a flow.

-   The Go back to flow logic must be within a branch of a parent flow logic block.
    -   Then branch of If, Else If, or Else flow logic
    -   Answer branch of Make a decision flow logic
    -   Catch branch of Try flow logic
-   The Go back to flow logic must be outside of the Error handler section.

## Valid Go back to target step

Go back to flow logic only allows you to select a valid return target step. A valid target step must meet all of these conditions.

1.  The target must be a step before the Go back to flow logic.
2.  The target can't be a step within a different branch of the flow.
3.  The target can't be a step within the same branch as the Go back to flow logic.
4.  The target can't be a step within a non-branching flow logic block unless the non-branching flow logic block also includes a child Go back to flow logic.
5.  The target can be a step outside of a non-branching flow logic block except for Do the following in parallel flow logic.

    **Warning:** Selecting a target step outside of a parent flow logic block exits the current loop and resets its loop iteration count. The system displays separate loop iteration counters for the Go back to loop and the parent flow logic block. All loops are limited by the maximum number of loop iterations property \(**sn\_flow\_designer.max\_iterations**\).


## Inputs

|Input|Description|
|-----|-----------|
|Go back to step|Step in the flow that meets the conditions of a Go back to step target.|

## Go back to start of flow

In this example, the flow goes back to the first step when the approval task for the trigger record is rejected. Valid Go back to targets include steps 1, 2, and 3. Step 4 violates rule 2 as it's a step within a different branch. Steps 5 and 6 violate rule 3 in that they're steps within the same branch of the flow.

![Sample flow demonstrating Go back to flow logic](../images/flow-logic-go-back-to-example.png)

![Go back to step menu displaying three choices for steps 1, 2, and 3.](../images/flow-logic-go-back-to-valid-targets.png)

## Outputs

This flow logic has no outputs.

## General guidelines

Use these general guidelines when adding Go back to flow logic.

-   **Add Go back to flow logic after the flow structure is complete**

    Go back to flow logic depends on a fixed sequence of steps to function properly. Wait to add Go back to flow logic until the flow has valid target steps.

-   **Avoid creating duplicate Go back to steps**

    A flow uses the first Go back to flow logic whose conditions are met. The flow ignores all Go back to flow logic steps after the first.

-   **Avoid creating infinite loops**

    Specify a condition to resume the flow or to throw an error with each Go back to loop. Error and resume conditions prevent a flow from running until it reaches the maximum number of loop iterations \(**sn\_flow\_designer.max\_iterations** property\). You can use an If flow logic to check for loop end conditions. For example, create a flow variable that counts how many times the flow has run the Go back to flow logic. When the flow variable reaches a limit, end the flow.

-   **Delete Go back to flow logic to move it**

    After you add Go back to flow logic, you can't move it to another location. You can only delete it from its current location and then add it to another valid location.


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

[If flow logic](../concept/flow-logic-if.md)

[Make a decision flow logic](../concept/flow-logic-make-decision.md)

[Set Flow Variables flow logic](../concept/flow-logic-set-flow-variables.md)

[Skip Iteration flow logic](skip-iteration-flow-logic.md)

[Try flow logic](../concept/flow-logic-try.md)

[Wait for a duration flow logic](../concept/flow-logic-wait-for-a-duration.md)

