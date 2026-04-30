---
title: Use the Show component
description: Display custom messages as part of a Attended Robot automation by using the Show component in the RPA Desktop Design Studio
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Show component

Display custom messages as part of a Attended Robot automation by using the Show component in the RPA Desktop Design Studio

## Before you begin

Role required: none

## About this task

For example, in an assisted automation, a component could evaluate a user input and show a message `Incorrect Date of Birth` through the Show component.

You can configure the properties for the Show component. For more information about these properties, see [Properties of the General components](../reference/Properties-general-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **MessageBox**.

2.  Drag the Show component to the Design surface.

3.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Show component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |Data in|Message|String|Takes the custom message that the component shows.|Yes|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[General](../concept/general-component.md)

