---
title: Universal app connector
description: Create automations for your Windows, Java, and web applications by using the Universal App Connector \(UAC\) of RPA Desktop Design Studio. Configure the application screens and their elements from a single, unified connector instead of using the individual connectors of these applications.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Universal app connector

Create automations for your Windows, Java, and web applications by using the Universal App Connector \(UAC\) of RPA Desktop Design Studio. Configure the application screens and their elements from a single, unified connector instead of using the individual connectors of these applications.

UAC is automatically added as a default connector to any attended, unattended, or skilled automation project of RPA Desktop Design Studio. UAC currently supports Windows, Java, and web applications \( Google Chrome and Microsoft Edge browsers only\).

**Important:** It is recommended that you create automations for Windows, Java, and web applications using UAC instead of using their individual connectors. However, RPA Desktop Design Studio still supports automation projects that are designed using the individual connectors.

**Tip:** If you've installed a hot fix for UAC connector, to verify that the hot fix is accurately downloaded to your machine, perform the post requisite steps. For more information, see [Post requisites after installing a hot fix](../task/post-req-hot-fix-rpa.md).

UAC is added as an object to Global Objects in Project Explorer similar to how the other connectors are added. For more information on how to use a connector, see [Use connector method](../task/use-connector-method.md).

Add the screens and elements of Windows, Java, and web applications that are open in your machine while you configure UAC. Modify the screens and elements match rules during the configuration. Add the methods related to the screens and elements from the Design surface, and then build your automation.

-   **[Use the Universal App Connector](../task/configure-uac.md)**  
Create automations for your Windows, Java, Google Chrome, and Edge browser-based applications by using the Universal App Connector \(UAC\). Configure the applications from a single, unified connector and capture the screens and elements or screen controls such as check boxes, and buttons. Use the methods of these screens and elements to build your automation.
-   **[Use the Start method for Universal App Connector](../task/use-start-method.md)**  
Use the Start method to launch a browser or an application for the Universal App Connector \(UAC\) object. You can use this method if you want a browser or application to start before interacting with any application screens or elements.
-   **[Use the WaitForAnyScreen method for Universal App Connector](../task/use-the-wait-for-any-screen-method.md)**  
Find one or more application screens and optionally, their child elements within a time period that you specify and then perform actions that you specify.
-   **[Additional options for application screens and elements in Universal App Connector](../reference/contextmenu-application-screens.md)**  
Validate and perform additional operations for the added application screens and their captured elements. The additional options for the application screens are categorized based on the application type.

**Parent Topic:**[Connectors](connectors.md)

