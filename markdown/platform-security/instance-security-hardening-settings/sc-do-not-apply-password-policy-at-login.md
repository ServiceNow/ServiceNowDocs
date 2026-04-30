---
title: Do not apply password policy at login \[Updated in Security Center 1.5 and removed in 2.0\]
description: Manage how password complexity is handled in your instance.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Do not apply password policy at login \[Updated in Security Center 1.5 and removed in 2.0\]

Manage how password complexity is handled in your instance.

By setting the property **glide.apply.password\_policy.on\_login** to false there will be no password complexity enforcement at login time. Setting the property to true will enforce password complexity and lead to organization policy compliance issues.

As per ASVS 4.03 v2.1.9 recommendations:

"Verify that there are no password composition rules limiting the type of characters permitted. There should be no requirement for upper or lower case or numbers or special characters. \(C6\)"

Instead of password complexity enforcement, ASVS recommendations are to enforce a minimum length of 12 characters for password length.

Refer to [OWASP ASVS v4.0 Authentication](https://github.com/OWASP/ASVS/blob/master/4.0/en/0x11-V2-Authentication.md).

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.apply.password\_policy.on\_login**

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

false

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.4
-   CVSS score: Medium
-   Security risk details: Setting this property to **true** could enforce password complexity and lead to organization compliance issues.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

