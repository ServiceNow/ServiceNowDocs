---
title: Use the TerminateByName component
description: Use the TerminateByName component to end the specified process or application, for example Chrome browser, Excel, Notepad, by its respective name.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System process, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the TerminateByName component

Use the TerminateByName component to end the specified process or application, for example Chrome browser, Excel, Notepad, by its respective name.

## Before you begin

Role required: none

## About this task

You can configure the properties for the TerminateByName component. For more information about these properties, see [Properties of the System Process components](../reference/util-sysprocess-prop.md).

During high density robots execution, the TerminateByName component checks and terminates the specified process or application only with in the current user session. When an automation runs on a virtual machine, it queries for the process and terminates it within the same user session of the robot. If the same process is running inside other user sessions on virtual machine, those process instances are not terminated.

**Note:** Within the current user session, if the robot user does not have permissions to terminate a process, component throws an error.

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **System Process**.

2.  Drag the TerminateByName component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the TerminateByName component to the corresponding ports of the other component as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In|Takes the process name of the process to terminate from a previously executed component. For example, Notepad.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of any other component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[System process](../concept/system-process-utilities.md)

