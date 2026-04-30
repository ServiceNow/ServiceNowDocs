---
title: Use the Scroll component
description: Simulate the scrolling by the mouse device on applications and programs using the Scroll component in the RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mouse, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Scroll component

Simulate the scrolling by the mouse device on applications and programs using the Scroll component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Scroll component. For more information about these properties, see [Properties of the Mouse components](../reference/util-mouse-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Mouse**.

2.  Drag the Scroll component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Scroll component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Left\)|Takes the position where the scrolling occurs relative to the left of the screen from a previously executed component.|Yes|
    |Data In \(Top\)|Takes the position where the scrolling occurs relative to the top of the screen from a previously executed component.|Yes|
    |Data In \(ScrollType\)|Takes the direction of scrolling from a previously executed component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of any other component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Mouse](../concept/mouse-utility.md)

