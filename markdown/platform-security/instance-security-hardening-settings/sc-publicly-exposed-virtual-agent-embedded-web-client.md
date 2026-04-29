---
title: Prevent Unauthenticated Access to Virtual Agent Embedded Web Client
description: Learn how to configure the sn\_va\_web\_client\_app\_embed table to block unauthenticated users from accessing embedded web clients.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Prevent Unauthenticated Access to Virtual Agent Embedded Web Client

Learn how to configure the **sn\_va\_web\_client\_app\_embed** table to block unauthenticated users from accessing embedded web clients.

The UI page **sn\_va\_web\_client\_app\_embed**, which is an embedded web client for Virtual Agent, contains the ACL marked 'true' in the sys\_public table Out of Box. It has been confirmed that there are use cases where public accessibility is needed however this is not a security best practice to set it to default publicly accessible.

Deactivate ui page **sn\_va\_web\_client\_app\_embed** from the Public Pages \[sys\_public\] table if embedded web client is not needed for unauthenticated users

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_va\_web\_client\_app\_embed**

</td></tr><tr><td>

Configuration type

</td><td>

UI Page\(sys\_ui\_page\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

table

</td></tr><tr><td>

Recommended value

</td><td>

The Public Pages \[sys\_public\] table record with sys\_id of `04b1905473222300e985658b4cf6a7ef` does exist or is not active.

</td></tr><tr><td>

Default value

</td><td>

Not available \(this is a table value\)

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS score: High
-   Security risk details: Sensitive information may be exposed to unauthenticated users.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

