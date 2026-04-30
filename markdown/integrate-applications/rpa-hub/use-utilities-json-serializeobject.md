---
title: Use the SerializeObject component
description: Convert a JSON object to a string by using the SerializeObject component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [JSON, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the SerializeObject component

Convert a JSON object to a string by using the SerializeObject component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

To configure the properties for the SerializeObject component, see [Properties of the JSON utilities](../reference/properties-utilities-json.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **JSON**.

2.  Drag the SerializeObject component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the SerializeObject component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Description|
    |---------|---------|---------|-----------|
    |Data In|ObjData|Object|The JSON object to be converted to a string.|
    |Data Out|Return|String|Returns a JSON string which is representation of given object.|

5.  To test the component, right-click the component bar and then click **Run From Here**.


## Convert employee data from JSON object format to string

![Convert JSON object to string.](../image/serialize-object-example.png)

In this example, a JSON object contains the name, date of joining, and the salary of an employee. The JSON object is created by using the SetProperties component. To convert the JSON object to string, we use the SerializeObject component. After you run the automation, point the mouse device over the **Return** Data Out port of the SerializeObject component. The component displays the data as a string.

**Parent Topic:**[JSON](../concept/json.md)

