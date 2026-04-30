---
title: Enable contextual security plugin \[Updated in Security Center 1.3\]
description: Activate the Contextual Security Plugin \(com.glide.role\_management\) plugin to enable contextual security, which secures a record/information using create, read, write, and delete functionality.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable contextual security plugin \[Updated in Security Center 1.3\]

Activate the Contextual Security Plugin \(**com.glide.role\_management**\) plugin to enable contextual security, which secures a record/information using create, read, write, and delete functionality.

After it is installed and activated, the dictionary roles \(created by simple security manager\) are no longer tested. Instead, the ServiceNow AI Platform looks for ACL rules on fields and tables. It secures the data with the help of ACL rules instead of traditional, role-based dictionary rules implemented by simple security manager. Even if you configure the dictionary form and add roles to a dictionary entry, no change in rights occurs.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Plugin ID

</td><td>

**com.glide.role\_management**

</td></tr><tr><td>

Configuration type

</td><td>

System Definition &gt; Plugins

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

Unlike the simple security manager, the contextual security manager is aware of the system table hierarchy. You can potentially have different security rules for a field based on where in the hierarchy it appears.

</td></tr><tr><td>

Recommended value

</td><td>

Active

</td></tr><tr><td>

Default value

</td><td>

There is no default value as this is a plugin, not a Glide property.

</td></tr><tr><td>

Security risk rating

</td><td>

8.1

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces functional level of access controls, which would let application determine the access restrictions based on ACL table alone.

</td></tr><tr><td>

Security risk

</td><td>

\(High\) Functional level access controls must be enforced from the server side prior to executing CRUD operations, ensuring the appropriate level of access to instance users.

</td></tr><tr><td>

References

</td><td>

[Contextual Security Manager](../../roles/reference/r_ContextualSecurity.md)

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

