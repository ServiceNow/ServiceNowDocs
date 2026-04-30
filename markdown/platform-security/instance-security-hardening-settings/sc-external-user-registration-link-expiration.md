---
title: Minimize external user registration link expiration duration \[Updated in Security Center 1.3 and 1.5\]
description: Manage the number of days that a registration link can be accessed.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize external user registration link expiration duration \[Updated in Security Center 1.3 and 1.5\]

Manage the number of days that a registration link can be accessed.

Use the **sn\_ext\_usr\_reg.Reg\_link\_expiration\_days** property to manage who can access a registration link. If the link is set to the recommended value of **3**, a registration link could be used by someone other than the intended user if the link is discovered at a later date.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_ext\_usr\_reg.Reg\_link\_expiration\_days**

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

3

</td></tr><tr><td>

Default value

</td><td>

3

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: Medium
-   CVSS score: 6.6
-   Security risk details: Not setting this property to the integer 3 could lead to the registration link being used by an unintended user.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

