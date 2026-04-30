---
title: Assign roles to Healthcare Operations Core users
description: Assign specific roles to give Healthcare Operations Core users visibility into healthcare organizations and the hierarchies they manage.
locale: en-US
release: yokohama
product: Care Team Operations
classification: care-team-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Healthcare Operations Core, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Assign roles to Healthcare Operations Core users

Assign specific roles to give Healthcare Operations Core users visibility into healthcare organizations and the hierarchies they manage.

## Before you begin

Role required: admin

## About this task

Roles control access to features, capabilities, and data in the Healthcare Operations Core application.

You can assign roles to individual users or groups. When you apply roles to groups, the members of those groups inherit those roles.

**Note:** User roles can be configured during the initial setup process for retail organizations or at any time thereafter as needed.

User roles can be configured during the initial setup process for retail organizations or at any time thereafter as needed.

**Example:** You could create a group called “HCO Team Members” and assign the role sn\_hco.care\_team\_member to the group. Then, when importing users, you would associate the users that are care team members with this group.

**Note:** This group doesn’t give them direct access to care team operations – they’ll still need to be associated with a healthcare organization as a member and assigned responsibilities.

For instructions on assigning roles to groups, see [Create a group for all team members in Healthcare Operations Core](hco-create-team-members-group.md)

<table id="table_w3v_gbg_d2c"><tbody><tr><td>

sn\_hco.care\_team\_member

</td><td>

-   sn\_customerservice.service\_organization\_contributor
-   sn\_hcls.foundation\_data\_viewer

</td><td>

Has access to create and view healthcare cases.

</td></tr><tr><td>

sn\_hco.care\_team\_manager

</td><td>

-   sn\_hco.care\_team\_member
-   sn\_customerservice.svc\_location\_manager\_contributor

</td><td>

Has access to create and view healthcare cases

 can add members to the care unit

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  In the **Roles** related list, select **Edit**.

3.  In the **Collection** list, select the desired roles, and then select **Add**.

4.  Select **Save**.


