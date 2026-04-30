---
title: Reference.\[Table\] data type
description: Store a single Sys ID reference to a record in a specific table.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow Studio input and output data variables, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Reference.\[Table\] data type

Store a single Sys ID reference to a record in a specific table.

## Basic options

|Option|Description|
|------|-----------|
|Label|Displays the label used to identify the data variable in the Workflow Studio interface. The label can consist of any text.|
|Name|Displays the name used to identify the data variable in script calls. The name can only consist of alphanumeric and underscore characters. The system automatically converts the label into a valid name by removing or replacing any special characters.|
|Type|Indicates the type of data stored by the data variable.|
|Mandatory|Indicates whether the data variable must contain a value when configured in an action.|

## Advanced options for Reference variables

|Option|Description|
|------|-----------|
|Hint|Provides guidance to flow or action designers on how to configure the data.|
|Default value|Specifies the value used when a flow or action designer does not provide a value.|
|Reference qualifier conditions|Specifies the conditions used to filter records from the target table. The system only displays records from the target table that match the reference qualifier conditions. Use the condition builder to add one or more conditions.|

**Parent Topic:**[Workflow Studio input and output data variables](action-inputs-outputs.md)

