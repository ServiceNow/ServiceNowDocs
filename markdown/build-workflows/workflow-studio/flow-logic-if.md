---
title: If flow logic
description: Selectively apply one or more actions only when a list of conditions is met.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/flow-logic-if.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# If flow logic

Selectively apply one or more actions only when a list of conditions is met.

Use this flow logic by specifying conditions that are based on the current record. Actions or subflows can be added to the flow within the if flow logic. The flow only runs the actions within this flow logic when the conditions evaluate to true. You build conditions based on data in records, such as the value of a task state or urgency.

**Note:** When you set a data pill value from inside a Then branch of If flow logic, the data pill value is only available to other actions in the same branch. Referencing a data pill value that was set inside a Then branch from outside of the flow logic branch produces a null value.

## Nested If flow logic blocks

You can add a child If flow logic block to a parent If flow logic block. Add the child If flow logic block to the Then branch of the parent flow logic block.

\[Omitted image "example-nested-if-flow-logic.png"\] Alt text: Example flow with one If flow logic block inside another If flow logic block.

## Inputs

|Input|Description|
|-----|-----------|
|Condition label|Descriptive label for the conditions of branch. A label can be easier to read than a long or complex condition data pill value.|
|Condition|Conditions under which the branch runs. The flow only runs the contents of the Then branch when the conditions evaluate to true.|

## Outputs

This flow logic has no outputs.

## Perform an action on if an incident has a high urgency

In this example, the action is triggered when the incident record has a high urgency value.

\[Omitted image "flow-logic-if.png"\] Alt text: Example If branch.

## Execution details

\[Omitted image "ex-details-if.png"\] Alt text: Execution details for an if branch.

1.  The header shows the state, start time, and runtime for the flow logic.
2.  The Configuration Details section shows the details about the variables that are used by the flow, including the type, configuration, and runtime values for each variable. Use the *condition* variable to see if the branch conditions were met.

## General guidelines

Use these general guidelines to create effective If flow logic blocks.

-   **Avoid referring to data pill values outside of the Then branch**

    When you set a data pill value from inside a Then branch of If flow logic, the data pill value is only available to other actions in the same branch. Referencing a data pill value that was set inside a Then branch from outside of the flow logic branch produces a null value.

-   **Group matching condition types in their own condition sets**

    Mixing conditions of different types for the same field values can produce unexpected results. For example, adding an AND condition to a group of multiple OR conditions for an incident short description can produce a situation where the If condition never evaluates to true. Use condition groups to group similar condition types for the same field. For example, group all OR conditions for an incident short description in one condition set and group all AND conditions for an incident short description in another condition set.

    \[Omitted image "example-condition-set-groups-if-conditions.png"\] Alt text: Example conditions sets. The first condition set has three or conditions, and the second condition set has two and conditions.

    \[Omitted image ""\] Alt text:

-   **Replace multiple If flow logic blocks with a Make a decision flow logic block**

    Rather than create duplicate If flow logic blocks that only vary by their conditions, use a decision table to generate an answer. For example, suppose you want to use the incident category to set the assignment group of an incident task record. Rather than create a duplicate If flow logic block for each category value, use the Make a decision flow logic to provide an answer for the assignment group.

    Here is an example flow that uses three If flow logic blocks that each create an incident task record. The only difference between the If flow logic blocks are the conditions of the incident category.

    \[Omitted image "example-multiple-ifs-before-conversion-decision.png"\] Alt text: Example flow containing three If flow logic blocks. Each If block checks for an incident category value and creates an incident task assigned to a matching group.

    Here is an example flow that uses a single Make a decision flow logic block to determine the incident task assignment group from the incident category. The Create task action uses the output of the decision as an input.

    \[Omitted image "example-multiple-ifs-after-conversion-decision.png"\] Alt text: Example flow containing a Make a decision flow logic block to determine the assignment by category. There is one Create Task action rather than three.

    Here is an example decision table that uses incident record values as an input. The Conditions column consists of two incident category values. The results column consists of the assignment group to use for each condition value.

    \[Omitted image "example-decision-table-get-assignment-group-from-category.png"\] Alt text: Example decision table with a conditions column for incident category and a results column for assignment group.


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

[Make a decision flow logic]()

[Set Flow Variables flow logic]()

[Skip Iteration flow logic]()

[Try flow logic]()

[Wait for a duration flow logic]()

