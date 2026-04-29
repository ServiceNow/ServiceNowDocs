---
title: Assign roles for Care Team Operations for Biomed
description: Confirm that the correct roles are assigned to users of Care Team Operations for Biomed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up roles and responsibilities in Care Team Operations for Biomed, Configure, Care Team Operations for Biomed, Healthcare Operations, Healthcare and Life Sciences]
---

# Assign roles for Care Team Operations for Biomed

Confirm that the correct roles are assigned to users of Care Team Operations for Biomed.

## Before you begin

Role required: admin

## About this task

Roles control access to features, capabilities, and data in the Care Team Operations for Biomed application.

You can assign roles to individual users or groups. When you apply roles to groups, the members of those groups inherit those roles.

**Note:** User roles can be configured during the initial setup process for healthcare organizations or at any time thereafter as needed.

<table id="table_o1p_2lm_c2c"><tbody><tr><td>

sn\_cto\_biomed.loc\_support\_agent​

</td><td>

Biomed support department agent

</td><td>

Can view/resolve all cases under their assignment group. Tracks and fulfills cases.

 **Note:**If view access to work orders is needed, this role can contain the wm\_read role.

</td></tr><tr><td>

sn\_cto\_biomed.loc\_manager

</td><td>

Biomed support department manager

</td><td>

Moniotors the tasks within their organization.

</td></tr></tbody>
</table>**Example:**

A user who must fulfill work orders created from the Care Team Portal using the Care Team Operations for Biomed plugin must be assigned the sn\_cto\_biomed.loc\_support\_agent role.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** then open a user record.

2.  In the **Roles** related list, select **Edit**.

3.  In the **Collection** list, select the desired roles, and then select **Add**.

4.  Select **Save**.


