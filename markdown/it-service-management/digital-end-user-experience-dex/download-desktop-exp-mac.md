---
title: Download Desktop Assistant installer on macOS devices
description: Download the Desktop Assistant installer on your macOS device to install the Desktop Assistant application.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Download and install, Set up Desktop Assistant, Configure, Digital End-User Experience, IT Service Management]
---

# Download Desktop Assistant installer on macOS devices

Download the Desktop Assistant installer on your macOS device to install the Desktop Assistant application.

## Before you begin

Role required: sn\_dex\_desktop.admin

## Procedure

1.  Navigate to **All** &gt; **Desktop Assistant** &gt; **Deployment** &gt; **Installer and Uninstaller**.

2.  In the macOS Download section of the Desktop Assistant Downloads page, select the download icon \(![](../image/icon-download-blue.png)\) for the installer you want to download.

    -   For macOS devices with Intel chips: Select the **Intel \[x64 arch\]** installer.
    -   For macOS devices with Apple Silicon chips: Select the **Apple Silicon \[x64 arch\]** installer.
    -   For macOS devices with either Intel or Apple Silicon chips: Select the **Universal Build** installer.
    The installer is downloaded to your computer.

3.  Double-click and open the downloaded installer file.

    -   For macOS devices with Intel chips: Open the `.x64.pkg` file.
    -   For macOS devices with Apple Silicon chips: Open the `-arm64.pkg` file.
    -   For macOS devices with either Intel or Apple Silicon chips: Open the `-universal.pkg` file.
4.  On the installation wizard, select **Continue** to proceed with the installation.

5.  In Destination Select, select the destination folder and then select **Continue**.

6.  In Installation Type, select **Install**.

7.  When prompted for a password, select **Use Password**, enter your password, and then select **Continue**.


## Result

The Desktop Assistant application is installed on your macOS device.

When you install Desktop Assistant by using the installer, the instance URL field on the login page is not populated automatically. As a system administrator, you can update the instance URL in the Desktop Assistant configuration file. For more information, see [Update instance URL in the Desktop Assistant configuration file](update-da-instance-url.md).

**Note:** Only the system administrator must update the configuration file or make changes to it while deploying Desktop Assistant on devices.

