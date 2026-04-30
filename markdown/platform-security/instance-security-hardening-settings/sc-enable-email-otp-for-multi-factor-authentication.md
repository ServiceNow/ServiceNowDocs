---
title: Enable email OTP for multi-factor authentication
description: Manage how two-factor authentication is applied on your instance.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable email OTP for multi-factor authentication

Manage how two-factor authentication is applied on your instance.

Use the **glide.authenticate.multifactor.email.otp.enabled** property to control whether a token for two-factor authentication is sent using email. Email is considered a weak MFA factor which an attacker is more likely to gain access into for bypassing MFA. By setting this property to **false**, the risk of an attacker bypassing MFA when they compromised a user's password is reduced.

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

boolean

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
-   Security risk details: Setting this property to **false** reduces the risk of a bad actor bypassing two-factor authentication.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Multi-factor authentication with Email](../../../integrate/authentication/concept/mfa-with-email.md)

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

