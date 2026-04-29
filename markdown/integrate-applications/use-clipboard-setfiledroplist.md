---
title: Use the SetFileDropList component
description: Clear the clipboard and then add a collection of file names by using the SetFileDropList component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Clipboard, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the SetFileDropList component

Clear the clipboard and then add a collection of file names by using the SetFileDropList component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

A file drop list is a collection of strings that contain the file paths and is stored on the Windows clipboard as a String array.

You can configure the properties for the SetFileDropList component. For more information about these properties, see [Properties of the Clipboard components](../reference/util-clipboard-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Clipboard**.

2.  Drag the SetFileDropList component to the Design surface.

3.  To configure the input field, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the control ports of the SetFileDropList component to the corresponding ports of the other components.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Filenames\)|Passes the file names as string array from the Data Out component of another component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of any other component.|No. Connecting the port is optional.|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Clipboard](../concept/clipboard.md)

