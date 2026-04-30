---
title: Enable UserCookie version 3.1 \[Updated in Security Center 2.0\]
description: Manage the version of UserCookie that is enabled on your instance to secure the storage of the secret key in the source code.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Enable UserCookie version 3.1 \[Updated in Security Center 2.0\]

Manage the version of UserCookie that is enabled on your instance to secure the storage of the secret key in the source code.

UserCookie v3 is generated only when property**glide.ui.secure.cookies.use\_kmf is disabled**. UserCookie v3 is not secure due to storing secret key for HMAC in source code and identical for all customers. That can support malicious actors to use this one secret key for attempts to hijacking user sessions. By setting the property **glide.ui.secure.cookies.use\_kmf** to true UserCookie v3.1 will be used and secret key will be stored in security storage such as KMF.

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

boolean

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
-   Security risk details: Setting this to **false** is a security vulnerability due to the secret key for hash-based message authentication codes \(HMAC\) being stored in the source code.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

