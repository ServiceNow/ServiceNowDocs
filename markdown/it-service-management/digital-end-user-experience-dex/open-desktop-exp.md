---
title: Open and log in to Desktop Assistant
description: Open and log in to Desktop Assistant to get quick access to self-service tools, network tests, important notifications, and support resources.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Desktop Assistant, Digital End-User Experience, IT Service Management]
---

# Open and log in to Desktop Assistant

Open and log in to Desktop Assistant to get quick access to self-service tools, network tests, important notifications, and support resources.

## Before you begin

-   Confirm that the DEX Desktop Assistant \[sn\_dex\_desktop\] application has been installed. For more information, see [Install Application and Device Health](install-app-device-health.md) and [Download and install Desktop Assistant](download-desktop-experience.md).

-   Confirm that the OAuth registry record for Desktop Assistant is active.

Role required: sn\_dex\_desktop.user or sn\_dex\_desktop.admin

## Procedure

1.  From your system tray, select and hold or select and hold \(or right-click\) the Desktop Assistant icon ![](../image/icon-desktop-exp.png), and then select **Open**.

2.  Update the instance URL.

    1.  On the login page, select the **Change URL** link.

    2.  In the **Instance URL** field on the Change instance URL page, enter the ServiceNow instance URL.

    3.  Select the **Go back to login** link.

3.  On the login page, select **Sign in**.

4.  Log in to Desktop Assistant.

    -   When Single Sign-On \(SSO\) is not enabled:

        1.  Enter the user name and password for the instance in the **User name** and **Password** field.
        2.  If you can't remember your login details, select **Forgot password** to reset your password.
        3.  Select **Log in**.
        4.  Select **Allow** to grant Desktop Assistant permission to connect to your ServiceNow account.
        **Note:** To enable SSO login, set up the SSO provider and configure SSO in the instance. For more information, see [Configure Open Authorization details](configure-oauth-details.md).

    -   When SSO is enabled:
        1.  Select the **Login with SSO** link.
        2.  Enter your user ID in the **User ID** field.
        3.  Select **Submit**.

            You’re redirected to the SSO login screen.

        4.  Enter your login credentials and sign in.
        5.  Select **Allow** to grant Desktop Assistant permission to connect to your ServiceNow account.

-   If you see an application version incompatibility error when opening Desktop Assistant, contact your administrator.
-   If you get an unintended page when logging in, quit the application and reopen it.

**Related topics**  


[Resolve Desktop Assistant screen loading issue](../reference/resolve-loading-da-screen.md)

