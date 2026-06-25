---
title: Append to Flow Variables flow logic
description: Append a value to one or more array of objects flow variables. Use flow data to generate values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/append-to-flow-variables-flow-logic.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Flow logic, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
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

\[Omitted image "example-append-to-flow-variables-01.png"\] Alt text: The Append to Flow Variables flow logic is configured to append values to the incidents flow variable. The Sys ID and short description are set from two other flow variables.

In this example, a subflow looks up incidents where the category is Network. For each network incident, the subflow sets the value of the incident Sys ID and incident short description in a subflow variable. The subflow then appends these values to the array of objects subflow variable. The subflow then provides the array of objects as a subflow output.

\[Omitted image "example-append-to-flow-variables-04.png"\] Alt text: JSON output of the incidents array of objects showing five entries in the array.

The subflow execution details show that the output value of the incidents array of objects.

**Parent Topic:**[Workflow Studio flow logic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-logic.md)

**Related topics**  


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

[Skip Iteration flow logic]()

[Try flow logic]()

[Wait for a duration flow logic]()

