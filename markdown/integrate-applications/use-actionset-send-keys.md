---
title: Use the ActionSet SendKeys action
description: Set text or perform keyboard shortcuts on fields and elements on the desktop, Windows applications, and web pages on the Internet Explorer browser using the ActionSet Send Keys action in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the ActionSet component, Actions \(UI\), Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use the ActionSet SendKeys action

Set text or perform keyboard shortcuts on fields and elements on the desktop, Windows applications, and web pages on the Internet Explorer browser using the ActionSet Send Keys action in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

Configure the properties for the ActionSet SendKeys action. For more information about these properties, see [ActionSet Send Keys properties](../reference/actionset-actions-properties.md#actionset-sendkeys).

## Procedure

1.  Right-click the anchor.

    To know about the anchor, see [Anchor](../concept/anchor.md).

2.  Click **Send Keys**.

3.  Drag and place the Green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) on the location in the captured image where the component will perform an action.

4.  Close the ACTIONSET SETTINGS window.

5.  Connect the data port of the ActionSet Send Keys component to the corresponding ports of the other components as described in the following table.

    |Port type|Port name|Data type|Purpose of connection|Mandatory?|Notes|
    |---------|---------|---------|---------------------|----------|-----|
    |Data In|SendKeys|String|Takes the string or keyboard shortcuts.|No. Connecting the port is optional.| |

6.  To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[Use the ActionSet component](use-actionsui-actionset.md)

