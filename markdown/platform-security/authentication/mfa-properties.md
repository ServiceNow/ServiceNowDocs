---
title: Multi-factor authentication system properties
description: Use system properties to enable and customize MFA to meet your security requirements.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Multi-factor authentication, Multi-factor authentication, Authentication, Access Management]
---

# Multi-factor authentication system properties

Use system properties to enable and customize MFA to meet your security requirements.

<table id="table_lxg_qcz_bs"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.authenticate.multifactor.setup.bypass.count**

</td><td>

Number of times that a user can choose to skip the setup of MFA. The default is 0.

</td></tr><tr><td>

**glide.multifactor.onetime.code.validity**

</td><td>

Number of minutes that the reset code is valid. See [Log in with multi-factor authentication](../task/t_LogOnWithMultifactorAuth.md). The default is 5.**Note:** This property is for email OTP validation time.

</td></tr><tr><td>

**glide.authenticate.multifactor.clock\_skew**

</td><td>

Number of additional seconds that the reset code is valid. The maximum is `60`. The default is `10`.The instance validates the code entered by the user against the single app-generated code that is generated at the `current time`. You can skew the time window with this property and allow one or more codes to be generated during a time window to be considered valid.

The property's value is used in the following calculation: `current time - X/2` and `current time + X/2`, where `X` is the value of this property. If you use the value of `10`, for example, the instance considers any codes that the app generates within the time range `[the current time - 5 seconds]` and `[current time + 5 seconds]` to be valid. Use this property to prevent login issues where the user is unable to enter the correct code in the default time allotted.

</td></tr><tr><td>

**glide.authenticate.multifactor.remember.browser.enable**

</td><td>

Set your instance to prompt a user for MFA when they log in from a new device or browser. The default is yes.

</td></tr><tr><td>

**glide.authenticate.multifactor.browser.fingerprint.validity**

</td><td>

After MFA remembers the browser, the user is not challenged for MFA in the same browser for this duration. The default is 8 hours.

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