---
title: Audit user roles
description: Changes to user roles are automatically tracked in the Audit Roles \[sys\_audit\_role\] table.
locale: en-US
release: zurich
product: User Administration
classification: user-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing roles, User admin, Configure core features, Administer]
---

# Audit user roles

Changes to user roles are automatically tracked in the Audit Roles \[sys\_audit\_role\] table.

## Before you begin

Role required: admin

**Note:** If the [Prevent duplicate entries with Contextual Security: Role Management V2](https://www.servicenow.com/docs/access?context=Role-Mgmt-V2&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) plugin is installed, you must [Enable role auditing with Contextual Security: Role Management V2](https://www.servicenow.com/docs/access?context=enable-audit-roles&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Procedure

1.  Navigate to **All**, and then enter `sys_audit_role.list` in the filter.

    The Audit Roles \[sys\_audit\_role\] table displays changes to user roles.

<table id="table_wr1_tsh_4z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Changed by

</td><td>

The user who made the change.

</td></tr><tr><td>

Count after change

</td><td>

Direct role added as a result of the change \(if any\), plus the number of inherited roles added.

</td></tr><tr><td>

Granted by group

</td><td>

If the role was inherited, the group that the role was inherited from.

</td></tr><tr><td>

Operation

</td><td>

The type of change. Values include:

 -   Added
-   Removed


</td></tr><tr><td>

Role

</td><td>

The affected role.

</td></tr><tr><td>

User

</td><td>

The affected user.

</td></tr></tbody>
</table>
**Parent Topic:**[Managing roles](../concept/ua-creating-roles.md)

