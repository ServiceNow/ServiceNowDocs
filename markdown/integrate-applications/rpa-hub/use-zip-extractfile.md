---
title: Use the ExtractFile component
description: Extract a file from a zip archive to a specified location by using the ExtractFile component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zip, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the ExtractFile component

Extract a file from a zip archive to a specified location by using the ExtractFile component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the ExtractFile component. For more information about these properties, see [Properties of the Zip components](../reference/util-zip-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Zip**.

2.  Drag the ExtractFile component to the Design surface.

3.  To configure the inputs, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the ExtractFile component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(zipFilePath\)|Provides the zipFilePath and PathtoExtract Data In ports to extract files to a location.|Yes|
    |Data In \(file\)|Takes the file name from a previously executed component.|Yes|
    |Data In \(filePath\)|Takes the file path from a previously executed component.|Yes|
    |Data Out|Returns **True** if the files are successfully extracted to the specified location. Otherwise, returns **False**.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Zip](../concept/zip-utilities.md)

