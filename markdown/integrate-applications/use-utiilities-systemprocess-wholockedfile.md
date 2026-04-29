---
title: Use the WhoLockedFile component
description: Provide a file path to find out the user name of the person who locked a file by using the WhoLockedFile component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System process, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the WhoLockedFile component

Provide a file path to find out the user name of the person who locked a file by using the WhoLockedFile component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the WhoLockedFile component. For more information about these properties, see [Properties of the System Process components](../reference/util-sysprocess-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities &gt; System Process**.

2.  Drag the WhoLockedFile component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the WhoLockedFile component to the corresponding ports of the other component as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(FilePath\)|Takes the file name from a previously executed component.|Yes|
    |Data Out \(Return\)|Returns the user name and passes to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[System process](../concept/system-process-utilities.md)

