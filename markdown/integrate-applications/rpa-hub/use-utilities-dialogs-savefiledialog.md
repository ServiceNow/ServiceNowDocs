---
title: Use the SaveFileDialog component
description: Save a file to a folder using the SaveFileDialog component in the RPA Desktop Design Studio. By default, the component opens the last file dialog you had opened.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Dialogs, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the SaveFileDialog component

Save a file to a folder using the SaveFileDialog component in the RPA Desktop Design Studio. By default, the component opens the last file dialog you had opened.

## Before you begin

Role required: none

## About this task

There are properties that you configure for the SaveFileDialog component. For more information, see [Dialog component properties](dialog-component-properties.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities&gt;Dialogs**.

2.  Drag the SaveFileDialog component onto the Design surface.

3.  To open the last file dialog you had opened, right-click the SaveFileDialog component bar.

4.  Click **Run From Here**.

5.  In the Save As dialog, enter the name of the file in the File name field.

6.  Click **Save**.

    The Result \(Boolean\) and FileName \(String\) returns the Boolean response to whether you had opened a file and the file name and path respectively.

7.  Connect the data and control ports of SaveFileDialog to the corresponding ports of other components.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data Out \(Result\)|Passes the boolean response to whether the file was saved to the next component.|Yes|
    |Data Out \(Filename\)|Passes the name of the file that you saved and the path to the file to the next component.|Yes|
    |Control In|Passes the control from the previously executed component.|Yes|
    |Control Out|Passes the control from the Get Text component to the next component to be executed.|Yes|

8.  To test the component, click **Run** under the **DESIGN** tab.


**Parent Topic:**[Dialogs](../concept/dialogs.md)

