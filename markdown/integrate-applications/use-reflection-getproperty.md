---
title: Use the GetProperty component
description: Access single or multiple properties of a given object at a time by using the GetProperty component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reflection, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the GetProperty component

Access single or multiple properties of a given object at a time by using the GetProperty component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the GetProperty component. For more information about these properties, see [Properties of the Reflection components](../reference/util-reflection-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Reflection**.

2.  Drag the GetProperty component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Click the add icon \(![Add icon.](../image/add-image-icon.png)\) on the GetProperty component title bar to add the additional parameters.

5.  Connect the data and control ports of the GetProperty component to the corresponding ports of the other components.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In|Connects to the Data Out port of another component from where the data is to be collected. The For Loop component exposes the From and To Data In ports.|Yes|
    |Dynamic Data Out|Connects to the Data In port of another component where the data is to be displayed. This port is displayed when you add items into the component.|No|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of any other component.|Yes|

6.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Reflection](../concept/reflection-utility.md)

