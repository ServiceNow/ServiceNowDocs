---
title: Minimize absolute session timeout duration
description: Use the glide.ui.user\_cookie.max\_life\_span\_in\_days property to set a maximum life span for user cookies created when users log in with the Remember Me checkbox selected. When the cookie expires, users who have selected the Remember Me checkbox are forced to reauthenticate into the instance.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Minimize absolute session timeout duration

Use the **glide.ui.user\_cookie.max\_life\_span\_in\_days** property to set a maximum life span for user cookies created when users log in with the **Remember Me** checkbox selected. When the cookie expires, users who have selected the **Remember Me** checkbox are forced to reauthenticate into the instance.

If the **glide.ui.user\_cookie.max\_life\_span\_in\_days** system property is not set to the recommended value of `30` or other appropriate value, then a very long life session could be more vulnerable to session hijack attacks.

Ensure that the property **glide.ui.user\_cookie.max\_life\_span\_in\_days** is set to `30` or less.

**Note:** To enforce a maximum session time for any active user sessions, see [Managing user sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/c_ManageUserSessions.md).

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.user\_cookie.max\_life\_span\_in\_days**

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

30 or less

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

-   Severity score: 4.2
-   CVSS rating: Medium
-   Security risk details: A long session lifespan extends the window of opportunity for attackers to hijack active sessions, increasing the likelihood of unauthorized access if credentials or session tokens are compromised.

</td></tr><tr><td>

Functional impact

</td><td>

This property enforces mandatory re-login by avoiding any sort of cookie rotation after a given time frame.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](sc-session-management.md)

