---
title: Understand levels of connector methods
description: Some connectors in the RPA Desktop Design Studio provide methods that interact with various applications at different levels. For example, the Chrome connector provides methods that interact with applications and their elements open in a Google Chrome browser to perform specific Robotic Process Automation tasks.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use a connector, Use, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Understand levels of connector methods

Some connectors in the RPA Desktop Design Studio provide methods that interact with various applications at different levels. For example, the Chrome connector provides methods that interact with applications and their elements open in a Google Chrome browser to perform specific Robotic Process Automation tasks.

## Connectors with different levels of methods

The RPA Desktop Design Studio provides connectors that interact with various applications at different levels.

|Connector name|What does it do?|
|--------------|----------------|
|Chrome|Provides methods that interact with applications open in the Google Chrome browser.|
|Internet Explorer \(IE\)|Provides methods that interact with applications open in the IE browser.|
|Java|Provides methods that interact with Java-based applications.|
|Windows|Provides methods that interact with Windowsapplications.|
|Terminal \(Mainframe\)|Provides methods that interact with Mainframe applications.|

## Know the different levels of methods

The methods in the connectors interact at different levels in the applications.

|Method level|What does it do?|Example|
|------------|----------------|-------|
|Connector|Interacts with the connector.|The Chrome connector interacts with the connector under the Global Objects in the Project Explorer and exposes the methods.|
|Screen|Interacts with the application.|The ServiceNow website opened in the Google Chrome browser.|
|Element|Interacts with elements in the application.|A text box in the ServiceNow website open in the Google Chrome browser.|

## Configure the connectors

To access the various methods, you must first configure the connectors.

-   [Configure the Chromium connector](../task/configure-chrome-connector.md)
-   [Configure the Internet Explorer connector](../task/configure-internet-explorer-connector.md)
-   [Configure the Java connector](../task/configure-java-connector.md)
-   [Configure the Terminal connector](configure-terminal-connector.md)
-   [Configure Windows connector](../task/configure-windows-connector.md)

## Expose the methods at different levels

After configuration, you can expose the methods at different levels. The methods appear in the Object Explorer pane.

![Methods at all levels.](../image/methods-all-levels.png)

**Parent Topic:**[Use a connector in RPA Desktop Design Studio](../task/use-connector.md)

