---
title: Download and install Desktop Assistant
description: Download and install Desktop Assistant by using operating system-specific installer commands, Desktop Assistant installers, or endpoint management solutions.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 2
breadcrumb: [Set up Desktop Assistant, Configure, Digital End-User Experience, IT Service Management]
---

# Download and install Desktop Assistant

Download and install Desktop Assistant by using operating system-specific installer commands, Desktop Assistant installers, or endpoint management solutions.

## Before you begin

-   Make sure that you have installed the Digital End-User Experience application. For more information, see [Install Digital End-User Experience](install-app-device-health.md).
-   Make sure that you install Desktop Assistant client version 2.6.0 or higher on end-user computers, as this is the minimum version supported by this version of the Desktop Assistant application.

**Note:** You can install Desktop Assistant on 75000 devices for each instance.

Role required: admin, sn\_dex\_desktop.admin

## Procedure

1.  Navigate to **All** &gt; **Desktop Assistant** &gt; **Deployment** &gt; **Installer and Uninstaller**.

2.  Download and install Desktop Assistant by using installer commands, Desktop Assistant installers, or endpoint management solutions.

<table id="choicetable_zv4_ylt_fgc"><thead><tr><th align="left" id="d248474e134">

Option

</th><th align="left" id="d248474e137">

Steps

</th></tr></thead><tbody><tr><td id="d248474e143">

**OS-specific single-line installer commands**

</td><td>

**Note:** You must have administrator privileges to run the single-line installer commands.

 1.  In the Single-line Installer commands table, select the Copy single line install command icon ![](../image/icon-installer-blue.png) for your operating system.
2.  On your computer, open Terminal.app \(macOS\) or run PowerShell \(Windows\) as administrator.
3.  Paste the command and press Enter.
4.  When prompted for a password, enter your active directory password and press Enter.
 Desktop Assistant is installed, and the instance URL from the installer is automatically populated in the **Instance URL** field of the Desktop Assistant login page.

</td></tr><tr><td id="d248474e192">

**Desktop Assistant installer specific to your operating system**

</td><td>

1.  For Windows devices, see [Download Desktop Assistant installer on Windows devices](download-desktop-exp-win.md).
2.  For macOS devices, see [Download Desktop Assistant installer on macOS devices](download-desktop-exp-mac.md).


</td></tr><tr><td id="d248474e250">

**Endpoint management solutions like Jamf or Microsoft Endpoint Configuration Manager \(MECM\) to install on multiple devices**

</td><td>

**Note:** You must have administrator privileges to install Desktop Assistant on multiple devices using endpoint management solutions.

 1.  Log in to your ServiceNow instance and download Desktop Assistant.
2.  Deploy the Desktop Assistant installation file on multiple devices using an endpoint management solution.

For deployment on Windows devices using Microsoft Intune, refer to article [KB2324452](https://support.servicenow.com/kb?sys_kb_id=bd1205e7973e2e50f03d739c1253af2a&id=kb_article_view) on the Now Support Knowledge Base.

3.  Update the Desktop Assistant instance URL for all the devices on which you have installed Desktop Assistant.

For more information, see [Update instance URL in the Desktop Assistant configuration file](update-da-instance-url.md).

</td></tr></tbody>
</table>    **Note:** The guided setup experience helps you install the Desktop Assistant on your employee's device.

    This guided setup provides guidance to install the Desktop Assistant.

    ![Guided setup DEX Desktop Assistant](../image/gs-dex-da.png)


## Result

Desktop Assistant is downloaded and installed.

