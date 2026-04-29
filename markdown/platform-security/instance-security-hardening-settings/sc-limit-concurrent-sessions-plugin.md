---
title: Activate Limit Concurrent Sessions Plugin
description: Configure the com.glide.limit.concurrent.sessions plugin to reduce the chance of session hijacking on your instance.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Activate Limit Concurrent Sessions Plugin

Configure the com.glide.limit.concurrent.sessions plugin to reduce the chance of session hijacking on your instance.

The Limit Concurrent Sessions plugin \(com.glide.limit.concurrent.sessions\) allows an administrator to limit the number of active sessions per user/role. It is recommended this plugin be enabled and configured to reduce the likelihood of session hijacking. If this plugin is enabled and configured, there will be a limit to the number of open sessions that can be hijacked.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **com.glide.limit.concurrent.sessions** \(plugin\)
-   **glide.authenticate.limit.concurrent.interactive.sessions**\(system property\)
-   **glide.authenticate.max.concurrent.interactive.sessions**\(system property\)

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   plugin
-   system property \(Boolean\)
-   system property \(Integer\)

plugin

</td></tr><tr><td>

Recommended value

</td><td>

-   **com.glide.limit.concurrent.sessions** is enabled
-   **glide.authenticate.limit.concurrent.interactive.sessions** system property set to **true**
-   **glide.authenticate.max.concurrent.interactive.sessions** set to a numeric value depending on the needs of your organization.

</td></tr><tr><td>

Default value

</td><td>

None

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS score: Low
-   Security risk details: Higher numbers of active concurrent sessions creates security risk by increasing the attack surface for account compromise, making it harder to detect unauthorized access and enforce session accountability across devices and locations.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

