---
title: Maximize reset password SMS complexity
description: The password\_reset.sms.default\_complexity property controls the minimum required SMS code verification size required during password reset.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Maximize reset password SMS complexity

The **password\_reset.sms.default\_complexity** property controls the minimum required SMS code verification size required during password reset.

If the **password\_reset.sms.default\_complexity** system property isn't set to the recommended value of `6` or greater, then a weak SMS validation token is used.

Ensure the property **password\_reset.sms.default\_complexity** is set to `6` or more.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.sms.default\_complexity**

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

6 or higher

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

4

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score:
-   CVSS rating:
-   Security risk details: This increases the possibility of token guessing which could lead to account takeover.

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

