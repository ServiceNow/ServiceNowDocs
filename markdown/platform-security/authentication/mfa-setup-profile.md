---
title: Setup multi-factor authentication on your user profile
description: Enable multi-factor authentication for your account in your user profile settings.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Multi-factor authentication \(MFA\), Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Setup multi-factor authentication on your user profile

Enable multi-factor authentication for your account in your user profile settings.

## Before you begin

Role required: none

Multi-factor authentication must be enabled on your instance.

**Note:** Your administrator may require that you use multi-factor authentication. In this case, you are automatically prompted when you log in. See [Setup multi-factor authentication for the first time](t_SetUpMultiFactorAuthUponLogin.md). Use the process below if your administrator allows you to opt-in to multi-factor authentication.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **My Profile**.

    **Note:** You can also access your profile by clicking on your user name in the instance header.

2.  In your user profile, click **Multi-factor Authentication** in the **Related Links** section.

3.  Choose the MFA Authenticator type that you would like to use.

    ![MFA Authenticators](../images/mfa-authenticator.png)

<table id="table_k2g_xg5_nbc"><thead><tr><th>

MFA Authenticators

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authenticator App

</td><td>

Time-Based One Time Password \(TOTP\) authenticator appSelect **Set up authenticator app** and follow the instructions on the screen to register for an authenticator app as the second factor for authentication.

![MFA Authenticator App setup screen](../images/mfa-authenticator-app.png)

</td></tr><tr><td>

Biometric authenticators

</td><td>

Device-based authenticators such as Windows Hello or Apple Touch IDSelect **Register biometric authentication** and follow the instructions on the screen to register for an authenticator app as the second factor for authentication.

![MFA Biometric setup](../images/mfa-biometric.png)

</td></tr><tr><td>

Hardware Security Keys

</td><td>

Hardware security keys such as YubiKeySelect **Register hardware security keys** and follow the instructions on the screen to register for an authenticator app as the second factor for authentication.

![MFA - Hardware key setup](../images/mfa-hardware-key.png)

</td></tr></tbody>
</table>
## Result

Multi-factor authentication is enabled for your user account. You will be prompted to use multi-factor authentication the next time you log in.

**Note:** You cannot disable multi-factor authentication on your account after you have enabled it. If you need to disable multi-factor authentication, contact your administrator.

