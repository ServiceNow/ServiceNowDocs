---
title: Skip Iteration flow logic
description: Skip the current iteration of a flow logic loop when the conditions of an If flow logic are met. Continue running the flow logic loop with the next item in the list. This flow logic is also known as continue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/skip-iteration-flow-logic.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
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

\[Omitted image "flow-logic-exit-loop.png"\] Alt text: Exit Loop flow logic within an If flow logic then branch

\[Omitted image "flow-logic-skip-iteration-execution-details.png"\] Alt text: Execution details of Skip Iteration flow logic

In this example, the first item is an incident in the Inquiry category, which meets the skip iteration conditions. The flow does not run the Send Email action for this iteration.

**Parent Topic:**[Workflow Studio flow logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-logic.md)

**Related topics**  


[Append to Flow Variables flow logic]()

[Assign subflow outputs flow logic]()

[Call a workflow flow logic]()

[Do the following until flow logic]()

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

[Try flow logic]()

[Wait for a duration flow logic]()

