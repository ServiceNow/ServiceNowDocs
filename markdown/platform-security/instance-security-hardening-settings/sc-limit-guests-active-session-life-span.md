---
title: Limit guest's active session life span \[New in Security Center 1.3\]
description: Use the glide.guest.active.session.life\_span property to control the duration of an active guest’s HTTP sessions.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit guest's active session life span \[New in Security Center 1.3\]

Use the **glide.guest.active.session.life\_span** property to control the duration of an active guest’s HTTP sessions.

The **glide.guest.active.session.life\_span** property enforces a maximum lifespan on active guest HTTP sessions, irrespective of their session inactivity or the amount of time a user is inactive before their session times out and closes.

The configured value is in minutes. A value of zero will disable timing out the active sessions. A larger value could allow an attacker to remain in a stolen session for longer, increasing the possibility of a security incident. This property is limited to guest users, which have low privilege access to an instance.

To remediate this security vulnerability, set **glide.guest.active.session.life\_span** to a value greater than 0 and less than or equal to 720.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.guest.active.session.life\_span**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

integer

</td></tr><tr><td>

Recommended value

</td><td>

1-720 \(minutes\)

</td></tr><tr><td>

Default value

</td><td>

0

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: Setting the maximum lifespan to a large value gives a bad actor more time within an instance in the event that they steal a session.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This configuration enforces max life-span on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes. A value of zero will disable timing out the active sessions. The max life-span should be more than the inactive timeout **glide.ui.session\_timeout** \(default 30 minutes\).

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

