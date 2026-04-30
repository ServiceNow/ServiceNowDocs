---
title: Use the ActionSet OCR Read Table action
description: Extract a table from images in the desktop, Windows applications, and web pages on the Internet Explorer browser by using the OCR Read Table action in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use the ActionSet component, Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the ActionSet OCR Read Table action

Extract a table from images in the desktop, Windows applications, and web pages on the Internet Explorer browser by using the OCR Read Table action in RPA Desktop Design Studio.

## Before you begin

Capture an image of the target application window and create an anchor. For information about how to do this, see [Use the ActionSet component](use-actionsui-actionset.md).

Role required: none

## About this task

The ActionSet OCR \(optical character recognition\) Read Table action can capture a table even when it appears in an image instead of in a text-based format.

You can configure the properties for the OCR Read Table action. For more information about these properties, see [ActionSet OCR Read Table properties](../reference/actionset-actions-properties.md#ActionSet-OCR-ReadTable).

## Procedure

1.  Right-click the anchor.

    To know about the anchor, see how to use the [Anchor](../concept/anchor.md).

2.  Navigate to **OCR** &gt; **Read Table**.

3.  Click **Read Table**.

4.  Click the OCR read table icon \(![OCR Read Table icon.](../image/ocr-read-table-icon.png)\) and drag the indicator over the area that contains the table that you want to capture.

    ![TABLE tab of the selection indicator](../image/ocr-table-action-set-rpa.png "TABLE tab of the selection indicator")

5.  Drag the lines that mark the cell boundaries to match the table, taking care to define the cells as accurately as possible and perform the following steps.

    The components returns OCR results from the individual cell areas.

    1.  Adjust the size of the selection indicator by dragging its edges.

    2.  Right-click an empty space within the selection indicator, and then select **Add Row** or **Add Column** to add rows and columns as necessary to match the table.

    3.  Drag the row and column division lines inside the selection area to match the table.

6.  Configure the properties of the OCR Read Table action in the Properties pane of the ACTIONSET SETTINGS window.

    For example, you can choose to consider the first row of the table as a table header.

    For more information about these properties, see [ActionSet OCR Read Table properties](../reference/actionset-actions-properties.md#ActionSet-OCR-ReadTable).

7.  Close the ACTIONSET SETTINGS window.

8.  If you didn’t hide the port for the OcrTable action in Step 6, connect the port so the action can return the text of the extracted table.

    The OcrTable parameter is described in the following table.

    |Port type|Port name|Data type|Purpose of connection|
    |---------|---------|---------|---------------------|
    |Data out|OcrTable|String|Returns text from the extracted table.|

9.  To test the component, right-click the component bar and then click **Run From Here**.


**Parent Topic:**[Use the ActionSet component](use-actionsui-actionset.md)

