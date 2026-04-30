---
title: Configure Google reCAPTCHA for the password reset process
description: To use the Google reCAPTCHA service, instances that are running on a domain other than service-now.com require an API key pair from Google.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Google reCAPTCHA for the password reset process

To use the Google reCAPTCHA service, instances that are running on a domain other than `service-now.com` require an API key pair from Google.

## Before you begin

Role required: admin

## About this task

-   The procedure described in this topic is optional for instances that are running on the `service-now.com` domain.
-   Because on-premises instances do not have access to the Internet, they cannot use the Google reCAPTCHA service. Do not follow the procedure described in this topic. Instead, set the password\_reset.captcha.google.enabled system property to **false**. This setting enables the CAPTCHA service that is provided with the base system.
-   The Password Reset Windows Application uses the base-system CAPTCHA service even if the Password Reset application is configured to use Google reCAPTCHA.

## Procedure

1.  Request an API key pair \(a site key and a secret\) from Google at [https://www.google.com/recaptcha](https://www.google.com/recaptcha).

2.  Set the following system properties:

<table id="table_xvy_qty_h1b"><thead><tr><th>

Property

</th><th>

Value

</th></tr></thead><tbody><tr><td>

**password\_reset.captcha.google.enabled**

</td><td>

Set to `true`.Type: string

 Default: true

</td></tr><tr><td>

**google.captcha.site\_key**

</td><td>

Set to the site key that Google provided.Type: string

 Default: A site key that Google provided to ServiceNow

</td></tr><tr><td>

**google.captcha.secret**

</td><td>

Set to the secret that Google provided.Type: password2

 Default: An encrypted secret that Google provided to ServiceNow

 **Note:**

Select reCAPTCHA v2, **I'm not a robot** option. \(reCAPTCHA v3 is not currently supported\).

![Google Captcha](../image/pw-reset-captcha-dialog.png)

</td></tr></tbody>
</table>
**Parent Topic:**[Configure your Password Reset process](t_CreateAPasswordResetProcess.md)

**Related topics**  


[Configure password expiration reminder](password-reset-expiration-setup.md)

[Credential stores for Password Reset](../concept/c_CredentialStores.md)

[Password Reset verifications](../concept/c_PWRVerifications.md)

[Configure your Password Reset process to auto-enroll users](../../security/task/configure-auto-enroll-for-pwd-reset.md)

[Enable users to enroll for Password Reset](../../security/task/configure-user-enroll-for-pwd-reset.md)

[Configuring Password Reset properties](t_SetPwdResetProps.md)

[Send email to remind users to enroll for Password Reset](config-pwd-reset-enroll-reminder.md)

[Configure the required strength for passwords](config-pwd-strength-rqmts.md)

[Specify lockout for failed login attempts](../../security/task/t_LockoutForFailedLogins.md)

