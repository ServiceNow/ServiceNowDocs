---
title: Honor Admin Override ACLs
description: The glide.security.admin.override.accessterm property controls admins to be unable to override ACL evaluation even where the override should be in effect.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Honor Admin Override ACLs

The **glide.security.admin.override.accessterm** property controls admins to be unable to override ACL evaluation even where the override should be in effect.

ACLs are evaluated cumulatively. If there are a number of ACLs on any given field and the Admin Overrides option is false \(not selected\) on one of them, then the effective admin overrides for all the ACLs are considered to be false. This causes admins to be unable to pass even the ACL where the override should be in effect. If **glide.security.admin.override.accessterm** is not set to the recommended value of **true** then, even if one of the ACL terms under the ACL rule is "Admin overrides" false, the entire rule evaluates to false.

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

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.8
-   CVSS rating: Low
-   Security risk details: ACLs with conflicting "Admin overrides" settings may cumulatively evaluate to false, potentially preventing administrators from accessing fields they should have access to and inadvertently causing denial of access to critical data.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see Add a system property.

**Parent Topic:**[Access control](sc-access-control.md)

