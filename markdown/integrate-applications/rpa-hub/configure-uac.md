---
title: Use the Universal App Connector
description: Create automations for your Windows, Java, Google Chrome, and Edge browser-based applications by using the Universal App Connector \(UAC\). Configure the applications from a single, unified connector and capture the screens and elements or screen controls such as check boxes, and buttons. Use the methods of these screens and elements to build your automation.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Universal app connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Use the Universal App Connector

Create automations for your Windows, Java, Google Chrome, and Edge browser-based applications by using the Universal App Connector \(UAC\). Configure the applications from a single, unified connector and capture the screens and elements or screen controls such as check boxes, and buttons. Use the methods of these screens and elements to build your automation.

## Before you begin

Ensure that you have open or active Windows, Java, Google Chrome, or Edge applications.

Role required: None

## Procedure

1.  In the Toolbox pane, navigate to **Connectors**, and drag **Universal App Connector** to **Global Objects** in the Project Explorer pane.

    The connector is added as a **UniversalApplication** object under **Global Objects**.

2.  To rename **UniversalApplication**, right-click and select **Rename**.

3.  To use the methods at the **Universal App Connector** connector level, double-click the **UniversalApplication** object.

    For example, the Start method is used if you want the browser or application to start before interacting with any application screens or elements. For more information on how to use the Start method, see [Use the Start method](use-start-method.md).

    The methods appear in the Object Explorer pane.

4.  To configure the screens and elements in the UAC, do the steps.

    1.  Under Global Objects, right-click **UniversalApplication** and select **Configure**.

    2.  On the Configure screens and elements window, select the Choose from an open window drop-down \(![Choose from an open window drop-down.](../image/UAC-connector-select-application-icon.png)\) and select an application screen.

        ![Open applications.](../image/uac-connector-open-apps.png)

        **Note:**

        -   If no supported applications are open, the `App window not found message` is displayed.
        -   To display newly opened application screens on the list, select the Click to refresh windows icon \(![Click to refresh windows icon.](../image/refresh-uac-list.png)\).
    3.  To filter the opened applications by their type, select the filter application type icon \(![Filter application type icon.](../image/uac-connector-all-applications-filter.png)\) and select All or the application type.

        For example, if you select **Chrome**, only Google Chrome web pages appear in the **Choose from an open window** list.

    4.  To add the selected application screen, select **Add screen**.

        After you do this step, you can capture the screen elements to perform actions.

        The application screen appears under the Screens and elements pane.

        ![Application screen name appears under Screens and elements.](../image/uac-connector-application-screen-added.png)

    5.  To change the name of the screen, select the name of the application screen under the Screens and elements pane.

        The information of the selected application screen appears under the Properties pane.

    6.  Update the name of the application screen in the **Name** field and press **Enter**.

        The name of the application is updated in the Screens and elements pane.

    7.  To capture the elements from the screen, under the Screen and elements pane, right-click the added screen and select **Capture Element**.

        ![Capture Element option.](../image/uac-connector-capture-window.png)

        The focus is set on the application screen that you had captured and the capture elements dialog appears.

        ![Captured screen in focus and capture dialog appears.](../image/UAC-connector-screen-focus.png)

    8.  Capture as many screen elements as you need by using the Capture element dialog.

        To learn to use the Capture element dialog, see [Use the Capture element dialog](use-context-dialog.md).

        The captured screen elements appear under the captured application screen as elements.

        ![Captured screen controls.](../image/uac-connector-captured-controls.png)

5.  Use the screen match rules to edit to the values in the provided match rules to identify the screen uniquely.

    During the execution, the plugin must identify the target screen uniquely to automate actions on the screen. Examples of attributes are the title or URL of the application screen. The attributes appear under the **Screen match rules** pane on the **Configure elements and screens** window. The UAC uses these attributes to identify the screen first and perform actions on elements such as Click or Get Text.

    ![Screen match rules.](../image/uac-connector-screen-match-rules.png)

    The image below shows an example of multiple elements that match the same criteria given in the Match Attributes section. A multiple number of instances, if any, appears when you refresh the captured element, is indicated within the brackets in red. In such cases, you must tweak the attributes to select exactly the element that needs to be automated. The user can refresh to check if the selected criteria match exactly one element.

    ![Multiple instances of captured element.](../image/uac-connector-multiple-instances.png)

