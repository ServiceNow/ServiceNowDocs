---
title: Use the SetProcessParameter component
description: Update the value of an existing process parameter you had set for a bot process in the RPA Hub with the SetProcessParameter component in the RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Process Parameters, RPA Hub, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the SetProcessParameter component

Update the value of an existing process parameter you had set for a bot process in the RPA Hub with the SetProcessParameter component in the RPA Desktop Design Studio.

## Before you begin

Set at least one process parameter as part of a bot process on the RPA Hub. See [Create a process parameter within a bot process in RPA Hub](../../rpa-hub/task/create-process-parameter-botprocess.md#).

Assign the automation to the bot process by using the **Assign bot process** option from the **Design** tab of RPA Desktop Design Studio. You must set the same bot process and robot associated with the process parameter. For more information, see [Assign bot process to an automation project](assign-bot-process.md).

Role required: none

## About this task

You can configure the properties for the SetProcessParameter component. For more information about these properties, see [Properties of the Process Parameters components](../reference/processprm-properties.md).

## Procedure

1.  In the Toolbox, navigate to **RPA Hub** &gt; **Process Parameters**.

2.  Drag the SetProcessParameter component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the SetProcessParameter component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Name\)|Takes the name of the process parameter you had set as part of the bot process on RPA Hub from a previously executed component.|Yes|
    |Data In \(Value\)|Takes the new value of the process parameter you had set as part of the bot process on RPA Hub from a previously executed component.|Yes|
    |Data Out|Returns the Boolean response to whether the process parameter value was updated and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|Yes|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Process Parameters](../concept/process-parameters.md)

