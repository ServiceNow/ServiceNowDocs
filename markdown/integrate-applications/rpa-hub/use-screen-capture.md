---
title: Use the Capture component
description: Capture a screen or a window in the desktop or an application as part of an automation Workflow using the Capture component in the RPA Desktop Design Studio .
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Screen, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Capture component

Capture a screen or a window in the desktop or an application as part of an automation Workflow using the Capture component in the RPA Desktop Design Studio .

## Before you begin

Role required: none

## About this task

You can configure the properties for the Capture component. For more information about these properties, see [Properties of the Screen components](../reference/util-screen-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Screen**.

2.  Drag the Capture component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Capture component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |Data in|Mode|Not applicable|Takes the input on whether the component captures a screen or a window.|Yes|
    |Data out|Return|Bitmap|Returns the image of the screen or window.|Not applicable|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Screen](../concept/screen.md)

