---
title: Using Multi-factor authentication \(MFA\)
description: Learn how to use multi-factor authentication tools to securely access your instance.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Using Multi-factor authentication \(MFA\)

Learn how to use multi-factor authentication tools to securely access your instance.

## Login with MFA

ServiceNow requires authenticator applications that support Time-based One-time Passwords \(TOTP\). ServiceNow tests MFA with the following authenticators:

-   Google Authenticator
-   Microsoft Authenticator
-   LastPass Authenticator
-   Authy
-   FreeOTP
-   Duo
-   Okta Verify

**Note:**

-   Other authenticators not listed might also be compatible, but are not tested by ServiceNow.
-   For information related to browser specific behavior change, see this [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0998122)

<table id="table_g22_2j4_dpb"><tbody><tr><td>

Validation with authenticator app

 ![Authenticator.](../images/auth-app.png)

 Enter the code displayed on your authenticator app to login.

</td><td>

If your administrator has enabled multi-factor authentication \(MFA\) on your instance, you are prompted for a second authentication after entering your user name and password. For details on the MFA login process, see [Log in with multi-factor authentication](../task/t_LogOnWithMultifactorAuth.md)

 If you haven't configured a second form of authentication, you will see a configuration page after logging in to guide you through the process of setting up an authentication app. For details on this setup, see [Setup multi-factor authentication for the first time](../task/t_SetUpMultiFactorAuthUponLogin.md).

</td></tr></tbody>
</table>## Register an authentication device

<table id="table_qm1_zj4_dpb"><tbody><tr><td>

After you've configured an authentication app, you can register other methods for authentication.

-   **Biometric authenticators**

You can use biometric authenticators like fingerprint or facial recognition as your second MFA authentication. If your administrator allows this option, you can configure biometric authenticators using the steps in [Register a biometric authenticator](../task/mfa-setup-bio-auth.md).

-   **Hardware key authenticators**

Hardware keys are physical security devices you can use for authentication. You can register a hardware device for use with your instance using the steps in [Register a hardware security key](../task/mfa-setup-hardware-key-auth.md).


</td><td>

![Biometrics icon](../images/biometric-2.png)

 ![Hardware key icon](../images/hardware-key.png)

</td></tr><tr><td>

Validation with Biometric or Hardware Key

 ![MFA - Biometric or Hardware](../images/biometirc-mfa.png)

</td><td>

Use the Biometric or Security Key to login.

</td></tr></tbody>
</table>## Register a phone number for OTP

<table id="table_bjc_2wb_2vb"><tbody><tr><td>

-   **SMS**

Admin configures ServiceNow instance to require users who attempt to login the instance using SMS based OTP.

When users attempt to login to ServiceNow, SMS OTP is sent to the mobile number associated with the sys\_user record. Users can enter the six-digit verification code that it sent to the mobile device and verify their identity.


</td><td>

![SMS.](../images/sms.png)

</td></tr><tr><td>

Validation with SMS

 ![MFA-SMS.](../images/mobile-screen-mfa.png)

</td><td>

Enter the 6-digit code sent to the mobile number to login. The code sent is valid for the next 5 minutes. You can use resend code to again send the code.

</td></tr></tbody>
</table>## Register an Email address for OTP

<table id="table_xwx_dwb_2vb"><tbody><tr><td>

-   **Email address**

Admin configures ServiceNow instance to require users who attempt to login the instance using Email based OTP.

When users attempt to login to ServiceNow, Email OTP is sent to the email address associated to the user. User's can enter the six-digit verification code that it sent to the mobile device and verify their identity.


</td><td>

![Email.](../images/email.png)

</td></tr><tr><td>

Validation with Email

 ![MFA-Email.](../images/email-screen-mfa.png)

</td><td>

Enter the 6-digit code sent to the email address to login. The code sent is valid for the next 5 minutes. You can use resend code to again send the code.

</td></tr></tbody>
</table>