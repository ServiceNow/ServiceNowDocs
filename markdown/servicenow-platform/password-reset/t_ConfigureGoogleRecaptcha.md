---
title: Configure Google reCAPTCHA for the password reset process
description: To use the Google reCAPTCHA service, instances that are running on a domain other than service-now.com require an API key pair from Google.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/password-reset/t\_ConfigureGoogleRecaptcha.html
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure Google reCAPTCHA for the password reset process

To use the Google reCAPTCHA service, instances that are running on a domain other than `service-now.com` require an API key pair from Google.

## Before you begin

Role required: password\_reset\_admin

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

\[Omitted image "pw-reset-captcha-dialog.png"\] Alt text: Google Captcha

</td></tr></tbody>
</table>
**Parent Topic:**[Configure your Password Reset process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/t_CreateAPasswordResetProcess.md)

**Related topics**  


[Calculating the security score for password reset process]()

[Configure password expiration reminder]()

[Credential stores for Password Reset]()

[Password Reset verifications]()

[Configure your Password Reset process to auto-enroll users]()

[Enable users to enroll for Password Reset]()

[Configure Password Reset properties]()

[Send email to remind users to enroll for Password Reset]()

[Configure the required strength for passwords]()

[Specify lockout for failed login attempts]()

