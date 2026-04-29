---
title: Enable UserCookie version 3.1
description: Manage the version of UserCookie that is enabled on your instance to secure the storage of the secret key in the source code.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Enable UserCookie version 3.1

Manage the version of UserCookie that is enabled on your instance to secure the storage of the secret key in the source code.

UserCookie v3 is generated only when property **glide.ui.secure.cookies.use\_kmf is disabled** is disabled. UserCookie v3 is not secure due to storing secret key for HMAC in source code and identical for all customers. By setting the property **glide.ui.secure.cookies.use\_kmf** to **true**, UserCookie v3.1 is used and secret key is stored in security storage such as KMF.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.secure.cookies.use\_kmf**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.1
-   CVSS score: High
-   Security risk details: This creates a significant risk of session hijacking, as attackers who obtain or reverse-engineer the key can forge authentication cookies and impersonate users.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

