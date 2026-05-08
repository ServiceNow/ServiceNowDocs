---
title: Share a data visualization in the Visualization Designer
description: Share a visualization to provide view or edit permissions to users, groups, or roles. A user can access a shared visualization in any workspace on the original instance.You can change the access rights of persons with whom the data visualization is shared.Use reference qualifiers to limit the users, groups, and roles in the recipients field of shared visualizations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Share a visualization, Share a report]
breadcrumb: [Share, edit, or delete, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Share a data visualization in the Visualization Designer

Share a visualization to provide view or edit permissions to users, groups, or roles. A user can access a shared visualization in any workspace on the original instance.

## Before you begin

**Important:** The right to share a dashboard or data visualization includes the right to add, edit, and delete sharing rights for any user, group, or role on that dashboard or data visualization. A user cannot use this ability to give themselves or others edit rights if they were not originally given edit rights.

Role required: You can share any data visualization that you created. When you share a data visualization, you can pass along the rights to share that visualization further. You also decide whether to share with editing rights or only viewing rights. If a data visualization has been shared with you with sharing and editing rights, you can also pass along editing rights.

Users with the admin and viz\_admin roles can share all data visualizations. Only users with the admin and viz\_admin roles can share data visualizations with roles.

Sharing a visualization with a user, group, or role adds that visualization to the **Shared with me** tab in the Data Visualizations overview. Any user with a role can list and view any visualization at the table level. Report\_view access control lists \(ACLs\) still apply no matter how the user gets to the visualization, however changes to ACLs can break data visualizations that are used in UI Builder.

Edit rights granted by sharing a data visualization do not apply to that visualization when placed on a dashboard, but only in the Visualization Designer.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or to a workspace with a visualization that you own.

2.  Locate and open the visualization that you want to share.

3.  Expand the More actions menu and select **Share**.

    ![Visualization designer More actions menu showing Share option.](../../par-for-workspace/image/share-data-viz.png)

4.  Enter the names of one or more users, groups, or roles you want to share the data visualization with.

    **Note:**

    -   It is not possible to share data visualizations with inactive users.
    -   Only users with the admin or viz\_admin role see the option to share visualizations with roles.
5.  To allow the people that you share the data visualization with also to share that data visualization, select **Allow recipients to share**.

    When you add a user, group, or role as a viewer, they can only share the visualization as a viewer. When you add a user, group, or role as an editor, they can share the dashboard as a viewer or as an editor.

6.  Select one of the following options.

<table id="choicetable_yxb_j15_q5b"><tbody><tr><td id="d78891e165">

**Add as viewer**

</td><td>

Grant only viewing rights to the users, groups, or roles you share the visualization with. The recipients cannot edit it.

</td></tr><tr><td id="d78891e174">

**Add as editor**

</td><td>

Grant editing rights to the users, groups, or roles you share the visualization with.

</td></tr></tbody>
</table>7.  Select **Confirm**.


**Parent Topic:**[Common data visualization tasks](../concept/common-dv-tasks.md)

## Manage data visualization access

You can change the access rights of persons with whom the data visualization is shared.

### Before you begin

**Important:** The right to share a dashboard or data visualization includes the right to add, edit, and delete sharing rights for any user, group, or role on that dashboard or data visualization. A user cannot use this ability to give themselves or others edit rights if they were not originally given edit rights.

Role required: You can change the access rights to any data visualization that you created, regardless of your role. Users with the admin and viz\_admin roles can change the access rights to all data visualizations. Only users with the admin and viz\_admin roles can change role-related access rights to data visualizations. Any user can view a data visualization by default.

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or to a workspace that has a component based on the Analytics Center template \(![](../../par-for-workspace/image/analytics-center-icon.png)\) and the data visualizations you want to share.

2.  Open the **Data visualizations** tab and select the data visualization whose access you want to manage.

3.  Expand the More actions menu and select **Share**.

    ![Visualization designer More actions menu showing Share option.](../../par-for-workspace/image/share-data-viz.png)

    Under Manage Access, you see a tile for every user, group, or role that the data visualization is shared with.

4.  Filter the user tiles.

    1.  In **Audience type**, limit the tiles that appear to show only users, only groups, or only roles.

    2.  Enter a partial name of a user, group, or role in the search field.

5.  When you locate the desired tile, expand the list of rights and select the rights to grant.

    You can grant editing rights or only viewing rights. You can give or take away the right to share the data visualization. Lastly, you can remove the user, no longer sharing the data visualization with them.![Possible rights you can grant or deny a user to a data visualization that is shared with them.](../../dashboards/image/share-db-ac-manage.png)


## Data visualization sharing reference qualifiers

Use reference qualifiers to limit the users, groups, and roles in the recipients field of shared visualizations.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **System Definition** &gt; **Tables**.

2.  Open the **par\_visualization\_permission** table.

3.  Press Ctrl+Click on the Preview Users button ![info button](../../performance-analytics/image/InfoIcon.png)next to Users on the **Columns** tab to open the Users dictionary entry.

    Point to the Users Column label to see this button.

    ![Preview Users and Preview Groups buttons on the Columns list of Par Notification Email Recipients](../../par-for-workspace/image/preview-buttons-sched-export.png)

4.  If you're in the wrong application, select the link to edit the record.

    ![Mismatched application message with link to edit the record](../../par-for-workspace/image/app-mismatch-msg-sched-export.png)

5.  On the Reference Specification tab of the dictionary entry, use the condition builder to add filter conditions to the User list.

    For example, configure the reference qualifier condition \[Name\] \[starts with\] \[b\]. Only users whose names start with the letter B will show up in the list of users in the recipients list when configuring an export.

6.  Select **Update**.


### What to do next

Perform the same actions on the Group and Role columns to limit sharing with those categories of recipient.

