---
title: Use the Get Text component
description: The Get Text component captures text from an area that you specify in the target application. You can use it to receive data that exists in text format. To capture text from an image, see Use the OCR Text component.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the Get Text component

The Get Text component captures text from an area that you specify in the target application. You can use it to receive data that exists in text format. To capture text from an image, see Use the OCR Text component.

## Before you begin

Role required: none

## About this task

The properties of the Get Text component are common with other Actions UI components, to configure these properties, see [Properties of Actions \(UI\) components](../reference/properties-actions-ui-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **Actions \(UI\)** &gt; **Get Text**.

2.  Drag the Get Text component to the Design surface.

3.  In the Get Text component, click the camera icon \(![Camera icon.](../image/camera-icon.png)\).

    The `Press "CTRL+SHIFT" for selection` message appears.

4.  Switch to the application that you want to capture text from, and press the **Ctrl + Shift** keys.

    The mouse device turns into a crossover icon \(![Crossover icon.](../image/crossover-icon.png)\).

5.  Drag the cursor to capture the area where you want the component to capture text.

    **Note:** For best results, include a part of the image that does not change in your selection. This can help the automation find the capture area when the unchanging part is used as an anchor. To designate an anchor, see Step 7.

    The selected area is captured as an image in the Get Text component.

6.  Drag the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) to the area in the captured image where you want to capture the text.

7.  Add an anchor to the captured image by doing the following actions:

    An anchor is a unique subset of the captured image that helps the Get Text component identify where the component will perform an action. Although adding an anchor is a good approach, it's optional. If you don't add an anchor, the Get Text component treats the whole captured image as an anchor. To know more about an anchor, see the steps to use the [Anchor](../concept/anchor.md).

    1.  In the Get Text component, right-click the image, and click **Add Anchor**.

        The anchor appears as a yellow rectangle with red borders.

    2.  To identify the part of the image for the Get Text component, drag and place the anchor at the unique location on the image.

        **Tip:**

        To change the dimensions of the anchor, position the mouse device along the edge of the anchor until the mouse device turns into a diagonal two-sided arrow \(![Two-sided arrow.](../image/bi-sided-arrow.png)\) and then drag the anchor.

8.  Capture one or more alternate images by doing the following actions:

    Alternate images let the component continue when the Get Text component doesn't find the first image that was captured. When this happens, the Get Text component searches for an alternate image. You can add as many alternate images as you need. The component searches for alternate images in the same order as they were added.

    1.  In the ALTERNATE IMAGES window, click the add image icon \(![Add image icon.](../image/add-image-icon.png)\)

    2.  Click the camera icon \(![Camera icon.](../image/camera-icon.png)\).

        The `Press "CTRL+SHIFT" for selection` message appears.

    3.  Press the **Ctrl + Shift** keys.

        The mouse device turns into a crossover icon \(![Crossover icon.](../image/crossover-icon.png)\).

    4.  Drag the mouse device over the application to capture the area where you want the component to perform an action and release.

        The selected area is captured as an image in the ALTERNATE IMAGES window.

    5.  Drag the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) over the captured image and place on the location where you want the component to perform an action.

    6.  To close the ALTERNATE IMAGES window, click **OK**.

9.  To configure the ways that the output fields show the output, see [Configure output port properties](configure-output-port-properties.md).

10. Connect the Data Out and control ports of the Get Text component to the corresponding ports of other suitable components within the automation.

    The Extracted Data port, which sends the extracted text to another component for display or further processing, is described in the following table.

    |Port type|Port name|Data type|Purpose of connection|
    |---------|---------|---------|---------------------|
    |Data out|Extracted Data|String|Sends the captured text to another component|

11. To test the component, right-click the component bar and then click **Run From Here**.


## Extract a line of text from a window and display with the Show component

![Extract a line of text from a window and display with the Show component.](../image/Actionc_GetText.PNG)

The Get Text component extracts the text "The world works with ServiceNow" and passes the text through its Data Out port to the Show component \(To use the Show component, see [Use the Show component](use-general-messagebox-show.md)\). The Show component displays the same text in a pop-up window.

**Parent Topic:**[Actions \(UI\)](../concept/actions-ui.md)

