---
title: Set up roles for Care Team Operations for Facilities
description: Confirm that the appropriate roles are assigned to users of Care Team Operations for Facilities.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up roles and responsibilities in Care Team Operations for Facilities, Configure, Care Team Operations for Facilities, Healthcare Operations, Healthcare and Life Sciences]
---

# Set up roles for Care Team Operations for Facilities

Confirm that the appropriate roles are assigned to users of Care Team Operations for Facilities.

## Before you begin

Role required: admin

## About this task

Roles control access to features, capabilities, and data in the Care Team Operations for Facilities application.

You can assign roles to individual users or groups. When you apply roles to groups, the members of those groups inherit those roles.

**Note:** User roles can be configured during the initial setup process for healthcare organizations. or at any time thereafter as needed.

<table id="table_o1p_2lm_c2c"><tbody><tr><td>

sn\_cto\_facilities.viewer​

</td><td>

Facilities case viewer

</td><td>

Can view Healthcare Facilities cases and all HCLS foundation data.

 **Note:**If view access to work orders is needed, this role can contain the wm\_read role.

</td></tr></tbody>
</table>**Example:**

A user who must fulfill work orders created from the Care Team Portal using Care Team Operations for Facilities should be assigned the sn\_cto\_facilities.loc\_support\_agent role.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** then open a user record.

2.  In the **Roles** related list, select **Edit**.

3.  In the **Collection** list, select the desired roles, and then select **Add**.

4.  Select **Save**.


