---
title: Use the GetMainWindowHandle component
description: Retrieve the window handle of a main window of an active process by using the GetMainWindowHandle component in RPA Desktop Design Studio. This component accepts the Process ID as input and returns the Integer value of the specified process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/use-sysprocess-getmainwindhandle.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System process, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the GetMainWindowHandle component

Retrieve the window handle of a main window of an active process by using the GetMainWindowHandle component in RPA Desktop Design Studio. This component accepts the Process ID as input and returns the Integer value of the specified process.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetMainWindowHandle component. For more information about these properties, see [Properties of the System Process components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/util-sysprocess-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **System Process**.

2.  Drag the GetMainWindowHandle component to the Design surface.

3.  To configure the input fields, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-input-port-properties.md).

4.  Connect the data and control ports of the GetMainMainWindowHandle to the corresponding ports of the other component as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(ProcessId\)|Takes the process ID of the window as a string from a previously executed component.|Yes|
    |Data Out \(Integer\)|Returns the Windows handle of the specified process and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[System process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/system-process-utilities.md)

