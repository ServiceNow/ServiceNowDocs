---
title: Set up Attended Robot
description: Establish a connection between the Attended Robot and the ServiceNow RPA Hub instance.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Attended Robot, Attended Robot, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Set up Attended Robot

Establish a connection between the Attended Robot and the ServiceNow RPA Hub instance.

Watch this video to learn about the configuration of Attended Robot.

Setup of Attended Robot application 

## Before you begin

Install the Attended Robot. For more information, see [Install Attended Robot](install-rda-runtime.md).

Role required: none

## About this task

Do this task when you’re setting up the Attended Robot for the first time unless you’re changing the RPA Hub instance.

If the Attended Robot is launched when the RPA Desktop Design Studio is open in your Windows machine and a new profile is added to the Attended Robot Connection Manager, it does not reflect in the RPA Desktop Design Studio Connection Manager. If a new profile is added to the RPA Desktop Design Studio Connection Manager, the entry that you added in the Attended Robot Connection Manager is overwritten. In such scenarios, restart RPA Desktop Design Studio when a profile is added in the Attended Robot Connection Manager.

## Procedure

1.  From your desktop, double-click the Attended Robot icon \(![Attended Robot icon.](../image/rda-robot-runtime-icon.png)\).

2.  In the Connection Manager dialog box, to add a new RPA Hub, select **Add New**.

    Do this step when you’re setting up the Attended Robot for the first time unless you’re changing the RPA Hub instance.

3.  In the Add ServiceNow Instance Details dialog box, fill in the fields.

<table id="table_sxd_pk3_grb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your ServiceNow RPA Hub instance. For example, `New Instance`

</td></tr><tr><td>

URL

</td><td>

Enter the ServiceNow RPA Hub instance URL. For example, `https://<instance name>.service-now.com/`.

</td></tr><tr><td>

Mark as default

</td><td>

Option to enable this instance as the default instance.Clearing this option opens the Connection Manager dialog box each time you double-click the Attended Robot icon.

</td></tr><tr><td>

Launch in default browser

</td><td>

Option to launch the login screen in the default browser.The Attended Robot is successfully connected to the instance after you have authenticated using the username and password.

</td></tr></tbody>
</table>4.  Select **Save**.

5.  To add the settings for an internet connection as per your company policies, do the following steps:

    1.  In the Connection Manager dialog box, in the Proxy Settings section, fill in the fields.

        |Field|Action|
        |-----|------|
        |Server Address|Enter the proxy server URL.|
        |Name|Enter your user name.|
        |Password|Enter the password.|
        |Save Password|Option to save the password.|

    2.  Select **Save**.

6.  In the Connection Manager dialog box, in the RPA Hub section, select an RPA Hub instance.

7.  In the ServiceNow dialog box, do any of the following actions:

    -   To set up the Attended Robot for the first time, select **Proceed**.
    -   To change the RPA Hub instance, select **Connect**.
8.  Enter your user name and password.

    If you have selected the **Launch in default browser** option, the login screen appears in the default browser.

9.  From the Domain list, select a domain.

10. Select **Log in**.

11. In the Connection Manager dialog box, set the permission for the Attended Robot application to connect to your ServiceNow instance and access data.

    -   To allow Attended Robot to connect to your ServiceNow instance and access data, select **Allow**.
    -   To prevent Attended Robot from connecting to your ServiceNow instance and accessing data, select **Deny**. You won't be able to proceed further.

## What to do next

Run an Attended Robot to execute the attended bot process. For more information, see [Run an automation using Attended Robot](run-rda-robot.md).

