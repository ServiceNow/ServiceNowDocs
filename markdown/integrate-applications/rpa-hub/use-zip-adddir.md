---
title: Use the AddDirectory component
description: Add the directory contents to an existing zip archive by using the AddDirectory component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Zip, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the AddDirectory component

Add the directory contents to an existing zip archive by using the AddDirectory component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the AddDirectory component. For more information about these properties, see [Properties of the Zip components](../reference/util-zip-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Zip**.

2.  Drag the AddDirectory component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the AddDirectory component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(zipFilePath\)|Takes the zipFilePath.|Yes|
    |Data In \(directoryPath\)|Takes the directory path.|Yes|
    |Data Out|Returns **True** if the directory contents are successfully added to the specified zip archive. Otherwise, returns **False**.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of another component or the default end component.|No|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Zip](../concept/zip-utilities.md)

