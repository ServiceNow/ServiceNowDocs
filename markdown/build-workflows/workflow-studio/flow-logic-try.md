---
title: Try flow logic
description: Allow a flow to continue running when an error occurs within a flow logic block. Run a sequence of actions in response to errors within the flow logic block.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Try flow logic

Allow a flow to continue running when an error occurs within a flow logic block. Run a sequence of actions in response to errors within the flow logic block.

## Inputs

Try flow logic does not have field inputs. Instead, it displays a plus \(![Add Action, Flow Logic, or Subflow after Icon](../images/add-action-icon.png)\) icon that enables you to add a sequence of actions, flow logic, or subflows to attempt to run and evaluate for errors. You can add multiple items to a Try block. When an error occurs, the flow runs the sequence of actions, flow logic, or subflows within the error section of the flow logic block.

## Outputs

This flow logic has no outputs, but the actions, flow logic, and subflows within the Try block may have outputs. When an error occurs within the Try flow logic block, the failing action returns an action status of **Completed \(error caught\)**. You can use this action status to determine which item failed and build conditional logic in the Catch block. For example, if a Create record action in the Try block has a status of Completed \(Error caught\), then run a Create record action in the Catch block that has different values.

## Create a Problem record for critical priority incidents

In this example, the flow attempts to send one of three possible notifications when a critical priority network incident is created. The flow first tries to send an SMS message, and if that fails, it tries to send a Connect message. If the Connect message fails, it sends an email.

![Example configuration of a Try flow logic block](../images/flow-logic-try-example.png "Try flow logic for multiple notification methods")

## Execution details

![Sample execution details of a Try flow logic block](../images/flow-logic-try-execution-details.png "Try flow logic execution details")

## Flow and action error handling resources

For more information about using error handling in actions and flows, see the ServiceNow® Community post [Flow and Action Error Handling Overview: Why and how to test for errors - Worfklow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-overview-why-and-how-to-test-for/ta-p/2877891).

-   [Flow and Action Error Handling Level 1: Retry and Action Error Evaluation - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-1-retry-and-action-error/ta-p/2877930)
-   [Flow and Action Error Handling Level 2: Flow Logic - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-2-flow-logic-workflow/ta-p/2877963)
-   [Flow and Action Error Handling Level 3: Flow Error Handling - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-3-flow-error-handling/ta-p/2877970)
-   [Flow and Action Error Handling Level 4: Good Practices and Summary - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/flow-and-action-error-handling-level-4-good-practices-and/ta-p/2877996)

**Parent Topic:**[Workflow Studio flow logic](flow-logic.md)

**Related topics**  


[Append to Flow Variables flow logic](../reference/append-to-flow-variables-flow-logic.md)

[Assign subflow outputs flow logic](flow-logic-assign-subflow-outputs.md)

[Call a workflow flow logic](flow-logic-call-workflow.md)

[Do the following until flow logic](flow-logic-do-until.md)

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

[Wait for a duration flow logic](flow-logic-wait-for-a-duration.md)

