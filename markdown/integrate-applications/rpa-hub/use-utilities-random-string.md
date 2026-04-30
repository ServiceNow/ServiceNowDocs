---
title: Use the String component
description: Generate a random string by using the String component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Random, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the String component

Generate a random string by using the String component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the String component. For more information about these properties, see [Properties of the Random components](../reference/properties-random-component.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Random**.

2.  Drag the String component to the Design surface.

3.  Connect the data and control ports of the String component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Size\)|Takes the length of the string from a previously executed component.|Yes|
    |Data Out|Returns the random string and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|Yes|

4.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Random](../concept/random.md)

