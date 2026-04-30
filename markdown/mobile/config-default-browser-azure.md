---
title: Configure the default authentication browser for ServiceNow mobile apps in Microsoft Azure
description: Learn how to configure the default authentication browser for your ServiceNow mobile apps managed by Microsoft Azure.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Intune, Device management, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure the default authentication browser for ServiceNow mobile apps in Microsoft Azure

Learn how to configure the default authentication browser for your ServiceNow mobile apps managed by Microsoft Azure.

## Before you begin

The following steps describe how to add your Intune integrated apps to an existing configuration policy. For information on creating configuration policies, refer to your Microsoft Azure documentation.

Role required: Microsoft Intune admin

## Procedure

1.  Log in to the Microsoft Endpoint Manager admin center at `https://endpoint.microsoft.com`.

2.  In the menu on the left side of the screen, navigate to **Apps**.

    ![Microsoft Endpoint Manager admin center menu showing the 'Apps' option.](../image/intune-mdm-config-select-apps.png)

3.  In the menu on the left side of the screen, select **App configuration policies**.

4.  Open the app configuration policy where you want to add your ServiceNow mobile apps.

5.  To the right of the **Settings** header, click **Edit**.

    ![Microsoft Endpoint Manager admin center shwoing where you can edit the app config properties.](../image/intune-mdm-config-def-browser.png)

6.  In the **General configuration settings** section, add the following **Name** and **Value** entries:

<table id="table_pph_jdz_4lb"><thead><tr><th>

Name

</th><th>

Value

</th></tr></thead><tbody><tr><td>

SNDefaultInstanceURL

</td><td>

https://INSTANCENAME.service-now.com/**Note:** Replace INSTANCENAME with the name of your instance.

</td></tr><tr><td>

SNAuthenticationBrowseriOS

</td><td>

Enter the value for the browser to use for apps on iOS mobile devices. For more information and a list of values, see [AppConfig for Mobile Apps](../reference/appconfig.md)

</td></tr><tr><td>

SNAuthenticationBrowserAndroid

</td><td>

Enter the value for the browser to use for apps on Android mobile devices. For more information and a list of values, see [AppConfig for Mobile Apps](../reference/appconfig.md)

</td></tr><tr><td>

SNBlockInstanceCreate

</td><td>

Enter the value to prevent end users from creating connections to new instances for managed mobile apps. For more information and a list of values, see [AppConfig for Mobile Apps](../reference/appconfig.md).

</td></tr><tr><td>

SNBlockMultiInstance

</td><td>

Enter the value to prevent end users from logging in to multiple instances simultaneously. For more information and a list of values, see [AppConfig for Mobile Apps](../reference/appconfig.md).

</td></tr></tbody>
</table>    ![Edit app configuration policy window in Microsoft Endpoint Manager admin center.](../image/azure-edit-policy.png)

7.  Select **Review + save**


**Parent Topic:**[Intune mobile device management \(MDM\)](../concept/intune-mdm.md)

