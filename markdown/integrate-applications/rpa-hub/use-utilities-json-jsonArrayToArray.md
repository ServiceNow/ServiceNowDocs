---
title: Use the JsonArrayToArray component
description: Convert a JSON object to an array of objects using the JsonArrayToArray component in the RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [JSON, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the JsonArrayToArray component

Convert a JSON object to an array of objects using the JsonArrayToArray component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

To configure the properties for the JsonArrayToArray component, see [Properties of the JSON utilities](../reference/properties-utilities-json.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **JSON**.

2.  Drag the JsonArrayToArray component to the Design surface.

3.  In the Toolbox pane, navigate to **General** &gt; **Variable**.

4.  Drag the Variable component to the Design surface.

5.  Double-click the variable and enter a script.

    An example of a script.

    ```
    
    [{
    
      "name": "Abel Tutor",
    
      "age": 30,
    
      "email": "abletutor@example.com",
    
    },
    
    {
    
      "name": "Alex Tutor",
    
      "age": 32,
    
      "email": "alextutor@example.com",
    
    }]
     
    ```

6.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

7.  Connect the data and control ports of the JsonArrayToArray component to the corresponding ports of the other components as described in the following table and image.

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

The JSON object to be converted to an array of objects.

</td></tr><tr><td>

Data Out

</td><td>

Return

</td><td>

Object\[\]

</td><td>

Used to return an array of JObjects. Each JObject has the same set of properties with different values for each property.To modify the details of a JObject, iterate over the JObjects in the array returned until the criteria is met.

</td></tr></tbody>
</table>    ![JsonArrayToArray component extracts data from the script in the Variable component.](../image/json-array-to-array-rpa.png "JsonArrayToArray component with Variable component")

8.  To test the component, right-click the component bar and then click **Run From Here**.

9.  To view the complete data output, right-click the Data port of JsonArrayToArray component and select **Preview Data**.


## JsonArrayToArray component with Variable component

![Data preview of the JsonArrayToArray component after execution.](../image/json-arraytoarray-data-preview-rpa.png)

**Parent Topic:**[JSON](../concept/json.md)

