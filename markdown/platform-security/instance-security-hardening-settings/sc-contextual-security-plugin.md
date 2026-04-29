---
title: Enable contextual security plugin
description: Activate the Contextual Security Plugin \(com.glide.role\_management\) plugin to enable contextual security, which secures a record/information using create, read, write, and delete functionality.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable contextual security plugin

Activate the Contextual Security Plugin \(**com.glide.role\_management**\) plugin to enable contextual security, which secures a record/information using create, read, write, and delete functionality.

The Contextual Security Plugin \(**com.glide.role\_management**\) plugin helps manage user groups and roles to protect information through role-based access controls. The plugin efficiently consolidates duplicate entries for inherited roles, and secures a record/information using create, read, write, and delete functionality. After it is installed and activated, the dictionary roles \(created by security manager\) are no longer tested. Instead, the Now Platform looks for ACL rules on fields and tables. It secures the data with the help of ACL rules instead of traditional, role-based dictionary rules implemented by simple security manager. Even if you configure the dictionary form and add roles to a dictionary entry, no change in rights occurs.

Ensure that the plugin **com.glide.role\_management** is activated.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.role\_management**

</td></tr><tr><td>

Configuration type

</td><td>

System Definition &gt; Plugins

</td></tr><tr><td>

Data type

</td><td>

N/A

</td></tr><tr><td>

Recommended value

</td><td>

The Contextual Security Plugin \(**com.glide.role\_management**\) plugin is active.

</td></tr><tr><td>

Default value

</td><td>

The Contextual Security Plugin \(**com.glide.role\_management**\) plugin is not active by default.

</td></tr><tr><td>

Fallback value

</td><td>

The Contextual Security Plugin \(**com.glide.role\_management**\) plugin is not active by default.

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS rating: High
-   Security risk details: Failing to transition fully to ACL-based controls may leave sensitive data exposed due to overlooked or outdated dictionary role configurations.

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces functional level of access controls, which would let application determine the access restrictions based on ACL table alone.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

