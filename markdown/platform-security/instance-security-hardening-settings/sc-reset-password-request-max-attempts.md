---
title: Limit Invalid Password Reset Attempts
description: The password\_reset.request.max\_attempt is used to control the maximum number of unsuccessful attempts that a user can reset or change their password before being locked out for a specified period of time.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Limit Invalid Password Reset Attempts

The **password\_reset.request.max\_attempt** is used to control the maximum number of unsuccessful attempts that a user can reset or change their password before being locked out for a specified period of time.

The **password\_reset.request.max\_attempt** system property dictates the maximum number of unsuccessful password reset attempts that can be taken before the user is locked out of password reset process. The lockout period is determined by the value in **password\_reset.request.max\_attempt\_window**.

Ensure that the property **password\_reset.request.max\_attempt** is set to `3` or less.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.request.max\_attempt**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Integer

</td></tr><tr><td>

Recommended value

</td><td>

An integer less than or equal to 3

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

3

</td></tr><tr><td>

Category

</td><td>

[Configure Password Reset properties](../../login/task/t_SetPwdResetProps.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS rating: High
-   Security risk details: If the value is too high, then it could be possible to perform brute force attack against password reset process.

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

