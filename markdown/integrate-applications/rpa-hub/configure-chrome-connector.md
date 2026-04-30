---
title: Configure the Chromium connector
description: Capture one or more web pages from the Google Chrome or Microsoft Edge browser and then the elements on the web pages by configuring the Chromium connector.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Chromium connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Configure the Chromium connector

Capture one or more web pages from the Google Chrome or Microsoft Edge browser and then the elements on the web pages by configuring the Chromium connector.

## Before you begin

Software prerequisites: The ServiceNow, Inc. RPA Google Chrome and the ServiceNow® Store RPA Microsoft Edge extensions are added. To add the extensions, see:

-   [Add the ServiceNow RPA Edge extension](add-servicenow-edge-extension.md).
-   [Add the ServiceNow RPA Chrome extension](../../rpa-hub/task/add-google-chrome-extension-rpa.md).

Ensure you have installed the Chromium plugin on the RPA Desktop Design Studio. To install, see [Manage plugins in RPA Desktop Design Studio](install-plugins-rpa-studio.md).

Ensure that at least one website or application is open or active on both the Microsoft Edge and the Google Chrome browsers.

Frame set automation is not supported when using the Chromium connector \(Google Chrome/Microsoft Edge\).

Role required: none

## Procedure

1.  Navigate to **Connectors** &gt; **Chromium Connector**.

2.  Drag the Chromium connector under Global Objects in the Project Explorer pane.

3.  Under the Global Objects, right-click the Chromium connector.

4.  Click **Configure**.

5.  In the Chromium Connector window, select **Edge** or **Chrome**.

6.  To load the window, click the refresh icon \(![Refresh icon.](../image/refresh-jav-program.png)\).

7.  In the list, select the required screen.

    ![Select required screen.](../image/chromium-add-screen.png)

8.  Click **Add Screen**.

    The screen is captured in the WEB PAGES section.

9.  Under the WEB PAGES section, right-click the name of the web page.

10. Click **Capture Element**.

11. Use the context dialog to capture the elements.

    To use the context dialog, see [Use the Capture element dialog](use-context-dialog.md).


**Parent Topic:**[Chromium connector](../concept/chrome-connector.md)

