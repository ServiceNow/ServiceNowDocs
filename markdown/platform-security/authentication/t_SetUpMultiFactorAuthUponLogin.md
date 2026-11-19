---
title: Set up Multi-factor authentication for the first time
description: If your administrator enabled MFA on your profile but you have not yet set up the application, you can set it up upon login.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/authentication/t\_SetUpMultiFactorAuthUponLogin.html
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using MFA, Multi-factor authentication, Authentication, Access Management]
---

# Set up Multi-factor authentication for the first time

If your administrator enabled MFA on your profile but you have not yet set up the application, you can set it up upon login.

## Before you begin

Role required: none

## Procedure

1.  Log in to your instance using your user name and password.

    The multi-factor authentication set up screen intercepts your login.

    \[Omitted image "new-mfa.png"\] Alt text: MFA screen

    **Note:** If you want to skip the authentication set up now, click **Bypass Setup**. You can bypass multi-factor authentication for a limited number of times that your administrator allows. Eventually, you must configure multi-factor authentication.

2.  Select one of the following methods to complete the mfa setup.

    1.  **Setup authenticator app**

        Follow the instructions on the screen to pair device and login.

        \[Omitted image "mfa-totp.png"\] Alt text: MFA-TOTP first time

    2.  **Setup Biometric authentication, Passkey or Hardware Security key**

        Select either of the option to complete the setup.

        \[Omitted image "biometirc-mfa.png"\] Alt text: MFA- Biometric or Hardware keys

    3.  **Get a verification code sent to your email**

        Enter the verification code that is sent to your email.

        \[Omitted image "mfa-email-login.png"\] Alt text: MFA- Email login

    After the successful completion of the either of the setup, you are logged in to the instance.


