---
title: Enable protected tables plugin
description: Use the com.glide.security.protected\_table.enabled property to prevent higher privilege users from tampering with log tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enable-protected-tables-plugin.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
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

To enable table protection through the guided activation flow:

-   Navigate to the Protected Tables plugin's guided activation flow.
-   Complete the activation process to enable table protection. Only users with the security\_admin role can activate this control.

**Important:** Don't turn on this control by directly editing the **com.glide.security.protected\_table.enabled** property outside that guided activation flow. Default protected tables: syslog, syslog\_transaction, sys\_outbound\_http\_log, sysevent, sys\_audit, sys\_push\_notification, protected\_table\_configuration, syslog\_app\_scope.

To extend protection to additional tables, configure insert, update, and delete protection rules for each additional table and operation in the protected\_table\_configuration list.

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

false

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Error handling and logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.0
-   CVSS rating: Medium
-   Security risk details: When turned off \(the default\), Protected Tables protections don't apply, allowing maintenance-role users to modify or delete critical audit and security logs without detection. An attacker with maintenance credentials could tamper with syslog, sys\_audit, and sysevent entries to cover malicious activity and evade forensic investigation. Disabling this property compromises the audit trail needed to detect and investigate security incidents.

</td></tr><tr><td>

Functional impact

</td><td>

Enabling the **com.glide.security.protected\_table.enabled** property causes create, update, and delete attempts on tables in the Protected Table Configuration list to be evaluated. Depending on that table's configured protection level, the attempt is blocked, logged, or ignored. The level shipped per table is not fixed. It depends on how long the Protected Tables plugin has been installed, so confirm the actual values on your instance rather than assuming a table is blocking.

 One exception holds everywhere: insert attempts on sysevent are never blocked or logged, since normal processing inserts sysevent records continuously. A refused attempt shows the message `Modifications to '<table>' have been refused due to the Protected Table configuration. Please contact your system administrator.` Any integration or business rule currently writing to or deleting from a blocking table will start failing once this property is enabled.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-error-handling-logging.md)

