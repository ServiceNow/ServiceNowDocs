---
title: Honor Admin Override ACLs
description: The glide.security.admin.override.accessterm property controls whether an administrator can bypass an access rule when a resource \(a table or a field\) has multiple access rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-honor-admin-override-acls.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-08-03"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Honor Admin Override ACLs

The **glide.security.admin.override.accessterm** property controls whether an administrator can bypass an access rule when a resource \(a table or a field\) has multiple access rules.

Each individual access rule can be configured to allow or disallow an admin override on its own. When set to `true` \(recommended\), each rule's admin override setting is honored individually. A rule explicitly configured to disallow an admin override still blocks the administrator even if another rule on the same resource permits it.

When set to `false`, rules are evaluated cumulatively. An admin can bypass one rule's override restriction if any other applicable rule permits it.

Set the **glide.security.admin.override.accessterm** property to `true` to ensure that access rules explicitly configured to deny override still blocks admins.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.security.admin.override.accessterm**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

Controls how admins can bypass an ACL evaluation.

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

True

</td></tr><tr><td>

Default value

</td><td>

True

</td></tr><tr><td>

Security risk

</td><td>

\(Low\) If access checks are too coarse, one rule's override denial is silently ignored in favor of a more permissive rule on the same resource. This allows admins to read or modify data and configurations that were intentionally locked down. Failure to enforce fine-grained evaluation of these override decisions may result in unauthorized access to sensitive information.

</td></tr><tr><td>

Security risk rating

</td><td>

3.8

</td></tr><tr><td>

Functional impact

</td><td>

When set to `true`, this property affects only admin access to resources with multiple rules. Regular users and single-rule resources are unaffected.

 Test that admins can't bypass override denials on a resource with multiple layered rules. Verify that if one rule denies admin override, that rule blocks the admin even if another rule permits override. This change has no service availability impact.

</td></tr><tr><td>

References

</td><td>

[Access Control List Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/access-control/access-control-rules.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-access-control.md)

