---
title: Exit Loop flow logic
description: Exit from a flow logic loop when the conditions of an If flow logic are met. Continue running the flow from the next step after the flow logic loop. This flow logic is also known as break.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/exit-loop-flow-logic.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
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

\[Omitted image "flow-logic-exit-loop.png"\] Alt text: Exit Loop flow logic within an If flow logic then branch

In this example, there are 19 incidents assigned to the user, which meets the exit conditions. The first item of the For Each flow logic counter shows the Exit Loop flow logic having a state of Completed.

\[Omitted image "flow-logic-exit-loop-execution-details.png"\] Alt text: Execution details of an Exit Loop flow logic

**Parent Topic:**[Workflow Studio flow logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-logic.md)

**Related topics**  


[Append to Flow Variables flow logic]()

[Assign subflow outputs flow logic]()

[Call a workflow flow logic]()

[Do the following until flow logic]()

[Do the following in parallel flow logic]()

[Dynamic flows flow logic]()

[End Flow flow logic]()

[For Each flow logic]()

[Get Flow Outputs flow logic]()

[Go back to flow logic]()

[If flow logic]()

[Make a decision flow logic]()

[Set Flow Variables flow logic]()

[Skip Iteration flow logic]()

[Try flow logic]()

[Wait for a duration flow logic]()

