---
title: Configure the Internet Explorer connector
description: Access the IE connector methods at all levels by configuring the IE connector. When you configure the IE connector, you capture a screen and its elements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/configure-internet-explorer-connector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [IE connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Configure the Internet Explorer connector

Access the IE connector methods at all levels by configuring the IE connector. When you configure the IE connector, you capture a screen and its elements.

## Before you begin

Add the Internet Explorer plugin from the Plugins Manager. For more information about adding the SSH plugin, see [Manage plugins in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/install-plugins-rpa-studio.md).

Ensure that at least a website or an application on the Internet Explorer browser window is open or active.

Role required: none

## Procedure

1.  Navigate to **Connectors** &gt; **IE Connector**.

2.  Drag the IE Connector under Global Objects in the Project Explorer pane.

3.  Under the Global Objects, right-click the IE connector.

4.  Click **Configure**.

5.  In the AVAILABLE WEB PAGES list, select the required web page.

    **Tip:** If the window doesn't appear in the list, click the refresh icon \(\[Omitted image "refresh-jav-program.png"\] Alt text: Refresh icon.\).

6.  Click **Add Screen**.

    The web page appears under the WEB PAGES section.

7.  Under the WEB PAGES section, right-click the name of the web page.

    The screen is captured.

8.  Click **Capture Element**.

    For more information on the context dialog, see [Use the Capture element dialog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/use-context-dialog.md).

9.  Move the mouse device over the web page to capture the element.

    As the mouse device moves over the web page, the context dialog displays the following information of each element it passes.

    -   POSITION: Position of the element in the web page.
    -   TAG: Name of the element tag.
    -   NAME: Custom name of the element that the user enters. This field is used when an element is captured.
    \[Omitted image "context-dialox-img.png"\] Alt text: Context dialog

    As you place the mouse device over an element, a red boundary icon \(\[Omitted image "red-boundary-icon.png"\] Alt text: Red boundary icon.\) indicates the element.

10. In the context window, enter a custom name of the element in the **NAME** field.

    **Tip:** To stop the context window from moving, press and hold the **Ctrl** key.

11. To add the custom name, click the add name icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add name icon.\).

    The element is captured.

12. To close the context window, click the close icon \(\[Omitted image "close.png"\] Alt text: Close icon.\).

    Methods at the connector, application, and element levels are captured.

13. To view the methods at the connector, application, and element levels, double-click the required connector level under the Global Objects in the Project Explorer pane.

14. Repeat the steps to capture multiple elements.


**Parent Topic:**[IE connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/internet-explorer-connector.md)

