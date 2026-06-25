---
title: Download and install Desktop Assistant
description: Download and install Desktop Assistant by using operating system-specific installer commands, Desktop Assistant installers, or endpoint management solutions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-service-management/digital-end-user-experience-dex/download-desktop-experience.html
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Setting up DEX Desktop Assistant, Configuring Digital End-User Experience, Digital End-User Experience, IT Service Management]
---

# Download and install Desktop Assistant

Download and install Desktop Assistant by using operating system-specific installer commands, Desktop Assistant installers, or endpoint management solutions.

## Before you begin

Make sure that you have installed the Digital End-User Experience application. For more information, see [Install Digital End-User Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/digital-end-user-experience-dex/install-app-device-health.md).

**Note:** You can install Desktop Assistant on 75000 devices for each instance.

Role required: sn\_dex\_desktop.admin

## Procedure

1.  Navigate to **All** &gt; **Desktop Assistant** &gt; **Deployment** &gt; **Installer and Uninstaller**.

    \[Omitted image "desktop-exp-installer-download.png"\] Alt text: The Desktop Assistant Downloads page

2.  Download and install Desktop Assistant by using installer commands, Desktop Assistant installers, or endpoint management solutions.

    -   Download and install Desktop Assistant by executing OS-specific single-line installer commands.

        **Note:** You must have administrator privileges to run the single-line installer commands.

        1.  Select the copy command icon \(\[Omitted image "icon-installer-blue.png"\] Alt text: Copy command icon\) to copy the command or script to execute.
        2.  On your computer, open Terminal.app \(macOS\) or run PowerShell \(Windows\) as administrator.
        3.  Paste the command and press Enter.
        4.  When prompted for a password, enter your active directory password and press Enter.
        Desktop Assistant is installed, and the instance URL from the installer is automatically populated in the **Instance URL** field of the Desktop Assistant login page.

    -   Download and install Desktop Assistant by using the Desktop Assistant installer specific to your operating system.
        1.  For Windows devices, see [Download Desktop Assistant for Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/digital-end-user-experience-dex/download-desktop-exp-win.md).
        2.  For macOS devices, see [Download Desktop Assistant for Mac](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/digital-end-user-experience-dex/download-desktop-exp-mac.md).
    -   Install Desktop Assistant on multiple devices using endpoint management solutions such as Jamf and Microsoft Endpoint Configuration Manager \(MECM\).

        **Note:** You must have administrator privileges to install Desktop Assistant on multiple devices using endpoint management solutions.

        1.  Log in to your ServiceNow instance and download Desktop Assistant.
        2.  Deploy the Desktop Assistant file on multiple devices using an endpoint management solution.
        3.  Update the Desktop Assistant instance URL for all the devices on which you have installed Desktop Assistant.

            For more information, see [Update instance URL in the Desktop Assistant configuration file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/digital-end-user-experience-dex/update-da-instance-url.md).


## Result

Desktop Assistant is downloaded and installed.

