---
title: Limit integrations' active session life span
description: Use the glide.integrations.active.session.life\_span property to enforce the maximum lifespan on active integration HTTP sessions, regardless of session inactivity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-limit-integrations-active-session-life-span.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit integrations' active session life span

Use the **glide.integrations.active.session.life\_span** property to enforce the maximum lifespan on active integration HTTP sessions, regardless of session inactivity.

The configured value is in minutes. A value of zero disables the lifespan limit entirely, allowing sessions to persist indefinitely until the inactive timeout fires. This particular property is limited to integrations that have low-privilege access to an instance.

A larger maximum lifespan allows an attacker to persist a stolen session for longer, increasing the scope of a security incident.

To configure the **glide.integrations.active.session.life\_span** propeerty:

1.  Navigate to /sys\_properties\_list.do on the instance.
2.  Ensure the **glide.integrations.active.session.life\_span** property exists and is set to a value greater than `0` and less than or equal to `720` minutes.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.integrations.active.session.life\_span**

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

Between 1 and 720

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
-   CVSS rating: Medium
-   Security risk details: A larger maximum lifespan allows an attacker to persist a stolen session for longer, increasing the scope of a security incident.

</td></tr><tr><td>

Functional impact

</td><td>

Integration sessions that exceed the configured lifespan are silently invalidated and reissued a new session ID. The integration user sees no error, but any session-scoped state accumulated during that session is lost and starts fresh.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

This control interacts with the **glide.integration.session\_timeout** property, which controls the integration idle-session timeout duration. The platform requires the active session maximum lifespan to be greater than or equal to the integration idle timeout. If the active session lifespan is configured lower than the idle-session timeout, the platform automatically increases the effective lifespan to match the idle-session timeout. The platform logs a warning message when this occurs.

</td></tr></tbody>
</table>**Parent Topic:**[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-session-management.md)

