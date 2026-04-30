---
title: Use the GetProperty component
description: Get the value of a property from a JSON object by using the GetProperty component in the RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [JSON, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the GetProperty component

Get the value of a property from a JSON object by using the GetProperty component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

To configure the properties for the GetProperty component, see [Properties of the JSON utilities](../reference/properties-utilities-json.md).

## Procedure

1.  In the Toolbox pane, navigate to **General** and drag the Variable component to the Design surface.

2.  Double-click the variable and enter a code as a variable.

    For example,

    ```
    {
      "name": "Abel Tutor",
      "age": 30,
      "email": "abletutor@example.com",
    }
    
    ```

3.  In the Toolbox pane, navigate to **Utilities** &gt; **JSON**.

4.  Drag the GetProperty component to the Design surface.

5.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

6.  Connect the ports as described in the following table.

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

The JSON object from which to extract a property value.

</td></tr><tr><td>

Data In

</td><td>

PropertyName

</td><td>

String

</td><td>

The name of the property whose value is to be retrieved.

</td></tr><tr><td>

Data Out

</td><td>

Return

</td><td>

Object

</td><td>

Returns the value of the property.If no property value is found, the port return an error.

</td></tr></tbody>
</table>7.  To test the component, right-click the component bar and click **Run From Here**.

    The name is displayed as Abel Tutor when you right-click the GetProperty Data Out port.

    ![Example of GetProperty component.](../image/get-property-utlities-json-example.png "GetProperty component automation example")


**Parent Topic:**[JSON](../concept/json.md)

