---
title: Deny by default with empty ACLs \[Updated in Security Center 1.3\]
description: Use the glide.sm.default\_mode property to control the default behavior of security manager when it finds that existing Access Control List \(ACL\) rules are a part of wildcard table ACL rules.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 2
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Deny by default with empty ACLs \[Updated in Security Center 1.3\]

Use the **glide.sm.default\_mode** property to control the default behavior of security manager when it finds that existing Access Control List \(ACL\) rules are a part of wildcard table ACL rules.

Prevent your instance's legacy security manager from allowing access to resources when there are no ACLs defined for that resource, or if there are only wildcard table-level ACLs \(for example, `incident.*`\). When allowed access by default, anything that does not have explicit ACLs set is susceptible to manipulation.

Set the **glide.sm.default\_mode** system property value to **deny** to disallow access when there are no define ACL rules, or there are only wildcard table-level ACLs.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.sm.default\_mode**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Purpose

</td><td>

Best security practice would be to restrict an Access to the tables by an unauthorized user. -   If there are no ACL rules in place for tables, this property ensures that at least wildcard ACLs are validated for any CRUD operation performed on the table/field.
-   These rules restrict the read, write, create, and delete operations on all tables, unless the user has the admin role or meets the requirements of another table ACL rule.

</td></tr><tr><td>

Recommended value

</td><td>

deny

</td></tr><tr><td>

Functional Impact

</td><td>

If you set this property to **Allow**, the wildcard table ACL rules allow CRUD operations on all tables unless there are specific table ACL rules in place to restrict such operations. **Note:** This plugin is not intended for existing instances, as it might modify security access to tables that are already in use in a production environment.

</td></tr><tr><td>

Security risk

</td><td>

6.3

</td></tr><tr><td>

References

</td><td>

[Default deny property](../../security/concept/c_DefaultDenyProperty.md)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

