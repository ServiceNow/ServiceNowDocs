---
title: Use the Switch component
description: Find the exact match of a value among multiple values as part of an automation Workflow by using the Switch component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Conditions, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Switch component

Find the exact match of a value among multiple values as part of an automation Workflow by using the Switch component in RPA Desktop Design Studio.

Watch this video to learn how to use the Switch component.

How to use the Switch component. 

## Before you begin

Role required: none

## About this task

The Switch component enables you to set multiple values that are matched with the value that it takes from another component or method. It switches between values until it finds an exact match. If no match is found, it enables you to execute an alternate action.

The Switch component can work with other components or methods to execute an automation Workflow.

You can configure the properties for the Switch component. For more information on these properties, see [Properties of the Conditions components](../reference/conditions-properties.md).

## Procedure

1.  In the Toolbox pane, navigate to **Conditions** &gt; **Switch**.

2.  Drag the Switch component to the Design surface.

3.  To set the values for matching, do the following actions:

    1.  Click the add value icon \(![Add value icon.](../image/add-image-icon.png)\).

    2.  Repeat Step 3 to add as many fields for the values as you need.

        Data In ports are dynamically created to accept values.![Switch component example.](../image/switch-illustration.png)

    3.  To configure the input method to the fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Switch component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|
    |---------|---------|---------|---------------------|
    |Data In|Comparison Data|Object|Takes the value that is matched with the values set up in the component.|
    |Data In|Value|String|Takes the value that is matched with the value that is passed through the Comparison Data port.|
    |Data Out|ELSE|Not applicable|If there is no match, the component passes the control to the next component.|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Conditions](../concept/conditions-components.md)

