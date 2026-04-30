---
title: Install Attended Robot
description: You can install the Attended Robot application in your Windows machine if you have the admin role.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Attended Robot, Attended Robot, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Install Attended Robot

You can install the Attended Robot application in your Windows machine if you have the admin role.

## Before you begin

Download and unzip the installation file for the Attended Robot application. For more information, see [Download the RPA applications from RPA Hub](../../rpa-hub/task/download-installer-rpa.md).

Ensure that you meet the hardware and software requirements.

The following hardware specifications list the minimum and recommended resources.

|Resource|Minimum|Recommended|
|--------|-------|-----------|
|CPU|Intel Processor \(1vCPU\)|Intel Processor \(4vCPU\)|
|RAM|4-GB RAM|8-GB RAM|
|Disk space|Minimum 20-GB free disk space after installing the OS, patches, and base software|Minimum 50-GB free disk space after installing the OS, patches, and base software|

-   **Software requirements**

    The software requirements are:

    -   Operating system: Microsoft Windows 10 or Windows 11 or Windows Server 2016 or Windows Server 2019
    -   NET framework: Windows 4.7.1 or greater.
    -   DPI scaling setting must be deactivated.

Microsoft Edge WebView2 Runtime is a prerequisite for the ServiceNow login screen to work with RPA users. The Microsoft Edge WebView2 Runtime is installed by default with only specific releases of Windows 10 OS. If it is not available, ensure to install the Microsoft Edge WebView2 Runtime.

For more information about the Microsoft Edge WebView2 Runtime, see [Delivering Microsoft Edge WebView2 Runtime to managed Windows 10 devices](https://blogs.windows.com/msedgedev/2022/12/14/delivering-microsoft-edge-webview2-runtime-to-managed-windows-10-devices). For more information about downloading the Microsoft Edge WebView2 Runtime MSI, see [Microsoft Edge WebView2](https://developer.microsoft.com/en-us/microsoft-edge/webview2/?form=MA13LH).

Role required: admin

## About this task

An attended robot is mapped to only one user.

## Procedure

1.  Locate and open the `Attended Robot.msi` file.

2.  In the Welcome to the Attended Robot Setup Wizard dialog box, select **Next**.

3.  In the Select Installation Folder dialog box, do one of the following actions to choose a folder:

    -   To install the application in the default folder, select **Next**.
    -   To install the application in a different folder, select the folder location in the **Folder** field or select **Browse** to select the folder, and then select **Next**.
4.  In the Confirm Installation dialog box, select **Next** to start the installation.

5.  After the installation is complete, in the Installation Complete dialog box, select **Close** to exit.


## Result

You can see the Attended Robot icon on your desktop.

## What to do next

Set up the Attended Robot application. For more information, see [Set up Attended Robot](set-up-rda-runtime.md).

