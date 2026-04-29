---
title: Windows connector
description: The Windows connector enables you to perform various actions on the Windows applications, and their user interface elements. These actions are performed through the methods provided by the Windows connector. You must configure the connector to expose its methods.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Windows connector

The Windows connector enables you to perform various actions on the Windows applications, and their user interface elements. These actions are performed through the methods provided by the Windows connector. You must configure the connector to expose its methods.

You must first use, configure, and then expose the methods in the Windows connector to use its methods.

-   To use the Windows connector, see [Use a connector in RPA Desktop Design Studio](../task/use-connector.md).
-   To configure the Windows connector, see [Configure Windows connector](../task/configure-windows-connector.md).
-   To expose the methods, see [Use connector method](../task/use-connector-method.md).
-   To use the methods, see [Use a component in RPA Desktop Design Studio](../task/configure-components.md).

Windows connector methods are available at the following levels:

-   Connector
-   Screen
-   Element

|Method level|Description|
|------------|-----------|
|Connector|These methods enable you to perform actions on the connector to set a working directory, get the Windows handle, and more.|
|Screen|These methods perform various actions on the screens you have configured. For example, click a button.|
|Element|These methods perform various tasks on the various elements on the screen.|

**Important:** Windows connector uses Microsoft UI Automation Framework internally to interact with applications built for Windows desktop such as Win32, WPF platforms. Any known issue or limitation published by Microsoft for this framework are applicable.

-   **[Configure Windows connector](../task/configure-windows-connector.md)**  
Configure the Windows connector to access its methods and build automation on a Windows application. It provides methods at different levels and you must first configure it to expose methods at all levels.
-   **[Windows Connector methods](../reference/connectors-windows-methods.md)**  
The Windows methods in RPA Desktop Design Studio interact with the Windows applications to perform various tasks. The connector provides methods at different levels of the Windows applications.
-   **[Parameters of the Windows connector methods](../reference/method-parameter-windows.md)**  
Learn about the parameters of the Windows connector methods in RPA Desktop Design Studio.

**Parent Topic:**[Connectors](connectors.md)

