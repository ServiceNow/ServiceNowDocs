---
title: Use the OpenFileDialog component
description: Open a file dialog from where you can open a file using the OpenFileDialog component in the RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Dialogs, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the OpenFileDialog component

Open a file dialog from where you can open a file using the OpenFileDialog component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

By default, the OpenFileDialog component opens the last file dialog you had opened. You can change the file dialog location and the type of file you want to open by specifying the location and the file type.

There are properties that you configure for the OpenFileDialog component. For more information, see [Dialog component properties](../reference/dialog-component-properties.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities&gt;Dialogs**.

2.  Drag the OpenFileDialog component onto the Design surface.

3.  To open the last file dialog you had opened, right-click the OpenFileDialog component bar.

4.  Click **Run From Here**.

5.  In the Save As file dialog, select the required file and click **Open**.

    The Result \(Boolean\) and FileName \(String\) returns the Boolean response to whether you had opened a file and the file name and path respectively.

6.  To configure the input ports, see [Configure port properties](configure-input-port-properties.md).

7.  Connect the data and control ports of OpenFileDialog to the corresponding ports of other components.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data In \(Filter\)|Takes the format of the file that you want to open from a previously executed component.|No. Connecting the port is optional.|
    |Data In \(InitialDirectory\)|Takes the path to the directory that contains the file you want to open from a previously executed component.|No. Connecting the port is optional.|
    |Data Out \(Result\)|Passes the Boolean response to whether you had opened a file to the next component.|Yes|
    |Data Out \(FileName\)|Passes the name of the file you had opened and its path to the next component.|Yes|
    |Control In|Passes the control from the previously executed component.|Yes|
    |Control Out|Passes the control from the Get Text component to the next component to be executed.|Yes|

8.  To test the component, click **Run** under the **DESIGN** tab.


**Parent Topic:**[Dialogs](../concept/dialogs.md)

