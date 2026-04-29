---
title: Minimize reset password request success window duration
description: The password\_reset.request.success\_window property controls the number of minutes a user must wait to reset or change their password again after successfully resetting the password. The user will be blocked to reset the password again for the specified duration.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize reset password request success window duration

The **password\_reset.request.success\_window** property controls the number of minutes a user must wait to reset or change their password again after successfully resetting the password. The user will be blocked to reset the password again for the specified duration.

If the **password\_reset.request.success\_window** system property isn't set to the recommended value of `1440` or less, then the opportunity of someone else abusing the password reset functionality to gain unauthorized access to a user account is increased.

Ensure the property **password\_reset.request.success\_window** is set to `1440` or less.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.request.success\_window**

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

An integer less than or equal to 1440

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

1440

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score:
-   CVSS rating:
-   Security risk details:

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

