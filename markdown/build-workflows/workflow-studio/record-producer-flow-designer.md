---
title: Record Producer action
description: Create a Task record from a Record Producer Catalog Item \[sc\_cat\_item\]. The Task record inherits values from the catalog item's variable values.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Record Producer action

Create a Task record from a Record Producer Catalog Item \[sc\_cat\_item\]. The Task record inherits values from the catalog item's variable values.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

|Input|Data type|Description|
|-----|---------|-----------|
|Catalog Item|Record|Reference to catalog item used to create a Task record.|
|Catalog Item Inputs|String|Catalog variables associated with the catalog item you choose. You can view associated catalog variables for Catalog Items from **Service Catalog** &gt; **Catalog Definitions** &gt; **Record Producers**.|
|Don't fail on error|True/False|Catalog variable indicating whether to fail on error.|

## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

<table id="table_szc_rny_lnb"><thead><tr><th>

Output

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table Name

</td><td>

Table where Task record was created.

</td></tr><tr><td>

Record

</td><td>

Record

</td><td>

Reference to Task record created.

</td></tr><tr><td>

Error Message

</td><td>

String

</td><td>

Error message produced when the record operation fails.

</td></tr><tr><td>

Status

</td><td>

Choice

</td><td>

Completion status of the action. The flow execution details page displays one of these numeric values.-   Success \[0\]: The action succeeded.
-   Error \[1\]: The action produced an error.

</td></tr></tbody>
</table>## Error messages

If an error occurs with this action, the following error messages appear in the [execution details](../concept/flow-execution-details.md) page.

|Error message|Description|
|-------------|-----------|
|Record generation failed, check logs to get more information.|This error typically occurs when your flow or action contains logic to insert a record or records into other tables. When this logic exists, the Record Producer action aborts inserting the record into the table.|

## Design considerations

Follow these design considerations when creating flows that contain Record Producer actions.

-   **Escape quotation marks from string data pills with the String Replace transform function**

    Complex string variables are converted into JSON format when stored in the system. To prevent any JSON formatting errors, you can use a Replace String transform function to escape the quotation marks present in any string data pills you use for catalog variables. See [String transform functions](string-transform-functions.md).

-   **Use transform functions to validate data pills**

    Whenever you use a data pill to provide data for an action input, you can use a transform function to validate the data. See [Transform functions](../concept/transform-functions.md) for a list of available transform functions.


**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

