---
title: Array.Object data type
description: Store a sequence of JavaScript objects in an array.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Input and output data variables, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Array.Object data type

Store a sequence of JavaScript objects in an array.

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

## Advanced options for Object variables

<table id="table_vky_jd4_dlb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Structure

</td><td>

Specifies how to structure the object hierarchy. Options include: -   Create Structure Manually
-   Start from Template

 **Note:** Creating the structure manually enables the **Save as Template** option. Starting from a template enables the **Template** option

</td></tr><tr><td>

Save as Template

</td><td>

Stores a manually created object structure for later reuse.

</td></tr><tr><td>

Template

</td><td>

Specifies the existing object structure to apply to this object.

</td></tr></tbody>
</table>**Note:** For more information on using complex object variables, see [Complex data](../concept/complex-data.md).

## Create a list of contacts from a list of users

![Execution details of a custom action that generates a list of contacts from users in a department.](../images/array-objects-execution-details-contacts-array.png)

This example uses a custom action to generate a list of contacts details from users in a specific department. To create the custom action to generate an array of objects, see [Create a custom action to generate an array of objects from a list of records](../task/create-custom-action-array-objects.md).

In this example, the contacts array contains three users from the Development department.

```
{
    "contacts": 
        "contact": [
            {
                "email_address": "allyson.gillispie@example.com",
                "first_name": "Allyson",
                "last_name": "Gillispie"
            },
            {
                "email_address": "alva.pennigton@example.com",
                "first_name": "Alva",
                "last_name": "Pennigton"
            },
            {
                "email_address": "andrew.och@example.com",
                "first_name": "Andrew",
                "last_name": "Och"
            }
        ]
    }
}

```

**Parent Topic:**[Workflow Studio input and output data variables](action-inputs-outputs.md)

