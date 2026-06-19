---
title: Use the GetResolution component
description: Get the resolution of the current screen by using the GetResolution component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-utilities-screen-getresolution.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Screen, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the GetResolution component

Get the resolution of the current screen by using the GetResolution component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

The properties of the GetResolution component are common with the properties of the other Screen components. To configure these properties, see [Properties of the Screen components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/util-screen-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Screen**.

2.  Drag the GetResolution component to the Design surface.

3.  Connect the data and control ports of the GetResolution component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |Data In|Return|String|Returns the resolution of the current screen.|Not applicable|

4.  To test the component, right-click the component bar and then click **Run From Here**.


## Display the current screen resolution in a message box

\[Omitted image "getresoluion-example.png"\] Alt text: Display the current screen resolution on a window.

The GetResolution component passes the current screen resolution through the Return Data Out port to the Show component. The Show component takes the resolution through its Message Data In port and is displayed in a message box.

**Parent Topic:**[Screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/screen.md)

