---
title: Use the DeserializeObject component
description: Convert a string containing JSON data to a JSON object by using the DeserializeObject component in RPA Desktop Design Studio. You can also extract specific properties from the JSON object.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [JSON, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the DeserializeObject component

Convert a string containing JSON data to a JSON object by using the DeserializeObject component in RPA Desktop Design Studio. You can also extract specific properties from the JSON object.

## Before you begin

Role required: none

## About this task

To configure the properties for the DeserializeObject component, see [Properties of the JSON utilities](../reference/properties-utilities-json.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **JSON**.

2.  Drag the DeserializeObject component to the Design surface.

3.  To specify the required property name in the JSON object that you want to extract, do the following steps.

    1.  Click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).

    2.  Click the add property icon \(![Add properties icon.](../image/add-image-icon.png)\).

    3.  Enter a property name.

    4.  Repeat the steps to add multiple properties.

        A Data Out port is added with each key that you provide.

    5.  Click **OK**.

4.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

5.  Connect the data and control ports of the DeserializeObject component to the corresponding ports of the other components as described in the following table.

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

JSON

</td><td>

String

</td><td>

The string containing JSON data to be converted to a JSON object.

</td></tr><tr><td>

Data Out

</td><td>

Object

</td><td>

Object

</td><td>

The output parameter to store the converted JSON object.

</td></tr><tr><td>

Data Out

</td><td>

Name of the port is the same as the name of the key that you add.

</td><td>

Object

</td><td>

Returns the value of the key from the string.This appears when additional properties are added to the component settings.

</td></tr></tbody>
</table>6.  To test the component, right-click the component bar and then click **Run From Here**.


## Convert a string to a JSON object

![Convert string to object.](../image/Deserialize_example.PNG)

In this example, the ReadFromExcel component reads data from an Excel document and passes to the SerializeObject component. The SerializeObject component converts the data to string and passes to the DeserializeObject component. The DeserializeObject component converts the string to the JSON object. The items in the Excel document traverses from first to last in the For Each component and passes the item to the GetProperties component. The GetProperties component returns the name of the component and passes the name of the item to the Show component. The item is shown in a message box.

**Parent Topic:**[JSON](../concept/json.md)

