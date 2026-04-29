---
title: Object data type
description: Store a JavaScript object.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Input and output data variables, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Object data type

Store a JavaScript object.

## Basic options

|Option|Description|
|------|-----------|
|Label|Displays the label used to identify the data variable in the Workflow Studio interface. The label can consist of any text.|
|Name|Displays the name used to identify the data variable in script calls. The name can only consist of alphanumeric and underscore characters. The system automatically converts the label into a valid name by removing or replacing any special characters.|
|Type|Indicates the type of data stored by the data variable.|
|Mandatory|Indicates whether the data variable must contain a value when configured in an action.|

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

**Parent Topic:**[Workflow Studio input and output data variables](action-inputs-outputs.md)

