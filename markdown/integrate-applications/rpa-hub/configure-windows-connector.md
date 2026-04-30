---
title: Configure Windows connector
description: Configure the Windows connector to access its methods and build automation on a Windows application. It provides methods at different levels and you must first configure it to expose methods at all levels.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Windows connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Configure Windows connector

Configure the Windows connector to access its methods and build automation on a Windows application. It provides methods at different levels and you must first configure it to expose methods at all levels.

## Before you begin

Ensure at least one Windows application is open or active.

Role required: none

## Procedure

1.  In the Toolbox pane, navigate to **Connectors** &gt; **Windows Connector**.

2.  Drag the Windows connector under Global Objects in the Project Explorer.

3.  Under the Global Objects node, right-click the connector.

4.  Click **Configure**.

5.  In the **AVAILABLE WINDOWS** list, select the required application window.

    **Tip:** If the window doesn't appear in the list, click the refresh icon \(![Refresh icon.](../image/refresh-jav-program.png)\).

6.  Click **Add Window**.

7.  Under the WINDOWS section, right-click the name of the window.

8.  Click **Add Element**.

9.  Use the context dialog to capture elements.

    To use the context dialog, see [Use the Capture element dialog](use-context-dialog.md).

    **Important:** If the language of your Microsoft Windows machine is non-english, then an unhandled exception error message is displayed when you click the Target Objects Preview pane. Click **Ok** on the error message box to proceed configuring the connector.


**Parent Topic:**[Windows connector](../concept/windows-connector.md)

