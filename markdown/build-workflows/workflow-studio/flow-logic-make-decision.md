---
title: Make a decision flow logic
description: You can use the decision table branching logic in situations where multiple conditional paths are required, as an alternative to nested If, Else If, or Else flow logic. For example, if you want to determine what kind of car insurance you need, you can add inputs such as your age, accident history, and car model to the decision table to determine a level of insurance coverage. This logic can save you time and present a more readable format than nested if conditions or switch case statements.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Make a decision flow logic

You can use the decision table branching logic in situations where multiple conditional paths are required, as an alternative to nested If, Else If, or Else flow logic. For example, if you want to determine what kind of car insurance you need, you can add inputs such as your age, accident history, and car model to the decision table to determine a level of insurance coverage. This logic can save you time and present a more readable format than nested if conditions or switch case statements.

The **Make a decision** flow logic requires that you create an external decision table for its branch paths. Each decision table answer produces a separate branch path within your flow. Decision tables accept any number of inputs and support any number of decisions. You can configure the Make a decision flow logic to return a single or multiple answers and to display the answers as branch paths or record data pills. For more information on decision tables, see [Exploring Decision Tables](../../decision-table/concept/decision-designer-overview.md).

**Note:**

-   When the **Use Branches** check box is cleared, the Make a decision data pills in other flow components is supported only if there are no branches.
-   The Make a decision data pill can be used in the answer branches only when the **Use Branches** check box is selected.​
-   When you set a data pill value from inside an answer branch of Make a decision flow logic, the data pill value is only available to other actions in the same branch. Referencing a data pill value that was set inside an answer branch from outside of the flow logic branch produces a null value.

## Inputs

<table id="table_m3l_b5l_p2b"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Decision Label

</td><td>

Descriptive label for the decision that you want to make. For example, you can create the `Recommended Insurance Policy` label if you want to determine the level of insurance coverage that you need. This value overrides the default action label.

</td></tr><tr><td>

Decision Table

</td><td>

Reference to a decision table \[sys\_decision\] record. This record provides the decision input answers that are available to the flow. To create a new decision table, select the create new record icon \(![Create new record icon](../images/add-record-button.png)\).

</td></tr><tr><td>

Execution

</td><td>

Decision answers you want the flow to run. -   **First decision that matches**: Run only the first matching decision answer. This option produces these outputs.
    -   Answer record
    -   Answer table
-   **Run all decisions that match**: Run all matching decision answers. This option produces these outputs.
    -   Answer table
    -   Ordered IDs
    -   Answer records
    -   Count

**Note:** Set the **Use Branches** option to specify how your flow displays matching decision answers.

</td></tr><tr><td>

Use Branches

</td><td>

Option to display each possible decision answer in its own branch flow logic block. Use the branch flow logic block to specify what content to run where the condition matches a specific decision table answer. Each branch flow logic block is equivalent to an If flow logic block for each answer. Disable branches when you want to return one or more answer records instead of branch flow logic blocks.

**Warning:** When you clear and confirm the **Use Branches** option, your flow removes the flow logic blocks for each branch and removes the **Include Otherwise** check box. Reselecting the **Use Branches** check box does not restore any removed branch flow logic blocks.

</td></tr><tr><td>

Include Otherwise

</td><td>

Option to add the **otherwise** branch to the list of available answers. This option is only available when **Use Branches** is selected. You can use this branch to specify the actions and subflows to run when the decision table does not generate an answer. An Otherwise branch is equivalent to an Else flow logic block. **Note:** If you specify a decision table default answer, this branch will never run because the decision table always selects an answer.

</td></tr><tr><td>

Decision table inputs

</td><td>

List of Decision Input \[sys\_decision\_input\] records that are associated with your decision table. Your flow displays a separate input for each record. For example, if you have decision inputs for `Units Ordered` and `Location of Sale`, an input displays for each record.

</td></tr></tbody>
</table>## Outputs

|Field|Description|Data Type|
|-----|-----------|---------|
|Answer table|Table containing the answer records. Each decision \[sys\_decision\_question\] table record refers to a matching answer record.|Table Name|
|Ordered IDs|List of matching answer record sys\_id values generated by the decision table. Your flow only generates this output when the **Use Branches** option is false and the **Execution** option is **Run all decisions that match**. You can use this output as the input for a For Each flow logic block or a Look Up Record action. Your flow sorts the list by the Order value listed in the Decision \[sys\_decision\_question\] table.|List|
|Answer records|Answer records returned by the decision table. Returns a single record when **Execution** is **First decision that matches**. Returns a list of records when Execution is **Run all decisions that match**.|Record or Records|
|Count|The number of answer records returned by the decision table. Only displayed when Execution is **Run all decisions that match**.|Integer|

## Use make a decision flow logic to determine insurance coverage

In this example, the flow uses a decision from the **Insurance Coverage** decision table, which an administrator had configured to determine the insurance coverage that was based on three inputs. The flow displays all the inputs that were used by the decision table. These inputs can be entered manually, or by dragging data pills into the inputs from the data panel on the right side of the screen. Below this section, the branches for each answer are shown in the decision table.

![Make a decision flow logic.](../images/example-make-decision-1.png)

## Execution details

![Example execution details for the make a decision flow logic.](../images/ex-details-make-decision.png "Make a decision flow execution details")

The **Flow execution details** tab provides runtime information about the flow logic.

1.  The header shows the state, start time, and runtime for the flow logic.
2.  The action shows details about the decision table configuration and inputs.
3.  Each possible answer for the decision table is represented as a branch. The state field indicates whether the branch was evaluated and the evaluation result. This section also displays details about the actions that are taken within a branch. Branches that evaluate to true are highlighted in green.

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

[Set Flow Variables flow logic](flow-logic-set-flow-variables.md)

[Skip Iteration flow logic](../reference/skip-iteration-flow-logic.md)

[Try flow logic](flow-logic-try.md)

[Wait for a duration flow logic](flow-logic-wait-for-a-duration.md)

