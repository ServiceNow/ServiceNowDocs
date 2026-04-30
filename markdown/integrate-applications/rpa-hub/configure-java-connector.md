---
title: Configure the Java connector
description: Configure the Java connector to set up the Java application screens and elements on which the automation will be performed. After setting up, you can expose methods at the connector, screen, and element levels.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Java, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Configure the Java connector

Configure the Java connector to set up the Java application screens and elements on which the automation will be performed. After setting up, you can expose methods at the connector, screen, and element levels.

## Before you begin

Ensure you have installed the Java plugin on the RPA Desktop Design Studio. To install, see [Manage plugins in RPA Desktop Design Studio](install-plugins-rpa-studio.md).

Ensure that Java is installed on the computer.

Ensure that at least one Java application window is active or open.

Role required: none

## Procedure

1.  Navigate to **Connectors** &gt; **Java Connector**.

2.  Drag the Java connector under Global Objects in the Project Explorer pane.

3.  Under Global Objects, right-click the Java connector.

4.  Click **Configure**.

5.  In the AVAILABLE WINDOWS list, select a Java application.

    **Tip:** If the window doesn't appear in the list, click the refresh icon \(![Refresh icon.](../image/refresh-jav-program.png)\).

6.  Click **Add Window**.

    The screen is captured under the WINDOWS section.

7.  To add more applications, repeat the steps.

    To know more about the Java Connector window, see

8.  Under the WINDOWS section, right-click the name of the window.

9.  Click **Add Element**.

10. To capture elements, use the context dialog.

    To use the context dialog, see [Use the Capture element dialog](use-context-dialog.md).

11. To close the Java Connector window, click **OK**.

    The connector, screen and its elements are configured.![Connector levels](../image/connector-levels.png)


**Parent Topic:**[Java](../concept/java-connector.md)

