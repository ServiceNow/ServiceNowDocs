---
title: Use the SendKeys component
description: Simulate the actions of the standard Microsoft Windows supported keys on various applications and programs with the SendKeys component in the RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Keyboard, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the SendKeys component

Simulate the actions of the standard Microsoft Windows supported keys on various applications and programs with the SendKeys component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

The standard Microsoft Windows keyboard provides many keyboard functions to perform various day-to-day tasks quickly and efficiently. For example, **\[Alt+A\]** can select all content on a file.

**Note:** You must specify the keyboard shortcuts within the square brackets \[\]. For example, \[Ctrl+A\].

To see the various supported keys, see [Supported keys and functions](../reference/supported-keys-and-functions.md).

You can configure the properties for the SendKeys component. For more information about these properties, see [Properties of keyboard components](../reference/properties-of-keyboard-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Keyboard**.

2.  Drag the SendKeys component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the SendKeys component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |Data In|keys|String|Takes keys that perform an action on the application.|Yes|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Keyboard](../concept/keyboard-utilities.md)

