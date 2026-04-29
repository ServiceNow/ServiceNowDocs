---
title: Universal app connector
description: Create automations for your Windows, Java, and web applications by using the Universal App Connector \(UAC\) of RPA Desktop Design Studio. Configure the application screens and their elements from a single, unified connector instead of using the individual connectors of these applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Universal app connector

Create automations for your Windows, Java, and web applications by using the Universal App Connector \(UAC\) of RPA Desktop Design Studio. Configure the application screens and their elements from a single, unified connector instead of using the individual connectors of these applications.

## How UAC works

UAC is automatically added as a default connector to any attended, unattended, or skilled automation project of RPA Desktop Design Studio. UAC currently supports Windows, Java, and web applications \( Google Chrome and Microsoft Edge browsers only\).

**Important:** It is recommended that you create automations for Windows, Java, and web applications using UAC instead of using their individual connectors. However, RPA Desktop Design Studio still supports automation projects that are designed using the individual connectors.

**Tip:** If you've installed a hot fix for UAC connector, to verify that the hot fix is accurately downloaded to your machine, perform the post requisite steps. For more information, see [Post requisites after installing a hot fix](../task/post-req-hot-fix-rpa.md).

UAC is added as an object to Global Objects in Project Explorer similar to how the other connectors are added. For more information on how to use a connector, see [Use connector method](../task/use-connector-method.md).

Add the screens and elements of Windows, Java, and web applications that are open in your machine while you configure UAC. Modify the screens and elements match rules during the configuration. Add the methods related to the screens and elements from the Design surface, and then build your automation.

For more information on using a UAC, see [Use the Universal App Connector](../task/configure-uac.md).

## Modes in UAC for Windows applications

Starting from Yokohama release, Active Accessibility is supported when adding elements in the Universal App Connector, for Windows applications.

Select the mode, UI automation or active accessibility, while capturing the elements and showing the captured elements. The mode determines which internal library is used for automating Windows applications. UI automation mode refers to UI automation library and active accessibility refers to active accessibility library of Microsoft. Active accessibility mode is for legacy Windows applications.

To capture the elements from the screen, under the Screen and elements pane, right-click the added screen and select **Capture Element**. There are two modes **UIA** and **AA**. **UIA** is the default mode.

![UIA and AA modes appear when you capture an element in Windows application screen.](../image/uac-capture-elements-both-modes.png "Modes in Capture element")

For more information about capturing an element in the Windows application, see [Use the Universal App Connector](../task/configure-uac.md).

From the Screen and elements pane, right-click the added screen and select **Show Elements** to display all the existing elements in the target application screen in a tree view. There are two modes **UI Automation** and **Active Accessibility**. **UI Automation** is the default mode.

![UI Automation and Active Accessibility modes appear when you select Show Elements option from the Windows application screen.](../image/uac-show-elements-both-modes.png "Modes in Show Elements options")

For more information about showing captured elements of the Windows application, see [Additional options for application screens and elements in Universal App Connector](../reference/contextmenu-application-screens.md).

For more information about the methods for UI Automation mode and Active Accessibility mode, see [Methods of UI Automation mode and Active Accessibility mode](../reference/uac-windows-uia-aa-methods.md).

-   **[Use the Universal App Connector](../task/configure-uac.md)**  
Create automations for your Windows, Java, Google Chrome, and Edge browser-based applications by using the Universal App Connector \(UAC\). Configure the applications from a single, unified connector and capture the screens and elements or screen controls such as check boxes, and buttons. Use the methods of these screens and elements to build your automation.
-   **[Use the Click method for Universal App Connector](../task/use-click-method-uac.md)**  
Use the Click method to perform a click action on an element.
-   **[Use the GetValue method for Universal App Connector](../task/use-getvalue-method-uac.md)**  
Use the GetValue method to retrieve a value from an element.
-   **[Use the SetValue method for Universal App Connector](../task/use-setvalue-uac.md)**  
Use the SetValue method to assign a specified value into an element.
-   **[Use the Start method for Universal App Connector](../task/use-start-method.md)**  
Use the Start method to launch a browser or an application for the Universal App Connector \(UAC\) object. You can use this method if you want a browser or application to start before interacting with any application screens or elements.
-   **[Use the WaitForAnyScreen method for Universal App Connector](../task/use-the-wait-for-any-screen-method.md)**  
Find one or more application screens and optionally, their child elements within a time period that you specify and then perform actions that you specify.
-   **[Find the elements on the application screen](../task/find-elements-screen-uac.md)**  
Use the locators of the captured elements to find the elements on the application screen while using the Universal App Connector \(UAC\) in the RPA Desktop Design Studio.
-   **[Additional options for application screens and elements in Universal App Connector](../reference/contextmenu-application-screens.md)**  
Validate and perform additional operations for the added application screens and their captured elements. The additional options for the application screens are categorized based on the application type.
-   **[Methods of UI Automation mode and Active Accessibility mode](../reference/uac-windows-uia-aa-methods.md)**  
The Universal app connector provides multiple methods that perform various actions when screens are captured in Windows applications, for UI Automation mode and Active Accessibility mode.

**Parent Topic:**[Connectors](connectors.md)

