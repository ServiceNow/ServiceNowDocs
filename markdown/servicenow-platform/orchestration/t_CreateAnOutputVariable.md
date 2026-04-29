---
title: Create an output variable
description: The Outputs form in the designer contains a variable builder for creating data structures of objects and arrays.Output variables contain messages returned from a destination that are available to other activities in a workflow or internally to the activity.Mapping is configured with parsing rules that allow you to build expressions in the appropriate data format for the selected payload.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create custom activities using custom activity designer templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an output variable

The **Outputs** form in the designer contains a variable builder for creating data structures of objects and arrays.

## Before you begin

Roles required: activity\_admin, activity\_creator

## About this task

Elements in this structure are mapped with [Create a parsing rule](t_CreateAParsingRule.md#) to specific data contained in payloads returned from an endpoint or host. These variables and their values are then made available locally or for reuse in other activities.

## Procedure

1.  Click the **+** icon in the **Outputs** column to create a local or output variable.

    Local variables are only available within an activity and are not visible in the data structures displayed in the **Custom** tab. Output variables are available for reuse in other activities, either individually or as an entire data structure. When you create a new variable of either type, the designer provides a default name of **Local1** or **Output1**.

2.  Type your new variable name in the field and select a data type.

    Variable names must be unique within an array or an object. You can assign a data type of **Encrypted** to output variables that contain sensitive data. Data protected by encryption is passed to other activities or processes encrypted and is never displayed in plain text.

3.  To change the name of a variable or any of its attributes, double-click the value, type a new value in the editing field, and then press **Enter**.

    The icon to the left of the name reflects the data type of the variable.

4.  To reorder the variable list, select a row and then drag the row to its new location.

    When you select a row to move it, the pointer icon changes to an up/down arrow icon \(![Up/down arrow icon.](../image/MoveVariable.png)\).

5.  Drag the row into another location.

6.  Choose from the following options.

    -   To reuse a variable from another activity, drag it from the **Custom** tab in the palette to the **Local** or **Output** heading at the top of the variable list.
    -   To copy an entire data structure, drag the parent object or array into the variable list header.
    The designer duplicates the copied data structure in the outputs variable builder.

    ![Reusing an output variable](../image/OutputsReuseVariable.png "Reuse of data structures")

7.  To delete a variable, click the delete icon \(![delete icon](../image/DeleteVar.png)\) in the row.


**Parent Topic:**[Create custom activities using custom activity designer templates](create-custom-activities.md)

## Activity designer template outputs

Output variables contain messages returned from a destination that are available to other activities in a workflow or internally to the activity.

|Field|Description|
|-----|-----------|
|Variable name|Name of a variable, either **Local** or **Output**, that this activity passes.|
|Local|Variable that contains a value used within an activity. For example, use a local variable to identify metadata that is processed within an activity before the final value is exported to an output variable.|
|Output|Variable that contains a value that is passed to other activities in the workflow.|

## Map an output field

Mapping is configured with parsing rules that allow you to build expressions in the appropriate data format for the selected payload.

### Before you begin

Role required: activity\_admin, activity\_creator

### About this task

When you are finished creating the output data structure, map each variable to the specific data you want to extract from the target host.

### Procedure

1.  To map a variable, drag it from the **Outputs** variable builder and drop it into an empty **Variable name** field in the Parsing rules section.

    See [create a parsing rule](t_CreateAParsingRule.md#) for instructions on configuring parsing for output variables.

    ![Mapping an output field](../image/OutputsMappingVariable.png)


