---
title: Use the ActionSet Text Selection action
description: Select, copy, or delete text from the Desktop and Windows applications, and the Internet Explorer browser by using the Text Selection action in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use the ActionSet component, Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the ActionSet Text Selection action

Select, copy, or delete text from the Desktop and Windows applications, and the Internet Explorer browser by using the Text Selection action in RPA Desktop Design Studio.

## Before you begin

Capture an image of the target application window and create an anchor. For information about how to do this, see [Use the ActionSet component](use-actionsui-actionset.md).

Role required: none

## About this task

In addition to selecting text, the ActionSet Text Selection action can copy or delete text in a targeted application window. You can also set the action to trim leading or trailing white space from the captured text.

You can configure the properties for the Text Selection component. For more information about these properties, see [ActionSet Text Selection- Properties](../reference/actionset-actions-properties.md#ActionSet-TextSelection).

## Procedure

1.  Right-click the anchor.

    To learn about the anchor, see how to use the [Anchor](../concept/anchor.md).

2.  Click **Text Selection**.

3.  Drag the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\) over the area that contains the text that you want to select, copy, or delete.

4.  To increase or decrease the area on the captured image covered by the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\), drag its edges.

5.  In the Properties pane, select **Copy** or **Delete** from the Type list in the General section.

    For example, you can set a delay or change the nature of the action. By default, the action selects text.

6.  Close the ACTIONSET SETTINGS window.

7.  If you didn’t hide the port for the TextSelection parameter in Step 4, connect the port so the action can send the captured text for use.

    The TextSelection parameter is described in the following table.

    |Port type|Port name|Data type|Purpose of connection|
    |---------|---------|---------|---------------------|
    |Data Out|TextSelection|String|Sends the captured text to another component.|

8.  To test the component, right-click the component bar and then click **Run From Here**.


**Parent Topic:**[Use the ActionSet component](use-actionsui-actionset.md)

