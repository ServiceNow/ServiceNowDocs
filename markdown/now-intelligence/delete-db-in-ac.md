---
title: Delete a Platform Analytics dashboard
description: You can delete a dashboard that is no longer useful. The Analytics Center invokes the Workflow Studio to remove the dashboard from your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/now-intelligence/delete-db-in-ac.html
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

**Note:** The steps to delete a Core UI responsive dashboard are different. For more information, see [Manage responsive dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/now-intelligence/performance-analytics/manage-responsive-dashboards.md).

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Dashboards**.

2.  Open the dashboard that you want to delete.

3.  From the More actions menu \(\[Omitted image "icon-vert-3dot-p.png"\] Alt text: More actions menu icon\), select **Delete**.

    \[Omitted image "delete-plat-admin-db.png"\] Alt text: Dashboard with More actions menu expanded and the Delete option highlighted

4.  Confirm the deletion.

    You can’t undo this action. If you accidentally delete a dashboard associated with a plugin, a system administrator can restore the original version of the dashboard.

    1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.
    2.  Find the plugin using the filter criteria and search bar.
    3.  Select the More actions menu button \[Omitted image "icon-vert-3dot-p.png"\] Alt text: More actions menu icon and choose **Repair**.
    4.  Select **Repair** in the Activate Plugin window.

