---
title: Workflow Studio flow logic
description: Enable flows and subflows to specify conditional or repeated actions. Combine the elements of flow logic to create workflows in a graphical interface with little or no scripting.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Workflow Studio flow logic

Enable flows and subflows to specify conditional or repeated actions. Combine the elements of flow logic to create workflows in a graphical interface with little or no scripting.

The system provides these flow logic options.

|Flow logic option|Description|
|-----------------|-----------|
|Assign subflow outputs|Specify the data the subflow returns when it completes running. Use subflow output as data for a parent flow or as input for another process.|
|Call a Workflow|Run a published and active workflow from your flow. You can use the flow data as a workflow input. For example, you can specify the current record as a workflow input.|
|Do the following until|Apply one or more actions repeatedly until an end condition is met. You can use the flow data to specify the end conditions.|
|Do the following in parallel|Run actions and subflows in separate paths within an isolated flow logic block.|
|Dynamic Flow|Identify and run a flow or subflow dynamically by using runtime data. Build templates to provide expected inputs for dynamically called flows or subflows.|
|End Flow|Stop running the current flow. Use End Flow within a branch of the flow to specify an exit condition. For example, end the flow when it reaches a specific If flow logic block.|
|For each|Apply one or more actions to each record in a list of records.|
|Get Flow Outputs|Use this flow logic to access flow contexts and derive the runtime values for dynamic flow outputs.|
|If|Selectively apply one or more actions only when a list of conditions is met.|
|Make a decision|You can use the decision table branching logic in situations where multiple conditional paths are required, as an alternative to nested If, Else If, or Else flow logic. For example, if you want to determine what kind of car insurance you need, you can add inputs such as your age, accident history, and car model to the decision table to determine a level of insurance coverage. This logic can save you time and present a more readable format than nested if conditions or switch case statements.|
|Set Flow Variables|Assign a value to one or more flow variables, which store flow data as data pills. Access flow variable values by referring to their data pill.|
|Try|Allow a flow to continue running when an error occurs within a flow logic block. Run a sequence of actions in response to errors within the flow logic block.|
|Wait for a duration of time|Use this flow logic to give your users time to act during automated processes or to wait for a specific date and time to complete actions|

## Flow logic inputs

Each flow logic option displays one or more fields that are used to determine its behavior. For example, the **Call Workflow** flow logic has an input where you are able to select a workflow to run. Use these inputs to define the behavior of the flow and enable optional functionality depending on your needs. See flow logic option documentation for a list of the available inputs and how they control the function of that element.

## Flow logic outputs

Flow logic options may also have outputs. These represent information that is returned by the flow logic. For example, the **Make a decision** flow logic has an output that contains a decision answer record representing the decision reached by the flow. See the documentation for a flow logic option to see definitions for its outputs.

-   **[Assign subflow outputs flow logic](flow-logic-assign-subflow-outputs.md)**  
Specify the data the subflow returns when it completes running. Use subflow output as data for a parent flow or as input for another process.
-   **[Call a workflow flow logic](flow-logic-call-workflow.md)**  
Run a published and active workflow from your flow. You can use the flow data as a workflow input. For example, you can specify the current record as a workflow input.
-   **[Do the following until flow logic](flow-logic-do-until.md)**  
Apply one or more actions repeatedly until an end condition is met. You can use the flow data to specify the end conditions.
-   **[Do the following in parallel flow logic](flow-logic-do-following-in-parallel.md)**  
Run actions and subflows in separate paths within an isolated flow logic block.
-   **[Dynamic flows flow logic](flow-logic-dynamic-flow.md)**  
Identify and run a flow or subflow dynamically by using runtime data. Build templates to provide expected inputs for dynamically called flows or subflows.
-   **[End Flow flow logic](flow-logic-end-action.md)**  
Stop running the current flow. Use End Flow within a branch of the flow to specify an exit condition. For example, end the flow when it reaches a specific If flow logic block.
-   **[Exit Loop flow logic](../reference/exit-loop-flow-logic.md)**  
Exit from a flow logic loop when the conditions of an If flow logic are met. Continue running the flow from the next step after the flow logic loop. This flow logic is also known as break.
-   **[For Each flow logic](flow-logic-for-each.md)**  
Apply one or more actions to each record in a list of records.
-   **[Get Flow Outputs flow logic](../reference/get-flow-outputs-flow-logic.md)**  
Retrieve output values generated by dynamic flows or subflows.
-   **[Go back to flow logic](../reference/go-back-to-flow-logic.md)**  
Return to a prior step in the flow to repeat a sequence of actions.
-   **[If flow logic](flow-logic-if.md)**  
Selectively apply one or more actions only when a list of conditions is met.
-   **[Make a decision flow logic](flow-logic-make-decision.md)**  
You can use the decision table branching logic in situations where multiple conditional paths are required, as an alternative to nested If, Else If, or Else flow logic. For example, if you want to determine what kind of car insurance you need, you can add inputs such as your age, accident history, and car model to the decision table to determine a level of insurance coverage. This logic can save you time and present a more readable format than nested if conditions or switch case statements.
-   **[Set Flow Variables flow logic](flow-logic-set-flow-variables.md)**  
Assign a value to one or more flow variables, which store flow data as data pills. Access flow variable values by referring to their data pill.
-   **[Skip Iteration flow logic](../reference/skip-iteration-flow-logic.md)**  
Skip the current iteration of a flow logic loop when the conditions of an If flow logic are met. Continue running the flow logic loop with the next item in the list. This flow logic is also known as continue.
-   **[Try flow logic](flow-logic-try.md)**  
Allow a flow to continue running when an error occurs within a flow logic block. Run a sequence of actions in response to errors within the flow logic block.
-   **[Wait for a duration flow logic](flow-logic-wait-for-a-duration.md)**  
Use this flow logic to give your users time to act during automated processes or to wait for a specific date and time to complete actions.

**Parent Topic:**[Flows, subflows, and actions reference](../reference/flow-designer-reference.md)

