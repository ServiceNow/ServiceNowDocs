---
title: Limit concurrent interactive sessions \[Updated in Security Center 1.3\]
description: Manage the number of interactive sessions on your instance.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit concurrent interactive sessions \[Updated in Security Center 1.3\]

Manage the number of interactive sessions on your instance.

This property is meant to be used with the Limit Concurrent Sessions \(**com.glide.limit.concurrent.sessions**\) plugin. When the plugin is active and the property is set to false, a user can have any number of concurrent interactive sessions on an instance. A greater number of open sessions means there is a great possibility for session hijacking to occur.

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

-   Severity score: 3.7
-   CVSS score: Low
-   Security risk details: When the plugin is active and the property is set to **false**, a user can have any number of concurrent interactive sessions which increases the possibility for a session hijacking.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Limit concurrent interactive sessions \[Updated in Security Center 1.3\]](sc-glide-authenticate-limit-concurrent-interactive-sessions.md)

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

