---
title: Use the SetProperties component
description: Set multiple properties within a JSON object by using the SetProperties component in the RPA Desktop Design Studio. You can also override a property within the JSON object.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [JSON, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the SetProperties component

Set multiple properties within a JSON object by using the SetProperties component in the RPA Desktop Design Studio. You can also override a property within the JSON object.

## Before you begin

Role required: none

## About this task

To configure the properties of the SetProperties component, see [Properties of the JSON utilities](../reference/properties-utilities-json.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **JSON**.

2.  Drag the SetProperties component to the Design surface.

3.  Click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).

4.  Click the add property icon \(![Add property icon.](../image/add-image-icon.png)\).

5.  Enter the property name.

6.  Repeat the steps to add more property names.

7.  Click **OK**.

8.  To provide the values for the property names, see [Configure port properties](configure-input-port-properties.md).

9.  Connect the data and control ports of the SetProperties component to the corresponding ports of the other components as described in the following table.

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

The JSON object in which the properties are to be set.The properties that you set in this component are added to the JSON object.

</td></tr><tr><td>

Data In

</td><td>

Override

</td><td>

Boolean

</td><td>

Indicates whether to override properties, if they already exist. If True, the component overrides an existing property in the JSON object with the property that you specify. Else, if False, it doesn't override any property.

</td></tr><tr><td>

Data In

</td><td>

Name of the port is the same as the name of the property that you added in the component settings.

</td><td>

Object

</td><td>

Takes the value of the property name.

</td></tr><tr><td>

Data Out

</td><td>

Return

</td><td>

Object

</td><td>

Returns a JSON object with updated or new values for multiple properties.

</td></tr></tbody>
</table>10. To test the component, right-click the component bar and then click **Run From Here**.


**Parent Topic:**[JSON](../concept/json.md)

