---
title: Limit concurrent sessions across all nodes \[Updated in Security Center 1.3\]
description: Use the glide.authenticate.limit.concurrent.sessions.across.all.nodes property with the Limit Concurrent Sessions plugin to manage the number of sessions tracked across all nodes.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit concurrent sessions across all nodes \[Updated in Security Center 1.3\]

Use the **glide.authenticate.limit.concurrent.sessions.across.all.nodes** property with the Limit Concurrent Sessions plugin to manage the number of sessions tracked across all nodes.

When the [Limit concurrent sessions](../../../integrate/authentication/concept/limit-concurrent-sessions.md) plugin is active, the number of open sessions can be limited per user. Ensure that when this plugin is active that the \(**Glide authenticate limit concurrent sessions across all nodes**\) property is set to **true** so that the number of open sessions are tracked across all nodes instead of a single application node. If this property is set to **false**, multiple sessions can be open across multiple nodes, which increases the chances of session hijacking.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.limit.concurrent.sessions.across.all.nodes**

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

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS score: Low
-   Security risk details: When using the **Limit Concurrent Sessions** plugin, setting this property to **false** enables multiple sessions across multiple nodes to be open which increases the chance of a security vulnerability like a session hijacking.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Limit concurrent sessions](../../../integrate/authentication/concept/limit-concurrent-sessions.md)

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

