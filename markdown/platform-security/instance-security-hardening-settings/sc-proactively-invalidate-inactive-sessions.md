---
title: Proactively invalidate inactive sessions \[New in Security Center 1.3 and updated in 1.5 and 2.0\]
description: The glide.active.session.timeout.invalidate.session property controls if a timeout session is proactively invalidated before the Tomcat server.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Proactively invalidate inactive sessions \[New in Security Center 1.3 and updated in 1.5 and 2.0\]

The **glide.active.session.timeout.invalidate.session** property controls if a timeout session is proactively invalidated before the Tomcat server.

When **glide.active.session.timeout.invalidate.session** is not set to **true**, there can be a small interval of time where a timed out session is not invalidated \(60 or more seconds depending on queue size\). If a session is hijacked, an attacker may be able to use a session during this small period of time. To remediate this security risk, set **glide.active.session.timeout.invalidate.session** to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.active.session.timeout.invalidate.session**

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

-   Severity score: 4.6
-   CVSS score: Medium
-   Security risk details: Not setting this property to the recommended value of true could cause a timed out session to not be validated. This increases the chances of a bad actor hijacking a session.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

