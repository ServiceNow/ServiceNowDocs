---
title: Configure the Internet Explorer connector
description: Access the IE connector methods at all levels by configuring the IE connector. When you configure the IE connector, you capture a screen and its elements.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [IE connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Configure the Internet Explorer connector

Access the IE connector methods at all levels by configuring the IE connector. When you configure the IE connector, you capture a screen and its elements.

## Before you begin

Add the Internet Explorer plugin from the Plugins Manager. For more information about adding the SSH plugin, see [Manage plugins in RPA Desktop Design Studio](install-plugins-rpa-studio.md).

Ensure that at least a website or an application on the Internet Explorer browser window is open or active.

Role required: none

## Procedure

1.  Navigate to **Connectors** &gt; **IE Connector**.

2.  Drag the IE Connector under Global Objects in the Project Explorer pane.

3.  Under the Global Objects, right-click the IE connector.

4.  Click **Configure**.

5.  In the AVAILABLE WEB PAGES list, select the required web page.

    **Tip:** If the window doesn't appear in the list, click the refresh icon \(![Refresh icon.](../image/refresh-jav-program.png)\).

6.  Click **Add Screen**.

    The web page appears under the WEB PAGES section.

7.  Under the WEB PAGES section, right-click the name of the web page.

    The screen is captured.

8.  Click **Capture Element**.

    For more information on the context dialog, see [Use the Capture element dialog](use-context-dialog.md).

9.  Move the mouse device over the web page to capture the element.

    As the mouse device moves over the web page, the context dialog displays the following information of each element it passes.

    -   POSITION: Position of the element in the web page.
    -   TAG: Name of the element tag.
    -   NAME: Custom name of the element that the user enters. This field is used when an element is captured.
    ![Context dialog](../image/context-dialox-img.png)

    As you place the mouse device over an element, a red boundary icon \(![Red boundary icon.](../image/red-boundary-icon.png)\) indicates the element.

10. In the context window, enter a custom name of the element in the **NAME** field.

    **Tip:** To stop the context window from moving, press and hold the **Ctrl** key.

11. To add the custom name, click the add name icon \(![Add name icon.](../image/add-image-icon.png)\).

    The element is captured.

12. To close the context window, click the close icon \(![Close icon.](../image/close.png)\).

    Methods at the connector, application, and element levels are captured.

13. To view the methods at the connector, application, and element levels, double-click the required connector level under the Global Objects in the Project Explorer pane.

14. Repeat the steps to capture multiple elements.


**Parent Topic:**[IE connector](../concept/internet-explorer-connector.md)

