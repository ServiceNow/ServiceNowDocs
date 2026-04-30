---
title: Multi-factor authentication system properties
description: Use system properties to enable and customize MFA to meet your security requirements.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring MFA, supported methods, and workflow, Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Multi-factor authentication system properties

Use system properties to enable and customize MFA to meet your security requirements.

<table id="table_lxg_qcz_bs"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Multi-factor authentication \(**glide.authenticate.multifactor**\)

</td><td>

Option that enables users and administrators to use this feature. The default is enabled. To learn more about this property, see  in Instance Security Hardening Settings.

</td></tr><tr><td>

Number of times a user can bypass multi-factor authentication\(**glide.authenticate.multifactor.setup.bypass.count**\)

</td><td>

Number of times that a user can choose to skip the setup of MFA. Your users can still log in to the instance even if they don't have their mobile device with them. If you disable this feature and then re-enable it, the counter starts over again. The default is 3.

</td></tr><tr><td>

The time in minutes the one-time code sent to user's email address is valid for \(**glide.multifactor.onetime.code.validity**\)

</td><td>

Number of minutes that the reset code is valid. See [Log in with multi-factor authentication](../task/t_LogOnWithMultifactorAuth.md). The default is 5.**Note:** This property is for email OTP validation time.

</td></tr><tr><td>

Additional time in seconds for which the code is valid to accommodate for the clock skew. The maximum value is 60 seconds. \(**glide.authenticate.multifactor.clock\_skew**\)

</td><td>

Number of additional seconds that the reset code is valid. The maximum is `60`. The default is `10`.The instance validates the code entered by the user against the single app-generated code that is generated at the `current time`. You can skew the time window with this property and allow one or more codes to be generated during a time window to be considered valid.

The property's value is used in the following calculation: `current time - X/2` and `current time + X/2`, where `X` is the value of this property. If you use the value of `10`, for example, the instance considers any codes that the app generates within the time range `[the current time - 5 seconds]` and `[current time + 5 seconds]` to be valid. Use this property to prevent login issues where the user is unable to enter the correct code in the default time allotted.

</td></tr><tr><td>

Enable remember browser feature for multi-factor authentication.\(**glide.authenticate.multifactor.remember.browser.enable**\)

</td><td>

Set your instance to prompt a user for MFA when they log in from a new device or browser. The default is yes.

</td></tr><tr><td>

Validity of browser fingerprint in hours.\(**glide.authenticate.multifactor.browser.fingerprint.validity**\)

</td><td>

After MFA remembers the browser, the user is not challenged for MFA in the same browser for this duration. The default is 8 hours.

</td></tr><tr><td>

Maximum number of browsers a user can remember. \(**glide.authenticate.multifactor.remembered.browser.max.count**\)

</td><td>

The number of browsers MFA remembers for this user.

</td></tr><tr><td>

Default value of remember browser check box in the validate multi-factor page.\(**glide.authenticate.multifactor.remember.browser.default**\)

</td><td>

Default value of the remember-browser check box in the validate multi-factor page.

</td></tr><tr><td>

Enable web authentication \(FIDO2\) based MFA. \(**glide.webauthn.enabled**\)

</td><td>

Option to enable passwordless authentication methods such as hardware key and biometric authentication.

</td></tr><tr><td>

Enable email OTP for Multi-factor authentication \(**glide.authenticate.multifactor.email.otp.enable**

</td><td>

Option to enable email based OTP as a factor for MFA.

</td></tr><tr><td>

Enable enhanced multi-factor authentication \(MFA\) setup UI to allow users to setup the factor independently. **glide.auth.mfa.ui.v2.enabled**

</td><td>

Option to enable MFA factor independently for the users without setting up an authenticator app.

</td></tr></tbody>
</table>