---
title: Limit policy based session access mobile refresh token interval
description: Use the glide.authenticate.session\_access.mobile.refresh\_token\_interval property to govern the length of time that must elapse before a mobile device user will be forced to re-authenticate.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit policy based session access mobile refresh token interval

Use the **glide.authenticate.session\_access.mobile.refresh\_token\_interval** property to govern the length of time that must elapse before a mobile device user will be forced to re-authenticate.

The **glide.authenticate.session\_access.mobile.refresh\_token\_interval** suystem property governs the length of time after which a mobile device user will be forced to re-authenticate. This only applies if the admin has configured the Identity Provider attributes \(which can vary for each login\) in the session access policy and the user authenticates via Single Sign On \(SSO\). The property value is an integer in seconds. The recommended value is `1800` \(30 minutes\).

Ensure that the **glide.authenticate.session\_access.mobile.refresh\_token\_interval** property is set to a value of `1800` or below.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.session\_access.mobile.refresh\_token\_interval**

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

An integer less than or equal to 1800

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

1800

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details: A large value may grant a larger timeframe for session access to be hijacked by an attacker.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Zero Trust- Policy Based Session Access

</td></tr><tr><td>

Functional impact

</td><td>

This setting governs the time in seconds after login, that users will be forced to logout from mobile devices if they are using Single Sign On to authenticate, and admin has configured the Identify provider attributes in the session access policy.

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

