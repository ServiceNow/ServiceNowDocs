---
title: Use the WaitForAnyScreen method for Universal App Connector
description: Find one or more application screens and optionally, their child elements within a time period that you specify and then perform actions that you specify.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Universal app connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the WaitForAnyScreen method for Universal App Connector

Find one or more application screens and optionally, their child elements within a time period that you specify and then perform actions that you specify.

## Before you begin

Role required: None

## About this task

When you use the WaitForAnyScreen method, it tries to find a screen by matching the screen match rules within a specified duration. If it fails to find the screen within that duration, you may optionally enable it to perform an action by passing the control to another component through the ELSE port. Else, the WaitForAnyScreen method completes its execution. For the WaitForAnyScreen method to find a screen, the screen must be in an opened state.

## Procedure

1.  Configure the UAC.

    To learn to configure the application screens and child elements, see [Use the Universal App Connector](configure-uac.md).

2.  Under Global Objects, double-click the **UniversalApplication** object.

    The WaitForAnyScreen method appears in the Object Explorer pane.

3.  Drag the WaitForAnyScreen method to the Design surface.

4.  Configure the WaitForAnyScreen method.

    1.  Select the settings icon \(![Wait For Any Screen method settings icon.](../image/uac-connector-settings-icon.png)\).

    2.  On the CHOOSE SCREENS window, select one or more application screens.

    3.  Select **OK**.

        The application screen that you selected appears in the WaitForAnyScreen method.

        ![Captured screen on the Wait For Any Screen method.](../image/uac-connector-captured-screen.png)

    4.  Configure the parameters on the WaitForAnyScreen method.

<table id="table_zlh_5kw_rzb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th><th>

Default value

</th><th>

Mandatory?

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

MatchAllChildren

</td><td>

If set to `True`, the method also finds the child elements of the parent screen that you had captured by matching the attributes of the child elements.

</td><td>

Data In

</td><td>

Boolean

</td><td>

False

</td><td>

No

</td><td>

**Warning:**

Setting this parameter to `True` may slow down the execution of the component.

</td></tr><tr><td>

Timeout

</td><td>

Duration in seconds within which the WaitForAnyScreen method tries to find the screen and, optionally, its child elements.

</td><td>

Data In

</td><td>

Integer

</td><td>

30 seconds

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

Application screen

</td><td>

Title of the application screen that you’ve selected in the CHOOSE SCREENS window. The component allows multiple window entries depending on the number of screens you had selected in the CHOOSE SCREENS window.

</td><td>

Data Out

</td><td>

Not applicable

</td><td>

Not applicable

</td><td>

Not applicable

</td><td>

If the WaitForAnyScreen method finds the first screen that is listed, the execution of the WaitForAnyScreen method completes.

</td></tr><tr><td>

ELSE

</td><td>

Executes another component or method if the WaitForAnyScreen method fails to find any screen within the duration specified in the Timeout port.

</td><td>

Data Out

</td><td>

Not applicable

</td><td>

Not applicable

</td><td>

No

</td><td>

 

</td></tr></tbody>
</table>5.  Double-click the required application screen or element and the Object Explorer pane is displayed listing the related methods.

    For example, if you select a Java application screen or element, the Java connector methods are displayed in Object Explorer.

    -   For more information on Java connector methods, see [Java connector methods](../reference/java-connector-methods.md).
    -   For more information on Google Chrome and Microsoft Edge connector methods, see [Chromium connector methods](../reference/connectors-chrome-methods.md).

    -   For more information on Windows connector methods, see [Windows Connector methods](../reference/connectors-windows-methods.md).
    -   If you have captured a web application screen and you want to execute a custom JavaScript on it, you can use the ExecuteJavascript method.


**Parent Topic:**[Universal app connector](../concept/universal-app-connector.md)

