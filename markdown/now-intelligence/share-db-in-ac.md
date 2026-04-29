---
title: Share a Platform Analytics dashboard
description: Share a dashboard with other users, groups, or roles to create a shared view of data that you can use to collaborate. You can grant viewing rights or both viewing and editing rights.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [How to share a dashboard, How to share a Platform Analytics dashboard, How to share a Next Experience dashboard]
breadcrumb: [Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Share a Platform Analytics dashboard

Share a dashboard with other users, groups, or roles to create a shared view of data that you can use to collaborate. You can grant viewing rights or both viewing and editing rights.

## Before you begin

Sharing a dashboard 

Role required: You can share any dashboard that you created. You can share dashboards that have been shared with you, if sharing is allowed. If you have the right to edit a dashboard that has been shared with you, you can pass that right along to whomever you share it with. Users with the admin or dashboard\_admin role can share all dashboards.

A role with read access to the Roles \[sys\_user\_role\] table is required to share a dashboard with roles.

**Note:** Data visualizations based on table data are automatically shared with users that you share a dashboard with.

Edit rights granted by sharing a dashboard do not apply to the underlying data visualizations on the dashboard. View rights granted do not apply to that dashboard's visualizations outside of the dashboard itself.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**

2.  Select the dashboard you want to share.

3.  Select the **More actions** button \(![More actions button](../image/icon-vert-3dot-p.png)\) and choose **Share**.

    The Share Dashboard dialog opens.

4.  In the **Grant access to** field, enter the names of one or more users, groups, or roles you want to share the dashboard with.

    To share the dashboard with roles, you need read access to the Roles \[sys\_user\_role\] table.

5.  To allow the people you share the dashboard with to share the dashboard as well, select **Allow recipients to add, edit, or delete sharing permissions associated with this dashboard**.

    When you add a user, group, or role as a viewer, they can only share the dashboard as a viewer. When you add a user, group, or role as an editor, they can share the dashboard as a viewer or as an editor.

    **Important:** The right to share a dashboard or data visualization includes the right to add, edit, and delete sharing rights for any user, group, or role on that dashboard or data visualization. A user cannot use this ability to give themselves or others edit rights if they were not originally given edit rights.

6.  Select one of the following options.

<table id="choicetable_yxb_j15_q5b"><tbody><tr><td id="d35680e166">

**Add as viewer**

</td><td>

Grant only viewing rights to the users, groups, or roles you are sharing the dashboard with. They cannot edit it.

</td></tr><tr><td id="d35680e175">

**Add as editor**

</td><td>

Grant editing rights to the users, groups, or roles you are sharing the dashboard with.You must be in the same application scope as the dashboard to add a user as an editor.

</td></tr></tbody>
</table>7.  Select **Copy link with filter** or **Copy link** to copy the dashboard's URL to the clipboard.

    The URL points to the tab that was open when you opened the **Share dashboard** dialogue. **Copy link with filter** also applies the filters as they're configured on the dashboard or dashboard tab.

8.  Select **Confirm**.


## Result

The roles, groups, and users you have shared the dashboard with appear when you reopen the dialog, along with the rights you have given them.

![Dashboard sharing dialog showing who the dashboard has been shared with and whether they can edit or only view it.](../../par-for-workspace/image/db-share-dialog.png)

**Tip:** The users, groups, and roles with which a dashboard is shared are also visible in the dashboard details. For more information, see [Configure Platform Analytics dashboard details](config-db-in-ac.md).

## What to do next

You can change the rights of whom you have shared the dashboard with in the Share Dashboard dialog, under the Can view/Can edit list for each user, group, or role.

![Rights selector for a user, group, or role that a dashboard was shared with.](../../par-for-workspace/image/db-share-rights-selector.png)

-   **[Dashboard sharing reference qualifiers](../../par-for-workspace/task/share-db-ref-qualifiers.md)**  
Use reference qualifiers to limit the users, groups, and roles in the recipients field of shared dashboards.

**Parent Topic:**[Common dashboard tasks in the in-line editor](../concept/common-dashboard-tasks.md)

**Related topics**  


[Create a dashboard with the in-line editor](create-db-in-ac.md)

[Edit Platform Analytics dashboards](edit-db-in-ac.md)

[Duplicate a Platform Analytics dashboard](../../reporting/task/duplicate-db.md#)

[Print a Platform Analytics dashboard](printer-friendly-db-ac.md)

[Export a Platform Analytics dashboard](export-pae-dashboard-ppt.md)

[Schedule the export of dashboards and data visualizations](../../par-for-workspace/task/schedule-export-dboards-data-viz.md)

[Bookmark a Platform Analytics dashboard](bookmark-dashboard-ac.md)

[Delete a Platform Analytics dashboard](delete-db-in-ac.md)

