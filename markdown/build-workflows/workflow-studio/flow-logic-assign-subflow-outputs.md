---
title: Assign subflow outputs flow logic
description: Specify the data the subflow returns when it completes running. Use subflow output as data for a parent flow or as input for another process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/flow-logic-assign-subflow-outputs.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Assign subflow outputs flow logic

Specify the data the subflow returns when it completes running. Use subflow output as data for a parent flow or as input for another process.

**Important:** This flow logic sets values for flow outputs that have already been created. For instructions on creating flow outputs, see [Building subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/subflows.md).

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

\[Omitted image "flow-logic-assign-subflow-outputs-example.png"\] Alt text: Assign Subflow Outputs example

## Design considerations

Follow these design considerations when assign output values from a subflow.

-   **Do not assign subflow output values within loops**

    Subflow outputs are intended to be static values generated at the completion of the subflow. Loops do not have access to subflow output values while the subflow is running. Assigning subflow output values within a loop can produce unexpected results such as the loop only receiving the last value set. If you need to generate dynamic values that change within a For each or Do until loop, use flow variables instead.


**Parent Topic:**[Workflow Studio flow logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-logic.md)

**Related topics**  


[Append to Flow Variables flow logic]()

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

[Skip Iteration flow logic]()

[Try flow logic]()

[Wait for a duration flow logic]()

