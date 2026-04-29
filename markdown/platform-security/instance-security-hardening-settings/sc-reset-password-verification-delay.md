---
title: Maximize reset password verification delay duration
description: Configure the delay, in milliseconds, that a user must wait before submitting a new password reset request.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Maximize reset password verification delay duration

Configure the delay, in milliseconds, that a user must wait before submitting a new password reset request.

If **password\_reset.verification.delay** isn't set to the recommended value of `1000` or more, then password reset verification codes will be susceptible to brute force attacks.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.verification.delay**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String

</td></tr><tr><td>

Recommended value

</td><td>

An integer greater than or equal to 1000

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

1000

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.9
-   CVSS rating: Medium
-   Security risk details: The milliseconds delay limits the ability of a malicious actor to attempt to guess users identification or verification details, by using automation tools \(bots\).

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

