---
title: ACL control of function fields
description: When evaluating access to a function field, in addition to checking access to the function field itself, the system also checks access to the function's contributing fields. Contributing fields are those used as the arguments in a given function definition.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore Access Control Lists, Access Control List Rules, Access Management]
---

# ACL control of function fields

When evaluating access to a function field, in addition to checking access to the function field itself, the system also checks access to the function's contributing fields. Contributing fields are those used as the arguments in a given function definition.

For more information about function fields, see [Function field](https://www.servicenow.com/docs/access?context=platform-support-functions&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

In Rome and earlier, the system simply checks access to the function field itself \(as with any other field\). If the ACLs on that field allow access, the user receives the resulting value, regardless of whether the user has access to the contributing fields.

In Australia and later, the system also requires access to all contributing fields in order to allow access to the function field. If one or more of the contributing field ACLs refuse access, the function field also refuses access.

The only operations affected by the new requirement are read and report\_view. Report\_view has its own additional requirements.

<table id="table_ush_tqq_nnb"><thead><tr><th>

Operation

</th><th>

Description

</th></tr></thead><tbody><tr><td>

read operation

</td><td>

A user has read access to a function field only if both of the following are true:-   The user has read access to the function field.
-   The user has read access to all of the contributing fields used in the function.

</td></tr><tr><td>

report\_view operation

</td><td>

A user has report\_view access to a function field only if all of the following are true:-   The user has report\_view access to the function field.
-   The user has report\_view access to each of the contributing fields.
-   There is a role-only read ACL without conditions and without a script, and the user has that role.
-   The user has role-only read access to the contributing fields, such that only ACLs without condition or script can allow.

</td></tr></tbody>
</table>## Examples

Given:

-   Table: salary
-   Columns: base, bonus, total \(all are Integers in this example\)
-   Function field: The total column is marked as a function field, with function definition `glidefunction:add(base, bonus)`.
-   Contributing fields: base and bonus, since they're used in the function definition
-   Roles: salary\_admin, bonus\_admin

|ACLs|Result|
|----|------|
|total, base, bonus: read and report\_view for role salary\_admin, with no conditions or scripts|A user with the salary\_admin role is granted read and report\_view access to total because they have the required role.|

<table id="table_hbj_4vq_nnb"><thead><tr><th>

ACLs

</th><th>

Result

</th></tr></thead><tbody><tr><td>

-   total, base: read and report\_view for role salary\_admin, with no conditions or scripts
-   bonus: report\_view for role salary\_admin , with no conditions or scripts
-   bonus: read for role bonus\_admin, with no conditions or scripts

</td><td>

A user with the salary\_admin role is refused read and report\_view access to total, because bonus refuses read access to their role.

</td></tr></tbody>
</table><table id="table_abn_xvq_nnb"><thead><tr><th>

ACLs

</th><th>

Result

</th></tr></thead><tbody><tr><td>

-   total, base: read and report\_view for role salary\_admin, with no conditions or scripts
-   bonus: report\_view for role bonus\_admin, with no conditions or scripts
-   bonus: read for role salary\_admin, with a script \(note that it doesn't matter what's in the script, only that it's there\)

</td><td>

A user with the salary\_admin role is granted read access to total, because they have the required role for all fields.But the same user with the salary\_admin is refused report\_view access, because the read ACL with the script refuses access by default for this case, even though they have the required role.

</td></tr></tbody>
</table>