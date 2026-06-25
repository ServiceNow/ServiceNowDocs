---
title: Map and Transform Data step
description: Map complex nested JSON objects to a target schema with dynamic field creation and data transformation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/map-transform-data-action.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-04-27"
reading_time_minutes: 2
breadcrumb: [Steps, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Map and Transform Data step

Map complex nested JSON objects to a target schema with dynamic field creation and data transformation.

## Roles and availability

Available as a Workflow Studio core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can drag pills from the Data panel or select them from the pill picker.

|Field|Description|
|-----|-----------|
|Source Data|Data type: JSON Object. The nested JSON object to map and transform. Drag-and-drop a JSON data pill or use the data pill picker to select the source object. The source can include multiple levels of nested objects and arrays.|
|Target|Data type: Object. The output structure for the transformed data. Select **Add field** to display options to create a target field and configure its mapping. The root label of the target defines the name of the output object. For example, to map a nested person object to user fields, set the root label to "user" and add fields for each element. You can map multiple source fields to a single target field to combine or transform data.|
|Scripted Fields|Data type: Script Objects. Optional custom transformations using JavaScript. Select **Add scripted field** to create a script object, define its name, select which source fields it uses, and write JavaScript code to perform transformations on those fields.|

## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

|Field|Description|
|-----|-----------|
|Target Object|Data type: Object. The transformed JSON object containing all mapped target fields with values from the source data and scripted field transformations. The object is named based on the target root label you configured.|
|Step Status|Data type: Object. Status information about the step execution, including success or failure indicators and error messages if any errors occurred during the transformation.|

## Example: Transform and flatten user data with field combinations

\[Omitted image "example-map-and-transform-data.png"\] Alt text: Example Map and Transform Data step.

In this example, a flow receives nested user data with a mix of simple and complex fields. The Map and Transform Data step transforms and combines source fields to create a simplified target structure.

The source data is a user object with the following structure:

-   user \(object\)
-   name \(string\)
-   age \(string\)
-   email \(object\)
    -   address \(string\)
    -   type \(string\)

The step configuration sets the target root label to "Root" and creates target fields that include field combinations:

-   name\_age \(combines name and age fields into a single target field\)
-   test \(also combines name and age fields for a different purpose\)
-   name\_name \(maps the name field\)
-   age \(maps the age field\)
-   email \(nested object containing address and type fields\)

The mapped source fields column shows the data pills for each mapping. For example, the name\_age field displays data pills showing both "name" and "age" selections. The transformation shows actual mapped values in real-time.

After the action runs, the Root output object contains all transformed fields with values combined and mapped. The Step Status output provides execution details. The transformed user data is ready for use in subsequent actions such as creating or updating user records.

**Parent Topic:**[Workflow Studio steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/steps.md)

