---
title: Use the SetProperty component
description: Set a property within a JSON object by using the SetProperty component in the RPA Desktop Design Studio. You can also override a property within the JSON object.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [JSON, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the SetProperty component

Set a property within a JSON object by using the SetProperty component in the RPA Desktop Design Studio. You can also override a property within the JSON object.

## Before you begin

Role required: none

## About this task

To configure the properties of the SetProperty component, see [Properties of the JSON utilities](../reference/properties-utilities-json.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **JSON**.

2.  Drag the SetProperty component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the SetProperty component to the corresponding ports of the other components as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Port type

</th><th>

Port name

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data In

</td><td>

JsonObject

</td><td>

Object

</td><td>

The JSON object in which the property is to be set.The property that you set in this component is added to the JSON object.

</td></tr><tr><td>

Data In

</td><td>

PropertyName

</td><td>

String

</td><td>

The name of the property to set in the JSON object.

</td></tr><tr><td>

Data In

</td><td>

PropertyValue

</td><td>

String

</td><td>

The value to set for the specified property in the JSON object.

</td></tr><tr><td>

Data In

</td><td>

Override

</td><td>

Boolean

</td><td>

Indicates whether to override the property if it already exists. If True, the component overrides an existing property in the JSON object with the property that you specify. Else, if False, it doesn't override any property.

</td></tr><tr><td>

Data Out

</td><td>

Return

</td><td>

Object

</td><td>

Returns the JSON object with the updated or new property value.

</td></tr></tbody>
</table>5.  To test the component, right-click the component bar and then click **Run From Here**.


**Parent Topic:**[JSON](../concept/json.md)

