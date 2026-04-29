---
title: Install Unattended Robot Login Agent
description: You can install the Unattended Robot Login Agent application in your Windows machine if you have the admin role.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Unattended Robot, Workflow Data Fabric]
---

# Install Unattended Robot Login Agent

You can install the Unattended Robot Login Agent application in your Windows machine if you have the admin role.

## Before you begin

Ensure that you meet the following set up requirements:

-   An unattended robot is mapped to only one machine.
-   The Windows machine or the Virtual Machine \(VM\) is persistent and constantly on to run unattended robots.
-   If connected via Citrix, the Windows machine or the VM must not go to sleep mode.
-   Login agent clears the legal notice message if the **sn\_rpa\_fdn.bypass\_legal\_notice** system property is selected.

    For more information about this property, see [Configure RPA Hub properties](../../rpa-hub/reference/rpahub-sys-properties.md).

    If you don't want the unattended robot to clear the legal notice, turn off the legal notice by turning off through the Active Directory Organizational \(AD OU\) policy. This ensures that the Unattended Robot Login Agent can log in seamlessly.

-   Unattended Robot Login Agent can handle only login-related screens, such as  the Ctrl+Alt+Del screen and the User Name and Password screen.
-   The idle timeout setting is turned off for the VDI pool.
-   Communication with the ServiceNow instance host is enabled.

Download and unzip the installation file for the Unattended Robot application. For more information, see [Download the RPA applications from RPA Hub](../../rpa-hub/task/download-installer-rpa.md).

Role required: admin

## About this task

The Unattended Robot Login Agent is a software agent that you install on a Windows machine with Unattended Robot.

This login agent application is used to unlock or self-log in to the robot machine when an unattended bot process is triggered.

Unattended Robot Login Agent does not support Multi-Factor Authentication \(MFA\) login.

## Procedure

1.  Locate and open the `Unattended Robot Login Agent.msi` file.

2.  In the Welcome to the Unattended Robot Login Agent Setup Wizard dialog box, select **Next**.

3.  After the installation is complete, in the Installation Complete dialog box, select **Close** to exit.


## Result

You can see the following image on your Windows lock screen after installation.

![Snapshot of the Unattended Robot Login Agent that appears on your Windows lock screen.](../image/login-agent-rpa-runtime.png "Unattended Robot Login Agent that appears on your Windows lock screen")

## What to do next

Set up the Unattended Robot application. For more information, see [Set up Unattended Robot](set-up-rpa-runtime.md).

