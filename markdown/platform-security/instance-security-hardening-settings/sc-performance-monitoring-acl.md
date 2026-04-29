---
title: Restrict performance monitoring access
description: Use the glide.security.diag\_txns\_acl property to control stats.do, threads.do, thread\_pool\_stats, and replication.do access from an unauthenticated connection.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Restrict performance monitoring access

Use the **glide.security.diag\_txns\_acl** property to control stats.do, threads.do, thread\_pool\_stats, and replication.do access from an unauthenticated connection.

If **glide.security.diag\_txns\_acl** is not set to the recommended value of **true**, then All users \(authenticated or not\) have access to diagnostic pages such as stats.do, xmlstats.do, threads.do and replication.do pages. These endpoints are intended to be used for monitoring instance health.

Ensure the property **glide.security.diag\_txns\_acl** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.diag\_txns\_acl**

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

[Configuration](sc-configuration.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS rating: Medium
-   Security risk details: Information exposed by performance monitoring endpoints may be useful to attackers.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Configuration](sc-configuration.md)

