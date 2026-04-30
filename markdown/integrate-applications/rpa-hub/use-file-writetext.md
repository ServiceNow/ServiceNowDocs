---
title: Use the WriteText component
description: Append or overwrite existing text to an existing file or create a file and write text to it with the WriteText component in the RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [File, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the WriteText component

Append or overwrite existing text to an existing file or create a file and write text to it with the WriteText component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the WriteText component. For more information about these properties, see [Properties of the File components](../reference/util-file-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **File**.

2.  Drag the WriteText component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the WriteText component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(filePath\)|Takes the path to an existing or a new file and the file name from a previously executed component.|Yes|
    |Data In \(text\)|Takes the text to be written to the exiting file or new file from a previously executed component.|Yes|
    |Data Out|Returns **True** if the text is written to the file. Otherwise, it returns **False** and passes the Boolean output to the next component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No. Connecting the port is optional.|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[File](../concept/file.md)

