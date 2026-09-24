---
title: Minimize session activity timeout duration
description: Use the glide.ui.session\_timeout property to set the session activity timeout duration in minutes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-session-activity-timeout.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Minimize session activity timeout duration

Use the **glide.ui.session\_timeout** property to set the session activity timeout duration in minutes.

The **glide.ui.session\_timeout** property controls the inactive session timeout for authenticated users, specified in minutes. If this property is not set to the recommended value of 30 minutes or less, the session may remain valid for extended periods without user activity.

A long session timeout allows inactive sessions to remain valid for extended periods, increasing the chance that an attacker could hijack the session before it expires.

To configure the **glide.ui.session\_timeout** property:

1.  Navigate to /sys\_properties\_list.do on the instance.
2.  Confirm the **glide.ui.session\_timeout** property doesn't exist in the sys\_properties table or is set to 30 minutes or less.

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

30 or less

</td></tr><tr><td>

Default value

</td><td>

30

</td></tr><tr><td>

Fallback value

</td><td>

30

</td></tr><tr><td>

Category

</td><td>

[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS rating: High
-   Security risk details: A long session timeout allows inactive sessions to remain valid for extended periods, increasing the chance that an attacker could hijack the session before it expires.

</td></tr><tr><td>

Functional impact

</td><td>

Reducing the **glide.ui.session\_timeout** property lowers the amount of idle time allowed before a user's session ends automatically, requiring re-authentication. Users who leave a session idle longer than the configured value \(for example, while completing a long form, waiting on an approval, or stepping away between tasks\) will be logged out and must sign in again.

 Administrators should verify that long-running interactive workflows still complete comfortably within the new timeout window. They should also confirm that any automation or integration currently relying on a long-lived interactive UI sessions is migrated to a dedicated authentication method. Use OAuth or a service account rather than depending on session longevity.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The **glide.ui.session\_timeout** property is capped by the static property **glide.ui.max\_session\_timeout**, which limits the maximum effective value to 1440 minutes.

</td></tr></tbody>
</table>**Parent Topic:**[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-session-management.md)

