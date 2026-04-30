---
title: Use the SetText component
description: Copy a text string to the Windows clipboard as part of an automation Workflow by using the SetText component in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Clipboard, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the SetText component

Copy a text string to the Windows clipboard as part of an automation Workflow by using the SetText component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the SetText component. For more information about these properties, see [Properties of the Clipboard components](../reference/util-clipboard-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Clipboard**.

2.  Drag the SetText component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the SetText component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(strText\)|Passes the string through the Data Out port of another component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of any other component.|No. Connecting the port is optional.|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Clipboard](../concept/clipboard.md)

