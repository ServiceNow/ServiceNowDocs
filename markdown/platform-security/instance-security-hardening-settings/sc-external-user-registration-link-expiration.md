---
title: Minimize external user registration link expiration duration
description: Manage the number of days that a registration link can be accessed.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize external user registration link expiration duration

Manage the number of days that a registration link can be accessed.

If the **sn\_ext\_usr\_reg.Reg\_link\_expiration\_days** system property is not set to the recommended value of `3`, then a registration link could be used by someone other than the intended user if the link is discovered later in time.

Ensure that the property **sn\_ext\_usr\_reg.Reg\_link\_expiration\_days** is set to `3` or less.

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

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
-   Security risk details: Longer expiration windows weaken account provisioning security and create opportunities for unauthorized account creation or impersonation.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

