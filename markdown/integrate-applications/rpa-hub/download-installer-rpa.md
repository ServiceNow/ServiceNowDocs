---
title: Download the RPA applications from RPA Hub
description: Download the Robotic Process Automation \(RPA\) applications in your Windows machine from RPA Hub as a prerequisite for installing the applications or upgrading them.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [msi rpa hub]
breadcrumb: [Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Download the RPA applications from RPA Hub

Download the Robotic Process Automation \(RPA\) applications in your Windows machine from RPA Hub as a prerequisite for installing the applications or upgrading them.

## Before you begin

You must do this task in the classic environment.

You need to have access to the RPA Hub instance for downloading the RPA applications.

Role required: admin, sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_business\_user, sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_support\_user, or sn\_rpa\_fdn.rpa\_admin

## About this task

Do this task to download the following RPA applications:

-   RPA Desktop Design Studio
-   Unattended Robot
-   Unattended Robot Login Agent
-   Attended Robot

**Important:** Ensure to upgrade the current installed MSIs \(RPA Desktop Design Studio, Attended Robot, and Unattended Robot\), if any by downloading the RPA applications.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Administration** &gt; **Downloads**.

2.  In the RPA Downloads page, do any of the following actions to download the required application:

    -   Select the download icon \(![Download icon.](../image/rpa-hub-download-icon.png)\).
    -   Select the copy link \(![Copy Link icon.](../image/rpa-hub-copyurl-icon.png)\). In a browser, right-click and select **paste and go** option.
    ![RPA Downloads.](../image/downloads-rpa.png "RPA Downloads")

    A dialog box might prompt you to save or open the zip file.

    **Note:** Depending on your browser setting, the browser might automatically save the file to your Downloads folder.

3.  From the downloaded zip file, extract the application installation file \(.msi file\).


## What to do next

Install RPA Desktop Design Studio. For more information, see [Install RPA Desktop Design Studio](../../rpa-studio/task/install-rpa-studio.md).

To run an unattended bot process, install Unattended Robot and install Unattended Robot Login Agent. For more information, see [Install Unattended Robot](../../rpa-runtime/task/install-rpa-runtime.md) and [Install Unattended Robot Login Agent](../../rpa-runtime/task/install-rpa-runtime-login-agent.md).

To run an attended bot process, install Attended Robot. For more information, see [Install Attended Robot](../../rda-runtime/task/install-rda-runtime.md).

Add the ServiceNow RPA Chrome extension to your Chrome browser to launch the Robotic Process Automation \(RPA\) applications in this browser and to establish a browser interaction. For more information, see [Add the ServiceNow RPA Chrome extension](add-google-chrome-extension-rpa.md).

