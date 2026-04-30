---
title: Use the SetValue method for Universal App Connector
description: Use the SetValue method to assign a specified value into an element.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Universal app connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the SetValue method for Universal App Connector

Use the SetValue method to assign a specified value into an element.

## Before you begin

Verify that you have open or active applications, for example, where you want to capture elements.

Role required: None

## About this task

For information on the various additional operations that are available for the application screens and elements, see [Additional options for application screens and elements in Universal App Connector](../reference/contextmenu-application-screens.md).

## Procedure

1.  Configure Universal App Connector.

    To learn more about configuring the application screens and child elements, see [Use the Universal App Connector](configure-uac.md).

2.  Under Global Objects, double-click the **UniversalApplication** object.

    The SetValue method appears in the Object Explorer pane.

3.  Drag the SetValue method to the Design surface.

4.  Double-click the SetValue method to configure the screens and elements in Universal App Connector.

5.  On the Configure screens and elements window, select the Choose from an open window drop-down \(![Choose from an open window drop-down.](../image/UAC-connector-select-application-icon.png)\) and select an application screen.

    For example, select the Badge Tool application.

    ![Configure screens and elements window displaying list of open windows in the drop-down. The Badge Tool application is selected.](../image/uac-set-value-select-screen.png)

    **Note:**

    -   If no supported applications are open, the `App window not found message` is displayed.
    -   To display newly opened application screens on the list, select the Click to refresh windows icon \(![Click to refresh windows icon.](../image/refresh-uac-list.png)\).
6.  To add the selected application screen, for example, Badge Tool application, select **Add screen**.

    After you do this step, you can capture the screen elements to perform actions.

    The application screen appears under the Screens and elements pane.

    ![Badge Tool application screen name appears under Screens and elements.](../image/uac-add-screen-badge-app.png)

7.  To capture the elements from the screen, right-click the added screen and select **Capture Element**.

    The focus is set on the application screen that you had captured and the capture elements dialog appears.

8.  After selecting the required element, select the Add Element icon \(![Add Element icon](../image/add-element-icon-RPA.png)\) and select the mode as **UIA**, to capture the element.

    **Note:** You must add at least one element to continue.

    For example, select the text box next to User Name field, select the **TAG** as **edit**.![The Badge Tool application shows Capture element dialog that captures the username field in UIA mode. This field can be added as an element using the Add element button.](../image/uac-set-value-textbox-capture.png)

9.  In the Configure screens and elements window, right-click the captured element, choose **Select** and select **Done**.

    **Note:** Select at least one element to perform the action. If none are selected, the action won't be executed. To proceed without selecting, select **OK**.

    ![Configure screens and elements window displaying the Select option on an element level.](../image/uac-set-value-select-element.png)

10. Complete the following parameters in the SetValue method:

<table id="table_ucm_psl_fwb"><thead><tr><th>

Parameter name

</th><th>

Parameter description

</th><th>

Port Type

</th><th>

Data Type

</th></tr></thead><tbody><tr><td>

Value

</td><td>

Enter the value that you want to assign in the element.For example, `ServiceNow`.

</td><td>

Data In

</td><td>

String

</td></tr></tbody>
</table>11. Right-click the SetValue method and select either **Run From Here** or **Run This**.

    The input value is displayed in the captured element. In this scenario, ServiceNow is displayed in the **User Name** Field.![ServiceNow displayed in the captured element that is the User Name field.](../image/uac-set-value-final-result.png)

12. Double-click the required application screen or element and the Object Explorer pane is displayed listing the related methods.

    For example, if you select a Java application screen or element, the Java connector methods are displayed in Object Explorer.

    -   For more information on Java connector methods, see [Java connector methods](../reference/java-connector-methods.md).
    -   For more information on Google Chrome and Microsoft Edge connector methods, see [Chromium connector methods](../reference/connectors-chrome-methods.md).

    -   For more information on Windows connector methods, see [Windows Connector methods](../reference/connectors-windows-methods.md).
    -   If you have captured a web application screen and you want to execute a custom JavaScript on it, you can use the ExecuteJavascript method.


**Parent Topic:**[Universal app connector](../concept/universal-app-connector.md)

