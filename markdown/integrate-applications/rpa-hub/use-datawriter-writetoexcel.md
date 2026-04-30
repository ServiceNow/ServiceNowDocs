---
title: Use the WriteToExcel component
description: Write the data to a worksheet of a Microsoft Excel file as part of an automation Workflow by using the WriteToExcel component in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Writer, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the WriteToExcel component

Write the data to a worksheet of a Microsoft Excel file as part of an automation Workflow by using the WriteToExcel component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the WriteToExcel component. For more information about these properties, see [Properties of the Data Writer components](../reference/util-datawriter-prop.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities** &gt; **Data Writer**.

2.  Drag the WriteToExcel component to the Design surface.

3.  To configure the input fields, see [Configure port properties](configure-input-port-properties.md).

4.  Connect the data and control ports of the WriteToExcel component to the corresponding ports of the other components as described in the following table.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Filepath\)|Passes the path to the Excel file from a previously executed component.|Yes|
    |Data In \(SheetName\)|Passes the name of the sheet in the Excel file to which data will be written from a previously executed component.|Yes|
    |Data In \(Data\)|Passes the data that will be written from a previously executed component.|Yes|
    |Control In|Connects to the Control Out port of one or more components.|Yes|
    |Control Out|Connects to the Control In port of any other component.|No. Connecting the port is optional.|

5.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Data Writer](../concept/datawriter-utility.md)

