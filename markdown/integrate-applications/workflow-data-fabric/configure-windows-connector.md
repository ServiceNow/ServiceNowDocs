---
title: Configure Windows connector
description: Configure the Windows connector to access its methods and build automation on a Windows application. It provides methods at different levels and you must first configure it to expose methods at all levels.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/configure-windows-connector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Windows connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Configure Windows connector

Configure the Windows connector to access its methods and build automation on a Windows application. It provides methods at different levels and you must first configure it to expose methods at all levels.

## Before you begin

Add the Windows plugin from the Plugins Manager before using the connector. For more information about adding the SSH plugin, see [Manage plugins in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/install-plugins-rpa-studio.md).

Ensure at least one Windows application is open or active.

Role required: none

## Procedure

1.  In the Toolbox pane, navigate to **Connectors** &gt; **Windows Connector**.

2.  Drag the Windows connector under Global Objects in the Project Explorer.

3.  Under the Global Objects node, right-click the connector.

4.  Click **Configure**.

5.  In the **AVAILABLE WINDOWS** list, select the required application window.

    **Tip:** If the window doesn't appear in the list, click the refresh icon \(\[Omitted image "refresh-jav-program.png"\] Alt text: Refresh icon.\).

6.  Click **Add Window**.

7.  Under the WINDOWS section, right-click the name of the window.

8.  Click **Add Element**.

9.  Use the context dialog to capture elements.

    To use the context dialog, see [Use the Capture element dialog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/use-context-dialog.md).

    **Important:** If the language of your Microsoft Windows machine is non-english, then an unhandled exception error message is displayed when you click the Target Objects Preview pane. Click **Ok** on the error message box to proceed configuring the connector.


**Parent Topic:**[Windows connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/windows-connector.md)

