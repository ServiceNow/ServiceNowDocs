---
title: Use the Move component
description: Move the mouse device to a precise location on the screen by specifying the parameters using the Move component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mouse, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Move component

Move the mouse device to a precise location on the screen by specifying the parameters using the Move component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Move component. For more information about these properties, see [Properties of the Mouse components](../reference/util-mouse-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Mouse**.

2.  Drag the Move component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Move component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Left\)|Takes the location relative to the left of the screen from a previously executed component.|Yes|
    |Data In \(Top\)|Takes the location relative to the top of the screen from a previously executed component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of any other component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Mouse](../concept/mouse-utility.md)

