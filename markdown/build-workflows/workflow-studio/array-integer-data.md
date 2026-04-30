---
title: Array.Integer data type
description: Store a sequence of numeric integer data in an array.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow Studio input and output data variables, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Array.Integer data type

Store a sequence of numeric integer data in an array.

## Basic options

|Option|Description|
|------|-----------|
|Label|Displays the label used to identify the data variable in the Workflow Studio interface. The label can consist of any text.|
|Name|Displays the name used to identify the data variable in script calls. The name can only consist of alphanumeric and underscore characters. The system automatically converts the label into a valid name by removing or replacing any special characters.|
|Type|Indicates the type of data stored by the data variable.|
|Mandatory|Indicates whether the data variable must contain a value when configured in an action.|

## Advanced options for Array variables

|Option|Description|
|------|-----------|
|Hint|Provides guidance to flow or action designers on how to configure the data.|
|Max rows|Specifies the maximum number of entries to display in the Workflow Studio interface. The array can store more values than it displays.|

## Advanced options for Integer variables

|Option|Description|
|------|-----------|
|Hint|Provides guidance to flow or action designers on how to configure the data.|
|Default value|Specifies the value used when a flow or action designer does not provide a value.|

## Example

You can use an array of integers to store the output of a script method call. For example, the Fetch Document Approval Sequence action uses a script step to generate an approval sequence data pill. The script output variable stores the sequence of approvers as an array of integers.

![Script step that defines an output variable named Approver Sequence with the data type of Array.Integer](../images/example-script-output-array-integers.png "Script output of Fetch Document Approval Sequence action")

**Parent Topic:**[Workflow Studio input and output data variables](action-inputs-outputs.md)

