---
title: Records.\[Table\] data type
description: Stores one or more Sys ID references to records in a specific table. The Records data format is also known as a Glide List since it stores a list of GlideRecord Sys ID values.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Workflow Studio input and output data variables, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Records.\[Table\] data type

Stores one or more Sys ID references to records in a specific table. The Records data format is also known as a Glide List since it stores a list of GlideRecord Sys ID values.

## Basic options

|Option|Description|
|------|-----------|
|Label|Displays the label used to identify the data variable in the Workflow Studio interface. The label can consist of any text.|
|Name|Displays the name used to identify the data variable in script calls. The name can only consist of alphanumeric and underscore characters. The system automatically converts the label into a valid name by removing or replacing any special characters.|
|Type|Indicates the type of data stored by the data variable.|
|Mandatory|Indicates whether the data variable must contain a value when configured in an action.|

## Advanced options

|Option|Description|
|------|-----------|
|Hint|Provides guidance to flow or action designers on how to configure the data.|
|Default value|Specifies the value used when a flow or action designer does not provide a value.|

## Script support

The records data type is supported in script by the GlideRecord class, which can produce an array containing one or more sys\_id values. For more information about the GlideRecord class and its available methods, see [GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

## Output of a Look Up Records action

![Execution details for a Look Up Records action](../images/example-look-up-records-action-execution-details.png)

The Look Up Records action uses the Records data type to store its results. In this example, the action looked up Configuration Item records assigned to the requester of a change request. Each configuration item record is a reference by its Sys ID. The flow execution details shows the configuration item display value, which in this case is the name.

**Parent Topic:**[Workflow Studio input and output data variables](action-inputs-outputs.md)

