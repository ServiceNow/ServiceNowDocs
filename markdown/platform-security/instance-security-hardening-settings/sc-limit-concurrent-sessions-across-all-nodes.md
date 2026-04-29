---
title: Limit concurrent sessions across all nodes
description: Use the glide.authenticate.limit.concurrent.sessions.across.all.nodes property with the Limit Concurrent Sessions plugin to manage the number of sessions tracked across all nodes.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit concurrent sessions across all nodes

Use the **glide.authenticate.limit.concurrent.sessions.across.all.nodes** property with the Limit Concurrent Sessions plugin to manage the number of sessions tracked across all nodes.

The **glide.authenticate.limit.concurrent.sessions.across.all.nodes** system property is meant to be used with the Limit Concurrent Sessions plugin \(com.glide.limit.concurrent.sessions\) plugin. When this plugin is installed and configured, the number of open sessions can be limited per user. When this property is set, the number of sessions will be tracked across all nodes instead of a single application nodes.

Ensure that the **glide.authenticate.limit.concurrent.sessions.across.all.nodes** sysem property is set to **true** when the Limit Concurrent Sessions plugin \(com.glide.limit.concurrent.sessions\) plugin is active.

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

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

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
-   Security risk details: If this property is not set to true, multiple sessions can be open across multiple nodes, increasing the likelihood of a successful session hijacking.

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

