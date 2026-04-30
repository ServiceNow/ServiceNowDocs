---
title: Use the CopyDirectory component
description: Copy a directory to another location by using the CopyDirectory component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Directory, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the CopyDirectory component

Copy a directory to another location by using the CopyDirectory component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the CopyDirectory component. For more information about these properties, see [Properties of the Directory components](../reference/util-directory-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Directory**.

2.  Drag the CopyDirectory component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the CopyDirectory component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(SourceDirPath\)|Takes the path to the source directory from a previously executed component.|Yes|
    |Data In \(destDirPath\)|Takes the path to the destination directory from a previously executed component.|Yes|
    |Data In \(overwrite\)|Takes the Boolean value to indicate whether the method overwrites the directory in the destination folder from a previously executed component.|No|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No. Connecting the port is optional.|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Directory](../concept/directory.md)

