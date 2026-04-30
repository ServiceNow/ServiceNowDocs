---
title: Use the Join component
description: Concatenate the elements of an array into a string by using the Join component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Join component

Concatenate the elements of an array into a string by using the Join component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can concatenate the elements of an array into a string by applying a specified separator such as dot, comma, or pipe. For example, if the string is \{“Apple”, “Banana”, “Orange”\} and separator is dot \(.\), then the concatenated string would be "Apple.Banana.Orange".

You can configure the properties for the Join component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the Join component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Join component to the corresponding ports of the other components as described in the following table.

    |Parameter name|Description|Data Port type|Data type|
    |--------------|-----------|--------------|---------|
    |StringArray|Specify a string array that you want to concatenate or use the string array from the previously executed component.|Data In|String\[\]|
    |Separator|The text separator that joins the arrays such as dot \(.\), comma \(,\), or pipe \(\|\).|Data In|String|
    |String|Returns concatenated string as an output that you can use in the next component.|Data Out|String|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[String utilities](../concept/string-utilities.md)

