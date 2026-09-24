---
title: Enforce field-level ACLs on records created from the filtered list view UI query string
description: Use a system property to prevent list filters from affecting the initial values of created records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enforce-field-level-acls-on.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce field-level ACLs on records created from the filtered list view UI query string

Use a system property to prevent list filters from affecting the initial values of created records.

Use the **com.glide.acl\_check\_all\_filter\_on\_new** system property to confirm field level ACLs are evaluated when query string parameters are applied during the creation of new table records triggered from the UI.

How filter query strings work:

When a new record is created from the list view UI, field values from the filter query string are applied to it.

For example, using this filter:

```
author={62826bf03710200044e0bfc8bcbe5df1}^state={3}
```

The **Author** field is assigned the value `62826bf03710200044e0bfc8bcbe5df1` and **State** is assigned the value `3`, regardless of their default value.

The **com.glide.acl\_check\_all\_filter\_on\_new** property verifies that field level ACLs are evaluated for all fields when a record is created from the filtered list view UI of a table.

However, exceptions are applied in the following order:

1.  If the **ignore\_filter\_on\_new** dictionary attribute is set for a field, the value of that field is never used during record creation from the filtered list view.
2.  If the **acl\_check\_filter\_on\_new** dictionary attribute is set for a field, ACLs must be checked for that field during record creation from the filtered list view.
3.  If the **allow\_filter\_on\_new** dictionary attribute is set for a field, ACLs aren't checked for that field during record creation from the filtered list view.
4.  The **sys\_domain** field and other domain fields defined by the **glide.sys.domain.domain\_determining\_field.\{table\_name\}** property aren't checked by ACLs on record creation from the filtered list view.
5.  If the **com.glide.acl\_check\_all\_filter\_on\_new** system property is set to `true`, ACLs must be checked for all other fields during record creation from the filtered list.
6.  If a field's type is listed in the **com.glide.ignore\_filter\_on\_new.field\_types** system property, ACLs must be checked for that field on record creation from the filtered list view.

Confirm that the **com.glide.acl\_check\_all\_filter\_on\_new** system property is set to `true`.

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

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.8
-   CVSS score: Medium
-   Security risk details: When **com.glide.acl\_check\_all\_filter\_on\_new** is set to `false`, then ACLs aren't checked for fields on new record creation from the filtered list view UI of a table, unless one of the other exceptions applies. In this state, users without create access to fields can bypass ACLs by setting protected fields through filter query strings during record creation. This allows protected fields to be set to improper values on record creation through the filtered list view UI of a table.

</td></tr><tr><td>

Functional impact

</td><td>

When **com.glide.acl\_check\_all\_filter\_on\_new** is set to `true`, ACLs are enforced for fields included in the filter query string during record creation from the list view UI. This prevents users without create access from modifying protected fields through filter parameters.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

