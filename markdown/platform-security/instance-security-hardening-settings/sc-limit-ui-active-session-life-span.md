---
title: Limit UI active session life span
description: The glide.ui.active.session.life\_span property enforces max lifespan on active authenticated HTTP sessions irrespective of inactive timeout.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-limit-ui-active-session-life-span.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit UI active session life span

The **glide.ui.active.session.life\_span** property enforces max lifespan on active authenticated HTTP sessions irrespective of inactive timeout.

The **glide.ui.active.session.life\_span** property enforces a maximum lifespan on active, authenticated UI HTTP sessions, regardless of session inactivity. The configured value is in minutes. A value of zero disables the lifespan limit entirely, allowing sessions to persist indefinitely until the inactive timeout fires. This particular property is limited to authenticated end users accessing the instance through the UI.

Navigate to /sys\_properties\_list.do on the instance. Ensure the **glide.ui.active.session.life\_span** property exists and is set to a value greater than 0 and less than or equal to 720 minutes.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.ui.active.session.life\_span**

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

1-720

</td></tr><tr><td>

Default value

</td><td>

0

</td></tr><tr><td>

Fallback value

</td><td>

0

</td></tr><tr><td>

Category

</td><td>

[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: A larger maximum lifespan allows an attacker to persist a stolen session for longer, increasing the scope of a security incident.

</td></tr><tr><td>

Functional impact

</td><td>

Authenticated UI sessions that exceed the configured lifespan are explicitly logged out. The session cookies are cleared and the session is invalidated, forcing the user to re-authenticate, rather than silently reissuing a new session ID as occurs with guest and integration sessions. Users must re-authenticate to continue working, even if they were actively using the platform when the session expired.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

This control interacts with the **glide.ui.session\_timeout** property, which controls the UI idle-session timeout duration. The platform requires the active session maximum lifespan to be greater than or equal to the idle timeout. If the active session lifespan is configured to a value lower than the idle-session timeout, the platform automatically increases the effective lifespan to match the idle-session timeout and logs a warning message.

</td></tr></tbody>
</table>**Parent Topic:**[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-session-management.md)

