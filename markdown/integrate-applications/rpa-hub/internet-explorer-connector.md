---
title: IE connector
description: The Internet Explorer \(IE\) connector enables you to perform various actions on the IE browser, applications, and their screen elements on the browser. For example, you can execute a method to open a website. You perform the actions through the methods.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# IE connector

The Internet Explorer \(IE\) connector enables you to perform various actions on the IE browser, applications, and their screen elements on the browser. For example, you can execute a method to open a website. You perform the actions through the methods.

You must first use, configure, and then expose the methods in the IE connector to use its methods.

-   To use the IE connector, see [Use a connector in RPA Desktop Design Studio](../task/use-connector.md).
-   To configure the IE connector, see [Configure the Internet Explorer connector](../task/configure-internet-explorer-connector.md).
-   To expose the methods, see [Use connector method](../task/use-connector-method.md).
-   To use the methods, see [Use a component in RPA Desktop Design Studio](../task/configure-components.md).

IE connector methods are available at the following levels:

-   Connector
-   Screen
-   Element

|Method level|Description|
|------------|-----------|
|Connector|These methods can open a website on the IE browser. It sets up the browser and application for the other methods to execute.|
|Screen|These methods perform various actions on the screens you have configured. For example, click a button.|
|Element|These methods perform various tasks on the various elements on the screen.|

**Note:** Automation support for frameset-based pages isn't available through the Chromium connector.

-   **[Configure the Internet Explorer connector](../task/configure-internet-explorer-connector.md)**  
Access the IE connector methods at all levels by configuring the IE connector. When you configure the IE connector, you capture a screen and its elements.
-   **[IE Connector methods](../reference/connectors-ie-methods.md)**  
The IE connector methods perform different tasks on the IE connector, screens, and the elements on the screens. The methods are available at the connector, screen, and the element levels and you can expose the methods by completing appropriate steps.
-   **[Parameters of the IE connector methods](../reference/method-parameter-ie.md)**  
Learn about the parameters of the Microsoft IE Connector \(Internet Explorer\) methods in RPA Desktop Design Studio.

**Parent Topic:**[Connectors](connectors.md)

