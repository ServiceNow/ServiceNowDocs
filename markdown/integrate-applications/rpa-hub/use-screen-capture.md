---
title: Use the Capture component
description: Capture a screen or a window in the desktop or an application as part of an automation Workflow using the Capture component in the RPA Desktop Design Studio .
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/integrate-applications/rpa-hub/use-screen-capture.html
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Screen, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Capture component

Capture a screen or a window in the desktop or an application as part of an automation Workflow using the Capture component in the RPA Desktop Design Studio .

## Before you begin

Role required: none

## About this task

You can configure the properties for the Capture component. For more information about these properties, see [Properties of the Screen components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/rpa-hub/util-screen-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Screen**.

2.  Drag the Capture component to the Design surface.

3.  To configure the input fields, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/rpa-hub/configure-input-port-properties.md).

4.  Connect the data and control ports of the Capture component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |Data in|Mode|Not applicable|Takes the input on whether the component captures a screen or a window.|Yes|
    |Data out|Return|Bitmap|Returns the image of the screen or window.|Not applicable|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/rpa-hub/screen.md)

