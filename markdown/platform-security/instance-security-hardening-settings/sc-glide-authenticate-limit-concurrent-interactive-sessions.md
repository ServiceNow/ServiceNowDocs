---
title: Minimize Concurrent Interactive Sessions with Limit Concurrent Sessions Plugin
description: Manage the number of interactive sessions on your instance.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Minimize Concurrent Interactive Sessions with Limit Concurrent Sessions Plugin

Manage the number of interactive sessions on your instance.

The **glide.authenticate.limit.concurrent.interactive.sessions** system property controls the number of active sessions that can be open for a user when the Limit Concurrent Sessions \(com.glide.limit.concurrent.sessions\) plugin is enabled. It is recommended that this value be the default of `1` to reduce the number of sessions that can be left open for a user.

Ensure that the property **glide.authenticate.limit.concurrent.interactive.sessions** is set to `1` when the Limit Concurrent Sessions \(com.glide.limit.concurrent.sessions\) plugin is active.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.limit.concurrent.interactive.sessions**

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

1

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

1

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS score: Low
-   Security risk details: A greater number of open sessions means there are more sessions that can potentially be hijacked.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Minimize Concurrent Interactive Sessions with Limit Concurrent Sessions Plugin](sc-glide-authenticate-limit-concurrent-interactive-sessions.md)

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

