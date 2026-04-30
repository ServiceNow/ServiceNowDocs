---
title: Enable MID audit log \[New in Security Center 1.3 and updated in 1.5\]
description: The MID Server command audit log records details such as the command name, command hash, name of credential used, and execution status.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Enable MID audit log \[New in Security Center 1.3and updated in 1.5\]

The MID Server command audit log records details such as the command name, command hash, name of credential used, and execution status.

Once enabled, audit logs can be viewed by users with the role agent\_security\_admin in the ecc\_agent\_command\_audit\_log table or by navigating to **Mid Server** &gt; **Command Audit Logs**.

Set **mid.log.command\_audit.enable** to true in the MID Server Properties \[ecc\_agent\_property\] table to turn on auditing for commands run by the MID server.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**mid.log.command\_audit.enable**

</td></tr><tr><td>

Configuration type

</td><td>

MID Server Property \[ecc\_agent\_property\] record

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

Category

</td><td>

[Error handling and logging](sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.2
-   CVSS score: Low
-   Security risk details: In the event of security investigation, this table can be used by incident response teams to audit the commands run on the MID server. Without this log, there might not be sufficient details to respond to situations such as unauthorized account use.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)

