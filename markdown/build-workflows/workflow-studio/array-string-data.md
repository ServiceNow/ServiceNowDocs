---
title: Array.String data type
description: Store a sequence of alphanumeric text values in an array.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Input and output data variables, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Array.String data type

Store a sequence of alphanumeric text values in an array.

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

## Advanced options for String variables

|Option|Description|
|------|-----------|
|Max length|Specifies the maximum length a string value can have when entered from the user interface. The variable can store longer strings than it can display.|
|Hint|Provides guidance to flow or action designers on how to configure the data.|
|Default value|Specifies the value used when a flow or action designer does not provide a value.|

## Create a list of users who have a user role

![Execution details of a custom action that generates user names who have a specific role.](../images/array-strings-execution-details.png)

This example uses a custom action to generate a list of users who have a specific user role. To create the custom action to generate an array of strings, see [Create a custom action to generate an array of strings from a list of records](../task/create-custom-action-array-strings.md).

In this example, the users array contains three users who have the admin role.

```
{
    "users": [
        "System Administrator",
        "Rob Phillips",
        "Fred Luddy"
    ]
}

```

**Parent Topic:**[Workflow Studio input and output data variables](action-inputs-outputs.md)

