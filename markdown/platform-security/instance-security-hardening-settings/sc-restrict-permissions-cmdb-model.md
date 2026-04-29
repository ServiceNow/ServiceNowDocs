---
title: Restrict permissions for CMDB model
description: Use the csm\_cmdb\_model.customer\_visible\_flag system property to limit customer access to data in the Product Models table as an additional access control to the CMDB model.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict permissions for CMDB model

Use the **csm\_cmdb\_model.customer\_visible\_flag** system property to limit customer access to data in the Product Models table as an additional access control to the CMDB model.

The **csm\_cmdb\_model.customer\_visible\_flag** system property is an additional access control to the CMDB model. If **csm\_cmdb\_model.customer\_visible\_flag** is not set to the recommended value of **true**, then any user with the sn\_esm\_user role and out of the box ACLs will have permissions to the CMDB model. Note that this role tends to be granted to external users.

Ensure that the property **csm\_cmdb\_model.customer\_visible\_flag** is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**csm\_cmdb\_model.customer\_visible\_flag**

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

-   Severity score: 6.5
-   CVSS rating: Medium
-   Security risk details: External users could unwillingly be given permissions to the CMDB model.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

