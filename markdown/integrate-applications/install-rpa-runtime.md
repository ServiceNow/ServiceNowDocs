---
title: Install Unattended Robot
description: You can install the Unattended Robot application in your Windows machine if you have the admin role.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Unattended Robot, Workflow Data Fabric]
---

# Install Unattended Robot

You can install the Unattended Robot application in your Windows machine if you have the admin role.

## Before you begin

Download and unzip the installation file for the Unattended Robot application. For more information, see [Download the RPA applications from RPA Hub](../../rpa-hub/task/download-installer-rpa.md).

![Download the Unattended Robot application from the RPA Downloads page.](../image/install-unattended-downloads-rpa.png "Download Unattended Robot application")

Ensure that you follow the hardware and software requirements. For more information, see [Requirements for Unattended Robot](../reference/requirements-unattended-robot.md).

Ensure that you meet the following set up requirements:

-   An unattended robot is mapped to only one machine. This is applicable for standard robot.
-   The Windows machine or the Virtual Machine \(VM\) is persistent and constantly on to run unattended robots.
-   If connected via Citrix, the Windows machine or the VM must not go to sleep mode.
-   The idle timeout setting is turned off for the VDI pool.
-   Communication with the ServiceNow instance host is enabled.
-   Verify that the **glide.cometd.websocket.enabled** system property is set to true in the ServiceNow instance, to ensure that the robot is connected to the instance via websocket.
-   Verify that the websockets are also enabled on the client machine where the unattended robot runs.

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

The installation of the Unattended Robot application is configured to function on a per-machine basis, with the default directory as `%ProgramFiles%\ServiceNow\Unattended Robot`.

## What to do next

Set up the Unattended Robot application. For more information, see [Set up Unattended Robot](set-up-rpa-runtime.md).

