---
title: Use the MoveFile component
description: Move a file from an existing location to a new location as part of an automation Workflow by using the MoveFile component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [File, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the MoveFile component

Move a file from an existing location to a new location as part of an automation Workflow by using the MoveFile component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the MoveFile component. For more information about these properties, see [Properties of the File components](../reference/util-file-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **File**.

2.  Drag the MoveFile component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the MoveFilecomponent to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(sourcefilePath\)|Takes the path to the source file from a previously executed component.|Yes|
    |Data IN \(destFilePath\)|Takes the path to the destination directory from a previously executed component.|Yes|
    |Data In \(Overwrite\)|Takes the Boolean value to indicate whether the method overwrites the same file in the destination directory from a previously executed component.|No|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No. Connecting the port is optional.|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[File](../concept/file.md)

