---
title: Minimize session activity timeout duration
description: Use the glide.ui.session\_timeout property to designate, in minutes, activity timeout value.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Minimize session activity timeout duration

Use the **glide.ui.session\_timeout** property to designate, in minutes, activity timeout value.

The **glide.ui.session\_timeout** system property determines the user session timeout, which determines how long a user session stays active. If **glide.ui.session\_timeout** is not set to the recommended value of `60` minutes or less, then the session may stay valid for long even without activity. This could provide too large of a time window to enable session hijacking attacks.

Ensure that the property **glide.ui.session\_timeout** is set to `60` or less.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.session\_timeout**

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

60 or less

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

30

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS rating: High
-   Security risk details: A long session timeout allows inactive sessions to remain valid for extended periods, increasing the chance that an attacker could hijack the session before it expires.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces timely expiration of user account. No functionality impact, however User experience is altered.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see Add a system property.

**Parent Topic:**[Session management](sc-session-management.md)

