---
title: Define active session timeout exception roles \[New in Security Center 1.3\]
description: Use a system property to exempt roles from active session timeout limits.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Define active session timeout exception roles \[New in Security Center 1.3\]

Use a system property to exempt roles from active session timeout limits.

Use the **glide.active.session.timeout.exception.roles** system property to exempt roles from an active session timeout limit. The active session timeout feature helps ensure that a hijacked session cannot be used indefinitely without providing authentication information. It is best practice to only consider an active session timeout limit exception for internal integration account roles.

Configure the **glide.active.session.timeout.exception.roles** property to roles which should be exempt from active session timeouts. This property value is a comma separated list of roles. The default value is **edge\_encryption,mid\_server,maint**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.active.session.timeout.exception.roles**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

edge\_encryption,mid\_server,maint

</td></tr><tr><td>

Default value

</td><td>

edge\_encryption,mid\_server,maint

</td></tr><tr><td>

Fallback value

</td><td>

edge\_encryption,mid\_server,maint

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.4
-   CVSS score: Medium
-   Consider an active session timeout limit exception only for internal integration account roles. If a user is a victim of a session hijacking attempt, and has a role with an exception, attackers using that session can continue to authenticate to that session indefinitely. This may increase the impact of a security incident by enabling an attacker more time to make use of a hijacked account.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

