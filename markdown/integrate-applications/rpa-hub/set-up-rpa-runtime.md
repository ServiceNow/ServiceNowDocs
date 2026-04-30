---
title: Set up Unattended Robot
description: Set up the Unattended Robot application to establish a connection between a robot and the ServiceNow RPA Hub instance.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configuring Unattended Robot, Unattended Robot, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Set up Unattended Robot

Set up the Unattended Robot application to establish a connection between a robot and the ServiceNow RPA Hub instance.

## Before you begin

Install the Unattended Robot. For more information, see [Install Unattended Robot](install-rpa-runtime.md).

Install the Unattended Robot Login Agent. For more information, see [Install Unattended Robot Login Agent](install-rpa-runtime-login-agent.md).

If you are selecting **mTLS** as the type of the authentication in the following task, install a user certificate, if you have the admin role. For more information, see [Install the user-generated certificates](../../rpa-core/concept/use-user-certificates-rpa.md#).

For high density robots, ensure that the following requirements are met:

-   Set up the environment for high density robots on a Windows Server machine. For more information, see [Set up Windows Server machine for high density robots](setup-windows-server-hdr.md).
-   Familiarize yourself with high density robots concepts. For more information, see [High density robots in Unattended Robot](../concept/high-density-robots-uat.md) and [High density robots in RPA Hub](../../rpa-hub/concept/high-density-robots-rpa-hub.md).

Role required: sn\_rpa\_fdn.rpa\_robot \(for connection\); sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin \(for setup\)

## About this task

Do this task when you’re setting up the Unattended Robot application for the first time, unless you’re changing the RPA Hub instance.

## Procedure

1.  From your desktop, to open the Unattended Robot, do either of the following tasks:

    -   Double-click the Unattended Robot icon \(![Unattended Robot icon.](../image/rpa-robot-runtime-desktop-icon.png)\).
    -   In the notification area \(system tray\) in the taskbar, select and hold \(or right-click\) the Unattended Robot icon \(![Unattended Robot icon in the notification area.](../image/rpa-robot-runtime-desktop-icon.png)\) and select **Settings**.
    The Unattended Robot dialog is displayed.

2.  In the ServiceNow Unattended Robot dialog box, under the RPA Hub section, fill in the fields.

<table id="table_sxd_pk3_grb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Instance URL

</td><td>

Enter the ServiceNow RPA Hub instance URL. For example, `https://<instance name>.service-now.com/`.

</td></tr><tr><td>

Authentication

</td><td>

Select the type of authentication that you want to use:-   **mTLS**: Mutual Transport Layer Security. As a prerequisite, install the user certificate.
-   **Basic**: Authentication happens based on the user name and password.

If the robot is connected using the **Basic** authentication type, a warning icon is displayed in the taskbar.

</td></tr><tr><td>

High density robots

</td><td>

Select this option to add multiple high density robots user profiles.High density robots leverage the Remote Desktop Services to execute multiple automations simultaneously in separate user sessions on the same Windows server machine.

For more information on high density robots, see [High density robots in RPA Hub](../../rpa-hub/concept/high-density-robots-rpa-hub.md) and [High density robots in Unattended Robot](../concept/high-density-robots-uat.md).

You must set up Windows server for high density robots. For more information, see [Set up Windows Server machine for high density robots](setup-windows-server-hdr.md).

</td></tr><tr><td>

Add profile

</td><td>

Select **Add profile** to connect the robots by adding the users associated to them. After a profile is added successfully, it fetches the associated robot for that user.Depending on your selection for the **Authentication** field, the respective fields appear.

When a new robot is created for a user who is already connected to the Unattended Robot, a connection is automatically established within a few minutes. However, if the user is not already connected, you must disconnect the Unattended Robot, add the new user, and then try connecting.

This field appears only when the **High density robots** option is selected.

</td></tr><tr><td>

Certificate

</td><td>

Perform the following actions to select a certificate:1.  Select the three-dot menu \(![Three-dot menu.](../image/rpa-runtime-run-three-dot-menu.png)\) next to the **Certificate** field.
2.  Select the installed client authentication certificate.

**Note:** You can only select a certificate that has the intended purpose as client authentication. If you select a certificate with any other intended purpose, an error is displayed.

3.  Select **OK**.
 This field appears only when **mTLS** is selected from the **Authentication** field.

</td></tr><tr><td>

Username

</td><td>

Enter your user name. This user must have a robot role for establishing connection. This field appears only when **Basic** is selected from the **Authentication** field.

</td></tr><tr><td>

Password

</td><td>

Enter the password.This field appears only when **Basic** is selected from the **Authentication** field.

</td></tr></tbody>
</table>3.  To add the settings for an internet connection as per your company policies, do the following steps:

    1.  In the ServiceNow Unattended Robot dialog box, under the Proxy Settings section, fill in the fields.

        |Field|Action|
        |-----|------|
        |Server Address|Enter the proxy server URL.|
        |Name|Enter your user name.|
        |Password|Enter the password.|

    2.  Select **Save**.

4.  Select **Connect**.


## What to do next

Run an unattended robot to execute the unattended bot process. For more information, see [Run an automation using Unattended Robot](run-rpa-robot.md).

**Related topics**  


[Install the user-generated certificates](../../rpa-core/concept/use-user-certificates-rpa.md#)

