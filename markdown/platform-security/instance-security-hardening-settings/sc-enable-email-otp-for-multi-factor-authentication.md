---
title: Enable email OTP for multi-factor authentication
description: Manage how two-factor authentication is applied on your instance.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable email OTP for multi-factor authentication

Manage how two-factor authentication is applied on your instance.

The property **glide.authenticate.multifactor.email.otp.enabled** controls whether a token for the second authentication factor can be sent via email. Email is considered a weak MFA factor which an attacker is more likely to gain access into for defeating MFA.

If the property is false, the user doesn't see email OTP option on the MFA validation screen.

If the property is true:

1.  The email factor is shown in cases where the email factor policy is inactive and no other 2fa registered.
2.  The email factor is shown if the email factor policy is active and evaluated to true.
3.  The email factor is not shown if the email factor policy is active and evaluated to false.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.multifactor.email.otp.enabled**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.1
-   CVSS score: Low
-   Security risk details: An attacker may successfully bypassing MFA when they have the user's password.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Email as an MFA factor](../../../integrate/authentication/concept/mfa-with-email.md)

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

