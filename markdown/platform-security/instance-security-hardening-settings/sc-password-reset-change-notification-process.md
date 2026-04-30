---
title: Notify users during password reset/change process \[Removed in Security Center 1.5\]
description: Use this property to enable end users to reset or change passwords using a self-service process.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Notify users during password reset/change process \[Removed in Security Center 1.5\]

Use this property to enable end users to reset or change passwords using a self-service process.

This property enables an end user to reset or change a password using a self-service process. Alternatively, your organization could implement a process that requires a service desk agent to reset passwords for end users. If a password change and or reset process doesn't notify users on password update, a bad actor may be able to lock that user out of their account without their knowledge. This would provide the bad actor more time to perform malicious activities. Ensure password reset process notifies users upon password change or reset.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**pwd\_process.change, pwd\_process.reset**

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

true

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS score: High
-   Security risk details: A bad actor may be able to lock a user out of their account without their knowledge if no notification is sent to them when a password change is reset.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)

