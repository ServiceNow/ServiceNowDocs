---
title: Enable protected tables plugin
description: Use the com.glide.security.protected\_table.enabled property to prevent higher privilege users from tampering with log tables.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Enable protected tables plugin

Use the **com.glide.security.protected\_table.enabled** property to prevent higher privilege users from tampering with log tables.

When the **com.glide.security.protected\_table.enabled** system property is set to **true**, The Protected Tables plugin is utilized to prevent higher privilege users on an instance from tampering with log tables. The following logging tables will have special protections when this property is set to **true**:

-   syslog \(config not modifiable\)
-   syslog\_transaction
-   sys\_outbound\_http\_log
-   sysevent
-   sys\_audit
-   sys\_push\_notification
-   protected\_table\_configuration \(config not modifiable\)
-   syslog\_app\_scope

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.security.protected\_table.enabled**

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Error handling and logging](sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.0
-   CVSS rating: Medium
-   Security risk details: Log integrity must be maintained to allow discovery of malicious activity.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)

