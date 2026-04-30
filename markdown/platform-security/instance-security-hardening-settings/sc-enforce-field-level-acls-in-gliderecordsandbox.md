---
title: Enforce field level ACLs in GlideRecordSandbox
description: Manage field level ACLs in GlideRecordSandbox on your instance.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce field level ACLs in GlideRecordSandbox

Manage field level ACLs in GlideRecordSandbox on your instance.

Use the **glide.sandbox.fields.check\_acl** property to enforce field level ACLs in GlideRecordSandbox. An example in which this property is applied is when a user can provide a script, like in **sysparm\_query**. If this property is not set to the recommended value of **true**, ACL restrictions can be bypassed, which enables sensitive data to be compromised, such as a **sys\_user.user\_password** from an unauthorized user.

**Warning:** The value for this property is a no DB override. It can't be altered or overridden.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sandbox.fields.check\_acl**

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

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS score: High
-   Security risk details: Setting this property to **false** enables ACL restrictions to be bypassed which could expose sensitive data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

