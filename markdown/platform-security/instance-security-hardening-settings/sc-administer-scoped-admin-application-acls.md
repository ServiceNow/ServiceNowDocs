---
title: Enable scoped admin application ACLs
description: The glide.security.scoped\_administration.honor\_global\_acl determines whether an application administration app can inherit global access control list \(ACL\) rules.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable scoped admin application ACLs

The **glide.security.scoped\_administration.honor\_global\_acl** determines whether an application administration app can inherit global access control list \(ACL\) rules.

The **glide.security.scoped\_administration.honor\_global\_acl** system property determines whether an application administration apps can inherit global access control list \(ACL\) rules. Useful when there are no scoped admin application ACLs defined for the record scope.

Ensure that the property **glide.security.scoped\_administration.honor\_global\_acl** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.scoped\_administration.honor\_global\_acl**

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

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.8
-   CVSS rating: Low
-   Security risk details:

Low privilege users with permissions to the application could potentially access sensitive records.


</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about activating a plugin, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md)

**Parent Topic:**[Access control](sc-access-control.md)

