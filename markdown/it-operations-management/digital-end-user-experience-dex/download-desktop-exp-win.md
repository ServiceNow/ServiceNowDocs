---
title: Download the Desktop Assistant installer on Windows devices
description: Download the Desktop Assistant installer on your Windows device to install the Desktop Assistant application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/download-desktop-exp-win.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Download and install, Setting up Desktop Assistant, Configure, Digital End-User Experience, IT Operations Management]
---

# Download the Desktop Assistant installer on Windows devices

Download the Desktop Assistant installer on your Windows device to install the Desktop Assistant application.

## Before you begin

Role required: sn\_dex\_desktop.admin

## Procedure

1.  Navigate to **All** &gt; **Desktop Assistant** &gt; **Deployment** &gt; **Installer and Uninstaller**.

2.  In the Windows Download section of the Desktop Assistant Downloads page, select the download icon \(\[Omitted image "icon-download-blue.png"\] Alt text: Download icon\) for the **MSI \[x64 arch\]** installer.

    The `Desktop_Assistant_<Version>.msi` file is downloaded to your computer.

3.  Open the setup file and follow the steps in the installation wizard to complete the installation.


## Result

Desktop Assistant is installed. You see the Desktop Assistant application in the Start menu and the Desktop Assistant icon \(\[Omitted image "icon-desktop-exp.png"\] Alt text: Desktop Assistant icon\) in the system tray.

When you install Desktop Assistant by using the installer, the instance URL field on the login page is not populated automatically. As an administrator, you can update the instance URL in the Desktop Assistant configuration file. For more information, see [Update instance URL in the Desktop Assistant configuration file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/update-da-instance-url.md).

**Note:** Only an administrator must update the configuration file or make changes to it while deploying Desktop Assistant on devices.

