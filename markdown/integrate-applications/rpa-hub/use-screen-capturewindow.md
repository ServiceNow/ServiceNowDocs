---
title: Use the CaptureWindow component
description: Capture the image of an application window as part of an automation Workflow by using the CaptureWindow component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Screen, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the CaptureWindow component

Capture the image of an application window as part of an automation Workflow by using the CaptureWindow component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the CaptureWindow component. For more information about these properties, see [Properties of the Screen components](../reference/util-screen-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Screen**.

2.  Drag the CaptureWindow component to the Design surface.

3.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the CaptureWindow component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |Data in|Handle|Integer|Takes the handle of the window that the component captures.|Yes|
    |Data out|Return|Bitmap|Returns the image of the window the component has captured.|Not applicable|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Screen](../concept/screen.md)

