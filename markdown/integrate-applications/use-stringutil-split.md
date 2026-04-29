---
title: Use the Split component
description: Divide a string into substrings by applying a specified separator. You can do this task by using the Split component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the Split component

Divide a string into substrings by applying a specified separator. You can do this task by using the Split component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Split component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the Split component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Split component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Text\)|Takes the text that the component will be separating with the separator from a previously executed component.|Yes|
    |Data In \(separator\)|Takes the separator that the component uses to separate the string from a previously executed component.|Yes|
    |Data Out|Returns the substring of the string and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[String utilities](../concept/string-utilities.md)

