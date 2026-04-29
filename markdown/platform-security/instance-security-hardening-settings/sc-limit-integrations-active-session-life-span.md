---
title: Limit integrations' active session life span
description: The glide.integrations.active.session.life\_span property enforces max lifespan on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes. A value of zero will disable timing out the active sessions.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit integrations' active session life span

The **glide.integrations.active.session.life\_span** property enforces max lifespan on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes. A value of zero will disable timing out the active sessions.

This configuration enforces the max lifespan on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes and the value of zero will disable timing out the active sessions. This particular property is limited to integrations that have low-privilege access to an instance.

Set the **glide.integrations.active.session.life\_span** system property to a value greater than `0` and less than or equal to `720`.

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

Integer

</td></tr><tr><td>

Recommended value

</td><td>

less than or equal to 720

</td></tr><tr><td>

Default value

</td><td>

0

</td></tr><tr><td>

Fallback value

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
-   CVSS rating: Medium
-   Security risk details: A larger maximum lifespan could allow an attacker to persist in a stolen session for longer, increasing the scope of a security incident.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

