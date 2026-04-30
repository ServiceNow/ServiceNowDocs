---
title: Use a connector in RPA Desktop Design Studio
description: Connect to the various data sources and tools to create automation by using a connector in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using automations, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Use a connector in RPA Desktop Design Studio

Connect to the various data sources and tools to create automation by using a connector in RPA Desktop Design Studio.

## Before you begin

Ensure that the connector plug-in is installed and added to the RPA Desktop Design Studio application. For more information, see [Manage plugins in RPA Desktop Design Studio](install-plugins-rpa-studio.md).

Role required: none

## About this task

For a list of connectors and their methods, see [Connectors in RPA Desktop Design Studio](../reference/connectors-automation.md).

For details on the issues related to connectors, see [KB article KB1123555](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123555).

## Procedure

1.  Right-click **Global Objects** in the Project Explorer pane and select **Add Connectors**.

    The Add Connector dialog box is displayed.

2.  Select the required connectors and click **Add Connectors**.

    The connectors are added to Global Objects. You can also drag and drop the required connector from the Toolbox pane to Global Objects.

    **Note:** If you add multiple instances of the same connector to Global Objects, each duplicate instance is appended with the numerical value of the duplication. For example, if you add 3 instances of the Email connector to Global Objects, they appear as Email, Email\_2, and Email\_3.

3.  To provide the connector a custom name, perform the following steps.

    1.  Double-click the connector under Global Objects.

    2.  Enter a custom name of the connector in the Name field under the Properties pane.

4.  In the Project Explorer pane, double-click the connector under Global Objects.

    Some connectors provide additional levels and methods for each level. To know more about the levels, see [Understand levels of connector methods](../concept/understand-connector-method-levels.md).

    The Object Explorer lists all methods of the connector.

5.  Drag a method to the Design surface.

6.  Configure the input fields.

    For more information, see [Configure port properties](configure-input-port-properties.md).

7.  Connect the control ports of the method to the corresponding ports of another method or component.


-   **[Use connector method](use-connector-method.md)**  
Expose and then use the methods within a connector to perform all the actions that the connector can do.
-   **[Connectors in RPA Desktop Design Studio](../reference/connectors-automation.md)**  
Learn about the connectors that you can use in RPA Desktop Design Studio to create an automation.
-   **[Understand levels of connector methods](../concept/understand-connector-method-levels.md)**  
Some connectors in the RPA Desktop Design Studio provide methods that interact with various applications at different levels. For example, the Chrome connector provides methods that interact with applications and their elements open in a Google Chrome browser to perform specific Robotic Process Automation tasks.

**Parent Topic:**[Using automations](../concept/rpa-studio-use.md)

