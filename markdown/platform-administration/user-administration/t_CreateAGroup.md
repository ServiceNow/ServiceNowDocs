---
title: Create a user group
description: Create groups and assign roles to them. Users assigned to the group inherit the roles.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Creating groups, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a user group

Create groups and assign roles to them. Users assigned to the group inherit the roles.

## Before you begin

Role required: user\_admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Select **New**.

3.  On the form, fill in the fields.

    Some fields appear after personalizing the form. Personalize a form.

<table id="table_flh_qwv_sbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the group.

</td></tr><tr><td>

Manager

</td><td>

Group manager or lead.

</td></tr><tr><td>

Type

</td><td>

Category for this group. For example, a group designated as type **catalog** is a service catalog group and can also be accessed under the **Service Catalog** &gt; **Catalog Policy** &gt; **Fulfillment Groups** module. See [Configure assignment group types](../concept/c_ConfigGroupTypesForAssignGroups.md#) for more information.You may need to Personalize a form to add the **Type** field. Activating the Work Management plugin adds the **Type** field automatically.

**Note:** ITIL is added for groups with an empty group type. Also, the default reference qualifier for tasks enables these groups to assign tasks and other task types to the group.

</td></tr><tr><td>

Group email

</td><td>

Group email distribution list or the email address of the point of contact, such as the group manager.

</td></tr><tr><td>

Parent

</td><td>

Other group of which this group is a member. If a group has a parent, the child group inherits the roles of the parent group. The members of the child group aren’t members of the parent group. For example, if an incident is assigned to the parent group and you select the **Assigned to** lookup icon, only the members in the parent group are available. The members of the child group aren’t available.

</td></tr><tr><td>

Active

</td><td>

Check box that indicates whether the group is active or inactive. Inactive groups still appear in any reference field that already references the group, but aren’t visible by non-admin users in:-   lists of groups
-   the reference lookup list for reference fields
-   the auto-complete list of groups displayed when you type into a reference field


</td></tr><tr><td>

Exclude manager

</td><td>

Check box that controls whether the group manager receives email notifications.

</td></tr><tr><td>

Include members

</td><td>

Check box that controls whether the group members receive individual emails when someone sends an email to the **Group Email** address. The only exception to this functionality is for approval notifications, whereby all members of a group receive an approval notification, regardless of the **Include members** selection. See Receive notifications for more information.

</td></tr><tr><td>

Description

</td><td>

Helpful information about the group.

</td></tr></tbody>
</table>4.  Remove or hide a group.

    1.  **Note:** Only users in the hidden group are able to see the hidden group when selecting a group in a reference field.

        Create a true/false field labeled `Hidden` on the Group form.

        For more information on creating fields, see [Add and customize a field in a table](../../field-administration/task/t_CreatingNewFields.md)

        The system creates a field called **u\_hidden** on the **Users \[sys\_user\_group\]** table and enables use of the **Hidden** check box to designate a hidden group.

    2.  Create a new before query business rule on the \[sys\_user\_group\] \(Group\) table with the following script:

        ```
        if (!gs.hasRole("admin") && !gs.hasRole("groups_admin") && gs.getSession().isInteractive()) { 
          var qc = current.addQuery("u_hidden", "!=", "true"); //cannot see hidden groups... 
          qc.addOrCondition("sys_id", "javascript:getMyGroups()"); //...unless in the hidden group 
        }
        ```

        **Note:** For more information, see Before Query business rules.


## Result

The user group is created based on the configuration that you've provided.

**Note:**

When `glide.ui.schedule_job_for_group_parent_change` is set to true, removing a parent group results in the roles of the parent group being added to the child group asynchronously. If `glide.ui.schedule_job_for_group_parent_change` is set to false, the roles of the parent group are added to the child group synchronously when the parent group is removed.

**Parent Topic:**[Creating groups](../../roles/concept/ua-creating-groups.md)

