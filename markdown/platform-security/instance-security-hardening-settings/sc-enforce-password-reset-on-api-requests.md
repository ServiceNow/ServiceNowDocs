---
title: Enforce password reset on api requests \[Updated in Security Center 1.5\]
description: Manage how the password reset functionality operates on your instance.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Enforce password reset on api requests \[Updated in Security Center 1.5\]

Manage how the password reset functionality operates on your instance.

When a user is marked for **Password needs reset**, they must provide a new password at the next authentication attempt. This property controls whether the password reset is mandatory before making API calls. If this property is not set to the recommended value of **true**, user accounts marked as **Password needs reset** can still perform operations by querying the table API through basic authentication. This security vulnerability could enable information leakage if an inactive account is compromised.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.api.user.reset\_password.mandatory**

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

true

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS score: High
-   Security risk details: Setting this property to **false** could lead to information leakage if an inactive account is compromised.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

