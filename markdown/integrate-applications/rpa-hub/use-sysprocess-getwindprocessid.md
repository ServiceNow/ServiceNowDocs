---
title: Use the GetWindowProcessID component
description: Retrieve the window handle of a main window of an active process as an integer by using the GetWindowProcessID component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [System process, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the GetWindowProcessID component

Retrieve the window handle of a main window of an active process as an integer by using the GetWindowProcessID component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetWindowProcessID component. For more information about these properties, see [Properties of the System Process components](../reference/util-sysprocess-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **System Process**.

2.  Drag the GetWindowProcessID component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the GetWindowProcessID component to the corresponding ports of the other component as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(WindowHandle\)|Takes the Windows handle number as an integer from a previously executed component.|Yes|
    |Data Out \(\)|Returns the ProcessID value of the specified process as a String and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[System process](../concept/system-process-utilities.md)

