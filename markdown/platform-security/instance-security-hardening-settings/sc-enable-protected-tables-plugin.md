---
title: Enable protected tables plugin \[New in Security Center 1.3\]
description: Use the com.glide.security.protected\_table.enabled property to prevent higher privilege users from tampering with log tables.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Enable protected tables plugin \[New in Security Center 1.3\]

Use the **com.glide.security.protected\_table.enabled** property to prevent higher privilege users from tampering with log tables.

When the **com.glide.security.protected\_table.enabled** property is set to **true**, the protected tables plugin will be used to prevent higher privilege users on an instance from tampering with log tables. The following log tables have special protections when this property is set to **true**:

-   syslog \(No DB Override\)
-   syslog\_transaction
-   sys\_outbound\_http\_log
-   sysevent
-   sys\_audit
-   sys\_push\_notification
-   protected\_table\_configuration \(No DB Override\)

The integrity of logs is important for determining malicious activity on an instance by a customer admin.

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

boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

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

-   Severity score: 4.5
-   CVSS score: Medium
-   Security risk details: Not setting **com.glide.security.protected\_table.enabled** to the recommended value of true enables higher privilege users on an instance to tamper with log tables.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[System logs](../../system-logs/concept/system-logs.md)

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)

