---
title: Limit guest's active session life span \[New in Security Center 1.3\]
description: Use the glide.guest.active.session.life\_span property to control the duration of an active guest's HTTP sessions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-limit-guests-active-session-life-span.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-05-29"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Limit guest's active session life span \[New in Security Center 1.3\]

Use the **glide.guest.active.session.life\_span** property to control the duration of an active guest's HTTP sessions.

The **glide.guest.active.session.life\_span** system property enforces a maximum lifespan on active guest HTTP sessions, regardless of session inactivity. The configured value is in minutes. A value of `0` disables the lifespan limit entirely, allowing sessions to persist until the inactive timeout fires. Guest users are unauthenticated users who access the instance without logging in.

Set the **glide.guest.active.session.life\_span** system property to `720`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.guest.active.session.life\_span**

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

720

</td></tr><tr><td>

Default value

</td><td>

0

</td></tr><tr><td>

Category

</td><td>

[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: A larger maximum lifespan could allow an attacker to persist a stolen session for longer, increasing the scope of a security incident.

</td></tr><tr><td>

Functional impact

</td><td>

This configuration enforces max life-span on active guest HTTP sessions irrespective of inactive timeout. The configured value is in minutes. A value of zero disables the lifespan limit entirely. The max life-span should be more than the inactive timeout **glide.ui.session\_timeout** \(default 30 minutes\).

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-session-management.md)

