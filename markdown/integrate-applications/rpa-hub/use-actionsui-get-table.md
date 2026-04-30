---
title: Use the Get Table component
description: Extract and display data and the count of rows from the grids, lists, combo boxes, and HTML tables, by using the Get Table component in the RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Get Table component

Extract and display data and the count of rows from the grids, lists, combo boxes, and HTML tables, by using the Get Table component in the RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

Many properties of the Get Table component are common with other Actions UI components, to configure these properties, see [Properties of Actions \(UI\) components](../reference/properties-actions-ui-components.md).

The properties unique to the Get Table component are given.

|Property|Description|
|--------|-----------|
|Ignore Header|Option to specify whether the automation captures or ignores the header of the table. The default value is False.|

## Procedure

1.  In the Toolbox pane, navigate to **Actions \(UI\)** &gt; **Get Table**.

2.  Drag the Get Table component to the Design surface.

3.  In the Get Table component, click the camera icon \(![Camera icon.](../image/camera-icon.png)\).

    The `Press "CTRL+SHIFT" for selection` message appears.

4.  Press the **Ctrl + Shift** keys.

    The mouse device turns into a crossover icon \(![Crossover icon.](../image/crossover-icon.png)\).

5.  Drag the mouse device over the application to cover the table and release.

    The selected area of the element is captured as an image in the Get Table component.

6.  Drag the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) over the captured image and place on the location where you want the component to perform an action.

7.  Add an anchor to the captured image by doing the following actions:

    An anchor is a unique identifier that enables the Get Table component to identify the application where the component will perform an action. Although adding an anchor is a good approach, it's optional. If you don't add an anchor, the Get Table component treats the whole captured image as an anchor. To know more about an anchor, see the steps to use the [Anchor](../concept/anchor.md).

    1.  In the Get Table component, right-click the image and click **Add Anchor**.

        The anchor appears as a yellow rectangle with red borders.

    2.  Drag and place the anchor on the captured image.

        **Tip:**

        To change the dimensions of the anchor, position the mouse device along the edge of the anchor until the mouse device turns into a diagonal two-sided arrow \(![Two-sided arrow.](../image/bi-sided-arrow.png)\) and then drag the anchor.

8.  Capture alternate images by doing the following actions:

    Alternate images prevent an execution failure when the Get Table component doesn't find the image that was captured first. In that case, the Get Table component then searches for alternate images to execute. You can add as many alternate images as you need.

    1.  In the ALTERNATE IMAGES window, click the add image icon \(![Add image icon.](../image/add-image-icon.png)\).

    2.  Click the camera icon \(![Camera icon.](../image/camera-icon.png)\).

        The `Press "CTRL+SHIFT" for selection` message appears.

    3.  Drag the mouse device over the application to cover the table and release.

        The selected area is captured as an image in the ALTERNATE IMAGES window.

    4.  Drag the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) over the captured image and place on the location where you want the component to perform an action.

    5.  To close the ALTERNATE IMAGES window, click **OK**.

9.  To configure the ways that the output fields show the output, see [Configure output port properties](configure-output-port-properties.md).

10. Connect the ports as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |Data out|Count|Integer|Returns the total count of rows.|Not applicable|
    |Data out|DataTable|Not applicable|Returns the table.|Not applicable.|

11. To test the component, right-click the component bar and then click **Run From Here**.


## Extract data from an HTML table to an Excel file

![Extract data from a table to an Excel file.](../image/Actions_GetTable.PNG)

The Get Table component extracts data from an HTML table and passes the data through the DataTable Data Out port. The data is passed through the Data In port of the WriteToExcel component \(To use the WriteToExcel component, see [Use the WriteToExcel component](use-datawriter-writetoexcel.md)\). The data is written to the sheet specified in the `SheetName` field of the Excel document specified in the `Filepath` field

.

**Parent Topic:**[Actions \(UI\)](../concept/actions-ui.md)

