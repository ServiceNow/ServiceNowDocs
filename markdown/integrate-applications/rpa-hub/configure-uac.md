---
title: Use the Universal App Connector
description: Create automations for your Windows, Java, Google Chrome, and Edge browser-based applications by using the Universal App Connector \(UAC\). Configure the applications from a single, unified connector and capture the screens and elements or screen controls such as check boxes, and buttons. Use the methods of these screens and elements to build your automation.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Universal app connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Universal App Connector

Create automations for your Windows, Java, Google Chrome, and Edge browser-based applications by using the Universal App Connector \(UAC\). Configure the applications from a single, unified connector and capture the screens and elements or screen controls such as check boxes, and buttons. Use the methods of these screens and elements to build your automation.

## Before you begin

Add the Universal App Connector plugin from the Plugins Manager before using the connector. For more information about adding the SSH plugin, see [Manage plugins in RPA Desktop Design Studio](install-plugins-rpa-studio.md).

Verify that you have open or active Windows, Java, Google Chrome, or Edge applications.

Role required: None

## Procedure

1.  In the Toolbox pane, navigate to **Connectors**, and drag **Universal App Connector** to **Global Objects** in the Project Explorer pane.

    The connector is added as a **UniversalApplication** object under **Global Objects**.

2.  To use the methods at the **Universal App Connector** connector level, double-click the **UniversalApplication** object.

    |Method name|Reference|
    |-----------|---------|
    |**Click**|[Use the Click method for Universal App Connector](use-click-method-uac.md)|
    |**GetValue**|[Use the GetValue method for Universal App Connector](use-getvalue-method-uac.md)|
    |**SetValue**|[Use the SetValue method for Universal App Connector](use-setvalue-uac.md)|
    |**Start**|[Use the Start method for Universal App Connector](use-start-method.md)|
    |**WaitForAnyScreen**|[Use the WaitForAnyScreen method for Universal App Connector](use-the-wait-for-any-screen-method.md)|

    For example, the Start method is used if you want the browser or application to start before interacting with any application screens or elements.

    The methods appear in the Object Explorer pane.

3.  To configure the screens and elements in the UAC, do the steps.

    1.  Under Global Objects, right-click **UniversalApplication** and select **Configure**.

    2.  On the Configure screens and elements window, select the **Choose from an open window** drop-down \(![Choose from an open window drop-down.](../image/UAC-connector-select-application-icon.png)\) and select an application screen.

        ![Open applications.](../image/uac-connector-open-apps.png)

        **Note:**

        -   If no supported applications are open, the `App window not found message` is displayed.
        -   To display newly opened application screens on the list, select the Click to refresh windows icon \(![Click to refresh windows icon.](../image/refresh-uac-list.png)\).
    3.  To filter the opened applications by their type, select the **All** filter application type icon \(![Filter application type icon.](../image/uac-connector-all-applications-filter.png)\) and select All or the application type.

        For example, if you select **Chrome**, only Google Chrome web pages appear in the **Choose from an open window** list.

        For example, if you select **Windows Application**, only Windows screens appear in the **Choose from an open window** list.

        ![Filter the application types.](../image/filter-app-type-uac.png "Filter the opened applications")

    4.  To add the selected application screen, select **Add screen**.

        After you do this step, you can capture the screen elements to perform actions.

        The application screen appears under the Screens and elements pane.

        ![Application screen name appears under Screens and elements.](../image/uac-connector-application-screen-added.png)

    5.  To capture the elements from the screen, under the Screen and elements pane, right-click the added screen and select **Capture Element**.

        ![Capture Element option.](../image/uac-connector-capture-window.png)

        The focus is set on the application screen that you had captured and the capture elements dialog appears.

        For example, when you are capturing elements of a Windows application such as Notepad. If you select the **UIA** mode \(UI Automation\), the scroll bar of the Notepad is also captured.

        ![UI Automation mode of the Windows application, such as Notepad.](../image/uac-windows-app-uia-mode.png "Capture dialog for Windows application - Notepad - UIA mode")

        If you select the **AA** mode \(Active Accessibility\), the scroll bar of the Notepad is not captured.

        ![Active Accessibility mode of the Windows application, such as Notepad.](../image/uac-windows-app-aa-mode.png "Capture dialog for Windows application - Notepad - AA mode")

    6.  To use the methods at the **Universal App Connector** connector level for the two modes, UI Automation and Active Accessibility, double-click the **UniversalApplication** object.

        For more information about the methods for UI Automation mode and Active Accessibility mode, see [Methods of UI Automation mode and Active Accessibility mode](../reference/uac-windows-uia-aa-methods.md).

        The methods appear in the Object Explorer pane.

4.  Do any of the following options for a desired action.

<table id="choicetable_zm4_lwz_vrb"><thead><tr><th align="left" id="d174437e431">

