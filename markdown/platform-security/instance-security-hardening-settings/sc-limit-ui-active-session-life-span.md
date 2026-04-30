---
title: Limit UI active session life span \[New in Security Center 1.3\]
description: The glide.ui.active.session.life\_span property enforces max lifespan on active authenticated HTTP sessions irrespective of inactive timeout.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit UI active session life span \[New in Security Center 1.3\]

The **glide.ui.active.session.life\_span** property enforces max lifespan on active authenticated HTTP sessions irrespective of inactive timeout.

Reduce the scope of potential security incidents by decreasing the lifespan of active HTTP sessions. The **glide.ui.active.session.life\_span** system property enforces a maximum lifespan on active HTTP sessions irrespective of inactive timeout. Longer maximum lifespans can allow an attacker to use a stolen session for a longer time, increasing the scope of a security incident. The default value of **0** disables timeout of active sessions

Set the **glide.ui.active.session.life\_span** to a value between 1 and 720. This value represents the time in minutes that HTTP sessions can remain active.

**Note:** The **glide.ui.active.session.life\_span** is limited to UI session timeout.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.active.session.life\_span**

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

1-720

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
-   Security risk details: A larger maximum lifespan could allow an attacker to remain in a stolen session longer, increasing the possibility of a security incident.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

Enforces max life-span on active authenticated HTTP sessions irrespective of inactive timeout. The configured value is in minutes. A value of zero will disable timing out the active sessions. The max life-span should be more than inactive timeout glide.ui.session\_timeout \(default 30 minutes\).

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

