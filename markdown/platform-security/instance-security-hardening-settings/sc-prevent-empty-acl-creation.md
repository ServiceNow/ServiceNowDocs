---
title: Prevent Empty ACL Creation \[New in Security Center 2.0\]
description: Set the glide.security.empty\_acl.popup\_window.enabled property to the secure value of true to block attempts to create, update, or save an invalid ACL. This setting will also provide a client-side model to configure a role or security attribute for the ACL.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-19"
reading_time_minutes: 2
breadcrumb: [Validation, sanitization, and encoding, Hardening settings, Platform Security]
---

# Prevent Empty ACL Creation \[New in Security Center 2.0\]

Set the **glide.security.empty\_acl.popup\_window.enabled** property to the secure value of true to block attempts to create, update, or save an invalid ACL. This setting will also provide a client-side model to configure a role or security attribute for the ACL.

The **glide.security.empty\_acl.popup\_window.enabled** property determines whether users making form-based edits to access control lists \(ACLs\), specifically sys\_security\_acl, can create, update, or save an invalid ACL that has an invalid data condition, script, security attribute, or roles list. Otherwise, it remains unconfigured \(an empty ACL\). As of the Xanadu release, any empty ACL will deny access. In ServiceNow versions prior to Xanadu, an empty ACL will permit unconditional access.

When the **glide.security.empty\_acl.popup\_window.enabled** property is set to the secure value of true, it blocks attempts to create, update, or save an invalid or empty ACL, and provides a client-side model to configure a role or security attribute for the ACL. If the property is set to the unsecure value of false, then such attempts will be permitted, and no client-side model will be displayed.

Note: This property is case-sensitive. For example, a value of True \(capital "T"\) will be evaluated as false. Moreover, this property only functions when the High Security \(com.glide.high\_security\) plugin is installed and active.

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

Category

</td><td>

[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS score: Medium
-   Security risk details: If this property is set to true, the empty ACL warning popup will prevent the user from submitting an empty ACL on the client side. If it is set to false, the popup will no longer show.

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

[Prevent Empty ACL Creation \[New in Security Center 2.0\]](sc-prevent-empty-acl-creation.md)

</td></tr></tbody>
</table>**Parent Topic:**[Validation, sanitization, and encoding](validation-sanitization-encoding.md)

