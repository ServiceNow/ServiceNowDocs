---
title: Set up roles for Care Team Operations for Healthcare IT
description: Ensure that the correct roles are assigned to users of Care Team Operations for Healthcare IT.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Care Team Operations for Healthcare IT, Care Team Operations for Healthcare IT, Healthcare Operations, Healthcare and Life Sciences]
---

# Set up roles for Care Team Operations for Healthcare IT

Ensure that the correct roles are assigned to users of Care Team Operations for Healthcare IT.

## Before you begin

Role required: admin

## About this task

Roles control access to features, capabilities, and data in the Care Team Operations application.

You can assign roles to individual users or groups. When you apply roles to groups, the members of those groups inherit those roles.

**Note:** User roles can be configured during the initial set up process for healthcare organizations or at any time thereafter as needed.

**Roles installed with Care Team Operations for Healthcare IT**

<table id="table_o3r_btl_c2c"><tbody><tr><td>

sn\_cto\_hcit.admin

</td><td>

IT Admin

</td><td>

IT Admin role for Care Team Operations for Healthcare IT.

</td></tr><tr><td>

sn\_cto\_hcit.loc\_support\_agent

</td><td>

IT Support Agent

</td><td>

Views/resolves all cases under their assignment group. Tracks and fulfills cases.

</td></tr><tr><td>

sn\_cto\_hcit.viewer

</td><td>

IT Viewer

</td><td>

Views all IT and HCLS foundation data.

 **Note:**If users need access to incidents, the sn\_incident\_read role can be added to this role.

</td></tr><tr><td>

sn\_cto\_hcit.loc\_contributor

</td><td>

CTO IT location contributor role for Nurse, Nurse Assistant

</td><td>

Reports cases, respond to cases, track cases at business location, views cases under their team.

</td></tr></tbody>
</table>**Example:**

A user who needs to fulfill incidents created from the Care Team Portal using the Care Team Operations for Healthcare IT plugin would need to be assigned the sn\_cto\_hcit.loc\_support\_agent role.

**Note:** After installing Care Team Operations for Healthcare IT, the sn\_hco.care\_team\_member role installed with Healthcare Operations Core will contain the sn\_cto\_hcit.loc\_contributor role automatically.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  In the **Roles** related list, select **Edit**.

3.  In the **Collection** list, select the desired roles, and then select **Add**.

4.  Select **Save**.


