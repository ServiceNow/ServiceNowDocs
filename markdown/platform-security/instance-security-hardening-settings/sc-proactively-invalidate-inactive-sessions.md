---
title: Proactively Invalidate Sessions After Defined Durations
description: The glide.active.session.timeout.invalidate.session property controls whether a timeout session is proactively invalidated before the Tomcat server.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Proactively Invalidate Sessions After Defined Durations

The **glide.active.session.timeout.invalidate.session** property controls whether a timeout session is proactively invalidated before the Tomcat server.

When **glide.active.session.timeout.invalidate.session** isn't set to true, there’s a small interval of time where a timed-out session isn’t invalidated proactively before the Tomcat container invalidates the session. The duration of this time interval is dependent on additional properties representing differing use cases.

|Property|Description|
|--------|-----------|
|glide.ui.active.session.life\_span|The value of this property defines the time, in minutes, before a UI session is invalidated.|
|glide.guest.active.session.life\_span|The value of this property defines the time, in minutes, before a guest session is invalidated.|
|glide.integrations.active.session.life\_span|The value of this property defines the time, in minutes, before an integrations session is invalidated.|

Ensure that the property **glide.active.session.timeout.invalidate.session** is set to true.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.active.session.timeout.invalidate.session**
-   **glide.ui.active.session.life\_span**
-   **glide.guest.active.session.life\_span**
-   **glide.integrations.active.session.life\_span**

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

Fallback value

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
-   Security risk details: If a session is hijacked, an attacker may be able to use a session during this small period.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

