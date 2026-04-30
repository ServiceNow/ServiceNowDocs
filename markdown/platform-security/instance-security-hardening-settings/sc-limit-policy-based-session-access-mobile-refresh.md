---
title: Limit policy based session access mobile refresh token interval \[New in Security Center 1.5\]
description: Use the glide.authenticate.session\_access.mobile.refresh\_token\_interval property to govern the length of time that must elapse before a mobile device user will be forced to re-authenticate.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit policy based session access mobile refresh token interval \[New in Security Center 1.5\]

Use the **glide.authenticate.session\_access.mobile.refresh\_token\_interval** property to govern the length of time that must elapse before a mobile device user will be forced to re-authenticate.

A user will be asked to re-authenticate only if the admin has configured the Identity Provider attributes in the session policy \(attributes can vary each login\), and the user authenticates using Single Sign On \(SSO\). The default value represents the time in seconds that a user has before being re-authenticated. A larger default value provides a bad actor more time for session access in the event of a session hijacking.

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

1800 \(seconds\)

</td></tr><tr><td>

Default value

</td><td>

1800 \(seconds\)

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details: If the ZTA policy is enabled on the instance, then users who are using SSO during mobile login will be forced to logout and re-login after the default value of 1800 seconds \(30 minutes\) have eclipsed. If a higher value is used, then users will be forced to wait that elapsed time.

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

