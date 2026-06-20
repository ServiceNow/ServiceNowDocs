---
title: Use the Click method for Universal App Connector
description: Use the Click method to perform a click action on an element.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/use-click-method-uac.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Universal app connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Click method for Universal App Connector

Use the Click method to perform a click action on an element.

## Before you begin

Verify that you have open or active applications, for example, where you want to capture elements.

Role required: None

## About this task

For information on the various additional operations that are available for the application screens and elements, see [Additional options for application screens and elements in Universal App Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/contextmenu-application-screens.md).

## Procedure

1.  Configure Universal App Connector.

    To learn more about configuring the application screens and child elements, see [Use the Universal App Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-uac.md).

2.  Under Global Objects, double-click the **UniversalApplication** object.

    The Click method appears in the Object Explorer pane.

3.  Drag the Click method to the Design surface.

4.  Double-click the Click method to configure the screens and elements in Universal App Connector.

5.  On the Configure screens and elements window, select the Choose from an open window drop-down \(\[Omitted image "UAC-connector-select-application-icon.png"\] Alt text: Choose from an open window drop-down.\) and select an application screen.

    For example, select the Badge Tool application.

    \[Omitted image "uac-set-value-select-screen.png"\] Alt text: Configure screens and elements window displaying list of open windows in the drop-down. The Badge Tool application is selected.

    **Note:**

    -   If no supported applications are open, the `App window not found message` is displayed.
    -   To display newly opened application screens on the list, select the Click to refresh windows icon \(\[Omitted image "refresh-uac-list.png"\] Alt text: Click to refresh windows icon.\).
6.  To add the selected application screen, for example, Badge Tool application, select **Add screen**.

    After you do this step, you can capture the screen elements to perform actions.

    The application screen appears under the Screens and elements pane.

    \[Omitted image "uac-add-screen-badge-app.png"\] Alt text: Badge Tool application screen name appears under Screens and elements.

7.  To capture the elements from the screen, right-click the added screen and select **Capture Element**.

    The focus is set on the application screen that you had captured and the Capture Element dialog appears.

8.  After selecting the required element, select the Add Element icon \(\[Omitted image "add-element-icon-RPA.png"\] Alt text: Add Element icon\) and select the mode as **UIA**, to capture the element

    **Note:** You must add at least one element to continue.

    For example, select the button element by selecting the Login button.\[Omitted image "uac-click-button-capture.png"\] Alt text: The Badge Tool application shows Capture element dialog that captures the Login button in UIA mode. This button can be added as an element using the Add element button.

9.  In the Configure screens and elements window, right-click the captured element, choose **Select** and select **Done**.

    **Note:** Select at least one element to perform the action. If none are selected, the action won't be executed. To proceed without selecting, select **OK**.

    \[Omitted image "uac-click-select-element.png"\] Alt text: Configure screens and elements window displaying the Select option on an element level.

10. Right-click the Click method and select either **Run From Here** or **Run This**.

    In this scenario, the captured element "Login" button is clicked and the next screen appears.\[Omitted image "uac-click-final-result.gif"\] Alt text: The captured element "Login" button is clicked and the next screen appears.

11. Double-click the required application screen or element and the Object Explorer pane is displayed listing the related methods.

    For example, if you select a Java application screen or element, the Java connector methods are displayed in Object Explorer.

    -   For more information on Java connector methods, see [Java connector methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/java-connector-methods.md).
    -   For more information on Google Chrome and Microsoft Edge connector methods, see [Chromium connector methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/connectors-chrome-methods.md).

    -   For more information on Windows connector methods, see [Windows Connector methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/connectors-windows-methods.md).
    -   If you have captured a web application screen and you want to execute a custom JavaScript on it, you can use the ExecuteJavascript method.


**Parent Topic:**[Universal app connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/universal-app-connector.md)

