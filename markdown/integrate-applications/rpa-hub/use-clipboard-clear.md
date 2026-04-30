---
title: Use the Clear component
description: Clear the contents of the clipboard as part of an automation Workflow using the Clear component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Clipboard, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Clear component

Clear the contents of the clipboard as part of an automation Workflow using the Clear component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

The Clear component can work with other components or methods to execute an automation Workflow.

You can configure the properties for the Clear component. For more information about these properties, see [Properties of the Clipboard components](../reference/util-clipboard-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Clipboard**.

2.  Drag the Clear component to the Design surface.

3.  Connect the control ports of the Clear component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Control In|Passes the control from another component.|Yes|
    |Control Out|Connects to the Control In port of any other component.|No. Connecting the port is optional.|

4.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Clipboard](../concept/clipboard.md)

