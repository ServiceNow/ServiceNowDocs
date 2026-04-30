---
title: Use the ActionSet Click action
description: Simulate a simple left-click on the target area as part of a series of actions in the ActionSet component.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use the ActionSet component, Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the ActionSet Click action

Simulate a simple left-click on the target area as part of a series of actions in the ActionSet component.

## Before you begin

Capture an image of the target application window and create an anchor. For information about how to do this, see [Use the ActionSet component](use-actionsui-actionset.md).

Role required: none

## About this task

The ActionSet Click action simulates a manual click at the area you specify in the ActionSet Settings window. You can use it to click a button, open a menu, select an object, or perform any action typically performed by a mouse click.

You can configure the properties for the Click action. For more information about these properties, see [ActionSet Click properties](../reference/actionset-actions-properties.md#actionset-click).

## Procedure

1.  Right-click the anchor.

    For more information about an anchor, see [Anchor](../concept/anchor.md).

2.  Click **Click**.

3.  Drag and place the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) to the location where you want to simulate a click.

4.  In the Properties pane of the ActionSet Settings window, configure the properties of the Click action.

    For example, you can set a delay or change the name of the action.

5.  Close the ACTIONSET SETTINGS window.

6.  Connect the port to let its input determine whether the Click action is performed, if you exposed the Click parameter’s port in Step 4.

    The Click parameter is described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Notes|
    |---------|---------|---------|---------------------|-----|
    |Data In|Click|Boolean|Determines whether the click action is performed. If the value of the Click parameter is True, the action is performed. If the value is False, the action is not performed.|The Data In port is available if you enable the Expose Port check box in the Properties section. The default Boolean value is True.|

7.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Use the ActionSet component](use-actionsui-actionset.md)

