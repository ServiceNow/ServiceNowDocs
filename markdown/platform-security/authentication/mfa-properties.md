---
title: Multi-factor Authentication system properties
description: Use system properties to enable and customize MFA to meet your security requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/mfa-properties.html
release: brazil
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configuring MFA, Multi-factor authentication, Authentication, Access Management]
---

# Multi-factor Authentication system properties

Use system properties to enable and customize MFA to meet your security requirements.

<table id="table_lxg_qcz_bs"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.authenticate.multifactor**

</td><td>

Enable Multi-factor Authentication.**Note:** To enforce MFA for API authentication, set the `glide.authenticate.multifactor.for_integrations` system property to `true`. MFA is enforced only for users who have already enrolled in MFA. Users who have not enrolled are not affected.

</td></tr><tr><td>

**glide.authenticate.multifactor.setup.bypass.count**

</td><td>

Number of times that a user can choose to skip the setup of MFA. The default is 0.

</td></tr><tr><td>

**glide.multifactor.onetime.code.validity**

</td><td>

Number of minutes that the reset code is valid. See [Log in with Multi-factor Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/t_LogOnWithMultifactorAuth.md). The default is 5.**Note:** This property is for email OTP validation time.

</td></tr><tr><td>

**glide.authenticate.multifactor.clock\_skew**

</td><td>

Number of additional seconds that the reset code is valid. The maximum is `60`. The default is `10`.The instance validates the code entered by the user against the single app-generated code that is generated at the `current time`. You can skew the time window with this property and allow one or more codes to be generated during a time window to be considered valid.

The property's value is used in the following calculation: `current time - X/2` and `current time + X/2`, where `X` is the value of this property. If you use the value of `10`, for example, the instance considers any codes that the app generates within the time range `[the current time - 5 seconds]` and `[current time + 5 seconds]` to be valid. Use this property to prevent login issues where the user is unable to enter the correct code in the default time allotted.

</td></tr><tr><td>

**glide.authenticate.multifactor.remember.browser.enable**

</td><td>

Enables "remember this browser" for multi-factor authentication. When enabled, a user who has completed MFA on a given browser or device isn't prompted again on subsequent logins from that same browser or device for the configured time period. The user is prompted for MFA again only when logging in from a new browser or device. Default: true.

</td></tr><tr><td>

**glide.authenticate.multifactor.browser.fingerprint.validity**

</td><td>

Sets how long a remembered browser stays trusted after MFA is completed. Within this period, the user isn't challenged for MFA again in the same browser. Default: 8 hours.**Note:** Browser trust relies on a browser fingerprint \(BFP\) — a hash computed from a set of browser and device parameters. If one of those parameters changes during the validity period — for example, screen resolution changes when an external monitor is connected or disconnected — the fingerprint no longer matches the one recorded when MFA was last completed, and the user is challenged for MFA again earlier than the validity period would suggest.

</td></tr><tr><td>

**glide.authenticate.multifactor.remembered.browser.max.count**

</td><td>

The number of browsers MFA remembers for this user.

</td></tr><tr><td>

**glide.authenticate.multifactor.remember.browser.default**

</td><td>

Default value of the remember-browser check box in the validate multi-factor page.

</td></tr><tr><td>

**glide.webauthn.enabled**\)

</td><td>

Option to enable passwordless authentication \(FIDO2 based MFA\) methods such as hardware key and biometric authentication.

</td></tr><tr><td>

**glide.authenticate.multifactor.email.otp.enable**

</td><td>

Option to enable email based OTP as a factor for MFA.

</td></tr><tr><td>

**glide.auth.mfa.ui.v2.enabled**

</td><td>

Option to enable MFA factor independently for the users without setting up an authenticator app.

</td></tr></tbody>
</table>