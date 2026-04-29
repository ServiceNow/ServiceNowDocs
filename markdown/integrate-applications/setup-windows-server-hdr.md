---
title: Set up Windows Server machine for high density robots
description: Set up the environment for high density robots on a Windows Server machine by installing a Remote Desktop Session Host. Then, add robot user names who can connect to the machine. It enables them to establish Remote Desktop Protocol \(RDP\) connection to the Windows Server machine.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Unattended Robot, Workflow Data Fabric]
---

# Set up Windows Server machine for high density robots

Set up the environment for high density robots on a Windows Server machine by installing a Remote Desktop Session Host. Then, add robot user names who can connect to the machine. It enables them to establish Remote Desktop Protocol \(RDP\) connection to the Windows Server machine.

## Before you begin

Familiarize yourself with high density robots concepts. For more information, see [High density robots in Unattended Robot](../concept/high-density-robots-uat.md) and [High density robots in RPA Hub](../../rpa-hub/concept/high-density-robots-rpa-hub.md).

The Remote Desktop Session Host service requires a valid license.

Ensure that you follow the hardware and software requirements. For more information, see [Requirements for Unattended Robot](../reference/requirements-unattended-robot.md).

Role required: admin

## Procedure

1.  Perform the following steps in your Windows Server machine to install the Remote Desktop Session Host.

    1.  Open Server Manager.

    2.  In the Dashboard panel, select **Manage** and then select **Add Roles and Features**.

        ![Server Manager Dashboard panel shows Manage option as selected and Add Roles and Features as selected.](../image/server-mgr-windows-setup-hdr.png "Server Manager Dashboard panel")

        The **Add Roles and Features Wizard** opens.

    3.  Follow the steps in the wizard until you reach the **Select server roles** window.

    4.  In the Roles section, from the Remote Desktop Services list, select the **Remote Desktop Session Host** option.

        ![Remote Desktop Session Host option is selected in the Select server roles window.](../image/select-server-roles-hdr.png "Select server roles")

    5.  In the Add Roles and Features Wizard dialog box, select **Add Features**.

        ![Add features in the Add Roles and Features Wizard dialog box.](../image/add-roles-features-hdr.png "Add Roles and Features Wizard dialog box")

        It returns to the wizard.

    6.  Follow the steps in the wizard until you reach the **Confirm installation selections** window.

    7.  Select **Install**.

2.  Configure the following settings to add users and edit policies:

    1.  Navigate to the **Local Group Policy Editor** and then, navigate to **Computer Configuration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **Remote Desktop Services** &gt; **Remote Desktop Session Host** &gt; **Security**.

    2.  Disable the **Always prompt for password upon connection** policy.

    3.  Enable the **Require user authentication for remote connections by using Network Level Authentication** policy for enhanced security and always authenticate prior establishing session to RDP.

        ![Local Group Policy Editor window shows selected settings that must be configured.](../image/policy-hdr-setup-windows-server.png "Configure policies in the Local Group Policy Editor")

    4.  Ensure that the Windows user mapped to the robots in the Process Robot Credentials tab of the bot process must be in the **Remote Desktop Users** group.


## What to do next

Restart the Windows Server machine after the installation is complete.

Enable the high density robot option in RPA Hub. For more information, see [Create an unattended robot in RPA Hub](../../rpa-hub/task/create-unattended-robot.md).

[Install Unattended Robot](install-rpa-runtime.md).

Add user profiles in the Unattended Robot application, so that multiple robots can execute jobs concurrently. For more information, see [Set up Unattended Robot](set-up-rpa-runtime.md)

