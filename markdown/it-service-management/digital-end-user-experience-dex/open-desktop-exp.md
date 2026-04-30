---
title: Open Desktop Assistant
description: Open or log in to Desktop Assistant to get an easy access to ServiceNow functionalities such as your applications, device health, your requests, network speed of your system, and Employee Center.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using DEX Desktop Assistant, Digital End-User Experience, IT Service Management]
---

# Open Desktop Assistant

Open or log in to Desktop Assistant to get an easy access to ServiceNow functionalities such as your applications, device health, your requests, network speed of your system, and Employee Center.

## Before you begin

Confirm that the DEX Desktop Assistant \[sn\_dex\_desktop\] application has been installed. For more information, see [Install Application and Device Health](install-app-device-health.md) and [Download and install Desktop Assistant](download-desktop-experience.md).

Role required: sn\_dex\_desktop.user or sn\_dex\_desktop.admin

## About this task

If you see the `Incompatibility application version detected` message, contact the administrator.

![Message showing version incompatibility.](../image/dex-da-incompatibility.png)

## Procedure

1.  From your system tray, select and hold \(or right-click\) the Desktop Assistant icon \(![Desktop Experience icon that opens Desktop Assistant](../image/icon-desktop-exp.png)\) and then select **Open**.

2.  Select **Sign in**.

    You can customize the login page by changing the following values in the settings.json file:

    -   loginHeader
    -   loginBody
    -   companyLogoSvg
    ![Login page to sign in to Desktop Assistant.](../image/desktop-exp-login-1.png)

3.  In the **Instance URL** field, enter the ServiceNow instance URL.

    ![Page where you can change the instance URL.](../image/desktop-exp-change-url.png)

4.  Select **Sign in**.

    The authentication window opens.

    ![Login page where you can enter the username and password.](../image/desktop-exp-login-2.png)

    If you can't remember your login details, use the **Forgot password** feature to reset your password.

5.  Perform any one of the following actions to log in:

    -   When you don't have a Single Sign-On \(SSO\):
        -   Enter the user name and password for the instance in the **User name** and **Password** field.
        -   Select **Log in**.
        -   Allow Desktop Assistant to connect to your ServiceNow account by selecting **Allow**.

            **Note:** To have an SSO login, you should set up the SSO provider and configure SSO in the instance. To learn more about configuring SSO, see [Configure OAuth details](configure-oauth-details.md).

    -   When you have Single Sign-On \(SSO\):
        -   Select the **Login with SSO** link.

            ![Login page where you can enter the user id.](../image/desktop-exp-login-sso-1.png)

        -   Enter your user ID in the **User ID** field.
        -   Select **Submit**.

            You’re redirected to the SSO login screen.

            ![The SSO login page where you can enter the username and password.](../image/desktop-exp-login-sso-2.png)

        -   Enter your user name and password in the **User name** and **Password** field.
        -   Select **Sign in**.
        -   Allow Desktop Assistant to connect to your ServiceNow account by selecting **Allow**.

## Result

The Desktop Assistant Home page opens.

If you get an unintended page when logging in, quit the application and reopen it to resolve the issue.

