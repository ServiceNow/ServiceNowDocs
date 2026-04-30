---
title: Log in with multi-factor authentication
description: Login with multi-factor authentication when it is enabled by your administrator on your instance.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up MFA on your user profile, Using MFA, Multi-factor authentication, Authentication, Access Management]
---

# Log in with multi-factor authentication

Login with multi-factor authentication when it is enabled by your administrator on your instance.

## Before you begin

You must have multi-factor authentication enabled for your profile. You can enable it yourself on your user profile or your administrator can enable it for you.

Role required: none

**Note:** The last used MFA verification factor is automatically shown for the users in the subsequent log in.

## Procedure

1.  Go to the URL of your instance to open the login screen.

2.  Enter your user name and password.

3.  Click **Log in**.

    The multi-factor authentication screen appears.

    ![MFA screen](../images/new-mfa.png)

4.  Select one of the methods to complete the MFA setup.

    For more information about each setup, see [Set up Multi-factor authentication for the first time](t_SetUpMultiFactorAuthUponLogin.md).

    If you wish to postpone the setup, select **Postpone setup**. The maximum number of time you can postpone the setup is displayed on the screen and this value is configured by your administrator.


## Result

If you have already setup MFA, the recently used factor is displayed when you login your instance after entering your username and password.

## Recently used MFA factor

If the recent used factor was Biometric login, then upon login using your username and password, you're directly displayed with the Biometric MFA setup screen.

![Used factor screen](../images/biometirc-mfa-recent.png)

