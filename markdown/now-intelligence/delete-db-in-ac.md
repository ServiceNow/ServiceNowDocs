---
title: Delete a Platform Analytics dashboard
description: You can delete a dashboard that is no longer useful. The Analytics Center invokes the Workflow Studio to remove the dashboard from your instance.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-09-27"
reading_time_minutes: 1
keywords: [How to delete a dashboard, How to delete a platform analytics dashboard, How to delete a Next Experience dashboard]
breadcrumb: [Dashboards in Platform Analytics, Platform Analytics experience, Platform Analytics]
---

# Delete a Platform Analytics dashboard

You can delete a dashboard that is no longer useful. The Analytics Center invokes the Workflow Studio to remove the dashboard from your instance.

## Before you begin

Inform any users who can view the dashboard that you’re deleting it. Users who have bookmarked a deleted dashboard see an error when they try to access it.

Role required: You can delete any dashboard that you created. Users with the admin or dashboard\_admin role can delete any dashboard.

**Note:** The steps to delete a Core UI responsive dashboard are different. For more information, see [Manage responsive dashboards](manage-responsive-dashboards.md#).

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Dashboards**.

2.  Open the dashboard that you want to delete.

3.  From the More actions menu \(![More actions menu icon](../image/icon-vert-3dot-p.png)\), select **Delete**.

    ![Dashboard with More actions menu expanded and the Delete option highlighted](../image/delete-plat-admin-db.png)

4.  Confirm the deletion.

    You can’t undo this action. If you accidentally delete a dashboard associated with a plugin, a system administrator can restore the original version of the dashboard.

    1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.
    2.  Find the plugin using the filter criteria and search bar.
    3.  Select the More actions menu button ![More actions menu icon](../image/icon-vert-3dot-p.png) and choose **Repair**.
    4.  Select **Repair** in the Activate Plugin window.

