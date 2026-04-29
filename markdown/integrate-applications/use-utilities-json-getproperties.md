---
title: Use the GetProperties component
description: Get the values of multiple properties from a JSON object by using the GetProperties component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [JSON, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the GetProperties component

Get the values of multiple properties from a JSON object by using the GetProperties component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

To configure the properties of the GetProperties component, see [Properties of the JSON utilities](../reference/properties-utilities-json.md).

## Procedure

1.  In the Toolbox pane, navigate to **General** and drag the Variable component to the Design surface.

2.  Double-click the variable and enter a code as a variable.

    ```
    {
      "name": "Abel Tutor",
      "age": 30,
      "email": "abletutor@example.com",
    }
    
    ```

3.  In the Toolbox pane, navigate to **Utilities** &gt; **JSON**.

4.  Drag the GetProperties component to the Design surface.

5.  Click the component settings icon \(![Component settings icon.](../image/component-settings-icon.png)\).

6.  Click the Add property icon \(![Add keys icon.](../image/add-image-icon.png)\).

7.  Enter a property name.

8.  Repeat the steps to add multiple property names.

    A Data In port is added with each property that you add.

9.  Click **OK**.

10. To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

11. Connect the data and control ports of the GetProperties component to the corresponding ports of the other components as described in the following table.

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

The JSON object from which to extract property values. JSON object to be passed from the previous component.

Serialize the JSON and pass it from the previous component to get properties.

Example of JSON object:

```
{
  "name": "Abel Tutor",
  "age": 30,
  "email": "abletutor@example.com",
  "address": {
    "street": "123 Main St",
    "city": "New York",
    "state": "NY",
    "zip": "10001"
  },
  "phoneNumbers": [
    {
      "type": "home",
      "number": "555-1234"
    },
    {
      "type": "work",
      "number": "555-5678"
    }
  ],
  "isActive": true
}

```

</td></tr><tr><td>

Data Out

</td><td>

Name of the port is the same as the name of the properties that you added.

</td><td>

Object

</td><td>

Returns the values of the properties.If no property value is found, the port return an error.

</td></tr></tbody>
</table>12. To test the component, right-click the component bar and click **Run From Here**.


**Parent Topic:**[JSON](../concept/json.md)

