---
title: End Flow flow logic
description: Stop running the current flow. Use End Flow within a branch of the flow to specify an exit condition. For example, end the flow when it reaches a specific If flow logic block.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# End Flow flow logic

Stop running the current flow. Use End Flow within a branch of the flow to specify an exit condition. For example, end the flow when it reaches a specific If flow logic block.

End Flow logic can be contained within a conditional flow logic block, such as an **If**, **Else If**, or **Else** flow logic block. Use this flow logic to stop a flow when certain conditions are met. You cannot add actions or flow logic after you use the **End Flow** flow logic. All branches of a flow are ended when a flow reaches the **End Flow** flow logic, including the **Wait for a duration** logic. Any branches that run in parallel also stop their progress when you use the **End Flow** flow logic.

## Inputs

This flow logic has no inputs.

## Outputs

This flow logic has no outputs. When this flow logic ends a flow or subflow, it sets the state to Completed. Subflows that end can only return an output value to a parent flow if there was an Assign subflow outputs flow logic prior to the End subflow flow logic.

## General guidelines

Use the general guidelines when adding an End flow or End subflow flow logic.

-   **Assign subflow outputs prior to End subflow flow logic**

    If a subflow always needs to return an output value to a parent flow, use an Assign Subflow Outputs flow logic prior to the End Subflow flow logic. By default, an ended subflow does not return any output values.

-   **Design parent flows to handle an ended subflow**

    If you call a subflow that has an end branch, make sure that the calling flow can handle not receiving subflow output. It is up to the flow and subflow author to pass data between flows.


## Request Ad hoc Approval subflow

![Subflow containing an End Subflow branch](../images/example-end-subflow-approval.png)

This example subflow supports adding arbitrary approvals from a Playbooks activity. The wait condition in steps 5 to 6 checks the flow data record for an end state such as cancelled, complete, error, or skipped. When the flow data record enters one of these states, the subflow ends without assigning any outputs.

![Execution details of subflow reaching the End branch.](../images/example-end-subflow-approval-execution-details.png)

When the subflow reaches this branch, it stops the subflow and sets the state to Completed. The actions in other branches are not run.

**Parent Topic:**[Workflow Studio flow logic](flow-logic.md)

**Related topics**  


[Append to Flow Variables flow logic](../reference/append-to-flow-variables-flow-logic.md)

[Assign subflow outputs flow logic](flow-logic-assign-subflow-outputs.md)

[Call a workflow flow logic](flow-logic-call-workflow.md)

[Do the following until flow logic](flow-logic-do-until.md)

[Do the following in parallel flow logic](flow-logic-do-following-in-parallel.md)

[Dynamic flows flow logic](flow-logic-dynamic-flow.md)

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

