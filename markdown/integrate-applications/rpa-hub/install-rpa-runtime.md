---
title: Install Unattended Robot
description: You can install the Unattended Robot application in your Windows machine if you have the admin role.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Unattended Robot, Unattended Robot, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Install Unattended Robot

You can install the Unattended Robot application in your Windows machine if you have the admin role.

## Before you begin

Ensure that you meet the infrastructure requirements.

The minimum requirements are as follows:

-   Intel Processor \(1vCPU\).
-   4-GB RAM.
-   Minimum 20-GB free disk space after installing the OS, patches, and base software.
-   Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019.
-   At least .NET Framework 4.7.1.
-   DPI scaling setting must be deactivated.

The recommended requirements are as follows:

-   Intel Processor \(4vCPU\).
-   8-GB RAM.
-   Minimum 50-GB free disk space after installing the OS, patches, and base software.
-   Microsoft Windows 10 or Windows Server 2016 or Windows Server 2019.
-   At least .NET Framework 4.7.1.
-   DPI scaling setting must be deactivated.

Ensure that you meet the following set up requirements:

-   An unattended robot is mapped to only one machine.
-   The Windows machine or the Virtual Machine \(VM\) is persistent and constantly on to run unattended robots.
-   If connected via Citrix, the Windows machine or the VM must not go to sleep mode.
-   Legal notices on the VDIs are turned off. RPA Hub can handle only login-related screens, such as  the Ctrl+Alt+Del screen and the User Name and Password screen. RPA Hub can't handle Legal Notice as this is an organization-specific setting. Therefore, it must be turned off through the Active Directory Organizational \(AD OU\) policy.
-   The idle timeout setting is turned off for the VDI pool.
-   Communication with the ServiceNow instance host is enabled.
-   Verify that the **glide.cometd.websocket.enabled** system property is set to true in the ServiceNow instance.
-   Verify that the websockets are also enabled on the client machine where the unattended robot runs.

Download and unzip the installation file for the Unattended Robot application. For more information, see [Download the RPA applications from RPA Hub](../../rpa-hub/task/download-installer-rpa.md).

![Download the Unattended Robot application from the RPA Downloads page.](../image/install-unattended-downloads-rpa.png "Download Unattended Robot application")

Role required: admin

## Procedure

1.  Locate and open the `Unattended Robot.msi` file.

2.  In the Welcome to the Unattended Robot Setup Wizard dialog box, select **Next**.

3.  In the Select Installation Folder dialog box, do one of the following actions to choose a folder:

    -   To install the application in the default folder, select **Next**.
    -   To install the application in a different folder, select the folder location in the **Folder** field or select **Browse** to select the folder, and then select **Next**.
4.  In the Confirm Installation dialog box, select **Next** to start the installation.

5.  After the installation is complete, in the Installation Complete dialog box, select **Close** to exit.


## Result

You can see the Unattended Robot icon on your desktop.

## What to do next

Set up the Unattended Robot application. For more information, see [Set up Unattended Robot](set-up-rpa-runtime.md).

