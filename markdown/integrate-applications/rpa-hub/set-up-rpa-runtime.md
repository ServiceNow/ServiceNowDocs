---
title: Set up Unattended Robot
description: Set up the Unattended Robot application to establish a connection between a robot and the ServiceNow RPA Hub instance.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Unattended Robot, Unattended Robot, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Set up Unattended Robot

Set up the Unattended Robot application to establish a connection between a robot and the ServiceNow RPA Hub instance.

Watch this video to learn about the configuration of Unattended Robot.Setup of Unattended Robot application 

## Before you begin

Install the Unattended Robot. For more information, see [Install Unattended Robot](install-rpa-runtime.md).

Install the Unattended Robot Login Agent. For more information, see [Install Unattended Robot Login Agent](install-rpa-runtime-login-agent.md).

If you are selecting **mTLS** as the type of the authentication in the following task, install a user certificate, if you have the admin role. For more information, see [Install the user-generated certificates](../../rpa-core/concept/use-user-certificates-rpa.md#).

Role required: sn\_rpa\_fdn.rpa\_robot \(for connection\); sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin \(for setup\)

## About this task

Do this task when you’re setting up the Unattended Robot application for the first time, unless you’re changing the RPA Hub instance.

## Procedure

1.  From your desktop, to open the Unattended Robot, do either of the following tasks:

    -   Double-click the Unattended Robot icon \(![Unattended Robot icon.](../image/rpa-robot-runtime-desktop-icon.png)\).
    -   In the notification area \(system tray\) in the taskbar, select and hold \(or right-click\) the Unattended Robot icon \(![Unattended Robot icon in the notification area.](../image/rpa-robot-runtime-desktop-icon.png)\) and select **Settings**.
    The Unattended Robot dialog is displayed.

2.  In the ServiceNow Unattended Robot dialog box, fill in the fields.

<table id="table_sxd_pk3_grb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

RPA Hub

</td><td>

Enter the ServiceNow RPA Hub instance URL. For example, `https://<instance name>.service-now.com/`.

</td></tr><tr><td>

Authentication

</td><td>

Select the type of authentication that you want to use:-   **mTLS**: Mutual Transport Layer Security. As a prerequisite, install the user certificate.
-   **Basic**: Authentication happens based on the user name and password.
 A warning icon is displayed in the taskbar to show that the robot is connected using the **Basic** authentication type.

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

Enter your user name.This field appears only when **Basic** is selected from the **Authentication** field.

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

