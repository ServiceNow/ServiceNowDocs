---
title: Configure role-based multi-factor criteria
description: Use role based multi-factor criteria to enforce Multi-factor authentication for all users assigned to specific roles.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MFA criteria, Configuring MFA, Multi-factor authentication, Authentication, Access Management]
---

# Configure role-based multi-factor criteria

Use role based multi-factor criteria to enforce Multi-factor authentication for all users assigned to specific roles.

## Before you begin

Role required: adaptive\_auth\_admin

## Procedure

1.  Navigate to **All** &gt; **Multi-factor Authentication** &gt; **Multi-factor Criteria**.

2.  In the **Multi-factor Criteria** list, open the **Role-based multi-factor authentication** record.

3.  Use the **Multi-factor Roles** list to add or remove roles.

<table id="choicetable_w45_gnx_bpb"><tbody><tr><td id="d32498e85">

**Add a role**

</td><td>

Double-click **Insert a new row...** and enter or select a role name. Click the **Save Icon** \(![Save icon](../images/save-icon.png)\) to save the entry.

</td></tr><tr><td id="d32498e106">

**Remove a role**

</td><td>

Click the delete icon \(![delete icon](../images/delete-icon.png)\) to remove a role from the list.

</td></tr></tbody>
</table>4.  Click **Update**.


## Result

Your instance enforces multi-factor authentication for all users who are members of the roles listed in the **Multi-factor Roles** list.

**Important:** The record must be active to enforce role-based multi-factor authentication.

