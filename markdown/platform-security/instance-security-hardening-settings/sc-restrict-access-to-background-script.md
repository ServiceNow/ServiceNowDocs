---
title: Restrict access to background script \[Updated in Security Center 1.3 and 2.0\]
description: Configure the glide.script\_processor.admin property to set the role required for accessing the Script Background module.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict access to background script \[Updated in Security Center 1.3 and 2.0\]

Configure the **glide.script\_processor.admin** property to set the role required for accessing the Script Background module.

This property holds the required role to access Script Background module. If **glide.script\_processor.admin** is not set to the recommended and default value of admin, then users having a lower privileged role will be able to run background scripts on the instance. This will lead to a complete bypass of the ACL system allowing full access to tables.

Ensure the property **glide.script\_processor.admin** is set to the admin. This is the default value on instances.

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

admin

</td></tr><tr><td>

Default value

</td><td>

admin

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.8
-   CVSS score: High
-   Security risk details: Not setting this property to the recommended value of **admin** lets any user run background scripts on the instance.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

