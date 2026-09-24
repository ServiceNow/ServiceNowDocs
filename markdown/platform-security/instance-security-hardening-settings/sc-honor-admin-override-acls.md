---
title: Honor admin override ACLs
description: The glide.security.admin.override.accessterm property controls whether admins can control override access control list \(ACL\) evaluation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-honor-admin-override-acls.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Honor admin override ACLs

The **glide.security.admin.override.accessterm** property controls whether admins can control override access control list \(ACL\) evaluation.

The **glide.security.admin.override.accessterm** property controls how the platform decides whether an administrator can bypass an access rule when a resource \(for example, a table, a field\) has more than one access rule applied to it. Each individual access rule can be configured to grant or deny an admin override on its own.

When this property is set to its recommended value of **true**, the per-rule setting is honored individually. A rule explicitly configured to deny an admin override still blocks the administrator even if another rule on the same resource permits one. When set to **false**, the bypass decision is instead made at a broader, combined level. This can let an administrator through even though one of the applicable rules was specifically configured to block the override.

Ensure that the property **glide.security.admin.override.accessterm** system property is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.admin.override.accessterm**

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

true

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.8
-   CVSS rating: Low
-   Security risk details: When access checks are evaluated coarsely, a privileged user can access a resource despite rules set to deny override. This allows the most restrictive protection to be ignored in favor of a more permissive rule on the same resource. Protected data can be set to readable or writable, risking unauthorized access to sensitive information.

</td></tr><tr><td>

Functional impact

</td><td>

Changing this property to **true** affects only elevated-admin access decisions on resources governed by more than one access rule; regular users and single-rule resources see no behavior change. After the change, test contextual security scenarios where an admin role is granted access to a field or record through multiple layered rules, confirming that a rule explicitly configured to deny override still blocks the admin as expected. No service availability impact is expected since the change only tightens an authorization decision path.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see .

**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

