---
title: List.\[Table\] data type
description: Stores a list of record Sys IDs associated to a specific table. This variable supports ServiceNow AI Platform List field options such as default records and reference qualifiers.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Input and output data variables, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# List.\[Table\] data type

Stores a list of record Sys IDs associated to a specific table. This variable supports ServiceNow AI Platform List field options such as default records and reference qualifiers.

## Basic options

|Option|Description|
|------|-----------|
|Label|Displays the label used to identify the data variable in the Workflow Studio interface. The label can consist of any text.|
|Name|Displays the name used to identify the data variable in script calls. The name can only consist of alphanumeric and underscore characters. The system automatically converts the label into a valid name by removing or replacing any special characters.|
|Type|Indicates the type of data stored by the data variable.|
|Mandatory|Indicates whether the data variable must contain a value when configured in an action.|

## Advanced options for List variables

|Option|Description|
|------|-----------|
|Hint|Provides guidance to flow or action designers on how to configure the data.|
|Default value|Specifies the value used when a flow or action designer does not provide a value.|
|Add \[Record Label\]|Select one or more records to include as default values for the list. If you filter the list with a reference qualifier, you can only select records that match the reference qualifier conditions.|
|Reference qualifier conditions|Select the filter conditions applied to the list of records. Flow designers can only select records that match the reference qualifier conditions.|

## General guidelines

-   **Add a reference qualifier to filter list records**

    Filter the records the list variable displays as valid options by adding a reference qualifier. The reference qualifier acts as a required list filter and causes the list variable to display only records that match the reference qualifier conditions. For example, to only displays active incident records add the reference qualifier condition **\[Active\]\[is\]\[true\]**.

-   **Avoid selecting default records for actions intended for ServiceNow Store**

    Avoid selecting default records for a list unless you know that all instances have access to the selected records. Spoke developers typically do not have access to the data of the customers who install their custom action. If you want to publish a custom action on the ServiceNow Store, you may need to provide default records as demo data.

-   **Use List variables in For Each flow logic**

    You can use a List variable to specify the records to process within For Each flow logic. The For Each flow logic ignores any non-record sys\_id present in the data. For example, if the List variable contains an email address, the flow logic ignores it.


**Parent Topic:**[Workflow Studio input and output data variables](action-inputs-outputs.md)

