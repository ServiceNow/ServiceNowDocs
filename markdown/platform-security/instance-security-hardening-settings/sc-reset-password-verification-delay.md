---
title: Maximize reset password verification delay duration \[Updated in Security Center 1.3\]
description: Configure the delay, in milliseconds, that a user must wait before submitting a new password reset request.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Maximize reset password verification delay duration \[Updated in Security Center 1.3\]

Configure the delay, in milliseconds, that a user must wait before submitting a new password reset request.

A bad actor could attempt to brute force login credentials by using automation tools like bots which the **reset password verification delay** property helps defend against. The property value represents the delay, in milliseconds, that a user must wait before they can place a request to reset the password. If this property is not set to the recommended value of **1000** or more, the login is more vulnerable to brute force attacks.

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

string

</td></tr><tr><td>

Recommended value

</td><td>

1000

</td></tr><tr><td>

Default value

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
-   CVSS score: Medium
-   Security risk details: Setting the property value to less than 1000 makes your login more vulnerable to brute force attacks.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Configure password for a user](../../../integrate/authentication/task/reset-your-password.md)

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

