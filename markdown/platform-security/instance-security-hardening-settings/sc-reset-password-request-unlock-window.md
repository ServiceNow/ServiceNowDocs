---
title: Maximize reset password request unlock window duration
description: The password\_reset.request.unlock\_window property controls the number of minutes a user must wait to start a reset request after the last successful unlock account action.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Maximize reset password request unlock window duration

The **password\_reset.request.unlock\_window** property controls the number of minutes a user must wait to start a reset request after the last successful unlock account action.

The **password\_reset.request.unlock\_window** system property controls the number of minutes a user must wait to start a reset request after the last successful unlock account.

Ensure the property **password\_reset.request.unlock\_window** is set to a value of `1440` or greater.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.request.unlock\_window**

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

An integer greater than or equal to 1440

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

-   Severity score: 5.9
-   CVSS rating: Medium
-   Security risk details: If the value is too low, it increases the opportunity for a malicious actor from brute forcing the user's password using automated tools.

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

