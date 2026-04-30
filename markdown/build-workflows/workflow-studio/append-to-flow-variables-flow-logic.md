---
title: Append to Flow Variables flow logic
description: Append a value to one or more array of objects flow variables. Use flow data to generate values.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-09-22"
reading_time_minutes: 5
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Append to Flow Variables flow logic

Append a value to one or more array of objects flow variables. Use flow data to generate values.

## Inputs

Provide a value for each input that your flow logic needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Name**

    Data type: **Flow Variable**

    Name of the array of objects flow variable that you want to append object values into. The drop down list only shows flow variables that are of type Array.Object.

-   **Data**

    Data type: **Array of Objects, Object, or flow variable data pill**

    Object or objects data pill containing the values that you want to append. If you use an existing object data pill, then the object schema must match that used by the flow variable. Alternatively, you can expand the schema of the flow variable and provide a flow variable data pill for each object property.


## Outputs

This flow logic produces no outputs of its own, but it does add object values to the Array.Object flow variable that you selected from the Data pane.

## General guidelines

Use these general guidelines when using the Append to Flow Variables flow logic.

-   **Create inputs or flow variables to provide data values**

    If you have an existing array of objects, you can use this array of objects as a subflow input. Alternatively, you can use one or more flow variables to create an array of objects within your flow. For example, you can save record values in a flow variable and then append the variables values to the objects within the array of objects.

-   **Define an array of objects flow variable**

    This flow logic depends on there being an array of objects flow variable. You must create an array of objects flow variable and that has the object schema structure that you want to update.

-   **Ensure that a data pill object schema matches a flow variable object schema**

    If you configure the Data input to use an existing object data pill, then the object schema must match that used by the flow variable. The flow logic can not append values to a flow variable object that has a different object schema.


## Build an array of incident objects

![The Append to Flow Variables flow logic is configured to append values to the incidents flow variable. The Sys ID and short description are set from two other flow variables.](../images/example-append-to-flow-variables-01.png)

In this example, a subflow looks up incidents where the category is Network. For each network incident, the subflow sets the value of the incident Sys ID and incident short description in a subflow variable. The subflow then appends these values to the array of objects subflow variable. The subflow then provides the array of objects as a subflow output.

![JSON output of the incidents array of objects showing five entries in the array.](../images/example-append-to-flow-variables-04.png)

The subflow execution details show that the output value of the incidents array of objects.

**Parent Topic:**[Workflow Studio flow logic](../concept/flow-logic.md)

**Related topics**  


[Assign subflow outputs flow logic](../concept/flow-logic-assign-subflow-outputs.md)

[Call a workflow flow logic](../concept/flow-logic-call-workflow.md)

[Do the following until flow logic](../concept/flow-logic-do-until.md)

[Do the following in parallel flow logic](../concept/flow-logic-do-following-in-parallel.md)

[Dynamic flows flow logic](../concept/flow-logic-dynamic-flow.md)

[End Flow flow logic](../concept/flow-logic-end-action.md)

[Exit Loop flow logic](exit-loop-flow-logic.md)

[For Each flow logic](../concept/flow-logic-for-each.md)

[Get Flow Outputs flow logic](get-flow-outputs-flow-logic.md)

[Go back to flow logic](go-back-to-flow-logic.md)

[If flow logic](../concept/flow-logic-if.md)

[Make a decision flow logic](../concept/flow-logic-make-decision.md)

[Set Flow Variables flow logic](../concept/flow-logic-set-flow-variables.md)

[Skip Iteration flow logic](skip-iteration-flow-logic.md)

[Try flow logic](../concept/flow-logic-try.md)

[Wait for a duration flow logic](../concept/flow-logic-wait-for-a-duration.md)

