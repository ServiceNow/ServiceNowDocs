---
title: Set up RPA Desktop Design Studio
description: Set up RPA Desktop Design Studio to add your ServiceNow RPA Hub instance details in Connection Manager and to start using the application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Set up RPA Desktop Design Studio

Set up RPA Desktop Design Studio to add your ServiceNow RPA Hub instance details in Connection Manager and to start using the application.

Watch this video to learn about the configuration of RPA Desktop Design Studio.

Setup of RPA Desktop Design Studio application 

## Before you begin

Install RPA Desktop Design Studio. For more information on how to install it, see [Install RPA Desktop Design Studio](install-rpa-studio.md).

Role required: none

## About this task

You can do this task when you’re setting up RPA Desktop Design Studio for the first time or when you’re adding an RPA Hub instance.

## Procedure

1.  From your desktop, double-click the RPA Desktop Design Studio icon \(![RPA Desktop Design Studio icon.](../image/rpa-design-studio-icon.png)\).

    If you’re using RPA Desktop Design Studio for the first time, you can add the instance details in the Connection Manager dialog box.

    ![Add the ServiceNow instance in Connection Manager.](../image/add-instance-cm.png "Connection Manager")

2.  When you start using RPA Desktop Design Studio and want to add an instance from Connection Manager, select **Add New**.

    ![Add new instance from Connection Manager.](../image/addnew-cm.png "Add new instance from Connection Manager")

3.  On the form, fill in the fields.

<table id="table_sxd_pk3_grb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your ServiceNow RPA Hub instance for easy identification of the instance. For example, `Dev instance`.

</td></tr><tr><td>

URL

</td><td>

ServiceNow RPA Hub instance URL. For example, `https://<instance name>.service-now.com/`.

</td></tr><tr><td>

Mark as default

</td><td>

Option for enabling this instance as the default. RPA Desktop Design Studio launches each time by using this default instance.Clearing this option opens the Connection Manager dialog box each time you double-click the RPA Desktop Design Studio icon \(![RPA Desktop Design Studio icon.](../image/rpa-design-studio-icon.png)\).

</td></tr><tr><td>

Launch in default browser

</td><td>

Option for launching the instance in the default browser of your machine.

</td></tr></tbody>
</table>4.  If you want to add proxy settings for your internet connection according to the company policies, do the following actions:

    1.  In the **Proxy Settings** tab of the Connection Manager dialog box, fill in the fields for the server address, user name, password, and select the **Save Password** check box to save the password.

    2.  Select **Save**.

5.  Select **Proceed** and the plugins from the RPA Hub instance download to your machine.

    ![Downloading plugins from the RPA Hub instance.](../image/plugin-download.png "Downloading plugins from the RPA Hub instance")

    When the plugins download, the login page of your RPA Hub instance is displayed.

    ![Login page for the RPA Hub instance.](../image/connection-manager-auth.png "Login page for the RPA Hub instance")

    **Note:** If the error `Connection failed. Verify if the RPA Plugins are available in the ServiceNow instance.` is displayed when you start RPA Desktop Design Studio, select **OK** and configure a ServiceNow instance URL that has the RPA plugins installed. Restart RPA Desktop Design Studio and try again.

6.  Authenticate your connection by entering the user name and password of your RPA Hub instance and then select **Log in**.

    The RPA Hub instance authentication page is displayed.

    ![RPA Hub instance authentication.](../image/cm-authenticate.png "RPA Hub instance authentication")

    **Important:**

    -   When you enter credentials in the Connection Manager dialog box but don’t select the **Allow** button in the next screen, the session times out.
    -   You must authenticate your RPA Hub instance each time that you launch RPA Desktop Design Studio. If you don't authenticate and cancel the login operation, RPA Desktop Design Studio doesn't launch.
7.  Select **Allow**.

    The authentication is complete and the home page of RPA Desktop Design Studio is displayed.


## What to do next

You can start creating automations from the RPA Desktop Design Studio home page. For more information on how to create automations, see [Create an automation project manually](create-automation-project.md) or [Create an automation with Now Assist](create-automation-now-assist.md).

