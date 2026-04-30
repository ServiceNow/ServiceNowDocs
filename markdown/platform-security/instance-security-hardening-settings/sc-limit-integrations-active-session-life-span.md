---
title: Limit integrations' active session life span \[New in Security Center 1.3\]
description: The glide.integrations.active.session.life\_span property enforces max lifespan on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes. A value of zero will disable timing out the active sessions.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit integrations' active session life span \[New in Security Center 1.3\]

The **glide.integrations.active.session.life\_span** property enforces max lifespan on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes. A value of zero will disable timing out the active sessions.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.integrations.active.session.life\_span**

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

0 to 720

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
-   Security risk details: A larger maximum lifespan could allow an attacker to persist in a stolen session for longer, increasing the scope of a security incident. This property is limited to integrations that have low-privilege access to an instance. Set the glide property, **glide.integrations.active.session.life\_span** to a value of 0, and less than or equal to 720.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

