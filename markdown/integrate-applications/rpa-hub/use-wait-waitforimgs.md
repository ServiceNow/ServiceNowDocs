---
title: Use the Wait For Images component
description: Change the automation execution flow that is based on the image information on the screen by using the Wait For Images component in RPA Desktop Design Studio. You can also identify the state of a business application or an item that is based on an error or status icon.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Wait, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Wait For Images component

Change the automation execution flow that is based on the image information on the screen by using the Wait For Images component in RPA Desktop Design Studio. You can also identify the state of a business application or an item that is based on an error or status icon.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Wait For Images component. For more information about these properties, see [Properties of the Wait components](../reference/wait-properties.md).

## Procedure

1.  In the Toolbox pane, navigate to **Wait**.

2.  Drag the Wait For Images component to the Design surface.

3.  To add images, click the add image icon![add image icon.](../image/add-image-icon.png) on the Wait For Images component title bar.

4.  To capture the image that you want the component to find first, click the ![Camera icon](../image/camera-icon.png).

5.  To select a region, press the **CTRL+SHIFT** keys.

    You can add as many screenshots as you want by clicking the add image icon.

    The selected area is displayed in the Wait For Images component.

6.  Connect the data and control ports of the Wait For Images component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Else|Connects to the Control In port of any other component. You can define an exception if no images are found.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Dynamic Control Out|Connects to the Control In port of any other component. After you add more cases to the component, a control out port for every individual case is displayed.|Yes|

7.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Wait](../concept/wait.md)

