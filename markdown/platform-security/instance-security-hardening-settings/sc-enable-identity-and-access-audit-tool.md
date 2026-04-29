---
title: Enable Identity and Access Audit Tool
description: Use Identity and Access Audit to track changes to user accounts, groups, and roles.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Enable Identity and Access Audit Tool

Use Identity and Access Audit to track changes to user accounts, groups, and roles.

Use Identity and Access Audit to track critical information about modifications made to user accounts, groups, and roles. Enable this feature to help detect malicious users, track unusual activity on your instance, and adhere to compliance standards for tracking access changes.

This tool stores audit records of successful create, update, and delete transactions to the Security Table Audits \[sys\_security\_table\_level\_audit\] table.

**Important:** Identity and Access Audit doesn’t audit successful read transactions, or any unsuccessful transactions.

Ensure that the Identity Security Audit \(com.glide.security.audit\) plugin is installed. After the plugin is installed, ensure that the **glide.identity.security.audit.enabled** system property is set to `true`, or doesn’t exist in the System Properties \[sys\_properties\] table.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **com.glide.security.audit**
-   **glide.identity.security.audit.enabled**

</td></tr><tr><td>

Configuration type

</td><td>

-   Plugin \(**All** &gt; **System Definition** &gt; **Plugins**\)
-   System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

-   N/A
-   Boolean

</td></tr><tr><td>

Recommended value

</td><td>

-   Plugin is active
-   true

</td></tr><tr><td>

Default value

</td><td>

-   Plugin is active
-   true

</td></tr><tr><td>

Fallback value

</td><td>

-   N/A
-   true

</td></tr><tr><td>

Category

</td><td>

[Error handling and logging](sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.6
-   CVSS score: Medium
-   Security risk details: Not auditing changes to user accounts, groups, and roles limits the effectiveness of audit and security personnel during investigations.

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

