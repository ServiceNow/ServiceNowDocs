---
title: Use the Wait For Time component
description: Set a wait time by using the Wait For Time component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Wait For Time component

Set a wait time by using the Wait For Time component in RPA Desktop Design Studio.

Watch this video to learn how to use the Wait For Time component.

How to use the Wait For Time component. 

## Before you begin

Role required: none

## About this task

You can use the Wait For Time component anywhere in an automation. Depending on the wait time that you have configured, the automation waits after the component previous to the Wait For Time component is executed.

To configure the properties for the Wait For Time component, see [Properties of the Wait components](../reference/wait-properties.md).

## Procedure

1.  In the Toolbox pane, navigate to **General**.

2.  Drag the Wait For Time component to the Design surface.

3.  To set the wait time, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Wait For Time component to the corresponding ports of the other components as described in the following table.

    |Port Type|Port name|Data type|Purpose|Mandatory?|Notes|
    |---------|---------|---------|-------|----------|-----|
    |Data In|Wait Time \(Seconds\)|Integer|Takes the wait time.|Yes| |

5.  To test the component, right-click the component bar and then click **Run From Here**.


## Set a wait time in an automation

![Set a wait time in the automation.](../image/WaitForTime.PNG)

In the example, the WHILE component executes while the value of "i" is true. The Wait For Time component is placed between the While component and the Post Process component. The Wait For Time component puts a waiting time of 30 seconds before the Post Process component executes.

**Parent Topic:**[General](../concept/general-component.md)

