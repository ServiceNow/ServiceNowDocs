---
title: Use the ExtractAll component
description: Extract all the files from a zip archive to a specific location by using the ExtractAll component in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Zip, Utilities, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the ExtractAll component

Extract all the files from a zip archive to a specific location by using the ExtractAll component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the ExtractAll component. For more information about these properties, see [Properties of the Zip components](../reference/util-zip-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Zip**.

2.  Drag the ExtractAll component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the ExtractAll component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(zipFilePath\)|Takes the zipFilePath from a previously executed component.|Yes|
    |Data In \(PathToExtract\)|Takes the extraction path from a previously executed component.|Yes|
    |Data Out|Returns **True** if the files are successfully extracted to the specified location. Otherwise, returns **False**.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|Yes|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Zip](../concept/zip-utilities.md)

