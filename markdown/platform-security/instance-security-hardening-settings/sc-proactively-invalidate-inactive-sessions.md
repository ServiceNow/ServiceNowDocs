---
title: Proactively invalidate sessions after defined durations
description: The glide.active.session.timeout.invalidate.session property controls whether a timed-out session is proactively invalidated before the Tomcat server processes it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-proactively-invalidate-inactive-sessions.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Proactively invalidate sessions after defined durations

The **glide.active.session.timeout.invalidate.session** property controls whether a timed-out session is proactively invalidated before the Tomcat server processes it.

When this property value isn't set to **true**, there’s a brief interval where the application doesn't proactively invalidates the timed-out session before the Tomcat container invalidates it. To enable active session timeout, the user also needs to define at least one of the following session timeout properties:

|Property|Description|
|--------|-----------|
|glide.ui.active.session.life\_span|Defines the timeout period \(in minutes\) for UI sessions.|
|glide.guest.active.session.life\_span|Defines the timeout period \(in minutes\) for guest sessions.|
|glide.integrations.active.session.life\_span|Defines the timeout period \(in minutes\) for integration sessions.|

Ensure that the property **glide.active.session.timeout.invalidate.session** is set to true.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **glide.active.session.timeout.invalidate.session**
-   **glide.ui.active.session.life\_span**
-   **glide.guest.active.session.life\_span**
-   **glide.integrations.active.session.life\_span**

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

false

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.6
-   CVSS score: Medium
-   Security risk details: If a session is hijacked, an attacker may be able to use a session during this small period.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-session-management.md)