Option

</th><th align="left" id="d174437e434">

Action

</th></tr></thead><tbody><tr><td id="d174437e440">

**To rename __UniversalApplication__**

</td><td>

Navigate to **Global Objects** in the Project Explorer pane, right-click the **UniversalApplication** and select **Rename**.![From Global objects, right-click the UniversalApplication and select Rename.](../image/uac-rename-right-click.png "Rename UniversalApplication")

</td></tr><tr><td id="d174437e480">

**To change the name of the screen while configuring the screens and elements**

</td><td>

1.  Select the name of the application screen under the Screens and elements pane.

The information of the selected application screen appears under the Properties pane.

2.  Update the name of the application screen in the **Name** field and press **Enter**.

The name of the application is updated in the Screens and elements pane.

 ![Update the application screen name in the Properties section.](../image/uac-update-screen-name.png "Update the application screen name")

</td></tr><tr><td id="d174437e523">

**To identify the screen uniquely**

</td><td>

Use the screen match rules to identify and locate the screen.During the execution, the plugin must identify the target screen uniquely to automate actions on the screen. Examples of attributes are the title or URL of the application screen. The attributes appear under the **Screen match rules** pane on the **Configure screens and elements** window. The UAC uses the screen match rules to identify the screen first, and uses the element match rule to identify the element, and then, perform actions on elements such as Click or Get Text.

![Screen match rules.](../image/uac-connector-screen-match-rules.png)

The image below shows an example of multiple elements that match the same criteria given in the Match Attributes section. A multiple number of instances, if any, appears when you refresh the captured element, is indicated within the brackets in red. In such cases, you must tweak the attributes to select exactly the element that needs to be automated. The user can refresh to check if the selected criteria match exactly one element.

![Multiple instances of captured element.](../image/uac-connector-multiple-instances.png)

</td></tr><tr><td id="d174437e554">

**To identify an element uniquely**

</td><td>

Use the element match rules to edit the values in the provided **Locator** and the **Match Attributes** sections.During the execution, the plugin must identify the target element uniquely to automate actions on the element. The attributes appear under the **Match Attributes** pane on the **Configure screens and elements** window. The UAC uses the screen match rules to identify the screen first, and uses the element match rule to identify the element, and then, perform actions on elements such as Click or Get Text.

The image shows the match rules of an element captured.

![Element and its match rules.](../image/uac-connector-child-element-match-rules.png)

</td></tr><tr><td id="d174437e586">

**To find the elements on the application screen**

</td><td>

Use the locators of the captured elements.For more information, see [Find the elements on the application screen](find-elements-screen-uac.md).

</td></tr><tr><td id="d174437e607">

**To view the path to an iframe, if any, in a captured element**

</td><td>

1.  In the **Screens and elements** pane, select the element.
2.  Select the **Advanced** tab.

The iframe appears.

![iframe appears.](../image/uac-connnector-iframe.png)

3.  From the **Locator** list, select a locator to find the path to the iframe.

![iframe locator.](../image/uac-connector-iframe-locator.png)

</td></tr></tbody>
</table>5.  Right-click the application screen or element to perform any additional operations such as **Refresh**, **Refresh screen and elements**, **Focus**, **Add custom element**, **Show Elements**, **Delete**, and more.

    For information on the various additional operations that are available for the application screens and elements, see [Additional options for application screens and elements in Universal App Connector](../reference/contextmenu-application-screens.md).

6.  Select **Done** after you finish configuring your application screens or elements.

    The application screens and their elements appear under the UAC object in **Global Objects**.

7.  Double-click the required application screen or element and the Object Explorer pane is displayed listing the related methods.

    For example, if you select a Java application screen or element, the Java connector methods are displayed in Object Explorer.

    -   For more information on Java connector methods, see [Java connector methods](../reference/java-connector-methods.md).
    -   For more information on Google Chrome and Microsoft Edge connector methods, see [Chromium connector methods](../reference/connectors-chrome-methods.md).

    -   For more information on Windows connector methods, see [Windows Connector methods](../reference/connectors-windows-methods.md).
    -   If you have captured a web application screen and you want to execute a custom JavaScript on it, you can use the ExecuteJavascript method.

8.  Capture as many screen elements as you need by using the Capture element dialog.

    To learn to use the Capture element dialog, see [Use the Capture element dialog](use-context-dialog.md).

    The captured screen elements appear under the captured application screen as elements.

    ![Captured screen controls.](../image/uac-connector-captured-controls.png)

9.  Drag the required method from the Object Explorer pane to the Design surface.

    The method is displayed with the application screen or element name in the Design surface.


## What to do next

Design the automation by using the different methods for the application screens and elements, and save the automation.

**Parent Topic:**[Universal app connector](../concept/universal-app-connector.md)