6.  Use the element match rules to edit the values in the provided **Locator** and the **Match Attributes** sections to identify an element uniquely.

    During the execution, the plugin must identify the target element uniquely to automate actions on the element. The attributes appear under the **Match Attributes** pane on the **Configure elements and screens** window. The UAC uses these attributes to identify the screen first and perform actions on elements such as Click or Get Text.

    The image shows the match rules of an element captured.

    ![Element and its match rules.](../image/uac-connector-child-element-match-rules.png)

7.  Use the locators of the captured elements to find the elements on the application screen.

    The UAC provides multiple locator types. For example, the XPath locator provides the XPath to the element.

    ![Element locators.](../image/uac-connector-element-attributes.png)

    1.  Under the Screens and elements pane, select an element under a screen.

    2.  From the **Locator** list, select one of the element locators.

<table id="table_d5c_1pn_rzb"><thead><tr><th>

Locator type

</th><th>

Application type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Id

</td><td>

Web, Java, and Windows

</td><td>

Unique identifier of the element if its defined in the target application.

</td></tr><tr><td>

Name

</td><td>

Web, Java, and Windows

</td><td>

Unique name of the element if its defined in the target application.

</td></tr><tr><td>

CssSelector

</td><td>

Web

</td><td>

The CSS selector that locates the captured web element. For example, `div#navbarNav > ul > li > a`. If a web application supports Shadow DOM, the CSS Selector shows the path with the shadow DOM elements. For example, `html > body > shop-app > /ShadowDom/ > app-header[id="header"] > app-toolbar > div:nth-of-type(3) > a > paper-icon-button > /ShadowDom/ > iron-icon[id="icon"]`

</td></tr><tr><td>

TagName

</td><td>

Web

</td><td>

Unique tag name of the web element.

</td></tr><tr><td>

JavaScript

</td><td>

Web

</td><td>

Allows the user to define a custom JavaScript code to locate an element.

</td></tr><tr><td>

XPath

</td><td>

Web

</td><td>

XPath to locate the web element. If a web application supports Shadow DOM, this locator shows the full XPath with the Shadow DOM elements. For example, `html > body > shop-app > /ShadowDom/ > iron-pages > shop-home > /ShadowDom/ > div > h2`.

</td></tr><tr><td>

Type

</td><td>

Java and Windows

</td><td>

Enables you to locate a screen element by its type. For example, button or text box.When you select the `Type` locator, the UAC connector populates the **Value** field with the type of the element.

</td></tr><tr><td>

Path

</td><td>

Java and Windows

</td><td>

Enables you to locate a screen element by specifying its position in the hierarchy of screen elements.When you select the `Path` locator, the UAC connector populates the **Value** field with the path of the element.

</td></tr><tr><td>

CustomPath

</td><td>

Windows

</td><td>

Enables you to fine-tune or trim the path to an element.

</td></tr></tbody>
</table>8.  To view the path to an iframe, if any, in a captured element, do the steps.

    1.  In the **Screens and elements** pane, select the element.

    2.  Select the **Advanced** tab.

        The iframe appears.

        ![iframe appears.](../image/uac-connnector-iframe.png)

    3.  From the **Locator** list, select a locator to find the path to the iframe.

        ![iframe locator.](../image/uac-connector-iframe-locator.png)

9.  Right-click the application screen or element to perform any additional operations.

    For information on the various additional operations that are available for the application screens and elements, see [Additional options for application screens and elements in Universal App Connector](../reference/contextmenu-application-screens.md).

10. Select **Done** after you finish configuring your application screens or elements.

    The application screens and their elements appear under the UAC object in **Global Objects**.

11. Double-click the required application screen or element and the Object Explorer pane is displayed listing the related methods.

    For example, if you select a Java application screen or element, the Java connector methods are displayed in Object Explorer.

    -   For more information on Java connector methods, see [Java connector methods](../reference/java-connector-methods.md).
    -   For more information on Google Chrome and Microsoft Edge connector methods, see [Chromium connector methods](../reference/connectors-chrome-methods.md).

    -   For more information on Windows connector methods, see [Windows Connector methods](../reference/connectors-windows-methods.md).
    -   If you have captured a web application screen and you want to execute a custom JavaScript on it, you can use the ExecuteJavascript method.

12. Drag the required method from the Object Explorer pane to the Design surface.

    The method is displayed with the application screen or element name in the Design surface.


## What to do next

Design the automation by using the different methods for the application screens and elements, and save the automation.

**Parent Topic:**[Universal app connector](../concept/universal-app-connector.md)

