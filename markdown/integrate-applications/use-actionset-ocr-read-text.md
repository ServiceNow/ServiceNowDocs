---
title: Use the ActionSet OCR Read Text action
description: Extract text from images in the desktop, Windows applications, and the Internet Explorer browser by using the OCR Read Text action in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use the ActionSet component, Actions \(UI\), Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the ActionSet OCR Read Text action

Extract text from images in the desktop, Windows applications, and the Internet Explorer browser by using the OCR Read Text action in RPA Desktop Design Studio.

## Before you begin

Capture an image of the target application window and create an anchor. For information about how to do this, see [Use the ActionSet component](use-actionsui-actionset.md).

Role required: none

## About this task

The ActionSet OCR \(optical character recognition\) Read Text action can capture text from images and return it in standard text format.

You can configure the properties for the OCR Read Text component. For more information about these properties, see [ActionSet OCR Read Text properties](../reference/actionset-actions-properties.md#ActionSet-OCR-ReadText).

## Procedure

1.  Right-click the anchor.

    To know about the anchor, see how to use the [Anchor](../concept/anchor.md).

2.  Navigate to **OCR** &gt; **Read Text**.

3.  Drag the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\) over the area that contains the text that you want to capture.

    If necessary, adjust the size of the selection rectangle by dragging its edges.

4.  In the Properties pane of the ActionSet Settings window, configure the properties of the OCR Read Text action.

    In addition to properties that are common to all ActionSet actions, including the option to set a delay before or after performing the action, several properties let you improve text recognition by adjusting or scaling the captured image, or by setting the options of the text recognition engine.

5.  To change the area in the image covered by the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\), do the following steps.

    1.  Place the mouse device along the edges of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\).

        The mouse device turns into a two-sided arrow \(![Two-sided arrow](../image/bi-sided-arrow.png)\).

    2.  Drag the edges of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\).

6.  Close the ACTIONSET SETTINGS window.

7.  If you didn’t hide the port for the OCR parameter in step 4, connect the port so the action can send the extracted text for use.

    The OCR parameter is described in the following table.

    |Port type|Port name|Data type|Purpose of connection|
    |---------|---------|---------|---------------------|
    |Data out|OCR|String|Returns the text from the image.|

8.  To test the component, right-click the component bar and then click **Run From Here**.


**Parent Topic:**[Use the ActionSet component](use-actionsui-actionset.md)

