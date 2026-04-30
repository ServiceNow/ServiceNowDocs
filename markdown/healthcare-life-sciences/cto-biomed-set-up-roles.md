---
title: Set up roles for Care Team Operations for Biomed
description: Ensure that the correct roles are assigned to users of Care Team Operations for Biomed.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Care Team Operations for Biomed, Care Team Operations for Biomed, Healthcare Operations, Healthcare and Life Sciences]
---

# Set up roles for Care Team Operations for Biomed

Ensure that the correct roles are assigned to users of Care Team Operations for Biomed.

## Before you begin

Role required: admin

## About this task

Roles control access to features, capabilities, and data in the Care Team Operations for Biomed application.

You can assign roles to individual users or groups. When you apply roles to groups, the members of those groups inherit those roles.

**Note:** User roles can be configured during the initial set up process for healthcare organizations or at any time thereafter as needed.

<table id="table_o1p_2lm_c2c"><tbody><tr><td>

sn\_cto\_biomed.admin​

</td><td>

Biomed Admin

</td><td>

Biomed Admin role for Care team operation

</td></tr><tr><td>

sn\_cto\_biomed.loc\_support\_agent​

</td><td>

Biomed Support Agent

</td><td>

Can view/resolve all cases under their assignment group. Tracks and fulfills cases.

 **Note:**If users need view access to work orders, this role can contain the wm\_read role.

</td></tr><tr><td>

sn\_cto\_biomed.viewer​

</td><td>

Biomed Viewer

</td><td>

Can view Biomed and HCLS foundation data.

 **Note:**If users need view access to work orders, this role can contain the wm\_read role.

</td></tr><tr><td>

sn\_cto\_biomed. loc\_contributor​

</td><td>

​CTO Biomed location contributor role for Nurse, Nurse Assistant

</td><td>

Reports cases, responds to cases,​ tracks cases at business locations, and views cases under their team.

</td></tr></tbody>
</table>**Example:**

A user who must fulfill work orders created from the Care Team Portal using the Care Team Operations for Healthcare Biomed plugin would need to be assigned the sn\_cto\_biomed.loc\_support\_agent​ role.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** then open a user record.

2.  In the **Roles** related list, select **Edit**.

3.  In the **Collection** list, select the desired roles, and then select **Add**.

4.  Select **Save**.


