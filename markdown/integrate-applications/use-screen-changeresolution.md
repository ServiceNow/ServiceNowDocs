---
title: Use the ChangeResolution component
description: Change the resolution of a user's system screen as part of an automation Workflow by using the ChangeResolution component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Screen, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the ChangeResolution component

Change the resolution of a user's system screen as part of an automation Workflow by using the ChangeResolution component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the ChangeResolution component. For more information about these properties, see [Properties of the Screen components](../reference/util-screen-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Screen**.

2.  Drag the ChangeResolution component to the Design surface.

3.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the ChangeResolution component to the corresponding ports of the other components as described in the following table.

    |Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------------------|----------|
    |Resolution|String|Takes the resolution of the user's system screen.|Yes|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Screen](../concept/screen.md)

