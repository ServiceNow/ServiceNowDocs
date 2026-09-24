---
title: Enforce strict deny for ACLs referencing only deleted or non-existent roles
description: Manage how the system handles access control lists that reference roles deleted from the system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enforce-deny-acls-referencing-deleted-roles.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [ACL, access control, deleted roles, security]
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce strict deny for ACLs referencing only deleted or non-existent roles

Manage how the system handles access control lists that reference roles deleted from the system.

The **glide.security.acl\_with\_invalid\_roles\_strict\_deny** property controls how the system handles access control lists \(ACLs\) that reference roles that have been deleted from the system. When enabled \(the default\), any ACL containing only non-existent role references is explicitly denied access and logged as an error, preventing potential unauthorized access. When turned off, such misconfigured ACLs fall back to default logic that may grant access based on authentication state alone, potentially bypassing intended role-based restrictions.

This property protects against ACLs with deleted role references and executes on every record-level access check.

To configure this property:

1.  Navigate to /sys\_properties\_list.do on the instance.
2.  Ensure the **glide.security.acl\_with\_invalid\_roles\_strict\_deny** property exists in the sys\_properties table and is set to `true`.

## More information

<table id="table_property_details"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.acl\_with\_invalid\_roles\_strict\_deny**

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

-   Security risk rating: Medium
-   CVSS score: 5.1
-   Security risk details:

Disabling this property allows ACLs with deleted role references to fall back to default logic. Access is granted based on authentication alone, bypassing intended role requirements.

Users without the originally-required role can access protected records after role deletion. This is particularly risky during role cleanup or application uninstalls that leave orphaned ACL references.

This failure mode is silent and difficult to detect. It risks unauthorized data exposure or modification until misconfigured ACLs are manually remediated.


</td></tr><tr><td>

Functional impact

</td><td>

When enabled \(the default\), this property denies access to ACLs with all role references deleted and logs errors identifying affected rules for remediation. Partially invalid ACLs are unaffected. Only fully-orphaned role references trigger the denial, and the check incurs negligible performance overhead since invalid-role status is determined at ACL load time. Access is denied for ACLs with only deleted role references. Update these rules with valid roles instead of relying on fallback behavior.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

