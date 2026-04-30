---
title: Use the Number component
description: Generate any random number between two integers by using the Number component in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Random, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Number component

Generate any random number between two integers by using the Number component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the Number component. For more information about these properties, see [Properties of the Random components](../reference/properties-random-component.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Random**.

2.  Drag the Number component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the Number component to the corresponding ports of the other components.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Min\)|Takes the starting integer of the range from a previously executed component.|Yes|
    |Data In \(Max\)|Takes the ending integer of the range from a previously executed component.|Yes|
    |Data Out \(Return\)|Returns the random number and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|No. Connecting the port is optional.|
    |Control Out|Connects to the Control In port of another component or the default end component.|No. Connecting the port is optional.|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Random](../concept/random.md)

