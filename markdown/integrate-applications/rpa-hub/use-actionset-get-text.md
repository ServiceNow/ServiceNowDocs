---
title: Use the ActionSet GetText action
description: Capture text from the Windows applications, and web pages on the Internet Explorer browser by using the Get Text action in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use the ActionSet component, Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use the ActionSet GetText action

Capture text from the Windows applications, and web pages on the Internet Explorer browser by using the Get Text action in RPA Desktop Design Studio.

## Before you begin

Capture an image of the target application window and create an anchor. For information about how to do this, see [Use the ActionSet component](use-actionsui-actionset.md).

Role required: none

## About this task

The ActionSet Get Text action captures text from an area that you specify in the ActionSet Settings window. You can use it to receive text in the target area when it is in text format. To capture text from an image, see [Use the ActionSet OCR Read Text action](use-actionset-ocr-read-text.md).

You can configure the properties for the GetText component. For more information about these properties, see [ActionSet-Get Text properties](../reference/actionset-actions-properties.md#ActionSet-GetText).

## Procedure

1.  Right-click the anchor.

    To learn about the anchor, see how to use the [Anchor](../concept/anchor.md).

2.  Click **Get Text**.

3.  Drag the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) to the field where you want to capture text.

4.  In the Properties pane of the ActionSet Settings window, configure the properties of the Get Text action.

    For example, you can set a delay or change the name of the action.

5.  Close the ACTIONSET SETTINGS window.

6.  If you didn’t hide the port for the GetText parameter in Step 4, connect the port so the action can transmit the captured text for use.

    The GetText parameter is described in the following table.

    |Port type|Port name|Data type|Purpose of connection|
    |---------|---------|---------|---------------------|
    |Data out|Get Text|String|Sends the captured text to another component.|

7.  To test the component, right-click the component bar and then click **Run From Here**.


**Parent Topic:**[Use the ActionSet component](use-actionsui-actionset.md)

