---
title: Restrict access to background script
description: Use a system property to set a role requirement for accessing the Script Background module.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict access to background script

Use a system property to set a role requirement for accessing the Script Background module.

Use the **glide.script\_processor.admin** system property to set a required role to access the **Scripts - Background** module. If this property isn't set to the recommended value of `background_script_admin` or another high privileged role, users with lower privileged roles are able to run background scripts on your instance.

Ensure the property **glide.script\_processor.admin** is set to `background_script_admin`. This is also the default value.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.script\_processor.admin**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

background\_script\_admin

</td></tr><tr><td>

Default value

</td><td>

background\_script\_admin

</td></tr><tr><td>

Fallback value

</td><td>

background\_script\_admin

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.8
-   CVSS score: High
-   Security risk details: Background scripts allow a complete bypass of the ACL system allowing full access to tables.

</td></tr><tr><td>

Functional Impact

</td><td>

Users without the role specified in the property are unable to access the **Scripts - Background** module, as intended.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

