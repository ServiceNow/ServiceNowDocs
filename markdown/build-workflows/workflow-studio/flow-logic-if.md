---
title: If flow logic
description: Selectively apply one or more actions only when a list of conditions is met.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Workflow Studio flow logic, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# If flow logic

Selectively apply one or more actions only when a list of conditions is met.

Use this flow logic by specifying conditions that are based on the current record. Actions or subflows can be added to the flow within the if flow logic. The flow only runs the actions within this flow logic when the conditions evaluate to true. You build conditions based on data in records, such as the value of a task state or urgency.

**Note:** When you set a data pill value from inside a Then branch of If flow logic, the data pill value is only available to other actions in the same branch. Referencing a data pill value that was set inside a Then branch from outside of the flow logic branch produces a null value.

## Nested If flow logic blocks

You can add a child If flow logic block to a parent If flow logic block. Add the child If flow logic block to the Then branch of the parent flow logic block.

![Example flow with one If flow logic block inside another If flow logic block.](../images/example-nested-if-flow-logic.png)

## Inputs

|Input|Description|
|-----|-----------|
|Condition label|Descriptive label for the conditions of branch. A label can be easier to read than a long or complex condition data pill value.|
|Condition|Conditions under which the branch runs. The flow only runs the contents of the Then branch when the conditions evaluate to true.|

## Outputs

This flow logic has no outputs.

## Perform an action on if an incident has a high urgency

In this example, the action is triggered when the incident record has a high urgency value.

![Example If branch.](../images/flow-logic-if.png)

## Execution details

![Execution details for an if branch.](../images/ex-details-if.png "Execution details for if flow logic")

1.  The header shows the state, start time, and runtime for the flow logic.
2.  The Configuration Details section shows the details about the variables that are used by the flow, including the type, configuration, and runtime values for each variable. Use the *condition* variable to see if the branch conditions were met.

## General guidelines

Use these general guidelines to create effective If flow logic blocks.

-   **Avoid referring to data pill values outside of the Then branch**

    When you set a data pill value from inside a Then branch of If flow logic, the data pill value is only available to other actions in the same branch. Referencing a data pill value that was set inside a Then branch from outside of the flow logic branch produces a null value.

-   **Group matching condition types in their own condition sets**

    Mixing conditions of different types for the same field values can produce unexpected results. For example, adding an AND condition to a group of multiple OR conditions for an incident short description can produce a situation where the If condition never evaluates to true. Use condition groups to group similar condition types for the same field. For example, group all OR conditions for an incident short description in one condition set and group all AND conditions for an incident short description in another condition set.

    ![Example conditions sets. The first condition set has three or conditions, and the second condition set has two and conditions.](../images/example-condition-set-groups-if-conditions.png "Example of grouping matching conditions into condition sets")

    ![]()

-   **Replace multiple If flow logic blocks with a Make a decision flow logic block**

    Rather than create duplicate If flow logic blocks that only vary by their conditions, use a decision table to generate an answer. For example, suppose you want to use the incident category to set the assignment group of an incident task record. Rather than create a duplicate If flow logic block for each category value, use the Make a decision flow logic to provide an answer for the assignment group.

    Here is an example flow that uses three If flow logic blocks that each create an incident task record. The only difference between the If flow logic blocks are the conditions of the incident category.

    ![Example flow containing three If flow logic blocks. Each If block checks for an incident category value and creates an incident task assigned to a matching group.](../images/example-multiple-ifs-before-conversion-decision.png "Example of multiple If flow logic blocks that do the same action")

    Here is an example flow that uses a single Make a decision flow logic block to determine the incident task assignment group from the incident category. The Create task action uses the output of the decision as an input.

    ![Example flow containing a Make a decision flow logic block to determine the assignment by category. There is one Create Task action rather than three.](../images/example-multiple-ifs-after-conversion-decision.png "Example of replacing multiple If flow logic blocks with a decision")

    Here is an example decision table that uses incident record values as an input. The Conditions column consists of two incident category values. The results column consists of the assignment group to use for each condition value.

    ![Example decision table with a conditions column for incident category and a results column for assignment group.](../images/example-decision-table-get-assignment-group-from-category.png "Example decision table Get Assignment Group from Category")


**Parent Topic:**[Workflow Studio flow logic](flow-logic.md)

**Related topics**  


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

[Make a decision flow logic](flow-logic-make-decision.md)

[Set Flow Variables flow logic](flow-logic-set-flow-variables.md)

[Skip Iteration flow logic](../reference/skip-iteration-flow-logic.md)

[Try flow logic](flow-logic-try.md)

[Wait for a duration flow logic](flow-logic-wait-for-a-duration.md)

