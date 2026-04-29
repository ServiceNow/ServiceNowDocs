---
title: Set OTP lifetime for password reset to 1 hour \[Updated in Security Center 2.0\]
description: Control the time duration of the link in the password reset email.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Set OTP lifetime for password reset to 1 hour \[Updated in Security Center 2.0\]

Control the time duration of the link in the password reset email.

The **glide.pwd\_reset.onetime.token.validity** system property makes the link in the password reset email expire after the number of hours specified in the property. The validity time of a password reset token should be kept as short as possible while not disrupting normal user experience

Set the property value to 1 \(in hours\).

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.pwd\_reset.onetime.token.validity**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

integer

</td></tr><tr><td>

Recommended value

</td><td>

1

</td></tr><tr><td>

Default value

</td><td>

1

</td></tr><tr><td>

Fallback value

</td><td>

1

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.6
-   CVSS score: Medium
-   Security risk details: A longer validity time for password reset token gives malicious actors a wider window to perform account takeover if the email with the reset token is leaked or compromised.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

