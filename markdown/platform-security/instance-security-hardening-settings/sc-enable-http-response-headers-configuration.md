---
title: Enable HTTP response headers configuration
description: Reduce the risk of cookie/session-related hijacking of web apps using a system property.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Enable HTTP response headers configuration

Reduce the risk of cookie/session-related hijacking of web apps using a system property.

If the **glide.http.headers\_config.enabled** system property isn't set to **true**, then response header configurations defined in the HTTP Response Headers \[sys\_response\_header\] table aren't used. Security related HTTP response headers include Content Security Policy, which aids in XSS-related protections. For details on HTTP response headers, see [http-response-header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/http-response-header.md).

Ensure that the property **glide.http.headers\_config.enabled** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.http.headers\_config.enabled**

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

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Session management](sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.5
-   CVSS score: Medium
-   Security Risk: The security risks of missing, incorrect, or weak HTTP response headers may allow for XSS, CSRF, and cookie/session related hijacking of web apps.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Configuration](sc-configuration.md)

