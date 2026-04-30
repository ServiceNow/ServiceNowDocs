---
title: Use the OpenFolderDialog component
description: Open a folder dialog so you can open a folder from there with the OpenFolderDialog component. After opening the folder dialog, you can create a folder.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Dialogs, Utilities, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the OpenFolderDialog component

Open a folder dialog so you can open a folder from there with the OpenFolderDialog component. After opening the folder dialog, you can create a folder.

## Before you begin

Role required: none

## About this task

There are properties that you configure for the OpenFolderDialog component. For more information, see [Dialog component properties](../reference/dialog-component-properties.md).

## Procedure

1.  In the Toolbox pane, navigate to **Utilities&gt;Dialogs**.

2.  Drag the OpenFolderDialog component onto the Design surface.

3.  To open the folder dialog, right-click the OpenFolderDialog component bar.

4.  In the Browse For Folder dialog, select the required folder and click **Open**.

5.  To configure the outputs from the data ports, see [Configure output port properties](configure-output-port-properties.md).

    The Result \(Boolean\) and Path \(String\) returns the Boolean response to whether you had opened a folder and the folder name and path respectively.

6.  Connect the data and control ports of OpenFolderDialog to the corresponding ports of other components.

    |Port type|Purpose of connection|Mandatory?|
    |---------|---------------------|----------|
    |Data Out \(Result\)|Passes the boolean response to whether you had opened a folder to the next component.|Yes|
    |Data Out \(Path\)|Passes the path to the folder you have opened from the folder dialog to the next component.|Yes|
    |Control In|Passes the control from the previously executed component.|Yes|
    |Control Out|Passes the control from the Get Text component to the next component to be executed.|Yes|

7.  To test the component, click **Run** under the **DESIGN** tab.


**Parent Topic:**[Dialogs](../concept/dialogs.md)

