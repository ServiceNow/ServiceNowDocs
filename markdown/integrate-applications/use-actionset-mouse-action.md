---
title: Use the ActionSet Mouse action
description: Do various mouse device actions on the desktop, Windows applications, and web pages on the Internet Explorer browser using the ActionSet Mouse action in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the ActionSet component, Actions \(UI\), Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the ActionSet Mouse action

Do various mouse device actions on the desktop, Windows applications, and web pages on the Internet Explorer browser using the ActionSet Mouse action in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

Configure the properties for the ActionSet Mouse action. For more information about these properties, see [ActionSet-Mouse Action properties](../reference/actionset-actions-properties.md#actionset-mouse-action).

## Procedure

1.  Right-click the anchor.

    To know about the anchor, see [Anchor](../concept/anchor.md).

2.  Click **Mouse Action**.

3.  Drag and place the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) to the location on the captured image where the component will perform an action.

4.  To specify a mouse device action, select the action from the Type list in the PROPERTIES pane.

    The default action is LeftClick.

5.  Close the ACTIONSET SETTINGS window.

6.  Connect the data port of the ActionSet Mouse action to the corresponding port of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|Notes|
    |---------|---------|---------|---------------------|----------|-----|
    |Data In|MouseAction|Boolean|If True, the Mouse action is performed, else, it is not performed.|No. Connecting the port is optional.|This port is exposed if the Expose Port option is enabled in the PROPERTIES pane.|

7.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Use the ActionSet component](use-actionsui-actionset.md)

