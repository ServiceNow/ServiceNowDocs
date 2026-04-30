---
title: Block access for delegated developers
description: This configuration affects access for delegated developers that are updating user roles through script. When the configuration is compliant, the developer will not be able to update or insert records into the sys\_user\_has\_role table without also having the user\_admin role.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Block access for delegated developers

This configuration affects access for delegated developers that are updating user roles through script. When the configuration is compliant, the developer will not be able to update or insert records into the sys\_user\_has\_role table without also having the user\_admin role.

The value of this property affects whether a delegated developer is allowed to grant or receive unexpected access to functionality in the instance. When the property contains roles, only those roles may execute script modules.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**com.glide.sys.security.delegateddev.block\_grant\_roles**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

The value of this property affects whether a delegated developer is allowed to grant or receive unexpected access to functionality in the instance.

</td></tr><tr><td>

Type

</td><td>

toggle switch

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Security Dependencies

</td><td>

none

</td></tr><tr><td>

Security risk rating

</td><td>

6.7

</td></tr><tr><td>

Functional impact

</td><td>

When a user with the delegated\_developer role is attempting to modify a record in the sys\_user\_has\_role table, this property enables additional security checks against the operation. The additional security checks validate that the user has been granted the user\_admin role if they're trying to create or update the sys\_user\_has\_role table. If they do not have the user\_admin role, the access will be denied. When the property is false, these additional checks are not validated.

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) Without appropriate authorization, unauthorized users may access sensitive content/data on the instance.

</td></tr><tr><td>

References

</td><td>

[Access control](sc-access-control.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

