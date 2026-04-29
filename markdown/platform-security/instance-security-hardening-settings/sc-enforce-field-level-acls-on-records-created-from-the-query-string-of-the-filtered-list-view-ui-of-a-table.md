---
title: Enforce field-level ACLs on records created from the query string of the Filtered List view UI of a table
description: Use a system property to prevent list filters from affecting the initial values of created records.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce field-level ACLs on records created from the query string of the Filtered List view UI of a table

Use a system property to prevent list filters from affecting the initial values of created records.

Use the **com.glide.acl\_check\_all\_filter\_on\_new** system property to ensure field level ACLs are evaluated when query string parameters are applied during the creation of new table records triggered from the UI.

When a new record is created from the list view UI of a table, the field values included in the filter query string are applied to the new record.

For example, using this filter:

```
author={62826bf03710200044e0bfc8bcbe5df1}^state={3}
```

The **Author** field is assigned the value `62826bf03710200044e0bfc8bcbe5df1` and **State** is assigned the value `3`, regardless of their default value. The **com.glide.acl\_check\_all\_filter\_on\_new** property ensures that field level ACLs are evaluated for all fields when a record is created from the filtered list view UI of a table. There are exceptions to this property, which are applied in the following order:

1.  If the **ignore\_filter\_on\_new** dictionary attribute is set for a field, then the value of that field in a filter query string is never used in record creation from the filtered list view UI of a table.
2.  If the **acl\_check\_filter\_on\_new** dictionary attribute is set for a field, then ACLs must be checked for that field on record creation from the filtered list view UI of a table.
3.  If the **allow\_filter\_on\_new** dictionary attribute is set for a field, then ACLs aren't checked for that field on record creation from the filtered list view UI of a table.
4.  The **sys\_domain** field and other domain fields specific to a table and defined by the **glide.sys.domain.domain\_determining\_field.\{table\_name\}** property aren't checked by ACLs on record creation from the filtered list view UI of a table.
5.  If the **com.glide.acl\_check\_all\_filter\_on\_new** system property is set to `true`, then ACLs must be checked for all other fields on record creation from the filtered list view UI of a table.
6.  If a field's type is listed in the **com.glide.ignore\_filter\_on\_new.field\_types** system property, then ACLs must be checked for that field on record creation from the filtered list view UI of a table.

Ensure that the **com.glide.acl\_check\_all\_filter\_on\_new** system property is set to `true`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.acl\_check\_all\_filter\_on\_new**

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

false

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

-   Severity score: 4.8
-   CVSS score: Medium
-   Security risk details: When **com.glide.acl\_check\_all\_filter\_on\_new** is set to `false`, then ACLs aren't checked for fields on new record creation from the filtered list view UI of a table, unless one of the other exceptions applies. In such a situation, ACLs can be bypassed by users without create access to fields. This allows protected fields to be set to improper values on record creation through the filtered list view UI of a table.

</td></tr><tr><td>

Functional impact

</td><td>

When **com.glide.acl\_check\_all\_filter\_on\_new** is set to `true`, then ACLs may prevent fields included in the filter query string from affecting the value of fields in a created record when the creation is triggered from the list view UI of a table. However, this previous behavior was incorrect as it bypassed ACLs and allowed user without creation access to a field to modify its value.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)

