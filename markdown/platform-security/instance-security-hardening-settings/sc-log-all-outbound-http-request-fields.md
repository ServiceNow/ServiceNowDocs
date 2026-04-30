---
title: Log all outbound http request fields \[Removed in Security Center v1.3.2\]
description: Configure the glide.outbound\_http.security.log.allow.all.fields property to false to prevent sensitive Outbound HTTP fields from being logged in plain text.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-01-20"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Log all outbound http request fields \[Removed in Security Center v1.3.2\]

Configure the **glide.outbound\_http.security.log.allow.all.fields** property to false to prevent sensitive Outbound HTTP fields from being logged in plain text.

If this property is not set to the recommended value of **false**, sensitive Outbound HTTP fields might be logged in plaintext. This can decrease the security posture of your enterprise network because outbound requests with sensitive data and credentials can be logged in plaintext which is unencrypted, and can be viewed by lower-privileged users.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.outbound\_http.security.log.allow.all.fields**

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

false

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Error handling and logging](sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.8
-   CVSS score: Medium
-   Security risk details: Not setting this property to **false** increases the chance of sensitive outbound fields being logged in plaintext which is a security risk.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)

