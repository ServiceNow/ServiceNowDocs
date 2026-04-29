---
title: Prevent Empty ACL Creation
description: Set the glide.security.empty\_acl.popup\_window.enabled property to the secure value of true to block attempts to create, update, or save an invalid ACL. This setting will also provide a client-side model to configure a role or security attribute for the ACL.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Prevent Empty ACL Creation

Set the **glide.security.empty\_acl.popup\_window.enabled** property to the secure value of true to block attempts to create, update, or save an invalid ACL. This setting will also provide a client-side model to configure a role or security attribute for the ACL.

The **glide.security.empty\_acl.popup\_window.enabled** property controls whether users making form-based edits to ACL \[sys\_security\_acl\] records can create, update, or save an invalid ACL that has an invalid data condition, script, security attribute, or roles list, or otherwise does not have any configured \(an "empty ACL"\). As of the Xanadu release, an empty ACL will completely deny access. On versions prior to Xanadu, empty an ACL will allow unconditional access.

When the **glide.security.empty\_acl.popup\_window.enabled** property is set to a secure value of **true**, attempts to create, update, or save an invalid or empty ACL will be blocked, and a client-side model will be provided to configure a role or security attribute for the ACL. If the property is insecurely set to any other value, then such attempts will be allowed and no client-side model will be displayed.

**Important:** This property is case sensitive. A value of "True" \(capital "T"\) will be equivalent to **false**. Additionally, this property will only function when the High Security \(com.glide.high\_security\) plugin is installed and active.

Ensure the that the **glide.security.empty\_acl.popup\_window.enabled** property is set to **true** and ensure that the High Security \(com.glide.high\_security\) plugin is active.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.empty\_acl.popup\_window.enabled**

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

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Fallback value

</td><td>

 

</td></tr><tr><td>

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS score: Medium
-   Security risk details: Misconfigured or empty Access Control Lists \(ACLs\) can unintentionally grant unrestricted access to sensitive data and system functionality. When ACLs lack proper conditions, roles, or security attributes, they fail to enforce authorization boundaries, enabling attackers or unauthorized users to bypass security controls. This can lead to data breaches, privilege escalation, and compromise of confidentiality, integrity, and availability across the platform.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property allows the user to toggle the empty ACL warning popup on and off.

</td></tr><tr><td>

References

</td><td>

[Prevent Empty ACL Creation](sc-prevent-empty-acl-creation.md)

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

