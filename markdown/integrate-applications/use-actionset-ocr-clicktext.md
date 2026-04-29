---
title: Use the ActionSet OCR ClickText action
description: Perform a mouse device action on a text in an image in the Internet Explorer browser or Windows applications by specifying the text using the OCR ClickText action.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the ActionSet component, Actions \(UI\), Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the ActionSet OCR ClickText action

Perform a mouse device action on a text in an image in the Internet Explorer browser or Windows applications by specifying the text using the OCR ClickText action.

## Before you begin

Role required: none

## About this task

You can configure the properties for the OCR ClickText action. For more information about these properties, see [OCR Click Text](../reference/actionset-actions-properties.md#section_lff_znr_h5b).

## Procedure

1.  Right-click the anchor.

    To know about the anchor, see how to use the [Anchor](../concept/anchor.md).

2.  Navigate to **OCR** &gt; **Click Text**.

3.  Drag the OCR read table icon \(![Green rectangle icon.](../image/green-rectangle.png)\) over the captured image to the location where the component will perform an action.

4.  To increase or decrease the area on the captured image covered by the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\), drag its edges.

5.  In the Properties pane, select the required action from the Type list in the General section.

6.  Close the ACTIONSET SETTINGS window.

7.  Connect the data and control ports of OCR ClickText to the corresponding ports of other components.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|
    |---------|---------|---------|---------------------|----------|
    |Data In|OCR Click|String|Takes the text that the action matches in the application.|Yes|

8.  To test the component, right-click the component bar and then click **Run From Here**.


**Parent Topic:**[Use the ActionSet component](use-actionsui-actionset.md)

