---
title: Minimize concurrent interactive session quantity \[Updated in Security Center 1.3\]
description: Use this property with the Limit Concurrent Sessions plugin to control the number of active sessions that can be opened by a user.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Minimize concurrent interactive session quantity \[Updated in Security Center 1.3\]

Use this property with the Limit Concurrent Sessions plugin to control the number of active sessions that can be opened by a user.

Use the **Glide Authenticate Max Concurrent Interactive Sessions** property with the **Limit Concurrent Session** \(**com.glide.limit.concurrent.sessions**\) plugin to control the number of active sessions opened for a user. The recommended value is **1**, which reduces the number of sessions opened \(a greater number increases the likelihood that a session could be hijacked\).

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.max.concurrent.interactive.sessions**

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

1

</td></tr><tr><td>

Default value

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
-   Security risk details: Setting the default value of the property greater than 1 increases the chance of session hijacking.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **Concurrent Interactive Sessions** \(**com.glide.limit.concurrent.sessions**\) plugin should be active.

</td></tr><tr><td>

References

</td><td>

[Limit concurrent sessions](../../../integrate/authentication/concept/limit-concurrent-sessions.md)

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

