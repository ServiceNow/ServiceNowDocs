---
title: Manage HR Groups
description: HR Groups are a set of users with common job skills.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage HR roles, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Manage HR Groups

HR Groups are a set of users with common job skills.

## Before you begin

Role required: sn\_hr\_core.admin, user\_admin

You can have multiple levels of groups. For example, HR is a group that contains all HR employees within your company. You can have subgroups under HR such as HR Benefits, Employee Relations, and more.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Manage Roles** &gt; **Manage HR Groups**.

2.  From the **Groups** list, click **New** or select an existing HR group.

    The **Group** form appears.

<table id="table_jst_j1g_jr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name that describes the group.

</td></tr><tr><td>

Manager

</td><td>

Click the **Lookup using list** icon and select the person responsible for this group.

</td></tr><tr><td>

Type

</td><td>

Use to define a category a group belongs to. A group can be associated with one group type \(narrow scope\) or multiple group types \(expanded scope\). This allows you to ensure qualified agents are assigned to complex cases or you have adequate coverage for less complex cases.

 Click the **Unlock Type** ![Unlock Type icon](../image/icon-hr-unlock-add-parties.png) icon. Then click the **Lookup using list** ![Lookup using list icon](../image/magnifying-glass.png) icon and add **human\_resources**.

</td></tr><tr><td>

Group email

</td><td>

Enter the email address of the group. This email acts as a group notification that sends an email to every member of the group.

</td></tr><tr><td>

Parent

</td><td>

Click the **Lookup using list** icon and select the HR group that is above the current group.

</td></tr><tr><td>

Vendors

</td><td>

Vendors that the group is responsible for.

</td></tr><tr><td>

Description

</td><td>

A description of the group.

</td></tr></tbody>
</table>3.  Click **Save** and a series of tabs appear at the bottom of the form.

<table id="table_rxw_xww_mx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Roles

</td><td>

Click **Edit** and from the **Edit Members** form, move the roles from the **Collection** column to the **Roles List** column.Adding a role to a group means that all group members also have that role.

**Note:** Roles associated with the parent group are automatically assigned.

</td></tr><tr><td>

Group Members

</td><td>

Click **Edit** to add users to the group. Click **New** to create a user and add it to the group.

</td></tr><tr><td>

Groups

</td><td>

Click **New** to create a new group.**Note:** Creating a group from here does not automatically create a child group under the group you have displayed.

</td></tr><tr><td>

Skills

</td><td>

Click **New** to create a new skill. Click **Edit** and the **Edit Members** form appears. Move skills from the **Collection** column to the **Skills List**. Click **Save** when done.

**Note:** Skills associated with the parent group are automatically assigned.

</td></tr><tr><td>

Activities

</td><td>

This field only appears for the Lifecycle Events application. The HR Service Activities the group manages. The HR Service Activities are part of the Activity Set and together make up a Lifecycle Event. Only members of this group can update this HR Service Activity.

Refer to [Configure a lifecycle event activity](configure-hr-lifecycle-event-activity.md#).

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


**Parent Topic:**[Manage HR roles](../concept/c_ManageRoles.md)

