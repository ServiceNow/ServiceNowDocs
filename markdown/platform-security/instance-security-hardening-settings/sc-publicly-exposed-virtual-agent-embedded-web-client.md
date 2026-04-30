---
title: Prevent Unauthenticated Access to Virtual Agent Embedded Web Client
description: Learn how to configure the sn\_va\_web\_client\_app\_embed table to block unauthenticated users from accessing embedded web clients.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Prevent Unauthenticated Access to Virtual Agent Embedded Web Client

Learn how to configure the **sn\_va\_web\_client\_app\_embed** table to block unauthenticated users from accessing embedded web clients.

The UI page, **sn\_va\_web\_client\_app\_embed**, which is an embedded web client for Virtual Agent, contains the access control lists \(ACLs\) marked true in the sys\_public table out of the box. It has been confirmed that there are use cases where public accessibility is needed however this is not a standard to set it to default publicly accessible.

If the embedded web client is not needed for unauthenticated users, open the **sn\_va\_web\_client\_app\_embed** record \(sys\_id `04b1905473222300e985658b4cf6a7ef`\) in the Public Pages \[sys\_public\] table and deselect the **Active** field to deactivate the page.

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

The **sn\_va\_web\_client\_app\_embed** public page \[sys\_public\] \(sys\_id `04b1905473222300e985658b4cf6a7ef`\) does not exist or is not active.

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
-   Security risk details: It is recommended to deactivate the UI page, **sn\_va\_web\_client\_app\_embed**, if an embedded web client is not needed for unauthenticated users.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

