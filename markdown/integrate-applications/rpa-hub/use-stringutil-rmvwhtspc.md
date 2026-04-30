---
title: Use the RemoveWhiteSpace component
description: Remove any white spaces from a string by using the RemoveWhiteSpace component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the RemoveWhiteSpace component

Remove any white spaces from a string by using the RemoveWhiteSpace component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the RemoveWhiteSpace component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the RemoveWhiteSpace component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the RemoveWhiteSpace component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Text\)|Takes the text from which the component removes whitespace from a previously executed component.|Yes|
    |Data Out|Returns the string after removing the whitespaces and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[String utilities](../concept/string-utilities.md)

