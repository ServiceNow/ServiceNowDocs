---
title: Set up Multi-factor authentication on your user profile
description: Enable multi-factor authentication for your account in your user profile settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/mfa-setup-profile.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using MFA, Multi-factor authentication, Authentication, Access Management]
---

# Set up Multi-factor authentication on your user profile

Enable multi-factor authentication for your account in your user profile settings.

## Before you begin

Role required: none

Multi-factor authentication must be enabled on your instance.

**Note:** Your administrator may require that you use multi-factor authentication. In this case, you are automatically prompted when you log in. See [Set up Multi-factor authentication for the first time](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/t_SetUpMultiFactorAuthUponLogin.md). Use the process below if your administrator allows you to opt-in to multi-factor authentication.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **My Profile**.

    **Note:** You can also access your profile by clicking on your user name in the instance header.

2.  In your user profile, click **Configure Multi-factor Authentication** in the **Related Links** section.

3.  Choose the MFA Authenticator type that you would like to use.

    \[Omitted image "mfa-authenticator.png"\] Alt text: MFA Authenticators

<table id="table_k2g_xg5_nbc"><thead><tr><th>

MFA Authenticators

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authenticator App

</td><td>

Time-Based One Time Password \(TOTP\) authenticator appSelect **Set up authenticator app** and follow the instructions on the screen to register for an authenticator app as the second factor for authentication.

\[Omitted image "mfa-authenticator-app.png"\] Alt text: MFA Authenticator App setup screen

</td></tr><tr><td>

Biometric authenticators

</td><td>

Device-based authenticators such as Windows Hello or Apple Touch IDSelect **Register biometric authentication** and follow the instructions on the screen to register for an authenticator app as the second factor for authentication.

\[Omitted image "mfa-biometric.png"\] Alt text: MFA Biometric setup

</td></tr><tr><td>

Hardware Security Keys

</td><td>

Hardware security keys such as YubiKeySelect **Register hardware security keys** and follow the instructions on the screen to register for an authenticator app as the second factor for authentication.

\[Omitted image "mfa-hardware-key.png"\] Alt text: MFA - Hardware key setup

</td></tr></tbody>
</table>
## Result

Multi-factor authentication is enabled for your user account. You will be prompted to use multi-factor authentication the next time you log in.

**Note:** You cannot disable multi-factor authentication on your account after you have enabled it. If you need to disable multi-factor authentication, contact your administrator.

