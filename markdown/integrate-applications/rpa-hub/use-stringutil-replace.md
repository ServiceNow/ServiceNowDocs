---
title: Use the Replace component
description: Replace all occurrences of a word in a text with another word by using the Replace component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [String utilities, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Replace component

Replace all occurrences of a word in a text with another word by using the Replace component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Replace component. For more information about these properties, see [Properties of the String Utilities components](../reference/util-stringutil-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **String Utilities**.

2.  Drag the Replace component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Replace component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Text\)|Takes the text where the component replaces a word or character from a previously executed component.|Yes|
    |Data In \(oldValue\)|Takes the text or character that the component replaces from a previously executed component.|Yes|
    |Data In \(newValue\)|Takes the text or character that the component replace the old text with from a previously executed component.|Yes|
    |Data Out \(String\)|Returns the text after replacing the specified word and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[String utilities](../concept/string-utilities.md)

