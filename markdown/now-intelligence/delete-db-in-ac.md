---
title: Delete a Platform Analytics dashboard
description: You can delete a dashboard that is no longer useful. The Analytics Center invokes the Workflow Studio to remove the dashboard from your instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [How to delete a dashboard, How to delete a platform analytics dashboard, How to delete a Next Experience dashboard]
breadcrumb: [Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
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

-   **[Configure dashboard deletion actions in the Workflow Studio](delete-db-in-ac-wf.md)**  
Using the Workflow Studio, you can add actions to the dashboard deletion process. Actions may include sending an email to the dashboard's users or generating an approval request.

**Parent Topic:**[Common dashboard tasks in the in-line editor](../concept/common-dashboard-tasks.md)

**Related topics**  


[Create a dashboard with the in-line editor](create-db-in-ac.md)

[Edit Platform Analytics dashboards](edit-db-in-ac.md)

[Share a Platform Analytics dashboard](share-db-in-ac.md)

[Duplicate a Platform Analytics dashboard](../../reporting/task/duplicate-db.md#)

[Print a Platform Analytics dashboard](printer-friendly-db-ac.md)

[Export a Platform Analytics dashboard](export-pae-dashboard-ppt.md)

[Schedule the export of dashboards and data visualizations](../../par-for-workspace/task/schedule-export-dboards-data-viz.md)

[Bookmark a Platform Analytics dashboard](bookmark-dashboard-ac.md)

