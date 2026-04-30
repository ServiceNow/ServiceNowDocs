---
title: Chromium connector
description: The Chromium connector enables you to interact with various elements in web applications running on Google Chrome or Microsoft Edge Edge and build automations around them.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Chromium connector

The Chromium connector enables you to interact with various elements in web applications running on Google Chrome or Microsoft Edge Edge and build automations around them.

To use the Chromium connector, do the following actions:

-   Enable the latest versions of the ServiceNow RPA Edge Extension and the ServiceNow RPA Chrome Extension. To enable, see [Add the ServiceNow RPA Chrome extension](../../rpa-hub/task/add-google-chrome-extension-rpa.md) and [Add the ServiceNow RPA Edge extension](../task/add-servicenow-edge-extension.md).
-   Ensure you have installed the Chromium plugin on the RPA Desktop Design Studio. To install, see [Manage plugins in RPA Desktop Design Studio](../task/install-plugins-rpa-studio.md).
-   To use the Chromium connector, see [Use a connector in RPA Desktop Design Studio](../task/use-connector.md).
-   To configure the Google Chrome connector, see [Configure the Chromium connector](../task/configure-chrome-connector.md).
-   To expose the methods, see [Use connector method](../task/use-connector-method.md).
-   To use the methods, see [Use a component in RPA Desktop Design Studio](../task/configure-components.md).
-   If you've installed a hot fix for Chromium connector, to verify that the hot fix is accurately downloaded to your machine, perform the post requisite steps. For more information, see [Post requisites after installing a hot fix](../task/post-req-hot-fix-rpa.md).

Chrome connector methods are available at the following levels:

-   Application
-   Screen
-   Element

|Method level|Description|
|------------|-----------|
|Application|These methods can open a website on the Google Chrome browser. The connector sets up the browser and application for the other methods to execute.|
|Screen|These methods perform various actions on the screens that you have configured. For example, click a button.|
|Element|These methods perform various tasks on the various elements on the screen.|

**Note:** Automation support for frameset-based pages isn't available through the Chromium connector.

-   **[Configure the Chromium connector](../task/configure-chrome-connector.md)**  
Capture one or more web pages from the Google Chrome or Microsoft Edge browser and then the elements on the web pages by configuring the Chromium connector.
-   **[Use the Capture element dialog](../task/use-context-dialog.md)**  
Identify and capture the elements on a web-based, Java, or Windows application screen by using the Capture element dialog.
-   **[Chromium connector methods](../reference/connectors-chrome-methods.md)**  
The Chromium connector methods do different tasks on the applications, screens, and the elements on the screens of the Google Chrome and the Microsoft Edge browsers.
-   **[Add the ServiceNow RPA Edge extension](../task/add-servicenow-edge-extension.md)**  
Add the ServiceNow RPA Edge extension to your Edge browser to enable the Chromium connector to interact with the elements on the web applications that are opened in this browser.

**Parent Topic:**[Connectors](connectors.md)

