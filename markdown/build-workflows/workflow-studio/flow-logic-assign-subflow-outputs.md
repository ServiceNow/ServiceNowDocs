---
title: Assign subflow outputs flow logic
description: Specify the data the subflow returns when it completes running. Use subflow output as data for a parent flow or as input for another process.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Assign subflow outputs flow logic

Specify the data the subflow returns when it completes running. Use subflow output as data for a parent flow or as input for another process.

**Important:** This flow logic sets values for flow outputs that have already been created. For instructions on creating flow outputs, see [Building subflows](subflows.md).

## Inputs

<table id="table_m4w_ktt_jnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the output. Select from the list of outputs available for the flow.

</td></tr><tr><td>

Data

</td><td>

Value for the output. Enter a string value, input a script, or use a data pill. Output values can reference any data pill from earlier in the flow, including other outputs. If you set outputs values by reference to other data pills, you must maintain the order of the output assignments. The referenced value must always come before the output that uses the referenced value. Changing the order may produce null values. To assign an empty value, leave this field empty.**Note:** Flow output values are set in the order in which they are assigned from top to bottom. If you set the value of the same output multiple times, the flow only uses the last value set.

</td></tr></tbody>
</table>## Outputs

This flow logic produces no outputs of its own, but it does set values in the **Subflow Outputs** section of the Data pane.

## Set the output code of a Delete Record action

In this example, the flow uses the Sys ID of a dashboard to look up a record, delete the record, and then return the action status code of the delete operation. The subflow assigns the output value of the Output code flow variable.

![Assign Subflow Outputs example](../images/flow-logic-assign-subflow-outputs-example.png "Assign Subflow Outputs flow logic inputs")

## Design considerations

Follow these design considerations when assign output values from a subflow.

-   **Do not assign subflow output values within loops**

    Subflow outputs are intended to be static values generated at the completion of the subflow. Loops do not have access to subflow output values while the subflow is running. Assigning subflow output values within a loop can produce unexpected results such as the loop only receiving the last value set. If you need to generate dynamic values that change within a For each or Do until loop, use flow variables instead.


**Parent Topic:**[Workflow Studio flow logic](flow-logic.md)

**Related topics**  


[Append to Flow Variables flow logic](../reference/append-to-flow-variables-flow-logic.md)

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

[Try flow logic](flow-logic-try.md)

[Wait for a duration flow logic](flow-logic-wait-for-a-duration.md)

