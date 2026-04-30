---
title: Java
description: The Java connector enables you to perform various actions on Java applications as part of an automation in the RPA Desktop Design Studio
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Java

The Java connector enables you to perform various actions on Java applications as part of an automation in the RPA Desktop Design Studio

**Important:** Java connector uses Oracle Java Access Bridge internally to interact with applications built for Windows desktop. Any known issue or limitation published by Oracle for this library are applicable.

In the context of RPA Desktop Design Studio, a Java application has three levels- connector, screen, and element. The Java connector exposes methods at all three levels and these methods enable you to perform various actions at all three levels. For example, one method might click a minimized screen and bring it back to focus and then another method could click a button on the screen to submit data in that order.

To use the Java connector, do the following steps:

1.  Use the Java connector. See [Use a connector in RPA Desktop Design Studio](../task/use-connector.md).
2.  Configure the connector. See [Configure the Java connector](../task/configure-java-connector.md).
3.  Expose the methods. See [Use connector method](../task/use-connector-method.md).
4.  Use the methods. See [Use a component in RPA Desktop Design Studio](../task/configure-components.md).

Java connector methods are available at the following levels:

-   Connector
-   Screen
-   Element

|Method level|Description|
|------------|-----------|
|Connector|These methods perform various actions on the Java application. For example, you can set the working directory of the application.|
|Screen|These methods perform various tasks on the screen of the Java application. For example, a method can click a minimized screen and bring it back to focus.|
|Element|These methods perform various tasks on the elements in the screen of the Java application. For example, a method could click a button.|

**Warning:** The Java connector doesn't work on machines with Java 32-bit installations.

As a workaround, copy the WindowsAccessBridge-64.dll available on the Oracle website for the particular Java version to C:\\Windows\\System32 folder on the target machine.

-   **[Configure the Java connector](../task/configure-java-connector.md)**  
Configure the Java connector to set up the Java application screens and elements on which the automation will be performed. After setting up, you can expose methods at the connector, screen, and element levels.
-   **[Java connector methods](../reference/java-connector-methods.md)**  
The Java connector exposes methods at the connector, screen, and element levels. While all types of elements have common methods, they also have different methods.
-   **[Java connector properties](../reference/java-connector-properties.md)**  
View or update Java connector properties.

**Parent Topic:**[Connectors](connectors.md)

