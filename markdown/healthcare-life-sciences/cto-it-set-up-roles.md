---
title: Assign roles to Care Team Operations for Healthcare IT users
description: Ensure that the correct roles are assigned to users of Care Team Operations for Healthcare IT.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up roles and responsibilities in Care Team Operations for Healthcare IT, Configure, Care Team Operations for Healthcare IT, Healthcare Operations, Healthcare and Life Sciences]
---

# Assign roles to Care Team Operations for Healthcare IT users

Ensure that the correct roles are assigned to users of Care Team Operations for Healthcare IT.

## Before you begin

Role required: admin

## About this task

Roles control access to features, capabilities, and data in the Care Team Operations application.

You can assign roles to individual users or groups. When you apply roles to groups, the members of those groups inherit those roles.

**Note:** User roles can be configured during the initial set up process for healthcare organizations or at any time thereafter as needed.

**Roles installed with Care Team Operations for Healthcare IT**

<table id="table_o3r_btl_c2c"><tbody><tr><td>

sn\_cto\_hcit.loc\_support\_agent

</td><td>

IT Support Agent

</td><td>

Views/resolves all cases under their assignment group. Tracks and fulfills cases.

</td></tr><tr><td>

sn\_cto\_hcit.loc\_manager

</td><td>

Healthcare IT services support department manager

</td><td>

Monitors the tasks within their organizations.

</td></tr></tbody>
</table>**Example:**

A user who needs to fulfill incidents created from the Care Team Portal using the Care Team Operations for Healthcare IT plugin would need to be assigned the sn\_cto\_hcit.loc\_support\_agent role.

**Note:** After installing Care Team Operations for Healthcare IT, the sn\_hco.care\_team\_member role installed with Healthcare Operations Core will contain the sn\_cto\_hcit.loc\_contributor role automatically.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  In the **Roles** related list, select **Edit**.

3.  In the **Collection** list, select the desired roles, and then select **Add**.

4.  Select **Save**.


