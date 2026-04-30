---
title: Limit concurrent sessions plugin
description: Configure the com.glide.limit.concurrent.sessions plugin to reduce the chance of session hijacking on your instance.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit concurrent sessions plugin

Configure the com.glide.limit.concurrent.sessions plugin to reduce the chance of session hijacking on your instance.

When the Limit Concurrent Sessions \(com.glide.limit.concurrent.sessions\) plugin is not active, the **glide.authenticate.limit.concurrent.interactive.sessions** property is not set to **true**, or the **glide.authenticate.max.concurrent.interactive.sessions** property is set beyond an organizationally-defined threshold, then ServiceNow instance user accounts are not limited to a defined number of concurrent interactive sessions.

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.
2.  Find and select the Limit Concurrent Sessions plugin. The plugin ID is **com.glide.limit.concurrent.sessions**
3.  On the System Plugin form, review the plugin details and then select the **Activate/Upgrade** related link.
4.  Select **Activate**.
5.  After the plugin has successfully activate, navigate to **All** &gt; **System Properties** &gt; **All Properties**.
6.  Open the **glide.authenticate.limit.concurrent.interactive.sessions** system property, and set the value to **true**.
7.  Open the **glide.authenticate.max.concurrent.interactive.sessions** system property, and set the maximum concurrent sessions. This value depends on the needs of your organization.

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
-   Security risk details: A greater number of open sessions means there are more sessions that could potentially be hijacked. Limiting the number of allowed sessions per user is helpful in limiting risks related to denial-of-service \(DoS\) attacks.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

